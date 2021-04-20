---
title: Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen
description: Dieses Thema enthält Informationen und Beispiele für die Verwendung von Zeitplan-APIs.
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
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868128"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

> [!IMPORTANT] 
> Einige oder alle der in diesem Thema genannten Funktionen stehen im Rahmen einer Vorschauversion zur Verfügung. Inhalt und Funktionalität können sich ändern. 

## <a name="scheduling-entities"></a>Planungsentitäten

Zeitplan-APIs bieten die Möglichkeit, Erstellungs-, Aktualisierungs- und Löschvorgänge mit **Planungsentitäten** auszuführen. Diese Entitäten werden über das Planungsmodul in Project für das Web verwaltet. Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten** wurden in früheren Version von Dynamics 365 Project Operations eingeschränkt.

Die folgende Tabelle enthält eine vollständige Liste der **Planungsentitäten**.

| Entitätsname  | Logischer Entitätsname |
| --- | --- |
| Project | msdyn_project |
| Projektaufgabe  | msdyn_projecttask  |
| Abhängigkeit der Projektaufgaben  | msdyn_projecttaskdependency  |
| Ressourcenzuweisung | msdyn_resourceassignment |
| Projekt-Bucket  | msdyn_projectbucket |
| Projektteammitglied | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet ist ein Arbeitseinheitsmuster, das verwendet werden kann, wenn innerhalb einer Transaktion mehrere zeitplanbezogene Anforderungen verarbeitet werden müssen.

## <a name="schedule-apis"></a>Zeitplan-APIs

Im Folgenden finden Sie eine Liste der aktuellen Zeitplan-APIs.

- **msdyn_CreateProjectV1**: Mit dieser API kann ein Projekt erstellt werden. Der Projekt- und Standardprojekt-Bucket wird sofort erstellt.
- **msdyn_CreateTeamMemberV1**: Mit dieser API kann ein Projektteammitglied erstellt werden. Der Teammitgliedsdatensatz wird sofort erstellt.
- **msdyn_CreateOperationSetV1**: Mit dieser API können mehrere Anforderungen geplant werden, die innerhalb einer Transaktion ausgeführt werden müssen.
- **msdyn_PSSCreateV1**: Mit dieser API kann eine Entität erstellt werden. Die Entität kann eine der Planungsentitäten sein, die den Erstellungsvorgang unterstützen.
- **msdyn_PSSUpdateV1**: Mit dieser API kann eine Entität aktualisiert werden. Die Entität kann eine der Planungsentitäten sein, die den Aktualisierungsvorgang unterstützen.
- **msdyn_PSSDeleteV1**: Mit dieser API kann eine Entität gelöscht werden. Die Entität kann eine der Planungsentitäten sein, die den Löschvorgang unterstützen.
- **msdyn_ExecuteOperationSetV1**: Diese API wird verwendet, um alle Operationen innerhalb des angegebenen Operationssatzes auszuführen.

## <a name="using-schedule-apis-with-operationset"></a>Verwenden von Zeitplan-APIs mit OperationSet

Weil Aufzeichnungen sowohl mit **CreateProjectV1** als auch **CreateTeamMemberV1** sofort erstellt werden, können diese APIs nicht direkt im **OperationSet** verwendet werden. Sie können jedoch die API verwenden, um die erforderlichen Datensätze zu erstellen, ein **OperationSet** zu erstellen und dann diese vorab erstellten Datensätze im **OperationSet** zu verwenden.

## <a name="supported-operations"></a>Unterstützte Vorgänge

| Planungsentität | Erstellen | Update | Entf | Wichtige Überlegungen |
| --- | --- | --- | --- | --- |
Projektaufgabe | Ja | Ja | Ja | Kein Wert |
| Abhängigkeit der Projektaufgaben | Ja | Ja | | Abhängigkeitsdatensätze für Projektaufgaben werden nicht aktualisiert. Stattdessen kann ein alter Datensatz gelöscht und ein neuer Datensatz erstellt werden. |
| Ressourcenzuweisung | Ja | Ja | | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **BookableResourceID**, **Aufwand**, **EffortCompleted**, **EffortRemaining** und **PlannedWork**. Ressourcenzuweisungsdatensätze werden nicht aktualisiert. Stattdessen kann der alte Datensatz gelöscht und ein neuer Datensatz erstellt werden. |
| Projekt-Bucket | N/V | N/V | N/V | Der Standard-Bucket wird mit der **CreateProjectV1**-API erstellt. |
| Projektteammitglied | Ja | Ja | Ja | Verwenden Sie für den Erstellungsvorgang die **CreateTeamMemberV1**-API. |
| Project | Ja | Ja | N/V | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Aufwand**, **EffortCompleted**, **EffortRemaining**, **Fortschritt**, **Fertigstellen**, **TaskEarliestStart** und **Dauer**. |

Diese APIs können mit Entitätsobjekten aufgerufen werden, die benutzerdefinierte Felder enthalten.

Diese ID-Eigenschaft ist optional. Wenn sie bereitgestellt wird, versucht das System, sie zu verwenden, und löst eine Ausnahme aus, wenn sie nicht verwendet werden kann. Wenn sie nicht bereitgestellt wird, generiert das System sie.

## <a name="limitations-and-known-issues"></a>Einschränkungen und Bekannte Probleme
Das Folgende ist eine Liste von Einschränkungen und bekannten Problemen:

- Zeitplan-APIs können nur von **Benutzern mit Microsoft Project-Lizenz** verwendet werden. Sie können nicht verwendet werden von:
    - Anwendungsbenutzer
    - Systembenutzern
    - Integrationsbenutzern
    - Andere Benutzer, die nicht über die erforderliche Lizenz verfügen
- Jeder **OperationSet** kann nur maximal 100 Operationen haben.
- Jeder Benutzer kann nur maximal 10 offene **OperationSets** haben.
- Project Operations unterstützt derzeit maximal 500 Gesamtaufgaben für ein Projekt.
- **OperationSet**-Fehlerstatus und -Fehlerprotokolle sind derzeit nicht verfügbar.
- Zeitplan-APIs befinden sich in der öffentlichen Vorschau. Die Verwendung dieser APIs in einer Produktionsumgebung wird von Microsoft nicht unterstützt.

## <a name="sample-scenario"></a>Beispielszenario

In diesem Szenario erstellen Sie ein Projekt, ein Teammitglied, vier Aufgaben und zwei Ressourcenzuweisungen. Als Nächstes aktualisieren Sie eine Aufgabe, aktualisieren das Projekt, löschen eine Aufgabe, löschen eine Ressourcenzuweisung und erstellen eine Aufgabenabhängigkeit.

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

## <a name="additional-samples"></a>Zusätzliche Beispiele

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
