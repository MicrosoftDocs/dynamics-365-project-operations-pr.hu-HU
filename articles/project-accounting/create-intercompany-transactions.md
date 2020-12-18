---
title: Vállalatközi tranzakciók létrehozása
description: Ez a témakör a vállalatközi tranzakciók létrehozásával kapcsolatban tartalmaz tájékoztatást.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595489"
---
# <a name="create-intercompany-transactions"></a>Vállalatközi tranzakciók létrehozása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A vállalatközi tranzakciók egy projektszerződésből származó idő-és költség-tranzakciók, amelyek egy vállalathoz vagy szervezeti egységhez tartoznak, miközben a projektszerződésben szereplő erőforrások egy másik vállalat vagy szervezeti egység részét képezik.

A vállalatközi tranzakciók jóváhagyásakor a rendszer a következő tényleges tranzakciókat hozza létre

| **Tranzakció típusa** | **Alkalmazott árlista** | **Tranzakció pénzneme** |
| --- | --- | --- |
| Költség | A szerződő egység önköltségi árlistája | Az ár sorban szereplő pénznem |
| Számlázatlan értékesítések. Ezek csak a számlázási típussal, időponttal és anyaggal rendelkező szerződéssorhoz tartozó tényleges adatokhoz jönnek létre. | Szerződéses projekt projektárlistája | Szerződés pénzneme |
| Erőforrás-kezelő részleg költsége | Az erőforrás-kezelő egység önköltségi árlistája | Az ár sorban szereplő pénznem |
| Szervezetek közötti értékesítések | A szerződő egység önköltségi árlistája | Az ár sorban szereplő pénznem |

A költségek, a beszerzési egységárak és a szervezeti egységek közötti értékesítési tranzakciók ára és pénzneme a **szervezeti egység** által vezérelt. Fontos ezt figyelembe venni, amikor eldönti, hogyan kell felépíteni a vállalatokat és a szervezeti egységeket a megvalósításban.

A lehetőség, az ajánlat, a projekt szerződés és a projekt rekordjainak létrehozásakor a rendszer ellenőrzi, hogy a szerződő egység pénzneme megegyezik-e a szerződő vállalat pénzügyi pénznemével. Ha nem egyeznek meg, akkor ezek a rekordok nem hozhatók létre. A szervezeti egység pénznemét Dynamics 365 Project Operations szolgáltatásban lehet meghatározni a **Dataverse** > **Beállítások** > **Szervezeti egységek** helyen. A vállalat könyvelési pénzneme Dynamics 365 Finance van megadva az **Általános főkönyv** > **Főkönyv beállítása** > **Főkönyv** helyen. A pénznemet a rendszer a Dataverse-környezetébe a főköny kettős írású leképezésével szinkronizálja.

A rendszer a következő helyzetekben hozza létre az erőforráskezelés költségeket és a szervezeti egység közötti valós értékesítéseket:

  - Ha a beszerzési egység eltér a szerződő egységtől
  - Ha a beszerzési vállalat eltér a szerződő vállalattól

Azonban csak olyan tranzakciók kerülnek át a Dynamics 365 Finance környezetbe további könyvelésre, ahol a beszerzési vállalat eltér a szerződő vállalattól.

A projektek tényleges adatainak könyvelése a Project Operations integrációs naplójában van rögzítve a Finance-ban. A rendszer a következő naplósorokat hozza létre.

| **Tranzakció típusa** | **Jogi személy** | **Project-tranzakciót hoz létre könyveléskor** | **A pénzügyi dimenzió alapértelmezetten innen** | **Alapértelmezett számlázási áfacsoport és a Számlázási cikk áfacsoport** |
| --- | --- | --- | --- | --- |
| Költség | Nem lesz hozzáadva az integrációs naplóhoz | N. a. | N. a. | N. a. |
| Számlázatlan értékesítés | A kölcsönvevő jogi személy integrációs naplója | Igen | Project | **Számlázási áfacsoport**: a **szerződéses ügyfél** alapján <br/> **Számlázási cikk áfacsoportja:** A naplósor aktuális, jogi személyből származó projekt kategóriája |
| Erőforrás-kezelő részleg költsége | A kölcsönző jogi személy integrációs naplója | No | Vállalatközi ügyfél | **Számlázási áfacsoport**: a **vállalatközi ügyfél** alapján <br/> **Számlázási cikk áfacsoportja:** A naplósor aktuális, jogi személyből származó projekt kategóriája |
| Vállalatközi értékesítések | A kölcsönző jogi személy integrációs naplója | No | Vállalatközi ügyfél | **Számlázási áfacsoport**: a **vállalatközi ügyfél** alapján <br/> **Számlázási cikk áfacsoportja:** A naplósor aktuális, jogi személyből származó projekt kategóriája |

### <a name="example-intercompany-transactions"></a>Példa: vállalatközi tranzakciók

Molly Clark, az GBPM-ben foglalkoztatott fejlesztő 10 órányi munkát végzett a USPM Adventure Works-projekten, amelyet a projektvezető hagy jóvá. A fejlesztői költség GBPM-ben 88 GBP/óra. A GBPM a USPM felé 120 USD-t számlát egy fejlesztői óráért. A USPM 200 dollárt számláz az Adventure Works felé a GBPM-erőforrás által végzett munkával kapcsolatosan. További információkért lásd: [Vállalatközi számlázás konfigurálása](configure-intercompany-invoicing.md).

1. A Project Operations alkalmazásban nyissa meg az **Erőforrások** lehetőséget és válassza **Molly Clarkot** a listából. Az **Ütemezés** lap **Vállalat** mezőjében válassza a **GBPM** lehetőséget.
2. Nyissa meg az **Értékesítési** > **Ügyfelek** lehetőséget, és új ügyfélbejegyzés létrehozásához válassza az **Új** lehetőséget a Kalandorbolt számára.
    1. Állítsa a vállalatot **USPM** értékre.
    2. A **Kapcsolat típusát** állítsa **Ügyfél** értékre.
    3. Válassza a **10. vevőcsoport – belföldi** lehetőséget.
    4. Állítsa pénznemet **USD-re**.
    5. Mentse a bejegyzést.
3. Nyissa meg a **Sales** > **Projektszerződések** lehetőséget, és hozzon létre egy új projekt szerződést az Adventure Works számára.
    1. Állítsa be a tulajdonos vállalatot **USPM** értékre, és a szerződő egységet a **Contoso Robotics US** értékre.
    2. Válassza az Adventure Workst ügyfélként.
    3. Válasszon egy termékárlistát, és mentse a rekordot.
    4. Hozzon létre egy új szerződéssort a **Szerződéssorok** lapon. Állítson be bármilyen nevet, és Számlázási módszerként válassza az **Idő és az anyagok** lehetőséget.
    5. Hozzon létre egy új projektet, és társítsa ezzel a szerződéssorral.
4. Jelentkezzen be **Molly Clark** erőforrásként. Nyissa meg a **Projektek** > **Időbejegyzések** lehetőséget, és hozzon létre egy időbevitelt az Adventure Works projekt számára.
5. Jelentkezzen be projektmenedzserként. Nyissa meg a **Projektek** > **Jóváhagyások** lehetőséget, és hagyja jóvá az Molly Clark által felvitt időbejegyzési tranzakciót.
6. Lépjen az Adventure Works projekthez, és válassza a **Kapcsolódó** > **Tényadatok** lehetőséget. A rendszer a következő tényleges tranzakciókat hozza létre.

| **Tranzakció típusa** | **Ár** | **Tranzakció pénzneme** | **Összeg** |
| --- | --- | --- | --- |
| Költség | 120 | USD | 1200 |
| Számlázatlan értékesítés | 200 | USD | 2000. |
| Erőforrás-kezelő részleg költsége | 88. | GBP | 880 |
| Szervezetek közötti értékesítések | 120 | USD | 1200 |

7. Jelentkezzen be USPM könyvelőjeként. Nyissa meg a Project Operations Finance példányát, és válassza ki a **USPM** vállalatot. 
8. Nyissa meg a **Projektvezetés és a Könyvelés** > **időszakos** > **Project Operations vagy Customer Engagement** > **Importálás az előkészítésből**, és válassza ki az időszakos folyamat futtatásához. Ez az időszakos folyamat kitölti a Project Operations integrációs naplóját.
9. Nyissa meg a **Projektvezetés és könyvelés** > **Naplók** > **Project Operations integrációs napló** lehetőséget és tekintse át a naplósorokat. A rendszer a következő sort hozza létre.

    | **Tranzakció típusa** | **Ár** | **Tranzakció pénzneme** | **Összeg** |
    | --- | --- | --- | --- |
    | Számlázatlan értékesítés | 200 | USD | 2000. |

    Ha a rendszer be van állítva a bevétel elhatárolásához ehhez a projekthez, a következő lesz feladva:

    - Terhelés: Projekt – a folyamatban lévő munka értékesítési értéke 200 USD
    - Jóváírás: Projekt – elhatárolt bevétel 200 USD

    Ez a nem számlázott értékesítés már készen áll a számlázásra. A számla az Adventure Works számára pénzügyi szempontból is feladható, ha szükséges.

10. Jelentkezzen be **GBPM** könyvelőjeként. Nyissa meg a Project Operations Finance példányát, és nyissa meg a **GBPM** vállalatot. 
11. Nyissa meg a **Projektvezetés és a Könyvelés** > **időszakos** > **Project Operations vagy Customer Engagement** > **Importálás az előkészítésből**, és futtassa az időszakos folyamatot a Project Operations integrációs naplójának kitöltéséhez.
12. Nyissa meg a **Projektvezetés és könyvelés** > **Naplók** > **Project Operations integrációs napló** lehetőséget és tekintse át a sorokat. A rendszer a következő sorokat hozza létre.

    | **Tranzakció típusa** | **Ár** | **Tranzakció pénzneme** | **Összeg** |
    | --- | --- | --- | --- |
    | Erőforrás-kezelő részleg költsége | 88. | GBP | 880 |
    | Szervezetek közötti értékesítések | 120 | USD | 1200 |

    A rekordok közzététele a következő bizonylat-tranzakciókat eredményezi:

    - Terhelés: Projekt költsége 88 GBP
    - Jóváírás: Bérlista-hozzárendelés 88 GBP

    Ha a rendszer be van állítva a vállalatközi bevétel elhatárolásához ehhez a projekthez, a következő lesz feladva:

    - Terhelés: Projekt – a folyamatban lévő munka értékesítési értéke 120 USD
    - Jóváírás: Projekt – elhatárolt bevétel 120 USD

    A rendszer most már készen áll a vállalatközi vevői számla létrehozására.
