---
title: A projektbecslések szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe
description: Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektórabecslések és a projektkiadás-becslések közvetlenül a Microsoft Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.
author: KimANelson
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752214"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a8ea1-103">A projektbecslések szinkronizálása közvetlenül a Project Service Automation alkalmazásból a Finance and Operations rendszerbe</span><span class="sxs-lookup"><span data-stu-id="a8ea1-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a8ea1-104">Ez a témakör ismerteti azokat a sablonokat és azokat az alapul szolgáló feladatokat, amelyek a projektórabecslések és a projektkiadás-becslések közvetlenül a Dynamics 365 Project Service Automation alkalmazásból a Dynamics 365 Finance rendszerbe történő szinkronizálására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a8ea1-105">A projektfeladatok integrációja, a kiadási tranzakciók kategóriái, az órabecslések, a kiadásbecslések és a funkciók zárolása a 8.0 verzióban érhető el.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="a8ea1-106">A tényadatok integrációja a 8.0.1 vagy újabb verziókban érhető el.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a8ea1-107">Adatfolyam a Project Service Automation és a Finance között</span><span class="sxs-lookup"><span data-stu-id="a8ea1-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a8ea1-108">A Project Service Automation és Finance közötti integrációs megoldás az adatintegrációs funkció segítségével szinkronizálja az adatokat a Project Service Automation és a Finance példányai között.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a8ea1-109">Az adatintegrációs szolgáltatással elérhető integrációs sablonok lehetővé teszik a projekt órabecsléseivel és a projekt költségbecsléseivel kapcsolatos adatok áramlását a Project Service Automation és a Finance között.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a8ea1-110">A következő ábra azt mutatja be, hogyan történik az adatok szinkronizálása a Project Service Automation és a Finance rendszer között.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a8ea1-111">[![Adatfolyam a Project Service Automation és a Finance közötti integrációhoz](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="a8ea1-112">Projekt órabecslései</span><span class="sxs-lookup"><span data-stu-id="a8ea1-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a8ea1-113">Sablon és feladatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-113">Template and tasks</span></span>

<span data-ttu-id="a8ea1-114">A rendelkezésre álló sablonok eléréséhez a Microsoft Power Apps felügyeleti központban válassza a **Projektek** lehetőséget, majd a jobb felső sarokban válassza az **Új projekt** lehetőséget a nyilvános sablonok kiválasztásához.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a8ea1-115">A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a projekt órabecsléseit a Project Service Automation alkalmazásból a Finance rendszerbe:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a8ea1-116">**A sablon neve az adatintegrációban:** Projekt órabecslései (PSA – Fin és Ops)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a8ea1-117">**A feladat neve a projektben:**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a8ea1-118">Tranzakciókapcsolatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-118">Transaction relationships</span></span>
    - <span data-ttu-id="a8ea1-119">Költség becslések</span><span class="sxs-lookup"><span data-stu-id="a8ea1-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a8ea1-120">Entitáskészlet</span><span class="sxs-lookup"><span data-stu-id="a8ea1-120">Entity set</span></span>

| <span data-ttu-id="a8ea1-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a8ea1-121">Project Service Automation</span></span> | <span data-ttu-id="a8ea1-122">Pénzügy</span><span class="sxs-lookup"><span data-stu-id="a8ea1-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="a8ea1-123">Projektfeladatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-123">Project tasks</span></span>              | <span data-ttu-id="a8ea1-124">Integrációs entitás a projekt órabecsléseihez</span><span class="sxs-lookup"><span data-stu-id="a8ea1-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a8ea1-125">Entitásfolyam</span><span class="sxs-lookup"><span data-stu-id="a8ea1-125">Entity flow</span></span>

<span data-ttu-id="a8ea1-126">A projekt órabecslései a Project Service Automation alkalmazásban kezelhetők, és a program projektóra-előrejelzésekként szinkronizálja őket a Finance rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a8ea1-127">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="a8ea1-127">Prerequisites</span></span>

<span data-ttu-id="a8ea1-128">A projekt ürabecsléseinek szinkronizálása előtt szinkronizálnia kell a projekteket, a projektfeladatokat és a projekt költségeinek tranzakciós kategóriáit.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a8ea1-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="a8ea1-129">Power Query</span></span>

<span data-ttu-id="a8ea1-130">A projekt órabecsléseinek sablonjában az Excelhez készült Microsoft Power Query használatával kell végrehajtania ezeket a feladatokat:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="a8ea1-131">Állítsa be az alapértelmezett előrejelzési modell azonosítóját, amelyet akkor használ a rendszer, ha az integráció új óra-előrejelzéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a8ea1-132">Szűrjön ki a feladatban minden olyan erőforrás-specifikus rekordot, amely miatt meghiúsul az óra-előrejelzésekkel való integráció.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="a8ea1-133">Szűrje ki az összes üres tranzakciós kategória sorát.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="a8ea1-134">A feladat végrehajtásának elmulasztása helytelen óra-előrejelzéseket eredményezhet.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a8ea1-135">Az alapértelmezett előrejelzési modell azonosítójának beállítása</span><span class="sxs-lookup"><span data-stu-id="a8ea1-135">Set the default forecast model ID</span></span>

<span data-ttu-id="a8ea1-136">A sablonban az alapértelmezett előrejelzési modell azonosítójának frissítéséhez kattintson a **Leképezés** nyílra a leképezés megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a8ea1-137">Ezután jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a8ea1-138">Ha az alapértelmezett Projekt órabecslései (PSA – Fin és Ops) sablont használja, akkor jelölje ki a **Beszúrt feltétel** lehetőséget az **Alkalmazott lépések** listájában.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="a8ea1-139">A **Funkció** bejegyzésében cserélje le au **O\_forecast** elemet az integrációval használni kívánt előrejelzési modell azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a8ea1-140">Az alapértelmezett sablon egy előrejelzési modell azonosítóval rendelkezik a demó adatokból.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a8ea1-141">Ha új sablont hoz létre, akkor ezt az oszlopot kell felvennie.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a8ea1-142">A Power Query alkalmazásban jelölje be a **Feltételes oszlop hozzáadása** jelölőnégyzetet, és adja meg az új oszlop nevét, például **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a8ea1-143">Adja meg az oszlop feltételeit, ahol ha a projektfeladat nem null, akkor \<adja meg az előrejelzési modell azonosítóját\> ; ellenkező esetben a null értéket.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="a8ea1-144">Erőforrás-specifikus bejegyzések kiszűrése</span><span class="sxs-lookup"><span data-stu-id="a8ea1-144">Filter out resource-specific records</span></span>

<span data-ttu-id="a8ea1-145">A Projekt órabecslései (PSA – Fin és Ops) sablon egy alapértelmezett szűrővel rendelkezik, amely eltávolítja az erőforrás-specifikus bejegyzéseket.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="a8ea1-146">Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a8ea1-147">Válassza ki a **Speciális lekérdezés és szűrés** hivatkozást a **msdyn\_islinetask** oszlop szűréséhez, hogy csak a **Hamis** rekordok maradjanak.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="a8ea1-148">Az üres tranzakciós kategória sorok kiszűrése</span><span class="sxs-lookup"><span data-stu-id="a8ea1-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="a8ea1-149">Hozzá kell adnia egy szűrőt az üres tranzakciós kategóriákat tartalmazó sorok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="a8ea1-150">Ez a feladat kötelező, függetlenül attól, hogy az alapértelmezett sablont használja-e, vagy saját sablont hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="a8ea1-151">Ez a szűrő eltávolítja a Project Service Automation minden összesítő sorát, amelyek miatt az óra-előrejelzések helytelenek lehetnek a Finance rendszerben.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="a8ea1-152">Válassza a **Speciális lekérdezés és szűrés** hivatkozást a null rekordok kiszűréséhez a **msdyn\_transactioncategory\_value** oszlopban.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a8ea1-153">Sablonok leképezése az adatintegrációban</span><span class="sxs-lookup"><span data-stu-id="a8ea1-153">Template mapping in Data integration</span></span>

<span data-ttu-id="a8ea1-154">A következő ábra egy példát mutat be az adatintegrációban az sablonfeladatok leképezésére.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a8ea1-155">A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a8ea1-156">[![Sablonok leképezése](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="a8ea1-157">Projekt költségbecslései</span><span class="sxs-lookup"><span data-stu-id="a8ea1-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="a8ea1-158">Sablon és feladatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-158">Template and tasks</span></span>

<span data-ttu-id="a8ea1-159">A következő sablon és a mögöttes feladatok segítségével szinkronizálhatja a projekt költségbecsléseit a Project Service Automation alkalmazásból a Finance rendszerbe:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a8ea1-160">**A sablon neve az adatintegrációban:** Projekt költségbecslései (PSA – Fin és Ops)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a8ea1-161">**A feladat neve a projektben:**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="a8ea1-162">Tranzakciókapcsolatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-162">Transaction relationships</span></span> 
    - <span data-ttu-id="a8ea1-163">Költség becslések</span><span class="sxs-lookup"><span data-stu-id="a8ea1-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="a8ea1-164">Entitáskészlet</span><span class="sxs-lookup"><span data-stu-id="a8ea1-164">Entity set</span></span>

| <span data-ttu-id="a8ea1-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a8ea1-165">Project Service Automation</span></span> | <span data-ttu-id="a8ea1-166">Pénzügy</span><span class="sxs-lookup"><span data-stu-id="a8ea1-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="a8ea1-167">Tranzakciós kapcsolatok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-167">Transaction Connections</span></span>    | <span data-ttu-id="a8ea1-168">A projekt tranzakciókapcsolatainak integrációs entitása</span><span class="sxs-lookup"><span data-stu-id="a8ea1-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="a8ea1-169">Becsléssorok</span><span class="sxs-lookup"><span data-stu-id="a8ea1-169">Estimate Lines</span></span>             | <span data-ttu-id="a8ea1-170">Integrációs entitás a projekt költségbecsléseihez</span><span class="sxs-lookup"><span data-stu-id="a8ea1-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="a8ea1-171">Entitásfolyam</span><span class="sxs-lookup"><span data-stu-id="a8ea1-171">Entity flow</span></span>

<span data-ttu-id="a8ea1-172">A projekt költségbecslései a Project Service Automation alkalmazásban kezelhetők, és a program projektköltség-előrejelzésekként szinkronizálja őket a Finance rendszerbe.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a8ea1-173">Előfeltételek</span><span class="sxs-lookup"><span data-stu-id="a8ea1-173">Prerequisites</span></span>

<span data-ttu-id="a8ea1-174">A projekt költségbecsléseinek szinkronizálása előtt szinkronizálnia kell a projekteket, a projektfeladatokat és a projekt költségeinek tranzakciós kategóriáit.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a8ea1-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="a8ea1-175">Power Query</span></span>

<span data-ttu-id="a8ea1-176">A projekt költségbecsléseinek sablonjában a Power Query használatával kell végrehajtania a következő feladatokat:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="a8ea1-177">Végezzen szűrést, hogy csak a költségbecslés sorrekordjai szerepeljenek.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="a8ea1-178">Állítsa be az alapértelmezett előrejelzési modell azonosítóját, amelyet akkor használ a rendszer, ha az integráció új óra-előrejelzéseket hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="a8ea1-179">Alakítsa át a számlázási típusokat.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-179">Transform the billing types.</span></span>
- <span data-ttu-id="a8ea1-180">Alakítsa át a tranzakciótípusokat.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="a8ea1-181">Szűrés, amellyel csak a költségbecslés sorai szerepelnek</span><span class="sxs-lookup"><span data-stu-id="a8ea1-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="a8ea1-182">A Projekt költségbecslései (PSA – Fin és Ops) sablon egy alapértelmezett szűrővel rendelkezik, amely csak az integrációban szereplő költségsorokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="a8ea1-183">Ha saját sablont hoz létre, akkor ezt a szűrőt kell hozzáadnia.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="a8ea1-184">Jelölje ki a **Tranzakciókapcsolatok** feladatot, majd kattintson a **Leképezés** nyílra a leképezés megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a8ea1-185">Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="a8ea1-186">Szűrje a **msdyn\_transactiontype1** oszlopot úgy, hogy csak a **msdyn\_estimateline** elemeket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="a8ea1-187">Az alapértelmezett előrejelzési modell azonosítójának beállítása</span><span class="sxs-lookup"><span data-stu-id="a8ea1-187">Set the default forecast model ID</span></span>

<span data-ttu-id="a8ea1-188">A sablonban az alapértelmezett előrejelzési modell azonosítójának frissítéséhez válassza a **Költségbecslések** feladatot, majd kattintson a **Leképezés** nyílra a leképezés megnyitásához.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="a8ea1-189">Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="a8ea1-190">Ha az alapértelmezett Projekt költségbecslései (PSA – Fin és Ops) sablont használja, akkor a Power Query alkalmazásban jelölje ki az első **Beszúrt feltétel** lehetőséget az **Alkalmazott lépések** szakaszból.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="a8ea1-191">A **Funkció** bejegyzésében cserélje le au **O\_forecast** elemet az integrációval használni kívánt előrejelzési modell azonosítójával.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="a8ea1-192">Az alapértelmezett sablon egy előrejelzési modell azonosítóval rendelkezik a demó adatokból.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="a8ea1-193">Ha új sablont hoz létre, akkor ezt az oszlopot kell felvennie.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="a8ea1-194">A Power Query alkalmazásban jelölje be a **Feltételes oszlop hozzáadása** jelölőnégyzetet, és adja meg az új oszlop nevét, például **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="a8ea1-195">Adja meg az oszlop feltételeit, ahol ha a Becslési sor azonosítója nem null, akkor \<adja meg az előrejelzési modell azonosítóját\> ; ellenkező esetben a null értéket.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="a8ea1-196">Számlázási típusok átalakítása</span><span class="sxs-lookup"><span data-stu-id="a8ea1-196">Transform the billing types</span></span>

<span data-ttu-id="a8ea1-197">A Projekt költségbecslései (PSA – Fin és Ops) sablonja tartalmaz egy feltételes oszlopot, amellyel átalakíthatja a Project Service Automation szolgáltatásból kapott számlázási típusokat az integráció során.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a8ea1-198">Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a8ea1-199">Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást, majd válassza a **Feltételes oszlop hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a8ea1-200">Adja meg az új oszlop nevét, például **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="a8ea1-201">Ezután adja meg a következő feltételt:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-201">Then enter the following condition:</span></span>

<span data-ttu-id="a8ea1-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="a8ea1-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="a8ea1-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="a8ea1-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="a8ea1-206">A tranzakciótípusok átalakítása</span><span class="sxs-lookup"><span data-stu-id="a8ea1-206">Transform the transaction types</span></span>

<span data-ttu-id="a8ea1-207">A Projekt költségbecslései (PSA – Fin és Ops) sablonja tartalmaz egy feltételes oszlopot, amellyel átalakíthatja a Project Service Automation szolgáltatásból kapott tranzakciótípusokat az integráció során.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="a8ea1-208">Ha saját sablont hoz létre, akkor ezt a feltételes oszlopot kell hozzáadnia.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="a8ea1-209">Jelölje ki a **Speciális lekérdezés és szűrés** hivatkozást, majd válassza a **Feltételes oszlop hozzáadása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="a8ea1-210">Adja meg az új oszlop nevét, például **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="a8ea1-211">Ezután adja meg a következő feltételt:</span><span class="sxs-lookup"><span data-stu-id="a8ea1-211">Then enter the following condition:</span></span>

<span data-ttu-id="a8ea1-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="a8ea1-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="a8ea1-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="a8ea1-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a8ea1-215">Sablonok leképezése az adatintegrációban</span><span class="sxs-lookup"><span data-stu-id="a8ea1-215">Template mapping in Data integration</span></span>

<span data-ttu-id="a8ea1-216">A következő ábra példákat mutat be az adatintegrációban az sablonfeladatok leképezésére.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="a8ea1-217">A leképezés azokat a mezőinformációkat mutatja, amelyek a Project Service Automation alkalmazásból a Finance rendszerbe lesznek szinkronizálva.</span><span class="sxs-lookup"><span data-stu-id="a8ea1-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a8ea1-218">[![Sablonok leképezése](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="a8ea1-219">[![Sablonok leképezése](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a8ea1-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
