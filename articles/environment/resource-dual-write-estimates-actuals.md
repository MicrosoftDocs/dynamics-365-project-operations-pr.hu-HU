---
title: Projektbecslések és tényadatok integrációja
description: Ez témakör a projektbecslésekkel és tényleges adatokkal kapcsolatos, kettős írású Project Operations integrációval kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006294"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektbecslések és tényadatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez témakör a projektbecslésekkel és tényleges adatokkal kapcsolatos, kettős írású Project Operations integrációval kapcsolatos információkat tartalmaz.

## <a name="project-estimates"></a>Projektbecslések

A projekt munka-, költség- és anyagbecslések létrehozása, karbantartása Microsoft Dataverse felületen és szinkronizálása a(z) Finance and Operations alkalmazásokkal könyvelési célokból történik. A létrehozási, frissítési és törlési műveletek nem támogatottak a(z) Finance and Operations alkalmazásokban.

A becsült értékek létrehozásához a projekthez érvényes könyvviteli konfiguráció szükséges. A szerződéssorhoz társított projekteknek a projekt költség- és bevételprofil-szabályokban megadott érvényes projektköltség- és bevételi profillal kell lennie megadva. További információkért lásd: [A számlázható projektek könyvelésének konfigurálása](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Munkabecslések

A munkabecsléseket a Projektmenedzser vagy az Erőforráskezelő hozza létre, aki általános vagy elnevezett erőforrást is rendel a projektfeladathoz. Az erőforrás-hozzárendelési bejegyzések a(z) Dataverse felületen, a **Projekt részletei** oldal **Erőforrás-hozzárendelések** lapján vizsgálhatók felül. A(z) Dataverse felületen az erőforrás-hozzárendelési rekordok óraszám-előrejelzési rekordokat hoznak létre a(z) Finance and Operations alkalmazásokban az **Project Operations integrációs egység az óraszámbecslésekhez (msdyn\_resourceassignments)** használatával.

   ![Munkabecslések integrációja.](./Media/DW4LaborEstimates.png)

A kettős írás szinkronizálja az erőforrás-hozzárendelési rekordokat az átmeneti táblázattal (**ProjCDSEstimateHoursImport**), majd üzleti logikát használ az óraszám-előrejelzési rekordok (**ProjForecastEmpl**) létrehozásához és frissítéséhez.

A projektkönyvelő a **Projektmenedzsment és könyvelés** > **Minden projekt** > **Terv** > **Órák előrejelzése** pontra kattintva tekinti át a(z) Finance and Operations alkalmazásban létrehozott óraszám-előrejelzési rekordokat.

## <a name="expense-estimates"></a>Költség becslések

A projektmenedzser költségbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Költségbecslések** lapján. A költségbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becslési rekordok **Költség** tranzakciós osztályúak, és a **Project Operations integrációs egység a költségbecslésekhez (msdyn\_estimatelines)** segítségével szinkronizálódnak a(z) Finance and Operations alkalmazásokban lévő költség-előrejelzési rekordokkal.

   ![Költségbecslések integrációja.](./Media/DW4ExpenseEstimates.png)

A kettős írás szinkronizálja a költségbecslési rekordokat az átmeneti táblázattal (**ProjCDSEstimateExpenseImport**), majd üzleti logikát használ a költség-előrejelzési rekordok (**ProjForecastCost**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A(z) Finance and Operations alkalmazások üzleti logikája egyetlen költség-előrejelzési rekordot tölt fel az előkészítési táblázat ezen részlete segítségével.

A projektkönyvelő a **Projektmenedzsment és könyvelés** > **Minden projekt** > **Terv** > **Költség-előrejelzés** pontra kattintva tekinti át a(z) Finance and Operations alkalmazásban létrehozott költség-előrejelzési rekordokat.

## <a name="material-estimates"></a>Anyagbecslések

A projektmenedzser anyagbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Anyagbecslések** lapján. Az anyagbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becslési rekordok **Anyag** tranzakciós osztályúak, és a **Project Operations integrációs egység a tételbecslésekhez (msdyn\_estimatelines)** segítségével szinkronizálódnak a(z) Finance and Operations alkalmazásokban lévő anyag-előrejelzési rekordokkal.

   ![Anyagbecslések integrációja.](./Media/DW4MaterialEstimates.png)

A kettős írás szinkronizálja az anyagbecslési rekordokat az átmeneti táblázattal (**ProjForecastSalesImpor**), majd üzleti logikát használ a tétel-előrejelzési rekordok (**ForecastSales**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A(z) Finance and Operations alkalmazások üzleti logikája egyetlen tétel-előrejelzési rekordot tölt fel az előkészítési táblázat ezen részlete segítségével.

A projektkönyvelő a **Projektmenedzsment és könyvelés** > **Minden projekt** > **Terv** > **Tétel-előrejelzés** pontra kattintva tekinti át a(z) Finance and Operations alkalmazásban létrehozott tétel-előrejelzési rekordokat.

## <a name="project-actuals"></a>Projekt tényleges adatai

A projekt tényleges adatai a(z) Dataverse felületen hozható létre az idő, a költség, az anyagok és a számlázási tevékenység alapján. A tranzakciók minden műveleti attribútumát – beleértve a mennyiséget, a költségárat, az értékesítési árat és a projektet – ebben a(z) Dataverse-entitásban rögzíti a rendszer. További tudnivalókért lásd: [Tényleges adatok](../actuals/actuals-overview.md). A rendszer a tényleges rekordokat a(z) Finance and Operations alkalmazásokkal a **Project Operations tényleges adatok integrációja (msdyn\_actuals)** kettős írású táblázatos leképezés segítségével szinkronizálja, a későbbi könyveléshez.

   ![Tényleges adatok integrációja.](./Media/DW4Actuals.png)

A **Project Operations tényleges adatok integrációja** táblázatos leképezés szinkronizálja a **Tényleges adatok** entitás összes rekordját a(z) Dataverse felületen úgy, hogy a **Szinkronizálás kihagyása (csak belső használatra)** attribútum **Hamis** értékre van állítva. Ez az attribútumérték a rekord létrehozásakor automatikusan beállításra kerül a(z) Dataverse felületen. Példák arra, amikor ez az attribútum **Igaz** értékre van állítva:

  - A projektköltség tényleges adatai a vállalatközi tranzakciókhoz. További tudnivalókért lásd: [Vállalatközi tranzakciók létrehozása](../project-accounting/create-intercompany-transactions.md). Ezeket a rekordokat a rendszer azért hagyja ki, mert a rendszer újra létrehozza a(z) Finance and Operations alkalmazásokban a projektköltséget a vállalatközi számla közzétételekor.
  - A negatív, kiszámlázatlan értékesítési rekordok a proforma számla megerősítéskor jönnek létre. Ezek a rekordok kimaradnak, mivel a(z) Finance and Operations alkalmazásokban a projekt alkönyve nem fordítja vissza a számlázatlan értékesítési rekordot a számlázáskor, hanem a státuszt teljes mértékben számlázottra állítja át.

A kettős írású táblatérkép szinkronizálja a tényleges adatokat a **ProjCDSActualsImport** előkészítő táblával. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat dolgozza fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor. További tudnivalókért lásd: [Project Operations integrációs naplója](../project-accounting/project-operations-integration-journal.md).

A(z) Dataverse a projekt aktuális tranzakciói közötti kapcsolatokat is rögzíti a **Tranzakciós kapcsolat** egységben. További tudnivalókért lásd: [Tényleges adatok összekapcsolása az eredeti rekordokkal](../actuals/linkingactuals.md). A tényleges tranzakciók közötti kapcsolatokat is szinkronizálja a rendszer a(z) Finance and Operations alkalmazásokkal a kettős írású táblaleképezés segítségével, **Integrációs entitás a projekttranzakciók kapcsolataihoz (msdyn\_transactionconnections)**. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat használja fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor.

A Project Operations integrációs naplója és a projektszámlákra vonatkozó javaslat közzétételével elindítja a megfelelő rekordok frissítését az előkészítő táblában, **ProjCDSActualsImport**. A rendszer rögzíti és nyilvántartja az aktuális tranzakciók következő számviteli attribútumait:

- Könyvelési pénznem
- Árfolyam
- Bizonylatszám
- Forgalmi adó összege

A **Project Operations tényleges adatok integrálása** táblaleképezés a tényleges adatok táblaleképezéskor ezekkel az adatokkal frissíti a(z) Dataverse felületen lévő tényleges adatokat.
