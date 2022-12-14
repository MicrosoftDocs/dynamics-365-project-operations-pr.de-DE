---
title: Neuigkeiten Oktober 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel enthält Informationen zu den Qualitätsupdates, die in der Version vom Oktober 2022 von Microsoft Dynamics 365 Project Operations für ressourcenbasierte/nicht vorratsbasierte Szenarien zur Verfügung stehen.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806604"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten Oktober 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.57.0.176
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.30

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

| Funktionsbereich | Funktionsname | Weitere Informationen |
| --- | --- | --- |
| Projektplanung und -nachverfolgung | **Project Operations externe Planung**<br>Mit der externen Zeitplanung können Kunden Entitäten, die sich auf Projektstrukturpläne (WBS) beziehen, durch die Verwendung der nativen Dataverse APIs nativ erstellen, aktualisieren und löschen, jedoch ohne die aktuellen Einschränkungen, die von Microsoft Project for the Web erzwungen werden. | [Externe Zeitplanung](/dynamics365/project-operations/project-management/external-scheduling) |
| Bereitstellung und Konfiguration | <p>**Erlauben Sie Kunden, den Bereitstellungstyp auszuwählen**<br>Produktgesteuerte Updates (PDUs) von Project Operations werden verwendet, um die Dual-Write-Lösung von Project Operations automatisch zu installieren, wenn Dual-Write-Kern- und -Orchestrierungslösungen in der Umgebung installiert sind.</p><p>Diese Funktion führt einen neuen **Lösungs-Upgrade-Verhalten** Parameter in den Projektparametern ein. Wenn dieser Parameter auf **Nur Lite** eingestellt ist, werden PUDs nicht mehr verwendet, um die Dual-Write-Lösung von Project Operations automatisch zu installieren, selbst wenn Dual-Write-Kern- und -Orchestrierungslösungen in der Umgebung installiert sind. Dieses Verhalten kommt Kunden zugute, die Dual-Write-Lösungen verwenden möchten, um Verkaufsaufträge in Finanz- und Betriebs-Apps zu integrieren, Project Operations jedoch in einem Lite-Modus verwenden möchten (d. h. ohne Integration in Finanz- und Betriebs-Apps).</p> | |
| Preise und Abrechnung | <p>**Währungsumrechnung für nicht fakturierte Verkaufstransaktionen in integrierten Umgebungen**<br>Für Kunden, die Project Operations integriert mit Finanz- und Betriebs-Apps verwenden (d. h. im Ressourcen-/nicht gelagerten Bereitstellungstyp), werden Wechselkurse in der Regel in Finanz- und Betriebs-Apps gemeistert. Wenn eine Ausgabenkategorie jedoch mit der Preisberechnungsmethode „zum Selbstkostenpreis“ oder „Aufschlag auf Selbstkostenpreis“ berechnet werden soll, wenn dem Kunden eine Rechnung gestellt wird, verwendet der Wechselkurs, der zur Berechnung des Verkaufsbetrags verwendet wird, die Wechselkurse in Dataverse, nicht die Wechselkurse aus Finanz- und Betriebs-Apps.</p><p>Diese Funktion führt einen neuen **Währungsumrechnungsverhalten** Parameter in den Projektparametern ein. Wenn dieser Parameter auf **Erweitert mit Fallback** gesetzt ist, werden nicht fakturierte Verkaufsbeträge für Spesentransaktionen anhand der Wechselkurse aus Finanz- und Betriebs-Apps berechnet.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Preise und Abrechnung | 2316317 | Das System ermöglicht die Erstellung von Rechnungen ohne fakturierbare Transaktionen. |
| Preise und Abrechnung | 2737300 | Überprüfen Sie die Verfügbarkeit des Felds **Kunde**, bevor auf das Formular zugegriffen wird. |
| Preise und Abrechnung | 2744948 | Fügen Sie eine Nullprüfung für die Abrechnungsmethode hinzu. |
| Preise und Abrechnung | 2763515 | Null-Referenz-Fehlerbehandlung, wenn der Kaufvertrag der Rechnung fehlt. |
| Preise und Abrechnung | 2844301 | Die Batch-Rechnungserstellung schlägt aufgrund eines Fehlers fehl. |
| Preise und Abrechnung | 2845869 | Falsche Speicherung des Organisationsdienstes. |
| Preise und Abrechnung | 2853729 | Rollen- und Preisdetails werden aktualisiert, wenn der Abrechnungstyp geändert wird. |
| Preise und Abrechnung | 2940350 | Bei der Bepreisung von Istwerten sollten nur aktive Preislisten automatisch eingetragen werden. |
| Bereitstellung und Konfiguration | 3001206 | Die Entität msdyn\_replaylogheader verhindert Upgrades von Kundenorganisationen. |
| Verkaufschancenmanagement | 2755582 | Behandlung von Ausnahmen für Nullreferenzen im Helfer für geteilte Abrechnungsregeln. |
| Verkaufschancenmanagement | 2761477 | Wenn geteilte Abrechnung verwendet wird, hinterlässt das Löschen eines Meilensteins (Kopfzeile) verwaiste Meilensteine. |
| Verkaufschancenmanagement | 2767595 | Wenn ein Materialnutzungsdatensatz im Hauptformular geöffnet wird, wird die buchbare Ressource für den Datensatz auf den aktuell angemeldeten Benutzer geändert. |
| Projektplanung und -nachverfolgung | 2790384 | Das Timeout Pending OperationSet ist zu kurz. |
| Projektplanung und -nachverfolgung | 2957840 | Auf der Seite **Aufgaben** in Integrated Project Operations können keine Aufgaben gespeichert und keine Spalten hinzugefügt werden. |
| Ressourcenverwaltung | 2751560 | Inkonsistente bevorzugte Organisationseinheiten im Ressourcenbedarf. |
| Fremdarbeit | 2853245 | Der Abgleich für Ist-Werte der Kreditorenrechnungsposition aktualisiert den Verifizierungsstatus nicht, wenn eine Vertragsposition bereits mit der Kreditorenrechnungsposition verknüpft ist. |
| Fremdarbeit | 2907231 | Die Prozessphase von Kreditorenrechnungen kann nicht fortschreiten. |
| Zeit und Ausgaben | 2867363 | Datensätze fallen nicht aus der Ansicht Abwesenheiten/Urlaub zur Genehmigung heraus, wenn sie zur Genehmigung in die Warteschlange gestellt werden. |
| Zeit und Ausgaben | 2894405 | TESA: Das ungenutzte POC-Verzeichnis verursacht Compliance-Probleme. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [Wissensdatenbankartikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) an.
