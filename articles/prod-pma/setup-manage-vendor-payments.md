---
title: Pay-When-Paid-Kreditorenzahlungen einrichten und verwenden
description: In diesem Thema wird erläutert, wie Sie Pay-When-Paid-Bedingungen (PWP) erstellen, damit Sie teilweise Kreditorenzahlungen basierend auf Kundenzahlungen freigeben können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288594"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Pay-When-Paid-Kreditorenzahlungen einrichten und verwenden

[!include [banner](../includes/banner.md)]

Wenn Sie einem Kreditor die Genehmigung erteilen, als Zulieferer zu arbeiten, möchten Sie möglicherweise die Zahlung an den Kreditor zurückhalten, bis Ihr Kunde Sie für das Projekt bezahlt. Um dieses Szenario zu unterstützen, können Sie PWP-Bedingungen (Pay-When-Paid) einrichten, wenn Sie die Bestellung (PO) beim Lieferanten einrichten.

Wenn ein Kunde beispielsweise einen Betrag auf einer Projektrechnung bezahlt, können Sie einen Teil oder den gesamten Rechnungsbetrag des Kreditors freigeben. Richten Sie einfach PWP-Bedingungen ein, die festlegen, dass der Kreditor bezahlt wird, nachdem Sie einen Prozentsatz der entsprechenden Zahlung vom Kunden erhalten haben. Wenn Sie eine Teilzahlung von einem Kunden erhalten, können Sie einige der zugehörigen Kreditorenrechnungen manuell zur Zahlung freigeben.

Das folgende Beispiel beschreibt den Prozess bei Verwendung von PWP-Bedingungen.

## <a name="example"></a>Beispiel

Ihre Organisation erklärt sich damit einverstanden, einem Kunden 100 Computer mit installierter Software zum Preis von 150,00 US-Dollar (USD) pro Computer zur Verfügung zu stellen. Anschließend beauftragen Sie einen Kreditor mit der Bereitstellung der Computer, auf denen Software installiert ist. Gemäß der Vereinbarung muss der Kunde die Qualität der Computer genehmigen, bevor er Ihre Organisation bezahlt. Die Richtlinie Ihres Unternehmens besteht darin, Zahlungen an Kreditoren zurückzuhalten, bis der Kunde Sie bezahlt hat. Daher richten Sie das Projekt so ein, dass es einen PWP-Prozentsatz von 100 Prozent aufweist.

Der Kreditor sendet Ihnen die 100 Computer, auf denen Software installiert ist, zusammen mit einer Rechnung für 10.000,00 USD. Da für Ihr Projekt PWP-Bedingungen eingerichtet sind, bezahlen Sie den Kreditor nicht nach Erhalt der Computer. Stattdessen senden Sie die Computer zusammen mit einer Rechnung für 15.000,00 an den Kunden. Der Kunde inspiziert die Computer und genehmigt den vollen Betrag der Projektrechnung.

Nachdem Sie die vollständige Zahlung vom Kunden erhalten haben, zahlen Sie dem Kreditor 10.000,00. Dies ist der volle Betrag der Kreditorenrechnung.

## <a name="set-up-pwp-terms-for-a-project"></a>PWP-Bedingungen für ein Projekt einrichten

Wenn Sie PWP-Bedingungen für ein Projekt einrichten, müssen Sie als Prozentsatz den Mindestbetrag angeben, den ein Kunde für das Projekt bezahlen muss, bevor Sie den Kreditor bezahlen. Der Schwellenbetrag wird automatisch auf den Kundenrechnungen für das Projekt berechnet. Befolgen Sie diese Schritte, um den Schwellenprozentsatz für PWP-Bedingungen festzulegen.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**.
2. Suchen und öffnen Sie das Projekt, für das Sie PWP-Bedingungen einrichten möchten.
3. Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Zeile hinzufügen** aus.
3. Wählen Sie im Feld **Kontocode** eine der folgenden Optionen aus:

    - **Tabelle** – Die PWP-Bedingungen gelten für einen einzelnen Kreditor.
    - **Gruppe** – Die PWP-Bedingungen gelten für alle Kreditoren in einer Kreditorengruppe.
    - **Alle** – Die PWP-Bedingungen gelten für alle Kreditoren.

4. Wenn Sie **Tabelle** oder **Gruppe** im vorherigen Schritt im Feld **Kreditor/Kreditorengruppe** ausgewählt haben, wählen Sie den Kreditor oder die Kreditorengruppe aus, auf die die PWP-Bedingungen zutreffen. Wenn Sie **Alle** im vorherigen Schritt ausgewählt haben, kann das Feld **Kreditor/Kreditorengruppe** nicht bearbeitet werden.
5. Wenn für den Kreditor im Projekt Bedingungen für die Einbehaltung eingerichtet sind, wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Regel-ID für die Bedingungen zur Einbehaltung aus.
6. Geben Sie im Feld **Pay When Paid - Schwellenwertprozentsatz** den Schwellenwertprozentsatz für das Projekt ein. Der Prozentsatz, den Sie für das Projekt eingeben, definiert den Mindestbetrag, den der Kunde Ihnen zahlen muss, bevor Sie den Kreditor bezahlen.

## <a name="create-a-po-that-has-pwp-terms"></a>Eine Bestellung mit PWP-Bedingungen

Wenn Sie eine Rechnung von einem Kreditor buchen und der Kreditor PWP-Bedingungen unterliegt, werden diese Bedingungen in der Bestellposition angezeigt. Um eine Bestellung mit PWP-Bedingungen zu erstellen, befolgen Sie diese Schritte.

1. Navigieren Sie zu **Beschaffung und Einkauf** \> **Einkaufsbestellungen** \> **Alle Einkaufsbestellungen**.
2. Wählen Sie im Aktionsbereich **Neu** aus. Geben Sie dann im Dialogfeld **Bestellung anlegen** die erforderlichen Informationen ein, und wählen Sie **OK** aus.

    Alternativ können Sie eine vorhandene Bestellung auf der Listenseite **Alle Bestellungen** öffnen.

4. Prüfen Sie auf der Seite **Bestellung** im Inforegister **Bestellposition** die Details der Bestellposition für den Kreditor. Die Option **Pay When Paid** wird automatisch ausgewählt, und der Wert im Feld **Pay When Paid - Schwellenwertprozentsatz** wird automatisch aus dem Feld **Pay When Paid - Schwellenwertprozentsatz** auf der Seite **Projekte** kopiert.
6. Wenn Sie keine PWP-Bedingungen für eine Bestellposition auf den Kreditor anwenden möchten, deaktivieren Sie das Kontrollkästchen **Pay When Paid**. In diesem Fall wird das Feld **Pay When Paid - Schwellenwertprozentsatz** für die Bestellzeile auf 0 (null) zurückgesetzt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Eine Kundenzahlung aktualisieren und den Kreditor bezahlen

Wenn ein Kreditor seine Arbeit an einem Projekt abgeschlossen hat und Ihnen eine Rechnung sendet, müssen Sie den Projektstatus und die Kundenrechnungen überprüfen, um festzustellen, ob die PWP-Bedingungen für das Projekt erfüllt wurden. Wenn die PWP-Bedingungen für den Kreditor erfüllt wurden, können Sie anhand der Kundenzahlungen für das Projekt bestimmen, welche Zeilen auf der Kreditorenrechnung zu bezahlen sind. Wenn Sie den Kreditor bezahlen möchten, obwohl die PWP-Bedingungen nicht erfüllt wurden, können Sie die PWP-Bedingungen auf der Seite **Kreditorenrechnung mit Pay When Paid** überschreiben.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Anfragen und Berichte** \> **Einbehaltungsabfragen** \> **Kreditorenrechnung mit Pay When Paid**.
2. Geben Sie auf der Seite **Kreditorenrechnungen mit Pay When Paid** im Suchfeld die Werte ein, um die Kreditorenrechnung zu finden, die Sie überprüfen möchten, und wählen Sie dann **Suchen** aus.
3. Wählen Sie im Inforegister **Kreditorenrechnungspositionen** die Zeilen aus, die Sie ändern möchten.
4. Wenn die **Pay When Paid**-Bedingungen für die Rechnungszeile erfüllt sind, wählen Sie **Kreditorenzahlung freigeben** aus. Die Option **Pay When Paid** wird gelöscht, und der Wert für das Feld **Bereit für Zahlung** wird in **Ja** geändert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]