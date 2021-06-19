---
title: Projekt másolása
description: Ez a témakör információkat nyújt a projektek másolásáról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091257"
---
# <a name="copy-a-project"></a><span data-ttu-id="7a76e-103">Projekt másolása</span><span class="sxs-lookup"><span data-stu-id="7a76e-103">Copy a project</span></span>

<span data-ttu-id="7a76e-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="7a76e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7a76e-105">A Dynamics 365 Project Operations segítségével gyorsan építhet új projekteket a **Projektek** űrlap **Projektek másolása** lehetőségének kiválasztásával.</span><span class="sxs-lookup"><span data-stu-id="7a76e-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="7a76e-106">Projekt másolásához nyissa meg a másolni kívánt projektet, majd válassza a **Projekt másolása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="7a76e-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="7a76e-107">A művelet a következőket másolja:</span><span class="sxs-lookup"><span data-stu-id="7a76e-107">The action will copy the following:</span></span>

- <span data-ttu-id="7a76e-108">Projekt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="7a76e-108">Project properties</span></span> 
- <span data-ttu-id="7a76e-109">Munkalebontási struktúra</span><span class="sxs-lookup"><span data-stu-id="7a76e-109">Work breakdown structure</span></span>
- <span data-ttu-id="7a76e-110">Projektcsoporttagok</span><span class="sxs-lookup"><span data-stu-id="7a76e-110">Project team members</span></span>
- <span data-ttu-id="7a76e-111">Projektbecslések</span><span class="sxs-lookup"><span data-stu-id="7a76e-111">Project estimates</span></span>
- <span data-ttu-id="7a76e-112">Projekt költségbecslései</span><span class="sxs-lookup"><span data-stu-id="7a76e-112">Project expense estimates</span></span>
- <span data-ttu-id="7a76e-113">Projektanyag-becslések</span><span class="sxs-lookup"><span data-stu-id="7a76e-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="7a76e-114">Projekt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="7a76e-114">Project properties</span></span>

<span data-ttu-id="7a76e-115">A projekt másolásakor a következő mezők értékei kerülnek másolásra:</span><span class="sxs-lookup"><span data-stu-id="7a76e-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="7a76e-116">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="7a76e-116">Name</span></span>
- <span data-ttu-id="7a76e-117">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="7a76e-117">Description</span></span>
- <span data-ttu-id="7a76e-118">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="7a76e-118">Customer</span></span>
- <span data-ttu-id="7a76e-119">Naptársablon</span><span class="sxs-lookup"><span data-stu-id="7a76e-119">Calendar Template</span></span>
- <span data-ttu-id="7a76e-120">Pénznem</span><span class="sxs-lookup"><span data-stu-id="7a76e-120">Currency</span></span>
- <span data-ttu-id="7a76e-121">Szerződő részleg</span><span class="sxs-lookup"><span data-stu-id="7a76e-121">Contracting Unit</span></span>
- <span data-ttu-id="7a76e-122">Projektmenedzser</span><span class="sxs-lookup"><span data-stu-id="7a76e-122">Project Manager</span></span>
- <span data-ttu-id="7a76e-123">Állapot</span><span class="sxs-lookup"><span data-stu-id="7a76e-123">Status</span></span>
- <span data-ttu-id="7a76e-124">Teljes projektállapot</span><span class="sxs-lookup"><span data-stu-id="7a76e-124">Overall Project Status</span></span>
- <span data-ttu-id="7a76e-125">Hozzászólások</span><span class="sxs-lookup"><span data-stu-id="7a76e-125">Comments</span></span>
- <span data-ttu-id="7a76e-126">Becslések</span><span class="sxs-lookup"><span data-stu-id="7a76e-126">Estimates</span></span>
- <span data-ttu-id="7a76e-127">Becsült kezdő dátum: Ez az a dátum, amikor a projektet létrehozzák a másolatból.</span><span class="sxs-lookup"><span data-stu-id="7a76e-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="7a76e-128">Becsült befejezési dátum: Az a program az másolatból készített új projekt kezdési dátumából van korrigálva.</span><span class="sxs-lookup"><span data-stu-id="7a76e-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="7a76e-129">Munkamennyiség (óra)</span><span class="sxs-lookup"><span data-stu-id="7a76e-129">Effort (Hours)</span></span>
- <span data-ttu-id="7a76e-130">Becsült munkaköltség</span><span class="sxs-lookup"><span data-stu-id="7a76e-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="7a76e-131">Becsült önköltség</span><span class="sxs-lookup"><span data-stu-id="7a76e-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="7a76e-132">Várható anyagköltség</span><span class="sxs-lookup"><span data-stu-id="7a76e-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="7a76e-133">A projekt másolása hosszú ideig futó művelet.</span><span class="sxs-lookup"><span data-stu-id="7a76e-133">Copy project is a long running operation.</span></span> <span data-ttu-id="7a76e-134">A rendszer a projektrekordokat, a kapcsolódó attribútumokat és számos kapcsolódó entitást is másol.</span><span class="sxs-lookup"><span data-stu-id="7a76e-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="7a76e-135">A művelet hosszú ideig futó jellege miatt a másolás indítása után a cél projekt oldala szerkesztésre zárolva van, amíg be nem fejeződik a másolási művelet.</span><span class="sxs-lookup"><span data-stu-id="7a76e-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="7a76e-136">Munkalebontási struktúra</span><span class="sxs-lookup"><span data-stu-id="7a76e-136">Work breakdown structure</span></span>

<span data-ttu-id="7a76e-137">A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik.</span><span class="sxs-lookup"><span data-stu-id="7a76e-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="7a76e-138">A megnevezett erőforrások helyébe általános erőforrások lépnek.</span><span class="sxs-lookup"><span data-stu-id="7a76e-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="7a76e-139">Ha a megnevezett erőforrások nem rendelkeznek az általános erőforrással megegyező munkaidővel, az ütemezés újraszámításra kerül, és a feladatok időtartama változhat.</span><span class="sxs-lookup"><span data-stu-id="7a76e-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="7a76e-140">Projektcsoporttagok</span><span class="sxs-lookup"><span data-stu-id="7a76e-140">Project team members</span></span>

<span data-ttu-id="7a76e-141">Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program.</span><span class="sxs-lookup"><span data-stu-id="7a76e-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="7a76e-142">Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak.</span><span class="sxs-lookup"><span data-stu-id="7a76e-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="7a76e-143">A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.</span><span class="sxs-lookup"><span data-stu-id="7a76e-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="7a76e-144">Becslések</span><span class="sxs-lookup"><span data-stu-id="7a76e-144">Estimates</span></span>

<span data-ttu-id="7a76e-145">A projekt másolása során a ez erőforrások, költségek és költségbecslési sorok a forrásprojektből vannak másolva.</span><span class="sxs-lookup"><span data-stu-id="7a76e-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="7a76e-146">A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="7a76e-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
