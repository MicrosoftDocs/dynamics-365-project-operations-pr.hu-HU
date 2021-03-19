---
title: Előrejelzési modellek létrehozása a projektköltségvetésekhez
description: Ez a témakör ismerteti, hogyan lehet előrejelzési modellt létrehozni a fennmaradó költségvetésekhez.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271041"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="c6339-103">Előrejelzési modellek létrehozása a projektköltségvetésekhez</span><span class="sxs-lookup"><span data-stu-id="c6339-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6339-104">Ez a témakör ismerteti, hogyan lehet előrejelzési modellt létrehozni a fennmaradó költségvetésekhez.</span><span class="sxs-lookup"><span data-stu-id="c6339-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="c6339-105">Egy költségvetés-ellenőrzés alá tartozó projekt a következő két típusú költségvetést használja: eredeti és fennmaradó.</span><span class="sxs-lookup"><span data-stu-id="c6339-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="c6339-106">A projektek költségvetésének létrehozásakor meg kell adnia az **Előrejelzési modellek** lapon létrehozott eredeti és fennmaradó költségvetési előrejelzési modelleket.</span><span class="sxs-lookup"><span data-stu-id="c6339-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="c6339-107">A projektek költségvetések a megadott modellek alapján jönnek létre, amikor véglegesíti a projekt költségvetését.</span><span class="sxs-lookup"><span data-stu-id="c6339-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="c6339-108">A költségvetés-ellenőrzéshez használt előrejelzési modell nem lehet almodell vagy nem használható almodellként.</span><span class="sxs-lookup"><span data-stu-id="c6339-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="c6339-109">Válassza a **Projektmenedzsment és könyvelés** > **Beállítások** > **Előrejelzések**  > **Előrejelzési modellek** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c6339-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="c6339-110">Új előrejelzési modell létrehozásához válassza az **Új** lehetőséget, majd adja meg az új modellhez tartozó modellszámot és nevet.</span><span class="sxs-lookup"><span data-stu-id="c6339-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="c6339-111">Állítsa be a **Leállítva** beállítást **Igen** értékre az előrejelzési modellre vonatkozó előrejelzési sorok módosulásának elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="c6339-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="c6339-112">Ha a modellhez társított előrejelzési sorokban pénzforgalmi előrejelzéseket kell létrehoznia a főkönyvben, akkor állítsa be a **Pénzforgalmi előrejelzések befoglalása** beállítást **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="c6339-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="c6339-113">Ha a projekt dátumát szeretné számlázási dátumként használni, akkor állítsa az **Előrejelzési számla dátuma** beállítást **Igen** értékre.</span><span class="sxs-lookup"><span data-stu-id="c6339-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="c6339-114">A **Költségvetés típusa** mezőben válassza ki a következő modelltípusok egyikét:</span><span class="sxs-lookup"><span data-stu-id="c6339-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="c6339-115">**Eredeti költségvetés**: A kezdeti költségvetés létrehozásakor és jóváhagyásakor meghatározott eredeti költségvetési összegek használata.</span><span class="sxs-lookup"><span data-stu-id="c6339-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="c6339-116">**Fennmaradó költségvetés**: A projekt élettartama során a fennmaradó költségvetési összegeket használja.</span><span class="sxs-lookup"><span data-stu-id="c6339-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="c6339-117">Az ebben az előrejelzési modellben szereplő egyenlegeket a rendszer a tényleges tranzakciókkal csökkenti, és a költségvetési módosítások szerint növeli vagy csökkenti.</span><span class="sxs-lookup"><span data-stu-id="c6339-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="c6339-118">**Átvitel**: A projekthez tartozó átviteli költségvetés összegeit használja.</span><span class="sxs-lookup"><span data-stu-id="c6339-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="c6339-119">Az átvitel egy opcionálisfolyamat, amely a fel nem használt költségvetési összegek átvitelére szolgál az egyik pénzügyi évből a másikba.</span><span class="sxs-lookup"><span data-stu-id="c6339-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="c6339-120">Végezze el a következő beállításokat igény szerint:</span><span class="sxs-lookup"><span data-stu-id="c6339-120">Set the following options as required:</span></span>

   - <span data-ttu-id="c6339-121">Ha a projekt dátumát szeretné számlázási dátumként használni, akkor használja az **Előrejelzési számla dátuma** beállítást.</span><span class="sxs-lookup"><span data-stu-id="c6339-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="c6339-122">Engedélyezze az **Előrejelzés folyamatban lévő munkával** lehetőséget, hogy előrejelzést készítsen folyamatban lévő munka alapján, majd válassza ki a folyamatban lévő munka típusát.</span><span class="sxs-lookup"><span data-stu-id="c6339-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="c6339-123">Az alapértelmezett **Költségvetési** típust **Nincs** értékként hagyhatja, vagy új típust adhat meg.</span><span class="sxs-lookup"><span data-stu-id="c6339-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="c6339-124">A költségvetés típusa a rekord módosítása után nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="c6339-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="c6339-125">Ha módosítja az alapértelmezett költségvetési típust, akkor az összes többi lehetőség nem lesz elérhető a frissítésekhez, és ez az előrejelzési modell nem használható fel újra.</span><span class="sxs-lookup"><span data-stu-id="c6339-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]