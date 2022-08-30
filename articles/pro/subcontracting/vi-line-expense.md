---
title: Kreditorenrechnungspositionen für Ausgabenkategorien
description: Dieser Artikel erklärt, wie Sie Zeilen für Lieferantenrechnungen für Ausgabenkategorien erfassen können.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261681"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Kreditorenrechnungspositionen für Ausgabenkategorien

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Kreditorenrechnung in Microsoft Dynamics 365 Project Operations kann Kreditorenrechnungspositionen für Ausgabenkategorien haben. Projektmanager können Kreditorenrechnungspositionen für Ausgabenkategorien verwenden, um die Kosten von Dienstleistungen zu erfassen, die als Ausgabenkategorien beschafft werden.

Kreditorenrechnungspositionen für Ausgabenkategorien können auf eine Fremdarbeitsposition für Ausgabenkategorien verweisen oder auch nicht. Wenn eine Kreditorenrechnungsposition für Ausgabenkategorien auf eine Fremdarbeit verweist, können Projektmanager die Ausgaben, die von der Kreditorenrechnungsposition in Rechnung gestellt werden, mit Ausgaben abgleichen und überprüfen, die in diesen Ausgabenkategorien erfasst und von Projektmanagern für das Projekt genehmigt wurden.

Die folgende Tabelle enthält Informationen zu den Feldern auf Kreditorenrechnungspositionen für Ausgabenkategorien.

| Feld | Beschreibung des Dataflows | Funktionsauswirkung |
| --- | --- | --- |
| Name des Dataflows | Der Name der Kreditorenrechnungsposition, um bei der Identifizierung zu helfen. | Dieser Name wird als erste Spalte in allen Nachschlagevorgängen angezeigt, die auf Kreditorenrechnungspositionen basieren. |
| Beschreibung des Dataflows | Eine kurze Beschreibung der Dienste, die vom Kreditor in der Kreditorenrechnungsposition in Rechnung gestellt werden. | Nein |
| Fremdarbeit | Die Fremdarbeit, für die die Dienste ursprünglich bestellt wurden. | Wenn eine Fremdarbeit für die Kreditorenrechnung ausgewählt wird, erben alle Zeilen auf der Kreditorenrechnung diese Auswahl. Eine Kreditorenrechnung darf keine Kreditorenrechnungspositionen haben, die auf verschiedene Fremdarbeiten verweisen. |
| Fremdarbeitsposition | Die Fremdarbeitsposition, für die die Dienste bestellt wurden. Die Liste der auswählbaren Fremdarbeitspositionen ist auf die Positionen der ausgewählten Fremdarbeit beschränkt. | Wenn eine Fremdarbeitsposition in einer Kreditorenrechnungsposition für Ausgabenkategorien ausgewählt wird, werden Standardwerte für die Felder **Projekt**, **Aufgabe** und **Transaktionskategorie** werden aus den entsprechenden Feldern in der Fremdarbeitsposition eingegeben. Wenn die ausgewählte Fremdarbeitsposition Werte in den Feldern **Projekt**, **Projektaufgabe** und **Transaktionskategorie** hat, können die Werte der entsprechenden Felder in der Kreditorenrechnungsposition nicht von diesen Werten abweichen. |
| Buchungsdatum | Das Datum, an dem die tatsächlichen Kosten der Kreditorenrechnungsposition im Projekt erfasst werden. |Nein |
| Transaktionsklasse | Wählen Sie **Aufwand**, um eine Kreditorenrechnung für eine Ausgabenkategorie zu erfassen. | Der Wert **Aufwand** gibt an, dass die Kreditorenrechnungsposition verwendet wird, um den Rechnungsbetrag für Dienstleistungen zu erfassen, die als Ausgabenkategorien beschafft wurden. |
| Project | Der Name des Projekts, für das die in Rechnung gestellten Dienste verwendet wurden. | Dieses Feld ist ein Pflichtfeld und darf nicht leer gelassen werden. |
| Task | Der Name der Aufgabe, für die die in Rechnung gestellten Dienste verwendet wurden. Dieses Feld ist nur verfügbar, wenn ein Projekt ausgewählt ist. Die Auswahl einer Projektaufgabe ist optional. | Wenn dieses Feld leer gelassen wird, kann der Projektmanager die Kreditorenrechnungsposition mit Ausgaben abgleichen, die für einen beliebigen Vorgang des Projekts erfasst wurden. Wenn die Kreditorenrechnungsposition nicht auf eine Fremdarbeitsposition verweist und dieses Feld leer gelassen wird, werden die Ist-Kosten, die von der Kreditorenrechnungsposition erstellt werden, nicht mit noch nicht fakturierten Verkaufs-Ist-Werten verknüpft. In diesem Fall können bei eingerichteter aufgabenbezogener Abrechnung die Kosten dem Endkunden ggf. nicht in Rechnung gestellt werden. |
| Transaktionskategorie | Die Transaktionskategorie, die fakturiert wird. Für die ausgewählte Vorgangskategorie muss eine entsprechende Ausgabenkategorie erstellt werden. | Die Kombination der Werte **Transaktionskategorie** und **Einheit** wird als Standardwert verwendet oder für das Feld **Einheitspreis** für die Kreditorenrechnungsposition berechnet. |
| Menge | Geben Sie die vom Kreditor in Rechnung gestellte Menge in die Rechnungsposition ein. |Nein|
| Einheitengruppe | Basierend auf der Einheitengruppe des ausgewählten Transaktionstyps wird ein Standardwert eingegeben. | Nein |
| Einheit | Der Standardwert ist die Basiseinheit der ausgewählten Einheitengruppe. Sie können diesen Wert ändern, um eine beliebige Einheit der Einheitengruppe zu kaufen. | Die Kombination der Werte **Transaktionskategorie** und **Einheit** wird als Standardwert verwendet oder für das Feld **Einheitspreis** für die Kreditorenrechnungsposition berechnet. |
| Einheitenpreis | Der Standardeinheitspreis verwendet die Kombination der Werte **Transaktionskategorie** und **Einheit** aus der Projektpreisliste, die für das Transaktionsdatum der Kreditorenrechnungsposition gilt. | Wenn der Preis für die entsprechende Projektpreisliste in einer Einheit eingerichtet ist, die sich von der Einheit in der Kreditorenrechnungsposition unterscheidet, verwendet das System die Einheitenumrechnung, um den Preis pro Einheit zu berechnen. |
| Zwischensumme | Dies ist ein schreibgeschütztes Feld, das als *Menge* &times; *Stückpreis* berechnet wird, wenn Werte in das Feld **Menge** und in das Feld **Stückpreis** eingegeben werden. Wenn eines oder beide Felder leer sind, können Sie in dieses Feld einen Wert eingeben.| Nein |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein. | Nein |
| Gesamtbetrag | Der Gesamtbetrag der Kreditorenrechnungsposition, einschließlich Steuern. Dieses Feld wird als *Zwischensumme* + *Mehrwertsteuer* berechnet. | Nein |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
