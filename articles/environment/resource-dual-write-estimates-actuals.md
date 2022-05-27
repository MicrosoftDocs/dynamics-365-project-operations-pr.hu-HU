---
title: Projektbecslések és tényadatok integrációja
description: Ez témakör a projektbecslésekkel és tényleges adatokkal kapcsolatos, kettős írású Project Operations integrációval kapcsolatos információkat tartalmaz.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577193"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektbecslések és tényadatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez témakör a projektbecslésekkel és tényleges adatokkal kapcsolatos, kettős írású Project Operations integrációval kapcsolatos információkat tartalmaz.

## <a name="project-estimates"></a>Projektbecslések

A projektmunka-, költség- és anyagbecslések számviteli célokra létrehozódnak és karbantartódnak Microsoft Dataverse, és szinkronizálódnak a Pénzügyi és műveletek alkalmazásokkal. A létrehozási, frissítési és törlési műveleteket a Pénzügy és műveletek alkalmazás nem támogatja.

A becsült értékek létrehozásához a projekthez érvényes könyvviteli konfiguráció szükséges. A szerződéssorhoz társított projekteknek a projekt költség- és bevételprofil-szabályokban megadott érvényes projektköltség- és bevételi profillal kell lennie megadva. További információkért lásd: [A számlázható projektek könyvelésének konfigurálása](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Munkabecslések

A munkabecsléseket a Projektmenedzser vagy az Erőforráskezelő hozza létre, aki általános vagy elnevezett erőforrást is rendel a projektfeladathoz. Az erőforrás-hozzárendelési bejegyzések a(z) Dataverse felületen, a **Projekt részletei** oldal **Erőforrás-hozzárendelések** lapján vizsgálhatók felül. Erőforrás-hozzárendelési rekordok létrehozása óra-előrejelzési rekordok létrehozásában Dataverse a Pénzügy és műveletek alkalmazásokban a Project Operations integrációs entitás használatával **órabecslésekhez (msdyn\_ resourceassignments)**.

   ![Munkabecslések integrációja.](./Media/DW4LaborEstimates.png)

A kettős írás szinkronizálja az erőforrás-hozzárendelési rekordokat az átmeneti táblázattal (**ProjCDSEstimateHoursImport**), majd üzleti logikát használ az óraszám-előrejelzési rekordok (**ProjForecastEmpl**) létrehozásához és frissítéséhez.

A Projektkönyvelő áttekinti a Pénzügy és műveletek alkalmazásban létrehozott előrejelzési órarekordokat a **Projektmenedzsment és -számvitel** > **minden projekt** > **Terv** > **órája előrejelzésének előrejelzésével**.

## <a name="expense-estimates"></a>Költség becslések

A projektmenedzser költségbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Költségbecslések** lapján. A költségbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becslési rekordok tranzakcióosztálysal rendelkeznek, költséggel, **és szinkronizálva vannak a Pénzügyi és üzemeltetési alkalmazások költség-előrejelzési rekordjaival, amelyek a Project Operations integrációs entitást használják** költségbecslésekhez (msdyn **estimatelines)\_.**

   ![Költségbecslések integrációja.](./Media/DW4ExpenseEstimates.png)

A kettős írás szinkronizálja a költségbecslési rekordokat az átmeneti táblázattal (**ProjCDSEstimateExpenseImport**), majd üzleti logikát használ a költség-előrejelzési rekordok (**ProjForecastCost**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A Pénzügy és műveletek alkalmazások üzleti logikája egyetlen költség-előrejelzési rekordot tölt fel az átmeneti táblában szereplő ezen részletek felhasználásával.

A Projektkönyvelő áttekintheti a Költség-előrejelzési rekordokat a Pénzügy és műveletek alkalmazásban a Projektmenedzsment és számvitel minden projekt **tervköltség-előrejelzésének** > **·** > **megnyitásával** > **.**

## <a name="material-estimates"></a>Anyagbecslések

A projektmenedzser anyagbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Anyagbecslések** lapján. Az anyagbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becsült rekordok tranzakciós osztálya az Anyag **,** és szinkronizálva vannak a Pénzügyi és üzemeltetési alkalmazások cikk-előrejelzési rekordjaival, amelyek a Project integrációs tábláját használják **anyagbecslésekhez (msdyn\_ estimatelines)**.

   ![Anyagbecslések integrációja.](./Media/DW4MaterialEstimates.png)

A kettős írás szinkronizálja az anyagbecslési rekordokat az átmeneti táblázattal (**ProjForecastSalesImpor**), majd üzleti logikát használ a tétel-előrejelzési rekordok (**ForecastSales**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A Pénzügy és műveletek alkalmazások üzleti logikája egyetlen cikk-előrejelzési rekordot tölt fel az átmeneti táblában szereplő ezen részletek felhasználásával.

A Projektkönyvelő a Pénzügyi és műveleti alkalmazások cikk-előrejelzési rekordjait a Projektkezelés és könyvelés minden projekt **cikk-előrejelzésének** > **·** > **megtekintésével** > **tekintheti** meg.

## <a name="project-actuals"></a>Projekt tényleges adatai

A projekt tényleges adatai a(z) Dataverse felületen hozható létre az idő, a költség, az anyagok és a számlázási tevékenység alapján. A tranzakciók minden műveleti attribútumát – beleértve a mennyiséget, a költségárat, az értékesítési árat és a projektet – ebben a(z) Dataverse-entitásban rögzíti a rendszer. További tudnivalókért lásd: [Tényleges adatok](../actuals/actuals-overview.md). A tényleges rekordok szinkronizálódnak a Pénzügy és műveletek alkalmazásokkal a project operations integrációs tényleges adatok (msdyn **tényleges adatok)\_ kettős írási táblatérkép** használatával az alsóbb szintű könyveléshez.

   ![Tényleges adatok integrációja.](./Media/DW4Actuals.png)

A **Project Operations tényleges adatok integrációja** táblázatos leképezés szinkronizálja a **Tényleges adatok** entitás összes rekordját a(z) Dataverse felületen úgy, hogy a **Szinkronizálás kihagyása (csak belső használatra)** attribútum **Hamis** értékre van állítva. Ez az attribútumérték a rekord létrehozásakor automatikusan beállításra kerül a(z) Dataverse felületen. Példák arra, amikor ez az attribútum **Igaz** értékre van állítva:

  - A projektköltség tényleges adatai a vállalatközi tranzakciókhoz. További tudnivalókért lásd: [Vállalatközi tranzakciók létrehozása](../project-accounting/create-intercompany-transactions.md). Ezek a rekordok kimaradnak, mert a rendszer a vállalatközi szállítói számla könyvelésekor újra létrehozza a projekt tényleges költségét a Pénzügy és műveletek alkalmazásban.
  - A negatív, kiszámlázatlan értékesítési rekordok a proforma számla megerősítéskor jönnek létre. Ezek a rekordok kimaradnak, mert a Pénzügyi és üzemeltetési alkalmazások projekt-alszervezője nem fordítja vissza a számlázáskor a nem számlázott értékesítési rekordot, hanem az állapotot teljes mértékben számlázottra módosítja.

A kettős írású táblatérkép szinkronizálja a tényleges adatokat a **ProjCDSActualsImport** előkészítő táblával. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat dolgozza fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor. További tudnivalókért lásd: [Project Operations integrációs naplója](../project-accounting/project-operations-integration-journal.md).

A(z) Dataverse a projekt aktuális tranzakciói közötti kapcsolatokat is rögzíti a **Tranzakciós kapcsolat** egységben. További tudnivalókért lásd: [Tényleges adatok összekapcsolása az eredeti rekordokkal](../actuals/linkingactuals.md). A tényleges tranzakciók közötti kapcsolatok szinkronizálódnak a Pénzügy és az Operations alkalmazásokkal is a kettős írási táblatérkép, **a projekttranzakciók integrációs entitása kapcsolatok (msdyn\_ tranzakciókapcsolatok)** használatával. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat használja fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor.

A Project Operations integrációs naplója és a projektszámlákra vonatkozó javaslat közzétételével elindítja a megfelelő rekordok frissítését az előkészítő táblában, **ProjCDSActualsImport**. A rendszer rögzíti és nyilvántartja az aktuális tranzakciók következő számviteli attribútumait:

- Könyvelési pénznem
- Árfolyam
- Bizonylatszám
- Forgalmi adó összege

A **Project Operations tényleges adatok integrálása** táblaleképezés a tényleges adatok táblaleképezéskor ezekkel az adatokkal frissíti a(z) Dataverse felületen lévő tényleges adatokat.
