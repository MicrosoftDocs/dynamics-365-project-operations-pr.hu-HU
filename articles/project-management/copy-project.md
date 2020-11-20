---
title: Projekt másolása
description: Ez a témakör információkat nyújt a projektek másolásáról a Dynamics 365 Project Operations alkalmazásban.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131796"
---
# <a name="copy-a-project"></a><span data-ttu-id="11867-103">Projekt másolása</span><span class="sxs-lookup"><span data-stu-id="11867-103">Copy a project</span></span>

<span data-ttu-id="11867-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="11867-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11867-105">A Dynamics 365 Project Operations segítségével gyorsan létrehozhat új projekteket a **Projekt másolása** művelet kiválasztásával a **Projektek** űrlapon.</span><span class="sxs-lookup"><span data-stu-id="11867-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="11867-106">Projekt másolásához nyissa meg a másolni kívánt projektet, majd válassza a **Projekt másolása** lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="11867-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="11867-107">A művelet a következőket másolja:</span><span class="sxs-lookup"><span data-stu-id="11867-107">The action will copy:</span></span>

- <span data-ttu-id="11867-108">Projekt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="11867-108">Project properties</span></span>
- <span data-ttu-id="11867-109">A munkalebontási struktúra</span><span class="sxs-lookup"><span data-stu-id="11867-109">The Work breakdown structure</span></span>
- <span data-ttu-id="11867-110">Projektcsoporttagok</span><span class="sxs-lookup"><span data-stu-id="11867-110">Project team members</span></span>
- <span data-ttu-id="11867-111">Projektbecslések</span><span class="sxs-lookup"><span data-stu-id="11867-111">Project estimates</span></span>
- <span data-ttu-id="11867-112">Projekt költségbecslései</span><span class="sxs-lookup"><span data-stu-id="11867-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="11867-113">Projekt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="11867-113">Project properties</span></span>

<span data-ttu-id="11867-114">A projekt másolásakor a következő mezők értékei kerülnek másolásra:</span><span class="sxs-lookup"><span data-stu-id="11867-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="11867-115">Adatfolyam neve</span><span class="sxs-lookup"><span data-stu-id="11867-115">Name</span></span>
- <span data-ttu-id="11867-116">Adatfolyam leírása</span><span class="sxs-lookup"><span data-stu-id="11867-116">Description</span></span>
- <span data-ttu-id="11867-117">Ügyfél</span><span class="sxs-lookup"><span data-stu-id="11867-117">Customer</span></span>
- <span data-ttu-id="11867-118">Naptársablon</span><span class="sxs-lookup"><span data-stu-id="11867-118">Calendar Template</span></span>
- <span data-ttu-id="11867-119">Pénznem</span><span class="sxs-lookup"><span data-stu-id="11867-119">Currency</span></span>
- <span data-ttu-id="11867-120">Szerződő részleg</span><span class="sxs-lookup"><span data-stu-id="11867-120">Contracting Unit</span></span>
- <span data-ttu-id="11867-121">Projektmenedzser</span><span class="sxs-lookup"><span data-stu-id="11867-121">Project Manager</span></span>
- <span data-ttu-id="11867-122">Állapot</span><span class="sxs-lookup"><span data-stu-id="11867-122">Status</span></span>
- <span data-ttu-id="11867-123">Teljes projektállapot</span><span class="sxs-lookup"><span data-stu-id="11867-123">Overall Project Status</span></span>
- <span data-ttu-id="11867-124">Hozzászólások</span><span class="sxs-lookup"><span data-stu-id="11867-124">Comments</span></span>
- <span data-ttu-id="11867-125">Becslések</span><span class="sxs-lookup"><span data-stu-id="11867-125">Estimates</span></span>
- <span data-ttu-id="11867-126">Becsült kezdő dátum</span><span class="sxs-lookup"><span data-stu-id="11867-126">Estimated Start Date</span></span>
- <span data-ttu-id="11867-127">Befejezési dátum</span><span class="sxs-lookup"><span data-stu-id="11867-127">Finish Date</span></span>
- <span data-ttu-id="11867-128">Munkamennyiség (óra)</span><span class="sxs-lookup"><span data-stu-id="11867-128">Effort (Hours)</span></span>
- <span data-ttu-id="11867-129">Becsült munkaköltség</span><span class="sxs-lookup"><span data-stu-id="11867-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="11867-130">Becsült önköltség</span><span class="sxs-lookup"><span data-stu-id="11867-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="11867-131">Munkalebontási struktúra</span><span class="sxs-lookup"><span data-stu-id="11867-131">Work breakdown structure</span></span>

<span data-ttu-id="11867-132">A projekt másolásakor a teljes erőforrásokkal feltöltött munkalebontási struktúra másolódik.</span><span class="sxs-lookup"><span data-stu-id="11867-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="11867-133">A megnevezett erőforrások helyébe általános erőforrások lépnek.</span><span class="sxs-lookup"><span data-stu-id="11867-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="11867-134">Ha a megnevezett erőforrások nem rendelkeznek az általános erőforrással megegyező munkaidővel, az ütemezés újraszámításra kerül, és a feladatok időtartama változhat.</span><span class="sxs-lookup"><span data-stu-id="11867-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="11867-135">Projektcsoporttagok</span><span class="sxs-lookup"><span data-stu-id="11867-135">Project team members</span></span>

<span data-ttu-id="11867-136">Amikor egy projektcsoportot a forrásprojektből másol, az általános erőforrásokat átmásolja a program.</span><span class="sxs-lookup"><span data-stu-id="11867-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="11867-137">Az általános erőforrások hozzárendelései szintén megmaradnak, ahogy a forrásprojektben voltak.</span><span class="sxs-lookup"><span data-stu-id="11867-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="11867-138">A megnevezett erőforrásokat a rendszer általános csapattagokká alakítja.</span><span class="sxs-lookup"><span data-stu-id="11867-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="11867-139">Becslések</span><span class="sxs-lookup"><span data-stu-id="11867-139">Estimates</span></span>

<span data-ttu-id="11867-140">A projekt másolásakor az erőforrás- és költségbecslési sorok is átkerülnek a forrásprojektből.</span><span class="sxs-lookup"><span data-stu-id="11867-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="11867-141">A projektek másolásának programozott elérésével kapcsolatos tudnivalók a [Projektsablonok fejlesztése a Projekt másolásával](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="11867-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
