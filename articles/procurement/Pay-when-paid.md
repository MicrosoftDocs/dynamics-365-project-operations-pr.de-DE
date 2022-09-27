---
title: Pay-When-Paid-Kreditorenzahlungen
description: In diesem Thema wird erläutert, wie das Pay-When-Payed-Szenario (PWP) verwendet wird.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525335"
---
# <a name="pay-when-paid-vendor-payments"></a>Pay-When-Paid-Kreditorenzahlungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In diesem Thema wird erläutert, wie das Pay-When-Payed-Szenario (PWP) verwendet wird.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Erstellen Sie eine Bestellung mit PWP-Bedingungen

Wenn Sie eine Rechnung von einem Kreditor buchen und der Kreditor PWP-Bedingungen unterliegt, werden diese Bedingungen in der Bestellposition angezeigt. Um eine Bestellung mit PWP-Bedingungen zu erstellen, befolgen Sie diese Schritte.

1. Befolgen Sie in Microsoft Dynamics 365 Finance mindestens einen der folgenden Schritte:

    - Navigieren Sie zu **Beschaffung und Einkauf** \> **Einkaufsbestellungen** \> **Alle Einkaufsbestellungen**. Wählen Sie im Aktionsbereich **Neu** aus. Wählen Sie im **Bestellung erstellen**-Dialogfeld den Anbieter aus, für den PWP-Bedingungen für das Projekt eingerichtet wurden, geben Sie weitere erforderliche Informationen ein und wählen Sie dann **OK** aus.
    - Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**. Wählen Sie im Aktionsbereich auf der Registerkarte **Verwalten** die Option **Artikelaufgabe**. Wählen Sie die Bestellung aus. Wählen Sie den Anbieter aus, für den PWP-Bedingungen für das Projekt eingerichtet wurden, und wählen Sie dann **OK**.

2. Wählen Sie auf der **Bestellung**-Seite auf dem Inforegister **Bestellpositionen** **Zeile hinzufügen** aus, um eine Bestellposition zu erstellen.
3. Wählen Sie die Artikelnummer oder die Beschaffungskategorie aus und geben Sie die anderen erforderlichen Details ein. Überprüfen Sie die Details des Bestellpostens für den Lieferanten.

    Die Option **Pay When Paid** wird automatisch ausgewählt, und der Wert im Feld **Pay When Paid - Schwellenwertprozentsatz** wird automatisch aus dem Feld **Pay When Paid - Schwellenwertprozentsatz** auf der Seite **Projekte** kopiert.

4. Wenn Sie keine PWP-Bedingungen für eine Bestellposition auf den Kreditor anwenden möchten, deaktivieren Sie das Kontrollkästchen **Pay When Paid**. In diesem Fall wird das Feld **Pay When Paid - Schwellenwertprozentsatz** für die Bestellzeile auf **0** (null) zurückgesetzt.
5. Klicken Sie im Aktivitätsbereich auf der Seite **Bestellung** auf der Registerkarte **Kauf** auf **Bestätigen**, um die Bestellung zu bestätigen.
6. Wählen Sie im Aktionsbereich auf der Registerkarte **Rechnung** **Rechnung**, um die Rechnung für die Bestellung zu erstellen.

## <a name="create-a-project-invoice-proposal"></a>Projektrechnungsvorschlag erstellen

Projektrechnungsvorschläge werden verwendet, um Projektrechnungen für den Kunden zu erstellen. Im PWP-Szenario sind Lieferantenzahlungen gemäß den PWP-Einstellungen von Kundenzahlungen abhängig. Es gibt jedoch Optionen, mit denen Sie die Zahlungen ohne Kundenzahlungen nach Bedarf freigeben können. Um eine Projektrechnung für den Kunden zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie in Customer Engagement-Apps zu **Projekt** \> **Projekte**, und wählen Sie das Projekt aus.
2. Wählen Sie auf der **Istwerte**-Registerkarte die tatsächliche Zeile aus, die von der Bestellung generiert wird, die den **Nicht fakturierte Umsätze**-Transaktionstyp hat. Wählen Sie dann **Bereit für Rechnung**.
3. Gehen Sie zu **Vertrieb** \> **Vertrieb** \> **Projektvertrag**, und wählen Sie den Projektvertrag aus.
4. Wählen Sie im Aktionsbereich **Rechnung**, um die Kundenrechnung zu erstellen.
5. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** \> **Periodisch** \> **Import aus Staging-Tabelle**, und wählen Sie **OK**, um das Integrationsjournal für Project Operations zu erstellen.
6. Gehen Sie zu **Projektmanagement und -buchhaltung** \> **Projektrechnungen** \> **Projektrechnungsvorschlag**, und wählen Sie **Buchen**, um den für das Projekt generierten Rechnungsvorschlag zu buchen.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Eine Kundenzahlung aktualisieren und den Kreditor bezahlen

Wenn ein Kreditor seine Arbeit an einem Projekt abgeschlossen hat und Ihnen eine Rechnung sendet, müssen Sie den Projektstatus und die Kundenrechnungen überprüfen, um festzustellen, ob die PWP-Bedingungen für das Projekt erfüllt wurden. Wenn die PWP-Bedingungen für den Kreditor erfüllt wurden, können Sie anhand der Kundenzahlungen für das Projekt bestimmen, welche Zeilen auf der Kreditorenrechnung zu bezahlen sind. Wenn Sie den Kreditor bezahlen möchten, obwohl die PWP-Bedingungen nicht erfüllt wurden, können Sie die PWP-Bedingungen auf der Seite **Kreditorenrechnung mit Pay When Paid** überschreiben.

1. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** \> **Projekte** \> **Alle Projekte** und wählen Sie ein Projekt aus.
2. Wählen Sie im Aktivitätsbereich **Steuerung**, und wählen Sie dann **Kreditorenrechnungen**, um alle Kreditorenrechnungen anzuzeigen, die für das Projekt generiert wurden.
3. Geben Sie auf der Seite **Kreditorenrechnungen mit Pay When Paid** im Suchfeld die Werte ein, um die Kreditorenrechnung zu finden, die Sie überprüfen möchten, und wählen Sie dann **Suchen** aus.
4. Wählen Sie die **Pay When Paid**-Option, um nur PWP-Rechnungen anzuzeigen.
5. Wählen Sie im Inforegister **Kreditorenrechnungspositionen** die Zeilen aus, die Sie für die Zahlung freigeben möchten.
6. Wählen Sie **Kreditorenzahlung freigeben**. Die Option **Pay When Paid** wird gelöscht, und der Wert für das Feld **Bereit für Zahlung** wird in **Ja** geändert.
