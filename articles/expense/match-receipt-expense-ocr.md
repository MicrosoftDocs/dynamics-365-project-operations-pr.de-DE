---
title: Eine Quittung mit OCR erfassen
description: Dieses Thema enthält Informationen zur optischen Zeichenerkennung (OCR) für Quittungen.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d4c2cce88514e7822515fc407fc7cf31cb34924
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596279"
---
# <a name="capture-a-receipt-using-ocr"></a>Eine Quittung mit OCR erfassen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die Ausgabenerfassung wurde durch die Einführung der optischen Zeichenerkennungsverarbeitung (OCR) für Belege verbessert. Diese Funktionalität soll die Benutzererfahrung beim Erstellen von Ausgabenabrechnungen verbessern.

## <a name="key-features"></a>Schlüsselfunktionen

- Das System extrahiert den Händlernamen, das Datum und den Gesamtbetrag aus den Belegen.
- Das System versucht, nicht angehängte Belege mit nicht angehängten Kostentransaktionen abzugleichen.
- Sie können manuell eingegebene Aufwandsbuchungen aus Belegen erstellen.

## <a name="attach-receipts-to-an-expense-report"></a>Anhängen von Belegen an eine Spesenabrechnung

Führen Sie die folgenden Schritte aus, um beim Erstellen einer Spesenabrechnung automatisch Belege mit Kreditkartentransaktionen anzuhängen.

  1. Öffnen des Arbeitsplatzes **Ausgabenmanagement**.
  2. Auf der Registerkarte **Quittungen** überprüfen Sie auf der Registerkarte, ob nicht angehängte Belege vorhanden sind. Sie können auch Belege auf die Registerkarte **Quittungen** hochladen.
  3. Auf der Registerkarte **Ausgaben** überprüfen Sie, dass  nicht angehängte Ausgaben vorhanden sind. In der Regel importiert der Ausgabenadministrator diese Ausgaben vom Kreditkartenanbieter.
  4. **Neuer Ausgabenbericht** auswählen. Beachten Sie, dass Sie jetzt auch Ausgaben und Belege einbeziehen können, wenn Sie eine Ausgabenabrechnung erstellen. Wenn Sie sowohl Ausgaben als auch Belege hinzufügen, wird ein automatischer Abgleich der Belege mit den Ausgaben ausgelöst.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Belege für einen Ausgabenbericht erstellen oder abgleichen
Führen Sie die folgenden Schritte aus, um eine Ausgabe zu erstellen oder eine Ausgabe aus einer Quittung abzugleichen.

  1. Auf einem Ausgabenbericht auf der Registerkarte **Quittungen** fügen Sie eine Quittung hinzu, indem Sie **Quittungen hinzufügen** auswählen.
  2. Beachten Sie unter dem hochgeladenen Bild der Quittung die Optionen **Erstellen** und **Abstimmen**.

      - Wählen Sie **Erstellen**, um eine manuell eingegebene Aufwandsbuchung zu erstellen und die Werte einzugeben, die aus dem Beleg extrahiert werden.
      - Wenn Sie **Abstimmen** auswählen, versucht das System, eine vorhandene Ausgabe mit der Quittung abzugleichen.

## <a name="installation"></a>Installation

Wenn Sie diese erweiterten Ausgabenfunktionen nutzen möchten, installieren Sie das Add-In für den Spesenverwaltungsdienst für Microsoft Microsoft Dynamics 365 Finance und aktivieren Sie die Funktionen in Ihrer Instance. Sie können von Ihrem Projekt aus auf das Add-In Microsoft Dynamics Lifecycle Services (LCS) zugreifen.

1. Melden Sie sich bei LCS an, und öffnen Sie die gewünschte Umgebung.
2. Gehen Sie zu **Alle Einzelheiten**.
3. Wählen Sie **Verwalten** oder blättern Sie nach unten zur Registerkarte **Umgebungs-Add-Ins**.
4. Wählen Sie **Installieren Sie ein neues Add-In**.
5. Wählen Sie **Ausgabenberwaltungsdienst** aus.
6. Befolgen Sie die Installationsanleitung und stimmen Sie den Nutzungsbedingungen zu.
7. Wählen Sie **Installieren** aus.

In dem Arbeitsbereich **Funktionsverwaltung** aktivieren Sie die folgenden Funktionen:

- Neu gestaltete Ausgabenabrechnungen
- Automatische Zuordnung und Erstellung von Kosten ab Quittung

Wenn Sie diese Funktionen aktivieren, werden die folgenden Aktionen ausgeführt:

- Der bestehende Arbeitsbereich **Ausgabenmanagement** wird durch den neuen Arbeitsbereich ersetzt.
- Ein neuer Menüpunkt für die Sichtbarkeit der Kostenfelder wurde hinzugefügt.
- Sie können die Seite **Ausgabenbericht** immer noch öffnen. Gehen Sie dazu zu **Ausgabenmanagement > Meine Ausgaben> Ausgabenabrechnungen**.
- Workflows und Genehmigungen führen Sie weiterhin zur vorhandenen Seite mit den Ausgabenabrechnungen.
- Quittungen werden durch Microsoft Azure Cognitive Services verarbeitet und Metadaten werden extrahiert und hinzugefügt.
- Es wurde eine Option hinzugefügt, mit der Sie eine Ausgabenabrechnung erstellen können, die übereinstimmende, nicht angehängte Belege enthält.
- Mit einer Option, die Ausgabenabrechnungen hinzugefügt wird, können Sie eine Ausgabenzeile aus einer Quittung erstellen oder versuchen, eine vorhandene Quittung einer vorhandenen Ausgabenzeile zuzuordnen.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

**Verwendet Microsoft meine Daten für seine Modelle?**

Nein, Microsoft hat ein allgemeines Maschinelles Lernen-Modell für seinen Belegverarbeitungsdienst erstellt. Dieses Modell basiert nicht auf den von Ihnen hochgeladenen Belegen.

**Wo ist diese Funktion verfügbar und wird sie verarbeitet?**

Die Verfügbarkeit dieser Funktion in verschiedenen Regionen ist in der folgenden Tabelle aufgeführt. Wenn Ihre Region derzeit nicht unterstützt wird, senden Sie eine Anfrage, um die Verfügbarkeit des OCR-Dienstes in Ihrer Region zu priorisieren. 

| Region | Unterstützt                         |
|--------|-----------------------------------|
| USA    | Ja                               |
| CAN    | Ja                               |
| UK     | Ja                               |
| AUS    | Ja                               |
| EU     | Teilweise. Nur englische Belege. |
| Asien   | Nr.                                |
| Japan  | Nr.                                |
| Afrika | Nr.                                |

**Wohin gehen meine Quittungen?**

Finance wird sich an Cognitive Services wenden, um die Felddaten zu extrahieren. Cognitive Services bewahrt eine Kopie Ihrer Quittung bis zu 24 Stunden lang auf, während die Verarbeitung erfolgt. Nach Abschluss der Verarbeitung entfernt Cognitive Services die Quittung. Belege werden weiterhin in Finanzen gespeichert.

Weitere Informationen finden Sie unter [Aktivieren Sie das Belegverständnis mit der neuen Funktion der Formularerkennung](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
