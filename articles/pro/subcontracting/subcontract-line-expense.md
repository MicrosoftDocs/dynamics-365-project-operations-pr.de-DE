---
title: Fremdarbeitspositionen für Ausgabenkategorien
description: Dieser Artikel erklärt, wie Sie Zeilen für Unteraufträge als Aufwand erfassen und die Felder verwenden, um den Kauf von Zeit von Lieferanten zu erfassen.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ba1241ce40b7c5b488e278e8f1b8e9f352f45dc8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522606"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Fremdarbeitspositionen für Ausgabenkategorien

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Eine Fremdarbeit in Dynamics 365 Project Operations kann eine Position für Ausgabenkategorien haben. Fremdarbeitspositionen für Ausgabenkategorien ermöglichen es einem Projektmanager, Kategorien von Dienstleistungen oder Produkten von Lieferanten zu kaufen, die er einem Projekt in Rechnung stellen kann.

Führen Sie die folgenden Schritte aus, um in Project Operations eine Fremdarbeitsposition für Ausgabenkategorien zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus, und öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten.
2. Auf der **Fremdarbeitsposition**-Registerkarte wählen Sie **Neu**, um eine neue Position zu erstellen.
3. Auf der Seite **Schnell erstellen** im Feld **Transaktionsklasse** wählen Sie **Ausgabe** und geben alle anderen erforderlichen Feldinformationen ein, oder Sie wählen sie aus.

Die folgende Tabelle enthält Informationen zu den Feldern auf der Detailseite **Fremdauftragsposition** und der Seite **Schnell erstellen**.

| **Feld** | **Beschreibung** | **Funktionsauswirkung** |
| --- | --- | --- |
| Name | Name der Unterauftragsposition, um bei der Identifizierung zu helfen. | Dies wird als erste Spalte in allen Nachschlagevorgängen basierend auf Fremdauftragspositionen angezeigt. |
| Beschreibung | Eine kurze Beschreibung der Ausgabenkategorien, die in der Unterauftragsposition gekauft werden. | Kein Wert |
|Leitungstyp | Dieses Feld hat einen Standardwert von **Mengenbasiert**. |Kein Wert |
| Fakturierungsmethode | Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden: **Festpreis** und **Zeit und Material**. | Ein meilensteinbasierter Rechnungsplan wird für Unterauftragspositionen verfügbar gemacht, wenn die Fakturierungsmethode Festpreis ausgewählt ist. |
| Transaktionsklasse | Dieses Feld hat einen Standardwert von **Zeit**. Um Fremdarbeitspositionen für den Einkauf von Produkten anzulegen, legen Sie im Feld **Transaktionsklasse** **Ausgabe** fest.  | Dies zeigt an, dass die Unterauftragsposition verwendet wird, um den Einkauf einer Ausgabenkategorie zu erfassen, die für Projekte verwendet werden soll. |
| Transaktionskategorie | Zeigt eine Liste der aktiven Transaktionskategorien im System an. |Kein Wert |
| Gewünschter Start | Geben Sie das Datum ein, an dem die Kaufkategorien beim Lieferanten verfügbar sein müssen. | Angeforderter Start wird verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die dem Unterauftrag beigefügt sind. Die Kosten der Kategorie in der Lohnbearbeitungsposition stammen aus dieser Preisliste. |
| Gewünschtes Ende | Geben Sie das Datum ein, an dem die Kaufkategorien nicht mehr benötigt werden. | Dies wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager diese Unterauftragsposition bestimmten Kostenschätzungen für das Projekt zuordnet, die nach diesem Datum erforderlich sind. |
| Bestellte Menge | Menge der Kategorie, die vom Lieferanten gekauft wird. | Dies wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager diese Menge überzieht.|
| Einheitengruppe | Der Standardwert basiert auf der Standardeinheitengruppe, die für die ausgewählte Kategorie eingerichtet ist. |Kein Wert |
| Einheit | Der Standardwert basiert auf der Standardeinheit, die für die ausgewählte Kategorie eingerichtet ist.  | Die Kombination von **Kategorie** und **Einheit** wird als Standardwert verwendet oder für den Einheitspreis für die Unterauftragsposition berechnet.  |
| Einheitenpreis | Der Standardwert verwendet die Kombination der **Kategorie** und **Einheit** aus der Kategorie Preise bezogen auf die Projektpreisliste, die für den gewünschten Beginn der Unterauftragsposition gilt. |Kein Wert |
| Zwischensumme | Dies ist ein schreibgeschütztes Feld, das als Menge X Stückpreis berechnet wird, wenn sowohl die Mengen- als auch die Stückpreiswerte eingegeben werden. Wenn eines oder beide Felder leer sind, können Sie in dieses Feld einen Wert eingeben. |Kein Wert |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein. |Kein Wert |
| Gesamtbetrag | Der Gesamtbetrag der Fremdarbeitsposition einschließlich Steuern. Dieses Feld wird als Zwischensumme + Mehrwertsteuer berechnet. |Kein Wert |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
