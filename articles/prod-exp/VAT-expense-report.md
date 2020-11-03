---
title: USt.-Beitreibung
description: In diesem Thema wird erläutert, wie Sie Rückerstattungen für Mehrwertsteuertransaktionen erhalten.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1be96521cdb486dd5a702cded615d3e1015b364
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076566"
---
# <a name="vat-recovery"></a>USt.-Beitreibung 

[!include [banner](../includes/banner.md)]

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
5. Prozesskosten für die inländische Mehrwertsteuerrückerstattung.

Die folgenden Abschnitte enthalten Beispiele, die zeigen, wie Contoso-Mitarbeiter die einzelnen Schritte ausführen.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Geben Sie in einer Spesenabrechnung Steuerinformationen zu Kreditkartentransaktionen ein, um berechtigte Mehrwertsteuerrückerstattungen zu ermitteln.

Nancy, eine in den USA ansässige Vertriebsmitarbeiterin von Contoso, ist kürzlich von einer Verkaufsreise in das Vereinigte Königreich zurückgekehrt. Während ihrer Reise sind bei ihr einige persönliche Kreditkartenkosten für Mahlzeiten entstanden. Nancy muss jetzt eine Spesenabrechnung erstellen, um ihre Spesen abzustimmen.

Wenn Nancy Informationen in ihre Spesenabrechnung eingibt, wählt Sie **Vereinigtes Königreich** im Feld **Land/Region** auf der Seite **Spesenabrechnung bearbeiten** aus. Die Liste der Umsatzsteuergruppen wird dann gefiltert, sodass nur die Gruppen angezeigt werden, die für das Vereinigte Königreich gelten. Nancy wählt die Mehrwertsteuergruppe **Vereinigtes Königreich 001** und dann die Artikel-Mehrwertsteuergruppe **Mahlzeiten** aus. Als Nächstes fügt sie eine neue Transaktion für ihre Unterbringung hinzu. Da es im Vereinigten Königreich nur eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe für Unterkünfte gibt, werden diese Informationen automatisch in die Spesenabrechnung von Nancy eingetragen.

Gemäß der Contoso-Richtlinie müssen alle Ausgaben mit einer entsprechenden Quittung versehen sein. Wenn Nancy ihre Spesenabrechnung speichert, erhält sie daher eine Nachricht, dass sie für jede Transaktion, die sie in ihrer Spesenabrechnung aufgeführt hat, eine Quittung anhängen muss. Nancy überprüft, ob sie ihrer Spesenabrechnung ein digitales Bild jedes Transaktionsbelegs beigefügt hat, und legt ihren Bericht dann zur Genehmigung vor. Anschließend sendet sie die Papierbelege an das Back-Office-Verarbeitungsteam. Dieses Team sendet die Mehrwertsteuer-Erstattungsdaten an den Drittanbieter, der die internationalen Mehrwertsteuer-Erstattungserklärungen für Contoso einreicht.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Stellen Sie sicher, dass alle Steuerinformationen vollständig sind, und buchen Sie dann die Spesenabrechnung.

April, die Kreditorenkoordinatorin für Contoso, muss alle Steuerinformationen eingeben, die in einer Spesenabrechnung fehlen, bevor die Abrechnung gebucht werden kann. Sie öffnet die Seite **Spesenabrechnungsdetails** und sieht Nancys genehmigte Spesenabrechnung. April öffnet dann die Spesenabrechnung, um die Details der Transaktionen anzuzeigen. Sie sieht, dass Nancy für eine der Transaktionen keine Artikel-Mehrwertsteuergruppe eingegeben hat. Da diese Informationen nicht bereitgestellt werden, kann April die Spesenabrechnung nicht buchen. Deshalb schaut April auf die Seite **Steuerkonfigurationen** in der Ausgabenverwaltung und findet die entsprechende Artikel-Mehrwertsteuergruppe für das Land/die Region und den Transaktionstyp. April kann nun die Spesenabrechnung in der Finanzbuchhaltung buchen.

Wenn April die Spesenabrechnung bucht, wird ein Arbeitsposten mit erstattungsfähiger Mehrwertsteuer erstellt. Dieses Arbeitselement wird einem Mitglied des Backoffice-Verarbeitungsteams zugewiesen. April erhält eine Nachricht, die bestätigt, dass die Buchung erfolgreich war. In dieser Nachricht wird auch die Anzahl der Mehrwertsteuertransaktionen aufgeführt, die für die Rückforderung identifiziert wurden.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Ausgaben verarbeiten, die für eine internationale Mehrwertsteuerrückerstattung in Frage kommen

Arnie, Mitglied des Back-Office-Verarbeitungsteams von Contoso, ist dafür verantwortlich, zu überprüfen, ob alle erforderlichen Informationen für die Mehrwertsteuerrückerstattung in den Spesenabrechnungen enthalten sind. Er öffnet die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die Nancy eingereicht hat. Arnie überprüft, ob alle erforderlichen Belege beigefügt sind und ob die richtigen Mehrwertsteuergruppen und Artikel-Mehrwertsteuercodes eingegeben wurden.

Wenn Arnie die Papierbelege von Nancy erhält, überprüft er sie anhand der Papierbelege und ändert dann den Status der Spesenabrechnung in **Bereit für Beitreibung**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Mehrwertsteuer-Erstattungsdaten an den Drittanbieter senden,, um internationale Rückforderungserklärungen einzureichen

Wenn Arnie bereit ist, die Spesenabrechnungsdaten an den Drittanbieter zu senden, der die Mehrwertsteuer-Erstattungserklärungen einreicht, öffnet er die Seite **Steuerrückerstattung**. Er filtert die Seite so, dass nur die Spesenabrechnungen angezeigt werden, die als **Bereit für Beitreibung** gekennzeichnet sind. Arnie wählt dann **Datei** &gt; **Nach Excel exportieren** aus. Die Umsatzsteuerinformationen aus den Spesenabrechnungen werden in das Microsoft Excel-Arbeitsblatt exportiert. Arnie sendet dieses Arbeitsblatt an den Drittanbieter und enthält eine Nachricht, die besagt, dass die Papierbelege per Kurier gesendet wurden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Prozesskosten für die inländische Mehrwertsteuerrückerstattung

Arnie muss überprüfen, ob die Spesenabrechnungstransaktionen für die Erstattung der Mehrwertsteuer in Frage kommen und ob die digitalen Belege den Berichten beigefügt sind. Um gültige Ausgaben für die inländische Rückforderung zu verarbeiten, öffnet Arnie die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die überprüft werden muss. Er überprüft, ob die Belege auf den Namen des Unternehmens und nicht auf den des Mitarbeiters lauten. Für die Erstattung der Mehrwertsteuer müssen die Belege auf den Namen des Unternehmens lauten. Arnie bestätigt dann, dass die richtigen Umsatzsteuergruppen- und Artikelumsatzsteuerkennzeichen angewendet wurden.

Wenn Arnie die Papierbelege erhält, ändert er den Status der Spesenabrechnung in **Bereit für Beitreibung**. Er kann die Steuererklärung dann bei der zuständigen Steuerbehörde einreichen. In diesem Fall ist die entsprechende Steuerbehörde in den USA der Internal Revenue Service (IRS).
