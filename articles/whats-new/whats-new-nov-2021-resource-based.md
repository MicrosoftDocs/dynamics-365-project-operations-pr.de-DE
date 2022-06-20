---
title: Neuigkeiten für November 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Version von Project Operations vom November 2021 für Szenarien mit/ohne Ressourcenvorrat zur Verfügung stehen.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932893"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für November 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Versionen 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.22

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- Anwendungsprogrammierschnittstellen (APIs) für die Projektplanung unterstützen jetzt die Möglichkeit, Projekt-Buckets zu erstellen und zu löschen.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](/dynamics365/project-operations/environment/resource-dual-write-maps).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-in-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2240080 | Das Feld **Zahlungsbedingungen** darf auf der Pro-forma-Rechnung nicht dupliziert werden. |
| Preise und Abrechnung | 2358236 | Die Rechnungskorrektur muss Korrekturen mit Nullpreiszeilen zulassen. |
| Ressourcenverwaltung | 2410072 | Einrichtung einer Ressource erlauben, die einer Aufgabe als Projektmanager zugewiesen ist. |
| Preise und Abrechnung | 2430234 | Ein Problem mit der Kosten-Leistungs-Berechnung beheben. |
| Zeit und Ausgaben | 2436978 | Zulassen, dass die Zeit im Format hh:mm eingegeben wird. |
| Preise und Abrechnung | 2448623 | Erlauben, dass Preislisten aktualisiert werden, nachdem sie einer Organisationseinheit zugeordnet wurden. |
| Zeit und Ausgaben | 2460396 | Erlauben, dass ein Zeiteintrag gelöscht wird, indem Sie die Zelle leeren. |
| Preise und Abrechnung | 2467386 | Zulassen, dass ein Projekt mit einer Aufgabe gelöscht wird, auch wenn die Aufgabe mit einem gewonnenen Angebot verknüpft ist. |
| Zeit und Ausgaben | 2461744 | Die Ansicht **Meine fehlgeschlagenen Genehmigungen** enthält nur Projektgenehmigungen in der Phase **Gesendet**. |
| Zeit und Ausgaben | 2464082 | Entfernen Sie den Link von den Projektgenehmigungen zum Genehmigungssatz, wenn ein Zielstatus übereinstimmt. |
| Zeit und Ausgaben | 2468108 | Der Zeitplanauftrag sollte keinen Status **Wird verarbeitet** für den Genehmigungssatz festlegen. |
| Zeit und Ausgaben | 2471503 | Löschen Sie Genehmigungssätze, die sieben Tage alt sind. |
| Preise und Abrechnung | 2480687 | Die Angebotszeilenreferenz darf nicht entfernt werden, wenn ein Angebotszeilen-Meilenstein erstellt wird. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Einbehaltene Zuliefererbeträge in Projektausgabentransaktionen werden nicht in der Transaktionsliste angezeigt. |
| Projektmanagement und -buchhaltung | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Die Intercompany-Zuliefererrechnung ist fehlerhaft, wenn die Zuliefererrechnungsintegration aktiviert ist. |
| Projektmanagement und -buchhaltung | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Die Zahlungsbedingungen auf Projektrechnungen funktionieren nicht wie erwartet. |
| Projektmanagement und -buchhaltung | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Wenn die Zuliefereraufbewahrung freigegeben wird, enthält die Belegbuchung zusätzliche Zeilen, die nicht korrekt sind. |
| Projektmanagement und -buchhaltung | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Wenn das Integrationsjournal von Project Operations gebucht wird, schlägt es aufgrund fehlender Dimensionen für ein Konto fehl, auf das nicht gebucht wird. |
| Projektmanagement und -buchhaltung | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Die Registerkarte **Projekt** kann auf einer ausstehenden Zuliefererrechnung nicht bearbeitet werden, wenn dem Artikel die Beschaffungskategorie zugewiesen ist. |
| Projektmanagement und -buchhaltung | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Der Navigationsbereich fehlt, wenn Sie nicht bei Project Operations Dataverse angemeldet sind. |
| Projektmanagement und -buchhaltung | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Wenn Sie Umsatz aus einer Projektrechnung in einem angewendeten Einbehaltungsfall buchen, tritt ein Problem auf, da die Transaktionen auf dem Beleg nicht ausgeglichen sind. |
| Projektmanagement und -buchhaltung | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Die Erstellung eines Kostenvoranschlags nach dem Buchen eines Rechnungsvorschlags blockiert Korrekturzeilen vom Import. |
| Projektmanagement und -buchhaltung | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Die Änderung eines vollständig fakturierten Meilensteindatensatzes sollte nicht möglich sein. |
| Reisekosten und Ausgaben | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle Ausgabenberichte sind sichtbar, wenn Sie in der mobilen Ausgaben-App nach einer Kategorie suchen. |
| Reisekosten und Ausgaben | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Falsche Beträge für Zulieferer- und Mehrwertsteuertransaktionen werden aus einer Ausgabe gebucht, die aus einer Kreditkartentransaktion erstellt wurde. |
| Reisekosten und Ausgaben | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Eine irrelevante Warnung wird angezeigt, wenn Sie die Seite **Ausgabenbericht** aktualisieren. |
| Reisekosten und Ausgaben | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Die falsche vorläufige genehmigende Person wird verwendet, wenn Sie eine vorläufigen genehmigende Person löschen und dann einen Ausgabenbericht über den Workflow erneut einreichen. |
| Reisekosten und Ausgaben | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es tritt ein Buchungsfehler im Zusammenhang mit der Kilometereinstellung auf. |
