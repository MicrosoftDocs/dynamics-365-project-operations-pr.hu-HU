---
title: A projektkiadás-kategóriák szinkronizálása a Finance and Operations és a Project Service Automation között
description: Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektkiadás-kategóriák Microsoft Dynamics 365 Finance és a Dynamics 365 Project Service Automation rendszer között történő szinkronizálására szolgálnak.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289642"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="2762a-103">A projektkiadás-kategóriák szinkronizálása a Finance and Operations és a Project Service Automation között</span><span class="sxs-lookup"><span data-stu-id="2762a-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2762a-104">Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektkiadás-kategóriák Dynamics 365 Finance és a Dynamics 365 Project Service Automation rendszer között történő szinkronizálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="2762a-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="2762a-105">A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="2762a-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="2762a-106">A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.</span><span class="sxs-lookup"><span data-stu-id="2762a-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="2762a-107">Ha az Enterprise Edition 7.3.0 verzióját használja, a KB 4132657 és a KB 4132660 telepítése után használhatja a sablonokat a projektfeladatok, a költségtranzakció-kategóriák, az órabecslések, a kiadásbecslések és a tényadatok integrálására, valamint a funkciók zárolásának konfigurálására.</span><span class="sxs-lookup"><span data-stu-id="2762a-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="2762a-108">Ha vissza kell állítania a könyvelési feloszlásokat, ajánlott a KB 4131710 telepítése is.</span><span class="sxs-lookup"><span data-stu-id="2762a-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="2762a-109">Adatfolyam a Project Service Automation és a Finance között</span><span class="sxs-lookup"><span data-stu-id="2762a-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="2762a-110">A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között.</span><span class="sxs-lookup"><span data-stu-id="2762a-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="2762a-111">Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projekt költségtranzakciós kategóriáival kapcsolatos adatok áramlását a Finance és a Project Service Automation között.</span><span class="sxs-lookup"><span data-stu-id="2762a-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="2762a-112">Ha a projekt költségkategóriái a Finance rendszerben vannak előállítva, akkor integrációs folyamat először a Finance rendszerből a Project Service Automation alkalmazásba irányul.</span><span class="sxs-lookup"><span data-stu-id="2762a-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="2762a-113">A projekt költségkategóriáinak integrációs azonosítói ezután frissítésre kerülnek a Project Service Automation alkalmazásból a Finance rendszerbe történő szinkronizálással.</span><span class="sxs-lookup"><span data-stu-id="2762a-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2762a-114">Ha a projekt költségkategóriái a Project Service Automation alkalmazásban vannak előállítva, akkor az integrációs folyamat először a Project Service Automation alkalmazásból a Finance rendszerbe irányul.</span><span class="sxs-lookup"><span data-stu-id="2762a-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="2762a-115">A projektek kategóriáinak a Project Service Automation alkalmazásból való szinkronizálás előtt már konfigurálva kell lenniük a Finance rendszerben.</span><span class="sxs-lookup"><span data-stu-id="2762a-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="2762a-116">Ezután szinkronizálja a Finance rendszerből vissza a Project Service Automation alkalmazásba, majd a Project Service Automation alkalmazásból ismét a Finance rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="2762a-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="2762a-117">Így garantálhatja, hogy a kategóriák össze legyenek kapcsolva, és hogy ne jöjjön létre ismétlődés.</span><span class="sxs-lookup"><span data-stu-id="2762a-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="2762a-118">A projekt költségkategóriái általában a Finance rendszerben vannak létrehozva.</span><span class="sxs-lookup"><span data-stu-id="2762a-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="2762a-119">Ha azonban nem, vagy ha a költségkategóriákat már létrehozták a Project Service Automation alkalmazásban, először szinkronizálnia kell a Projekt költségtranzakciós kategóriái (PSA – Fin és Ops) sablon segítségével.</span><span class="sxs-lookup"><span data-stu-id="2762a-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="2762a-120">Ezután szinkronizáljon a Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablon segítségével.</span><span class="sxs-lookup"><span data-stu-id="2762a-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="2762a-121">Ezután futtassa a szinkronizálást a Project Service Automation alkalmazásból a Finance rendszerbe még egyszer.</span><span class="sxs-lookup"><span data-stu-id="2762a-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="2762a-122">Ha először a Project Service Automation alkalmazásból szinkronizál, a szinkronizálás futtatása előtt a következő követelményeknek kell teljesülniük a Finance alkalmazásban:</span><span class="sxs-lookup"><span data-stu-id="2762a-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="2762a-123">A Project Service Automation rendszerben beállított projektkategóriának megfelelő megosztott kategóriának léteznie kell, és engedélyezve kell lennie a **Projekt** és a **Költség** elemhez is.</span><span class="sxs-lookup"><span data-stu-id="2762a-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="2762a-124">Minden olyan Finance jogi személy esetében, amellyel integrálni kell, a következő projektkategóriáknak kell léteznie:</span><span class="sxs-lookup"><span data-stu-id="2762a-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="2762a-125">A **Projektkategória** létezik.</span><span class="sxs-lookup"><span data-stu-id="2762a-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="2762a-126">A **Felhasználás a költségben** engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2762a-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="2762a-127">Az **Aktív a naplóban** engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2762a-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="2762a-128">A **Tranzakció típusa** **Költség** értékre van beállítva.</span><span class="sxs-lookup"><span data-stu-id="2762a-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="2762a-129">A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.</span><span class="sxs-lookup"><span data-stu-id="2762a-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="2762a-130">[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="2762a-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="2762a-131">A projekt költségkategóriájának szinkronizálása a Finance rendszerből a Project Service Automation alkalmazásba</span><span class="sxs-lookup"><span data-stu-id="2762a-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="2762a-132">Sablon és feladat</span><span class="sxs-lookup"><span data-stu-id="2762a-132">Template and task</span></span>

<span data-ttu-id="2762a-133">A sablon eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="2762a-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2762a-134">A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projekt költségkategóriáit a Finance rendszerből a Project Service Automation alkalmazásba:</span><span class="sxs-lookup"><span data-stu-id="2762a-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="2762a-135">**A sablon neve az adatintegrációban:** Projekt költségtranzakciós kategóriái (Fin és Ops – PSA)</span><span class="sxs-lookup"><span data-stu-id="2762a-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="2762a-136">**A feladat neve a projektben:** Kategóriák szinkronizálása a PSA-val</span><span class="sxs-lookup"><span data-stu-id="2762a-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="2762a-137">Entitáskészlet</span><span class="sxs-lookup"><span data-stu-id="2762a-137">Entity set</span></span>

| <span data-ttu-id="2762a-138">Pénzügy</span><span class="sxs-lookup"><span data-stu-id="2762a-138">Finance</span></span>                           | <span data-ttu-id="2762a-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2762a-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="2762a-140">A kategóriák integrációs entitása</span><span class="sxs-lookup"><span data-stu-id="2762a-140">Integration entity for categories</span></span> | <span data-ttu-id="2762a-141">Tranzakciókategóriák</span><span class="sxs-lookup"><span data-stu-id="2762a-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="2762a-142">Entitásfolyam</span><span class="sxs-lookup"><span data-stu-id="2762a-142">Entity flow</span></span>

<span data-ttu-id="2762a-143">A projekt költségkategóriái a Finance rendszerben kezelhetők, és a program tranzakciós kategóriákként szinkronizálja őket a Project Service Automation alkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="2762a-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="2762a-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="2762a-144">Power Query</span></span>

<span data-ttu-id="2762a-145">Ha a Project Service Automation alkalmazásba szinkronizál, az Excelhez készült Microsoft Power Query alkalmazást kell használnia a számlázási típus beállításához a tranzakciókategórián.</span><span class="sxs-lookup"><span data-stu-id="2762a-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="2762a-146">A Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablon egy alapértelmezett oszlopot és leképezést biztosít.</span><span class="sxs-lookup"><span data-stu-id="2762a-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="2762a-147">Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia a Power Query alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="2762a-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="2762a-148">Kövesse ezeket a lépéseket.</span><span class="sxs-lookup"><span data-stu-id="2762a-148">Follow these steps.</span></span>

1. <span data-ttu-id="2762a-149">A nyílra kattintva megnyithatja a projekt költségkategóriáihoz tartozó feladat leképezését a Projekt költségtranzakciós kategóriái (Fin és Ops – PSA) sablonban.</span><span class="sxs-lookup"><span data-stu-id="2762a-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="2762a-150">Kattintson a **Speciális lekérdezés és szűrés** hivatkozásra a Power Query megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="2762a-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="2762a-151">Válassza a **Feltételes oszlop hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="2762a-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="2762a-152">Adja meg az új oszlop nevét, például **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="2762a-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="2762a-153">Írja be a következő feltételt: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="2762a-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="2762a-154">Az oszlopban kattintson az **OK** gombra.</span><span class="sxs-lookup"><span data-stu-id="2762a-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="2762a-155">Ne felejtse el leképezni ezt az új oszlopot a leképezési oldalon.</span><span class="sxs-lookup"><span data-stu-id="2762a-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="2762a-156">A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére.</span><span class="sxs-lookup"><span data-stu-id="2762a-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="2762a-157">A leképezés azokat a mezőinformációkat mutatja, amelyek a Finance rendszerből a Project Service Automation alkalmazásba lesznek szinkronizálva.</span><span class="sxs-lookup"><span data-stu-id="2762a-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="2762a-158">[![A projekt költségkategóriái a Project Service Automation sablonleképezéséhez](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2762a-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="2762a-159">A projekt költségkategóriájának szinkronizálása a Project Service Automation alkalmazásból a Finance rendszerbe</span><span class="sxs-lookup"><span data-stu-id="2762a-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="2762a-160">Sablon és feladat</span><span class="sxs-lookup"><span data-stu-id="2762a-160">Template and task</span></span>

<span data-ttu-id="2762a-161">A következő sablon és a mögöttes feladat segítségével szinkronizálhatja a projekt költségkategóriáit a Project Service Automation alkalmazásból a Finance rendszerbe:</span><span class="sxs-lookup"><span data-stu-id="2762a-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="2762a-162">**A sablon neve az adatintegrációban:** Projekt költségtranzakciós kategóriái (PSA – Fin és Ops)</span><span class="sxs-lookup"><span data-stu-id="2762a-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="2762a-163">**A feladat neve a projektben:** Kategóriák szinkronizálása a Fin Ops rendszerbe</span><span class="sxs-lookup"><span data-stu-id="2762a-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="2762a-164">Entitáskészlet</span><span class="sxs-lookup"><span data-stu-id="2762a-164">Entity set</span></span>

| <span data-ttu-id="2762a-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2762a-165">Project Service Automation</span></span> | <span data-ttu-id="2762a-166">Pénzügy</span><span class="sxs-lookup"><span data-stu-id="2762a-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="2762a-167">Tranzakciókategóriák</span><span class="sxs-lookup"><span data-stu-id="2762a-167">Transaction categories</span></span>     | <span data-ttu-id="2762a-168">A kategóriák integrációs entitása</span><span class="sxs-lookup"><span data-stu-id="2762a-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="2762a-169">Entitásfolyam</span><span class="sxs-lookup"><span data-stu-id="2762a-169">Entity flow</span></span>

<span data-ttu-id="2762a-170">A projekt költségkategóriái a Finance rendszerben kezelhetők, és a program tranzakciós kategóriákként szinkronizálja őket a Project Service Automation alkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="2762a-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="2762a-171">A Finance rendszerbe történő visszaszinkronizálás frissíti a projektkategóriát a Finance alkalmazásban a Project Service Automation alkalmazásból származó integrációs azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="2762a-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2762a-172">Sablonok leképezése az adatintegrációban</span><span class="sxs-lookup"><span data-stu-id="2762a-172">Template mapping in Data integration</span></span>

<span data-ttu-id="2762a-173">A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére.</span><span class="sxs-lookup"><span data-stu-id="2762a-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="2762a-174">A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.</span><span class="sxs-lookup"><span data-stu-id="2762a-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2762a-175">[![Project Service Automation és Finance sablonleképezése](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2762a-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]