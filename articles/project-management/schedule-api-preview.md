---
title: Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung
description: Dieser Artikel enthält Informationen und Beispiele für die Verwendung von Project Schedule APIs.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ada06186121d41edddaa06f747b3e1687c303928
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929213"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_



## <a name="scheduling-entities"></a>Planungsentitäten

Projektzeitplan-APIs bieten die Möglichkeit, Vorgänge zum Erstellen, Aktualisieren und Löschen mit **Terminplan-Entitäten** auszuführen. Diese Entitäten werden über das Planungsmodul in Project für das Web verwaltet. Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten** wurden in früheren Version von Dynamics 365 Project Operations eingeschränkt.

Die folgende Tabelle enthält eine vollständige Liste der Projektzeitplan-Entitäten.

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

## <a name="project-schedule-apis"></a>Projektzeitplan-APIs

Im Folgenden finden Sie eine Liste der aktuellen Projektzeitplan-APIs.

- **msdyn_CreateProjectV1**: Mit dieser API kann ein Projekt erstellt werden. Das Projekt und der Standardprojekt-Bucket werden sofort erstellt.
- **msdyn_CreateTeamMemberV1**: Mit dieser API kann ein Projektteammitglied erstellt werden. Der Teammitgliedsdatensatz wird sofort erstellt.
- **msdyn_CreateOperationSetV1**: Mit dieser API können mehrere Anforderungen geplant werden, die innerhalb einer Transaktion ausgeführt werden müssen.
- **msdyn_PSSCreateV1**: Mit dieser API kann eine Entität erstellt werden. Die Entität kann eine der Projektplanungs-Entitäten sein, die den Vorgang des Erstellens unterstützen.
- **msdyn_PSSUpdateV1**: Mit dieser API kann eine Entität aktualisiert werden. Die Entität kann eine beliebige Projektplanungs-Entität sein, die den Vorgang „Aktualisieren“ unterstützt.
- **msdyn_PSSDeleteV1**: Mit dieser API kann eine Entität gelöscht werden. Die Entität kann eine beliebige Projektplanungs-Entität sein, die den Vorgang „Löschen“ unterstützt.
- **msdyn_ExecuteOperationSetV1**: Diese API wird verwendet, um alle Operationen innerhalb des angegebenen Operationssatzes auszuführen.

## <a name="using-project-schedule-apis-with-operationset"></a>Verwenden von Projektzeitplan-APIs mit OperationSet

Weil Aufzeichnungen sowohl mit **CreateProjectV1** als auch **CreateTeamMemberV1** sofort erstellt werden, können diese APIs nicht direkt im **OperationSet** verwendet werden. Sie können jedoch die API verwenden, um die erforderlichen Datensätze zu erstellen, ein **OperationSet** zu erstellen und dann diese vorab erstellten Datensätze im **OperationSet** zu verwenden.

## <a name="supported-operations"></a>Unterstützte Vorgänge

| Planungsentität | Erstellen | Aktualisieren | Delete | Wichtige Überlegungen |
| --- | --- | --- | --- | --- |
Projektaufgabe | Ja | Ja | Ja | Die Felder **Fortschritt**, **EffortCompleted** und **EffortRemaining** können in Project for the Web bearbeitet werden, aber sie können nicht in Project Operations bearbeitet werden.  |
| Abhängigkeit der Projektaufgaben | Ja |  | Ja | Abhängigkeitsdatensätze für Projektaufgaben werden nicht aktualisiert. Stattdessen kann ein alter Datensatz gelöscht und ein neuer Datensatz erstellt werden. |
| Ressourcenzuweisung | Ja | Ja | | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **BookableResourceID**, **Aufwand**, **EffortCompleted**, **EffortRemaining** und **PlannedWork**. Ressourcenzuweisungsdatensätze werden nicht aktualisiert. Stattdessen kann der alte Datensatz gelöscht und ein neuer Datensatz erstellt werden. |
| Projekt-Bucket | Ja | Ja | Ja | Der Standard-Bucket wird mithilfe der **CreateProjectV1**-API erstellt. Unterstützung für das Erstellen und Löschen von Projekt-Buckets wurde in Update Release 16 hinzugefügt. |
| Projektteammitglied | Ja | Ja | Ja | Verwenden Sie für den Erstellungsvorgang die **CreateTeamMemberV1**-API. |
| Project | Ja | Ja |  | Vorgänge mit den folgenden Feldern werden nicht unterstützt: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Aufwand**, **EffortCompleted**, **EffortRemaining**, **Fortschritt**, **Fertigstellen**, **TaskEarliestStart** und **Dauer**. |

Diese APIs können mit Entitätsobjekten aufgerufen werden, die benutzerdefinierte Felder enthalten.

Diese ID-Eigenschaft ist optional. Wenn sie bereitgestellt wird, versucht das System, sie zu verwenden, und löst eine Ausnahme aus, wenn sie nicht verwendet werden kann. Wenn sie nicht bereitgestellt wird, generiert das System sie.

## <a name="restricted-fields"></a>Eingeschränkte Felder

In den folgenden Tabellen werden die Felder definiert, für die **Erstellen** und **Bearbeiten** eingeschränkt ist.

### <a name="project-task"></a>Projektaufgabe

| Logischer Name                           | Kan erstellen     | Kann bearbeiten:         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | Nr.             | Nr.               |
| msdyn_actualcost_base                  | Nr.             | Nr.               |
| msdyn_actualend                        | Nr.             | Nr.               |
| msdyn_actualsales                      | Nr.             | Nr.               |
| msdyn_actualsales_base                 | Nr.             | Nr.               |
| msdyn_actualstart                      | Nr.             | Nr.               |
| msdyn_costatcompleteestimate           | Nr.             | Nr.               |
| msdyn_costatcompleteestimate_base      | Nr.             | Nr.               |
| msdyn_costconsumptionpercentage        | Nr.             | Nr.               |
| msdyn_effortcompleted                  | Nein (Ja für Projekt)             | Nein (Ja für Projekt)               |
| msdyn_effortremaining                  | Nein (Ja für Projekt)              | Nein (Ja für Projekt)                |
| msdyn_effortestimateatcomplete         | Nr.             | Nr.               |
| msdyn_iscritical                       | Nr.             | Nr.               |
| msdyn_iscriticalname                   | Nr.             | Nr.               |
| msdyn_ismanual                         | Nr.             | Nr.               |
| msdyn_ismanualname                     | Nr.             | Nr.               |
| msdyn_ismilestone                      | Nr.             | Nr.               |
| msdyn_ismilestonename                  | Nr.             | Nr.               |
| msdyn_LinkStatus                       | Nr.             | Nr.               |
| msdyn_linkstatusname                   | Nr.             | Nr.               |
| msdyn_msprojectclientid                | Nr.             | Nr.               |
| msdyn_plannedcost                      | Nr.             | Nr.               |
| msdyn_plannedcost_base                 | Nr.             | Nr.               |
| msdyn_plannedsales                     | Nr.             | Nr.               |
| msdyn_plannedsales_base                | Nr.             | Nr.               |
| msdyn_pluginprocessingdata             | Nr.             | Nr.               |
| msdyn_progress                         | Nein (Ja für Projekt)             | Nein (Ja für Projekt) |
| msdyn_remainingcost                    | Nr.             | Nr.               |
| msdyn_remainingcost_base               | Nr.             | Nr.               |
| msdyn_remainingsales                   | Nr.             | Nr.               |
| msdyn_remainingsales_base              | Nr.             | Nr.               |
| msdyn_requestedhours                   | Nr.             | Nr.               |
| msdyn_resourcecategory                 | Nr.             | Nr.               |
| msdyn_resourcecategoryname             | Nr.             | Nr.               |
| msdyn_resourceorganizationalunitid     | Nr.             | Nr.               |
| msdyn_resourceorganizationalunitidname | Nr.             | Nr.               |
| msdyn_salesconsumptionpercentage       | Nr.             | Nr.               |
| msdyn_salesestimateatcomplete          | Nr.             | Nr.               |
| msdyn_salesestimateatcomplete_base     | Nr.             | Nr.               |
| msdyn_salesvariance                    | Nr.             | Nr.               |
| msdyn_salesvariance_base               | Nr.             | Nr.               |
| msdyn_scheduleddurationminutes         | Nr.             | Nr.               |
| msdyn_scheduledend                     | Nr.             | Nr.               |
| msdyn_scheduledstart                   | Nr.             | Nr.               |
| msdyn_schedulevariance                 | Nr.             | Nr.               |
| msdyn_skipupdateestimateline           | Nr.             | Nr.               |
| msdyn_skipupdateestimatelinename       | Nr.             | Nr.               |
| msdyn_summary                          | Nr.             | Nr.               |
| msdyn_varianceofcost                   | Nr.             | Nr.               |
| msdyn_varianceofcost_base              | Nr.             | Nr.               |

### <a name="project-task-dependency"></a>Abhängigkeit der Projektaufgaben

| Logischer Name                  | Kan erstellen     | Kann bearbeiten:     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | Nr.             | Nr.           |
| msdyn_linktypename            | Nr.             | Nr.           |
| msdyn_predecessortask         | Ja            | Nr.           |
| msdyn_predecessortaskname     | Ja            | Nr.           |
| msdyn_project                 | Ja            | Nr.           |
| msdyn_projectname             | Ja            | Nr.           |
| msdyn_projecttaskdependencyid | Ja            | Nr.           |
| msdyn_successortask           | Ja            | Nr.           |
| msdyn_successortaskname       | Ja            | Nr.           |

### <a name="resource-assignment"></a>Ressourcenzuweisung

| Logischer Name                 | Kan erstellen     | Kann bearbeiten:     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Ja            | Nr.           |
| msdyn_bookableresourceidname | Ja            | Nr.           |
| msdyn_bookingstatusid        | Nr.             | Nr.           |
| msdyn_bookingstatusidname    | Nr.             | Nr.           |
| msdyn_committype             | Nr.             | Nr.           |
| msdyn_committypename         | Nr.             | Nr.           |
| msdyn_effort                 | Nr.             | Nr.           |
| msdyn_effortcompleted        | Nr.             | Nr.           |
| msdyn_effortremaining        | Nr.             | Nr.           |
| msdyn_finish                 | Nr.             | Nr.           |
| msdyn_plannedcost            | Nr.             | Nr.           |
| msdyn_plannedcost_base       | Nr.             | Nr.           |
| msdyn_plannedcostcontour     | Nr.             | Nr.           |
| msdyn_plannedsales           | Nr.             | Nr.           |
| msdyn_plannedsales_base      | Nr.             | Nr.           |
| msdyn_plannedsalescontour    | Nr.             | Nr.           |
| msdyn_plannedwork            | Nr.             | Nr.           |
| msdyn_projectid              | Ja            | Nr.           |
| msdyn_projectidname          | Nr.             | Nr.           |
| msdyn_projectteamid          | Nr.             | Nr.           |
| msdyn_projectteamidname      | Nr.             | Nr.           |
| msdyn_start                  | Nr.             | Nr.           |
| msdyn_taskid                 | Nr.             | Nr.           |
| msdyn_taskidname             | Nr.             | Nr.           |
| msdyn_userresourceid         | Nr.             | Nr.           |

### <a name="project-team-member"></a>Projektteammitglied

| Logischer Name                                     | Kan erstellen     | Kann bearbeiten:     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | Nr.             | Nr.           |
| msdyn_creategenericteammemberwithrequirementname | Nr.             | Nr.           |
| msdyn_deletestatus                               | Nr.             | Nr.           |
| msdyn_deletestatusname                           | Nr.             | Nr.           |
| msdyn_effort                                     | Nr.             | Nr.           |
| msdyn_effortcompleted                            | Nr.             | Nr.           |
| msdyn_effortremaining                            | Nr.             | Nr.           |
| msdyn_finish                                     | Nr.             | Nr.           |
| msdyn_hardbookedhours                            | Nr.             | Nr.           |
| msdyn_hours                                      | Nr.             | Nr.           |
| msdyn_markedfordeletiontimer                     | Nr.             | Nr.           |
| msdyn_markedfordeletiontimestamp                 | Nr.             | Nr.           |
| msdyn_msprojectclientid                          | Nr.             | Nr.           |
| msdyn_percentage                                 | Nr.             | Nr.           |
| msdyn_requiredhours                              | Nr.             | Nr.           |
| msdyn_softbookedhours                            | Nr.             | Nr.           |
| msdyn_start                                      | Nr.             | Nr.           |

### <a name="project"></a>Project

| Logischer Name                           | Kan erstellen     | Kann bearbeiten:     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | Nr.             | Nr.           |
| msdyn_actualexpensecost_base           | Nr.             | Nr.           |
| msdyn_actuallaborcost                  | Nr.             | Nr.           |
| msdyn_actuallaborcost_base             | Nr.             | Nr.           |
| msdyn_actualsales                      | Nr.             | Nr.           |
| msdyn_actualsales_base                 | Nr.             | Nr.           |
| msdyn_contractlineproject              | Ja            | Nr.           |
| msdyn_contractorganizationalunitid     | Ja            | Nr.           |
| msdyn_contractorganizationalunitidname | Ja            | Nr.           |
| msdyn_costconsumption                  | Nr.             | Nr.           |
| msdyn_costestimateatcomplete           | Nr.             | Nr.           |
| msdyn_costestimateatcomplete_base      | Nr.             | Nr.           |
| msdyn_costvariance                     | Nr.             | Nr.           |
| msdyn_costvariance_base                | Nr.             | Nr.           |
| msdyn_duration                         | Nr.             | Nr.           |
| msdyn_effort                           | Nr.             | Nr.           |
| msdyn_effortcompleted                  | Nr.             | Nr.           |
| msdyn_effortestimateatcompleteeac      | Nr.             | Nr.           |
| msdyn_effortremaining                  | Nr.             | Nr.           |
| msdyn_finish                           | Ja            | Ja          |
| msdyn_globalrevisiontoken              | Nr.             | Nr.           |
| msdyn_islinkedtomsprojectclient        | Nr.             | Nr.           |
| msdyn_islinkedtomsprojectclientname    | Nr.             | Nr.           |
| msdyn_linkeddocumenturl                | Nr.             | Nr.           |
| msdyn_msprojectdocument                | Nr.             | Nr.           |
| msdyn_msprojectdocumentname            | Nr.             | Nr.           |
| msdyn_plannedexpensecost               | Nr.             | Nr.           |
| msdyn_plannedexpensecost_base          | Nr.             | Nr.           |
| msdyn_plannedlaborcost                 | Nr.             | Nr.           |
| msdyn_plannedlaborcost_base            | Nr.             | Nr.           |
| msdyn_plannedsales                     | Nr.             | Nr.           |
| msdyn_plannedsales_base                | Nr.             | Nr.           |
| msdyn_progress                         | Nr.             | Nr.           |
| msdyn_remainingcost                    | Nr.             | Nr.           |
| msdyn_remainingcost_base               | Nr.             | Nr.           |
| msdyn_remainingsales                   | Nr.             | Nr.           |
| msdyn_remainingsales_base              | Nr.             | Nr.           |
| msdyn_replaylogheader                  | Nr.             | Nr.           |
| msdyn_salesconsumption                 | Nr.             | Nr.           |
| msdyn_salesestimateatcompleteeac       | Nr.             | Nr.           |
| msdyn_salesestimateatcompleteeac_base  | Nr.             | Nr.           |
| msdyn_salesvariance                    | Nr.             | Nr.           |
| msdyn_salesvariance_base               | Nr.             | Nr.           |
| msdyn_scheduleperformance              | Nr.             | Nr.           |
| msdyn_scheduleperformancename          | Nr.             | Nr.           |
| msdyn_schedulevariance                 | Nr.             | Nr.           |
| msdyn_taskearlieststart                | Nr.             | Nr.           |
| msdyn_teamsize                         | Nr.             | Nr.           |
| msdyn_teamsize_date                    | Nr.             | Nr.           |
| msdyn_teamsize_state                   | Nr.             | Nr.           |
| msdyn_totalactualcost                  | Nr.             | Nr.           |
| msdyn_totalactualcost_base             | Nr.             | Nr.           |
| msdyn_totalplannedcost                 | Nr.             | Nr.           |
| msdyn_totalplannedcost_base            | Nr.             | Nr.           |

### <a name="project-bucket"></a>Projekt-Bucket

| Logischer Name          | Kan erstellen      | Kann bearbeiten:     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Ja             | Nr.           |
| msdyn_name            | Ja             | Ja          |
| msdyn_project         | Ja             | Nr.           |
| msdyn_projectbucketid | Ja             | Nr.           |

## <a name="limitations-and-known-issues"></a>Einschränkungen und bekannte Probleme
Das Folgende ist eine Liste von Einschränkungen und bekannten Problemen:

- Project Schedule APIs können nur von **Benutzern mit Microsoft Project-Lizenz verwendet werden**. Sie können nicht verwendet werden von:

    - Anwendungsbenutzer
    - Systembenutzern
    - Integrationsbenutzern
    - Andere Benutzer, die nicht über die erforderliche Lizenz verfügen

- Jeder **OperationSet** kann nur maximal 100 Operationen haben.
- Jeder Benutzer kann nur maximal 10 offene **OperationSets** haben.
- Project Operations unterstützt derzeit maximal 500 Gesamtaufgaben für ein Projekt.
- **OperationSet**-Fehlerstatus und -Fehlerprotokolle sind derzeit nicht verfügbar.
- [Grenzwerte und Beschränkungen von Projekten und Aufgaben](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Fehlerbehandlung

- Um die aus den Operations-Sätzen generierten Fehler zu überprüfen, gehen Sie zu **Einstellungen** \> **Integration planen** \> **Operationssätze**.
- Um vom Project Schedule Service generierte Fehler zu überprüfen, gehen Sie auf **Einstellungen** \> **Planungsintegration** \> **PSS Fehlerprotokolle**.

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
