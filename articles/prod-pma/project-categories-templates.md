---
title: A projektkiadás-kategóriák szinkronizálása a Finance and Operations és a Project Service Automation között
description: Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektkiadás-kategóriák Microsoft Dynamics 365 Finance és a Dynamics 365 Project Service Automation rendszer között történő szinkronizálására szolgálnak.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999854"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>A projektkiadás-kategóriák szinkronizálása a Finance and Operations és a Project Service Automation között

[!include[banner](../includes/banner.md)]

Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektkiadás-kategóriák Dynamics 365 Finance és a Dynamics 365 Project Service Automation rendszer között történő szinkronizálására szolgálnak.

> [!NOTE]
> - A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.
> - A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.
> - Ha az Enterprise Edition 7.3.0 verzióját használja, a KB 4132657 és a KB 4132660 telepítése után használhatja a sablonokat a projektfeladatok, a költségtranzakció-kategóriák, az órabecslések, a kiadásbecslések és a tényadatok integrálására, valamint a funkciók zárolásának konfigurálására. Ha vissza kell állítania a könyvelési feloszlásokat, ajánlott a KB 4131710 telepítése is.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Adatfolyam a Project Service Automation és a Finance között

A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között. Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projekt költségtranzakciós kategóriáival kapcsolatos adatok áramlását a Finance és a Project Service Automation között.

Ha a projekt költségkategóriái a Finance rendszerben vannak előállítva, akkor integrációs folyamat először a Finance rendszerből a Project Service Automation alkalmazásba irányul. A projekt költségkategóriáinak integrációs azonosítói ezután frissítésre kerülnek a Project Service Automation alkalmazásból a Finance rendszerbe történő szinkronizálással.

Ha a projekt költségkategóriái a Project Service Automation alkalmazásban vannak előállítva, akkor az integrációs folyamat először a Project Service Automation alkalmazásból a Finance rendszerbe irányul. A projektek kategóriáinak a Project Service Automation alkalmazásból való szinkronizálás előtt már konfigurálva kell lenniük a Finance rendszerben. Ezután szinkronizálja a Finance rendszerből vissza a Project Service Automation alkalmazásba, majd a Project Service Automation alkalmazásból ismét a Finance rendszerbe. Így garantálhatja, hogy a kategóriák össze legyenek kapcsolva, és hogy ne jöjjön létre ismétlődés.

> [!NOTE]
> A projekt költségkategóriái általában a Finance rendszerben vannak létrehozva. Ha azonban nem, vagy ha a költségkategóriákat már létrehozták a Project Service Automation alkalmazásban, először szinkronizálnia kell a Projekt költségtranzakciós kategóriái (PSA – Fin és Ops) sablon segítségével. Ezután szinkronizáljon a Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablon segítségével. Ezután futtassa a szinkronizálást a Project Service Automation alkalmazásból a Finance rendszerbe még egyszer.
>
> Ha először a Project Service Automation alkalmazásból szinkronizál, a szinkronizálás futtatása előtt a következő követelményeknek kell teljesülniük a Finance alkalmazásban:
>
> - A Project Service Automation rendszerben beállított projektkategóriának megfelelő megosztott kategóriának léteznie kell, és engedélyezve kell lennie a **Projekt** és a **Költség** elemhez is.
> - Minden olyan Finance jogi személy esetében, amellyel integrálni kell, a következő projektkategóriáknak kell léteznie:
>
>     - A **Projektkategória** létezik. 
>     - A **Felhasználás a költségben** engedélyezve van.
>     - Az **Aktív a naplóban** engedélyezve van.
>     - A **Tranzakció típusa** **Költség** értékre van beállítva.

A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.

[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>A projekt költségkategóriájának szinkronizálása a Finance rendszerből a Project Service Automation alkalmazásba

### <a name="template-and-task"></a>Sablon és feladat

A sablon eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.

A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projekt költségkategóriáit a Finance rendszerből a Project Service Automation alkalmazásba:

- **A sablon neve az adatintegrációban:** Projekt költségtranzakciós kategóriái (Fin és Ops – PSA)
- **A feladat neve a projektben:** Kategóriák szinkronizálása a PSA-val

### <a name="entity-set"></a>Entitáskészlet

| Pénzügy                           | Project Service Automation |
|-----------------------------------|----------------------------|
| A kategóriák integrációs entitása | Tranzakciókategóriák     |

### <a name="entity-flow"></a>Entitásfolyam

A projekt költségkategóriái a Finance rendszerben kezelhetők, és a program tranzakciós kategóriákként szinkronizálja őket a Project Service Automation alkalmazásba.

### <a name="power-query"></a>Power Query

Ha a Project Service Automation alkalmazásba szinkronizál, az Excelhez készült Microsoft Power Query alkalmazást kell használnia a számlázási típus beállításához a tranzakciókategórián. A Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablon egy alapértelmezett oszlopot és leképezést biztosít. Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia a Power Query alkalmazásban. Kövesse ezeket a lépéseket.

1. A nyílra kattintva megnyithatja a projekt költségkategóriáihoz tartozó feladat leképezését a Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablonban.
2. Kattintson a **Speciális lekérdezés és szűrés** hivatkozásra a Power Query megnyitásához.
2. Válassza a **Feltételes oszlop hozzáadása** lehetőséget.
3. Adja meg az új oszlop nevét, például **BillingType**.
4. Írja be a következő feltételt: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Az oszlopban kattintson az **OK** gombra.
6. Ne felejtse el leképezni ezt az új oszlopot a leképezési oldalon.

A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére. A leképezés azokat a mezőinformációkat mutatja, amelyek a Finance rendszerből a Project Service Automation alkalmazásba lesznek szinkronizálva.

[![A projekt költségkategóriái a Project Service Automation sablonleképezéséhez](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>A projekt költségkategóriájának szinkronizálása a Project Service Automation alkalmazásból a Finance rendszerbe

### <a name="template-and-task"></a>Sablon és feladat

A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projekt költségkategóriáit a Project Service Automation alkalmazásból a Finance rendszerbe:

- **A sablon neve az adatintegrációban:** Projekt költségtranzakciós kategóriái (PSA – Fin és Ops)
- **A feladat neve a projektben:** Kategóriák szinkronizálása a Fin Ops rendszerbe

### <a name="entity-set"></a>Entitáskészlet

| Project Service Automation | Pénzügy                           |
|----------------------------|-----------------------------------|
| Tranzakciókategóriák     | A kategóriák integrációs entitása |

### <a name="entity-flow"></a>Entitásfolyam

A projekt költségkategóriái a Finance rendszerben kezelhetők, és a program tranzakciós kategóriákként szinkronizálja őket a Project Service Automation alkalmazásba. A Finance rendszerbe történő visszaszinkronizálás frissíti a projektkategóriát a Finance alkalmazásban a Project Service Automation alkalmazásból származó integrációs azonosítóval.

### <a name="template-mapping-in-data-integration"></a>Sablonok leképezése az adatintegrációban

A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére.

> [!NOTE]
> A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.

[![Project Service Automation és Finance sablonleképezése](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]