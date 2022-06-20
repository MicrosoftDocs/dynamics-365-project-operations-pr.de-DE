---
title: Projektbasierte Korrekturrechnungen
description: Dieser Artikel informiert Sie darüber, wie Sie in Project Operations Korrekturrechnungen für ein Projekt erstellen und bestätigen können.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eecaf3dedeab5ff72d12808eb3144f9161313009
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931099"
---
# <a name="corrective-project-based-invoices"></a>Projektbasierte Korrekturrechnungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Eine bestätigte Projektrechnung kann korrigiert werden, um Änderungen oder Gutschriften zu verarbeiten, die mit dem Kunden und dem Projektmanager ausgehandelt wurden.

Um eine bestätigte Rechnung zu bearbeiten, öffnen Sie die bestätigte Rechnung und wählen Sie **Korrigieren Sie diese Rechnung** aus. 

> [!NOTE]
> Diese Auswahl ist nur verfügbar, wenn eine Projektrechnung bestätigt wurde oder die projektbasierte Rechnung Vorschüsse oder Vorbehalte oder Abstimmungen von Vorschüssen oder Vorbehalten enthält.

Aus der bestätigten Rechnung wird ein neuer Rechnungsentwurf erstellt. Alle Rechnungszeilendetails aus der zuvor bestätigten Rechnung werden in den neuen Entwurf kopiert. Im Folgenden sind einige der wichtigsten Punkte aufgeführt, die Sie zum Verständnis der Zeilendetails auf der neuen korrigierten Rechnung beachten sollten:

- Alle Mengen werden auf Null aktualisiert. Dynamics 365 Project Operations setzt voraus, dass alle in Rechnung gestellten Artikel vollständig gutgeschrieben werden. Bei Bedarf können Sie diese Mengen manuell aktualisieren, um die in Rechnung gestellte Menge und nicht die gutgeschriebene Menge widerzuspiegeln. Basierend auf der von Ihnen eingegebenen Menge berechnet die Anwendung die gutgeschriebene Menge. Dieser Betrag spiegelt sich in den Istwerten wider, die erstellt werden, wenn die korrigierte Rechnung bestätigt wird. Wenn Sie Änderungen am Steuerbetrag vornehmen, müssen Sie den richtigen Steuerbetrag eingeben und nicht den Steuerbetrag, der gutgeschrieben wird.
- Meilensteinkorrekturen werden immer als volle Gutschriften verarbeitet.


> [!IMPORTANT]
> Für Rechnungszeilendetails, bei denen es sich um Korrekturen zu anderen bereits in Rechnung gestellten Gebühren handelt, wird das **Korrektur**-Feld auf **Ja** gesetzt. Für Rechnungen mit korrigierten Rechnungszeilendetails wird das **Hat Korrekturen**-Feld auf **Ja** gesetzt.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Tatsächliche Transaktionen werden erstellt, wenn eine Korrekturrechnung bestätigt wird

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
Fakturierung des vollen Guthabens einer zuvor in Rechnung gestellten Materialtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine in Rechnung gestellte Umsatzstornierung für die Menge und den Betrag in der ursprünglichen Rechnungszeile für das Material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Eine neue noch nicht in Rechnung gestellte tatsächliche Verkaufstransaktion für die Menge und den Betrag in der ursprünglichen Rechnungszeile für das Material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturierung der Teilgutschrift für eine Materialtransaktion.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Eine in Rechnung gestellte Umsatzstornierung für die Menge und den berechneten Betrag in der ursprünglichen Rechnungszeile für das Material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Ein neuer nicht in Rechnung gestellter tatsächlicher Umsatz, der für die Menge und den Betrag in den bearbeiteten Rechnungszeilendetails berechnet wird, eine Umkehrung davon und ein gleichwertiger in Rechnung gestellter tatsächlicher Umsatz.
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
Dies ist kein unterstütztes Szenario.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
