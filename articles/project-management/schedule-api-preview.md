---
title: Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez
description: Ez témakör az ütemezési API-k használatával kapcsolatos információkat és mintákat tartalmaz.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868132"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="c81f7-103">Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez</span><span class="sxs-lookup"><span data-stu-id="c81f7-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="c81f7-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="c81f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c81f7-105">A témakörben ismertetett egyes funkciók vagy az összes funkció az előzetes verzió részeként áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="c81f7-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="c81f7-106">A tartalom és a funkciók tekintetében a változtatás jogát fenntartjuk.</span><span class="sxs-lookup"><span data-stu-id="c81f7-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="c81f7-107">Ütemezési entitások</span><span class="sxs-lookup"><span data-stu-id="c81f7-107">Scheduling entities</span></span>

<span data-ttu-id="c81f7-108">Az ütemezési API-k lehetővé teszik a létrehozási, frissítési és törlési műveletek elvégzését az **Ütemezési entitásokkal**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="c81f7-109">Ezeket az entitásokat a Project for the web ütemezési motorja kezeli.</span><span class="sxs-lookup"><span data-stu-id="c81f7-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="c81f7-110">Az **Ütemezési entitásokkal** végzett műveletek létrehozása, frissítése és törlése korlátozott volt a korábbi Dynamics 365 Project Operations kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="c81f7-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="c81f7-111">Az alábbi tábla az **Ütemezési entitások** teljes listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c81f7-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="c81f7-112">Entitás neve</span><span class="sxs-lookup"><span data-stu-id="c81f7-112">Entity name</span></span>  | <span data-ttu-id="c81f7-113">Entitás logikai neve</span><span class="sxs-lookup"><span data-stu-id="c81f7-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="c81f7-114">Project</span><span class="sxs-lookup"><span data-stu-id="c81f7-114">Project</span></span> | <span data-ttu-id="c81f7-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="c81f7-115">msdyn_project</span></span> |
| <span data-ttu-id="c81f7-116">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="c81f7-116">Project Task</span></span>  | <span data-ttu-id="c81f7-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="c81f7-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="c81f7-118">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="c81f7-118">Project Task Dependency</span></span>  | <span data-ttu-id="c81f7-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="c81f7-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="c81f7-120">Erőforrás-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="c81f7-120">Resource Assignment</span></span> | <span data-ttu-id="c81f7-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="c81f7-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="c81f7-122">Projektgyűjtő</span><span class="sxs-lookup"><span data-stu-id="c81f7-122">Project Bucket</span></span>  | <span data-ttu-id="c81f7-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="c81f7-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="c81f7-124">Projektcsoporttag</span><span class="sxs-lookup"><span data-stu-id="c81f7-124">Project Team Member</span></span> | <span data-ttu-id="c81f7-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="c81f7-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="c81f7-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="c81f7-126">OperationSet</span></span>

<span data-ttu-id="c81f7-127">Az OperationSet egy munkaegység-minta, amely akkor használható, ha egy tranzakción belül több ütemezést is fel kell dolgozni, amely a kérelmeket érinti.</span><span class="sxs-lookup"><span data-stu-id="c81f7-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="c81f7-128">API-k ütemezése</span><span class="sxs-lookup"><span data-stu-id="c81f7-128">Schedule APIs</span></span>

<span data-ttu-id="c81f7-129">Az alábbiakban az aktuális ütemezési API-k listája szerepel.</span><span class="sxs-lookup"><span data-stu-id="c81f7-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="c81f7-130">**msdyn_CreateProjectV1**: Ez az API projekt létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="c81f7-131">A projekt és az alapértelmezett projektgyűjtő azonnal létrejön.</span><span class="sxs-lookup"><span data-stu-id="c81f7-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="c81f7-132">**msdyn_CreateTeamMemberV1**: Ez az API projekt csoporttag létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="c81f7-133">A csoporttag-rekord azonnal létrejön.</span><span class="sxs-lookup"><span data-stu-id="c81f7-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="c81f7-134">**msdyn_CreateOperationSetV1**: Ez az API több olyan kérés ütemezésére használható, amelyet egy tranzakción belül kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="c81f7-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="c81f7-135">**msdyn_PSSCreateV1**: Ez az API entitás létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="c81f7-136">Az entitás lehet a létrehozási műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="c81f7-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="c81f7-137">**msdyn_PSSUpdateV1**: Ez az API entitás frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="c81f7-138">Az entitás lehet a frissítési műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="c81f7-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="c81f7-139">**msdyn_PSSDeleteV1**: Ez az API entitás törlésére használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="c81f7-140">Az entitás lehet a törlési műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="c81f7-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="c81f7-141">**msdyn_ExecuteOperationSetV1**: Ez az API az adott műveletkészleten belüli összes művelet végrehajtására használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="c81f7-142">Ütemezési API-k használata az OperationSettel</span><span class="sxs-lookup"><span data-stu-id="c81f7-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="c81f7-143">Mivel a **CreateProjectV1** és a **CreateTeamMemberV1** rekordok azonnal létrejönnek, ezek az API-k nem használhatók közvetlenül az **OperationSetben**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="c81f7-144">Az API-val azonban létrehozhatja a szükséges rekordokat, létrehozhat egy **OperationSetet**, majd használhatja ezeket az előre létrehozott rekordokat az **OperationSetben**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="c81f7-145">Támogatott műveletek</span><span class="sxs-lookup"><span data-stu-id="c81f7-145">Supported operations</span></span>

| <span data-ttu-id="c81f7-146">Ütemezési entitás</span><span class="sxs-lookup"><span data-stu-id="c81f7-146">Scheduling entity</span></span> | <span data-ttu-id="c81f7-147">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="c81f7-147">Create</span></span> | <span data-ttu-id="c81f7-148">Frissítés</span><span class="sxs-lookup"><span data-stu-id="c81f7-148">Update</span></span> | <span data-ttu-id="c81f7-149">Delete</span><span class="sxs-lookup"><span data-stu-id="c81f7-149">Delete</span></span> | <span data-ttu-id="c81f7-150">Fontos tényezők</span><span class="sxs-lookup"><span data-stu-id="c81f7-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="c81f7-151">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="c81f7-151">Project task</span></span> | <span data-ttu-id="c81f7-152">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-152">Yes</span></span> | <span data-ttu-id="c81f7-153">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-153">Yes</span></span> | <span data-ttu-id="c81f7-154">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-154">Yes</span></span> | <span data-ttu-id="c81f7-155">Egyik sem</span><span class="sxs-lookup"><span data-stu-id="c81f7-155">None</span></span> |
| <span data-ttu-id="c81f7-156">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="c81f7-156">Project task dependency</span></span> | <span data-ttu-id="c81f7-157">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-157">Yes</span></span> | <span data-ttu-id="c81f7-158">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-158">Yes</span></span> | | <span data-ttu-id="c81f7-159">A projektfeladat függőségi rekordok nem frissülnek.</span><span class="sxs-lookup"><span data-stu-id="c81f7-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="c81f7-160">Ehelyett egy régi rekord törölhető, és új rekord is létrehozható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c81f7-161">Erőforrás-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="c81f7-161">Resource assignment</span></span> | <span data-ttu-id="c81f7-162">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-162">Yes</span></span> | <span data-ttu-id="c81f7-163">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-163">Yes</span></span> | | <span data-ttu-id="c81f7-164">A következő mezőkkel végzett műveletek nem támogatottak: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** és **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="c81f7-165">Az erőforrás-hozzárendelési rekordok nem frissülnek.</span><span class="sxs-lookup"><span data-stu-id="c81f7-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="c81f7-166">Ehelyett a régi rekord törölhető, és új rekord is létrehozható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="c81f7-167">Projektgyűjtő</span><span class="sxs-lookup"><span data-stu-id="c81f7-167">Project bucket</span></span> | <span data-ttu-id="c81f7-168">N. a.</span><span class="sxs-lookup"><span data-stu-id="c81f7-168">N/A</span></span> | <span data-ttu-id="c81f7-169">N. a.</span><span class="sxs-lookup"><span data-stu-id="c81f7-169">N/A</span></span> | <span data-ttu-id="c81f7-170">N. a.</span><span class="sxs-lookup"><span data-stu-id="c81f7-170">N/A</span></span> | <span data-ttu-id="c81f7-171">Az alapértelmezett gyűjtő létrehozása a **CreateProjectV1** API használatával jön létre.</span><span class="sxs-lookup"><span data-stu-id="c81f7-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="c81f7-172">A projekt csapattagja</span><span class="sxs-lookup"><span data-stu-id="c81f7-172">Project team member</span></span> | <span data-ttu-id="c81f7-173">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-173">Yes</span></span> | <span data-ttu-id="c81f7-174">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-174">Yes</span></span> | <span data-ttu-id="c81f7-175">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-175">Yes</span></span> | <span data-ttu-id="c81f7-176">A létrehozáshoz használja a **CreateTeamMemberV1** API-t.</span><span class="sxs-lookup"><span data-stu-id="c81f7-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="c81f7-177">Project</span><span class="sxs-lookup"><span data-stu-id="c81f7-177">Project</span></span> | <span data-ttu-id="c81f7-178">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-178">Yes</span></span> | <span data-ttu-id="c81f7-179">Igen</span><span class="sxs-lookup"><span data-stu-id="c81f7-179">Yes</span></span> | <span data-ttu-id="c81f7-180">N. a.</span><span class="sxs-lookup"><span data-stu-id="c81f7-180">N/A</span></span> | <span data-ttu-id="c81f7-181">A következő mezőkkel végzett műveletek nem támogatottak: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, és **Duration**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="c81f7-182">Ezek az API-k egyéni mezőket tartalmazó entitásobjektumokkal hívhatóak meg.</span><span class="sxs-lookup"><span data-stu-id="c81f7-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="c81f7-183">Ez az azonosító-tulajdonság nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c81f7-183">The ID property is optional.</span></span> <span data-ttu-id="c81f7-184">Ha rendelkezésre áll, a rendszer megpróbálja használni, illetve kivételt okoz, ha nem használható.</span><span class="sxs-lookup"><span data-stu-id="c81f7-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="c81f7-185">Ha nincs biztosítva, a rendszer fogja létrehozni.</span><span class="sxs-lookup"><span data-stu-id="c81f7-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="c81f7-186">Korlátozások és ismert problémák</span><span class="sxs-lookup"><span data-stu-id="c81f7-186">Limitations and known issues</span></span>
<span data-ttu-id="c81f7-187">Az alábbiakban felsoroljuk a korlátozásokat és az ismert problémákat:</span><span class="sxs-lookup"><span data-stu-id="c81f7-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="c81f7-188">Az ütemezési API-kat csak **Microsoft Project licenccel rendelkező felhasználók használhatják**.</span><span class="sxs-lookup"><span data-stu-id="c81f7-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="c81f7-189">Nem használhatják:</span><span class="sxs-lookup"><span data-stu-id="c81f7-189">They can't be used by:</span></span>
    - <span data-ttu-id="c81f7-190">Alkalmazásfelhasználók</span><span class="sxs-lookup"><span data-stu-id="c81f7-190">Application users</span></span>
    - <span data-ttu-id="c81f7-191">Rendszerfelhasználók</span><span class="sxs-lookup"><span data-stu-id="c81f7-191">System users</span></span>
    - <span data-ttu-id="c81f7-192">Integrációs felhasználók</span><span class="sxs-lookup"><span data-stu-id="c81f7-192">Integration users</span></span>
    - <span data-ttu-id="c81f7-193">Más felhasználók, akik nem rendelkeznek a szükséges licenccel</span><span class="sxs-lookup"><span data-stu-id="c81f7-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="c81f7-194">Minden **OperationSet** legfeljebb 100 művelettel rendelkezhet.</span><span class="sxs-lookup"><span data-stu-id="c81f7-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="c81f7-195">Minden felhasználó legfeljebb 10 nyitott **OperationSet** művelettel rendelkezhet.</span><span class="sxs-lookup"><span data-stu-id="c81f7-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="c81f7-196">A Project Operations jelenleg legfeljebb 500 projektfeladatot támogat.</span><span class="sxs-lookup"><span data-stu-id="c81f7-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="c81f7-197">Az **OperationSet** hibaállapotok és hibanaplók jelenleg nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="c81f7-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="c81f7-198">Az ütemezési API-k nyilvános előzetes verzióban vannak.</span><span class="sxs-lookup"><span data-stu-id="c81f7-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="c81f7-199">Ezeket az API-kat Működési környezetben nem támogatja a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c81f7-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="c81f7-200">Példaforgatókönyv</span><span class="sxs-lookup"><span data-stu-id="c81f7-200">Sample scenario</span></span>

<span data-ttu-id="c81f7-201">Ebben a forgatókönyvben létre fog hozni egy projektet, egy csoporttagot, négy feladatot és két erőforrás-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="c81f7-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="c81f7-202">Ezután frissít egy feladatot, frissíti a projektet, töröl egy feladatot, töröl egy erőforrás-hozzárendelést, és létrehoz egy feladatfüggőséget.</span><span class="sxs-lookup"><span data-stu-id="c81f7-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="c81f7-203">További minták</span><span class="sxs-lookup"><span data-stu-id="c81f7-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
