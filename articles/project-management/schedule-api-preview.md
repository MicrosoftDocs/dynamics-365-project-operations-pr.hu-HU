---
title: Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez
description: Ez témakör az ütemezési API-k használatával kapcsolatos információkat és mintákat tartalmaz.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950807"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="b14ef-103">Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez</span><span class="sxs-lookup"><span data-stu-id="b14ef-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="b14ef-104">_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_</span><span class="sxs-lookup"><span data-stu-id="b14ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b14ef-105">A témakörben ismertetett egyes funkciók vagy az összes funkció az előzetes verzió részeként áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="b14ef-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="b14ef-106">A tartalom és a funkciók tekintetében a változtatás jogát fenntartjuk.</span><span class="sxs-lookup"><span data-stu-id="b14ef-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="b14ef-107">Ütemezési entitások</span><span class="sxs-lookup"><span data-stu-id="b14ef-107">Scheduling entities</span></span>

<span data-ttu-id="b14ef-108">Az ütemezési API-k lehetővé teszik a létrehozási, frissítési és törlési műveletek elvégzését az **Ütemezési entitásokkal**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="b14ef-109">Ezeket az entitásokat a Project for the web ütemezési motorja kezeli.</span><span class="sxs-lookup"><span data-stu-id="b14ef-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="b14ef-110">Az **Ütemezési entitásokkal** végzett műveletek létrehozása, frissítése és törlése korlátozott volt a korábbi Dynamics 365 Project Operations kiadásokban.</span><span class="sxs-lookup"><span data-stu-id="b14ef-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="b14ef-111">Az alábbi tábla az **Ütemezési entitások** teljes listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b14ef-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="b14ef-112">Entitás neve</span><span class="sxs-lookup"><span data-stu-id="b14ef-112">Entity name</span></span>  | <span data-ttu-id="b14ef-113">Entitás logikai neve</span><span class="sxs-lookup"><span data-stu-id="b14ef-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="b14ef-114">Project</span><span class="sxs-lookup"><span data-stu-id="b14ef-114">Project</span></span> | <span data-ttu-id="b14ef-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b14ef-115">msdyn_project</span></span> |
| <span data-ttu-id="b14ef-116">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="b14ef-116">Project Task</span></span>  | <span data-ttu-id="b14ef-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="b14ef-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="b14ef-118">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="b14ef-118">Project Task Dependency</span></span>  | <span data-ttu-id="b14ef-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="b14ef-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="b14ef-120">Erőforrás-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="b14ef-120">Resource Assignment</span></span> | <span data-ttu-id="b14ef-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="b14ef-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="b14ef-122">Projektgyűjtő</span><span class="sxs-lookup"><span data-stu-id="b14ef-122">Project Bucket</span></span>  | <span data-ttu-id="b14ef-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="b14ef-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="b14ef-124">Projektcsoporttag</span><span class="sxs-lookup"><span data-stu-id="b14ef-124">Project Team Member</span></span> | <span data-ttu-id="b14ef-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="b14ef-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="b14ef-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="b14ef-126">OperationSet</span></span>

<span data-ttu-id="b14ef-127">Az OperationSet egy munkaegység-minta, amely akkor használható, ha egy tranzakción belül több ütemezést is fel kell dolgozni, amely a kérelmeket érinti.</span><span class="sxs-lookup"><span data-stu-id="b14ef-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="b14ef-128">API-k ütemezése</span><span class="sxs-lookup"><span data-stu-id="b14ef-128">Schedule APIs</span></span>

<span data-ttu-id="b14ef-129">Az alábbiakban az aktuális ütemezési API-k listája szerepel.</span><span class="sxs-lookup"><span data-stu-id="b14ef-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="b14ef-130">**msdyn_CreateProjectV1**: Ez az API projekt létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="b14ef-131">A projekt és az alapértelmezett projektgyűjtő azonnal létrejön.</span><span class="sxs-lookup"><span data-stu-id="b14ef-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="b14ef-132">**msdyn_CreateTeamMemberV1**: Ez az API projekt csoporttag létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="b14ef-133">A csoporttag-rekord azonnal létrejön.</span><span class="sxs-lookup"><span data-stu-id="b14ef-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="b14ef-134">**msdyn_CreateOperationSetV1**: Ez az API több olyan kérés ütemezésére használható, amelyet egy tranzakción belül kell végrehajtani.</span><span class="sxs-lookup"><span data-stu-id="b14ef-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="b14ef-135">**msdyn_PSSCreateV1**: Ez az API entitás létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="b14ef-136">Az entitás lehet a létrehozási műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="b14ef-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="b14ef-137">**msdyn_PSSUpdateV1**: Ez az API entitás frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="b14ef-138">Az entitás lehet a frissítési műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="b14ef-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="b14ef-139">**msdyn_PSSDeleteV1**: Ez az API entitás törlésére használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="b14ef-140">Az entitás lehet a törlési műveletet támogató Ütemezési entitások bármelyike.</span><span class="sxs-lookup"><span data-stu-id="b14ef-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="b14ef-141">**msdyn_ExecuteOperationSetV1**: Ez az API az adott műveletkészleten belüli összes művelet végrehajtására használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="b14ef-142">Ütemezési API-k használata az OperationSettel</span><span class="sxs-lookup"><span data-stu-id="b14ef-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="b14ef-143">Mivel a **CreateProjectV1** és a **CreateTeamMemberV1** rekordok azonnal létrejönnek, ezek az API-k nem használhatók közvetlenül az **OperationSetben**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="b14ef-144">Az API-val azonban létrehozhatja a szükséges rekordokat, létrehozhat egy **OperationSetet**, majd használhatja ezeket az előre létrehozott rekordokat az **OperationSetben**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="b14ef-145">Támogatott műveletek</span><span class="sxs-lookup"><span data-stu-id="b14ef-145">Supported operations</span></span>

| <span data-ttu-id="b14ef-146">Ütemezési entitás</span><span class="sxs-lookup"><span data-stu-id="b14ef-146">Scheduling entity</span></span> | <span data-ttu-id="b14ef-147">Létrehozás</span><span class="sxs-lookup"><span data-stu-id="b14ef-147">Create</span></span> | <span data-ttu-id="b14ef-148">Frissítés</span><span class="sxs-lookup"><span data-stu-id="b14ef-148">Update</span></span> | <span data-ttu-id="b14ef-149">Delete</span><span class="sxs-lookup"><span data-stu-id="b14ef-149">Delete</span></span> | <span data-ttu-id="b14ef-150">Fontos tényezők</span><span class="sxs-lookup"><span data-stu-id="b14ef-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="b14ef-151">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="b14ef-151">Project task</span></span> | <span data-ttu-id="b14ef-152">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-152">Yes</span></span> | <span data-ttu-id="b14ef-153">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-153">Yes</span></span> | <span data-ttu-id="b14ef-154">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-154">Yes</span></span> | <span data-ttu-id="b14ef-155">Egyik sem</span><span class="sxs-lookup"><span data-stu-id="b14ef-155">None</span></span> |
| <span data-ttu-id="b14ef-156">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="b14ef-156">Project task dependency</span></span> | <span data-ttu-id="b14ef-157">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-157">Yes</span></span> | <span data-ttu-id="b14ef-158">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-158">Yes</span></span> | | <span data-ttu-id="b14ef-159">A projektfeladat függőségi rekordok nem frissülnek.</span><span class="sxs-lookup"><span data-stu-id="b14ef-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="b14ef-160">Ehelyett egy régi rekord törölhető, és új rekord is létrehozható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b14ef-161">Erőforrás-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="b14ef-161">Resource assignment</span></span> | <span data-ttu-id="b14ef-162">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-162">Yes</span></span> | <span data-ttu-id="b14ef-163">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-163">Yes</span></span> | | <span data-ttu-id="b14ef-164">A következő mezőkkel végzett műveletek nem támogatottak: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** és **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="b14ef-165">Az erőforrás-hozzárendelési rekordok nem frissülnek.</span><span class="sxs-lookup"><span data-stu-id="b14ef-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="b14ef-166">Ehelyett a régi rekord törölhető, és új rekord is létrehozható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b14ef-167">Projektgyűjtő</span><span class="sxs-lookup"><span data-stu-id="b14ef-167">Project bucket</span></span> | <span data-ttu-id="b14ef-168">N. a.</span><span class="sxs-lookup"><span data-stu-id="b14ef-168">N/A</span></span> | <span data-ttu-id="b14ef-169">N. a.</span><span class="sxs-lookup"><span data-stu-id="b14ef-169">N/A</span></span> | <span data-ttu-id="b14ef-170">N. a.</span><span class="sxs-lookup"><span data-stu-id="b14ef-170">N/A</span></span> | <span data-ttu-id="b14ef-171">Az alapértelmezett gyűjtő létrehozása a **CreateProjectV1** API használatával jön létre.</span><span class="sxs-lookup"><span data-stu-id="b14ef-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="b14ef-172">A projekt csapattagja</span><span class="sxs-lookup"><span data-stu-id="b14ef-172">Project team member</span></span> | <span data-ttu-id="b14ef-173">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-173">Yes</span></span> | <span data-ttu-id="b14ef-174">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-174">Yes</span></span> | <span data-ttu-id="b14ef-175">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-175">Yes</span></span> | <span data-ttu-id="b14ef-176">A létrehozáshoz használja a **CreateTeamMemberV1** API-t.</span><span class="sxs-lookup"><span data-stu-id="b14ef-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="b14ef-177">Project</span><span class="sxs-lookup"><span data-stu-id="b14ef-177">Project</span></span> | <span data-ttu-id="b14ef-178">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-178">Yes</span></span> | <span data-ttu-id="b14ef-179">Igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-179">Yes</span></span> | <span data-ttu-id="b14ef-180">N. a.</span><span class="sxs-lookup"><span data-stu-id="b14ef-180">N/A</span></span> | <span data-ttu-id="b14ef-181">A következő mezőkkel végzett műveletek nem támogatottak: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, és **Duration**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="b14ef-182">Ezek az API-k egyéni mezőket tartalmazó entitásobjektumokkal hívhatóak meg.</span><span class="sxs-lookup"><span data-stu-id="b14ef-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="b14ef-183">Ez az azonosító-tulajdonság nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b14ef-183">The ID property is optional.</span></span> <span data-ttu-id="b14ef-184">Ha rendelkezésre áll, a rendszer megpróbálja használni, illetve kivételt okoz, ha nem használható.</span><span class="sxs-lookup"><span data-stu-id="b14ef-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="b14ef-185">Ha nincs biztosítva, a rendszer fogja létrehozni.</span><span class="sxs-lookup"><span data-stu-id="b14ef-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="b14ef-186">Korlátozott mezők</span><span class="sxs-lookup"><span data-stu-id="b14ef-186">Restricted fields</span></span>

<span data-ttu-id="b14ef-187">A következő táblázatok határozzák meg a **Létrehozás** és **Szerkesztés** mezőkre vonatkozó korlátozásokat.</span><span class="sxs-lookup"><span data-stu-id="b14ef-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="b14ef-188">Projektfeladat</span><span class="sxs-lookup"><span data-stu-id="b14ef-188">Project task</span></span>

| <span data-ttu-id="b14ef-189">**Logikai név**</span><span class="sxs-lookup"><span data-stu-id="b14ef-189">**Logical name**</span></span>                       | <span data-ttu-id="b14ef-190">**Létrehozhat**</span><span class="sxs-lookup"><span data-stu-id="b14ef-190">**Can create**</span></span> | <span data-ttu-id="b14ef-191">**Szerkeszthet**</span><span class="sxs-lookup"><span data-stu-id="b14ef-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="b14ef-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="b14ef-193">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-193">no</span></span>             | <span data-ttu-id="b14ef-194">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-194">no</span></span>               |
| <span data-ttu-id="b14ef-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="b14ef-196">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-196">no</span></span>             | <span data-ttu-id="b14ef-197">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-197">no</span></span>               |
| <span data-ttu-id="b14ef-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="b14ef-198">msdyn_actualend</span></span>                        | <span data-ttu-id="b14ef-199">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-199">no</span></span>             | <span data-ttu-id="b14ef-200">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-200">no</span></span>               |
| <span data-ttu-id="b14ef-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="b14ef-202">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-202">no</span></span>             | <span data-ttu-id="b14ef-203">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-203">no</span></span>               |
| <span data-ttu-id="b14ef-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b14ef-205">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-205">no</span></span>             | <span data-ttu-id="b14ef-206">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-206">no</span></span>               |
| <span data-ttu-id="b14ef-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="b14ef-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="b14ef-208">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-208">no</span></span>             | <span data-ttu-id="b14ef-209">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-209">no</span></span>               |
| <span data-ttu-id="b14ef-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="b14ef-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="b14ef-211">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-211">no</span></span>             | <span data-ttu-id="b14ef-212">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-212">no</span></span>               |
| <span data-ttu-id="b14ef-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="b14ef-214">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-214">no</span></span>             | <span data-ttu-id="b14ef-215">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-215">no</span></span>               |
| <span data-ttu-id="b14ef-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b14ef-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="b14ef-217">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-217">no</span></span>             | <span data-ttu-id="b14ef-218">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-218">no</span></span>               |
| <span data-ttu-id="b14ef-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b14ef-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b14ef-220">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-220">no</span></span>             | <span data-ttu-id="b14ef-221">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-221">no</span></span>               |
| <span data-ttu-id="b14ef-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b14ef-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="b14ef-223">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-223">no</span></span>             | <span data-ttu-id="b14ef-224">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-224">no</span></span>               |
| <span data-ttu-id="b14ef-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="b14ef-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="b14ef-226">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-226">no</span></span>             | <span data-ttu-id="b14ef-227">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-227">no</span></span>               |
| <span data-ttu-id="b14ef-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="b14ef-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="b14ef-229">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-229">no</span></span>             | <span data-ttu-id="b14ef-230">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-230">no</span></span>               |
| <span data-ttu-id="b14ef-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="b14ef-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="b14ef-232">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-232">no</span></span>             | <span data-ttu-id="b14ef-233">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-233">no</span></span>               |
| <span data-ttu-id="b14ef-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="b14ef-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="b14ef-235">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-235">no</span></span>             | <span data-ttu-id="b14ef-236">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-236">no</span></span>               |
| <span data-ttu-id="b14ef-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="b14ef-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="b14ef-238">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-238">no</span></span>             | <span data-ttu-id="b14ef-239">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-239">no</span></span>               |
| <span data-ttu-id="b14ef-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="b14ef-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="b14ef-241">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-241">no</span></span>             | <span data-ttu-id="b14ef-242">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-242">no</span></span>               |
| <span data-ttu-id="b14ef-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="b14ef-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="b14ef-244">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-244">no</span></span>             | <span data-ttu-id="b14ef-245">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-245">no</span></span>               |
| <span data-ttu-id="b14ef-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="b14ef-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="b14ef-247">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-247">no</span></span>             | <span data-ttu-id="b14ef-248">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-248">no</span></span>               |
| <span data-ttu-id="b14ef-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b14ef-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="b14ef-250">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-250">no</span></span>             | <span data-ttu-id="b14ef-251">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-251">no</span></span>               |
| <span data-ttu-id="b14ef-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="b14ef-253">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-253">no</span></span>             | <span data-ttu-id="b14ef-254">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-254">no</span></span>               |
| <span data-ttu-id="b14ef-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="b14ef-256">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-256">no</span></span>             | <span data-ttu-id="b14ef-257">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-257">no</span></span>               |
| <span data-ttu-id="b14ef-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b14ef-259">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-259">no</span></span>             | <span data-ttu-id="b14ef-260">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-260">no</span></span>               |
| <span data-ttu-id="b14ef-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b14ef-262">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-262">no</span></span>             | <span data-ttu-id="b14ef-263">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-263">no</span></span>               |
| <span data-ttu-id="b14ef-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="b14ef-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="b14ef-265">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-265">no</span></span>             | <span data-ttu-id="b14ef-266">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-266">no</span></span>               |
| <span data-ttu-id="b14ef-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b14ef-267">msdyn_progress</span></span>                         | <span data-ttu-id="b14ef-268">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-268">no</span></span>             | <span data-ttu-id="b14ef-269">nem (igen a P4W- hez)</span><span class="sxs-lookup"><span data-stu-id="b14ef-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="b14ef-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b14ef-271">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-271">no</span></span>             | <span data-ttu-id="b14ef-272">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-272">no</span></span>               |
| <span data-ttu-id="b14ef-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b14ef-274">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-274">no</span></span>             | <span data-ttu-id="b14ef-275">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-275">no</span></span>               |
| <span data-ttu-id="b14ef-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b14ef-277">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-277">no</span></span>             | <span data-ttu-id="b14ef-278">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-278">no</span></span>               |
| <span data-ttu-id="b14ef-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b14ef-280">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-280">no</span></span>             | <span data-ttu-id="b14ef-281">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-281">no</span></span>               |
| <span data-ttu-id="b14ef-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="b14ef-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="b14ef-283">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-283">no</span></span>             | <span data-ttu-id="b14ef-284">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-284">no</span></span>               |
| <span data-ttu-id="b14ef-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b14ef-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="b14ef-286">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-286">no</span></span>             | <span data-ttu-id="b14ef-287">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-287">no</span></span>               |
| <span data-ttu-id="b14ef-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="b14ef-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="b14ef-289">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-289">no</span></span>             | <span data-ttu-id="b14ef-290">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-290">no</span></span>               |
| <span data-ttu-id="b14ef-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b14ef-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="b14ef-292">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-292">no</span></span>             | <span data-ttu-id="b14ef-293">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-293">no</span></span>               |
| <span data-ttu-id="b14ef-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="b14ef-295">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-295">no</span></span>             | <span data-ttu-id="b14ef-296">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-296">no</span></span>               |
| <span data-ttu-id="b14ef-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b14ef-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="b14ef-298">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-298">no</span></span>             | <span data-ttu-id="b14ef-299">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-299">no</span></span>               |
| <span data-ttu-id="b14ef-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b14ef-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="b14ef-301">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-301">no</span></span>             | <span data-ttu-id="b14ef-302">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-302">no</span></span>               |
| <span data-ttu-id="b14ef-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="b14ef-304">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-304">no</span></span>             | <span data-ttu-id="b14ef-305">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-305">no</span></span>               |
| <span data-ttu-id="b14ef-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b14ef-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b14ef-307">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-307">no</span></span>             | <span data-ttu-id="b14ef-308">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-308">no</span></span>               |
| <span data-ttu-id="b14ef-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b14ef-310">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-310">no</span></span>             | <span data-ttu-id="b14ef-311">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-311">no</span></span>               |
| <span data-ttu-id="b14ef-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="b14ef-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="b14ef-313">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-313">no</span></span>             | <span data-ttu-id="b14ef-314">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-314">no</span></span>               |
| <span data-ttu-id="b14ef-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="b14ef-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="b14ef-316">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-316">no</span></span>             | <span data-ttu-id="b14ef-317">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-317">no</span></span>               |
| <span data-ttu-id="b14ef-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="b14ef-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="b14ef-319">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-319">no</span></span>             | <span data-ttu-id="b14ef-320">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-320">no</span></span>               |
| <span data-ttu-id="b14ef-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b14ef-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b14ef-322">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-322">no</span></span>             | <span data-ttu-id="b14ef-323">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-323">no</span></span>               |
| <span data-ttu-id="b14ef-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="b14ef-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="b14ef-325">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-325">no</span></span>             | <span data-ttu-id="b14ef-326">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-326">no</span></span>               |
| <span data-ttu-id="b14ef-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="b14ef-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="b14ef-328">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-328">no</span></span>             | <span data-ttu-id="b14ef-329">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-329">no</span></span>               |
| <span data-ttu-id="b14ef-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="b14ef-330">msdyn_summary</span></span>                          | <span data-ttu-id="b14ef-331">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-331">no</span></span>             | <span data-ttu-id="b14ef-332">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-332">no</span></span>               |
| <span data-ttu-id="b14ef-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="b14ef-334">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-334">no</span></span>             | <span data-ttu-id="b14ef-335">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-335">no</span></span>               |
| <span data-ttu-id="b14ef-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="b14ef-337">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-337">no</span></span>             | <span data-ttu-id="b14ef-338">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="b14ef-339">Projektfeladat függősége</span><span class="sxs-lookup"><span data-stu-id="b14ef-339">Project task dependency</span></span>

| <span data-ttu-id="b14ef-340">**Logikai név**</span><span class="sxs-lookup"><span data-stu-id="b14ef-340">**Logical name**</span></span>              | <span data-ttu-id="b14ef-341">**Létrehozhat**</span><span class="sxs-lookup"><span data-stu-id="b14ef-341">**Can create**</span></span> | <span data-ttu-id="b14ef-342">**Szerkeszthet**</span><span class="sxs-lookup"><span data-stu-id="b14ef-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="b14ef-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="b14ef-343">msdyn_linktype</span></span>                | <span data-ttu-id="b14ef-344">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-344">no</span></span>             | <span data-ttu-id="b14ef-345">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-345">no</span></span>           |
| <span data-ttu-id="b14ef-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="b14ef-346">msdyn_linktypename</span></span>            | <span data-ttu-id="b14ef-347">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-347">no</span></span>             | <span data-ttu-id="b14ef-348">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-348">no</span></span>           |
| <span data-ttu-id="b14ef-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="b14ef-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="b14ef-350">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-350">yes</span></span>            | <span data-ttu-id="b14ef-351">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-351">no</span></span>           |
| <span data-ttu-id="b14ef-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="b14ef-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="b14ef-353">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-353">yes</span></span>            | <span data-ttu-id="b14ef-354">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-354">no</span></span>           |
| <span data-ttu-id="b14ef-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b14ef-355">msdyn_project</span></span>                 | <span data-ttu-id="b14ef-356">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-356">yes</span></span>            | <span data-ttu-id="b14ef-357">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-357">no</span></span>           |
| <span data-ttu-id="b14ef-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="b14ef-358">msdyn_projectname</span></span>             | <span data-ttu-id="b14ef-359">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-359">yes</span></span>            | <span data-ttu-id="b14ef-360">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-360">no</span></span>           |
| <span data-ttu-id="b14ef-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="b14ef-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="b14ef-362">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-362">yes</span></span>            | <span data-ttu-id="b14ef-363">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-363">no</span></span>           |
| <span data-ttu-id="b14ef-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="b14ef-364">msdyn_successortask</span></span>           | <span data-ttu-id="b14ef-365">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-365">yes</span></span>            | <span data-ttu-id="b14ef-366">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-366">no</span></span>           |
| <span data-ttu-id="b14ef-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="b14ef-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="b14ef-368">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-368">yes</span></span>            | <span data-ttu-id="b14ef-369">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="b14ef-370">Erőforrás-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="b14ef-370">Resource assignment</span></span>

| <span data-ttu-id="b14ef-371">**Logikai név**</span><span class="sxs-lookup"><span data-stu-id="b14ef-371">**Logical name**</span></span>             | <span data-ttu-id="b14ef-372">**Létrehozhat**</span><span class="sxs-lookup"><span data-stu-id="b14ef-372">**Can create**</span></span> | <span data-ttu-id="b14ef-373">**Szerkeszthet**</span><span class="sxs-lookup"><span data-stu-id="b14ef-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="b14ef-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="b14ef-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="b14ef-375">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-375">yes</span></span>            | <span data-ttu-id="b14ef-376">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-376">no</span></span>           |
| <span data-ttu-id="b14ef-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="b14ef-378">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-378">yes</span></span>            | <span data-ttu-id="b14ef-379">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-379">no</span></span>           |
| <span data-ttu-id="b14ef-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="b14ef-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="b14ef-381">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-381">no</span></span>             | <span data-ttu-id="b14ef-382">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-382">no</span></span>           |
| <span data-ttu-id="b14ef-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="b14ef-384">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-384">no</span></span>             | <span data-ttu-id="b14ef-385">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-385">no</span></span>           |
| <span data-ttu-id="b14ef-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="b14ef-386">msdyn_committype</span></span>             | <span data-ttu-id="b14ef-387">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-387">no</span></span>             | <span data-ttu-id="b14ef-388">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-388">no</span></span>           |
| <span data-ttu-id="b14ef-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="b14ef-389">msdyn_committypename</span></span>         | <span data-ttu-id="b14ef-390">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-390">no</span></span>             | <span data-ttu-id="b14ef-391">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-391">no</span></span>           |
| <span data-ttu-id="b14ef-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b14ef-392">msdyn_effort</span></span>                 | <span data-ttu-id="b14ef-393">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-393">no</span></span>             | <span data-ttu-id="b14ef-394">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-394">no</span></span>           |
| <span data-ttu-id="b14ef-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b14ef-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="b14ef-396">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-396">no</span></span>             | <span data-ttu-id="b14ef-397">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-397">no</span></span>           |
| <span data-ttu-id="b14ef-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b14ef-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="b14ef-399">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-399">no</span></span>             | <span data-ttu-id="b14ef-400">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-400">no</span></span>           |
| <span data-ttu-id="b14ef-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b14ef-401">msdyn_finish</span></span>                 | <span data-ttu-id="b14ef-402">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-402">no</span></span>             | <span data-ttu-id="b14ef-403">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-403">no</span></span>           |
| <span data-ttu-id="b14ef-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="b14ef-405">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-405">no</span></span>             | <span data-ttu-id="b14ef-406">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-406">no</span></span>           |
| <span data-ttu-id="b14ef-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="b14ef-408">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-408">no</span></span>             | <span data-ttu-id="b14ef-409">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-409">no</span></span>           |
| <span data-ttu-id="b14ef-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b14ef-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="b14ef-411">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-411">no</span></span>             | <span data-ttu-id="b14ef-412">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-412">no</span></span>           |
| <span data-ttu-id="b14ef-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="b14ef-414">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-414">no</span></span>             | <span data-ttu-id="b14ef-415">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-415">no</span></span>           |
| <span data-ttu-id="b14ef-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="b14ef-417">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-417">no</span></span>             | <span data-ttu-id="b14ef-418">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-418">no</span></span>           |
| <span data-ttu-id="b14ef-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b14ef-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="b14ef-420">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-420">no</span></span>             | <span data-ttu-id="b14ef-421">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-421">no</span></span>           |
| <span data-ttu-id="b14ef-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b14ef-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="b14ef-423">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-423">no</span></span>             | <span data-ttu-id="b14ef-424">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-424">no</span></span>           |
| <span data-ttu-id="b14ef-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="b14ef-425">msdyn_projectid</span></span>              | <span data-ttu-id="b14ef-426">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-426">yes</span></span>            | <span data-ttu-id="b14ef-427">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-427">no</span></span>           |
| <span data-ttu-id="b14ef-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-428">msdyn_projectidname</span></span>          | <span data-ttu-id="b14ef-429">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-429">no</span></span>             | <span data-ttu-id="b14ef-430">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-430">no</span></span>           |
| <span data-ttu-id="b14ef-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="b14ef-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="b14ef-432">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-432">no</span></span>             | <span data-ttu-id="b14ef-433">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-433">no</span></span>           |
| <span data-ttu-id="b14ef-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="b14ef-435">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-435">no</span></span>             | <span data-ttu-id="b14ef-436">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-436">no</span></span>           |
| <span data-ttu-id="b14ef-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b14ef-437">msdyn_start</span></span>                  | <span data-ttu-id="b14ef-438">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-438">no</span></span>             | <span data-ttu-id="b14ef-439">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-439">no</span></span>           |
| <span data-ttu-id="b14ef-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="b14ef-440">msdyn_taskid</span></span>                 | <span data-ttu-id="b14ef-441">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-441">no</span></span>             | <span data-ttu-id="b14ef-442">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-442">no</span></span>           |
| <span data-ttu-id="b14ef-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-443">msdyn_taskidname</span></span>             | <span data-ttu-id="b14ef-444">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-444">no</span></span>             | <span data-ttu-id="b14ef-445">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-445">no</span></span>           |
| <span data-ttu-id="b14ef-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="b14ef-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="b14ef-447">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-447">no</span></span>             | <span data-ttu-id="b14ef-448">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="b14ef-449">A projekt csapattagja</span><span class="sxs-lookup"><span data-stu-id="b14ef-449">Project team member</span></span>

| <span data-ttu-id="b14ef-450">**Logikai név**</span><span class="sxs-lookup"><span data-stu-id="b14ef-450">**Logical name**</span></span>                                 | <span data-ttu-id="b14ef-451">**Létrehozhat**</span><span class="sxs-lookup"><span data-stu-id="b14ef-451">**Can create**</span></span> | <span data-ttu-id="b14ef-452">**Szerkeszthet**</span><span class="sxs-lookup"><span data-stu-id="b14ef-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="b14ef-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="b14ef-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="b14ef-454">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-454">no</span></span>             | <span data-ttu-id="b14ef-455">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-455">no</span></span>           |
| <span data-ttu-id="b14ef-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="b14ef-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="b14ef-457">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-457">no</span></span>             | <span data-ttu-id="b14ef-458">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-458">no</span></span>           |
| <span data-ttu-id="b14ef-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="b14ef-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="b14ef-460">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-460">no</span></span>             | <span data-ttu-id="b14ef-461">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-461">no</span></span>           |
| <span data-ttu-id="b14ef-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="b14ef-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="b14ef-463">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-463">no</span></span>             | <span data-ttu-id="b14ef-464">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-464">no</span></span>           |
| <span data-ttu-id="b14ef-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b14ef-465">msdyn_effort</span></span>                                     | <span data-ttu-id="b14ef-466">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-466">no</span></span>             | <span data-ttu-id="b14ef-467">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-467">no</span></span>           |
| <span data-ttu-id="b14ef-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b14ef-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="b14ef-469">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-469">no</span></span>             | <span data-ttu-id="b14ef-470">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-470">no</span></span>           |
| <span data-ttu-id="b14ef-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b14ef-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="b14ef-472">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-472">no</span></span>             | <span data-ttu-id="b14ef-473">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-473">no</span></span>           |
| <span data-ttu-id="b14ef-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b14ef-474">msdyn_finish</span></span>                                     | <span data-ttu-id="b14ef-475">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-475">no</span></span>             | <span data-ttu-id="b14ef-476">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-476">no</span></span>           |
| <span data-ttu-id="b14ef-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="b14ef-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="b14ef-478">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-478">no</span></span>             | <span data-ttu-id="b14ef-479">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-479">no</span></span>           |
| <span data-ttu-id="b14ef-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="b14ef-480">msdyn_hours</span></span>                                      | <span data-ttu-id="b14ef-481">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-481">no</span></span>             | <span data-ttu-id="b14ef-482">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-482">no</span></span>           |
| <span data-ttu-id="b14ef-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="b14ef-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="b14ef-484">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-484">no</span></span>             | <span data-ttu-id="b14ef-485">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-485">no</span></span>           |
| <span data-ttu-id="b14ef-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="b14ef-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="b14ef-487">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-487">no</span></span>             | <span data-ttu-id="b14ef-488">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-488">no</span></span>           |
| <span data-ttu-id="b14ef-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b14ef-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="b14ef-490">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-490">no</span></span>             | <span data-ttu-id="b14ef-491">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-491">no</span></span>           |
| <span data-ttu-id="b14ef-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="b14ef-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="b14ef-493">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-493">no</span></span>             | <span data-ttu-id="b14ef-494">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-494">no</span></span>           |
| <span data-ttu-id="b14ef-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="b14ef-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="b14ef-496">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-496">no</span></span>             | <span data-ttu-id="b14ef-497">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-497">no</span></span>           |
| <span data-ttu-id="b14ef-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="b14ef-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="b14ef-499">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-499">no</span></span>             | <span data-ttu-id="b14ef-500">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-500">no</span></span>           |
| <span data-ttu-id="b14ef-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b14ef-501">msdyn_start</span></span>                                      | <span data-ttu-id="b14ef-502">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-502">no</span></span>             | <span data-ttu-id="b14ef-503">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="b14ef-504">Project</span><span class="sxs-lookup"><span data-stu-id="b14ef-504">Project</span></span>

| <span data-ttu-id="b14ef-505">**Logikai név**</span><span class="sxs-lookup"><span data-stu-id="b14ef-505">**Logical name**</span></span>                       | <span data-ttu-id="b14ef-506">**Létrehozhat**</span><span class="sxs-lookup"><span data-stu-id="b14ef-506">**Can create**</span></span> | <span data-ttu-id="b14ef-507">**Szerkeszthet**</span><span class="sxs-lookup"><span data-stu-id="b14ef-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="b14ef-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="b14ef-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="b14ef-509">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-509">no</span></span>             | <span data-ttu-id="b14ef-510">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-510">no</span></span>           |
| <span data-ttu-id="b14ef-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="b14ef-512">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-512">no</span></span>             | <span data-ttu-id="b14ef-513">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-513">no</span></span>           |
| <span data-ttu-id="b14ef-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="b14ef-515">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-515">no</span></span>             | <span data-ttu-id="b14ef-516">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-516">no</span></span>           |
| <span data-ttu-id="b14ef-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="b14ef-518">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-518">no</span></span>             | <span data-ttu-id="b14ef-519">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-519">no</span></span>           |
| <span data-ttu-id="b14ef-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="b14ef-521">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-521">no</span></span>             | <span data-ttu-id="b14ef-522">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-522">no</span></span>           |
| <span data-ttu-id="b14ef-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b14ef-524">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-524">no</span></span>             | <span data-ttu-id="b14ef-525">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-525">no</span></span>           |
| <span data-ttu-id="b14ef-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="b14ef-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="b14ef-527">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-527">yes</span></span>            | <span data-ttu-id="b14ef-528">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-528">no</span></span>           |
| <span data-ttu-id="b14ef-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b14ef-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="b14ef-530">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-530">yes</span></span>            | <span data-ttu-id="b14ef-531">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-531">no</span></span>           |
| <span data-ttu-id="b14ef-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b14ef-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="b14ef-533">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-533">yes</span></span>            | <span data-ttu-id="b14ef-534">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-534">no</span></span>           |
| <span data-ttu-id="b14ef-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="b14ef-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="b14ef-536">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-536">no</span></span>             | <span data-ttu-id="b14ef-537">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-537">no</span></span>           |
| <span data-ttu-id="b14ef-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b14ef-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="b14ef-539">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-539">no</span></span>             | <span data-ttu-id="b14ef-540">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-540">no</span></span>           |
| <span data-ttu-id="b14ef-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="b14ef-542">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-542">no</span></span>             | <span data-ttu-id="b14ef-543">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-543">no</span></span>           |
| <span data-ttu-id="b14ef-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="b14ef-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="b14ef-545">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-545">no</span></span>             | <span data-ttu-id="b14ef-546">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-546">no</span></span>           |
| <span data-ttu-id="b14ef-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="b14ef-548">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-548">no</span></span>             | <span data-ttu-id="b14ef-549">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-549">no</span></span>           |
| <span data-ttu-id="b14ef-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="b14ef-550">msdyn_duration</span></span>                         | <span data-ttu-id="b14ef-551">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-551">no</span></span>             | <span data-ttu-id="b14ef-552">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-552">no</span></span>           |
| <span data-ttu-id="b14ef-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b14ef-553">msdyn_effort</span></span>                           | <span data-ttu-id="b14ef-554">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-554">no</span></span>             | <span data-ttu-id="b14ef-555">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-555">no</span></span>           |
| <span data-ttu-id="b14ef-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b14ef-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b14ef-557">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-557">no</span></span>             | <span data-ttu-id="b14ef-558">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-558">no</span></span>           |
| <span data-ttu-id="b14ef-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b14ef-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="b14ef-560">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-560">no</span></span>             | <span data-ttu-id="b14ef-561">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-561">no</span></span>           |
| <span data-ttu-id="b14ef-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b14ef-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="b14ef-563">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-563">no</span></span>             | <span data-ttu-id="b14ef-564">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-564">no</span></span>           |
| <span data-ttu-id="b14ef-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b14ef-565">msdyn_finish</span></span>                           | <span data-ttu-id="b14ef-566">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-566">yes</span></span>            | <span data-ttu-id="b14ef-567">igen</span><span class="sxs-lookup"><span data-stu-id="b14ef-567">yes</span></span>          |
| <span data-ttu-id="b14ef-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="b14ef-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="b14ef-569">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-569">no</span></span>             | <span data-ttu-id="b14ef-570">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-570">no</span></span>           |
| <span data-ttu-id="b14ef-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="b14ef-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="b14ef-572">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-572">no</span></span>             | <span data-ttu-id="b14ef-573">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-573">no</span></span>           |
| <span data-ttu-id="b14ef-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="b14ef-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="b14ef-575">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-575">no</span></span>             | <span data-ttu-id="b14ef-576">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-576">no</span></span>           |
| <span data-ttu-id="b14ef-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="b14ef-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="b14ef-578">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-578">no</span></span>             | <span data-ttu-id="b14ef-579">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-579">no</span></span>           |
| <span data-ttu-id="b14ef-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="b14ef-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="b14ef-581">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-581">no</span></span>             | <span data-ttu-id="b14ef-582">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-582">no</span></span>           |
| <span data-ttu-id="b14ef-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="b14ef-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="b14ef-584">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-584">no</span></span>             | <span data-ttu-id="b14ef-585">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-585">no</span></span>           |
| <span data-ttu-id="b14ef-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="b14ef-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="b14ef-587">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-587">no</span></span>             | <span data-ttu-id="b14ef-588">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-588">no</span></span>           |
| <span data-ttu-id="b14ef-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="b14ef-590">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-590">no</span></span>             | <span data-ttu-id="b14ef-591">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-591">no</span></span>           |
| <span data-ttu-id="b14ef-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="b14ef-593">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-593">no</span></span>             | <span data-ttu-id="b14ef-594">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-594">no</span></span>           |
| <span data-ttu-id="b14ef-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="b14ef-596">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-596">no</span></span>             | <span data-ttu-id="b14ef-597">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-597">no</span></span>           |
| <span data-ttu-id="b14ef-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b14ef-599">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-599">no</span></span>             | <span data-ttu-id="b14ef-600">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-600">no</span></span>           |
| <span data-ttu-id="b14ef-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b14ef-602">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-602">no</span></span>             | <span data-ttu-id="b14ef-603">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-603">no</span></span>           |
| <span data-ttu-id="b14ef-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b14ef-604">msdyn_progress</span></span>                         | <span data-ttu-id="b14ef-605">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-605">no</span></span>             | <span data-ttu-id="b14ef-606">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-606">no</span></span>           |
| <span data-ttu-id="b14ef-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b14ef-608">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-608">no</span></span>             | <span data-ttu-id="b14ef-609">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-609">no</span></span>           |
| <span data-ttu-id="b14ef-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b14ef-611">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-611">no</span></span>             | <span data-ttu-id="b14ef-612">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-612">no</span></span>           |
| <span data-ttu-id="b14ef-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b14ef-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b14ef-614">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-614">no</span></span>             | <span data-ttu-id="b14ef-615">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-615">no</span></span>           |
| <span data-ttu-id="b14ef-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b14ef-617">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-617">no</span></span>             | <span data-ttu-id="b14ef-618">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-618">no</span></span>           |
| <span data-ttu-id="b14ef-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="b14ef-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="b14ef-620">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-620">no</span></span>             | <span data-ttu-id="b14ef-621">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-621">no</span></span>           |
| <span data-ttu-id="b14ef-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="b14ef-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="b14ef-623">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-623">no</span></span>             | <span data-ttu-id="b14ef-624">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-624">no</span></span>           |
| <span data-ttu-id="b14ef-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b14ef-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="b14ef-626">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-626">no</span></span>             | <span data-ttu-id="b14ef-627">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-627">no</span></span>           |
| <span data-ttu-id="b14ef-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="b14ef-629">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-629">no</span></span>             | <span data-ttu-id="b14ef-630">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-630">no</span></span>           |
| <span data-ttu-id="b14ef-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b14ef-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b14ef-632">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-632">no</span></span>             | <span data-ttu-id="b14ef-633">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-633">no</span></span>           |
| <span data-ttu-id="b14ef-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b14ef-635">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-635">no</span></span>             | <span data-ttu-id="b14ef-636">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-636">no</span></span>           |
| <span data-ttu-id="b14ef-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="b14ef-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="b14ef-638">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-638">no</span></span>             | <span data-ttu-id="b14ef-639">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-639">no</span></span>           |
| <span data-ttu-id="b14ef-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="b14ef-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="b14ef-641">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-641">no</span></span>             | <span data-ttu-id="b14ef-642">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-642">no</span></span>           |
| <span data-ttu-id="b14ef-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b14ef-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b14ef-644">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-644">no</span></span>             | <span data-ttu-id="b14ef-645">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-645">no</span></span>           |
| <span data-ttu-id="b14ef-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="b14ef-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="b14ef-647">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-647">no</span></span>             | <span data-ttu-id="b14ef-648">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-648">no</span></span>           |
| <span data-ttu-id="b14ef-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="b14ef-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="b14ef-650">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-650">no</span></span>             | <span data-ttu-id="b14ef-651">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-651">no</span></span>           |
| <span data-ttu-id="b14ef-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="b14ef-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="b14ef-653">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-653">no</span></span>             | <span data-ttu-id="b14ef-654">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-654">no</span></span>           |
| <span data-ttu-id="b14ef-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="b14ef-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="b14ef-656">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-656">no</span></span>             | <span data-ttu-id="b14ef-657">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-657">no</span></span>           |
| <span data-ttu-id="b14ef-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="b14ef-659">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-659">no</span></span>             | <span data-ttu-id="b14ef-660">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-660">no</span></span>           |
| <span data-ttu-id="b14ef-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="b14ef-662">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-662">no</span></span>             | <span data-ttu-id="b14ef-663">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-663">no</span></span>           |
| <span data-ttu-id="b14ef-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="b14ef-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="b14ef-665">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-665">no</span></span>             | <span data-ttu-id="b14ef-666">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-666">no</span></span>           |
| <span data-ttu-id="b14ef-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b14ef-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="b14ef-668">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-668">no</span></span>             | <span data-ttu-id="b14ef-669">nem</span><span class="sxs-lookup"><span data-stu-id="b14ef-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="b14ef-670">Korlátozások és ismert problémák</span><span class="sxs-lookup"><span data-stu-id="b14ef-670">Limitations and known issues</span></span>
<span data-ttu-id="b14ef-671">Az alábbiakban felsoroljuk a korlátozásokat és az ismert problémákat:</span><span class="sxs-lookup"><span data-stu-id="b14ef-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="b14ef-672">Az ütemezési API-kat csak **Microsoft Project licenccel rendelkező felhasználók használhatják**.</span><span class="sxs-lookup"><span data-stu-id="b14ef-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="b14ef-673">Nem használhatják:</span><span class="sxs-lookup"><span data-stu-id="b14ef-673">They can't be used by:</span></span>
    - <span data-ttu-id="b14ef-674">Alkalmazásfelhasználók</span><span class="sxs-lookup"><span data-stu-id="b14ef-674">Application users</span></span>
    - <span data-ttu-id="b14ef-675">Rendszerfelhasználók</span><span class="sxs-lookup"><span data-stu-id="b14ef-675">System users</span></span>
    - <span data-ttu-id="b14ef-676">Integrációs felhasználók</span><span class="sxs-lookup"><span data-stu-id="b14ef-676">Integration users</span></span>
    - <span data-ttu-id="b14ef-677">Más felhasználók, akik nem rendelkeznek a szükséges licenccel</span><span class="sxs-lookup"><span data-stu-id="b14ef-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="b14ef-678">Minden **OperationSet** legfeljebb 100 művelettel rendelkezhet.</span><span class="sxs-lookup"><span data-stu-id="b14ef-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="b14ef-679">Minden felhasználó legfeljebb 10 nyitott **OperationSet** művelettel rendelkezhet.</span><span class="sxs-lookup"><span data-stu-id="b14ef-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="b14ef-680">A Project Operations jelenleg legfeljebb 500 projektfeladatot támogat.</span><span class="sxs-lookup"><span data-stu-id="b14ef-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="b14ef-681">Az **OperationSet** hibaállapotok és hibanaplók jelenleg nem érhetők el.</span><span class="sxs-lookup"><span data-stu-id="b14ef-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="b14ef-682">Az ütemezési API-k nyilvános előzetes verzióban vannak.</span><span class="sxs-lookup"><span data-stu-id="b14ef-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="b14ef-683">Ezeket az API-kat Működési környezetben nem támogatja a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b14ef-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="b14ef-684">Projektek és feladatok korlátai és korlátai</span><span class="sxs-lookup"><span data-stu-id="b14ef-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="b14ef-685">Hibakezelés</span><span class="sxs-lookup"><span data-stu-id="b14ef-685">Error handling</span></span>

   - <span data-ttu-id="b14ef-686">Az Operation Setsből generált hibák áttekintéséhez lépjen a **Beállítások** \> **Ütemezésintegráció** \> **Műveleti készletek** lapra.</span><span class="sxs-lookup"><span data-stu-id="b14ef-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="b14ef-687">A Projektütemezési szolgáltatás által generált hibák áttekintéséhez lépjen a **Beállítások** \> **Ütemezési integráció** \> **PSS hibanaplók** menüpontba.</span><span class="sxs-lookup"><span data-stu-id="b14ef-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="b14ef-688">Példaforgatókönyv</span><span class="sxs-lookup"><span data-stu-id="b14ef-688">Sample scenario</span></span>

<span data-ttu-id="b14ef-689">Ebben a forgatókönyvben létre fog hozni egy projektet, egy csoporttagot, négy feladatot és két erőforrás-hozzárendelést.</span><span class="sxs-lookup"><span data-stu-id="b14ef-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="b14ef-690">Ezután frissít egy feladatot, frissíti a projektet, töröl egy feladatot, töröl egy erőforrás-hozzárendelést, és létrehoz egy feladatfüggőséget.</span><span class="sxs-lookup"><span data-stu-id="b14ef-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="b14ef-691">További minták</span><span class="sxs-lookup"><span data-stu-id="b14ef-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
