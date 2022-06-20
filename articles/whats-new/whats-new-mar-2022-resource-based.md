---
title: Neuerungen im März 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieser Artikel informiert Sie über die Qualitätsupdates, die in der Version von Project Operations vom März 2022 für ressourcenbasierte/nicht vorrätige Szenarien zur Verfügung stehen.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910905"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuerungen im März 2022 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

*Gilt für: Project Operations für ressourcen-/nicht vorratsbasierte Szenarien*

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Version 4.30.0.99
- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.25

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Tagegelder werden jetzt im neuen und überarbeiteten modernen Arbeitsbereich für Ausgaben unterstützt. Unternehmen, die Tagessätze verwenden, können diese Funktion aktivieren, um Benutzern eine einfache Möglichkeit zu geben, ihre Tagessätze einzureichen und sich erstatten zu lassen. Weitere Informationen finden Sie unter [Tagesausgaben](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations – Duales Schreiben-Kartenupdates

Die folgende Liste zeigt die Zuordnungen für duales Schreiben, die in der Project Operations-Version vom März 2022 geändert oder hinzugefügt wurden.

| **Entitätszuordnung** | **Aktualisierte Version** | **Anmerkungen** |
| --- | --- | --- |
| Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität msdyn\_projectvendorinvoicelines | 1.0.0.3 | Die Mappings wurden aktualisiert, um sie an der Entität der Kreditorenrechnungsposition in Dataverse auszurichten. <br>Mapping-Version 1.0.0.4 nicht aktivieren. Es wird in Kombination mit der Finance-Umgebungsversion 10.0.26 im nächsten monatlichen Update einsatzbereit sein. |

Führen Sie immer die neueste Version der Map in Ihrer Umgebung aus und aktivieren Sie alle zugehörigen Tabellen-Zuordnungen, wenn Sie Ihre Project Operations Dataverse-Lösung und die Finance-Lösungsversion aktualisieren. Einige Funktionen und Fähigkeiten funktionieren möglicherweise nicht richtig, wenn die neueste Version der Karte nicht aktiviert ist. Sie können die aktive Version der Zuordnung in der Spalte **Version** auf der Seite **Dual-Write** anzeigen. Sie können eine neue Version der Zuordnung aktivieren, indem Sie **Tabellenzuordnungsversionen** auswählen und dann die aktuellste Version auswählen und speichern. Wenn Sie eine vorkonfigurierte Tabellenzuordnung angepasst haben, wenden Sie die Änderungen erneut an. Weitere Informationen finden Sie unter [Application Lifecycle Management](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Wenn beim Starten der Karte ein Problem auftritt, befolgen Sie die Anweisungen im Abschnitt [Problem mit fehlenden Tabellenspalten auf Karten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) des Handbuchs zur Fehlerbehebung für duales Schreiben.

## <a name="quality-updates"></a>Qualitätsupdates

### <a name="project-operations-on-dataverse"></a>Project Operations in Dataverse

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Zeit und Ausgaben | 2388011 | Anzeigen von Ablehnungskommentaren für Einreicher von Zeiteinträgen während der Massengenehmigung. |
| Projektplanung und -nachverfolgung | 2495294 | Projektdetails dürfen auf der **Aufgabendetails**-Seite nicht editierbar sein. |
| Preise und Abrechnung | 2499605 | Vertragsmeilensteine, die aus Angebotsmeilensteinen erstellt werden, sind fälschlicherweise als schreibgeschützt gekennzeichnet. |
| Projektplanung und -nachverfolgung | 2506050 | Der Vorgangssatz bleibt eine Stunde lang ausstehend, wenn keine Änderung zu speichern ist. Der Satz wird dann fälschlicherweise als **Fehlgeschlagen** markiert, wobei er sofort abgeschlossen werden sollte. |
| Preise und Abrechnung | 2507401 | Standardvertragseinheiten werden aufgrund von falschem Zwischenspeichern in Projekten falsch eingegeben. |
| Preise und Abrechnung | 2541660 | **Validierung der Vertriebsauftragserstellung** beim dualen Schreiben sollten nur für projektbasierte Aufträge verwendet werden. |
| Preise und Abrechnung | 2552745 | Die Steuer wird nicht zwischen Kunden aufgeteilt, die Regeln für die getrennte Abrechnung eingerichtet haben. |
| Preise und Abrechnung | 2558859 | Verbesserte Fehlermeldungen beim Einrichten von Preisdimensionen. |
| Preise und Abrechnung | 2558933 | **Import aus Project Estimates** scheitert, wenn **msdyn\_project** als Preisdimension hinzugefügt wird. |
| Preise und Abrechnung | 2559101 | Das Löschen von Projektparametern wird nicht blockiert und verursacht Probleme. |
| Verkaufschancenmanagement | 2570390 | Das Plug-In für duales Schreiben erzwingt bei Angeboten, Aufträgen und Verkaufschancen den Kontotyp **Kunde**, auch wenn dieser Kontotyp nicht korrekt ist. |
| Preise und Abrechnung | 2586097 | Geteilte abgerechnete Kosten-Ist-Werte werden nicht storniert, wenn ein Projekt aus einer Projektvertragsposition entfernt wird. |
| Preise und Abrechnung | 2589619 | Die Steuer auf manuell eingetragenes Material wird auf die nicht fakturierten Verkaufs-Ist-Werte und die Rechnung übertragen. |
| Verkaufschancenmanagement | 2594015 | Ein Angebot kann für Kunden mit **Net60**-Zahlungsbedingungen nicht als gewonnen abgeschlossen werden. |
| Projektplanung und -nachverfolgung | 2595841 | In Project for the Web erhalten Benutzer eine Fehlermeldung zu einem fehlenden **msdyn\_actualstart**, wenn sie eine neue Ressourcenanforderung erstellen. |
| Zeit und Ausgaben | 2602511 | Das **Zurückgewiesen von**-Feld für Zeiteinträge zeigt als Ablehner **System** anstelle eines benannten Benutzers. |
| Zeit und Ausgaben | 2602528 | Ein Projektgenehmiger kann Zeit für Projekte genehmigen, in denen er nicht als Genehmiger aufgeführt ist. |
| Preise und Abrechnung | 2608550 | Eine Korrekturrechnung kann auch dann bestätigt werden, wenn gegenüber dem Original keine Änderungen vorgenommen wurden. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektmanagement und -buchhaltung bei Dynamics 365 Finance

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Projektmanagement und -buchhaltung | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Es gibt eine Diskrepanz zwischen Finance und Project Operations in der zulässigen Länge des **Kategorie-ID**-Felds. |
| Projektmanagement und -buchhaltung | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Festpreisprojekte können nicht eliminiert werden, wenn das **Akonto-Rechnungsstellung**-Feld auf **Gewinn- und Verlust** eingestellt ist und das **Abgeschlossener Prozentsatz**-Prinzip verwendet wird. |
| Projektmanagement und -buchhaltung | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Eine falsche Standard-Mehrwertsteuergruppe wird aus der Projekteinrichtung in Ausgabenpositionen in der Project Operations-Integrationserfassung eingegeben. |
| Projektmanagement und -buchhaltung | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Sie können die Kopfdimensionen des Projektrechnungsvorschlags in einer integrierten Bereitstellung mit Project Operations nicht bearbeiten. |
| Projektmanagement und -buchhaltung | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Intercompany-Lieferantenrechnungen dürfen nicht in Dataverse integriert werden. |
| Projektmanagement und -buchhaltung | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Die Währung der Kundensalden und die Berichtswährung stimmen nicht überein. |
| Projektmanagement und -buchhaltung | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Sie können eine Projektrechnung auch dann buchen, wenn der Kunde für alle Rechnungen zurückgestellt ist. |
| Projektmanagement und -buchhaltung | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Die Schaltfläche **Alle Zeilen löschen** fehlt bei Projektrechnungsvorschlägen mit den Ansichten **Header** und **Positionen**. |
| Projektmanagement und -buchhaltung | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Beim Buchen einer Kreditorenrechnung tritt folgender Fehler auf: „Das Buchungsdatum der Rechnung muss im selben Geschäftsjahr liegen wie die zugehörige Bestellung. Führen Sie den Jahresendprozess für Bestellungen aus oder ändern Sie das Datum auf das aktuelle Geschäftsjahr." |
| Reisekosten und Ausgaben | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Die zugesagten Kosten für ein Projekt werden nicht freigegeben, nachdem die zugesagten Kosten der Reiseanforderung freigegeben wurden. |
| Reisekosten und Ausgaben | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Der folgende Fehler tritt auf, wenn Sie eine Spesenabrechnung einreichen: "Stapelüberwachung: Das Unternehmen existiert nicht". |
| Reisekosten und Ausgaben | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Die Standard-**Projekt-ID** wird nicht auf Spesenabrechnungen eingetragen, wenn der **Aktivität für Erfassung erforderlich**-Parameter im Projekt ausgewählt ist. |
| Reisekosten und Ausgaben | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Die Schaltfläche **Ausgaben buchen** funktioniert in Project Operations für Ressourcen-/nicht gelagerte Szenarien nicht richtig. |
| Reisekosten und Ausgaben | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Es gibt ein Problem mit **Satz pro Kilometer** für eine Kilometerkostenabrechnung, die Passagiere enthält. |
| Reisekosten und Ausgaben | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Ausgabenkilometersätze für Mitarbeiter werden nicht korrekt summiert, wenn zwei verschiedene Fahrzeugtypen in der **Kilometersatzstufen**-Ausgabenkategorie verwendet werden. |
| Reisekosten und Ausgaben | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Die Suche nach dem **Projekt**-Feld in einer Reiseanforderungsposition gibt nicht die richtige Projektliste zurück. |
| Reisekosten und Ausgaben | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Kilometerstand im Bewertung** zeigt eine Warnung auf Spesenabrechnungen. |
| Reisekosten und Ausgaben | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Der OCR-Dienst (Optical Character Recognition) für Belege funktioniert aufgrund eines Problems mit der URL des OCR-Dienstes für Ausgaben nicht. |
| Reisekosten und Ausgaben | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Wenn die **Möglichkeit, wiederkehrende Ausgaben schnell aufzuschlüsseln**-Funktion aktiviert ist, ändern sich die Beträge in Einzelpostenzeilen in Spesenabrechnungen jedes Mal, wenn die **Aufschlüsseln**-Seite geöffnet wird. |
| Reisekosten und Ausgaben | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Sie können eine Spesenabrechnung nicht löschen, wenn die vorläufige Liste mehr als eine genehmigende Person hat. |

## <a name="removed-and-deprecated-features"></a>Entfernte und veraltete Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Project Operations](removed-depreciated-features-project.md) beschreibt Funktionen, die für Dynamics 365 Project Operations entfernt oder außer Betrieb genommen wurden.

- Eine entfernte Funktion ist im Produkt nicht mehr verfügbar.
- Eine veraltete Funktion wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Eine Ankündigung, dass eine Funktion veraltet ist, erscheint im Artikel [Entfernte oder veraltete Funktionen in Project Operations](removed-depreciated-features-project.md) 12 Monate bevor eine Funktion aus dem Produkt entfernt wird.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Zeit für die Entfernung weniger als 12 Monate. In der Regel handelt es sich bei diesen Änderungen um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.
