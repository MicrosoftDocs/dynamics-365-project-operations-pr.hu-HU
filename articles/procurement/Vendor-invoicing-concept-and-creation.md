---
title: Szállítói számlák létrehozása
description: Ez a cikk a szállítói számlák fogalmát ismerteti, és elmagyarázza, hogyan hozhatja létre őket a Microsoftban Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475467"
---
# <a name="create-vendor-invoices"></a>Szállítói számlák létrehozása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

A cikkben ismertetett funkciók használatához engedélyeznie kell az Alvállalkozói tényleges feldolgozás engedélyezése a **Project Operations használatával erőforrás-alapú forgatókönyvekhez** funkciót a **Funkciókezelés** munkaterületen.

A Microsoftnál Dynamics 365 Project Operations a szállítói számlázással rögzítheti a szállítók által befejezett projekt szolgáltatásainak és/vagy anyagainak leszállításából származó költségeket.

Amikor a szolgáltatásokat és/vagy anyagokat alvállalkozásba adják egy szállítónak, az alvállalkozói szerződés az adott szállítóval kötött szerződéses megállapodást jelenti. Ahogy a szállító nyújtja a szolgáltatásokat, vagy ahogy az anyagokat fogadják és felhasználják a projektfeladatokhoz, a költségeket a projekten rögzítik. A szállító ezután rendszeresen számlákat küld. Ezeket a számlákat ellenőrzik, és összevetik a projekten rögzített költségekkel. Az ellenőrzési folyamat befejezése után a szállítói számlát visszaigazolják, és kifizetésre felszabadítják.

## <a name="scenarios-for-use"></a>Használati forgatókönyvek

A Project Operations szállítói számlái két különböző forgatókönyv támogatására használhatók:

- Az ügyfelek a teljes alvállalkozói élményt használják.
- Az ügyfelek nem használják a teljes alvállalkozói élményt, hanem egységes képet szeretnének kapni a Project Operations projektjeinek költségeiről.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Az ügyfelek a teljes alvállalkozói élményt használják

A szállítói számla felhasználói élménye lehetővé teszi az alvállalkozásba adott összetevőkre hivatkozó időbevitelek, anyaghasználat és költségbejegyzések ellenőrzését, valamint a szállítói számlasorokkal való egyeztetésüket. Ezzel a folyamattal ellenőrizhető a szállítói számlasorok pontossága. Az ellenőrzési folyamat befejezése és a szállítói számla megerősítése után a rendszer visszafordítja a jóváhagyott idő-, költség- és anyaghasználati naplókban rögzített tényleges adatokat, majd a szállítói számlasorok használatával új költség-tényleges költségeket hoz létre.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Az ügyfelek nem használják a teljes alvállalkozói élményt, de egységes képet szeretnének kapni a project operations-projektek költségeinekről

Ha az alvállalkozói folyamatot egy harmadik féltől származó rendszerben követi nyomon, az adott harmadik féltől származó rendszerből származó költségeket rögzítheti a Project Operationsbe olyan szállítói számlák létrehozásával, amelyek nem hivatkoznak alvállalkozói szerződésekre. Ily módon a projektmenedzserek egyetlen, egységes nézettel rendelkezhetnek egy adott projekt összes költségéről.

## <a name="create-vendor-invoices-in-project-operations"></a>Szállítói számlák létrehozása a Project Operationsben

A szállítói számlák Dynamics 365 Finance-ben jönnek létre a **Kötelezettségek** modul használatával. Szállítói számlákat nem hozhat létre közvetlenül a Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Szállítói számla ellenőrzésének beállítása

Ha a szállítói számlát alvállalkozói szerződéshez Dataverse szánják, engedélyeznie kell a **Pm által végzett kézi ellenőrzés kötelező** paramétert. Az opció beállítása határozza meg, hogy a szállítói számlát automatikusan vissza kell-e erősíteni a Dataverse, vagy manuális megerősítést igényel. Minden projektszállítói számla fejléce tartalmaz egy azonos nevű beállítást. Alapértelmezés szerint az összes projektszállítói számla fejlécén lévő beállítás az itt beállított értékre van állítva. Az értéket azonban szükség szerint frissítheti az egyes szállítói számlák fejlécében.

Ha a beállítás Igen értékre **van állítva, a Finance rendszerben létrehozott és szinkronizált** Dataverse szállítói számla Vázlat **állapotú**. A számlát ezután a projektmenedzsernek érvényesítenie és ellenőriznie kell, majd meg kell erősítenie, mielőtt feldolgozná és feladná az adott projekt- és főkönyvi számlákra a Finance rendszerben.

Ha a beállítás nem **értékre** van állítva, a szállítói számla automatikusan megerősítésre kerül. Nincs szükség további intézkedésre.

A szállítói számla ellenőrzésének beállításához kövesse az alábbi lépéseket.

1. A Pénzügyek területen lépjen a **Projektvezetési és könyvelés** \> **beállítása Projektvezetési és könyvelési paraméterek elemre.** \> **·**
1. **A Pénzügyi** lapon állítsa a Kötelező a PM általi manuális ellenőrzés beállítást **Igen** értékre **, ha a** vállalati szabályzat megköveteli az alvállalkozói szállítói számlák ellenőrzését. Ha a projektmenedzser általi ellenőrzés nem szükséges, Dataverse hagyja a értékkészlet Nem **értékre**. Alapértelmezés szerint a beállítás a Függőben lévő **szállítói számla** oldalon lesz használva.

> [!NOTE]
> Az alvállalkozói Dataverse szerződésekhez létrehozott szállítói számlák csak akkor dolgozhatók fel megfelelően, ha a **Pm által végzett manuális ellenőrzés kötelező** beállítás Igen **értékre** van állítva. Az alvállalkozók által létrehozott idő-, anyag- és költségköltség-tényleges adatokat a projektmenedzser csak akkor tudja manuálisan egyeztetni a szállítói számlasorokkal, ha ez a beállítás Igen **értékre** van állítva.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Beszerzési integrációs fiók beállítása szállítói számlákhoz

Amikor egy szállítói számlát a Finance for Project Operations – Integrated environment (nem készlet) területen adnak fel, a pénzügyi adatok feladásra kerülnek a Beszerzési integrációs számlára. A rendszer létrehozza a feladott számla tényleges adatait Dataverse. Ezek a tényleges adatok a Finance mappában vannak közzétéve a Project integrációs napló használatával. A Projektintegrációs napló közzététele közzéteszi a tényleges költséget, és megfordítja a beszerzési integrációs fiókot.

Beszerzési integrációs fiók szállítói számlákhoz való beállításához kövesse az alábbi lépéseket.

1. A Pénzügyek területen lépjen a **Projektvezetési és könyvelés** \> **beállítása Projektvezetési és könyvelési paraméterek elemre.** \> **·**
1. A Dynamics 365 ügyfélkapcsolati műveletek projektműveletei lapon válassza az **Anyagbeszerzés** **integrációs** fiók \> lehetőséget.**·**

### <a name="create-and-post-subcontract-vendor-invoices"></a>Alvállalkozói szállítói számlák létrehozása és feladása

Amikor egy kötelezettségekért felelős ügyintéző számlát kap az alvállalkozótól, új számla jön létre a Finance-ben.

1. A Pénzügyek területen lépjen a Kötelezettségek **számlák** \> **·**\> függőben lévő szállítói számlák elemre.**·**
1. A műveleti ablaktáblán **válassza az** Új **lehetőséget** egy szállítói számla létrehozásához.
1. A számla fejlécében, a Számlaszámla **mezőben válassza az** Alvállalkozó **lehetőséget**.
1. Válassza ki a számla dátumát.
1. **A Fejléc** lapon állítsa a **Pm által végzett manuális ellenőrzés kötelező** beállítást Igen **értékre**. Ennek a beállításnak az alapértelmezett beállítása a **Projektvezetési és könyvelési paraméterek** oldalon található. Ez azonban a szállítói számla szintjén módosítható.
1. A Számlasor **gyorslapon válassza a** Sor **hozzáadása lehetőséget** a szállítói számlasor létrehozásához.
1. Válassza ki az alvállalkozói sorokhoz létrehozott beszerzési kategóriát, és adja meg az egységárat, a mértékegységet és a mennyiséget.
1. A szállítói számlasorok szakasz Projekt **lapján válassza ki azt a** projektet, amellyel az alvállalkozó megosztja az alvállalkozói számlát.
1. Válassza ki a projektkategóriát. Bármilyen típusú **tétel**, költség **·**, **anyag** vagy **óra** lehet.
1. Csak akkor válassza ki a szerepkört, **ha a kiválasztott projektkategória Óra** típusú.
1. Válassza a Feladás **lehetőséget** a szállítói számla feladásához.

Másik lehetőségként szállítói számlát is létrehozhat, ha a **Kötelezettségek**\> számlák **·**\> A szállítói számlák **megnyitása elemre** lép, és az Új **lehetőséget választja.**

A szállítói számla feladásakor az elérhetővé válik a Dataverse projektmenedzser ellenőrzéséhez és feldolgozásához.

## <a name="vendor-invoice-processing-in-dataverse"></a>Szállítói számlafeldolgozás Dataverse

A létrehozott Dataverse szállítói számlán néhány mezőérték a Finance rendszerben rögzített szállítói számlából származik. Más értékek az alvállalkozói szerződésből származó alapértelmezett értékek.

A rendszer a következő mezőket és a kapcsolódó rekordokat másolja az alvállalkozói szerződésből a szállítói számla fejlécébe:

- Pénznem
- Szerződő részleg
- Fizetési feltételek

A szállítói számlasorokban a Project Operations a következő mezőértékeket használja az alapértelmezett alvállalkozói és alvállalkozói sorhivatkozás megadásához:

- Tranzakcióosztály
- Beosztás
- Tranzakció kategóriája
- Termék mezők
- Project
- Feladatok

> [!NOTE]
> A rögzített árú alvállalkozói sorok nem támogatottak a Project Operationsben.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
