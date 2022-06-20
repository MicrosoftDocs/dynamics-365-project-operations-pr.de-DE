---
title: Funktionsänderungen von Project Service Automation auf Project Operations
description: Dieser Artikel gibt einen Überblick über die Änderungen der Funktionen von Project Service Automation auf Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925349"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funktionsänderungen von Project Service Automation auf Project Operations

Das Upgrade von Dynamics 365 Project Service Automation zu Dynamics 365 Project Operations Lite wird in drei Phasen ausgeliefert. Dieser Artikel informiert Sie über die wichtigsten Änderungen, die Sie erwarten können, wenn das Upgrade abgeschlossen ist.

| Upgrade-Lieferung | Phase 1 <br>(Januar 2022) | Phase 2 <br>(April-Welle 2022) | Phase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Keine Abhängigkeit vom Projektstrukturplan (PSP) für Projekte. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP ist in der derzeit unterstützten Grenzen von Project Operations enthalten. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP außerhalb der derzeit unterstützten Grenzen von Project Operations, einschließlich der Unterstützung für den Project Desktop Client. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektmanagement

Die wichtigsten Änderungen in der Benutzererfahrung werden im Bereich der Projektplanung stattfinden. Project Operations übernimmt eine neue, moderne Erfahrung für die Verwaltung eines Projektstrukturplans (WBS), indem es die von [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) bereitgestellten Planungsfunktionen nutzt.

## <a name="differences-in-the-scheduling-experience"></a>Unterschiede in der Planungserfahrung

Die folgende Tabelle fasst die Planungsunterschiede zwischen Project Service Automation und Project Operations zusammen.

|  Terminplanung     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektvorlagen – Möglichkeit, Projektvorlagen zu definieren und anzuwenden, wenn ein Projekt erstellt wird  |  &nbsp;    | :heavy_check_mark: |
| Integration des Projektstrukturplans (WBS) im Desktop-Client   |    &nbsp;  | :heavy_check_mark: |
| Einschränkungen – nicht früher beginnen als,nicht später beenden als  | :heavy_check_mark: |   &nbsp;  |
| Meilensteine – Aufgaben ohne Dauer   | :heavy_check_mark:  |  &nbsp;  |
| Ressourcengesteuerte Aufgaben respektieren die Verfügbarkeit zugewiesener Ressourcen   | :heavy_check_mark: |  &nbsp;    |
| Zeitphasenbearbeitung – Pläne bearbeiten und auf Tag-für-Tag-Basis arbeiten   |   &nbsp;  | :heavy_check_mark: |
| Automatische/manuelle Planung – die Projektplanungs-Engine verwenden, um Aufgaben automatisch oder manuell zu planen |  &nbsp; | :heavy_check_mark:  |
| Bearbeiten Sie große Projekte direkt in der Benutzeroberfläche: Die Größe der bearbeitbaren Pläne ist unbegrenzt  | 500 Aufgaben Limit  | :heavy_check_mark:       |
| Prozent abgeschlossen – Aufgabenfortschritt markieren   | :heavy_check_mark:  |  &nbsp;  |
| [Projektzeitplan-Modi](../project-management/scheduling-modes.md) – das Projekt als feste Einheiten, festen Aufwand oder feste Dauer definieren | :heavy_check_mark: | &nbsp; |
| Zeitachse – die Zeitachsenansicht erstellen und anpassen, um Zeitplandetails zu visualisieren und mit Stakeholdern zu kommunizieren. | :heavy_check_mark:  | &nbsp; |
| Aufwandsgesteuerte Aufgaben – Planungs-Engine-Unterstützung zum Planen einer Aufgabe als aufwandsgesteuert  | :heavy_check_mark:  | &nbsp; |
| **Aufgabeninformationen**-Dialogfeld – Aufgabendetails mithilfe eines Dialogfelds speichern | :heavy_check_mark:  |  &nbsp;  |
| Drag-and-Drop – Aufgaben mehrfach auswählen und ihre Position auf dem PSP ändern | :heavy_check_mark: | &nbsp;  |
| Flexible persistente Ansichten – detailliertere Ansichten von Aufgabenattributen definieren   | :heavy_check_mark:  | &nbsp; |
| Sortieren und Filtern des WBS  | :heavy_check_mark:  | &nbsp; |
| Boards-Ansicht für Projektlieferungen ohne Wasserfallstruktur  | :heavy_check_mark:   | &nbsp; |
| Zeitachsenansicht – interaktives Gantt-Diagramm zur Visualisierung und Bearbeitung des WBS   | :heavy_check_mark:  | &nbsp; |
| Tastenkombinationen – Tastenkombinationen für häufige Vorgänge wie Einrücken oder Einfügen verwenden  | :heavy_check_mark:  |  &nbsp; |
| Rückgängigmachen auf mehreren Ebenen – Was-wäre-wenn-Analysen durchführen, um die Auswirkungen von Änderungen vollständig zu verstehen, indem Sie eine ganze Reihe von Vorgängen rückgängig machen und erneut anwenden | :heavy_check_mark: | &nbsp; |
| Ausschneiden/Kopieren/Einfügen – bei der Zeitplanentwicklung zusammenarbeiten, indem Sie Zeitplandetails zwischen Anwendungen kopieren und einfügen  | :heavy_check_mark: | &nbsp; |
| Aufgaben-Checklisten – einer Aufgabe bis zu 20 Checklisten-Elemente hinzufügen   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projektplanung

Die **Projekt**-Seite in Project Operations weist eine erhebliche Anzahl von Unterschieden im Vergleich zur **Projekt**-Seite in Project Service Automation auf.

Die folgenden Aktionen wurden aus der **Projekte**-Seite als Teil des Phase-1-Upgrades entfernt:

  - **In MS Project öffnen**
  - **Vorlage erstellen**
  - **Projekt von MS Project lösen**

Die **Projekt**-Seite in Project Operations enthält die folgenden neuen Registerkarten.

- **Materialvorkalkulationen**
- **Einrichtung der Aufgabenfakturierung**

Die **Status**-Registerkarte wurde entfernt und das **Status**-Feld ist jetzt auf der **Zusammenfassung**-Registerkarte mit dem Planungsmodus des Projekts.

   ![Aktualisierungen der Projektseite.](media/projectform.png)

Die **Zeitplan**-Registerkarte wurde zur **Aufgabe**-Registerkarte umbenannt und bietet die neue Projektplanungserfahrung mit Project for the Web.

   ![Neue Projektaufgaben-Registerkarte.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planungsmodi

Project Operations hat eine neue Funktion eingeführt: [Zeitplanungsmodi](../project-management/scheduling-modes.md). Alle vorhandenen Project Service Automation-Projekte werden in Project Operations standardmäßig auf **Feste Dauer** gesetzt. Die Voreinstellung für neue Projekte kann jedoch unter **Einstellungen** > **Parameter** > **Parameter** > **Zeitplanmodus** verwaltet werden.

   ![Projektparametereinstellungen für den Zeitplanmodus.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Grenzwerte der Projektplanung

Project Operations stützt sich für alle Projektplanungsvorgänge auf Project for the Web. Project for the Web verwaltet den Projektstrukturplan mithilfe der Grenzwerte in der folgenden Tabelle.

| **Feld**                                          | **Grenze**             |
|----------------------------------------------------|-----------------------|
| Maximale Gesamtanzahl an Aufgaben für ein Projekt                  | 500                   |
| Maximale Gesamtdauer für ein Projekt               | 3650 Tage (10 Jahre)  |
| Maximale Gesamtressourcen für ein Projekt              | 300                   |
| Maximale Gesamtzahl der Links (nur Nachfolger) für ein Projekt | 600                   |
| Maximale Gesamtanzahl benutzerdefinierter Felder für ein Projekt          | 10                    |
| Maximale Hierarchieebene                            | 10 Ebenen             |
| Maximale Links (Nachfolger + Vorgänger)            | 20                    |
| Maximale Dauer der Blattaufgabe                      | 1250 Tage             |
| Maximale Dauer einer Sammelaufgabe                 | 3650 Tage (10 Jahre)  |
| Maximale Ressourcen, die einer Aufgabe zugewiesen sind               | 20 Ressourcen          |
| Unterstützter Datumsbereich für eine Aufgabe                    | 1.1.2000 bis 31.12.2149 |
| Prüflistenelemente                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Erweiterbarkeit und Entwicklung der Projektplanung

Nach dem Upgrade auf Project Operations müssen Sie die Project Scheduling APIs verwenden, um Erstellungs-, Aktualisierungs- und Löschvorgänge für die folgenden Entitäten auszuführen:

|   Name der Entität           |   Logischer Entitätsname       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektaufgabe            | msdyn_projecttask           |
| Abhängigkeit der Projektaufgaben | msdyn_projecttaskdependency |
| Ressourcenzuweisung     | msdyn_resourceassignment    |
| Projekt-Bucket          | msdyn_projectbucket         |
| Projektteammitglied     | msdyn_projectteam           |

Wenn Sie derzeit über Anpassungen verfügen, die diese Entitäten betreffen, finden Sie unter [Verwenden der Projektplan-APIs zur Durchführung von Operationen mit Zeitplan-Entitäten](../project-management/schedule-api-preview.md) eine Anleitung zur Umsetzung.

## <a name="data-model-changes"></a>Datenmodeländerungen

Im Rahmen der Upgrade Phase 1 gibt es Änderungen am Datenmodell. Diese Änderungen sind in erster Linie Feldänderungen an bestehenden Entitäten. In Phase 1 sind die Entitäten **msydn_project** und **msdyn_projectteam** ein Refactoring von Anpassungen. 

> [!IMPORTANT]
> Dieser Abschnitt wird mit zusätzlichen Entitäten aktualisiert, wenn zukünftige Upgrade-Phasen abgeschlossen sind.

Die folgenden Felder wurden durch neue Felder ersetzt.

|   Entity          |   Alter logischer Name   |   Neuer logischer Name    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Die folgenden Felder sollten hinzugefügt worden sein.

|   Entity          |   Logischer Name                               |   Beschreibung des Dataflows |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Zeigt die aggregierten tatsächlichen Gebühren für das Projekt an. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_actualmaterialcost                     | Zeigt die aggregierten tatsächlichen Materialkosten für das Projekt an. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_actualmaterialsales                    | Zeigt die aggregierten tatsächlichen Materialausgaben für das Projekt an. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Die diesem Projekt zugeordnete Vertragszeile. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Dies ist ein internes Systemfeld, das für eine **Projektkopie** verwendet wird, die sich auf die Korrelations-ID bezieht. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_copyprojectsessionid                   | Dies ist ein internes Systemfeld, das für eine **Projektkopie** verwendet wird, die sich auf die Sitzungs-ID bezieht. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_globalrevisiontoken                    | Letzte Synchronisierung xRM Global Revision Token vom Projektplanungsdienst. |
| msdyn_project     | msdyn_msprojectdocument                      | Das Microsoft Project-Dokument, das dem Projekt angehört. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Die aggregierten geplanten tatsächlichen Materialkosten für das Projekt an. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_plannedmaterialsales                   | Die aggregierten geplanten tatsächlichen Materialausgaben für das Projekt an. Nur zur Verwendung in Project Service Automation |
| msdyn_project     | msdyn_program                                | Das Programm, mit dem dieses Projekt verknüpft ist. |
| msdyn_project     | msdyn_quotelineproject                       | Die diesem Projekt zugeordnete Angebotszeile. |
| msdyn_project     | msdyn_replaylogheader                        | Die Kopfzeile für die Wiedergabeprotokolle. |
| msdyn_project     | msdyn_schedulemode                           | Der Standardplanungsmodus, der für alle Aufgaben des Projekts verwendet wird.  |
| msdyn_project     | msdyn_taskearlieststart                      | Das früheste Startdatum einer beliebigen Aufgabe im Projekt.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Das Mitglied des Projektteams an, von dem dieses Mitglied des Projektteams kopiert wurde. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Gibt an, ob die Ressourcenanforderung für ein neu erstelltes allgemeines Teammitglied erstellt werden soll.  |
| msdyn_projectteam | msdyn_deletestatus                           | Der Löschstatus des Teammitglieds, um nachzuverfolgen, ob eine Löschanforderung an den Project-Zeitplanservice gesendet wurde und ob es die Antwort erfolgreich innerhalb des erwarteten Zeitfensters zurücksendet. |
| msdyn_projectteam | msdyn_effortcompleted                        | Verfolgt den Aufwand, den das Teammitglied für seine Zuweisungen erzielt hat. |
| msdyn_projectteam | msdyn_effortremaining                        | Verfolgt den Aufwand, der noch vom Teammitglied für seine Zuweisungen abgeschlossen werden muss. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Die Wartezeit ab dem Zeitpunkt, an dem das Teammitglied eine Löschanforderung an den Project-Planungsdienst sendet, bis das Teammitglied tatsächlich in Microsoft Dataverse gelöscht wird.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Der Zeitstempel, der aufgezeichnet werden soll, wenn die Löschanforderung für das Teammitglied an den Project-Planungsdienst gesendet wird. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Zeigt das Mitglied des Projektteams an, von dem dieses Mitglied des Projektteams kopiert wurde.  |

## <a name="project-templates"></a>Projektvorlagen

Project Operations bietet keine Unterstützung für Projektvorlagen. Sie können jedoch einen Großteil der Kernfunktionalität mit der Verwendung der [Project Copy-API](../project-management/dev-copy-project.md) replizieren.

## <a name="desktop-add-in-support"></a>Unterstützung für Desktop-Add-Ins

Die Unterstützung für das Microsoft Project Desktop-Add-In ist in den ersten beiden Phasen des Upgrades nicht verfügbar. In Phase 3 können Kunden mit Projekten, die die derzeit unterstützten Grenzwerte von Project for the Web überschreiten, das Desktop-Add-In verwenden.

## <a name="editing-resource-assignment-contours"></a>Bearbeiten der Konturen der Ressourcenzuweisung

Die Möglichkeit, Ressourcenzuweisungskonturen zu bearbeiten, wird verfügbar sein, wenn Phase 2 des Upgrades verfügbar ist.

## <a name="billing-and-pricing"></a>Preise und Abrechnung

Die folgenden neuen Funktionen wurden in Project Operations hinzugefügt. Diese Funktionen sind von Natur aus additiv und wirken sich nicht auf das Project Service Automation-Datenmodell aus.

- [Materialverbrauch für Projekte und Projektaufgaben erfassen](../material/material-usage-log.md)
- [Fremdarbeitsverwaltung](../pro/subcontracting/managing-subcontracts-overview.md)
- [Vorauszahlungen oder auf dem Vorbehalt basierende Verträge](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status und Validierungen des Vertrags, die nicht überschritten werden dürfen](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Aufgabenbasierte Abrechnung](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Veraltete Komponenten

Die folgenden Tabellen dokumentieren alle veralteten Felder, die nach dem Upgrade in die Lösung für veraltete Komponenten verschoben werden. Weitere Informationen und einen Link zur Lösung finden Sie unter [Dynamics 365 Project Service Automation 3x zu Project Operations 4x veraltete Komponenten](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Felder                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

