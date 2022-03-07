---
title: Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen
description: Dieses Thema enthält Informationen und Beispiele für die Verwendung von Zeitplan-APIs.
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
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950803"
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

## <a name="restricted-fields"></a>Eingeschränkte Felder

In den folgenden Tabellen werden die Felder definiert, für die **Erstellen** und **Bearbeiten** eingeschränkt ist.

### <a name="project-task"></a>Projektaufgabe

| **Logischer Name**                       | **Kann erstellen** | **Kann bearbeiten**:     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | Nein             | Nein               |
| msdyn_actualcost_base                  | Nein             | Nein               |
| msdyn_actualend                        | Nein             | Nein               |
| msdyn_actualsales                      | Nein             | Nein               |
| msdyn_actualsales_base                 | Nein             | Nein               |
| msdyn_actualstart                      | Nein             | Nein               |
| msdyn_costatcompleteestimate           | Nein             | Nein               |
| msdyn_costatcompleteestimate_base      | Nein             | Nein               |
| msdyn_costconsumptionpercentage        | Nein             | Nein               |
| msdyn_effortcompleted                  | Nein             | Nein               |
| msdyn_effortestimateatcomplete         | Nein             | Nein               |
| msdyn_iscritical                       | Nein             | Nein               |
| msdyn_iscriticalname                   | Nein             | Nein               |
| msdyn_ismanual                         | Nein             | Nein               |
| msdyn_ismanualname                     | Nein             | Nein               |
| msdyn_ismilestone                      | Nein             | Nein               |
| msdyn_ismilestonename                  | Nein             | Nein               |
| msdyn_LinkStatus                       | Nein             | Nein               |
| msdyn_linkstatusname                   | Nein             | Nein               |
| msdyn_msprojectclientid                | Nein             | Nein               |
| msdyn_plannedcost                      | Nein             | Nein               |
| msdyn_plannedcost_base                 | Nein             | Nein               |
| msdyn_plannedsales                     | Nein             | Nein               |
| msdyn_plannedsales_base                | Nein             | Nein               |
| msdyn_pluginprocessingdata             | Nein             | Nein               |
| msdyn_progress                         | Nein             | nein (ja für P4W) |
| msdyn_remainingcost                    | Nein             | Nein               |
| msdyn_remainingcost_base               | Nein             | Nein               |
| msdyn_remainingsales                   | Nein             | Nein               |
| msdyn_remainingsales_base              | Nein             | Nein               |
| msdyn_requestedhours                   | Nein             | Nein               |
| msdyn_resourcecategory                 | Nein             | Nein               |
| msdyn_resourcecategoryname             | Nein             | Nein               |
| msdyn_resourceorganizationalunitid     | Nein             | Nein               |
| msdyn_resourceorganizationalunitidname | Nein             | Nein               |
| msdyn_salesconsumptionpercentage       | Nein             | Nein               |
| msdyn_salesestimateatcomplete          | Nein             | Nein               |
| msdyn_salesestimateatcomplete_base     | Nein             | Nein               |
| msdyn_salesvariance                    | Nein             | Nein               |
| msdyn_salesvariance_base               | Nein             | Nein               |
| msdyn_scheduleddurationminutes         | Nein             | Nein               |
| msdyn_scheduledend                     | Nein             | Nein               |
| msdyn_scheduledstart                   | Nein             | Nein               |
| msdyn_schedulevariance                 | Nein             | Nein               |
| msdyn_skipupdateestimateline           | Nein             | Nein               |
| msdyn_skipupdateestimatelinename       | Nein             | Nein               |
| msdyn_summary                          | Nein             | Nein               |
| msdyn_varianceofcost                   | Nein             | Nein               |
| msdyn_varianceofcost_base              | Nein             | Nein               |

### <a name="project-task-dependency"></a>Abhängigkeit der Projektaufgaben

| **Logischer Name**              | **Kann erstellen** | **Kann bearbeiten**: |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | Nein             | Nein           |
| msdyn_linktypename            | Nein             | Nein           |
| msdyn_predecessortask         | Ja            | Nein           |
| msdyn_predecessortaskname     | Ja            | Nein           |
| msdyn_project                 | Ja            | Nein           |
| msdyn_projectname             | Ja            | Nein           |
| msdyn_projecttaskdependencyid | Ja            | Nein           |
| msdyn_successortask           | Ja            | Nein           |
| msdyn_successortaskname       | Ja            | Nein           |

### <a name="resource-assignment"></a>Ressourcenzuweisung

| **Logischer Name**             | **Kann erstellen** | **Kann bearbeiten**: |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Ja            | Nein           |
| msdyn_bookableresourceidname | Ja            | Nein           |
| msdyn_bookingstatusid        | Nein             | Nein           |
| msdyn_bookingstatusidname    | Nein             | Nein           |
| msdyn_committype             | Nein             | Nein           |
| msdyn_committypename         | Nein             | Nein           |
| msdyn_effort                 | Nein             | Nein           |
| msdyn_effortcompleted        | Nein             | Nein           |
| msdyn_effortremaining        | Nein             | Nein           |
| msdyn_finish                 | Nein             | Nein           |
| msdyn_plannedcost            | Nein             | Nein           |
| msdyn_plannedcost_base       | Nein             | Nein           |
| msdyn_plannedcostcontour     | Nein             | Nein           |
| msdyn_plannedsales           | Nein             | Nein           |
| msdyn_plannedsales_base      | Nein             | Nein           |
| msdyn_plannedsalescontour    | Nein             | Nein           |
| msdyn_plannedwork            | Nein             | Nein           |
| msdyn_projectid              | Ja            | Nein           |
| msdyn_projectidname          | Nein             | Nein           |
| msdyn_projectteamid          | Nein             | Nein           |
| msdyn_projectteamidname      | Nein             | Nein           |
| msdyn_start                  | Nein             | Nein           |
| msdyn_taskid                 | Nein             | Nein           |
| msdyn_taskidname             | Nein             | Nein           |
| msdyn_userresourceid         | Nein             | Nein           |

### <a name="project-team-member"></a>Projektteammitglied

| **Logischer Name**                                 | **Kann erstellen** | **Kann bearbeiten**: |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | Nein             | Nein           |
| msdyn_creategenericteammemberwithrequirementname | Nein             | Nein           |
| msdyn_deletestatus                               | Nein             | Nein           |
| msdyn_deletestatusname                           | Nein             | Nein           |
| msdyn_effort                                     | Nein             | Nein           |
| msdyn_effortcompleted                            | Nein             | Nein           |
| msdyn_effortremaining                            | Nein             | Nein           |
| msdyn_finish                                     | Nein             | Nein           |
| msdyn_hardbookedhours                            | Nein             | Nein           |
| msdyn_hours                                      | Nein             | Nein           |
| msdyn_markedfordeletiontimer                     | Nein             | Nein           |
| msdyn_markedfordeletiontimestamp                 | Nein             | Nein           |
| msdyn_msprojectclientid                          | Nein             | Nein           |
| msdyn_percentage                                 | Nein             | Nein           |
| msdyn_requiredhours                              | Nein             | Nein           |
| msdyn_softbookedhours                            | Nein             | Nein           |
| msdyn_start                                      | Nein             | Nein           |

### <a name="project"></a>Project

| **Logischer Name**                       | **Kann erstellen** | **Kann bearbeiten**: |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | Nein             | Nein           |
| msdyn_actualexpensecost_base           | Nein             | Nein           |
| msdyn_actuallaborcost                  | Nein             | Nein           |
| msdyn_actuallaborcost_base             | Nein             | Nein           |
| msdyn_actualsales                      | Nein             | Nein           |
| msdyn_actualsales_base                 | Nein             | Nein           |
| msdyn_contractlineproject              | Ja            | Nein           |
| msdyn_contractorganizationalunitid     | Ja            | Nein           |
| msdyn_contractorganizationalunitidname | Ja            | Nein           |
| msdyn_costconsumption                  | Nein             | Nein           |
| msdyn_costestimateatcomplete           | Nein             | Nein           |
| msdyn_costestimateatcomplete_base      | Nein             | Nein           |
| msdyn_costvariance                     | Nein             | Nein           |
| msdyn_costvariance_base                | Nein             | Nein           |
| msdyn_duration                         | Nein             | Nein           |
| msdyn_effort                           | Nein             | Nein           |
| msdyn_effortcompleted                  | Nein             | Nein           |
| msdyn_effortestimateatcompleteeac      | Nein             | Nein           |
| msdyn_effortremaining                  | Nein             | Nein           |
| msdyn_finish                           | Ja            | Ja          |
| msdyn_globalrevisiontoken              | Nein             | Nein           |
| msdyn_islinkedtomsprojectclient        | Nein             | Nein           |
| msdyn_islinkedtomsprojectclientname    | Nein             | Nein           |
| msdyn_linkeddocumenturl                | Nein             | Nein           |
| msdyn_msprojectdocument                | Nein             | Nein           |
| msdyn_msprojectdocumentname            | Nein             | Nein           |
| msdyn_plannedexpensecost               | Nein             | Nein           |
| msdyn_plannedexpensecost_base          | Nein             | Nein           |
| msdyn_plannedlaborcost                 | Nein             | Nein           |
| msdyn_plannedlaborcost_base            | Nein             | Nein           |
| msdyn_plannedsales                     | Nein             | Nein           |
| msdyn_plannedsales_base                | Nein             | Nein           |
| msdyn_progress                         | Nein             | Nein           |
| msdyn_remainingcost                    | Nein             | Nein           |
| msdyn_remainingcost_base               | Nein             | Nein           |
| msdyn_remainingsales                   | Nein             | Nein           |
| msdyn_remainingsales_base              | Nein             | Nein           |
| msdyn_replaylogheader                  | Nein             | Nein           |
| msdyn_salesconsumption                 | Nein             | Nein           |
| msdyn_salesestimateatcompleteeac       | Nein             | Nein           |
| msdyn_salesestimateatcompleteeac_base  | Nein             | Nein           |
| msdyn_salesvariance                    | Nein             | Nein           |
| msdyn_salesvariance_base               | Nein             | Nein           |
| msdyn_scheduleperformance              | Nein             | Nein           |
| msdyn_scheduleperformancename          | Nein             | Nein           |
| msdyn_schedulevariance                 | Nein             | Nein           |
| msdyn_taskearlieststart                | Nein             | Nein           |
| msdyn_teamsize                         | Nein             | Nein           |
| msdyn_teamsize_date                    | Nein             | Nein           |
| msdyn_teamsize_state                   | Nein             | Nein           |
| msdyn_totalactualcost                  | Nein             | Nein           |
| msdyn_totalactualcost_base             | Nein             | Nein           |
| msdyn_totalplannedcost                 | Nein             | Nein           |
| msdyn_totalplannedcost_base            | Nein             | Nein           |


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
- [Grenzwerte und Beschränkungen von Projekten und Aufgaben](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Fehlerbehandlung

   - Um die aus den Operations-Sätzen generierten Fehler zu überprüfen, gehen Sie zu **Einstellungen** \> **Integration planen** \> **Operationssätze**.
   - Um die vom Project Scheduling Service generierten Fehler zu überprüfen, gehen Sie **Einstellungen** \> **Planen Sie die Integration** \> **PSS-Fehlerprotokolle**.

## <a name="sample-scenario"></a>Beispielszenario

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

## <a name="additional-samples"></a>Zusätzliche Beispiele

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
