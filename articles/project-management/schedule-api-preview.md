---
title: Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung
description: Dieser Artikel enthält Informationen und Beispiele für die Verwendung von Project Schedule APIs.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541123"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


**Planungsentitäten**

Projektzeitplan-APIs bieten die Möglichkeit, Vorgänge zum Erstellen, Aktualisieren und Löschen mit **Terminplan-Entitäten** auszuführen. Diese Entitäten werden über das Planungsmodul in Project für das Web verwaltet. Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten** wurden in früheren Version von Dynamics 365 Project Operations eingeschränkt.

Die folgende Tabelle enthält eine vollständige Liste der Projektzeitplan-Entitäten.

| **Entitätsname**         | **Logischer Entitätsname**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektaufgabe            | msdyn_projecttask           |
| Abhängigkeit der Projektaufgaben | msdyn_projecttaskdependency |
| Ressourcenzuweisung     | msdyn_resourceassignment    |
| Projekt-Bucket          | msdyn_projectbucket         |
| Projektteammitglied     | msdyn_projectteam           |
| Projektprüflisten      | msdyn_projectchecklist      |
| Projektbeschriftung           | msdyn_projectlabel          |
| Zu beschriftende Projektaufgabe   | msdyn_projecttasktolabel    |
| Projektsprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet ist ein Arbeitseinheitsmuster, das verwendet werden kann, wenn innerhalb einer Transaktion mehrere zeitplanbezogene Anforderungen verarbeitet werden müssen.

**Projektzeitplan-APIs**

Im Folgenden finden Sie eine Liste der aktuellen Projektzeitplan-APIs.

| **API**                                 | Beschreibung des Dataflows                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Diese API wird verwendet, um ein Projekt zu erstellen. Das Projekt und der Standardprojekt-Bucket werden sofort erstellt.                         |
| **msdyn_CreateTeamMemberV1**            | Diese API wird verwendet, um ein Teammitglied zu erstellen. Der Teammitgliedsdatensatz wird sofort erstellt.                                  |
| **msdyn_CreateOperationSetV1**          | Mit dieser API können mehrere Anforderungen geplant werden, die innerhalb einer Transaktion ausgeführt werden müssen.                                        |
| **msdyn_PssCreateV1**                   | Diese API wird verwendet, um eine Entität zu erstellen. Die Entität kann eine der Projektplanungs-Entitäten sein, die den Vorgang des Erstellens unterstützen. |
| **msdyn_PssUpdateV1**                   | Diese API wird verwendet, um eine Entität zu aktualisieren. Die Entität kann eine von den Projektplanungsentitäten sein, die den Aktualisierungsvorgang unterstützen  |
| **msdyn_PssDeleteV1**                   | Diese API wird verwendet, um eine Entität zu löschen. Die Entität kann eine beliebige Projektplanungs-Entität sein, die den Vorgang „Löschen“ unterstützt. |
| **msdyn_ExecuteOperationSetV1**         | Diese API wird verwendet, um alle Operationen innerhalb des angegebenen Operationssatzes auszuführen.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Diese API wird verwendet, um eine geplante Arbeitskontur der Ressourcenzuweisung zu aktualisieren.                                                        |



**Verwenden von Projektzeitplan-APIs mit OperationSet**

Weil Aufzeichnungen sowohl mit **CreateProjectV1** als auch **CreateTeamMemberV1** sofort erstellt werden, können diese APIs nicht direkt im **OperationSet** verwendet werden. Sie können jedoch die API verwenden, um die erforderlichen Datensätze zu erstellen, ein **OperationSet** zu erstellen und dann diese vorab erstellten Datensätze im **OperationSet** zu verwenden.

**Unterstützte Vorgänge**

| **Planungsentität**   | **Erstellen** | **Update** | **Delete** | **Wichtige Überlegungen**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektaufgabe            | Ja        | Ja        | Ja        | Die Felder **Fortschritt**, **EffortCompleted** und **EffortRemaining** können in Project for the Web bearbeitet werden, aber sie können nicht in Project Operations bearbeitet werden.                                                                                                                                                                                             |
| Abhängigkeit der Projektaufgaben | Ja        | Nr.         | Ja        | Abhängigkeitsdatensätze für Projektaufgaben werden nicht aktualisiert. Stattdessen kann ein alter Datensatz gelöscht und ein neuer Datensatz erstellt werden.                                                                                                                                                                                                                                 |
| Ressourcenzuweisung     | Ja        | Ja\*      | Ja        | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **BookableResourceID**, **Aufwand**, **EffortCompleted**, **EffortRemaining** und **PlannedWork**. Ressourcenzuweisungsdatensätze werden nicht aktualisiert. Stattdessen kann der alte Datensatz gelöscht und ein neuer Datensatz erstellt werden. Eine separate API wurde bereitgestellt, um die Konturen der Ressourcenzuweisung zu aktualisieren. |
| Projekt-Bucket          | Ja        | Ja        | Ja        | Der Standard-Bucket wird mithilfe der **CreateProjectV1**-API erstellt. Unterstützung für das Erstellen und Löschen von Projekt-Buckets wurde in Update Release 16 hinzugefügt.                                                                                                                                                                                                   |
| Projektteammitglied     | Ja        | Ja        | Ja        | Verwenden Sie für den Erstellungsvorgang die **CreateTeamMemberV1**-API.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Aufwand**, **EffortCompleted**, **EffortRemaining**, **Fortschritt**, **Fertigstellen**, **TaskEarliestStart** und **Dauer**.                                                                                       |
| Projektprüflisten      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Projektbeschriftung           | Nr.         | Ja        | Nr.         | Etikettennamen können geändert werden. Diese Funktion ist nur für Project for the Web verfügbar.                                                                                                                                                                                                                                                                      |
| Zu beschriftende Projektaufgabe   | Ja        | Nr.         | Ja        | Diese Funktion ist nur für Project for the Web verfügbar.                                                                                                                                                                                                                                                                                                  |
| Projektsprint          | Ja        | Ja        | Ja        | Das **Start**-Feld muss ein Datum vor dem **Fertig**-Feld haben. Sprints für dasselbe Projekt dürfen sich nicht überschneiden. Diese Funktion ist nur für Project for the Web verfügbar.                                                                                                                                                                    |




Diese ID-Eigenschaft ist optional. Wenn sie bereitgestellt wird, versucht das System, sie zu verwenden, und löst eine Ausnahme aus, wenn sie nicht verwendet werden kann. Wenn sie nicht bereitgestellt wird, generiert das System sie.

**Einschränkungen und bekannte Probleme**

Das Folgende ist eine Liste von Einschränkungen und bekannten Problemen:

-   Project Schedule APIs können nur von **Benutzern mit Microsoft Project-Lizenz verwendet werden**. Sie können nicht verwendet werden von:
    -   Anwendungsbenutzer
    -   Systembenutzern
    -   Integrationsbenutzern
    -   Andere Benutzer, die nicht über die erforderliche Lizenz verfügen
-   Jeder **OperationSet** kann nur maximal 100 Operationen haben.
-   Jeder Benutzer kann nur maximal 10 offene **OperationSets** haben.
-   Project Operations unterstützt derzeit maximal 500 Gesamtaufgaben für ein Projekt.
-   Jeder Vorgang zum Aktualisieren der Ressourcenzuweisungskontur zählt als ein einzelner Vorgang.
-   Jede Liste aktualisierter Konturen kann maximal 100 Zeitscheiben enthalten.
-   **OperationSet**-Fehlerstatus und -Fehlerprotokolle sind derzeit nicht verfügbar.
-   Es gibt maximal 400 Sprints pro Projekt.
-   [Grenzwerte und Beschränkungen von Projekten und Aufgaben](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Beschriftungen sind derzeit nur für Project for the Web verfügbar.

**Fehlerbehandlung**

-   Um die aus den Operations-Sätzen generierten Fehler zu überprüfen, gehen Sie zu **Einstellungen** \> **Integration planen** \> **Operationssätze**.
-   Um vom Project Schedule Service generierte Fehler zu überprüfen, gehen Sie auf **Einstellungen** \> **Planungsintegration** \> **PSS Fehlerprotokolle**.

**Bearbeiten der Konturen der Ressourcenzuweisung**

Im Gegensatz zu allen anderen Projektplanungs-APIs, die eine Entität aktualisieren, ist die Ressourcenzuweisungskontur-API ausschließlich für Aktualisierungen eines einzelnen Felds, msdyn_plannedwork, auf einer einzelnen Entität, msydn_resourceassignment, verantwortlich.

Der gegebene Zeitplanmodus ist:

-   **Feste Einheiten**
-   Projektkalender: 9-17 Uhr, Mo, Di, Do, Freitag (MITTWOCH KEINE ARBEIT)
-   Und Ressourcenkalender ist 9-13:00 Uhr PST Mo bis Fr

Diese Aufgabe dauert eine Woche, vier Stunden pro Tag. Dies liegt daran, dass der Ressourcenkalender von 9-13:00 Uhr PST oder vier Stunden pro Tag ist.

| &nbsp;     | Task | Startdatum | Enddatum  | Menge | 13.6.2022 | 14.6.2022 | 15.6.2022 | 16.6.2022 | 17.6.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 Arbeitskraft |  T1  | 13.6.2022  | 17.6.2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Wenn Sie beispielsweise möchten, dass die Arbeitskraft diese Woche nur drei Stunden pro Tag arbeitet und eine Stunde für andere Aufgaben einplanen soll.

#### <a name="updatedcontours-sample-payload"></a>Wählen Sie die UpdatedContours-Beispiel-Nutzlast aus.

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Dies ist die Zuweisung, nachdem die Update Contour Schedule API ausgeführt wurde.

| &nbsp;     | Task | Startdatum | Enddatum  | Menge | 13.6.2022 | 14.6.2022 | 15.6.2022 | 16.6.2022 | 17.6.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 Arbeitskraft | T1   | 13.6.2022  | 17.6.2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Beispielszenario**

In diesem Szenario erstellen Sie ein Projekt, ein Teammitglied, vier Aufgaben und zwei Ressourcenzuweisungen. Als Nächstes aktualisieren Sie eine Aufgabe, aktualisieren das Projekt, löschen eine Aufgabe, löschen eine Ressourcenzuweisung und erstellen eine Aufgabenabhängigkeit.

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

** Zusätzliche Beispiele

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
