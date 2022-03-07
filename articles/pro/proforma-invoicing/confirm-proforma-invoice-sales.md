---
title: Eine Proforma-Projektrechnung bestätigen
description: Dieses Thema enthält Informationen zur Bestätigung von Proforma-Projektrechnungen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 37efb4923cbf9696ff85dfcd6dee9aac6badd68ed74a515e5ea5598aacfa3a83
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992970"
---
# <a name="confirm-a-proforma-project-invoice"></a>Eine Proforma-Projektrechnung bestätigen 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Nachdem eine Proforma-Rechnung bestätigt wurde, wird der Status der Projektrechnung auf **Bestätigt** aktualisiert. Wenn eine Rechnung bestätigt wird, ist sie schreibgeschützt. In Zukunft kann die Rechnung nur korrigiert werden, wenn vom Kunden initiierte Korrekturen oder Gutschriften vorliegen.

Die folgende Tabelle führt die Istwerte auf, die vom System erstellt wurden. Diese Istwerte werden erstellt, wenn bestimmte Vorgänge für den Entwurf der Projektrechnung ausgeführt werden, bevor dieser bestätigt wird.

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
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung eines Vorschusses oder einer Vorauszahlung </p>
            </td>
            <td width="408" valign="top">
                <p>
Ein fakturierter tatsächlicher Umsatz vom Typ <strong>Vorauszahlung</strong> wird für den Betrag im Vorschuss oder in der Vorauszahlung erstellt.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein nicht fakturierter tatsächlicher Umsatz eines negativen Betrags der Vorauszahlung oder des Vorschusses, der für die Abstimmung verwendet werden soll
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Nach vollständiger Abstimmung einer Vorauszahlung oder eines Vorschusses auf eine Rechnung
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
Ein fakturierter tatsächlicher Umsatz für den Betrag auf dieser Rechnung
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Nach teilweiser Abstimmung einer Vorauszahlung oder eines Vorschusses auf eine Rechnung
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
Ein fakturierter tatsächlicher Umsatz für den Betrag auf dieser Rechnung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein negativer nicht fakturierter tatsächlicher Umsatz des verbleibenden Vorauszahlungs- oder Vorschussbetrags, der zur Abstimmung in künftigen Rechnungen verwendet werden soll
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer Zeittransaktion ohne Änderungen am Rechnungsentwurf
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein fakturierter tatsächlicher Umsatz für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu reduzieren
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung
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
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibenden Stunden und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer Zeittransaktion, die bearbeitet wurde, um die Menge zu erhöhen
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Stunden und den Betrag der ursprünglichen Zeitgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Stunden und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer Ausgabentransaktion ohne Änderungen am Rechnungsentwurf
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu reduzieren
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer Ausgabentransaktion, die bearbeitet wurde, um die Menge zu erhöhen
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für die Menge und den Betrag der ursprünglichen Auftragsgenehmigung
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer wesentlichen Transaktion ohne Änderungen am Rechnungsentwurf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht in Rechnung gestellte Umsatzstornierung für die Menge und den Betrag in der ursprünglichen Materialverbrauchsgenehmigung.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein abgerechneter vertrieblicher Ist-Wert für die Menge und den Betrag in der ursprünglichen Materialverbrauchsgenehmigung.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung einer Materialtransaktion, die bearbeitet wurde, um die Menge zu reduzieren.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht in Rechnung gestellte Umsatzstornierung für die Menge und den Betrag in der ursprünglichen Zeitgenehmigung.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die verbleibende Menge und den Betrag nach Abzug der korrigierten Zahlen im bearbeiteten Rechnungszeilendetail nicht fakturierbar ist, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturierung einer Materialtransaktion, die bearbeitet wurde, um die Menge zu erhöhen.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht in Rechnung gestellte Umsatzstornierung für die Menge und den Betrag in der ursprünglichen Materialverbrauchsgenehmigung.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht fakturierter tatsächlicher Umsatz, der für die Menge und den Betrag im bearbeiteten Rechnungszeilendetail berechnet wird, eine Umkehrung des nicht fakturierten tatsächlichen Umsatzes und ein gleichwertiger fakturierter tatsächlicher Umsatz
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturieren einer Gebühr
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine nicht fakturierte Umsatzumkehrung für Gebührenbetrag der ursprünglichen Erfassungsposition
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein fakturierter tatsächlicher Umsatz für die Menge und den Betrag der ursprünglichen Erfassungsposition der Gebühr.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturierung eines Meilensteins
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ein in Rechnung gestellter tatsächlicher Umsatz für den Meilensteinbetrag im ursprünglichen Meilenstein in der Projektvertragszeile
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturieren einer produktbasierenden Vertragszeile
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ein fakturierter tatsächlicher Umsatz für die Produktzeile mit der Menge und dem Betrag aus der produktbasierten Vertragszeile
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
