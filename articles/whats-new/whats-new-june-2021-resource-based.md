---
title: Was ist neu Juni 2021 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien
description: Dieses Thema enthält Informationen zu den Qualitätsaktualisierungen, die in der Version Juni 2021 von Project Operations für ressourcen-/nicht vorratsbasierte Szenarien verfügbar sind.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6a40335df89cc6b2bb35e54832140aac6eb9ac6
ms.sourcegitcommit: 03414a74ddf1f2d63043d734ebdee7485f1aadd2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679208"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Was ist neu Juni 2021 - Project Operations für ressourcenbasierte/nicht vorrätige Szenarien

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations in Dynamics 365 Dataverse-Umgebung Version 4.11.0.156 oder 4.11.0.164.
- Projektmanagement und -buchhaltung in Finance and Operations-Apps Umgebungen Version 10.0.19.

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- Möglichkeit zum Löschen von [Projektrechnungsvorschlagszeilen für Anpassungsszenarien](../invoicing/correct-project-invoice-proposals.md).
- Zeilen für Einzelkosten spiegeln die Namen von Unterkategorien in der Spesenabrechnung wider [Neu gestaltete Spesenabrechnungen - neue Funktionen](../expense/expense-reports-reimagined.md#new-features).
- Die Zahlungsmethode ist im neuen Ausgabenbereich verfügbar, wenn eine neue Ausgabe erstellt wird.
- Allgemeine Verfügbarkeit von Projektzeitplan-APIs. Diese neue Funktionalität ermöglicht es Kunden, programmgesteuert Erstellungs-, Aktualisierungs- und Löschvorgänge für Projektaufgaben, Ressourcenzuweisungen, Aufgabenabhängigkeiten und Datensätze von Projektteammitgliedern durchzuführen. Weitere Informationen finden Sie unter [Project-Zeitplan-APIs verwenden, um Vorgänge mit Planungsentitäten auszuführen](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Es gibt keine Updates für Project Operations Dual-Write Zuordnungen in dieser Version. 

Eine aktuelle Liste und Versionen von Project Operations dual-write Zuordnungen finden Sie unter [Versionen von Project Operations dual-write Zuordnungen](../environment/resource-dual-write-maps.md).

Sie sollten immer die neueste Version der Karte in Ihrer Umgebung ausführen und alle zugehörigen Tabellenkarten aktivieren, wenn Sie Ihre Project Operations Dataverse-Lösung und Finance and Operations Apps-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Die aktive Version der Zuordnung können Sie auf der Seite **Dual-write** in der Spalte **Version** sehen. Aktivieren Sie eine neue Version der Zuordnung, indem Sie **Kartenversionen zuordnen** wählen, die neueste Version auswählen und dann die ausgewählte Version speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn ein Problem beim Starten der Karte auftritt, befolgen Sie die Anweisungen im Abschnitt [Fehlende Tabellenspalten bei Zuordnungen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in der Anleitung zur Fehlerbehebung für Dual-Write.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2281417 | Es wurde das Problem behoben, dass die automatische Rechnungserstellung über den Rechnungszeitplan fehlschlug. |
| Preise und Abrechnung | 2287835 | Die Leistung der Rechnungsbestätigung wurde verbessert. |
| Verkaufschancenmanagement | 2222555 | Die Anrechenbarkeit von Materialschätzungen muss korrekt in die Details von Angebotszeilen kopiert werden, wenn **Import aus Projektschätzung** verwendet wird. |
| Verkaufschancenmanagement | 2223427 | Anpassungen sind jetzt für die Aktion **GenerateRetainersFromRetainerScheduleOptions** zugelassen. |
| Verkaufschancenmanagement | 2277528 | Die Berechnung des Meilensteins für Projektvertragszeilen mit mehreren Debitoren wurde korrigiert. |
| Projektplanung und -nachverfolgung | 2226110 | Das zeitweise auftretende Problem mit der Funktion **Anforderung generieren** im Raster **Projektteam** wurde behoben. |
| Projektplanung und -nachverfolgung | 2208109 | Benutzer können kein Projekt in einer Währung mit zugehörigen Aufgaben in einer anderen Währung erstellen. |
| Projektplanung und -nachverfolgung | 2258228 | Die Liste der Felder, die bei **Planung** Entitäten mit der Zeitplan-API geändert werden dürfen, wurde aktualisiert. |
| Projektplanung und -nachverfolgung | 2293989 | Die korrekten Sprach- und Regionaleinstellungen müssen an das **Projektaufgaben** Raster übergeben werden. |
| Ressourcenverwaltung | 2220493 | Das Benutzererlebnis im Raster **Aufgabe** beim schnellen Markieren einer Ressourcenanfrage als abgeschlossen wurde korrigiert. |
| Ressourcenverwaltung | 2330496 | Das Problem mit dem Laden der **Zeitplanungstafel** wurde behoben. (Qualitäts-Update ist in Version 4.11.0.164 verfügbar) |
| Zeit und Ausgaben | 2194431 | Das **Zeiteintrag** Raster muss den Wochenbeginn berücksichtigen, wie er in den **Systemeinstellungen** festgelegt ist. |
| Zeit und Ausgaben | 2277311 | Nachdem Sie den Wert in einer Zelle im Raster **Zeiteintrag** gelöscht haben, bleibt der Cursor im Raster stehen. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formularhinweise** und **Formular einrichten** ist nicht sichtbar unter **Projektmanagement einrichten** in juristischen Entitäten von Finance, die mit Project Operations integriert sind. |
| Projektmanagement und -buchhaltung | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Die Standardbeschreibung für die Mehrwertsteuer ist leer, wenn die **Buchungsart** = **Umsatzsteuer** für Projektrechnungsbelege. |
| Projektmanagement und -buchhaltung | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Es werden doppelte Transaktionen gebucht, wenn die aufgabenbasierte Abrechnung in Dataverse mit Project Operations-Integration verwendet wird. |
| Projektmanagement und -buchhaltung | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Der Prozentsatz der Fertigstellung bei der Umsatzrealisierung ist bei Verwendung der Project Operations-Integration falsch. |
| Projektmanagement und -buchhaltung | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Die Abgrenzung des Umsatzes wird bei einer ausstehenden Kreditor-Rechnung in einem Szenario mit Project Operations Integration verdoppelt. |
| Projektmanagement und -buchhaltung | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Das Integrationsjournal kann nicht gebucht werden, wenn die Regel für das Umsatzprofil auf **Gruppe** festgelegt ist. |
| Projektmanagement und -buchhaltung | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Eine Einkaufsrechnung kann nicht für Projektbestellungen gebucht werden, die Zeilen mit mehreren Maßeinheiten haben. |
| Projektmanagement und -buchhaltung | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Die Standard-Finanzdimension auf einem Projekt kann nicht mit der Daten-Entität Projekte **V2** aktualisiert werden. |
| Projektmanagement und -buchhaltung | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Der Batch-Prozess zum Erstellen von Projektkostenvoranschlägen dauert zu lange. |
| Projektmanagement und -buchhaltung | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Beim Löschen eines Vertrags wird auch die mit dem Debitor verknüpfte Adresse gelöscht. |
| Reisen und Spesen | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Die Workflow-Bedingung für die Genehmigung einer Spesenabrechnung wird nicht korrekt ausgewertet. |
| Reisen und Spesen | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Die Richtlinie für die Spesenabrechnung wertet die Projekt-ID nicht korrekt aus. |
| Reisen und Spesen | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Die Aktion **Bei Intercompany Spesen-Transaktionen auf Personen aufteilen** funktioniert nicht korrekt. |
| Reisen und Spesen | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Zeilenbegründungen der Spesenabrechnung werden versehentlich gelöscht, wenn bestimmte Reiseanträge gelöscht werden. Dies tritt auf, wenn die recID der Spesenabrechnung und des Reiseantrags gleich sind. |
| Reisen und Spesen | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Es gibt ein Problem in der Mobile-App „Spesen“, wenn das Feld **Projekt-ID** in Richtlinien für Spesenabrechnungen erforderlich ist. |
| Reisen und Spesen | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Intercompany-Ausgaben, die mit einem Projekt verbunden sind, können nicht bearbeitet werden. Stattdessen wird die folgende Fehlermeldung angezeigt: „Objektreferenz nicht auf eine Instanz eines Objekts festgelegt.“ |
| Reisen und Spesen | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Nach dem Buchen der Spesenabrechnung wird im untergeordneten Sachkonto die falsche Währung und der falsche Betrag aufgeführt. |
| Reisen und Spesen | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Die Funktion *Löschen von Kreditkartentransaktionen* wurde verbessert.  |
| Reisen und Spesen | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Die in einer Spesenabrechnung enthaltene Mehrwertsteuer wird nicht konsistent berechnet, wenn in einer juristischen Entität eine andere Berichtswährung angegeben ist. |
| Reisen und Spesen | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Die Leistung wird beeinträchtigt, wenn eine neue Bar-Reisekostenabrechnung hinzugefügt wird. |
| Reisen und Spesen | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Die Regeln der Richtlinie für Ausgaben werden bei einer Spesenabrechnung nicht ausgelöst. |
| Reisen und Spesen | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Beim Hochladen einer neuen gemeinsamen Kategorie unter Verwendung des Data Management Frameworks werden alle Unterkategorien für alle gemeinsamen Kategorien entfernt. |
| Reisen und Spesen | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Wenn Sie eine Spesenzeile erstellen und dann eine Kategorie auswählen, wird die folgende Fehlermeldung angezeigt: „Die Kombination aus Mehrwertsteuergruppe DOM und Element Mehrwertsteuergruppe STD ist nicht gültig.“ |
| Reisen und Spesen | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Es gibt Synchronisationsprobleme in der mobilen Anwendung Spesen. |
