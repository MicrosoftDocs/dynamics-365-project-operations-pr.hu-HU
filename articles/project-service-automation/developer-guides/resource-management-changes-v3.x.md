---
title: Erőforrás-menedzsment változások (Project Service Automation 3.x)
description: Ez a témakör az erőforrás-kezelési terület változásairól nyújt információkat.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752243"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="c62be-103">Erőforrás-menedzsment változások (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="c62be-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="c62be-104">A témakör szakaszai információkat tartalmaznak a Dynamics 365 Project Service Automation 3.x. változat erőforrás-kezelési területén végrehajtott változásokról.</span><span class="sxs-lookup"><span data-stu-id="c62be-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="c62be-105">Projektbecslések</span><span class="sxs-lookup"><span data-stu-id="c62be-105">Project estimates</span></span>

<span data-ttu-id="c62be-106">Az **msdyn\_projecttask** entitás **(Projektfeladat**) helyett a projektbecslések az **msdyn\_resourceassignment** entitáson alapulnak **(Erőforrás hozzárendelés**).</span><span class="sxs-lookup"><span data-stu-id="c62be-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="c62be-107">Az erőforrás-hozzárendelések váltak az igazság forrásává a feladatok ütemezése és árazása során.</span><span class="sxs-lookup"><span data-stu-id="c62be-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="c62be-108">Sori feladatok</span><span class="sxs-lookup"><span data-stu-id="c62be-108">Line tasks</span></span>

<span data-ttu-id="c62be-109">A PSA 3.x-ben a sorfeladatok elavultak (elavultak).</span><span class="sxs-lookup"><span data-stu-id="c62be-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="c62be-110">A hozzárendelések a soros feladatok helyett az egész feladatra mutatnak.</span><span class="sxs-lookup"><span data-stu-id="c62be-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="c62be-111">A következő példa bemutatja, hogy a PSA korábbi verzióiban és a PSA 3.x-ben egy „Tesztfeladat” elnevezésű feladatot kapnak az A és B csapat tagjai.</span><span class="sxs-lookup"><span data-stu-id="c62be-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="c62be-112">**A PSA 3.x előtt:**</span><span class="sxs-lookup"><span data-stu-id="c62be-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="c62be-113">Tesztfeladat</span><span class="sxs-lookup"><span data-stu-id="c62be-113">Test task</span></span>

        - <span data-ttu-id="c62be-114">Tesztfeladat - 1. sorfeladat</span><span class="sxs-lookup"><span data-stu-id="c62be-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="c62be-115">Hozzárendelés az A-hoz</span><span class="sxs-lookup"><span data-stu-id="c62be-115">Assignment to A</span></span>

        - <span data-ttu-id="c62be-116">Tesztfeladat - 2. sorfeladat</span><span class="sxs-lookup"><span data-stu-id="c62be-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="c62be-117">Hozzárendelés a B-hoz</span><span class="sxs-lookup"><span data-stu-id="c62be-117">Assignment to B</span></span>

- <span data-ttu-id="c62be-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="c62be-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="c62be-119">Tesztfeladat</span><span class="sxs-lookup"><span data-stu-id="c62be-119">Test task</span></span>

        - <span data-ttu-id="c62be-120">Hozzárendelés az A-hoz</span><span class="sxs-lookup"><span data-stu-id="c62be-120">Assignment to A</span></span>
        - <span data-ttu-id="c62be-121">Hozzárendelés a B-hoz</span><span class="sxs-lookup"><span data-stu-id="c62be-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="c62be-122">Nincs hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="c62be-122">Unassigned assignment</span></span>

<span data-ttu-id="c62be-123">A PSA 3.x-ben a hozzá nem rendelt hozzárendelés egy olyan hozzárendelés, amelyet egy **NULL** csapattaghoz és **NULL** erőforráshoz rendelnek.</span><span class="sxs-lookup"><span data-stu-id="c62be-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="c62be-124">Rendeletlen hozzárendelések fordulhatnak elő néhány esetben:</span><span class="sxs-lookup"><span data-stu-id="c62be-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="c62be-125">Ha létrehoztunk egy feladatot, de még nem adták hozzá senkihez a csapat tagjaihoz, akkor mindig hozzárendelés nélküli hozzárendelést hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="c62be-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="c62be-126">Ha egy feladat összes megbízottját eltávolítják, akkor hozzárendelés nélküli hozzárendelést hoz létre a feladathoz.</span><span class="sxs-lookup"><span data-stu-id="c62be-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="c62be-127">A mezők ütemezése a Project Task entitáson</span><span class="sxs-lookup"><span data-stu-id="c62be-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="c62be-128">Az **msdyn\_projecttask** entitás mezői elavultak vagy átkerültek az **msdyn\_resourceassignment** entitásba, vagy most hivatkoznak ezekre a **msdyn\_projectteam** entitásból (**Project Team Member**).</span><span class="sxs-lookup"><span data-stu-id="c62be-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="c62be-129">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="c62be-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="c62be-130">Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés)</span><span class="sxs-lookup"><span data-stu-id="c62be-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="c62be-131">Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="c62be-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="c62be-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="c62be-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="c62be-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="c62be-133">None</span></span> | |
| <span data-ttu-id="c62be-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="c62be-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="c62be-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="c62be-135">None</span></span> | |
| <span data-ttu-id="c62be-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="c62be-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="c62be-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="c62be-137">None</span></span> | |
| <span data-ttu-id="c62be-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="c62be-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="c62be-139">Nincs</span><span class="sxs-lookup"><span data-stu-id="c62be-139">None</span></span> | |
| <span data-ttu-id="c62be-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="c62be-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="c62be-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="c62be-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="c62be-142">A mezőben tárolt JavaScript Object Notation (JSON) adatszerkezet formátuma megváltozott.</span><span class="sxs-lookup"><span data-stu-id="c62be-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="c62be-143">Ütemezéskontúr</span><span class="sxs-lookup"><span data-stu-id="c62be-143">Schedule contour</span></span>

<span data-ttu-id="c62be-144">Az ütemezéskontúr van tárolva a **Tervezett munka** mezőben (**msdyn\_plannedwork**) az egyes **Erőforrás-hozzárendelés** egységekben (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="c62be-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="c62be-145">Struktúra</span><span class="sxs-lookup"><span data-stu-id="c62be-145">Structure</span></span>

<span data-ttu-id="c62be-146">Az ütemezési kontúr új struktúrája rugalmas időszeletekből áll, amelyeket az ütemterv minden napjára meghatároznak.</span><span class="sxs-lookup"><span data-stu-id="c62be-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="c62be-147">Minden egyes szeletnek a következő tulajdonságai vannak:</span><span class="sxs-lookup"><span data-stu-id="c62be-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="c62be-148">**Kezdés** - megkezdődik a munkaidő a nap szerint a projekt naptár.</span><span class="sxs-lookup"><span data-stu-id="c62be-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="c62be-149">**Vége** - A napi munkaidő vége a projektnaptár szerint.</span><span class="sxs-lookup"><span data-stu-id="c62be-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="c62be-150">**Órák** - A napra kijelölt órák száma.</span><span class="sxs-lookup"><span data-stu-id="c62be-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="c62be-151">**Példa**</span><span class="sxs-lookup"><span data-stu-id="c62be-151">**Example**</span></span>

<span data-ttu-id="c62be-152">Ez a példa egy olyan projektnaptárt használ, ahol a munkanap 9:00 és 17:00 között van az UTC-8 időzónában.</span><span class="sxs-lookup"><span data-stu-id="c62be-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="c62be-153">Automatikus ütemezés és kézi ütemezés</span><span class="sxs-lookup"><span data-stu-id="c62be-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="c62be-154">Ha egy feladat automatikus ütemezése van, az órák előre vannak töltve, és a feladat időtartama csökkenhet.</span><span class="sxs-lookup"><span data-stu-id="c62be-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="c62be-155">**Példa**</span><span class="sxs-lookup"><span data-stu-id="c62be-155">**Example**</span></span>

<span data-ttu-id="c62be-156">A következő feladat automatikusan ütemeződik 18 órára három nap alatt (2018. december 3., 2018. december 5.).</span><span class="sxs-lookup"><span data-stu-id="c62be-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="c62be-157">Ha egy feladatot manuálisan ütemeznek, akkor az órák egyenletesen oszlanak meg az összes dátumra.</span><span class="sxs-lookup"><span data-stu-id="c62be-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="c62be-158">**Példa**</span><span class="sxs-lookup"><span data-stu-id="c62be-158">**Example**</span></span>

<span data-ttu-id="c62be-159">A következő feladatot kézzel, 18 órás időtartamra tervezzük három nap alatt (2018. december 3., 2018. december 5.).</span><span class="sxs-lookup"><span data-stu-id="c62be-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="c62be-160">Hozzárendelési egység</span><span class="sxs-lookup"><span data-stu-id="c62be-160">Assignment unit</span></span>

<span data-ttu-id="c62be-161">A hozzárendelési egység elavult a PSA 3.x-ben.</span><span class="sxs-lookup"><span data-stu-id="c62be-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="c62be-162">A feladat elvégzésének órái napi módon egyenlően oszlanak meg az összes hozzárendelt erőforrás között.</span><span class="sxs-lookup"><span data-stu-id="c62be-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="c62be-163">**Példa**</span><span class="sxs-lookup"><span data-stu-id="c62be-163">**Example**</span></span>

<span data-ttu-id="c62be-164">Ebben a példában a feladatot két erőforráshoz rendelik, és automatikusan ütemezik 36 órára három nap alatt (2018. december 3-tól 2018. december 5-ig).</span><span class="sxs-lookup"><span data-stu-id="c62be-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="c62be-165">1. feladat:</span><span class="sxs-lookup"><span data-stu-id="c62be-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="c62be-166">2. feladat:</span><span class="sxs-lookup"><span data-stu-id="c62be-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="c62be-167">Árképzési dimenziók</span><span class="sxs-lookup"><span data-stu-id="c62be-167">Pricing dimensions</span></span>

<span data-ttu-id="c62be-168">A PSA 3.x alkalmazásban az erőforrás-specifikus árazási dimenziós mezőket (például **Szerep** és **Szervezeti egység**) eltávolították a **msdyn\_projecttask** entitásból.</span><span class="sxs-lookup"><span data-stu-id="c62be-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="c62be-169">Ezek a mezők előhívhatók a megfelelő projekt csapat tagjából (**msdyn\_projectteam**) a erőforrás hozzárendelés (**msdyn\_resourceassignment**), amikor a projekt becslések keletkeznek.</span><span class="sxs-lookup"><span data-stu-id="c62be-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="c62be-170">Egy új mező, az **msdyn\_organizationalunit** került hozzáadásra az **msdyn\_projectteam** entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="c62be-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="c62be-171">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="c62be-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="c62be-172">A helyette használt msdyn\_projectteam (Project Team Member)</span><span class="sxs-lookup"><span data-stu-id="c62be-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="c62be-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="c62be-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="c62be-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="c62be-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="c62be-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="c62be-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="c62be-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="c62be-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="c62be-177">Kontúrok</span><span class="sxs-lookup"><span data-stu-id="c62be-177">Contours</span></span>

<span data-ttu-id="c62be-178">Az árazási és becslési kontúrmezők elavultak az **msdyn\_projecttask** entitáson.</span><span class="sxs-lookup"><span data-stu-id="c62be-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="c62be-179">Áthelyezték őket az **msdyn\_resourceassignment** entitásba.</span><span class="sxs-lookup"><span data-stu-id="c62be-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="c62be-180">Elavult mező az msdyn\_projecttaskban (Project Task)</span><span class="sxs-lookup"><span data-stu-id="c62be-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="c62be-181">Új mező az msdyn\_resourceassignmentben (erőforrás-hozzárendelés)</span><span class="sxs-lookup"><span data-stu-id="c62be-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="c62be-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="c62be-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="c62be-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="c62be-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="c62be-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="c62be-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="c62be-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="c62be-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="c62be-186">A következő mezők kerültek hozzáadásra az **msdyn\_resourceassignment** entitáshoz:</span><span class="sxs-lookup"><span data-stu-id="c62be-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="c62be-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c62be-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="c62be-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c62be-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="c62be-189">A tervezett, a tényleges és a fennmaradó költségek és az értékesítés alábbi mezői nem változnak az **msdyn\_projecttask** entitáson:</span><span class="sxs-lookup"><span data-stu-id="c62be-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="c62be-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="c62be-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="c62be-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="c62be-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="c62be-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="c62be-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="c62be-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="c62be-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="c62be-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="c62be-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="c62be-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="c62be-195">msdyn\_remainingsales</span></span>
