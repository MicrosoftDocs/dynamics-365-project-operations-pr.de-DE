---
title: Neuigkeiten April 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom April 2021 für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen verfügbar sind.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 07622ed798fd8d70e0ce5cc42297bd5056402474
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589103"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten April 2021 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations in Dataverse, Umgebungsversion 4.9.0.221
- Projektmanagement und -buchhaltung in Dynamics 365 Finance-Umgebungsversion 10.0.17

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- Nicht vorrätige Materialien für Projekte. Die Hauptfunktionen umfassen Folgendes:
  - Schätzung und Preisgestaltung von nicht vorrätigen Materialien während des Verkaufszyklus für ein Projekt. Weitere Informationen finden Sie unter [Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Verfolgung der Verwendung nicht vorrätiger Materialien während der Projektabwicklung. Weitere Informationen finden Sie unter [Materialverbrauch für Projekte und Projektaufgaben erfassen](../material/material-usage-log.md).
  - Fakturierung gebrauchter nicht vorrätiger Materialkosten. Weitere Informationen finden Sie unter [Abrechnungsstau verwalten](../proforma-invoicing/manage-billing-backlog.md).
  - Informationen zum Konfigurieren dieser Funktion finden Sie unter [Konfigurieren nicht vorrätiger Materialien und ausstehender Lieferantenrechnungen](../procurement/configure-materials-nonstocked.md)
- Aufgabenbasierte Abrechnung: Es wurde die Möglichkeit hinzugefügt, Projektaufgaben mit Projektvertragszeilen zu verknüpfen, wodurch diese der gleichen Abrechnungsmethode, Rechnungshäufigkeit und Kunden wie in der Vertragszeile unterliegen. Diese Zuordnung stellt eine genaue Rechnungsstellung, Buchhaltung, Umsatzvorkalkulation und Erfassung sicher, damit gemäß dieser Einrichtung für Projektaufgaben gearbeitet werden kann.
- Neue APIs in Dynamics 365 Dataverse ermöglichen das Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten**. Weitere informationen finden Sie unter [Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Liste zeigt die Dual-Write-Maps, die in der Version Project Operations April 2021 geändert oder hinzugefügt wurden.

| **Entitätszuordnung** | **Aktualisierte Version** | **Kommentare** |
| --- | --- | --- |
| Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals) | 1.0.0.14 | Karte geändert, um Materialprojekt-Istwerte zu synchronisieren. |
| Project Operations-Integrationsentität für Ausgabenschätzungen (msdyn\_estimateslines) | 1.0.0.2 | Synchronisierung von Projektvertragszeilen zu Finanz- und Betriebs-Apps für aufgabenbasierte Abrechnungsunterstützung hinzugefügt. |
| Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments) | 1.0.0.5 | Synchronisierung von Projektvertragszeilen zu Finanz- und Betriebs-Apps für aufgabenbasierte Abrechnungsunterstützung hinzugefügt. |
| Project Operations-Integrationstabelle für Materialschätzungen (msdyn\_estimatelines) | 1.0.0.0 | Neue Tabellenzuordnung zum Synchronisieren von Materialschätzungen von Dataverse zur Finanz- und Betriebs-Apps |
| Project Operations-Integrationsprojektanbieter-Rechnungsexportentität (msdyn\_projectvendorinvoices) | 1.0.0.0 | Neue Tabellenzuordnung zum Synchronisieren von Kreditorenrechnungskopfzeilen von der Finanz- und Betriebs-Apps zu Dataverse. |
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Neue Tabellenzuordnung zum Synchronisieren von Kreditorenrechnungspositionen von der Finanz- und Betriebs-Apps zu Dataverse. |

Sie sollten immer die neueste Version der Map in Ihrer Umgebung ausführen und alle zugehörigen Tabellen-Zuordnungen aktivieren, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance and Operations-Lösungsversion aktualisieren. Bestimmte Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Karte in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine sofort einsatzbereite Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen unter [Fehlende Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) in der Anleitung zur Fehlerbehebung bei Dual Write.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations in Dynamics 365 Dataverse

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2124532 | Die **Rechnung berichtigen**-Schaltfläche wird auf einer Proforma-Rechnung angezeigt, wenn der Einbehaltungsbetrag oder der angewendete Einbehaltungsbetrag auf der Originalrechnung vorhanden ist. Die Schaltfläche wird nur für Umgebungen mit Finance Version 10.0.19 oder höher angezeigt. |
| Preise und Abrechnung | 2224568 | Logik hinzugefügt, um Anpassungen zu ermöglichen, bei denen das Rechnungsbestätigungs-Plug-In aufgerufen wird. |
| Preise und Abrechnung | 2101098 | Die Logik der Standardfelder für die Proforma-Rechnung wurde verbessert: **Rechnungsadresse**, **Name für Rechnungsadresse** und **Zahlungsbedingungen** werden jetzt standardmäßig aus dem entsprechenden Projektvertrags-Kundendatensatz entnommen. |
| Preise und Abrechnung | 2021413 | Die Felder **Tatsächliche Kosten** und **Vertrieb** in der **Aufgabe**-Entität wurden aktualisiert, um Verkaufswerte aus nicht in Rechnung gestellten und in Rechnung gestellten Ausgaben für Aufgaben einzubeziehen. |
| Preise und Abrechnung | 2182110 | Beim Kopieren eines Projektvertrags wird die Vertragszeilen-ID im Zielprojektvertrag neu generiert, um sicherzustellen, dass sie eindeutig ist. |
| Verkaufschancenmanagement | 2186741 | Es wurden Validierungen hinzugefügt, um sicherzustellen, dass das Feld **Ursprung** und **Transaktionstyp** nicht auf vorhandenen Angebotszeilendetails aktualisiert werden kann. |
| Verkaufschancenmanagement | 2191353 | Meilensteine dürfen nicht auf einer zeitlichen und materiellen Vertragszeile erstellt werden. |
| Verkaufschancenmanagement | 2216956 | Probleme mit **Preise aktualisieren** behoben. |
| Planung und Nachverfolgung | 2182979 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass die Kostenvorkalkulationszeilen aus dem ursprünglichen Projekt kopiert werden. |
| Planung und Nachverfolgung | 2184144 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass der Ressourcenpositionsname aus dem ursprünglichen Projekt kopiert wird. |
| Planung und Nachverfolgung | 2184799 | Projektkopie: Das Steuerelement wurde verbessert, um sicherzustellen, dass das geschätzte Startdatum während des Kopiervorgangs nicht geändert werden kann. |
| Planung und Nachverfolgung | 2185134 | Projektkopie: Das geschätzte Startdatum des Zielprojekts wird auf das heutige Datum festgelegt. |
| Planung und Nachverfolgung | 2196373 | Projektkopie: Stellen Sie sicher, dass die Datensätze des Projektmanagers und der Teammitglieder nicht im Projektteam dupliziert werden. |
| Planung und Nachverfolgung | 2211833 | Projektkopie: Ressourcenzuweisungen werden von der Quellprojektaufgabe in das Zielprojekt kopiert. |
| Planung und Nachverfolgung | 2186541 | Probleme im **Schätzungen**-Raster bei der Gruppierung nach Ressourcen behoben. |
| Planung und Nachverfolgung | 2166906 | Die Transaktionskategorie einer Aufgabe muss in die **Ressourcenzuweisung**-Entität kopiert werden. |
| Ressourcenverwaltung | 2125362 | Probleme beim Erstellen eines generischen Teammitglieds mithilfe einer stundenbasierten Zuordnungsmethode behoben. |
| Zeit und Ausgaben | 2113603 | Das Anpassungsproblem beim Entfernen von Attributen von der **Zeiteintrag**-Seite wurde behoben. Das System prüft nun mithilfe eines Skripts, ob das Attribut auf der Seite vorhanden ist, bevor es darauf zugreift. |
| Zeit und Ausgaben | 2204377 | Kopierte Arbeitszeittabellen müssen bei der Auswahl von **Woche kopieren** während der Zeiteingabe automatisch angezeigt werden. |
| Zeit und Ausgaben | 2209059 | **Status**-Feld kann für Dynamics 365 Field Service-Zeiteinträge bearbeitet werden. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Die Eliminierung der umgekehrten Schätzung funktioniert im Abschnitt **Periodisch**.  |
| Projektmanagement und -buchhaltung | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Die **Bilanzierungsanpassung**-Funktion erstellt ein Problem mit Sachkonten, die **Manuelle Eingabe nicht zulassen** ausgewählt haben. |
| Projektmanagement und -buchhaltung | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Geschäftslogik hinzugefügt, um Korrekturrechnungen einschließlich des Einbehaltungsbetrags oder des angewendeten Einbehaltungsbetrags zu verarbeiten. |
| Projektmanagement und -buchhaltung | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP – Buchung des Verkaufswerts in der konzerninternen Projektrechnung wählt ein unerwartetes Konto aus. |
| Projektmanagement und -buchhaltung | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Wenn Sie mit Retainern in Project Operations arbeiten, führt das Ändern des Standardprojekts im Vertrag nach Rechnungsstellung der Vorauszahlungen zu Problemen mit eingehenden Abzügen. |
| Projektmanagement und -buchhaltung | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Wenn Sie in Project Operations ein Projekt aus einem Vertrag entfernen, sollte das Standardprojekt des Vertrags bei Bedarf zurückgesetzt werden. |
| Projektmanagement und -buchhaltung | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | In Project Operations werden die falschen Ausgabenzeilen in der **Zeile hinzufügen**-Liste auf der Intercompany-Rechnung angezeigt. |
| Projektmanagement und -buchhaltung | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | In Project Operations ist die **Kaufvertrag**-Seite in juristischen Personen des Finanzsektors, die in Project Operations integriert sind, nicht sichtbar. |
| Projektmanagement und -buchhaltung | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Aufgrund eines Dataverse-Integrationsfehlers können Sie ein Angebot nicht in Won in Project Operations konvertieren. |
| Projektmanagement und -buchhaltung | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** kann die Rechnungsadresse der Finanzierungsquelle von einem anderen Kunden festlegen.  |
| Projektmanagement und -buchhaltung | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | In Project Operations werden keine Dimensionen ausgewählt, wenn Sie eine Buchungsrechnung für eine Transaktion erstellen. |
| Reisekosten und Spesen | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Der Vorauszahlungssaldo wird für eine Spesenabrechnung nicht aktualisiert, wenn er zeilenweise genehmigt und gebucht wird. |
| Reisekosten und Ausgaben | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Steuern für detaillierte konzerninterne Spesenabrechnungen werden nicht korrekt berechnet. |
| Reisekosten und Ausgaben | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Zusätzliche Felder, die sich auf Projekte beziehen, werden auf der überarbeiteten Seite **Konzerninterne Spesenabrechnungen** angezeigt. |
| Reisekosten und Ausgaben | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Auf den Kopfzeilenbelegen der Spesenabrechnungen tritt eine falsche Fehlermeldung auf. |
| Reisekosten und Ausgaben | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Eine Spesenabrechnung wird in einem konzerninternen Szenario falsch gebucht, wenn die Umsatzsteuer an die juristische Person des Ziels gebucht wird. |
| Reisekosten und Ausgaben | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Die Übermittlungstermine für Berichte werden nicht auf genehmigten Spesenabrechnungen gedruckt. |
| Reisekosten und Ausgaben | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Die Felder **Datum der Genehmigung** und **Datum abgelehnt** werden nicht ausgefüllt, nachdem eine Ausgabe genehmigt wurde. |
| Reisekosten und Ausgaben | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Eine für einen Mitarbeiter erstellte Reiseanforderung kann für die Spesenabrechnung eines anderen Mitarbeiters verwendet werden. |
| Reisekosten und Ausgaben | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Ausgabenkategorien werden beim Hinzufügen einer neuen Ausgabenzeile gesperrt. |
| Reisekosten und Ausgaben | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Das Auflisten bereits geteilter Spesenabrechnungszeilen führt zu einer unvollständigen Buchung des Gutscheins „Kreditorenbuchhaltung\Hauptbuch“ und zu einer Unterbrechung des Buchhaltungsquellen-Explorers, da **TRVEXPTRANS.SOURCEDOCUMENTLINE** dupliziert wird. |
| Reisekosten und Ausgaben | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Die Reiseanforderungsrichtlinie funktioniert nicht wie erwartet. |
| Reisekosten und Ausgaben | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Der Name des Zuliefererkontos wird bei gebuchten Projekttransaktionen für Spesenabrechnungen nicht angezeigt. |
| Reisekosten und Ausgaben | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | In Project Operations können Sie keine Zeit mit einer Aufgabe für ein Intercompany-Projekt genehmigen. |
| Reisekosten und Ausgaben | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | In der Kategorie „Vorauszahlungsrendite“ werden die Vorauszahlungssalden bei der Buchung nicht aktualisiert. |
| Reisekosten und Ausgaben | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Der Verkaufspreis wird in Spesenabrechnungen falsch berechnet, die mit importierten Kreditkartentransaktionen in einer Fremdwährung erstellt wurden und einem Projekt zugeordnet sind. |
| Reisekosten und Ausgaben | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Rollback der **TrvRequisitionLine**-Datenentität und des zugehörigen eindeutigen Index. |
| Reisekosten und Ausgaben | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Instrumentierung zur **SOURCEDOCUMENTLINE**-Generierung hinzugefügt. |
| Reisekosten und Ausgaben | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Das falsche untergeordnete Sachkonto wird in einem konzerninternen Szenario angezeigt, wenn die Umsatzsteuer an die juristische Person des Ziels gebucht wird. |
| Reisekosten und Ausgaben | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | In Project Operations werden Kostenvoranschläge nicht aus der Finanzabteilung gelöscht, wenn sie aus Dataverse gelöscht werden. |
| Reisekosten und Ausgaben | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Wenn eine Ausgabenkategorie eine Nicht-Projektkategorie ist, werden die finanziellen Dimensionen auf der **Kosten**-Seite nicht in die Spesenabrechnung kopiert. |
