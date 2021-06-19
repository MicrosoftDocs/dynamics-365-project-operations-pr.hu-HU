---
title: Ütemezési módok
description: Ez a témakör az ütemezési módokkal kapcsolatban nyújt információkat.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116710"
---
# <a name="scheduling-modes"></a><span data-ttu-id="7a254-103">Ütemezési módok</span><span class="sxs-lookup"><span data-stu-id="7a254-103">Scheduling modes</span></span>

<span data-ttu-id="7a254-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="7a254-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7a254-105">A(z) Dynamics 365 Project Operations lehetővé teszi a szervezetek számára, hogy meghatározzák, hogyan kezelik a feladatok kulcsfontosságú változóinak változásait a munka lebontási struktúrájában.</span><span class="sxs-lookup"><span data-stu-id="7a254-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="7a254-106">A szervezet egyedi igényei alapján a projektmenedzserek módosíthatják az ütemezési módot a projekt létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="7a254-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="7a254-107">A Project Operations három ütemezési módból áll rendelkezésre:</span><span class="sxs-lookup"><span data-stu-id="7a254-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="7a254-108">Rögzített időtartam (ez az alapértelmezett mód)</span><span class="sxs-lookup"><span data-stu-id="7a254-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="7a254-109">Fix ráfordítás (*Munka*)</span><span class="sxs-lookup"><span data-stu-id="7a254-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="7a254-110">Rögzített egységek</span><span class="sxs-lookup"><span data-stu-id="7a254-110">Fixed units</span></span>

<span data-ttu-id="7a254-111">Az adott ütemezési mód meghatározásával érintett értékeket a következő képlet határozza meg:</span><span class="sxs-lookup"><span data-stu-id="7a254-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="7a254-112">Erőfeszítés = Időtartam x Egység</span><span class="sxs-lookup"><span data-stu-id="7a254-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="7a254-113">Amikor beállítja a projekt ütemezési módját, beállítja az alábbi értékek egyikét, amelyet ezután nem lehet módosítani.</span><span class="sxs-lookup"><span data-stu-id="7a254-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="7a254-114">Ha ezt az értéket állandóként tartjuk, az elsőbbséget élvez ezzel az értékkel, ami értesíti a rendszert, hogy a másik két érték változásakor ne változtassa meg azt.</span><span class="sxs-lookup"><span data-stu-id="7a254-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="7a254-115">Az alábbi táblázat egy adott mód kiválasztásának hatásairól ad tájékoztatást.</span><span class="sxs-lookup"><span data-stu-id="7a254-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="7a254-116">**Ebben a feladatban**</span><span class="sxs-lookup"><span data-stu-id="7a254-116">**In this task**</span></span>             | <span data-ttu-id="7a254-117">**Ha felülvizsgálja az egységeket**</span><span class="sxs-lookup"><span data-stu-id="7a254-117">**If you revise units**</span></span>   | <span data-ttu-id="7a254-118">**Ha felülvizsgálja az időtartamot**</span><span class="sxs-lookup"><span data-stu-id="7a254-118">**If you revise duration**</span></span> | <span data-ttu-id="7a254-119">**Ha felülvizsgálja a munkát**</span><span class="sxs-lookup"><span data-stu-id="7a254-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="7a254-120">Fix egységek feladata</span><span class="sxs-lookup"><span data-stu-id="7a254-120">Fixed units task</span></span>     | <span data-ttu-id="7a254-121">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="7a254-121">Duration is recalculated.</span></span> | <span data-ttu-id="7a254-122">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="7a254-122">Effort is recalculated.</span></span>    | <span data-ttu-id="7a254-123">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="7a254-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="7a254-124">Fix ráfordítású feladat</span><span class="sxs-lookup"><span data-stu-id="7a254-124">Fixed effort task</span></span>    | <span data-ttu-id="7a254-125">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="7a254-125">Duration is recalculated.</span></span> | <span data-ttu-id="7a254-126">Az egységek újraszámításra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="7a254-126">Units are recalculated.</span></span>    | <span data-ttu-id="7a254-127">Az időtartam újraszámításra kerül.</span><span class="sxs-lookup"><span data-stu-id="7a254-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="7a254-128">Fix időtartamú feladat</span><span class="sxs-lookup"><span data-stu-id="7a254-128">Fixed duration task</span></span>  | <span data-ttu-id="7a254-129">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="7a254-129">Effort is recalculated.</span></span>   | <span data-ttu-id="7a254-130">Az erőfeszítést újraszámolják.</span><span class="sxs-lookup"><span data-stu-id="7a254-130">Effort is recalculated.</span></span>    | <span data-ttu-id="7a254-131">Az egységek újraszámításra kerülnek.</span><span class="sxs-lookup"><span data-stu-id="7a254-131">Units are recalculated.</span></span>   |

<span data-ttu-id="7a254-132">Az adott mód következményeiről a [Feladattípus módosítása](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72) című lapon tájékozódhat a pontosabb ütemezésért.</span><span class="sxs-lookup"><span data-stu-id="7a254-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="7a254-133">A témakörben a **Munka** kifejezést használjuk **Erőfeszítés** helyett.</span><span class="sxs-lookup"><span data-stu-id="7a254-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="7a254-134">A szervezet ütemezési módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="7a254-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="7a254-135">Hajtsa végre a következő lépéseket a szervezet ütemezési módjának meghatározásához.</span><span class="sxs-lookup"><span data-stu-id="7a254-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="7a254-136">Válassza a **Beállítások** \> **Általános** \> **Paraméterek** menüpontot, majd válassza ki a projekt paraméterét.</span><span class="sxs-lookup"><span data-stu-id="7a254-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="7a254-137">A **Projektparaméterek** lapon jelölje ki a szervezet alapértelmezett ütemezési módját, majd határozza meg, hogy a projektmenedzser felülbírálhatja-e a beállítást új projekt létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="7a254-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="7a254-138">Projekt ütemezési módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="7a254-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="7a254-139">Ha egy szervezet lehetővé teszi a projektmenedzser számára, hogy felülbírálja az alapértelmezett ütemezési módot, a Projektmenedzser módosíthatja ezt a módosítást, amikor új projektet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7a254-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="7a254-140">A projekt mentése után azonban az ütemezési mód nem módosítható.</span><span class="sxs-lookup"><span data-stu-id="7a254-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="7a254-141">Átmásolt projektek</span><span class="sxs-lookup"><span data-stu-id="7a254-141">Copied projects</span></span>

<span data-ttu-id="7a254-142">Mivel a projekt másolása a projekt másolása közben jön létre, a projektmenedzser nem tudja beállítani az ütemezési módot.</span><span class="sxs-lookup"><span data-stu-id="7a254-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="7a254-143">A célprojekt mindig a szervezeti szinten meghatározott mód szerint fog alapértelmezett lenni.</span><span class="sxs-lookup"><span data-stu-id="7a254-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="7a254-144">Átmásolt feladatok</span><span class="sxs-lookup"><span data-stu-id="7a254-144">Copied tasks</span></span>

<span data-ttu-id="7a254-145">Ha egy tevékenység átmásolódik egyik projektből a másikba, a tevékenység örökli a célprojekt ütemezési módját.</span><span class="sxs-lookup"><span data-stu-id="7a254-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
