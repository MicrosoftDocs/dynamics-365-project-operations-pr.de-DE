---
title: Mehrwertsteuerrückerstattung in der Ausgabenverwaltung
description: In diesem Thema wird erläutert, wie Sie Rückerstattungen für berechtigte Mehrwertsteuertransaktionen erhalten.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7c961763d3d670117c5a576db485ebcfdcf9ec9f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581145"
---
# <a name="vat-recovery-in-expense-management"></a>Mehrwertsteuerrückerstattung in der Ausgabenverwaltung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Um Rückerstattungen für berechtigte Mehrwertsteuertransaktionen zu erhalten, muss ein Unternehmen oder eine Organisation genaue Informationen identifizieren, sammeln, überprüfen und übermitteln. Dieser Prozess umfasst mehrere Aufgaben und kann je nach Größe Ihres Unternehmens mehrere Mitarbeiter oder Rollen umfassen.

Um die Mehrwertsteuer im Modul **Ausgabenverwaltung** wiederherzustellen, müssen folgende Voraussetzungen erfüllt sein:

- Für Länder/Regionen, die Ausgabenkategorien zugeordnet sind, müssen Steuercodes erstellt werden.
- Für jeden Steuercode muss eine Mehrwertsteuergruppe erstellt werden.
- Ein Artikel-Mehrwertsteuercode muss für jede Mehrwertsteuergruppe erstellt werden.

Nachdem die Voraussetzungen erfüllt sind, müssen die folgenden Schritte ausgeführt werden, um Rückerstattungen für Mehrwertsteuertransaktionen anzufordern.

1. Geben Sie in einer Spesenabrechnung Steuerinformationen zu Kreditkartentransaktionen ein, um berechtigte Mehrwertsteuerrückerstattungen zu ermitteln.
2. Stellen Sie sicher, dass alle Steuerinformationen vollständig sind, und buchen Sie dann die Spesenabrechnung.
3. Verarbeiten Sie Ausgaben, die für eine internationale Mehrwertsteuerrückerstattung in Frage kommen.
4. Senden Sie Mehrwertsteuer-Erstattungsdaten an den Drittanbieter, um internationale Rückforderungserklärungen einzureichen.
5. Prozesskosten für die inländische Mehrwertsteuerrückerstattung.

Die folgenden Abschnitte enthalten Beispiele, die zeigen, wie Contoso-Mitarbeiter die einzelnen Schritte ausführen.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Geben Sie in einer Spesenabrechnung Steuerinformationen zu Kreditkartentransaktionen ein, um berechtigte Mehrwertsteuerrückerstattungen zu ermitteln.

Nancy, eine in den Vereinigten Staaten ansässige Vertriebsmitarbeiterin von Contoso, ist kürzlich von einer Verkaufsreise in das Vereinigte Königreich zurückgekehrt. Während der Reise sind bei Nancy einige persönliche Kreditkartenkosten für Mahlzeiten entstanden. Nancy muss jetzt eine Spesenabrechnung erstellen, um die Spesen abzustimmen.

Wenn Nancy Informationen in die Spesenabrechnung eingibt, wählt Sie **Vereinigtes Königreich** im Feld **Land/Region** auf der Seite **Spesenabrechnung bearbeiten** aus. Die Liste der Umsatzsteuergruppen wird dann gefiltert, sodass nur die Gruppen angezeigt werden, die für das Vereinigte Königreich gelten. Nancy wählt die Mehrwertsteuergruppe **Vereinigtes Königreich 001** und dann die Artikel-Mehrwertsteuergruppe **Mahlzeiten** aus. Als Nächstes fügt Nancy eine neue Transaktion für die Unterbringung hinzu. Da es im Vereinigten Königreich nur eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe für Unterkünfte gibt, werden diese Informationen automatisch in die Spesenabrechnung von Nancy eingetragen.

Gemäß der Contoso-Richtlinie müssen alle Ausgaben mit einer entsprechenden Quittung versehen sein. Wenn Nancy die Spesenabrechnung speichert, erhält sie daher eine Nachricht, dass sie für jede Transaktion, die sie in ihrer Spesenabrechnung aufgeführt hat, eine Quittung anhängen muss. Nancy überprüft, ob sie ihrer Spesenabrechnung ein digitales Bild jedes Transaktionsbelegs beigefügt hat, und legt ihren Bericht dann zur Genehmigung vor. Anschließend sendet sie die Papierbelege an das Back-Office-Verarbeitungsteam. Dieses Team sendet die Mehrwertsteuer-Erstattungsdaten an den Drittanbieter, der die internationalen Mehrwertsteuer-Erstattungserklärungen für Contoso einreicht.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Die Steuerinformationen überprüfen und eine Spesenabrechnung veröffentlichen

Vor April kann die Kreditorenkoordinatorin für Contoso eine Spesenabrechnung erstellen. Sie muss alle darin fehlenden Steuerinformationen eingeben. Sie öffnet die Seite **Spesenabrechnungsdetails** und sieht Nancys genehmigte Spesenabrechnung. April öffnet dann die Spesenabrechnung, um die Details der Transaktionen anzuzeigen. Sie sieht, dass Nancy für eine der Transaktionen keine Artikel-Mehrwertsteuergruppe eingegeben hat. Da diese Informationen nicht bereitgestellt werden, kann April die Spesenabrechnung nicht buchen. Deshalb schaut sie auf die Seite **Steuerkonfigurationen** in der Ausgabenverwaltung und findet die entsprechende Artikel-Mehrwertsteuergruppe für das Land/die Region und den Transaktionstyp. April kann nun die Spesenabrechnung in der Finanzbuchhaltung buchen.

Wenn April die Spesenabrechnung bucht, wird ein Arbeitsposten mit erstattungsfähiger Mehrwertsteuer erstellt. Dieses Arbeitselement wird einem Mitglied des Backoffice-Verarbeitungsteams zugewiesen. April erhält eine Nachricht, die bestätigt, dass die Buchung erfolgreich war. In dieser Nachricht wird auch die Anzahl der Mehrwertsteuertransaktionen aufgeführt, die für die Rückforderung identifiziert wurden.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Ausgaben verarbeiten, die für eine internationale Mehrwertsteuerrückerstattung in Frage kommen

Arnie, Mitglied des Back-Office-Verarbeitungsteams von Contoso, ist dafür verantwortlich, zu überprüfen, ob alle erforderlichen Informationen für die Mehrwertsteuerrückerstattung in den Spesenabrechnungen enthalten sind. Er öffnet die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die Nancy eingereicht hat. Arnie überprüft dann, ob alle erforderlichen Belege beigefügt sind und ob die richtigen Mehrwertsteuergruppen und Artikel-Mehrwertsteuercodes eingegeben wurden.

Wenn Arnie die Papierbelege von Nancy erhält, überprüft er sie anhand der digitalen Belege und ändert dann den Status der Spesenabrechnung in **Bereit für Beitreibung**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Mehrwertsteuer-Erstattungsdaten an den Drittanbieter senden

Wenn Arnie bereit ist, die Spesenabrechnungsdaten an den Drittanbieter zu senden, der die Mehrwertsteuer-Erstattungserklärungen einreicht, öffnet er die Seite **Steuerrückerstattung**. Er filtert die Seite so, dass nur die Spesenabrechnungen angezeigt werden, die als **Bereit für Beitreibung** gekennzeichnet sind. Arnie wählt dann **Datei** &gt; **Nach Excel exportieren** aus. Die Umsatzsteuerinformationen aus den Spesenabrechnungen werden in das Microsoft Excel-Arbeitsblatt exportiert. Arnie sendet dieses Arbeitsblatt an den Drittanbieter und enthält eine Nachricht, die besagt, dass die Papierbelege per Kurier gesendet wurden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Prozesskosten für die inländische Mehrwertsteuerrückerstattung

Arnie muss überprüfen, ob die Spesenabrechnungstransaktionen für die Erstattung der Mehrwertsteuer in Frage kommen und ob die digitalen Belege den Berichten beigefügt sind. Um gültige Ausgaben für die inländische Rückforderung zu verarbeiten, öffnet Arnie die Seite **Steuerrückerstattung** und wählt die Spesenabrechnung aus, die überprüft werden muss. Er überprüft, ob die Belege auf den Namen des Unternehmens und nicht auf den des Mitarbeiters lauten. (Für die Mehrwertsteuerrückerstattung müssen die Belege im Namen des Unternehmens ausgestellt sein). Arnie überprüft dann, ob alle erforderlichen Belege beigefügt sind und ob die richtigen Mehrwertsteuergruppen und Artikel-Mehrwertsteuercodes eingegeben wurden.

Wenn Arnie die Papierbelege erhält, ändert er den Status der Spesenabrechnung in **Bereit für Beitreibung**. Er kann die Steuererklärung dann bei der zuständigen Steuerbehörde einreichen. In diesem Fall ist die entsprechende Steuerbehörde in den Vereinigten Staaten der Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]