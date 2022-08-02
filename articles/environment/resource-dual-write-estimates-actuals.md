---
title: Projektbecslések és tényadatok integrációja
description: Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást a projektbecslésekhez és a tényleges adatokhoz.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029083"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektbecslések és tényadatok integrációja

_**Érvényesség:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén_

Ez a cikk a Project Operations kettős írású integrációjáról nyújt tájékoztatást a projektbecslésekhez és a tényleges adatokhoz.

## <a name="project-estimates"></a>Projektbecslések

A projektmunka-, költség- és anyagbecslések a pénzügyi és üzemeltetési alkalmazásokban jönnek létre és vannak tárolva Microsoft Dataverse, valamint szinkronizálódnak a számviteli célú pénzügyi és üzemeltetési alkalmazásokkal. A létrehozási, frissítési és törlési műveletek nem támogatottak a pénzügyi és üzemeltetési alkalmazásokon keresztül.

A becsült értékek létrehozásához a projekthez érvényes könyvviteli konfiguráció szükséges. A szerződéssorhoz társított projekteknek a projekt költség- és bevételprofil-szabályokban megadott érvényes projektköltség- és bevételi profillal kell lennie megadva. További információkért lásd: [A számlázható projektek könyvelésének konfigurálása](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Munkabecslések

A munkabecsléseket a Projektmenedzser vagy az Erőforráskezelő hozza létre, aki általános vagy elnevezett erőforrást is rendel a projektfeladathoz. Az erőforrás-hozzárendelési bejegyzések a(z) Dataverse felületen, a **Projekt részletei** oldal **Erőforrás-hozzárendelések** lapján vizsgálhatók felül. Erőforrás-hozzárendelési rekordok a Dataverse finance and operations alkalmazásokban óra-előrejelzési rekordok létrehozása a Project Operations integrációs entitás használatával **az órabecslésekhez (msdyn\_ resourceassignments)**.

   ![Munkabecslések integrációja.](./Media/DW4LaborEstimates.png)

A kettős írás szinkronizálja az erőforrás-hozzárendelési rekordokat az átmeneti táblázattal (**ProjCDSEstimateHoursImport**), majd üzleti logikát használ az óraszám-előrejelzési rekordok (**ProjForecastEmpl**) létrehozásához és frissítéséhez.

A projektkönyvelő áttekinti a pénzügyi és üzemeltetési alkalmazásokban létrehozott előrejelzési órarekordokat a Projektvezetés és könyvelés **Minden projekt** > **Tervóra** > **előrejelzései** > **oldalon**.

## <a name="expense-estimates"></a>Költség becslések

A projektmenedzser költségbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Költségbecslések** lapján. A költségbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becsült rekordok tranzakciós osztálya Költség, **és szinkronizálva vannak a pénzügyi és üzemeltetési alkalmazások költség-előrejelzési rekordjaival a Project Operations integrációs entitás használatával** a költségbecslésekhez (msdyn **becsült vonalak)\_.**

   ![Költségbecslések integrációja.](./Media/DW4ExpenseEstimates.png)

A kettős írás szinkronizálja a költségbecslési rekordokat az átmeneti táblázattal (**ProjCDSEstimateExpenseImport**), majd üzleti logikát használ a költség-előrejelzési rekordok (**ProjForecastCost**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A pénzügyi és üzemeltetési alkalmazások üzleti logikája egyetlen költség-előrejelzési rekordot tölt fel az átmeneti táblázatban található ezen részlet használatával.

A projektkönyvelő áttekintheti a költség-előrejelzési rekordokat a pénzügyi és üzemeltetési alkalmazásokban a **Projektvezetés és könyvelés** > **Minden projekt** > **terv** > **költség-előrejelzések** című témakörben.

## <a name="material-estimates"></a>Anyagbecslések

A projektmenedzser anyagbecsléseket hoz létre a(z) Dataverse felületen, a **Projekt részletei** oldal **Anyagbecslések** lapján. Az anyagbecslési rekordokat a(z) Dataverse felületen a **Becslés sor** entitás tárolja. Ezek a becsült rekordok a Material tranzakciós osztályt tartalmazzák, **és szinkronizálódnak a pénzügyi és műveleti alkalmazások cikk-előrejelzési rekordjaival a Project integrációs táblázat segítségével** az anyagbecslésekhez (msdyn **becsült vonalak)\_.**

   ![Anyagbecslések integrációja.](./Media/DW4MaterialEstimates.png)

A kettős írás szinkronizálja az anyagbecslési rekordokat az átmeneti táblázattal (**ProjForecastSalesImpor**), majd üzleti logikát használ a tétel-előrejelzési rekordok (**ForecastSales**) létrehozásához és frissítéséhez. A becslési sorok külön-külön tárolják az értékesítési és költségbecslési rekordokat. A pénzügyi és üzemeltetési alkalmazások üzleti logikája egyetlen cikk-előrejelzési rekordot tölt fel az átmeneti tábla ezen részleteinek felhasználásával.

A projektkönyvelő áttekintheti a cikk-előrejelzési rekordokat a pénzügyi és műveleti alkalmazásokban a Projektvezetés és könyvelés **Minden projekt** > **tervelem** > **előrejelzése** > **oldalon**.

## <a name="project-actuals"></a>Projekt tényleges adatai

A projekt tényleges adatai a(z) Dataverse felületen hozható létre az idő, a költség, az anyagok és a számlázási tevékenység alapján. A tranzakciók minden műveleti attribútumát – beleértve a mennyiséget, a költségárat, az értékesítési árat és a projektet – ebben a(z) Dataverse-entitásban rögzíti a rendszer. További tudnivalókért lásd: [Tényleges adatok](../actuals/actuals-overview.md). A tényleges rekordok szinkronizálása a pénzügyi és üzemeltetési alkalmazásokkal a Project Operations kettős írású táblatérképével **történik\_** a downstream könyveléshez.

   ![Tényleges adatok integrációja.](./Media/DW4Actuals.png)

A **Project Operations tényleges adatok integrációja** táblázatos leképezés szinkronizálja a **Tényleges adatok** entitás összes rekordját a(z) Dataverse felületen úgy, hogy a **Szinkronizálás kihagyása (csak belső használatra)** attribútum **Hamis** értékre van állítva. Ez az attribútumérték a rekord létrehozásakor automatikusan beállításra kerül a(z) Dataverse felületen. Példák arra, amikor ez az attribútum **Igaz** értékre van állítva:

  - A projektköltség tényleges adatai a vállalatközi tranzakciókhoz. További tudnivalókért lásd: [Vállalatközi tranzakciók létrehozása](../project-accounting/create-intercompany-transactions.md). Ezeket a rekordokat a rendszer kihagyja, mert a rendszer újra létrehozza a projekt pénzügyi és üzemeltetési alkalmazásokban való tényleges költségét a vállalatközi szállítói számla feladásakor.
  - A negatív, kiszámlázatlan értékesítési rekordok a proforma számla megerősítéskor jönnek létre. Ezeket a rekordokat a rendszer kihagyja, mert a pénzügyi és üzemeltetési alkalmazásokban a projekt analitikus alkalmazásai nem fordítják vissza a számlázatlan értékesítési rekordot a számlázáskor, hanem az állapotot teljes mértékben számlázva állapotra változtatja.

A kettős írású táblatérkép szinkronizálja a tényleges adatokat a **ProjCDSActualsImport** előkészítő táblával. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat dolgozza fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor. További tudnivalókért lásd: [Project Operations integrációs naplója](../project-accounting/project-operations-integration-journal.md).

A(z) Dataverse a projekt aktuális tranzakciói közötti kapcsolatokat is rögzíti a **Tranzakciós kapcsolat** egységben. További tudnivalókért lásd: [Tényleges adatok összekapcsolása az eredeti rekordokkal](../actuals/linkingactuals.md). A tényleges tranzakciók közötti kapcsolatok a pénzügyi és üzemeltetési alkalmazásokkal is szinkronizálódnak a kettős írású táblatérkép, **az Integrációs entitás a projekttranzakciókhoz kapcsolatok (msdyn\_ tranzakciókapcsolatok)** használatával. Ezeket a rekordokat az **Importálás előkészítő táblából** időszakos folyamat használja fel a Project Operations integráció naplósorok és a projektszámla-javaslat sorainak létrehozásakor.

A Project Operations integrációs naplója és a projektszámlákra vonatkozó javaslat közzétételével elindítja a megfelelő rekordok frissítését az előkészítő táblában, **ProjCDSActualsImport**. A rendszer rögzíti és nyilvántartja az aktuális tranzakciók következő számviteli attribútumait:

- Könyvelési pénznem
- Árfolyam
- Bizonylatszám
- Forgalmi adó összege

A **Project Operations tényleges adatok integrálása** táblaleképezés a tényleges adatok táblaleképezéskor ezekkel az adatokkal frissíti a(z) Dataverse felületen lévő tényleges adatokat.
