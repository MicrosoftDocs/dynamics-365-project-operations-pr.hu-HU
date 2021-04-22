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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Ütemezési API-k használata az Ütemezési entitásokkal végzett műveletekhez

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_

> [!IMPORTANT] 
> A témakörben ismertetett egyes funkciók vagy az összes funkció az előzetes verzió részeként áll rendelkezésre. A tartalom és a funkciók tekintetében a változtatás jogát fenntartjuk. 

## <a name="scheduling-entities"></a>Ütemezési entitások

Az ütemezési API-k lehetővé teszik a létrehozási, frissítési és törlési műveletek elvégzését az **Ütemezési entitásokkal**. Ezeket az entitásokat a Project for the web ütemezési motorja kezeli. Az **Ütemezési entitásokkal** végzett műveletek létrehozása, frissítése és törlése korlátozott volt a korábbi Dynamics 365 Project Operations kiadásokban.

Az alábbi tábla az **Ütemezési entitások** teljes listáját tartalmazza.

| Entitás neve  | Entitás logikai neve |
| --- | --- |
| Project | msdyn_project |
| Projektfeladat  | msdyn_projecttask  |
| Projektfeladat függősége  | msdyn_projecttaskdependency  |
| Erőforrás-hozzárendelés | msdyn_resourceassignment |
| Projektgyűjtő  | msdyn_projectbucket |
| Projektcsoporttag | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

Az OperationSet egy munkaegység-minta, amely akkor használható, ha egy tranzakción belül több ütemezést is fel kell dolgozni, amely a kérelmeket érinti.

## <a name="schedule-apis"></a>API-k ütemezése

Az alábbiakban az aktuális ütemezési API-k listája szerepel.

- **msdyn_CreateProjectV1**: Ez az API projekt létrehozására használható. A projekt és az alapértelmezett projektgyűjtő azonnal létrejön.
- **msdyn_CreateTeamMemberV1**: Ez az API projekt csoporttag létrehozására használható. A csoporttag-rekord azonnal létrejön.
- **msdyn_CreateOperationSetV1**: Ez az API több olyan kérés ütemezésére használható, amelyet egy tranzakción belül kell végrehajtani.
- **msdyn_PSSCreateV1**: Ez az API entitás létrehozására használható. Az entitás lehet a létrehozási műveletet támogató Ütemezési entitások bármelyike.
- **msdyn_PSSUpdateV1**: Ez az API entitás frissítésére használható. Az entitás lehet a frissítési műveletet támogató Ütemezési entitások bármelyike.
- **msdyn_PSSDeleteV1**: Ez az API entitás törlésére használható. Az entitás lehet a törlési műveletet támogató Ütemezési entitások bármelyike.
- **msdyn_ExecuteOperationSetV1**: Ez az API az adott műveletkészleten belüli összes művelet végrehajtására használható.

## <a name="using-schedule-apis-with-operationset"></a>Ütemezési API-k használata az OperationSettel

Mivel a **CreateProjectV1** és a **CreateTeamMemberV1** rekordok azonnal létrejönnek, ezek az API-k nem használhatók közvetlenül az **OperationSetben**. Az API-val azonban létrehozhatja a szükséges rekordokat, létrehozhat egy **OperationSetet**, majd használhatja ezeket az előre létrehozott rekordokat az **OperationSetben**.

## <a name="supported-operations"></a>Támogatott műveletek

| Ütemezési entitás | Létrehozás | Frissítés | Delete | Fontos tényezők |
| --- | --- | --- | --- | --- |
Projektfeladat | Igen | Igen | Igen | Egyik sem |
| Projektfeladat függősége | Igen | Igen | | A projektfeladat függőségi rekordok nem frissülnek. Ehelyett egy régi rekord törölhető, és új rekord is létrehozható. |
| Erőforrás-hozzárendelés | Igen | Igen | | A következő mezőkkel végzett műveletek nem támogatottak: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** és **PlannedWork**. Az erőforrás-hozzárendelési rekordok nem frissülnek. Ehelyett a régi rekord törölhető, és új rekord is létrehozható. |
| Projektgyűjtő | N. a. | N. a. | N. a. | Az alapértelmezett gyűjtő létrehozása a **CreateProjectV1** API használatával jön létre. |
| A projekt csapattagja | Igen | Igen | Igen | A létrehozáshoz használja a **CreateTeamMemberV1** API-t. |
| Project | Igen | Igen | N. a. | A következő mezőkkel végzett műveletek nem támogatottak: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, és **Duration**. |

Ezek az API-k egyéni mezőket tartalmazó entitásobjektumokkal hívhatóak meg.

Ez az azonosító-tulajdonság nem kötelező. Ha rendelkezésre áll, a rendszer megpróbálja használni, illetve kivételt okoz, ha nem használható. Ha nincs biztosítva, a rendszer fogja létrehozni.

## <a name="limitations-and-known-issues"></a>Korlátozások és ismert problémák
Az alábbiakban felsoroljuk a korlátozásokat és az ismert problémákat:

- Az ütemezési API-kat csak **Microsoft Project licenccel rendelkező felhasználók használhatják**. Nem használhatják:
    - Alkalmazásfelhasználók
    - Rendszerfelhasználók
    - Integrációs felhasználók
    - Más felhasználók, akik nem rendelkeznek a szükséges licenccel
- Minden **OperationSet** legfeljebb 100 művelettel rendelkezhet.
- Minden felhasználó legfeljebb 10 nyitott **OperationSet** művelettel rendelkezhet.
- A Project Operations jelenleg legfeljebb 500 projektfeladatot támogat.
- Az **OperationSet** hibaállapotok és hibanaplók jelenleg nem érhetők el.
- Az ütemezési API-k nyilvános előzetes verzióban vannak. Ezeket az API-kat Működési környezetben nem támogatja a Microsoft.

## <a name="sample-scenario"></a>Példaforgatókönyv

Ebben a forgatókönyvben létre fog hozni egy projektet, egy csoporttagot, négy feladatot és két erőforrás-hozzárendelést. Ezután frissít egy feladatot, frissíti a projektet, töröl egy feladatot, töröl egy erőforrás-hozzárendelést, és létrehoz egy feladatfüggőséget.

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

## <a name="additional-samples"></a>További minták

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
