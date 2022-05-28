---
title: Neuigkeiten oder Änderungen für September 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version vom September 2021 der Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582019"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Neuigkeiten oder Änderungen für September 2021 – Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung

_**Gilt für:** Project Operations für lager-/produktionsbasierte Szenarien_

Dieses Thema gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Projektmanagement und -buchhaltung in einer Dynamics 365 Finance-Umgebungsversion 10.0.21
 
## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
|---|---|---|
| Projektmanagement und -buchhaltung | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Wenn der Einkaufsmanagerrolle Zugriff auf eine juristische Person gewährt wird, erhält sie auch der Zugriff auf alle Projekte in allen juristischen Personen. |
| Projektmanagement und -buchhaltung | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Ein Rundungsproblem bei der Mehrwertsteuer (MwSt.) tritt auf, wenn eine Gutschrift mit einer ursprünglichen Projektrechnung verrechnet wird. |
| Projektmanagement und -buchhaltung | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Verwenden Sie ein alternatives Projektbudget für die Budgetüberprüfung. |
| Projektmanagement und -buchhaltung | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Die Preisgruppe **Verkaufspreis – Stunde** wird nicht im Projektstrukturplan für Projektangebote berechnet. |
| Projektmanagement und -buchhaltung | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Die Eliminierung der Schätzung schlägt fehl, wenn die Funktion **Projektvertragswährung für Schätzungsberechnung aktivieren** aktiviert ist. |
| Projektmanagement und -buchhaltung | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Die Mehrwertsteuerfaktorisierung nach Menge wird dem Verkaufspreisbetrag hinzugefügt, wenn die Verbrauchsteuer für die Mehrwertsteuergruppe der Projektausgabenerfassung verwendet wird. |
| Projektmanagement und -buchhaltung | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Die bedingte Steuer wird für die letzte Zahlung nicht korrekt berechnet, wenn der Zulieferereinbehalt und die Vorauszahlung auf Bestellrechnungen angewendet werden. |
| Projektmanagement und -buchhaltung | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Anpassungsverfolgung funktioniert nicht für Anfangssaldenerfassungen. |
| Projektmanagement und -buchhaltung | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Zuteilung der Projektbudgetrevision nach Periode** wird auf alle Budgetperioden aufgeteilt. Wenn die Zuteilung übermittelt wird, wird der Datensatz nicht gelöscht. |
| Projektmanagement und -buchhaltung | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | WIP-Buchungen ins Hauptbuch haben einen falschen Betrag. |
| Projektmanagement und -buchhaltung | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Die Genehmigung der Projektstundenerfassung funktioniert nicht. |
| Projektmanagement und -buchhaltung | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Der Verkaufspreis der Projektanpassung wird nicht mit indirekten Kosten aktualisiert, wenn das Finanzierungslimit nicht markiert ist. |
| Projektmanagement und -buchhaltung | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Eine Artikelanforderung kann nicht erstellt werden, wenn die Kopfzeile der Verkaufstabelle fakturiert wird und die unterstützende Bestellung für vorhandene Positionen abgeschlossen wurde. |
| Projektmanagement und -buchhaltung | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Der Einbehaltungsbetrag für eine Abrechnungsregel, die einen Meilenstein für ein anderes Projekt hat, wird nicht in der entsprechenden Projekt-ID gebucht, die für den Meilenstein ausgewählt wurde. Stattdessen wird er mit dem ersten Projekt veröffentlicht. |
| Projektmanagement und -buchhaltung | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Wenn Sie **Finanzdimensionssatz** bei einem Rechnungsvorschlag auswählen, tritt der folgende Fehler auf: „Objekt vom Typ 'Dynamics.AX.Application.FormIntControl' kann nicht auf Typ 'Dynamics.AX.Application.FormStringControl' übertragen werden.“ |
| Projektmanagement und -buchhaltung | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Der Bericht **Projektrechnung** überspringt Zeilen. |
| Projektmanagement und -buchhaltung | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Bei der Berechnung der Kostenkontrolle für ein Investitionsprojekt tritt ein Fehler auf. |
| Projektmanagement und -buchhaltung | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Die **ProjTable::InitFromCustTable – canDeletePostalAddress**-Methode verursacht ein Leistungsproblem. |
| Projektmanagement und -buchhaltung | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Die Fehlermeldung sollte klarer sein als „Unerwarteter Fehler“. |
| Projektmanagement und -buchhaltung | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Der Buchungs-Batch-Auftrag der Projektrechnung verarbeitet und bucht den Rechnungsvorschlag, auch wenn die Rechnungsposten nicht generiert wurden. |
| Projektmanagement und -buchhaltung | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Ein Rundungsproblem tritt auf, wenn der Konfigurationsschlüssel für die Lizenz für den öffentlichen Sektor deaktiviert ist. Bei Verträgen mit mehreren Gründungsquellen wird in den Arbeitszeittabellenstunden ein falscher Einstands- oder Verkaufspreis generiert. |
| Projektmanagement und -buchhaltung | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Der Projektverkaufspreis einer fakturierten Projektbestellung wird falsch berechnet, wenn das Verkaufspreismodell **Deckungsbeitragsverhältnis** ist. |
| Projektmanagement und -buchhaltung | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Das System berücksichtigt die dazwischen liegenden aktiven Tage nicht, wenn es den effektiven Arbeitssatz für einen Mitarbeiter berechnet. |
| Projektmanagement und -buchhaltung | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Aufgrund des folgenden Validierungsfehlers tritt in der Intercompany-Arbeitszeittabelle ein Buchungsfehler auf: „Für die juristische Person ist kein Handelspartner konfiguriert.“ |
| Projektmanagement und -buchhaltung | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Die Beschreibung aus einer Bestellung mit einer Ausgabenkategorie wird nicht in der gebuchten Projekttransaktionsliste abgerufen. |
| Projektmanagement und -buchhaltung | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Bei Artikelerfassungen, die auf ein Projekt gebucht werden, gibt es eine falsche Konvertierung. |
| Projektmanagement und -buchhaltung | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Sie können eine Bestellung auch dann bestätigen, wenn das Finanzierungslimit überschritten wurde. |
| Projektmanagement und -buchhaltung | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Der Abschnitt **Rechnung korrigieren/stornieren** auf einer Freitextrechnung verschwindet, wenn eine Projekt-ID ausgewählt wird. |
| Projektmanagement und -buchhaltung | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Es treten Leistungsprobleme auf, wenn ein Projektrechnungsvorschlag aus einem Projektvertriebsauftrag gebucht wird, der einen Lagerartikel enthält. |
| Projektmanagement und -buchhaltung | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projekt-Einkaufsrechnungen können nicht gebucht werden, weil der folgende Fehler auftritt: „Die Funktion AccDistProcessorProjectExtension.createForProjectRevenueLine wurde falsch aufgerufen.“ |
| Projektmanagement und -buchhaltung | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Aktualisieren Sie die Erstellung eines Batch-Auftrags für die Projektschätzung, um die Ausführung mehrerer Unteraufgaben zu unterstützen. |
| Projektmanagement und -buchhaltung | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Der Status einer Arbeitszeittabelle kann nicht auf **Entwurf** aktualisiert werden, wenn der Workflow in einem Status **Storniert** festhängt. |
| Projektmanagement und -buchhaltung | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Einbehaltungsbeträge werden im Gutschriftsrechnungsvorschlag nicht berechnet, wenn mehrere Zeilen vorhanden sind. |
| Projektmanagement und -buchhaltung | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Wenn Sie versuchen, den Betrag einer generierten Rechnung aus einer Bestellung zu ändern, tritt der folgende Fehler auf: „Die Transaktionen auf dem Gutschein werden nicht gemäß XX/XX/XXXX ausgeglichen. (Abrechnungswährung: 0,00 – Berichtswährung: 0,01).“ |
| Projektmanagement und -buchhaltung | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Es gibt ein Leistungsproblem, wenn ein Projektrechnungsvorschlag im Batch-Modus gebucht wird, aufgrund der Verknüpfung mit **GeneralJournalAccountEntry**. |
| Projektmanagement und -buchhaltung | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Beim Buchen einer Arbeitszeittabelle treten Leistungsprobleme auf. |
| Projektmanagement und -buchhaltung | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Die Kalkulationshierarchie des Projektstrukturplans ist nicht korrekt ausgerichtet, nachdem alle Aufgaben erweitert wurden oder nachdem eine einzelne Aufgabe manuell erweitert wurde. |
| Projektmanagement und -buchhaltung | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Die Excel-Vorlage für das Projektangebot kann nicht im Menü **In Excel öffnen** hinzugefügt werden. |
| Projektmanagement und -buchhaltung | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Die Steuerbefreiungsnummer für eine juristische Person ist nicht in einer gedruckten Projektrechnung enthalten. |
| Projektmanagement und -buchhaltung | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Im Bestandseinheitsfehler werden keine Finanzdaten aktualisiert, wenn ein Projekt in Bezug auf Kreditlinien angepasst wird. |
| Projektmanagement und -buchhaltung | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Nachdem Sie KB 461935 angewendet haben, können Sie keine Schätzungen veröffentlichen, wenn Sie zu fortlaufenden Nummernsequenzen wechseln. |
| Projektmanagement und -buchhaltung | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** führt dazu, dass die mobile App für Projektarbeitszeitnachweise für Android nicht mehr reagiert. |
| Projektmanagement und -buchhaltung | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Der WIP-Stornowert aus einer Rechnungsbuchung weicht vom ursprünglich gebuchten WIP-Wert aus der Zeiterfassung ab. |
| Projektmanagement und -buchhaltung | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | In angewendeten Einbehaltungsfällen werden die Transaktionen von Gutscheinen nicht ausgeglichen, wenn für ein Projekt in Rechnung gestellte Umsätze gebucht werden. |
| Projektmanagement und -buchhaltung | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Wenn die Funktion **Leistungsverbesserung bei der Projektressourcenplanung** aktiviert ist, werden Dezimalwerte für Ressourcenverfügbarkeit und -kapazität falsch gerundet. |
| Projektmanagement und -buchhaltung | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Wenn die Funktion **Projektschätzungen mit mehreren Batch-Aufgaben erstellen** aktiviert ist, funktioniert die Erstellung von Schätzungen in einem Batch mit mehreren Unteraufgaben nur für die aktuelle Periode. |
| Reisekosten und Ausgaben | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Eine Richtlinie für Reiseanforderungen wird ignoriert, und der Workflow wird ohne Fehler genehmigt. |
| Reisekosten und Ausgaben | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Die mobile Ausgaben-App speichert nicht die folgenden Informationen in der Ausgabenzeile:</p><ul><li>Die ID des Projekts</li><li>Ob die Ausgabe abrechenbar ist</li><li>Die Aktivitätsnummer</li></ul> |
| Reisekosten und Ausgaben | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Das Feld **Beigefügte Quittungen** ist auf **Ja** gesetzt, auch wenn der Ausgabenzeile keine Quittung beigefügt ist. |
| Reisekosten und Ausgaben | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Wenn Sie versuchen, die Ausgabenkategorie in **Persönlich** zu ändern, tritt ein Fehler auf. |
| Reisekosten und Ausgaben | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Sie können keinen Beleg anhängen und die übergeordnete Ausgabe nicht bearbeiten, nachdem eine Kreditkartentransaktion in eine persönliche Ausgabe aufgeteilt wird. |
| Reisekosten und Ausgaben | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Die Ausgabenrichtlinie für Intercompany-Transaktionen mit einer Projekt-ID funktioniert nicht richtig. |
| Reisekosten und Ausgaben | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Die gebuchten Datumsinformationen fehlen für gebuchte Ausgabenberichte. |
| Reisekosten und Ausgaben | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Es gibt Probleme mit der Zahlungsmethode in der mobilen Ausgaben-App. |
| Reisekosten und Ausgaben | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Eine Reiseanforderung, die für eine Arbeitskraft erstellt wird, kann vor dem Stellvertretungsdatum für den Ausgabenbericht einer anderen Arbeitskraft verwendet werden. |
| Reisekosten und Ausgaben | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Wenn Sie eine Ausgabe erstellt wird, werden Änderungen an Finanzdimensionswerten auf der Buchhaltungsverteilungsebene im Arbeitsplatz **Ausgabenmanagement** nicht korrekt aktualisiert. |
| Reisekosten und Ausgaben | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Der Genehmigungsstatus der Hauptausgabenzeile wird nicht mit dem Genehmigungsstatus des Einzelposten-Workflows synchronisiert. |
| Reisekosten und Ausgaben | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ein Fehler tritt auf, wenn Sie einen Ausgabenbericht buchen und die Steuerrückerstattung aktiviert ist. |
| Reisekosten und Ausgaben | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Ein Delegierter kann keine Spesendokumente für einen gekündigten Mitarbeiter löschen. |
| Reisekosten und Ausgaben | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Das Löschen einer Ausgabenzeile dauert länger als erwartet und beeinträchtigt die Leistung. |
| Reisekosten und Ausgaben | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** verursacht einen verwaisten **TaxUncommitted**-Datensatz, weil nur **SourceDocumentLine** gelöscht wird. |
| Reisekosten und Ausgaben | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** berücksichtigt nicht **trvExpTrans.ReferenceDataAreaId**, um die neue Nummersequenz zu erstellen. |

## <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften

Informationen zu regulatorischen Aktualisierungen für Finanz- und Betriebs-Apps finden Sie unter [Regulatorische Aktualisierungen](/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei Microsoft Dynamics Lifecycle Services (LCS) anmelden und das Problemsuchtool verwenden, um die geplanten regulatorischen Updates anzuzeigen. Mit der Problemsuche können Sie nach Land oder Region, Funktionstyp und Release suchen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
