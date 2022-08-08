---
title: Was ist neu Juni 2022 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Version vom Juni 2022 von Microsoft Dynamics 365 Project Operations für Szenarien mit und ohne Ressourcenvorrat zur Verfügung stehen.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031330"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu Juni 2022 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Versionen 4.43.0.77 oder 4.43.0.119
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Tabelle zeigt die Dual-write Zuordnungen, die in der Version Project Operations Juni 2022 geändert oder hinzugefügt wurden.

| Entitätszuordnung | Aktualisierte Version | Anmerkungen |
| --- | --- | --- |
| Project Operations-Integrationsprojektanbieter-Rechnungsexportentität (msdyn_projectvendorinvoices) | 1.0.0.1 | Das veraltete Feld wurde außer Betrieb genommen und dem neuen Feld für die Verfolgung des Status von Lieferantenrechnungen zugeordnet. |

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Fremdarbeit | 2708885 | Die Fehlermeldung, die angezeigt wird, wenn ein Benutzer einen Datensatz für den Buchungskopf einer buchbaren Ressource erstellt, in dem keine buchbare Ressource eingetragen ist, wurde behoben. |
| Projektplanung und -nachverfolgung | 2629441 | Die Logik zum Auslösen von Workflows wurde korrigiert, um eine Endlosschleife zu verhindern, wenn Projektaufgaben aktualisiert werden. |
| Zeit und Ausgaben | 2641209 | Zeitbuchungsimporte aus Zuweisungen/Buchungen müssen eine buchbare Ressourcenreferenz beibehalten. |
| Projektplanung und -nachverfolgung | 2651148 | Der Projektdokumentenkopf muss geschützt werden.|
| Projektplanung und -nachverfolgung | 2653145 | Es wurden Validierungen hinzugefügt, um sicherzustellen, dass kein Datensatz erstellt werden kann, der nicht gültige Zeichen in seinem Namen enthält. |
| Zeit und Ausgaben | 2654710 | Die Filterung auf der Seite **Genehmigungen** wurde korrigiert. |
| Preise und Abrechnung | 2667805 | Es wurden Validierungen hinzugefügt, um zu verhindern, dass fakturierte Umsätze erstellt werden, wenn noch keine nicht fakturierten Umsätze vorhanden sind. |
| Preise und Abrechnung | 2668378 | Es wurden Validierungen hinzugefügt, um zu verhindern, dass eine angepasste Dimension für die Preisgestaltung hinzugefügt wird, wenn kein logischer Name und kein Feldname eingegeben wird. |
| Fremdarbeit | 2677485 | Die Zielversion der Dual-write-Zuordnung für Lieferantenrechnungszeilen wurde aktualisiert. |
| Zeit und Ausgaben | 2700428 | Die Genehmigungslogik wurde verbessert, um sicherzustellen, dass andere Genehmigungssätze für das Projekt auch dann verarbeitet werden können, wenn einer der Genehmigungssätze in Systemaufträgen festhängt. |

### <a name="project-management-and-accounting-in-finance"></a>Projektmanagement und -buchhaltung in Finance

Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) an.
