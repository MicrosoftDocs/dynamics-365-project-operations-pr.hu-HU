---
title: Javaslattétel a projekt erőforrásaira
description: Ez a témakör információt nyújt a projekt erőforrásainak javaslatáról.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fc18c5cbd1a564e186f533a3c0f972e60229a6d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587451"
---
# <a name="propose-project-resources"></a>Javaslattétel a projekt erőforrásaira

[!include [banner](../includes/psa-now-project-operations.md)]

Az erőforrás-kezelők erőforrás-igénylés felhasználásával erőforrást javasolhatnak a projektmenedzser számára.

1. A kérési rácsból vagy maga a kérelemből válassza a **Források keresése** lehetőséget.
2. Az **Ütemezési asszisztens** oldalon válassza ki az erőforrást, majd az **Erőforrás foglalás létrehozása** ablaktáblában a **Foglalási állapot** mezőben válassza a **Foglalás** lehetőséget.

    ![A javasolt erőforrás kiválasztva.](media/Resource-Management-image62.png)

A következő állapotfrissítések történnek:

- Az **Ütemezési asszisztens** oldalon az állapotjelzők frissülnek, jelezve, hogy a foglalást javasolják, nem pedig keményen lefoglalják.

    ![A javasolt foglalás állapotjelzői az Ütemezési segéd oldalon.](media/Resource-Management-image63.png)

- Az erőforrás-kérésnél az állapot megváltozik: **Áttekintést igényel**.

    ![Az erőforrás-kérés státusza Áttekintést igényel-re változott.](media/Resource-Management-image64.png)

- A projekt **Csapat** lapján az általános csapattag **Állapotkérés** értéke megváltozik **Áttekintést igényel** értékre.

    ![Az általános csapattag kérésének állapota a Csapat fülön átkerül az Áttekintést igényel elemre.](media/Resource-Management-image48.png)

A projektvezető elfogadhatja vagy elutasíthatja a javaslatot.

Amikor az erőforrás-kezelők feldolgozzák az erőforrás-kérelmeket, a következő megközelítések bármelyikét használhatják:

- Javasoljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a szükséges órák teljesítéséhez. A javasolt órákat ezután több forrásra osztják, amelyek kielégítik a szükséges órákat. Ebben a forgatókönyvben az órák nem fedhetik át egymást.
- Javasoljon kevesebb erőforrást a szükségesnél. Ebben a forgatókönyvben a javasolt erőforrás-kapacitás kevesebb, mint a kérelmező által megadott szükséges óra. Ezért, amikor a kérelmező elfogadja a javasolt erőforrásokat, nem teljesült erőforrás-követelmény jön létre a fennmaradó kereslet rögzítéséhez.
- Foglaljon több erőforrást a kereslet kielégítésére, ha egyetlen erőforrás sem áll rendelkezésre a munka befejezéséhez.
- Foglaljon kevesebb erőforrást, mint amennyire szükség van. Ebben a forgatókönyvben a foglalt órák kevesebbek, mint a szükséges órák. A rendszer arra irányul, hogy erőforrásokat javasoljon a foglalás helyett, hogy a kérelmező ellenőrizhesse és nyomon tudja követni a fennmaradó igényeket.

## <a name="billable-utilization"></a>Számlázható felhasználás

Az erőforrások megcélozhatók számlázható felhasználással. Ezt a célfelhasználást vagy határozza meg egy erőforrás alapértelmezett szerepének attribútumaként, vagy beállítja az egyes foglalható erőforrások rekordjában. A hasznosítási számítások azon tényleges órákon alapulnak, amelyeket az erőforrások jóváhagyott időbejegyzésekkel jelentettek.

A felhasználás kiszámításához a következő képleteket kell használni:

- Számlázható felhasználás = Számlázható tényleges óra ÷ Erőforrás-kapacitás
- Nem számlázható felhasználás = Tényleges idő számlaszám-azonosítóval = Nem terhelhető, kiegészítő vagy nem elérhető ÷ Erőforrás-kapacitás
- Belső = Valós idő eladási szerződés nélkül ÷ Erőforrás-kapacitás
- Erőforrás-kapacitás = Erőforrás-munkaidő - Irodán kívüli - Nem munkanapok

Az **Erőforrás-hasznosítás** nézetet az **Erőforrások** ablaktáblában találhatja meg.

![Erőforrás-kihasználtság megtekintése.](media/Resource-Management-image65.png)

A rács minden cellája képviseli az erőforrás számlázható felhasználási százalékát egy időszakban, például egy nap, hét vagy hónap. A cellák színezésére a következő képleteket használják:

- **Zöld:** Számlázható felhasználás \>= Erőforrás célfelhasználás
- **Sárga:** Célfelhasználás - 20 \<= Számlázható felhasználás \< Célfelhasználás
- **Piros:** Számlázható felhasználás \< Célfelhasználás - 20

Mivel az **Erőforrás-hasznosítás** nézet az Ütemezési táblán alapul, az Ütemezési tábla szűrési képességeit használhatja az eredmények szűrésére.

A rács megköveteli, hogy állítson be egy célfelhasználást a szerepre vagy az egyes erőforrásokra. A beállítás elvégzéséhez ugorjon a **Erőforrások** \> **Erőforrás szerepek** elemre.

Ezenkívül minden foglalható erőforráshoz alapértelmezett szerepet kell hozzárendelni. Lépjen a **Források** \> **Források** oldalra. A **Project Service** lapon ellenőrizze, hogy az erőforrás szerepe van meghatározva, és hogy a **Alapértelmezett** mező **Igen** értékre van állítva. További szerepeket adhat hozzá, ahol **Alapértelmezett = Nem**. A szerep, ahol az **Alapértelmezett = Igen**, az erőforrás felhasználásának értékelésére szolgál annak a célnak a függvényében.

![Alapértelmezett szerepkészlet.](media/Resource-Management-image67.png)

A **Project Service** lapon az erőforrás egyedi célhasználatát is beállíthatja. A hasznosítási számítás ezt követően a célfelhasználást használja az erőforrás céljának értékelésére, az erőforrás alapértelmezett szerepének célpontja helyett.

Az erőforrás felhasználása csak akkor jelenik meg, ha az erőforrás jóváhagyott, díjköteles időt mutat a rácson megjelenített időszakban.

## <a name="resource-availability"></a>Erőforrás elérhetősége

Fontos, hogy az erőforrás-kezelők képesek legyenek megtekinteni az erőforrások rendelkezésre állását és frissíteni a foglalásokat. Bizonyos esetekben nincs hivatalos igény (erőforrás-igény), de az erőforrás-kezelőnek válaszolnia kell egy nem tervezett igényre, amely csatornákon, például e-mailben, telefonhívásban vagy azonnali üzenetben érkezik. Az erőforrás-kezelők az Ütemezési táblát használják az erőforrások és a foglalások frissítésére.

Az erőforrás rendelkezésre állásának kiszámításához az erőforrás munkaidőjét vesszük alapul. Az erőforrás-foglalások felhasználják az erőforrások kapacitását.

![Ütemezési-tábla.](media/Resource-Management-image68.png)

Az Ütemezési tábla színeket és árnyalatokat használ a foglalások, a rendelkezésre állás és a túlfoglalások, valamint a foglalások állapotának megjelenítésére. Az Ütemezési tábla beállításai lehetővé teszik a jelmagyarázat megjelenítését.

Ha egy jobbra mutató nyíl jelenik meg az ütemező táblán az egyes foglalható források mellett, az erőforrás kibővíthető, hogy megjelenjen az erőforrás által lefoglalt munka részletei.

![A foglalható erőforrás kibővült az Ütemezési táblán.](media/Resource-Management-image69.png)

Mivel a Dynamics 365 Project Service Automation a Universal Resource Scheduling motort használja, ha telepítette a Dynamics 365 Field Service rendszert is, akkor megtekintheti a projektek erőforrás-foglalási, munkamegrendelési és minden más entitás részleteit, amelyekre az ütemezést kiterjesztette.

![A projektek és a megrendelések forrásfoglalásainak részletei.](media/Resource-Management-image70.png)

Az egyes erőforrásokkal kapcsolatos további részletek megtekintéséhez kattintson a jobb gombbal az erőforráskártya megnyitásához.

![Erőforrás-kártya.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
