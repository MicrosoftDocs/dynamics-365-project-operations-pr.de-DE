---
title: Neuigkeiten Mai 2021 – Project Operations für Ressourcen basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel informiert über die Qualitätsupdates, die in der Version von Project Operations vom Mai 2021 für ressourcenbasierte/nicht vorrätige Szenarien zur Verfügung stehen.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930409"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten Mai 2021 – Project Operations für Ressourcen basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel bezieht sich auf die folgenden Dynamics 365 Project Operations-Komponenten und Versionen:

- Project Operations on Dynamics 365 Dataverse Umgebungsversion 4.10.0.186
- Projektmanagement und Buchhaltung in Finanz- und Betriebs-App-Umgebungen Version 10.0.18

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- [Planungsmodi](../project-management/scheduling-modes.md): Projektmanager können festlegen, ob ein Projekt im Planungsmodus feste Dauer, feste Arbeit oder feste Einheiten verwaltet werden soll.
- [Richten Sie den Kilometerstand mithilfe von Kilometertarifstufen ein](../expense/set-up-mileage.md): Meilentarifstufen für Mitarbeiterkostenabrechnungen aktualisieren.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Liste zeigt die Zuordnungen für duales Schreiben, die in der Version Project Operations Mai 2021 geändert oder hinzugefügt wurden.

| Entitätszuordnung | Aktualisierte Version | Kommentare |
| --- | --- | --- |
| Projektfinanzierungsquelle (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synchronisierung der Zahlungsbedingungen des Projektvertragskunden. |
| Projektrechnungsvorschläge V2 (Rechnungen) | 1.0.0.3 | Zahlungsbedingungen für Proforma-Rechnungen synchronisieren. |
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Qualitätsupdates |
| Projekte V2 (msdyn\_projects) | 1.0.0.2 | Qualitätsupdates |

Aktivieren Sie immer die neueste Version der Map in Ihrer Umgebung ausführen und alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finanz- und Betriebs-Apps-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Karte in der Spalte **Version** auf der Seite **Duales Schreiben** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen unter [Fehlende Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in der Anleitung zur Fehlerbehebung bei Dualem Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2227635 | Die Werte in den Standardfeldern **Einheitengruppe** und **Einheit** aus dem Produkt im Raster **Materialschätzungen**. |
| Preise und Abrechnung | 2234127 | Das Feld **Aufgaben-ID** integriert sich jetzt korrekt in die Dataverse Projekt-Istwerte, wenn eine Kreditorenrechnung gebucht wird. |
| Preise und Abrechnung | 2235564 | Durch das Speichern der Erfassungsposition wird sichergestellt, dass die im Journalzeileneintrag angezeigte Währung nach dem Speichern mit der Standardwährung der Zeile übereinstimmt. |
| Preise und Abrechnung | 2246671 | Wenn Sie eine Transaktion während der Fakturierung als gebührenfrei festlegen, wird der ursprüngliche Datensatz für nicht in Rechnung gestellte Verkäufe rückgängig gemacht und ein neuer Datensatz für nicht in Rechnung gestellte Verkäufe als nicht gebührenpflichtig erstellt. |
| Preise und Abrechnung | 2264042 | Eine gültige Rechnungskorrektur darf nicht gesperrt werden, wenn ein in der Umgebung ungültiges Rechnungskorrekturdetail vorhanden ist. |
| Preise und Abrechnung | 2146367 | Die Zuordnung duales Schreiben des Projektrechnungskopfes wird um Zahlungsbedingungen erweitert. |
| Verkaufschancenmanagement | 2086888 | Fügen Sie keine Rollen und Kategorien hinzu, die deaktiviert sind, bevor Sie ein Angebot zu kostenpflichtigen Rollen und Kategorien eines neu kopierten Angebots kopieren. |
| Verkaufschancenmanagement | 2234376 | Schreibgeschützte Felder sind im Raster **Materialschätzungen** ausgegraut. |
| Verkaufschancenmanagement | 2238337 | Ein auf einem Kontakt basierendes Angebot kann gespeichert werden, auch wenn es keiner Projektpreisliste zugeordnet ist. |
| Verkaufschancenmanagement | 2239810 | Das Schließen eines Angebots als verloren schließt auch das zugehörige Projekt und storniert alle Buchungen. |
| Projektplanung und -nachverfolgung | 2099559 | Zusätzliche Validierungen für den Systemzustand vor dem Raster **Projektaufgaben** öffnet sich. |
| Projektplanung und -nachverfolgung | 2178987 | Ein vorübergehender Fehler wurde behoben, der bei der Auswahl **Nächste Phase** auf der Seite **Projekt** auftritt. |
| Ressourcenverwaltung | 2224817 | Die Funktion zum Erweitern von Buchungen verwendet standardmäßig den korrekten Buchungsstatus. |
| Zeiteintrag | 2202476 | Die Seite **Zeiteingabe** verwendet jetzt die Reaktionsrastersteuerung und behebt Probleme wie Rasterfehlausrichtung. |
| Zeiteintrag | 2223377 | Die Zeiteingabe ist vor dem Abschnitt **verbunden** auf der Seite **Buchbare Ressource** ausgeblendet, um Verwechslungen mit der Benutzerfreundlichkeit zu vermeiden. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations für ressourcenbasierte Szenarien: Können Aufgrund eines Integrationsfehlers nicht in gewonnen konvertiert werden. |
| Projektmanagement und -buchhaltung | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Es tritt eine Fehlermeldung auf, wenn Sie versuchen, einer Projekt-ID eine Vertragszeile zuzuordnen, da überprüft wird, ob sich Vertragszeilen und Transaktionstypen überschneiden. |
| Projektmanagement und -buchhaltung | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** legt die Rechnungsadresse der Finanzierungsquelle von einem anderen Kunden fest. |
| Reisekosten und Ausgaben | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Es kann ein Buchungsfehler im Zusammenhang mit der Meileneinstellung auftreten. |
| Reisekosten und Ausgaben | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | **Auf persönlich aufteilen** funktioniert nicht für Ausgabebuchungen in Fremdwährung. |
| Reisekosten und Ausgaben | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Das Dropdown-Menü Ausgabenkategorie zeigt falsche Kategorien an, unabhängig davon, ob Delegiert als Ressource eingerichtet ist. |
| Reisekosten und Ausgaben | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Sie können eine konzerninterne Spesenabrechnung aufgrund eines Fehlers bei der **Ressourcen-/Kategorieüberprüfung** nicht speichern. |
| Reisekosten und Ausgaben | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Die falsche Berechnung der Meilensätze in der Spesenabrechnung weist Trennlinien auf. |
| Reisekosten und Ausgaben | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Sie können keine konzerninterne Spesenabrechnung buchen, wenn die Umsatzsteuer enthalten ist und der Gegenkontotyp für die Zahlungsmethode **Worker** lautet. |
| Reisekosten und Ausgaben | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Rollback der **TrvRequisitionLine**-Datenentität und des eindeutigen Indexes sind zugehörig. |
| Reisekosten und Ausgaben | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Der Spesenbericht unterstützt das Erstellen und Aktualisieren von Quelldokumentzeilen. |
| Reisekosten und Ausgaben | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Ein falsch untergeordnete Sachkonto wird in einem konzerninternen Szenario angezeigt, wenn die Umsatzsteuer an die juristische Person des Ziels gebucht wird. |
| Reisekosten und Ausgaben | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Die Ausgabenvoranschläge werden nicht aus Finance gelöscht, wenn sie aus Dataverse gelöscht werden. |
| Reisekosten und Ausgaben | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Wenn eine Ausgabenkategorie eine Nicht-Projektkategorie ist, werden die finanziellen Dimensionen auf der Seite **Spesen** nicht in die Spesenabrechnung kopiert. |
