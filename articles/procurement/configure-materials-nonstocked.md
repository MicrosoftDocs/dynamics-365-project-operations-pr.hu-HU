---
title: Nem készletezett anyagok és függőben lévő szállítói számlák konfigurálása
description: Ez a témakör elmagyarázza, hogyan engedélyezheti a nem raktározott anyagokat és a függőben lévő szállítói számlákat.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1b14ab17a317e7082bc9c24709590745a5c48ea8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592971"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Nem készletezett anyagok és függőben lévő szállítói számlák konfigurálása

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

## <a name="minimum-version-requirement"></a>A minimálisan szükséges verzió

A nem raktározott anyagok és a függőben lévő szállítói számlák nem Dynamics 365 Project Operations raktározott/erőforrás-alapú forgatókönyvekhez a következő verziókra van szükség:

Dynamics 365 Dataverse megoldások:

- Project Operations – 4.9.0.221 vagy magasabb
- Kettős írású alkalmazás vezénylőmegoldás megoldás - 2.2.2.23 vagy magasabb

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) vagy magasabb. Győződjön meg arról, hogy a pénzügyi környezet aktuális, és minden minőségi frissítést alkalmazunk, hogy megfeleljen a minimális verziókövetelményeknek.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Kettős írású térképek futtatása nem raktározott anyagokhoz és szállítói számlaintegrációhoz

Ez a rész a nem raktározott anyagokhoz és szállítói számlákhoz szükséges térképek konkrét adatairól nyújt tájékoztatást. Ellenőrizze, hogy a Rendelkezésben felsorolt előfeltételes térképek [új környezet](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) témakör fut-e a környezetében.

1. Nyissa meg a Lifecycle Services (LCS) lapot, navigáljon az LCS-projekthez, és lépjen a **Környezetvédelem részletei** oldalra.
2. A **Common Data Service Környezeti információk** szakaszban válassza a **CDS-re alkalmazásokra mutató hivatkozás** lehetőséget. Miután kijelölte a hivatkozást, a rendszer átirányítja a leképezésekben szereplő entitások listájára.
3. Győződjön meg arról, hogy a következő térképek futnak. Ha nem futnak, indítsa el őket, és győződjön meg róla, hogy tartalmazza az összes kapcsolódó táblázattérképet.

    - CDS kiadott különböző termékek (termékek)
    - Szállítók v2 (msdyn_vendors)
    - Project Operations táblázat az anyagbecslésekhez (msdyn_estimatelines)
    - Project Operations integrációs projekt szállítói számlát exportáló entitása (msdyn_projectvendorinvoices)
    - Project Operations integrációs projekt szállítói számlasort exportáló entitása (msdyn_projectvendorinvoicelines)
    - Project Operations integrációjának tényleges adatai (msdyn_actuals). Győződjön meg arról, hogy 1.0.0.14 vagy annál magasabb térképverziót futtat. A térkép aktív verzióját a **Verzió** oszlopban, a **Kettős írás** oldalon láthatja. A térkép új verzióját aktiválhatja a **Táblázat térképverzió** kiválasztásával, majd a kijelölt verzió mentésével.

Ha általános demo adatokat használ, előfordulhat, hogy a következő entitástérképeket is le kell állítania és újra kell indítania kezdeti szinkronizálással:
  - Fizetési napok CDS V2 (msdyn_paymentdays)
  - Fizetési ütemezés (msdyn_paymentschedules)
  - Fizetési feltételek (msdyn_paymentterms)
  - Szállítói csoportok (msdyn_vendorgroups)
  - Mértékegységek (uom)

> [!NOTE]
> Előfordulhat, hogy a szállítói csoportok és egységek kezdeti szinkronizálása nem sikerül a meglévő demó adatkészlet néhány rekordja esetén. Figyelmen kívül hagyhatja a hibákat, mivel ezek nem akadályozzák meg a demoadatok használatát a Project Operations segítségével.

## <a name="configure-prerequisites-in-dataverse"></a>Előfeltételek konfigurálása itt: Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Munkafolyamat aktiválása szállító entitáson alapuló fiókok létrehozásához

A Kettős írású vezénylőmegoldás biztosítja a [szállítók fő integrációját](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Ennek a funkciónak az előfeltételeként a szállítói adatokat létre kell hozni a **Fiókok** entitásban. Sablon-munkafolyamat aktiválása szállítók létrehozásához a **Fiókok** táblázatban a [Szállítótervek közötti váltásban](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch) leírtak szerint.

### <a name="set-products-to-be-created-as-active"></a>A létrehozandó termékek beállítása aktívként

A nem raktározott anyagokat a Pénzügyekben **Megjelent termékekként** kell konfigurálni. A Dual Write Orchestration megoldás egyéni [Kiadott termékek integrációját biztosítja a Dataverse Termékkatalógusba](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Alapértelmezés szerint a Pénzügy termékeit egy tervezet állapotában szinkronizálják a(z) Dataverse helyre. A termék aktív állapotba szinkronizálásához, hogy közvetlenül felhasználható legyen az anyagfelhasználási dokumentumokban vagy a függőben lévő szállítói számlákban, lépjen a **Rendszer** > **Adminisztráció** > **Rendszeradminisztráció** > **Rendszerbeállítások** menüpontba, és az **Eladások** lapon állítsa a **Termékek aktív állapotba hozása** értéket **Igen**-re.

## <a name="configure-prerequisites-in-finance"></a>Előfeltételek konfigurálása a Pénzügyekben

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>A függőben lévő szállítói számlák funkciókulcsának engedélyezése

Végezze el a következő lépéseket, hogy engedélyezze a függőben lévő szállítói számlák sorainak projektadatokkal való kiegészítését.

1. A Pénzügyekben lépjen a **Szolgáltatáskezelés** munkaterületre.
2. A szolgáltatáslistában keresse meg a **Project Operations alkalmazásban függőben lévő szállítói számlák engedélyezése az erőforrás-alapú/nem raktározott forgatókönyvek** funkcióhoz, és válassza az **Engedélyezés** lehetőséget.

### <a name="define-category-groups-and-project-categories-for-items"></a>Kategóriacsoportok és projektkategóriák meghatározása az elemekhez

Konfiguráljon legalább egy kategóriacsoportot az **Elem** tranzakciótípushoz, és legalább egy projektkategóriát ezzel a csoporttal. További információkért lásd: [Projektkategóriák konfigurálása](../project-accounting/configure-project-categories.md#category-groups).

Tekintse át a projekt költség- és bevételprofiljait, és konfigurálja a főkönyvi feladás beállítását az elemtranzakciókhoz. További információkért lásd: [A számlázható projektek könyvelésének konfigurálása](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Nem katalogizált termék beállítása

A Project Operations alkalmazásban rögzítheti a kiadott termékkatalógusban konfigurált katalógustermékek és a nem kategorizált termékek anyagbecsléseit és használatát. A nem kategorizált termékek használatához egyetlen kiadott termékre van szükség, amely erre a célra van konfigurálva a Pénzügyekben. A következő lépésekkel konfigurálható egy nem kategorizált termék. Ismételje meg ezeket a lépéseket minden olyan jogi személyben, amely erőforrás-/nem raktározott forgatókönyvekhez használja a Project Operations alkalmazást.

1. A Pénzügyek csoportban lépjen a **Termékinformáció-kezelés** > **Termékek** > **Kiadott termékek** menüpontra, és válassza az **Új** lehetőséget.
2. A **Terméktípus** mezőben válassza az **Elem** lehetőséget, a **Termék altípus** mezőben pedig válassza a **Termék** lehetőséget.
3. Adja meg a termékszámot (WRITEIN) és a termék nevét (Write-in Product).
4. Jelölje ki az elemmodell-csoportot. Győződjön meg arról, hogy a kiválasztott cikkmodell-csoport **Készletezési szabályzatában a Készletezett termék** mező **Hamis** értékre van állítva.
5. Válassza ki az értékeket az **Elemcsoport**, **Tárolási dimenziócsoport** és a **Dimenziócsoport nyomon követése** mezőben. A **Tárolási dimenzió** elemet csak a **Tephely** elemhez használja, és a **Nyomonkövetési-dimenzió** mezőben válassza a **Nincs** lehetőséget.
6. Válassza ki az értékeket a **Készlet egység**, **Beszerzési egység** és **Értékesítési egység** mezőben, majd mentse a módosításokat.
7. A **Terv** lapon állítsa be az alapértelmezett rendelési beállításokat, a **Készlet** lapon pedig állítsa be az alapértelmezett webhelyet és tárhelyet.
8. Lépjen a **Projektmenedzsment és -könyvelés** > **Beállítás** > **Projektkezelési és -könyvelési paraméterek** menüpontra, és nyissa meg a **Project Operations a Dynamics 365 Dataverse** projektet. 
9. Az **Anyagok** lapon, a **Nem kategorizált termék** mezőben válassza ki a létrehozott terméket.
10. A Dataverse környezetben, a webhelytérképen nyissa meg a **Termékek** entitást, és keresse meg a nem kategorizált termék rekordját. 
11. Nyissa meg a rekordadatokat, és állítsa be a termék állapotát **Visszavontra**. Ez a termékállapot megakadályozza, hogy bárki véletlenül használja ezt a rekordot közvetlenül az anyagbecslésekben és a használati dokumentumokban.

### <a name="set-up-a-procurement-integration-account"></a>Beszerzési integrációs fiók beállítása

A beszerzési integrációs számla elszámolási számlaként használatos, amikor egy függőben lévő szállítói számlát könyvelnek egy projekthez rendelt sorokkal.

Ha a rendszer egy függőben lévő szállítói számlát könyvel, ezt a számlát használja a projektköltség összegére. A szállítói számla adatait a(z) Dataverse rendszer feldolgozza, és létrehoz egy megfelelő aktuális projektet. A projekt tényleges adatai bekerülnek a Project Operations integrációja naplóba. Az integrációs napló közzétételekor az összeg törlődik a beszerzési integrációs számláról, és a projekt költségére kerül rögzítésre.

1. A beszerzési integrációs fiók beállításához lépjen a **Projektmenedzsment és -könyvelés** > **Beállítás** > **Projektkezelési és -könyvelési paraméterek** menüpontra, és nyissa meg a **Project Operations a Dynamics 365 Dataverse** projektet. 
2. Jelölje ki az **Anyagok** lapot, és válasszon értéket a **Beszerzési integráció fiók** mezőben.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Projektkategória-alapértelmezések beállítása egy elemhez

1. A Pénzügyekben lépjen a **Projektmenedzsment és -könyvelés** > **Beállítás** > **Projektkezelési és -könyvelési paraméterek** menüpontra, és nyissa meg a **Project Operations a Dynamics 365 Dataverse** projektet. 
2. A **Projektkategória alapértelmezései** lapján, az **Elem mezőben** jelöljön ki egy értéket. Ezt a projektkategóriát akkor használják az anyagtranzakciókhoz, ha a projektkategória nem volt beállítva az aktuális projekt rekordján.
