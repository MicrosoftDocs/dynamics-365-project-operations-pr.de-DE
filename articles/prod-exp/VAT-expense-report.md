---
title: USt.-Beitreibung
description: In diesem Thema wird erläutert, wie Sie Rückerstattungen für Mehrwertsteuertransaktionen erhalten.
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986040"
---
# <a name="vat-recovery"></a>USt.-Beitreibung 

Um Rückerstattungen für berechtigte Mehrwertsteuertransaktionen zu erhalten, muss ein Unternehmen oder eine Organisation genaue Informationen identifizieren, sammeln, überprüfen und übermitteln. Dieser Prozess umfasst mehrere Aufgaben und kann je nach Größe Ihres Unternehmens mehrere Mitarbeiter oder Rollen umfassen.

Um die Mehrwertsteuer durch Verwendung der Ausgabenverwaltung wiederherzustellen, müssen folgende Voraussetzungen erfüllt sein:

- Für Länder/Regionen, die Ausgabenkategorien zugeordnet sind, müssen Steuercodes erstellt werden.
- Für jeden Steuercode muss eine Mehrwertsteuergruppe erstellt werden.
- Ein Artikel-Mehrwertsteuercode muss für jede Mehrwertsteuergruppe erstellt werden.

Nachdem die Voraussetzungen erfüllt sind, müssen Mitarbeiter die folgenden Schritte ausführen, um Rückerstattungen für Mehrwertsteuertransaktionen anzufordern.

1. Geben Sie in einer Spesenabrechnung Steuerinformationen zu Kreditkartentransaktionen ein, um berechtigte Mehrwertsteuerrückerstattungen zu ermitteln.
2. Stellen Sie sicher, dass alle Steuerinformationen vollständig sind, und buchen Sie dann die Spesenabrechnung.
3. Verarbeiten Sie Ausgaben, die für eine internationale Mehrwertsteuerrückerstattung in Frage kommen.
4. Senden Sie Mehrwertsteuer-Erstattungsdaten an den Drittanbieter, um internationale Rückforderungserklärungen einzureichen.
5. Spesen für die inländische Mehrwertsteuerrückerstattung verarbeiten

Die folgenden Abschnitte enthalten Beispiele, die zeigen, wie Contoso Mitarbeiter jeden Schritt durchführen.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Geben Sie in einer Spesenabrechnung Steuerinformationen zu Kreditkartentransaktionen ein, um berechtigte Mehrwertsteuerrückerstattungen zu ermitteln.

Nancy, eine Contoso Vertriebsmitarbeiter mit Standort in den USA, die vor kurzem von einer Verkaufsreise in das Vereinigte Königreich zurückgekehrt ist. Während ihrer Reise sind bei ihr einige persönliche Kreditkartenkosten für Mahlzeiten entstanden. Nancy muss jetzt eine Spesenabrechnung erstellen, um ihre Spesen abzustimmen.

Wenn Nancy Informationen in ihre Spesenabrechnung eingibt, wählt Sie **Vereinigtes Königreich** im Feld **Land/Region** auf der Seite **Spesenabrechnung bearbeiten** aus. Die Liste der Umsatzsteuergruppen wird dann gefiltert, sodass nur die Gruppen angezeigt werden, die für das Vereinigte Königreich gelten. Nancy wählt die Mehrwertsteuergruppe **Vereinigtes Königreich 001** und dann die Artikel-Mehrwertsteuergruppe **Mahlzeiten** aus. Als Nächstes fügt sie eine neue Transaktion für ihre Unterbringung hinzu. Da es im Vereinigten Königreich nur eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe für Unterkünfte gibt, werden diese Informationen automatisch in die Spesenabrechnung von Nancy eingetragen.

Per Contoso Richtlinie muss für alle Ausgaben ein entsprechender Beleg vorliegen. Wenn Nancy ihre Spesenabrechnung speichert, erhält sie daher eine Nachricht, dass sie für jede Transaktion, die sie in ihrer Spesenabrechnung aufgeführt hat, eine Quittung anhängen muss. Nancy überprüft, ob sie ihrer Spesenabrechnung ein digitales Bild jedes Transaktionsbelegs beigefügt hat, und legt ihren Bericht dann zur Genehmigung vor. Anschließend sendet sie die Papierbelege an das Back-Office-Verarbeitungsteam. Dieses Team sendet die Umsatzsteuerrückerstattungsdaten an den Drittanbieter, der internationale Umsatzsteuerrückerstattungserklärungen für Contoso einreicht.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Stellen Sie sicher, dass alle Steuerinformationen vollständig sind, und buchen Sie dann die Spesenabrechnung.

April, der Kreditorenkoordinator für Contoso, muss alle Steuerinformationen eingeben, die in einer Spesenabrechnung fehlen, bevor die Abrechnung gebucht werden kann. Sie öffnet die Seite **Spesenabrechnungsdetails** und sieht Nancys genehmigte Spesenabrechnung. April öffnet dann die Spesenabrechnung, um die Details der Transaktionen anzuzeigen. Sie sieht, dass Nancy für eine der Transaktionen keine Artikel-Mehrwertsteuergruppe eingegeben hat. Da diese Informationen nicht bereitgestellt werden, kann April die Spesenabrechnung nicht buchen. Deshalb schaut April auf die Seite **Steuerkonfigurationen** in der Ausgabenverwaltung und findet die entsprechende Artikel-Mehrwertsteuergruppe für das Land/die Region und den Transaktionstyp. April kann nun die Spesenabrechnung in der Finanzbuchhaltung buchen.

Wenn April die Spesenabrechnung bucht, wird ein Arbeitsposten mit erstattungsfähiger Mehrwertsteuer erstellt. Dieses Arbeitselement wird einem Mitglied des Backoffice-Verarbeitungsteams zugewiesen. April erhält eine Nachricht, die bestätigt, dass die Buchung erfolgreich war. In dieser Nachricht wird auch die Anzahl der Mehrwertsteuertransaktionen aufgeführt, die für die Rückforderung identifiziert wurden.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Ausgaben verarbeiten, die für eine internationale Mehrwertsteuerrückerstattung in Frage kommen

Arnie, ein Mitglied vom Contoso Backoffice-Verarbeitungsteam ist dafür verantwortlich, zu bestätigen, dass alle erforderlichen Informationen für die Mehrwertsteuerrückerstattung in den Spesenabrechnungen enthalten sind. Er öffnet die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die Nancy eingereicht hat. Arnie überprüft, ob alle erforderlichen Belege beigefügt sind und ob die richtigen Mehrwertsteuergruppen und Artikel-Mehrwertsteuercodes eingegeben wurden.

Wenn Arnie die Papierbelege von Nancy erhält, überprüft er sie anhand der Papierbelege und ändert dann den Status der Spesenabrechnung in **Bereit für Beitreibung**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Mehrwertsteuer-Erstattungsdaten an den Drittanbieter senden,, um internationale Rückforderungserklärungen einzureichen

Wenn Arnie bereit ist, die Spesenabrechnungsdaten an den Drittanbieter zu senden, der die Mehrwertsteuer-Erstattungserklärungen einreicht, öffnet er die Seite **Steuerrückerstattung**. Er filtert die Seite so, dass nur die Spesenabrechnungen angezeigt werden, die als **Bereit für Beitreibung** gekennzeichnet sind. Arnie wählt dann **Datei** &gt; **Nach Excel exportieren** aus. Die Umsatzsteuerinformationen aus den Spesenabrechnungen werden in das Microsoft Excel-Arbeitsblatt exportiert. Arnie sendet dieses Arbeitsblatt an den Drittanbieter und enthält eine Nachricht, die besagt, dass die Papierbelege per Kurier gesendet wurden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Prozesskosten für die inländische Mehrwertsteuerrückerstattung

Arnie muss überprüfen, ob die Spesenabrechnungstransaktionen für die Erstattung der Mehrwertsteuer in Frage kommen und ob die digitalen Belege den Berichten beigefügt sind. Um gültige Ausgaben für die inländische Rückforderung zu verarbeiten, öffnet Arnie die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die überprüft werden muss. Er überprüft, ob die Belege auf den Namen des Unternehmens und nicht auf den des Mitarbeiters lauten. Für die Erstattung der Mehrwertsteuer müssen die Belege auf den Namen des Unternehmens lauten. Arnie bestätigt dann, dass die richtigen Umsatzsteuergruppen- und Artikelumsatzsteuerkennzeichen angewendet wurden.

Wenn Arnie die Papierbelege erhält, ändert er den Status der Spesenabrechnung in **Bereit für Beitreibung**. Er kann die Steuererklärung dann bei der zuständigen Steuerbehörde einreichen. In diesem Fall ist die entsprechende Steuerbehörde in den USA der Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]