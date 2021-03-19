---
title: Erőforrás-menedzsment változások (Project Service Automation 3.x)
description: Ez a témakör az erőforrás-kezelési terület változásairól nyújt információkat.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284766"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="41902-103">Erőforrás-menedzsment változások (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="41902-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="41902-104">A témakör szakaszai információkat tartalmaznak a Dynamics 365 Project Service Automation 3.x. változat erőforrás-kezelési területén végrehajtott változásokról.</span><span class="sxs-lookup"><span data-stu-id="41902-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="41902-105">Projektbecslések</span><span class="sxs-lookup"><span data-stu-id="41902-105">Project estimates</span></span>

<span data-ttu-id="41902-106">Az **msdyn\_projecttask** entitás **(Projektfeladat**) helyett a projektbecslések az **msdyn\_resourceassignment** entitáson alapulnak (**Erőforrás hozzárendelés**).</span><span class="sxs-lookup"><span data-stu-id="41902-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="41902-107">Az erőforrás-hozzárendelések váltak az igazság forrásává a feladatok ütemezése és árazása során.</span><span class="sxs-lookup"><span data-stu-id="41902-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="41902-108">Sori feladatok</span><span class="sxs-lookup"><span data-stu-id="41902-108">Line tasks</span></span>

<span data-ttu-id="41902-109">A PSA 3.x-ben a sorfeladatok elavultak (elavultak).</span><span class="sxs-lookup"><span data-stu-id="41902-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="41902-110">A hozzárendelések a soros feladatok helyett az egész feladatra mutatnak.</span><span class="sxs-lookup"><span data-stu-id="41902-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="41902-111">A következő példa bemutatja, hogy a PSA korábbi verzióiban és a PSA 3.x-ben egy „Tesztfeladat” elnevezésű feladatot kapnak az A és B csapat tagjai.</span><span class="sxs-lookup"><span data-stu-id="41902-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="41902-112">**A PSA 3.x előtt:**</span><span class="sxs-lookup"><span data-stu-id="41902-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="41902-113">Tesztfeladat</span><span class="sxs-lookup"><span data-stu-id="41902-113">Test task</span></span>

        - <span data-ttu-id="41902-114">Tesztfeladat - 1. sorfeladat</span><span class="sxs-lookup"><span data-stu-id="41902-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="41902-115">Hozzárendelés az A-hoz</span><span class="sxs-lookup"><span data-stu-id="41902-115">Assignment to A</span></span>

        - <span data-ttu-id="41902-116">Tesztfeladat - 2. sorfeladat</span><span class="sxs-lookup"><span data-stu-id="41902-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="41902-117">Hozzárendelés a B-hoz</span><span class="sxs-lookup"><span data-stu-id="41902-117">Assignment to B</span></span>

- <span data-ttu-id="41902-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="41902-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="41902-119">Tesztfeladat</span><span class="sxs-lookup"><span data-stu-id="41902-119">Test task</span></span>

        - <span data-ttu-id="41902-120">Hozzárendelés az A-hoz</span><span class="sxs-lookup"><span data-stu-id="41902-120">Assignment to A</span></span>
        - <span data-ttu-id="41902-121">Hozzárendelés a B-hoz</span><span class="sxs-lookup"><span data-stu-id="41902-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="41902-122">Nincs hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="41902-122">Unassigned assignment</span></span>

<span data-ttu-id="41902-123">A PSA 3.x-ben a hozzá nem rendelt hozzárendelés egy olyan hozzárendelés, amelyet egy **NULL** csapattaghoz és **NULL** erőforráshoz rendelnek.</span><span class="sxs-lookup"><span data-stu-id="41902-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="41902-124">Rendeletlen hozzárendelések fordulhatnak elő néhány esetben:</span><span class="sxs-lookup"><span data-stu-id="41902-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="41902-125">Ha létrehoztunk egy feladatot, de még nem adták hozzá senkihez a csapat tagjaihoz, akkor mindig hozzárendelés nélküli hozzárendelést hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="41902-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="41902-126">Ha egy feladat összes megbízottját eltávolítják, akkor hozzárendelés nélküli hozzárendelést hoz létre a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="41902-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="41902-127">A mezők ütemezése a Project Task entitáson</span><span class="sxs-lookup"><span data-stu-id="41902-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="41902-128">Az **msdyn\_projecttask** entitás mezői elavultak vagy átkerültek az **msdyn\_resourceassignment** entitásba, vagy most hivatkoznak ezekre a **msdyn\_projectteam** entitásból (**Project Team Member**).</span><span class="sxs-lookup"><span data-stu-id="41902-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="41902-129">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="41902-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="41902-130">Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés)</span><span class="sxs-lookup"><span data-stu-id="41902-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="41902-131">Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="41902-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="41902-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="41902-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="41902-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="41902-133">None</span></span> | |
| <span data-ttu-id="41902-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="41902-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="41902-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="41902-135">None</span></span> | |
| <span data-ttu-id="41902-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="41902-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="41902-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="41902-137">None</span></span> | |
| <span data-ttu-id="41902-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="41902-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="41902-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="41902-139">None</span></span> | |
| <span data-ttu-id="41902-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="41902-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="41902-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="41902-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="41902-142">A mezőben tárolt JavaScript Object Notation (JSON) adatszerkezet formátuma megváltozott.</span><span class="sxs-lookup"><span data-stu-id="41902-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="41902-143">Ütemezéskontúr</span><span class="sxs-lookup"><span data-stu-id="41902-143">Schedule contour</span></span>

<span data-ttu-id="41902-144">Az ütemezéskontúr van tárolva a **Tervezett munka** mezőben (**msdyn\_plannedwork**) az egyes **Erőforrás-hozzárendelés** egységekben (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="41902-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="41902-145">Struktúra</span><span class="sxs-lookup"><span data-stu-id="41902-145">Structure</span></span>

<span data-ttu-id="41902-146">Az ütemezési kontúr új struktúrája rugalmas időszeletekből áll, amelyeket az ütemterv minden napjára meghatároznak.</span><span class="sxs-lookup"><span data-stu-id="41902-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="41902-147">Minden egyes szeletnek a következő tulajdonságai vannak:</span><span class="sxs-lookup"><span data-stu-id="41902-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="41902-148">**Kezdés** - megkezdődik a munkaidő a nap szerint a projekt naptár.</span><span class="sxs-lookup"><span data-stu-id="41902-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="41902-149">**Vége** - A napi munkaidő vége a projektnaptár szerint.</span><span class="sxs-lookup"><span data-stu-id="41902-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="41902-150">**Órák** - A napra kijelölt órák száma.</span><span class="sxs-lookup"><span data-stu-id="41902-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="41902-151">**Példa**</span><span class="sxs-lookup"><span data-stu-id="41902-151">**Example**</span></span>

<span data-ttu-id="41902-152">Ez a példa egy olyan projektnaptárt használ, ahol a munkanap 9:00 és 17:00 között van az UTC-8 időzónában.</span><span class="sxs-lookup"><span data-stu-id="41902-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="41902-153">Automatikus ütemezés és kézi ütemezés</span><span class="sxs-lookup"><span data-stu-id="41902-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="41902-154">Ha egy feladat automatikus ütemezése van, az órák előre vannak töltve, és a feladat időtartama csökkenhet.</span><span class="sxs-lookup"><span data-stu-id="41902-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="41902-155">**Példa**</span><span class="sxs-lookup"><span data-stu-id="41902-155">**Example**</span></span>

<span data-ttu-id="41902-156">A következő feladat automatikusan ütemeződik 18 órára három nap alatt (2018. december 3., 2018. december 5.).</span><span class="sxs-lookup"><span data-stu-id="41902-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="41902-157">Ha egy feladatot manuálisan ütemeznek, akkor az órák egyenletesen oszlanak meg az összes dátumra.</span><span class="sxs-lookup"><span data-stu-id="41902-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="41902-158">**Példa**</span><span class="sxs-lookup"><span data-stu-id="41902-158">**Example**</span></span>

<span data-ttu-id="41902-159">A következő feladatot kézzel, 18 órás időtartamra tervezzük három nap alatt (2018. december 3., 2018. december 5.).</span><span class="sxs-lookup"><span data-stu-id="41902-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="41902-160">Hozzárendelési egység</span><span class="sxs-lookup"><span data-stu-id="41902-160">Assignment unit</span></span>

<span data-ttu-id="41902-161">A hozzárendelési egység elavult a PSA 3.x-ben.</span><span class="sxs-lookup"><span data-stu-id="41902-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="41902-162">A feladat elvégzésének órái napi módon egyenlően oszlanak meg az összes hozzárendelt erőforrás között.</span><span class="sxs-lookup"><span data-stu-id="41902-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="41902-163">**Példa**</span><span class="sxs-lookup"><span data-stu-id="41902-163">**Example**</span></span>

<span data-ttu-id="41902-164">Ebben a példában a feladatot két erőforráshoz rendelik, és automatikusan ütemezik 36 órára három nap alatt (2018. december 3-tól 2018. december 5-ig).</span><span class="sxs-lookup"><span data-stu-id="41902-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="41902-165">1. feladat:</span><span class="sxs-lookup"><span data-stu-id="41902-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="41902-166">2. feladat:</span><span class="sxs-lookup"><span data-stu-id="41902-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="41902-167">Árképzési dimenziók</span><span class="sxs-lookup"><span data-stu-id="41902-167">Pricing dimensions</span></span>

<span data-ttu-id="41902-168">A PSA 3.x alkalmazásban az erőforrás-specifikus árazási dimenziós mezőket (például **Szerep** és **Szervezeti egység**) eltávolították a **msdyn\_projecttask** entitásból.</span><span class="sxs-lookup"><span data-stu-id="41902-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="41902-169">Ezek a mezők előhívhatók a megfelelő projekt csapat tagjából (**msdyn\_projectteam**) a erőforrás hozzárendelés (**msdyn\_resourceassignment**), amikor a projekt becslések keletkeznek.</span><span class="sxs-lookup"><span data-stu-id="41902-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="41902-170">Egy új mező, az **msdyn\_organizationalunit** került hozzáadásra az **msdyn\_projectteam** entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="41902-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="41902-171">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="41902-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="41902-172">A helyette használt msdyn\_projectteam (Project Team Member)</span><span class="sxs-lookup"><span data-stu-id="41902-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="41902-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="41902-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="41902-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="41902-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="41902-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="41902-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="41902-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="41902-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="41902-177">Kontúrok</span><span class="sxs-lookup"><span data-stu-id="41902-177">Contours</span></span>

<span data-ttu-id="41902-178">Az árazási és becslési kontúrmezők elavultak az **msdyn\_projecttask** entitáson.</span><span class="sxs-lookup"><span data-stu-id="41902-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="41902-179">Áthelyezték őket az **msdyn\_resourceassignment** entitásba.</span><span class="sxs-lookup"><span data-stu-id="41902-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="41902-180">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="41902-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="41902-181">Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés)</span><span class="sxs-lookup"><span data-stu-id="41902-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="41902-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="41902-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="41902-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="41902-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="41902-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="41902-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="41902-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="41902-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="41902-186">A következő mezők kerültek hozzáadásra az **msdyn\_resourceassignment** entitáshoz:</span><span class="sxs-lookup"><span data-stu-id="41902-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="41902-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="41902-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="41902-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="41902-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="41902-189">A tervezett, a tényleges és a fennmaradó költségek és az értékesítés alábbi mezői nem változnak az **msdyn\_projecttask** entitáson:</span><span class="sxs-lookup"><span data-stu-id="41902-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="41902-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="41902-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="41902-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="41902-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="41902-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="41902-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="41902-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="41902-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="41902-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="41902-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="41902-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="41902-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]