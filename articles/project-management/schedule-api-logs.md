---
title: Projektzeitplanungsprotokolle
description: Dieser Artikel enthält Informationen und Beispiele, die Ihnen helfen, die Projektplanungsprotokolle zu verwenden, um Fehler zu verfolgen, die mit dem Projektplanungsdienst und den Projektplanungs-APIs zusammenhängen.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923694"
---
# <a name="project-scheduling-logs"></a>Projektzeitplanungsprotokolle

_**Gilt für:** Die Basisbereitstellung ist für die Szenarien Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen und Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung verfügbar_, _Project for the web_

Microsoft Dynamics 365 Project Operations verwendet [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) als primäres Planungsmodul. Anstatt die standardmäßige Microsoft Dataverse-Webanwendungs-Programmierschnittstellen (APIs) zu nutzen, verwendet Project Operations die neuen Projektplanungs-APIs, um Projektaufgaben, Ressourcenzuweisungen, Aufgabenabhängigkeiten, Projekt-Buckets und Projektteammitglieder zu erstellen, zu aktualisieren und zu löschen. Wenn jedoch Erstellungs-, Aktualisierungs- oder Löschvorgänge programmgesteuert für Projektstrukturplan(PSP)-Entitäten ausgeführt werden, können Fehler auftreten. Um diese Fehler und den Verlauf der Vorgänge nachzuverfolgen, wurden zwei neue Verwaltungsprotokolle implementiert: **Vorgangssatz** und **Projektplanungsdienst (PSS)**. Um auf diese Protokolle zuzugreifen, gehen Sie zu **Einstellungen** \> **Zeitplanintegration**.

Die folgende Abbildung zeigt das Datenmodell für die Projektzeitplanungsprotokolle.

![Datenmodell für die Projektzeitplanungsprotokolle.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Vorgangssatzprotokoll

Das Vorgangssatzprotokoll verfolgt die Ausführung eines Vorgangssatzes, der verwendet wird, um einen oder mehrere Erstellungs-, Aktualisierungs- oder Löschvorgänge in einem Batch für Projekte, Projektaufgaben, Ressourcenzuweisungen, Aufgabenabhängigkeiten, Projekt-Buckets oder Projektteammitglieder auszuführen. Das Feld **Vorgang im Status** zeigt den Gesamtstatus des Vorgangssatzes an. Die Details der Vorgangssatz-Nutzdaten werden in den zugehörigen Vorgangssatz-Detaildatensätzen erfasst.

### <a name="operation-set"></a>Vorgangssatz

In der folgenden Tabelle werden die Felder angezeigt, die zu der Entität **Vorgangssatz** gehören.

| Schemaname            | Beschreibung des Dataflows                                                                                                  | Anzeigename            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Das Datum bzw. die Uhrzeit, zu dem bzw. zu der der Vorgang abgeschlossen oder fehlgeschlagen ist.                                                | CompletedOn            |
| msdyn_correlationid   | Der **correlationId**-Wert der Anforderung.                                                                  | CorrelationId          |
| msdyn_description     | Die Beschreibung des Vorgangssatzes.                                                                        | Beschreibung des Dataflows            |
| msdyn_executedon      | Das Datum und die Uhrzeit der Datensatzausführung.                                                                       | Ausgeführt am            |
| msdyn_operationsetId  | Der eindeutige Bezeichner der Entitätsinstanzen.                                                                   | OperationSet           |
| msdyn_Project         | Das mit dem Vorgangssatz verknüpfte Projekt.                                                            | Project                |
| msdyn_projectid       | Der **projectId**-Wert der Anforderung.                                                                      | ProjectId (veraltet) |
| msdyn_projectName     | Nicht verfügbar.                                                                                              | Nicht verfügbar         |
| msdyn_PSSErrorLog     | Der eindeutige Bezeichner des Projektplanungsservice-Fehlerprotokolls, das dem Vorgangssatz zugeordnet ist. | PSS-Fehlerprotokoll          |
| msdyn_PSSErrorLogName | Nicht verfügbar.                                                                                              | Nicht verfügbar         |
| msdyn_status          | Der Status des Vorgangssatzes.                                                                             | Status                 |
| msdyn_statusName      | Nicht verfügbar.                                                                                              | Nicht verfügbar         |
| msdyn_useraadid       | Die Azure Active Directory (Azure AD)-Objekt-ID des Benutzers, zu dem diese Anforderung gehört.                     | UserAADID              |

### <a name="operation-set-detail"></a>Vorgangssatzdetail

In der folgenden Tabelle werden die Felder angezeigt, die zu der Entität **Vorgangssatzdetail** gehören.

| Schemaname                 | Beschreibung des Dataflows                                                                                 | Anzeigename           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Die serialisierten Dataverse-Felder für die Anforderung.                                            | CdsPayload            |
| msdyn_entityname           | Der Name der Entität für die Anforderung.                                                     | EntityName            |
| msdyn_httpverb             | Die Anforderungsmethode.                                                                         | HTTP-Verb (veraltet) |
| msdyn_httpverbName         | Nicht verfügbar.                                                                             | Nicht verfügbar        |
| msdyn_operationset         | Der eindeutige Bezeichner des Vorgangssatzes, zu dem der Datensatz gehört.                      | OperationSet          |
| msdyn_operationsetdetailId | Der eindeutige Bezeichner der Entitätsinstanzen.                                                  | OperationSet-Detail   |
| msdyn_operationsetName     | Nicht verfügbar.                                                                             | Nicht verfügbar        |
| msdyn_operationtype        | Der Vorgangstyp des Vorgangssatzdetails.                                             | OperationType         |
| msdyn_operationtypeName    | Nicht verfügbar.                                                                             | Nicht verfügbar        |
| msdyn_psspayload           | Die serialisierten Projektplanungsservice-Felder für die Anforderung.                           | PssPayload            |
| msdyn_recordid             | Der eindeutige Bezeichner des Anforderungsdatensatzes.                                                       | Datensatz-ID             |
| msdyn_requestnumber        | Eine automatisch generierte Nummer zur Identifizierung der Reihenfolge, in der Anforderungen eingegangen sind. | Anforderungsnummer        |

## <a name="project-scheduling-service-error-logs"></a>Projektplanungsservice-Fehlerprotokolle

Die Projektplanungsservice-Fehlerprotokolle erfassen Fehler, die auftreten, wenn der Projektplanungsservice versucht, einen Vorgang **Speichern** oder **Öffnen** auszuführen. Es gibt drei unterstützte Szenarien, in denen diese Protokolle generiert werden:

- Vom Benutzer initiierte Aktionen schlagen kritisch fehl (z. B. kann eine Zuweisung aufgrund fehlender Berechtigungen nicht erstellt werden).
- Der Projektplanungsservice kann eine Entität nicht programmgesteuert erstellen, aktualisieren, löschen oder einen anderen kaskadierenden Vorgang für eine Entität ausführen.
- Beim Benutzer treten Fehler auf, wenn ein Datensatz nicht geöffnet werden kann (z. B. wenn ein Projekt geöffnet oder die Informationen eines Teammitglieds aktualisiert werden).

### <a name="project-scheduling-service-log"></a>Projektplanungsservice-Protokoll

In der folgenden Tabelle werden die Felder angezeigt, die im Projektplanungsservice-Protokoll enthalten sind.

| Schemaname          | Beschreibung des Dataflows                                                                    | Anzeigename    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Die Aufrufliste der Ausnahme.                                               | Aufrufliste     |
| msdyn_correlationid | Die Korrelations-ID des Fehlers.                                               | CorrelationId  |
| msdyn_errorcode     | Ein Feld, das verwendet wird, um den Dataverse-Fehlercode oder den HTTP-Fehlercode zu speichern. | Fehlercode     |
| msdyn_HelpLink      | Ein Link zur öffentlichen Hilfedokumentation.                                       | Hilfelink      |
| msdyn_log           | Das Protokoll des Projektplanungsservice.                                   | Protokoll            |
| msdyn_project       | Das Projekt, das dem Fehlerprotokoll zugeordnete ist.                             | Project        |
| msdyn_projectName   | Der Name des Projekts, wenn die Nutzdaten des Vorgangssatzes beibehalten werden. | Nicht verfügbar |
| msdyn_psserrorlogId | Der eindeutige Bezeichner der Entitätsinstanzen.                                     | PSS-Fehlerprotokoll  |
| msdyn_SessionId     | Die Sitzungs-ID des Projekts.                                                        | Sitzungs-ID     |

## <a name="error-log-cleanup"></a>Fehlerprotokollbereinigung

Standardmäßig können sowohl die Fehlerprotokolle des Projektplanungsservice als auch das Vorgangssatz-Protokoll alle 90 Tage bereinigt werden. Alle Datensätze, die älter als 90 Tage sind, werden gelöscht. Durch das Ändern des Wertes des Feldes **msdyn_StateOperationSetAge** auf der Seite **Projektparameter** können Administratoren den Bereinigungsbereich so anpassen, dass er zwischen 1 und 120 Tagen liegt. Es stehen mehrere Methoden zum Ändern dieses Werts zur Verfügung:

- Sie können die Entität **Projektparameter** anpassen, indem Sie eine benutzerdefinierte Seite erstellen und das Feld **Alter des veralteten Vorgangssatzes** hinzufügen.
- Verwenden Sie Clientcode, der das [WebApi-Software Development Kit (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) nutzt.
- Verwenden Sie den Service-SDK-Code, der die Xrm-SDK-**updateRecord**-Methode (Client-API-Referenz) in modellgesteuerten Apps nutzt. Power Apps enthält eine Beschreibung und unterstützte Parameter für die **updateRecord**-Methode.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
