---
title: Project Operations – Duales Schreiben-Zuordnungsversionen
description: Dieser Artikel enthält die Liste der Dual-write Zuordnungen, die für Dynamics 365 Project Operations erforderlich sind.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee0b6a1722405e6a50c42db6bd2a25b872c6118c
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959454"
---
# <a name="project-operations-dual-write-map-versions"></a>Project Operations – Duales Schreiben-Zuordnungsversionen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Verwenden von Dynamics 365 Project Operations für Szenarien mit oder ohne Lagerbestand muss eine Reihe von Dual-Write-Zuordnungen in der Umgebung ausgeführt werden. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Vorausgesetzte Zuordnungen: Orchestrierungslösung für duales Schreiben

Die folgenden Zuordnungen sind erforderliche Voraussetzungen für die Project Operations-Lösung. Stellen Sie sicher, dass Sie die in der folgenden Tabelle aufgeführten Zuordnungen und alle zugehörigen Tabellenzuordnungen in Ihrer Umgebung ausführen.

| Tabellenzuordnung | Erste Synchronisierung |
| --- | --- |
| Sachkonto (msdyn_ledgers) | Erfordert eine anfängliche Synchronisierung für die Tabellenzuordnung und alle Voraussetzungen. Master für die erste Synchronisierung ist Finanz- und Betriebs-Apps. |
| Juristische Personen (cdm_companies) | Nicht erforderlich. Das System füllt diese Entität automatisch, wenn Umgebungen mit Dual-Write verknüpft werden. |
| Kunden V3 (Konten) | Für die Bereitstellung nicht erforderlich. |
| Anbieter V2 (msdyn_vendors) | Für die Bereitstellung nicht erforderlich. |

1. Wählen Sie aus der Liste der Zuordnungen Finanzbuchhaltung **(msdyn\_ledgers)** mit allen Voraussetzungen aus und wählen Sie das Kontrollkästchen **Erstsynchronisation** aus. Wählen Sie im Feld **Master für die erste Synchronisierung** **Finanz- und Betriebs-Apps** sowohl für die Hauptbuchzuordnung als auch für alle erforderlichen Zuordnungen aus. **Ausführen** auswählen.

![Synchronisation der Ledger-Zuordnung.](media/DW6.png)

2. Befolgen Sie die gleichen Schritte für alle verbleibenden Tabellenzuordnungen, die in der obigen Tabelle aufgeführt sind. Wählen Sie nicht **Erstsynchronisation** Kontrollkästchen beim Ausführen dieser Zuordnungen aus.

## <a name="project-operations-dual-write-maps"></a>Duales Schreiben-Zuordnungen für Project Operations

Die folgenden Zuordnungen sind erforderliche Voraussetzungen für eine Project Operations-Lösung. Kartenversionen mit doppeltem Schreibzugriff werden ab der Aktualisierung von Project Operations vom Mai 2021, Version 4.10.0.186, aufgelistet.

| Entitätszuordnung | Neueste Version | Erste Synchronisierung | Erforderliche Dynamics 365 Finance-Version |
| --- | --- | --- | --- |
| Integrationsentität für die Projekttransaktionsbeziehungen (msdyn\_transactionconnections) | 1.0.0.0 | Für die Bereitstellung nicht erforderlich. ||
| Projektvertragskopfzeilen (Vertriebsaufträge) | 1.0.0.1 | Für die Bereitstellung nicht erforderlich. ||
| Projektvertragszeilen (salesorderdetails) | 1.0.0.0 | Für die Bereitstellung nicht erforderlich. ||
| Projektfinanzierungsquelle (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Für die Bereitstellung nicht erforderlich. ||
| Project Operations-Integrationstabelle für Materialschätzungen (msdyn\_estimatelines) | 1.0.0.0 | Für die Bereitstellung nicht erforderlich. ||
| Projektrechnungsvorschläge V2 (Rechnungen) | 1.0.0.3 | Für die Bereitstellung nicht erforderlich. ||
| Tatsächliche Werte der Project Operations-Integration (msdyn_actuals) | 1.0.0.14 | Für die Bereitstellung nicht erforderlich. ||
| Vertragszeilenmeilensteine für die Integration von Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Für die Bereitstellung nicht erforderlich. ||
| Project Operations-Integrationsentität für Spesenvorkalkulationen (msdyn_estimatelines) | 1.0.0.2 | Für die Bereitstellung nicht erforderlich. ||
| Project Operations-Integritätsentität für Stundenvorkalkulationen (msdyn_resourceassignments) | 1.0.0.5 | Für die Bereitstellung nicht erforderlich. ||
| Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn_expensecategories) | 1.0.0.1 | Für die Bereitstellung nicht erforderlich. ||
| Exportentität für Projektkosten der Project Operations-Integration (msdyn_expenses) | 1.0.0.3 | Für die Bereitstellung nicht erforderlich. ||
| Project Operations-Integrationsprojektanbieter-Rechnungsexportentität (msdyn_projectvendorinvoices) | 1.0.0.1 | Für die Bereitstellung nicht erforderlich. |10.0.26 oder höher|
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Für die Bereitstellung nicht erforderlich. | 10.0.26 oder höher |
| Projektressourcenrollen für alle Unternehmen (bookableresourcecategories) | 1.0.0.1 | Erfordert eine erste Synchronisierung für die Tabellenzuordnung, um die Ressourcenrollen des Projektmanagers und der Teammitglieder zu synchronisieren, die in der Dynamics 365 Dataverse Umgebung während der Bereitstellung ausgefüllt sind. Dataverse ist die Hauptquelle für die anfängliche Synchronisation. ||
| Projektaufgaben (msdyn_projecttasks) | 1.0.0.4 | Für die Bereitstellung nicht erforderlich. ||
| Projekttransaktionskategorien (msdyn_transactioncategories) | 1.0.0.0 | Für die Bereitstellung nicht erforderlich. ||
| Projekte V2 (msdyn_projects) | 1.0.0.2 | Für die Bereitstellung nicht erforderlich. ||

Schließen Sie die folgenden Schritte ab, um die aufgeführten Zuordnungen auszuführen.

1. Aktivieren Sie die Projektressourcenrollen für die Tabellenzuordnung **alle Unternehmen (bookableresourcecategories)**, da diese Zuordnung die anfängliche Synchronisierung erfordert. Wählen Sie im Feld **Master für die Erstsynchronisation** **Common Data Service**. 

 ![Synchronisierung der Zuordnung von Ressourcenrollentabellen.](media/6ResourceInitialSync.jpg)

 Warten Sie, bis der Status der Zuordnung **Wird ausgeführt** lautet, bevor Sie mit dem nächsten Schritt fortfahren.

2. Wählen Sie alle verbleibenden erforderlichen Zuordnungen aus. Sie können sie in der Liste der Dual-Write-Zuordnungen mit dem Schlüsselwort **Project** in der Suche in der oberen rechten Ecke filtern. Sie können alle Zuordnungen mehrfach auswählen und dann ausführen. Weitere Informationen finden Sie unter [Verwalten mehrerer Tabellenzuordnungen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Stellen Sie sicher, dass Sie auch zugehörige Entitätszuordnungen aktivieren und ausführen.

### <a name="project-operations-dual-write-map-versions"></a>Project Operations – Duales Schreiben-Zuordnungsversionen

Führen Sie immer die neueste Version der Zuordnung in Ihrer Umgebung aus. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn eine der folgenden Bedingungen vorliegt:

- Eine Zuordnung ist nicht aktiviert.
- Die neueste Version der Zuordnung ist nicht aktiviert. 
- Verwandte Tabellenzuordnungen sind nicht aktiviert.

Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, müssen Sie die Änderungen erneut anwenden. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
