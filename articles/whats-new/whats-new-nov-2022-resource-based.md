---
title: Neuigkeiten für November 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen zu den Qualitätsupdates, die in der Version vom November 2022 von Microsoft Dynamics 365 Project Operations für ressourcenbasierte/nicht vorratsbasierte Szenarien zur Verfügung stehen.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831083"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für November 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.58.0.119
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2781818 | Fehler „Schlüssel nicht gefunden“ beim Standardpreis für das Materialnutzungsprotokoll. |
| Preise und Abrechnung | 2922373 | Die Angebotsposition kann nicht mit einem Projekt verknüpft werden, das als verlorenes Angebot geschlossen wurde. |
| Preise und Abrechnung | 2943206 | **Das Feld Vertragszeile** in der Projektentität sollte optional sein. |
| Preise und Abrechnung | 2953182 | Fehlermeldung für Korrekturrechnungen verbessert.|
| Preise und Abrechnung | 2959500 | Die Angebotsposition kann nicht mit einer Projektaufgabe verknüpft werden, die bereits mit einem verlorenen Angebot verknüpft ist.|
| Preise und Abrechnung | 2959560 | Die Nachricht „Dieser Kunde ist bereits im Projektvertrag“, die beim Schließen des Angebots als gewonnen in bestimmten Gebietsschemas empfangen wird. |
| Preise und Abrechnung | 3031727 | Ressourcenzuweisungen schlagen mit dem Fehler „erforderliches Feld „msdyn_Company“ fehlt“ fehl. |
| Preise und Abrechnung | 3036905 | Ownering Company wird niemals auf dem ProjectTeamMember initialisiert. |
| Verkaufschancenmanagement | 2763519 | Null-Referenz-Fehler in „EnsureProjectContractAllowsUpdates“. |
| Verkaufschancenmanagement | 2783798 | Beim Importieren von Projektschätzungen in die Angebotsposition fehlen Aufgabenbeschreibungen für Kosten- und Materialschätzungen.|
| Verkaufschancenmanagement | 2988635 | Verbessern Sie die Beschreibung der Fehlermeldung beim Löschen des Kunden im Angebot. |
| Verkaufschancenmanagement | 3001191 | Angebot aus Verkaufschance kann nicht erstellt werden, wenn die Abrechnungsmethode als null angegeben ist. |
| Upgrade ausführen | 3012324 | Die Projektkonvertierung ist bei einem Projekt mit Steuerzeichen wie Tab im Namen fehlgeschlagen. || Projektplanung und -nachverfolgung | 2790384 | Das Timeout Pending OperationSet ist zu kurz. |
| Projektplanung und -nachverfolgung | 3044275 | Fehlende Lokalisierung für: missingProjectSchedulerErrorMessage. |
| Projektplanung und -nachverfolgung | 3044277 | Project Recon-Raster wird nicht geladen, wenn der Scheduler deaktiviert ist.|
| Ressourcenverwaltung | 2943153 | Aktualisieren Sie die Registerkarte Nachverfolgung, um zwei Dezimalstellen für die Dauer anzuzeigen.|
| Fremdarbeit | 2932774 | Fehler beim Lesen der Kreditorenrechnungszeile fälschlicherweise. |
| Fremdarbeit | 2939556 | Der Status Kreditorenrechnungskopf sollte nicht auf Entwurf online löschen gesetzt werden, wenn er nicht aktiv ist. |
| Zeit und Ausgaben | 2939998 | Nehmen Sie die neue TESA-Version in ProjOps auf. |


### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [Wissensdatenbankartikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) an.
