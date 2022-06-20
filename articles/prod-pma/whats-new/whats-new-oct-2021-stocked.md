---
title: Neuigkeiten oder Änderungen für Oktober 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung
description: Dieser Artikel informiert Sie über die Qualitätsupdates, die in der Version von Project Operations vom Oktober 2021 für lager-/produktionsbasierte Szenarien verfügbar sind.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: ba88268e74269c774b41396a8b6574e5bab477b9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933675"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Neuigkeiten oder Änderungen für Oktober 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung

_**Gilt für:** Project Operations für lager-/produktionsbasierte Szenarien_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.22
 
## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
|--------------|------------------|----------------|
| Projektmanagement und -buchhaltung | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | In Arbeit befindliche Projekte (WIP) und aufgelaufene Umsatzbeträge werden nicht korrekt storniert, wenn eine Intercompany-Kundenrechnung gebucht wird. |
| Projektmanagement und -buchhaltung | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Die Funktion **Projektabschluss verhindern, wenn offene Transaktionen vorhanden sind** funktioniert nicht. |
| Projektmanagement und -buchhaltung | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Die Abrechnungsklassifizierung auf einer Freitextrechnung füllt Dimensionen aus Projekten nicht automatisch aus, wenn diese Funktion aktiviert ist. |
| Projektmanagement und -buchhaltung | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Nicht-Intercompany-Szenarios, in Arbeit befindliche Projekte (WIP) und aufgelaufene Umsatzbeträge werden nicht korrekt storniert, wenn die Projektrechnung gebucht wird. |
| Projektmanagement und -buchhaltung | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debit- und Kreditwerte werden geändert, wenn das Microsoft Excel-Add-In mit der Projektausgabenerfassung verwendet und das Feld **Gegenkontotyp** auf **Projekt** festgelegt wird. |
| Projektmanagement und -buchhaltung | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Der in Projekttransaktionen gebuchte Betrag ist in einer Projektbestellung zu hoch ausgewiesen, die Lagerartikel und nicht abzugsfähige Steuerbeträge enthält, wenn **UseTax** gekennzeichnet ist. |
| Projektmanagement und -buchhaltung | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Das System teilt den Betrag zwischen den Projektgewinn- und -verlustberichten und den Projekt-WIP-Berichten auf. |
| Projektmanagement und -buchhaltung | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Der verfügbare Lagerbestand ist falsch, nachdem eine teilweise zurückgegebene Artikelanforderung angepasst wurde. |
| Projektmanagement und -buchhaltung | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressourcennamen werden in Project Operations dupliziert, wenn sie in Microsoft Project bearbeitet werden. |
| Projektmanagement und -buchhaltung | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Intercompany-Ausgabenberichte, die ausstehende Intercompany-Zuliefererrechnungskosten aufweisen, werden zuerst auf dem Buchungstyp **Projekt-WIP-Kosten** gebucht. Bei der Bearbeitung werden jedoch die kalkulationsbezogenen Kosten auf den Buchungstyp **Projektkosten** statt des erwarteten Buchungstyps **Intercompany-Kosten** gebucht. |
| Projektmanagement und -buchhaltung | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Die Ergebnisse der Lieferantenbindung in Projektausgabentransaktionen werden nicht angezeigt. |
| Projektmanagement und -buchhaltung | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Die Arbeitszeittabelle muss den Transaktionsbetrag in der Transaktionswährung bei allen Buchungsverteilungen und allgemeinen Erfassungszuteilungseinträgen auf eine bestimmte Anzahl von Dezimalstellen runden. |
| Projektmanagement und -buchhaltung | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Die Mengen der Projektartikelanforderungen werden automatisch aktualisiert, wenn die Planaufträge bestätigt werden. |
| Projektmanagement und -buchhaltung | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Die Belegnummer, der Zulieferersaldo der Transaktionsart und die Firmennummer können auf der Vorauszahlungsrechnung einer Bestellung nicht storniert werden. |
| Projektmanagement und -buchhaltung | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Die Intercompany-Zuliefererrechnung ist fehlerhaft, wenn die Zuliefererrechnungsintegration aktiviert ist. |
| Projektmanagement und -buchhaltung | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Wenn Sie eine Projektausgabenerfassung erstellen, wird der Kostenbetrag im Feld **Guthaben** angezeigt. |
| Projektmanagement und -buchhaltung | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Die Zahlungsbedingungen auf Projektrechnungen funktionieren nicht wie erwartet. |
| Projektmanagement und -buchhaltung | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Arbeitszeitbelege können wiederverwendet werden, wenn der Nummernreihenfolge als fortlaufend eingerichtet ist. |
| Projektmanagement und -buchhaltung | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANKREICH: Die Logik **Manueller Aufbewahrungsbetrag** stimmt nicht mit der Logik **Automatischer Aufbewahrungsbetrag** im Rechnungsvorschlag für den Projektvertrag überein. |
| Projektmanagement und -buchhaltung | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Wenn die Zuliefereraufbewahrung freigegeben wird, enthält die Belegbuchung zusätzliche nicht korrekte Zeilen. |
| Projektmanagement und -buchhaltung | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Wenn das Feld **Rechnungsdatum** auf der Seite **Rechnungsvorschlag erstellen** geändert wird, kann der folgende Fehler auftreten: „Objektverweis, der auf eine Instanz festgelegt wurde, ist nicht gesetzt.“ |
| Projektmanagement und -buchhaltung | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Ein Fehler tritt auf, wenn Sie versuchen, eine Arbeitszeittabelle aus dem Workflow **TSLine** zu genehmigen, und es gibt eine Arbeitszeittabellenrichtlinie für Samstag und Sonntag. |
| Projektmanagement und -buchhaltung | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Der Projektartikeltyp „Anfangssaldo“ ist aus **Transaktionszusammenfassungen für Rechnungsvorschläge** ausgeschlossen, wenn der Rechnungsbetrag des Rechnungsvorschlags berechnet wird. |
| Projektmanagement und -buchhaltung | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Wenn die Verbrauchskosten für einen Projektproduktionsauftrag 0 (null) sind, tritt der folgende Fehler auf, wenn Sie versuchen, zu schätzen: „Versucht, durch null zu teilen.“ |
| Projektmanagement und -buchhaltung | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Die mobile App für Projektarbeitszeitnachweise für Android antwortet nicht mehr. Das Problem steht im Zusammenhang mit **TimeEntryDataManager ArgumentNullException**. |
| Projektmanagement und -buchhaltung | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Die Integrationserfassung von Project Operations schlägt bei der Buchung fehl, weil bei einem Konto Dimensionen fehlen. Das Konto, dem die Dimensionen fehlen, ist jedoch nicht das Konto, auf das Sie buchen. |
| Projektmanagement und -buchhaltung | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Der Filter **ToDate** in Suchanfragen wird nicht gelöscht, wenn er aus dem Dialogfeld **Auswählen** auf der Seite **Buchungskosten** entfernt wird. |
| Projektmanagement und -buchhaltung | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Alle Verteilung zurücksetzen** schlägt fehl und zeigt einen Fehler für die Arbeitszeittabellen an, die für ein Projekt des Typs **Nur Uhrzeit** erstellt werden. |
| Projektmanagement und -buchhaltung | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Die Registerkarte **Projekt** kann auf einer ausstehenden Zuliefererrechnung nicht bearbeitet werden, wenn dem Artikel die Beschaffungskategorie zugewiesen ist. |
| Projektmanagement und -buchhaltung | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Der Navigationsbereich fehlt, wenn Sie nicht bei Project Operations Dataverse angemeldet sind. |
| Projektmanagement und -buchhaltung | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Bei Intercompany-Projektanpassungstransaktionen gibt es Probleme im Zielunternehmen. |
| Projektmanagement und -buchhaltung | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Zugesagte Kosten für ein Projekt berechnen die falsche Menge und den falschen Einstandspreis, wenn die Bestellung mithilfe von **Bestellvorgang zum Jahresende** im Hauptbuch bearbeitet wurde. |
| Projektmanagement und -buchhaltung | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Wenn ein Projektproduktionsauftrag mit Qualitätsaufträgen als abgeschlossen gemeldet wird, tritt der folgende Fehler auf: „Keine virtuelle Transaktion mit Bestandstransaktion gekennzeichnet.“ |
| Projektmanagement und -buchhaltung | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Beim Buchen einer projektbezogenen Kreditorenrechnung tritt der folgende Fehler auf: „Aufzählungstext Projekt – Kosten – Artikel existiert nicht.“ |
| Projektmanagement und -buchhaltung | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirekte Kosten werden verdoppelt, wenn Sie manuell Umsatz erzielen. |
| Projektmanagement und -buchhaltung | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | „Umsatzerlös antizipieren“ und die WIP-Buchung führt nicht zu Transaktionen. |
| Projektmanagement und -buchhaltung | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Die Aktivierung des ausstehenden Preises schlägt für einen Standardkostenartikel fehl, wenn eine eingegangene Projektbestellung vorhanden ist. |
| Projektmanagement und -buchhaltung | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Der WIP-Stornowert aus einer Rechnungsbuchung weicht vom ursprünglich gebuchten WIP-Wert aus einer Zeiterfassung ab. |
| Projektmanagement und -buchhaltung | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Es gibt ein Buchungsproblem für vom Projekt in Rechnung gestellte Umsätze in angewendeten Einbehaltungsfällen, bei denen die Transaktionen von Gutscheinen nicht ausgeglichen werden. |
| Projektmanagement und -buchhaltung | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Die Erstellung eines Kostenvoranschlags nach der Buchung eines Rechnungsvorschlags blockiert den Import von Korrekturzeilen in Project Operations. |
| Projektmanagement und -buchhaltung | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Die Änderung eines vollständig fakturierten Meilensteindatensatzes sollte nicht möglich sein. |
| Projektmanagement und -buchhaltung | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Wenn automatische Gebühren verwendet werden, kann die Intercompany-Kundenrechnung für eine Arbeitszeittabelle nicht gebucht werden, und es wird eine Fehlermeldung angezeigt. |
| Projektmanagement und -buchhaltung | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Die Adresse eines Unterprojekts wird nicht korrekt aktualisiert. |
| Projektmanagement und -buchhaltung | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Der Einstandspreis für Artikelanforderungen wird mit dem Einkaufspreis für konsolidierte Bestellungen aktualisiert. |
| Projektmanagement und -buchhaltung | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Die gebuchten Kosten sind nicht korrekt, nachdem der Kaufpreis aktualisiert und der Parameter **Änderungsmanagement aktivieren** aktiviert wurde. |
| Reisekosten und Ausgaben | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Alle Benutzerausgaben sind sichtbar, wenn Sie in der mobilen Ausgaben-App nach einer Kategorie suchen. |
| Reisekosten und Ausgaben | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Falsche Beträge für Zulieferer- und Mehrwertsteuertransaktionen werden aus einer Ausgabe gebucht, die aus einer Kreditkartentransaktion erstellt wurde. |
| Reisekosten und Ausgaben | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Eine irrelevante Warnung wird angezeigt, wenn Sie die Seiten für den Ausgabenbericht aktualisieren. |
| Reisekosten und Ausgaben | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Die falsche vorläufige genehmigende Person wird verwendet, wenn Sie eine vorläufigen genehmigende Person löschen und dann über den Workflow erneut einreichen. |
| Reisekosten und Ausgaben | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es tritt ein Buchungsfehler im Zusammenhang mit der Kilometereinstellung auf. |
| Reisekosten und Ausgaben | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Bei der Verteilung wird die juristische Person nicht aktualisiert, wenn eine nicht angehängte Transaktion dem Ausgabenbericht für eine Intercompany-Ausgabe erneut hinzugefügt wird. |

### <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu regulatorischen Aktualisierungen für Finanz- und Betriebs-Apps finden Sie unter [Regulatorische Aktualisierungen](/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei Microsoft Dynamics Lifecycle Services (LCS) anmelden und das Problemsuchtool verwenden, um die geplanten regulatorischen Updates anzuzeigen. Mit der Problemsuche können Sie nach Land oder Region, Funktionstyp und Release suchen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
