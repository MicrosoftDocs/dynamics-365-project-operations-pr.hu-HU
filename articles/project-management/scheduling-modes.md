---
title: Ütemezési módok
description: Ez a témakör az ütemezési módokkal kapcsolatban nyújt információkat.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981438"
---
# <a name="scheduling-modes"></a><span data-ttu-id="934a4-103">Ütemezési módok</span><span class="sxs-lookup"><span data-stu-id="934a4-103">Scheduling modes</span></span>

<span data-ttu-id="934a4-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="934a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="934a4-105">A(z) Dynamics 365 Project Operations lehetővé teszi a szervezetek számára, hogy meghatározzák, hogyan kezelik a feladatok kulcsfontosságú változóinak változásait a munka lebontási struktúrájában.</span><span class="sxs-lookup"><span data-stu-id="934a4-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="934a4-106">A szervezet egyedi igényei alapján a projektmenedzserek módosíthatják az ütemezési módot a projekt létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="934a4-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="934a4-107">A Project Operations három ütemezési módból áll rendelkezésre:</span><span class="sxs-lookup"><span data-stu-id="934a4-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="934a4-108">Rögzített időtartam (ez az alapértelmezett mód)</span><span class="sxs-lookup"><span data-stu-id="934a4-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="934a4-109">Rögzített munka</span><span class="sxs-lookup"><span data-stu-id="934a4-109">Fixed work</span></span>
  - <span data-ttu-id="934a4-110">Rögzített egységek</span><span class="sxs-lookup"><span data-stu-id="934a4-110">Fixed units</span></span>

<span data-ttu-id="934a4-111">Az adott ütemezési mód meghatározásával érintett értékeket a következő képlet határozza meg:</span><span class="sxs-lookup"><span data-stu-id="934a4-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="934a4-112">Erőfeszítés ( *Munka* ) = Időtartam x Egységek</span><span class="sxs-lookup"><span data-stu-id="934a4-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="934a4-113">Amikor beállítja a projekt ütemezési módját, beállítja az alábbi értékek egyikét, amelyet ezután nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="934a4-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="934a4-114">Ha ezt az értéket állandóként tartjuk, az elsőbbséget élvez ezzel az értékkel, ami értesíti a rendszert, hogy a másik két érték változásakor ne változtassa meg azt.</span><span class="sxs-lookup"><span data-stu-id="934a4-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="934a4-115">Az alábbi táblázat egy adott mód kiválasztásának hatásairól ad tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="934a4-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="934a4-116">**Ebben a feladatban**</span><span class="sxs-lookup"><span data-stu-id="934a4-116">**In this task**</span></span>             | <span data-ttu-id="934a4-117">**Ha felülvizsgálja az egységeket**</span><span class="sxs-lookup"><span data-stu-id="934a4-117">**If you revise units**</span></span>   | <span data-ttu-id="934a4-118">**Ha felülvizsgálja az időtartamot**</span><span class="sxs-lookup"><span data-stu-id="934a4-118">**If you revise duration**</span></span> | <span data-ttu-id="934a4-119">**Ha felülvizsgálja a munkát**</span><span class="sxs-lookup"><span data-stu-id="934a4-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="934a4-120">Fix egységek feladata</span><span class="sxs-lookup"><span data-stu-id="934a4-120">Fixed units task</span></span>     | <span data-ttu-id="934a4-121">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="934a4-121">Duration is recalculated.</span></span> | <span data-ttu-id="934a4-122">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="934a4-122">Effort is recalculated.</span></span>    | <span data-ttu-id="934a4-123">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="934a4-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="934a4-124">Fix ráfordítású feladat</span><span class="sxs-lookup"><span data-stu-id="934a4-124">Fixed effort task</span></span>    | <span data-ttu-id="934a4-125">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="934a4-125">Duration is recalculated.</span></span> | <span data-ttu-id="934a4-126">Az egységek újraszámításra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="934a4-126">Units are recalculated.</span></span>    | <span data-ttu-id="934a4-127">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="934a4-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="934a4-128">Fix időtartamú feladat</span><span class="sxs-lookup"><span data-stu-id="934a4-128">Fixed duration task</span></span>  | <span data-ttu-id="934a4-129">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="934a4-129">Effort is recalculated.</span></span>   | <span data-ttu-id="934a4-130">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="934a4-130">Effort is recalculated.</span></span>    | <span data-ttu-id="934a4-131">Az egységek újraszámításra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="934a4-131">Units are recalculated.</span></span>   |

<span data-ttu-id="934a4-132">Az adott mód következményeiről a [Feladattípus módosítása](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72) című lapon tájékozódhat a pontosabb ütemezésért.</span><span class="sxs-lookup"><span data-stu-id="934a4-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="934a4-133">A témakörben a **Munka** kifejezést használjuk **Erőfeszítés** helyett.</span><span class="sxs-lookup"><span data-stu-id="934a4-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="934a4-134">A szervezet ütemezési módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="934a4-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="934a4-135">Hajtsa végre a következő lépéseket a szervezet ütemezési módjának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="934a4-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="934a4-136">Válassza a **Beállítások** \> **Általános** \> **Paraméterek** menüpontot, majd válassza ki a projekt paraméterét.</span><span class="sxs-lookup"><span data-stu-id="934a4-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="934a4-137">A **Projektparaméterek** lapon jelölje ki a szervezet alapértelmezett ütemezési módját, majd határozza meg, hogy a projektmenedzser felülbírálhatja-e a beállítást új projekt létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="934a4-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="934a4-138">Projekt ütemezési módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="934a4-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="934a4-139">Ha egy szervezet lehetővé teszi a projektmenedzser számára, hogy felülbírálja az alapértelmezett ütemezési módot, a Projektmenedzser módosíthatja ezt a módosítást, amikor új projektet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="934a4-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="934a4-140">A projekt mentése után azonban az ütemezési mód nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="934a4-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="934a4-141">Átmásolt projektek</span><span class="sxs-lookup"><span data-stu-id="934a4-141">Copied projects</span></span>

<span data-ttu-id="934a4-142">Mivel a projekt másolása a projekt másolása közben jön létre, a projektmenedzser nem tudja beállítani az ütemezési módot.</span><span class="sxs-lookup"><span data-stu-id="934a4-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="934a4-143">A célprojekt mindig a szervezeti szinten meghatározott mód szerint fog alapértelmezett lenni.</span><span class="sxs-lookup"><span data-stu-id="934a4-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="934a4-144">Átmásolt feladatok</span><span class="sxs-lookup"><span data-stu-id="934a4-144">Copied tasks</span></span>

<span data-ttu-id="934a4-145">Ha egy tevékenység átmásolódik egyik projektből a másikba, a tevékenység örökli a célprojekt ütemezési módját.</span><span class="sxs-lookup"><span data-stu-id="934a4-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
