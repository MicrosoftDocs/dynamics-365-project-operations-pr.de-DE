---
title: Ausgabenverwaltungsparameter
description: Die folgenden Parameter steuern das Verhalten in der Ausgabenverwaltung.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991350"
---
# <a name="expense-management-parameters"></a>Ausgabenverwaltungsparameter


Die Parameter steuern das allgemeine Verhalten in der Ausgabenverwaltung.

### <a name="general"></a>Allgemein

| **Feld**                                                | **Beschreibung des Dataflows**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardrate der Fahrleistung**                             | Geben Sie den Erstattungssatz für die Fahrausgaben ein. Dieser Satz wird mit dem Kilometerstand multipliziert, der für die Ausgabe eingegeben wurde, um den Betrag zu berechnen, der für die Reisekosten erstattet wird.                       |
|**Persönliche Ausgaben bezahlt von**                             | Wählen Sie aus, wer für die Zahlung von Kreditkartentransaktionsbeträgen verantwortlich ist, die als persönlich eingestuft sind.                                                                                                     |
|**Zeigen Sie die gesamte Ausgabenabrechnung beim Drillback an**               | Wählen Sie diese Option aus, um alle Ausgaben für eine Spesenabrechnung anzuzeigen, wenn die Details des Originaldokuments für einen bestimmten Gutschein angezeigt werden, der beim Buchen der Spesenabrechnung generiert wurde.              |
|**Eine Vorautorisierung der Reise ist obligatorisch**                 | Wählen Sie diese Option aus, um zu verlangen, dass eine Reiseanforderung eingereicht und genehmigt wird, bevor ein Mitarbeiter eine Ausgabenabrechnung einreichen kann.                                                                    |
|**Die Bearbeitung von Verteilungen vor dem Buchen zulassen**            | Wählen Sie aus, ob die Verteilungen einer Spesenabrechnung vor der Buchung bearbeitet werden können.                                                                                                                 |
|**Die Richtlinien für das Kostenmanagement bewerten**                     | Wählen Sie aus, wann Ausgaben ausgewertet werden, um festzustellen, ob eine Ausgabenrichtlinie verletzt wurde. Ausgaben können auf Verstöße untersucht werden, wenn der Ausgabeneintrag eingegeben und gespeichert wird oder wenn die Ausgaben zur Genehmigung eingereicht werden. Die Richtlinienregeln für erforderliche Belege werden beim Speichern der Ausgabenposition ausgewertet.                   |
|**Konzerninterne Ausgabenpositionen zulassen**                         | Wählen Sie aus, ob die Eingabe von Ausgaben für andere juristische Personen in einer Spesenabrechnung erfasst werden können.                                                                                                          |
|**Ermöglichen Sie die Bearbeitung des Wechselkurses für Kreditkartenausgaben** | Wählen Sie diese Option, damit der Benutzer den Wechselkurs für importierte Kreditkartenausgaben bearbeiten kann.                                                                        |
|**Mehrstufige Hierarchiefelder, die angezeigt werden sollen**                  | Wählen Sie aus, welche Genehmigerfelder angezeigt werden, wenn der Workflow-Zuweisungstyp für die Spesenabrechnung als Hierarchie festgelegt ist, und die Hierarchie-Auswahl so festgelegt wird, dass die mehrstufige Genehmigungshierarchie für die Ausgabe verwendet wird. Wenn die mehrstufige Genehmigungshierarchie für einen Workflow verwendet wird, werden die ausgewählten Felder in der Spesenrechnung angezeigt und können bearbeitet werden. |
|**Geben Sie die Kreditkartennummer des Mitarbeiters ein (Update Juli 2017)**     | Wählen Sie aus, ob eine 15-stellige oder 16-stellige Nummer eingegeben und im Feld **Karten-ID** auf der Seite **Kreditkarten** für einen Mitarbeiter gespeichert werden soll.                                                                          |

### <a name="financial"></a>Finanzen

| **Feld**                                                            | **Beschreibung**     |
|----------------------------------------------------------------------|------------------------------------|
|**Name des täglichen Ledger-Journals**                                         | Wählen Sie den Namen des Ledger-Journals aus, in das genehmigte Ausgabenabrechnungen gebucht werden.            |
|**Steuerrückerstattung von Ausgaben aktivieren**                                  | Wählen Sie diese Option aus, um die Steuerrückerstattung für förderfähige Ausgaben zu aktivieren. Diese Option kann nicht aktiviert werden, wenn die US-Umsatzsteuer- und Steuerregeln aktiviert sind.      |
|**Bargeldvorschüsse sofort buchen**                                     | Wählen Sie diese Option aus, um einen genehmigten Vorschuss zu buchen, wenn der Zahlungs- und Überweisungsprozess abgeschlossen ist. Wenn diese Option nicht ausgewählt ist, generiert der Zahlungs- und Überweisungsprozess ein nicht gebuchtes allgemeines Journal. |
|**Abrechnungsdatum während der Buchung korrigieren**                             | Wählen Sie diese Option aus, um das Abrechnungsdatum zu aktualisieren, wenn Ausgaben gebucht werden, wenn die aktuelle Periode angehalten oder geschlossen wird. Das Buchhaltungsdatum wird auf die nächste offene Periode gesetzt.   |
|**Gruppierung von Transaktionen basierend auf dem in der Zahlungsmethode angegebenen Gegenkonto zulassen**      | Wählen Sie diese Option aus, um die Ausgabentransaktionen für eine Spesenabrechnung basierend auf dem Gegenkonto zusammenzufassen, das in der Zahlungsmethode für die Ausgaben angegeben ist.   
|**Einschließlich Steuer**                                                   | Wählen Sie diese Option, um die Umsatzsteuer standardmäßig in den Ausgabenbetrag einzubeziehen.             |
|**Belastungen beim Schließen von Reiseanforderungen freigeben**            | Wählen Sie diese Option, um belastete Gelder freizugeben, wenn eine genehmigte Reiseanforderung geschlossen wird.                                                                                   |
|**Reiseanforderung bei Budgetüberschreitung für Budgetregister und Projektbudget zulassen** | Wählen Sie diese Option aus, damit Mitarbeiter Reiseanforderungen zur Genehmigung einreichen können, obwohl sie entweder das im Budgetregister festgelegte zulässige Budget oder das zulässige Budget für ein Projekt überschreiten.            |
|**Ausgabenabrechnungseinreichung bei Budgetüberschreitung für Budgetregister und Projektbudget zulassen**    | Wählen Sie diese Option aus, damit Mitarbeiter Spesenabrechnungen zur Genehmigung einreichen können, obwohl sie entweder das im Budgetregister festgelegte zulässige Budget oder das zulässige Budget für ein Projekt überschreiten.                |
|**Ausgabenabrechnungsgenehmigung nur bei Budgetüberschreitung für Budgetregister zulassen**                | Wählen Sie diese Option aus, damit Genehmigende Ausgabenabrechnungen genehmigen können, die das im Budgetregister festgelegte zulässige Budget überschreiten.                                                                       |

### <a name="per-diem"></a>Pro Tag

| **Feld**                             | **Beschreibung des Dataflows**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Mindeststunden pro Tag**           | Geben Sie die Standard-Mindeststundenzahl ein, die ein Mitarbeiter an einem Tag arbeiten muss, um einen Tagessatz für reisebezogene Ausgaben zu erhalten.  Dieser Wert wird nur als Standardwert für das Mindeststunden-Feld für Tagessätze verwendet.                                                                                      |
|**Prozentuale Aufteilung der Mahlzeit**                          | Geben Sie den Standardprozentsatz des Tagessatzes für Mahlzeiten ein, der am ersten und letzten Tag der reisebezogenen Kosten verwendet wird, wenn das **Reduzierung der Mahlzeiten berechnen um**-Feld entweder auf **Mahlzeitentyp pro Tag** oder **Anzahl der Mahlzeiten pro Tag** festgelegt ist. Der Arbeitstag am ersten und letzten Tag ist möglicherweise kürzer als ein Standardarbeitstag. Daher kann die Höhe des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Wenn der Prozentsatz auf 0 (Null) eingestellt ist, betragen die Abzüge für den ersten und den letzten Tag 0,00. |
|**Prozentuale Aufteilung des Hotels**                        | Geben Sie den Standardprozentsatz des Tagessatzes für Hotels ein, der am ersten und letzten Tag der reisebezogenen Kosten verwendet wird. Der Arbeitstag am ersten und letzten Tag ist möglicherweise kürzer als ein Standardarbeitstag. Daher kann die Höhe des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Wenn der Prozentsatz auf 0 (Null) eingestellt ist, betragen die Abzüge für den ersten und den letzten Tag 0,00.                                              |
|**Prozentuale Aufteilung – Sonstiges**                        | Geben Sie den Standardprozentsatz des Tagessatzes für verschiedene Ausgaben ein, der am ersten und letzten Tag der reisebezogenen Kosten verwendet wird. Der Arbeitstag am ersten und letzten Tag ist möglicherweise kürzer als ein Standardarbeitstag. Daher kann die Höhe des Tagessatzes an diesen Tagen vom Standardbetrag abweichen. Wenn der Prozentsatz auf 0 (Null) eingestellt ist, betragen die Abzüge für den ersten und den letzten Tag 0,00.                                                                                                     |
|**Prozentuale Reduzierung für das Frühstück** | Geben Sie den Betrag ein, um den der Tagessatz für das Frühstück reduziert wird. Wenn ein Mitarbeiter beispielsweise ein kostenloses Frühstück erhält, können Sie möglicherweise die Höhe des Tagessatzes um 10 Prozent reduzieren.                               |
|**Prozentuale Reduzierung für das Mittagessen**    | Geben Sie den Betrag ein, um den der Tagessatz für das Mittagessen reduziert wird. Wenn ein Mitarbeiter beispielsweise ein kostenloses Mittagessen erhält, können Sie möglicherweise die Höhe des Tagessatzes um 15 Prozent reduzieren.                                       |
|**Prozentuale Reduzierung für das Abendessen**   | Geben Sie den Betrag ein, um den der Tagessatz für das Abendessen reduziert wird. Wenn ein Mitarbeiter beispielsweise ein kostenloses Abendessen erhält, können Sie möglicherweise die Höhe des Tagessatzes um 25 Prozent reduzieren.                                     |
|**Die Reduzierung der Mahlzeiten berechnen um**         | Wählen Sie aus, wie das System die Reduzierung der täglichen Mahlzeiten berechnen soll, indem Sie auswählen, ob die Reduzierung auf der Art der Mahlzeit pro Fahrt oder pro Tag basiert oder ob die Reduzierung auf der Anzahl der Mahlzeiten basiert, die pro Tag zulässig sind.|
|**Tagessatzrundung**                  | Wählen Sie die Art der Rundung aus, die für die Tagessätze verwendet wird. Wenn Sie die normale Rundung auswählen, werden alle Tagessätze mit einem Betrag von 0,50 auf 1,00 und alle Tagessätze mit einem Betrag von weniger als 0,50 auf 0,00 gerundet.                                                                                              |
|**Basis Tagessatzberechnung ein**         | Wählen Sie aus, ob ein Tagessatz auf einem Kalendertag oder einem 24-Stunden-Zeitraum basiert.       |

### <a name="fax-cover-pages"></a>Faxdeckblätter

| **Feld**                      | **Beschreibung des Dataflows**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Anweisungen**                   | Geben Sie die Anweisungen ein, die Mitarbeiter befolgen müssen, wenn sie ein Deckblatt für ein Fax erstellen, das zum Senden von Belegen verwendet wird, die sich auf eine Ausgabenabrechnung beziehen. Klicken Sie auf die Schaltfläche **Übersetzungen**, um sprachspezifischen Text einzugeben, der basierend auf der Benutzersprache angezeigt wird. |
|**Benutzer-ID (Barcode-Informationen)** | Wählen Sie diese Option aus, um die eindeutige Kennung eines Mitarbeiters im Barcode zu speichern, der auf dem Deckblatt des Faxes verwendet wird.                 |
|**Strichcode**                      | Wählen Sie den Barcode aus, der auf dem Deckblatt des Faxes verwendet wird. Die Strichcodes 39 und 128 werden in der Ausgabenverwaltung unterstützt.               |

### <a name="anti-corruption"></a>Korruptionsbekämpfung

|                 <strong>Feld</strong>                 |                                                                                                                                                                                            <strong>Beschreibung</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Anzeige der Korruptionsbekämpfung</strong>  | Wählen Sie diese Option, um den Antikorruptionstext anzuzeigen, wenn eine Spesenabrechnung erstellt wird. Anschließend können bestimmte Ausgabenkategorien aktiviert werden, für die die Antikorruptionsbescheinigung in der Spesenabrechnung ausgewählt werden muss. Beispielsweise kann eine Geschenkkategorie, die sich auf Ausgaben eines Regierungsbeamten bezieht, erfordern, dass der Mitarbeiter bestätigt, dass die Kosten den Unternehmensrichtlinien entsprechen, die sich auf Regierungsbeamte beziehen. |
| <strong>Korruptionsbekämpfungsnachricht für den Einsender</strong> |                                                                                             Geben Sie den Text ein, der dem Mitarbeiter beim Erstellen einer neuen Spesenabrechnung angezeigt wird. Klicken Sie auf die Schaltfläche <strong>Übersetzungen</strong>, um sprachspezifischen Text einzugeben, der basierend auf der Benutzersprache angezeigt wird.                                                                                             |
| <strong>Korruptionsbekämpfungsnachricht für den Genehmiger</strong>  |                                                                                             Geben Sie den Text ein, der der genehmigenden Person beim Erstellen einer neuen Spesenabrechnung angezeigt wird. Klicken Sie auf die Schaltfläche <strong>Übersetzungen</strong>, um sprachspezifischen Text einzugeben, der basierend auf der Benutzersprache angezeigt wird.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]