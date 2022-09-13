---
title: Was ist neu August 2022 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien
description: Dieser Artikel enthält Informationen zu den Qualitätsupdates, die in der Version vom August 2022 von Microsoft Dynamics 365 Project Operations für ressourcenbasierte/nicht vorratsbasierte Szenarien zur Verfügung stehen.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403855"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu August 2022 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.45.0.53
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Verkaufschancenmanagement | 2762089 | Fehlerbehandlung beim Schließen des Vertrags als verloren, wenn die automatische Speicherung in der Organisation deaktiviert ist.|
|Projektplanung und -nachverfolgung | 2767841 | Telemetrieaktualisierungsprojekt Entitäts- oder Aktualisierungsszenarien erstellen|
|Preise und Abrechnung | 2771072 | Nullreferenz-Ausnahmebehandlung beim Gewinnen des Angebots.|
|Preise und Abrechnung | 2844181 |Fehler beim Abrufen einer Korrelations-ID und Blockieren einer Rechnungserstellung.|
|Preise und Abrechnung | 2852836 | Intercompany-Ist-Werte fehlen für Intercompany-Ausgaben, die in CE erstellt und genehmigt wurden.|


### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) an.
