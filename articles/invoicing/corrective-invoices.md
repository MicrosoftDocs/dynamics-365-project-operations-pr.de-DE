---
title: Projektbasierte Korrekturrechnungen erstellen
description: Dieser Artikel informiert Sie über Korrekturrechnungen in Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 86bb05242c74e97533c7555ffa645278c8519430
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927879"
---
# <a name="create-corrective-project-based-invoices"></a>Projektbasierte Korrekturrechnungen erstellen 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Eine bestätigte Projektrechnung kann korrigiert werden, um Änderungen oder Gutschriften zu verarbeiten, die mit dem Kunden und dem Projektmanager ausgehandelt wurden.

Um eine bestätigte Rechnung zu bearbeiten, öffnen Sie die bestätigte Rechnung und wählen Sie **Korrigieren Sie diese Rechnung** aus. 

> [!NOTE]
> Diese Auswahl ist nur verfügbar, wenn eine Projektrechnung bestätigt wurde.

Aus der bestätigten Rechnung wird ein neuer Rechnungsentwurf erstellt. Alle Rechnungszeilendetails aus der zuvor bestätigten Rechnung werden in den neuen Entwurf kopiert. Im Folgenden finden Sie einige wichtige Punkte, die Ihnen helfen sollen, mehr über die Zeilendetails auf der neuen Korrekturrechnung zu erfahren:

- Alle Mengen werden auf Null aktualisiert. Dies setzt voraus, dass alle in Rechnung gestellten Artikel vollständig gutgeschrieben werden. Bei Bedarf können Sie diese Mengen manuell aktualisieren, um die in Rechnung gestellte Menge und nicht die gutgeschriebene Menge widerzuspiegeln. Basierend auf der von Ihnen eingegebenen Menge berechnet die Anwendung die gutgeschriebene Menge. Dieser Betrag spiegelt sich in den Istwerten wider, die erstellt werden, wenn die korrigierte Rechnung bestätigt wird. Wenn Sie Änderungen am Steuerbetrag vornehmen, müssen Sie den richtigen Steuerbetrag eingeben und nicht den Steuerbetrag, der gutgeschrieben wird.
- Meilensteinkorrekturen werden immer als volle Gutschriften verarbeitet.
- Vorauszahlungs- oder Vorschussbeträge können korrigiert werden, wenn dem Kunden ein falscher Betrag in Rechnung gestellt wurde.
- Abstimmungen von Vorauszahlungen und Vorschüssen können korrigiert werden, wenn ein falscher Betrag verwendet wurde, um die Gebühren auf einer zuvor bestätigten Rechnung abzugleichen.

> [!IMPORTANT]
> Rechnungszeilendetails, bei denen es sich um Korrekturen zu anderen bereits in Rechnung gestellten Gebühren handelt, haben das **Korrektur**-Feld auf **Ja** gesetzt. Rechnungen mit korrigierten Rechnungszeilendetails haben ein Feld mit dem Namen **Hat Korrekturen**, das auch auf **Ja** eingestellt ist.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Istwerten, die bei Bestätigung einer Korrekturrechnung erstellt wurden

In der folgenden Tabelle sind die Istwerte aufgeführt, die erstellt werden, wenn eine Korrekturrechnung bestätigt wird.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Szenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Bei Bestätigung erstellte Istwerte</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Bestätigen Sie die Korrektur eines in Rechnung gestellten Vorschusses oder einer Vorauszahlung.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde Dieser Betrag ist positiv, da er das negative Ergebnis aufheben soll, das bei der Rechnungsstellung der Vorauszahlung oder des Vorschusses erstellt wurde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzistwert-Umkehrung wird für den Betrag in der Vorauszahlung oder im Vorschuss erstellt, um den ursprünglich fakturierten Umsatz umzukehren.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer fakturierter Umsatz-Istwert wird für den korrigierten Betrag in der vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile erstellt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein nicht fakturierter tatsächlicher Umsatz eines negativen Betrags einer vorauszahlungs- oder vorschussbasierten korrigierten Rechnungszeile, die für die Abstimmung verwendet wird.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Eine Bestätigung der Korrektur einer zuvor abgestimmten Vorauszahlung oder des Vorschusses.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung der Vorauszahlung oder des Vorschusses, der für die Abstimmung erstellt wurde Dieser Betrag ist positiv und soll das negative Ergebnis aufhaben, das beim Auftreten der vorherigen Abstimmung erstellt wurde.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzistwert-Umkehrung für den Betrag auf der vorherigen Rechnung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer fakturierter Umsatz-Istwert für den korrigierten Vorauszahlungsbetrag, der auf die korrigierte Rechnung angewendet wird.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein nicht fakturierter tatsächlicher Umsatz mit einem negativen Betrag aus der korrigierten restlichen Vorauszahlung oder dem Vorschuss, der zur Abstimmung auf späteren Rechnungen verwendet wird.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Zeittransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter Umsatz-Istwert für die Stunden und den Betrag des ursprünglichen Rechnungszeilendetails für Zeit
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung der Teilgutschrift bei einer Zeittransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Stunden und den Betrag, die im ursprünglichen Rechnungszeilendetail für Zeit in Rechnung gestellt wurden
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen auf dem Rechnungszeilendetail berechnet wird.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Ausgabentransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Ausgaben
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Ausgabentransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für eine Ausgabe in Rechnung gestellt wurden
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im Rechnungszeilendetail berechnet wird.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Gebührentransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter Umsatz-Istwert für die Menge und den Betrag im ursprünglichen Rechnungszeilendetail für die Gebühr
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung der Teilgutschrift einer zuvor in Rechnung gestellten Gebührentransaktion
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für die Menge und den Betrag, die im ursprünglichen Rechnungszeilendetail für die Gebühr in Rechnung gestellt wurde
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten korrigierten Rechnungszeilendetail berechnet wird, eine Umkehrung hiervon und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturierung des vollen Guthabens eines zuvor in Rechnung gestellten Meilensteins
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine fakturierte Umsatzumkehrung für den Betrag im ursprünglichen Rechnungszeilendetail für den Meilenstein
                </p>
                <p>
Der Rechnungsstatus des Meilensteins wird von <b>Gebuchte Kundenrechnung</b> zu <b>Bereit für die Rechnungsstellung</b> aktualisiert.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturierung der Teilgutschrift eines zuvor in Rechnung gestellten Meilensteins
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nicht unterstützt </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
