---
title: Kreditorenrechnungspositionen für Produkte
description: In diesem Artikel wird erklärt, wie Sie Zeilen für Einkaufsrechnungen für Produkte erfassen und die verschiedenen Felder verwenden, um den Kauf von Produkten bei den Lieferanten zu erfassen.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931375"
---
# <a name="vendor-invoice-lines-for-products"></a>Kreditorenrechnungspositionen für Produkte

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Kreditorenrechnung in Microsoft Dynamics 365 Project Operations kann Kreditorenrechnungspositionen für Produkte (auch als Materialien bezeichnet) haben. Projektmanager können Kreditorenrechnungspositionen für Produkte verwenden, um die Kosten von Produkten zu erfassen, die für Projekte gekauft wurden.

Kreditorenrechnungspositionen für Produkte können auf eine Fremdarbeitsposition für Materialien verweisen oder auch nicht. Wenn eine Kreditorenrechnungsposition für Produkte auf eine Fremdarbeit verweist, können Projektmanager die Produkte, die von der Kreditorenrechnungsposition in Rechnung gestellt werden, mit der Verwendung gekaufter Produkte abgleichen, die von Projektmanagern erfasst und genehmigt wurden.

Die folgende Tabelle enthält Informationen zu den Feldern auf Kreditorenrechnungspositionen für Produkte.

| Feld | Beschreibung des Dataflows | Funktionsauswirkung |
| --- | --- | --- |
| Name des Dataflows | Der Name der Kreditorenrechnungsposition, um bei der Identifizierung zu helfen. | Dieser Name wird als erste Spalte in allen Nachschlagevorgängen angezeigt, die auf Kreditorenrechnungspositionen basieren. |
| Beschreibung des Dataflows | Eine kurze Beschreibung der Produkte, die vom Kreditor in der Kreditorenrechnungsposition in Rechnung gestellt werden. | Nein |
| Fremdarbeit | Die Fremdarbeit, für die die Produkte ursprünglich bestellt wurden. | Wenn eine Fremdarbeit für die Kreditorenrechnung ausgewählt wird, erben alle Zeilen auf der Kreditorenrechnung diese Auswahl. Eine Kreditorenrechnung darf keine Kreditorenrechnungspositionen haben, die auf verschiedene Fremdarbeiten verweisen. |
| Fremdarbeitsposition | Die Fremdarbeitsposition, für die die Produkte bestellt wurden. Die Liste der auswählbaren Fremdarbeitspositionen ist auf die Positionen der ausgewählten Fremdarbeit beschränkt. | Wenn eine Fremdarbeitsposition in einer Kreditorenrechnungsposition für Produkte ausgewählt wird, werden Standardwerte für die Felder **Projekt**, **Aufgabe** und **Produkt** werden aus den entsprechenden Feldern in der Fremdarbeitsposition eingegeben. Wenn die ausgewählte Fremdarbeitsposition Werte in den Feldern **Projekt**, **Aufgabe** und **Produkt** hat, können die Werte der entsprechenden Felder in der Kreditorenrechnungsposition nicht von diesen Werten abweichen. |
| Buchungsdatum | Das Datum, an dem die tatsächlichen Kosten der Kreditorenrechnungsposition im Projekt erfasst werden. | Nein|
| Transaktionsklasse | Wenn Produkte in Rechnung gestellt werden, sollte dieses Feld auf **Material** gesetzt werden. | Der Wert **Material** gibt an, dass die Kreditorenrechnungsposition verwendet wird, um den Rechnungsbetrag für Materialen zu erfassen, die beschafft wurden. |
| Project | Der Name des Projekts, für das die in Rechnung gestellten Produkte verwendet wurden. | Dieses Feld ist ein Pflichtfeld und darf nicht leer gelassen werden. |
| Task | Der Name der Projektaufgabe, für das die in Rechnung gestellten Produkte verwendet wurden. Dieses Feld ist nur verfügbar, wenn ein Projekt ausgewählt ist. Die Auswahl einer Projektaufgabe ist optional. | Wenn dieses Feld leer gelassen wird, kann der Projektmanager die Kreditorenrechnungsposition mit gekaufen Produkten abgleichen, die für einen beliebigen Vorgang des Projekts verwendet wurden. Wenn die Kreditorenrechnungsposition nicht auf eine Fremdarbeitsposition verweist und dieses Feld leer gelassen wird, werden die Ist-Kosten, die von der Kreditorenrechnungsposition erstellt werden, nicht mit noch nicht fakturierten Verkaufs-Ist-Werten verknüpft. In diesem Fall werden bei eingerichteter aufgabenbezogener Abrechnung die Kosten dem Endkunden ggf. nicht in Rechnung gestellt. |
| Produkt auswählen | Wählen Sie aus, ob das fakturierte Produkt ein vorhandenes Produkt aus dem Katalog ist oder ein manuell einzutragendes Produkt. | Der Standardwert wird aus der Untervertragsposition eingegeben, wenn eine Untervertragsposition ausgewählt wird. |
| Produkt | Wählen Sie das Produkt aus dem Katalog aus. Wenn das Produkt ein manuell einzutragendes Produkts ist, geben Sie dann den Namen des Produkts ein. | Dieses Feld wird verwendet, um Standardeinkaufspreise für vorhandene Produkte einzugeben. |
| Menge | Geben Sie die vom Kreditor in Rechnung gestellte Materialmenge in dieser Rechnungsposition ein. | Nein |
| Einheitengruppe | Wählen Sie die Einheitengruppe der Einheit aus, in der die fakturierte Menge ausgedrückt wird. | Nein |
| Einheit | Der Standardwert ist die Basiseinheit der ausgewählten Einheitengruppe. Sie können diesen Wert ändern, um eine beliebige Einheit der ausgewählten Einheitengruppe zu bezahlen. | Die Kombination der Werte **Produkt** und **Einheit** wird als Standardwert verwendet oder für das Feld **Einheitspreis** für die Kreditorenrechnungsposition berechnet. |
| Einheitenpreis | Der Standardeinheitspreis verwendet die Kombination der Werte **Produkt** und **Einheit** aus der Projektpreisliste, die für das Transaktionsdatum der Kreditorenrechnungsposition gilt. | Nein |
| Zwischensumme | Dies ist ein schreibgeschütztes Feld, das als *Menge* &times; *Stückpreis* berechnet wird, wenn Werte in das Feld **Menge** und in das Feld **Stückpreis** eingegeben werden. Wenn eines oder beide Felder leer sind, können Sie in dieses Feld einen Wert eingeben. | Nein |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein. | Nein |
| Gesamtbetrag | Der Gesamtbetrag der Kreditorenrechnungsposition, einschließlich Steuern. Dieses Feld wird als *Zwischensumme* + *Mehrwertsteuer* berechnet. | Nein |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
