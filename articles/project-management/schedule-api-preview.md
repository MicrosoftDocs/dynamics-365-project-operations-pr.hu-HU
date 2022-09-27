---
title: Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal
description: Ez a cikk információkat és mintákat tartalmaz a Project ütemezési API-k használatához.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541127"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projektütemezés API-k használata műveletek végrehajtásához az Ütemező entitásokkal

_**A következőre vonatkozik:** Project Operations erőforrás-/nem készletalapú forgatókönyvek esetén, egyszerű telepítés – proforma számlázás_


**Ütemezési entitások**

A projektütemezési API-k lehetőséget biztosítanak a létrehozási, frissítési és törlési műveletek végrehajtására **Ütemező entitásokkal**. Ezeket az entitásokat a Project for the web ütemezési motorja kezeli. Az **Ütemezési entitásokkal** végzett műveletek létrehozása, frissítése és törlése korlátozott volt a korábbi Dynamics 365 Project Operations kiadásokban.

Az alábbi táblázat a Projektütemezési entitások teljes listáját tartalmazza.

| **Entitás neve**         | **Entitás logikai neve**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektfeladat            | msdyn_projecttask           |
| Projektfeladat függősége | msdyn_projecttaskdependency |
| Erőforrás-hozzárendelés     | msdyn_resourceassignment    |
| Projektgyűjtő          | msdyn_projectbucket         |
| Projektcsoporttag     | msdyn_projectteam           |
| Projekt-ellenőrzőlisták      | msdyn_projectchecklist      |
| Projektcímke           | msdyn_projectlabel          |
| A címkézendő projektfeladat   | msdyn_projecttasktolabel    |
| Projektfutam          | msdyn_projectsprint         |

**OperationSet**

Az OperationSet egy munkaegység-minta, amely akkor használható, ha egy tranzakción belül több ütemezést is fel kell dolgozni, amely a kérelmeket érinti.

**Projektütemezés API-k**

A következő lista az aktuális Projektütemezési API-kat sorolja fel.

| **Api**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Ez az API egy projekt létrehozására szolgál. A projekt és az alapértelmezett projektvödör azonnal létrejön.                         |
| **msdyn_CreateTeamMemberV1**            | Ez az API egy projektcsapat-tag létrehozására szolgál. A csoporttag-rekord azonnal létrejön.                                  |
| **msdyn_CreateOperationSetV1**          | Ez az API több olyan kérés ütemezésére szolgál, amelyeket egy tranzakción belül kell végrehajtani.                                        |
| **msdyn_PssCreateV1**                   | Ez az API egy entitás létrehozására szolgál. Az entitás a létrehozási műveletet támogató bármely Projektütemezési entitás lehet. |
| **msdyn_PssUpdateV1**                   | Ez az API egy entitás frissítésére szolgál. Az entitás lehet a frissítési műveletet támogató Projektütemezés-entitások bármelyike  |
| **msdyn_PssDeleteV1**                   | Ez az API egy entitás törlésére szolgál. Az entitás a törlés műveletet támogató bármely Projektütemezési entitás lehet. |
| **msdyn_ExecuteOperationSetV1**         | Ez az API az adott műveletkészleten belüli összes művelet végrehajtására szolgál.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Ez az API az erőforrás-hozzárendelés tervezett munkaeloszlásának frissítésére szolgál.                                                        |



**Projektütemezési API-k használata az OperationSet elemmel**

Mivel a **CreateProjectV1** és a **CreateTeamMemberV1** rekordok azonnal létrejönnek, ezek az API-k nem használhatók közvetlenül az **OperationSetben**. Az API-val azonban létrehozhatja a szükséges rekordokat, létrehozhat egy **OperationSetet**, majd használhatja ezeket az előre létrehozott rekordokat az **OperationSetben**.

**Támogatott műveletek**

| **Ütemezési entitás**   | **Létrehozás** | **Frissítés** | **Delete** | **Fontos tényezők**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektfeladat            | Igen        | Igen        | Igen        | A **Folyamat,** **a Befejezett munkamennyiség** és **a Munkaigénylés** mezők szerkeszthetők a Webes Projektben, de a Project Operationsben nem szerkeszthetők.                                                                                                                                                                                             |
| Projektfeladat függősége | Igen        | No         | Igen        | A projektfeladat függőségi rekordok nem frissülnek. Ehelyett egy régi rekord törölhető, és létrehozható egy új rekord.                                                                                                                                                                                                                                 |
| Erőforrás-hozzárendelés     | Igen        | Igen\*      | Igen        | A következő mezőkkel végzett műveletek nem támogatottak: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** és **PlannedWork**. Az erőforrás-hozzárendelési rekordok nem frissülnek. Ehelyett a régi rekord törölhető, és létrehozható egy új rekord. Külön API-t biztosítottunk az erőforrás-hozzárendelési eloszlások frissítéséhez. |
| Projektgyűjtő          | Igen        | Igen        | Igen        | Az alapértelmezett gyűjtő a **CreateProjectV1** API használatával jön létre. A projektgyűjtők létrehozásának és törlésének támogatása a 16-os frissítésben lett hozzáadva.                                                                                                                                                                                                   |
| A projekt csapattagja     | Igen        | Igen        | Igen        | A létrehozáshoz használja a **CreateTeamMemberV1** API-t.                                                                                                                                                                                                                                                                                           |
| Project                 | Igen        | Igen        |            | A következő mezőkkel végzett műveletek nem támogatottak: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, és **Duration**.                                                                                       |
| Projekt-ellenőrzőlisták      | Igen        | Igen        | Igen        |                                                                                                                                                                                                                                                                                                                                                         |
| Projektcímke           | No         | Igen        | No         | A címkenevek módosíthatók. Ez a szolgáltatás csak a Webes Projecthez bővítményhez érhető el                                                                                                                                                                                                                                                                      |
| A címkézendő projektfeladat   | Igen        | No         | Igen        | Ez a szolgáltatás csak a Webes Projecthez bővítményhez érhető el                                                                                                                                                                                                                                                                                                  |
| Projektfutam          | Igen        | Igen        | Igen        | A **Kezdés** mező dátumának korábbinak kell lennie, mint a **Befejezés** mezőnek. Ugyanazon projekt sprintjei nem lehetnek átfedésben egymással. Ez a szolgáltatás csak a Webes Projecthez bővítményhez érhető el                                                                                                                                                                    |




Ez az azonosító-tulajdonság nem kötelező. Ha rendelkezésre áll, a rendszer megpróbálja használni, illetve kivételt okoz, ha nem használható. Ha nincs biztosítva, a rendszer fogja létrehozni.

**Korlátozások és ismert problémák**

Az alábbiakban felsoroljuk a korlátozásokat és az ismert problémákat:

-   A Projektütemezés API-kat csak a Microsoft Project licenccel **rendelkező felhasználók használhatják**. Nem használhatják:
    -   Alkalmazásfelhasználók
    -   Rendszerfelhasználók
    -   Integrációs felhasználók
    -   Más felhasználók, akik nem rendelkeznek a szükséges licenccel
-   Minden **OperationSet** legfeljebb 100 művelettel rendelkezhet.
-   Minden felhasználó legfeljebb 10 nyitott **OperationSet** művelettel rendelkezhet.
-   A Project Operations jelenleg legfeljebb 500 projektfeladatot támogat.
-   Minden Erőforrás-hozzárendelési eloszlás frissítése művelet egyetlen műveletnek számít.
-   A frissített kontúrok minden listája legfeljebb 100 időszeletet tartalmazhat.
-   Az **OperationSet** hibaállapotok és hibanaplók jelenleg nem érhetők el.
-   Projektenként legfeljebb 400 sprint van.
-   [A projektek és tevékenységek](/project-for-the-web/project-for-the-web-limits-and-boundaries) korlátai és határai.
-   A címkék jelenleg csak a Webes Projecthez érhetők el.

**Hibakezelés**

-   Az Operation Setsből generált hibák áttekintéséhez lépjen a **Beállítások** \> **Ütemezésintegráció** \> **Műveleti készletek** lapra.
-   A Projektütemező szolgáltatásból származó hibák megtekintéséhez menjena **Beállítások** \> **Ütemezésintegráció** \> **PSS hibanaplókban** menübe.

**Erőforrás-hozzárendelési kontúrok szerkesztése**

Az entitást frissítő összes többi projektütemezési API-val ellentétben az erőforrás-hozzárendelési kontúr API kizárólag egyetlen mező, msdyn_plannedwork egyetlen entitáson msydn_resourceassignment frissítéséért felelős.

Adott ütemezési mód:

-   **rögzített egységek**
-   A projektnaptár 9-5p 9-5pst, hétfő, kedd, Thurs, péntek (NINCS MUNKA SZERDÁNKÉNT)
-   Az erőforrásnaptár pedig 9-1p PST hétfőtől péntekig

Ez a feladat egy hétre, napi négy órára szól. Ennek az az oka, hogy az erőforrásnaptár 9-1 PST vagy napi négy óra között van.

| &nbsp;     | Feladatok | Kezdési dátum | Befejező dátum  | Mennyiség | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 munkavállaló |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Ha például azt szeretné, hogy a dolgozó ezen a héten naponta csak három órát dolgozzon, és egy órát hagyjon más tevékenységek számára.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours minta hasznos adat:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Ez a hozzárendelés az Update Contour Schedule API futtatása után.

| &nbsp;     | Feladatok | Kezdési dátum | Befejező dátum  | Mennyiség | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 munkavállaló | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Példaforgatókönyv**

Ebben a forgatókönyvben létre fog hozni egy projektet, egy csoporttagot, négy feladatot és két erőforrás-hozzárendelést. Ezután frissít egy feladatot, frissíti a projektet, töröl egy feladatot, töröl egy erőforrás-hozzárendelést, és létrehoz egy feladatfüggőséget.

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

** További minták

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
