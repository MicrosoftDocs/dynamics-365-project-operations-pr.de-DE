---
title: Kreditorenrechnungspositionen für Zeit
description: In diesem Thema wird erläutert, wie Kreditorenrechnungszeilen für Zeitkosten erfasst werden, die von Subunternehmern aufgewendet werden.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597199"
---
# <a name="vendor-invoice-lines-for-time"></a>Kreditorenrechnungspositionen für Zeit

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Kreditorenrechnung in Microsoft Dynamics 365 Project Operations kann Kreditorenrechnungspositionen für Zeit haben. Projektmanager können Kreditorenrechnungspositionen für Zeit verwenden, um die Kosten von Fremdarbeitszeit zu erfassen, die für Projekte gekauft wurden.

Kreditorenrechnungspositionen für Zeit können auf eine Fremdarbeitsposition für Zeit verweisen oder auch nicht. Wenn eine Kreditorenrechnungsposition für Zeit auf eine Fremdarbeit verweist, können Projektmanager die Produkte, die von der Kreditorenrechnungsposition in Rechnung gestellt werden, mit der Zeit, die von Subunternehmern erfasst und von Projektmanagern zum Projekt erfasst wurden.

Die folgende Tabelle enthält Informationen zu den Feldern auf Kreditorenrechnungspositionen für Zeit.

| Feld | Beschreibung des Dataflows | Funktionsauswirkung |
| --- | --- | --- |
| Name des Dataflows | Der Name der Kreditorenrechnungsposition, um bei der Identifizierung zu helfen. | Dieser Name wird als erste Spalte in allen Nachschlagevorgängen angezeigt, die auf Kreditorenrechnungspositionen basieren. |
| Beschreibung des Dataflows | Eine kurze Beschreibung der Dienste, die vom Kreditor in der Kreditorenrechnungsposition in Rechnung gestellt werden. | Nein |
| Fremdarbeit | Die Fremdarbeit, für die die Dienste ursprünglich bestellt wurden. | Wenn eine Fremdarbeit für die Kreditorenrechnung ausgewählt wird, erben alle Zeilen auf der Kreditorenrechnung diese Auswahl. Eine Kreditorenrechnung darf keine Kreditorenrechnungspositionen haben, die auf verschiedene Fremdarbeiten verweisen. |
| Fremdarbeitsposition | Die Fremdarbeitsposition, für die die Dienste bestellt wurden. Die Liste der auswählbaren Fremdarbeitspositionen ist auf die Positionen der ausgewählten Fremdarbeit beschränkt. | Wenn eine Fremdarbeitsposition in einer Kreditorenrechnungsposition für Zeit ausgewählt wird, werden Standardwerte für die Felder **Projekt**, **Rolle** und **Buchbare Ressource** werden aus den entsprechenden Feldern in der Fremdarbeitsposition eingegeben. Wenn die ausgewählte Fremdarbeitsposition Werte in den Feldern **Projekt**, **Rolle** und **Buchbar** hat, können die Werte der entsprechenden Felder in der Kreditorenrechnungsposition nicht von diesen Werten abweichen. |
| Buchungsdatum | Das Datum, an dem die tatsächlichen Kosten der Kreditorenrechnungsposition im Projekt erfasst werden. | Nein |
| Transaktionsklasse | Der Standardwert ist **Zeit**. | Der Wert **Zeit** gibt an, dass die Kreditorenrechnungsposition verwendet wird, um den Rechnungsbetrag der Subunternehmerzeit zu erfassen. |
| Project | Der Name des Projekts, für das die in Rechnung gestellten Dienste verwendet wurden. | Dieses Feld ist ein Pflichtfeld und darf nicht leer gelassen werden. |
| Task | Der Name der Aufgabe, für die die in Rechnung gestellten Dienste verwendet wurden. Dieses Feld ist nur verfügbar, wenn ein Projekt ausgewählt ist. Die Auswahl einer Projektaufgabe ist optional. | Wenn dieses Feld leer gelassen wird, kann der Projektmanager die Kreditorenrechnungsposition mit Zeit abgleichen, die von Subunternehmerressourcen für einen beliebigen Auftrag des Projekts erfasst wurde. Wenn die Kreditorenrechnungsposition nicht auf eine Fremdarbeitsposition verweist und dieses Feld leer gelassen wird, werden die Ist-Kosten, die von der Kreditorenrechnungsposition erstellt werden, nicht mit noch nicht fakturierten Verkaufs-Ist-Werten verknüpft. In diesem Fall können bei eingerichteter aufgabenbezogener Abrechnung die Kosten dem Endkunden ggf. nicht in Rechnung gestellt werden. |
| Role | Die Rolle der Subunternehmerressourcen,deren Zeit fakturiert wird. | Dieses Feld gibt die Rolle an, die von den Subunternehmerressourcen ausgeführt wird, deren Zeit auf der Kreditorenrechnung in Rechnung gestellt wird. |
| Buchbare Ressource | Der Name des Subunternehmers, dessen Zeit fakturiert wird. Die Auswahl einer buchbaren Ressource ist optional. | Wenn dieses Feld leer gelassen wird, kann der Projektmanager die Kreditorenrechnungsposition auf mit Zeit abgleichen, die von beliebigen Ressourcen erfasst wird, die zum Kreditor auf der Kreditorenrechnungsposition gehört. |
| Menge | Geben Sie die Anzahl der Stunden ein, die vom Kreditor in der Rechnungsposition in Rechnung gestellt werden. |Nein |
| Einheitengruppe | Der Standardwert ist **Zeiteinheitengruppe** und kann nicht geändert werden. | Nein |
| Einheit | Der Standardwert ist die Basiseinheit der Stunden der Zeiteinheitengruppe. Sie können diesen Wert ändern, um eine beliebige Einheit der Zeiteinheitengruppe zu kaufen, z. B. Tag oder Woche. | Die Kombination der Werte **Rolle** und **Einheit** wird als Standardwert verwendet oder für das Feld **Einheitspreis** für die Kreditorenrechnungsposition berechnet. |
| Einheitenpreis | Der Standardeinheitspreis verwendet die Kombination der Werte **Rolle** und **Einheit** aus der Projektpreisliste, die für das Transaktionsdatum der Kreditorenrechnungsposition gilt. | Wenn der Preis für die entsprechende Projektpreisliste in einer Einheit eingerichtet ist, die sich von der Einheit in der Kreditorenrechnungsposition unterscheidet, verwendet das System die Einheitenumrechnung, um den Preis pro Einheit zu berechnen. |
| Zwischensumme | Dies ist ein schreibgeschütztes Feld, das als *Menge* &times; *Stückpreis* berechnet wird, wenn Werte in das Feld **Menge** und in das Feld **Stückpreis** eingegeben werden. Wenn eines oder beide Felder leer sind, können Sie in dieses Feld einen Wert eingeben. | Nein |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein. | Nein |
| Gesamtbetrag | Der Gesamtbetrag der Kreditorenrechnungsposition, einschließlich Steuern. Dieses Feld wird als *Zwischensumme* + *Mehrwertsteuer* berechnet. | Nein |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
