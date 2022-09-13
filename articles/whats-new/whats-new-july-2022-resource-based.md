---
title: Was ist neu Juli 2022 - Project Operations für ressourcen-/nicht vorrätig-basierte Szenarien
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Version vom Juli 2022 von Microsoft Dynamics 365 Project Operations für Szenarien mit und ohne Ressourcenvorrat zur Verfügung stehen.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403950"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu Juli 2022 - Project Operations für ressourcen-/nicht vorrätig-basierte Szenarien

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.44.0.22
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Bereitstellung und Konfiguration | 2761472 | Ein Project Operations-Installationsfehler wird behandelt. |
| Preise und Abrechnung | 2746940 | Der Positionsname des Unterauftrags darf maximal 100 Zeichen lang sein. |
| Preise und Abrechnung | 2739162 | Kunden müssen Menübandschaltflächen in der Ist-Rasteransicht sehen können. |
| Projektplanung und -nachverfolgung | 2730318 | Aktualisierte Validierung für nicht unterstützte Zeichen im Projektbetreff. |
| Preise und Abrechnung | 2705361 | Abgerechnete Umsatz-Ist-Werte für Meilensteine müssen in die Projektverfolgungsfelder aufgenommen werden. |
| Preise und Abrechnung | 2675880 | Verhindern, dass ein Projekt mit einer Vertragsposition verknüpft wird, die nicht arbeitsbasiert ist. |
| Preise und Abrechnung | 2664396 | Wenn eine Angebotspreisliste ohne Angebot gespeichert wird, muss ein Fehler auftreten, der besagt, dass das Angebot nicht leer sein darf. |
| Preise und Abrechnung | 2184019 | Die Registerkarte **Aufgabenbasierte Abrechnung** sollte nicht für Projekte angezeigt werden, die keinen Rahmenvertrag oder kein Angebot haben. |
| Zeit und Ausgaben | 2754459 | Wenn der Cloud-Flow für die wiederkehrende Planung inaktiv ist, wird das Banner angezeigt und die asynchrone Verarbeitung umgangen. |
| Preise und Abrechnung | 2724391 | Eine falsche Ausnahme wird ausgelöst, wenn in der Abrechnungsregel für die Teilung des Projektvertrags ein Kundenwert fehlt. |
| Preise und Abrechnung | 2708638 | Der Datensatz wurde bei der Suche mit der Rastersuche in Materialverwendungen und Genehmigungen für Materialverwendungen nicht gefunden.|
| Preise und Abrechnung | 2686977 | Validierung für Rechnungsposten während der Rechnungserstellung verhindern. |
| Preise und Abrechnung | 2683032 | Das Kopieren kostenpflichtiger Rollen und Kategorien skaliert nicht über 5000 Datensätze hinaus.|
| Preise und Abrechnung | 2673363 | Cost Consumption % on Project ist beschädigt, wenn sowohl Aufwands- als auch Kostenschätzungen und Ist-Werte für ein Projekt vorhanden sind. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) an.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Diese Features sind in der nächsten Version standardmäßig aktiviert.

Die folgende Tabelle listet die Features auf, die in Version 10.0.29 standardmäßig aktiviert sind. Die meisten Features, die automatisch aktiviert wurden, können in [Featureverwaltung](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) deaktiviert werden. In Zukunft könnten einige Features, die automatisch aktiviert wurden, aus der Featureverwaltung entfernt und obligatorisch werden. Diese Änderung stellt sicher, dass Kunden die aktuelle Funktionalität verwenden, sodass Erweiterungen auf der aktuellen Funktionalität aufbauen können, wenn sie hinzugefügt werden. Features werden niemals in weniger als einem Jahr automatisch aktiviert, es sei denn, sie gelten als wesentlich.

| Funktionsname | Datum aktivieren | Feature hinzugefügt | Featurezustand | Modul |
| --- | --- | --- |--- |--- |
| Anpassung der Stundentransaktion basierend auf einer Änderung der Zuordnung der Finanzierungsregeln aktivieren | 16. September 2022 | 7. Oktober 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Stornierungsfunktion für Vorauszahlungsrechnungen für Projektbestellungen | 16. September 2022 | 6. Oktober 2021 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Rechnungsvorschlagspositionen löschen, wenn Project Operations für ressourcenbasierte/nicht gelagerte Szenarien verwendet werden | 16. September 2022 | 6. Oktober 2021 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Buchhaltung für eine gebuchte Projekttransaktion anpassen | 16. September 2022 | 10  Mai 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Standardmäßige Buchhaltungseinrichtung für das Projekt aktivieren | 16. September 2022 | 19. Februar 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Mehrere Vertragszeilen für ein Projekt aktivieren | 16. September 2022 | 29. Juni 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Schreibschutz für Projektstundenjournale festlegen, wenn der aktuelle Genehmigungsstatus keine Bearbeitung zulässt | 16. September 2022 | 6. Oktober 2021 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Synchronisierung von Verkaufspositionen mit Einkaufspositionen aktualisieren, wenn Einkaufspositionen aktualisiert werden und der Änderungsverwaltungsparameter aktiviert ist | 16. September 2022 | 7. Oktober 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Project Operations auf Dynamics 365 Customer Engagement aktivieren | 16. September 2022 | 29. Juni 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |
| Feature zur Korrektur der Stornierung von Projekttransaktionen | 16. September 2022 | 13. Juli 2020 | Standardmäßig aktiviert | Projektmanagement und -buchhaltung |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funktionen, die in der kommenden Version obligatorisch werden

Die folgende Tabelle listet die Funktionen auf, die ab Version 10.0.29 obligatorisch sind.

| Funktionsname | Datum aktivieren | Feature hinzugefügt | Featurezustand | Modul |
| --- | --- | --- | --- | --- |
| Den zugesagten Wert für die Finanzierungsquelle berechnen, ohne den Wechselkurs zu runden | 16. September 2022 | 14. Juni 2020 | Obligatorisch | Projektmanagement und -buchhaltung |
| Projektanpassungsbuchung mit demselben Sachkonto wie die ursprüngliche Transaktion buchen | 16. September 2022 | 14. Juni 2020 | Obligatorisch | Projektmanagement und -buchhaltung |
| Details zum zugesagten Betrag des Projektvertrags | 16. September 2022 | 31. August 2019 | Obligatorisch | Projektmanagement und -buchhaltung |
| Sortierung nach Ressourcen während der Erstellung von Projektrechnungsvorschlägen aktivieren | 16. September 2022 | 31. August 2019 | Obligatorisch | Projektmanagement und -buchhaltung |
