---
title: Fremdarbeitspositionen für Produkte
description: In diesem Artikel wird erklärt, wie Sie Zeilen für Unterverträge für Produkte erfassen und die verschiedenen Felder verwenden, um den Kauf von Produkten bei Lieferanten zu erfassen.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1ca042eaf95a5e252f00248e83efb959ab3ce801
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522841"
---
# <a name="subcontract-lines-for-products"></a>Fremdarbeitspositionen für Produkte

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ein Unterauftrag in Dynamics 365 Project Operations kann eine Fremdarbeiotsposition für Produkte haben. Diese Positionen ermöglichen es einem Projektmanager, Produkte von Lieferanten zu kaufen, die er dann für Projektaufgaben verwenden kann.

Führen Sie die folgenden Schritte aus, um eine Fremdarbeitsposition für Produkte in Project Operations zu erstellen.

1. Wählen Sie auf der Navigationsseite **Fremdarbeiten** aus, und öffnen Sie dann den Unterauftrag, mit dem Sie arbeiten möchten. 
2. Auf der **Fremdarbeitsposition** Registerkarte wählen Sie **+ Neu**, um eine neue Fremdarbeitsposition zu erstellen.
3. Auf der Seite **Schnell erstellen** im Feld **Transaktionsklasse** wählen Sie **Material** und geben die erforderlichen Feldinformationen ein, oder Sie wählen sie aus. 
4. Wählen Sie **Speichern** aus.

Die folgende Tabelle gibt Auskunft über die Felder auf der **Details zu Fremdarbeitspositionen**-Seite und die **Schnell erstellen**-Seite, da sie für den Kauf von Produkten relevant sind.

| Feld | Beschreibung | Funktionsauswirkung|
| ----- | ----------- | ----------- |
| Name | Name der Unterauftragsposition, um bei der Identifizierung zu helfen. |Dies wird als erste Spalte in allen Nachschlagevorgängen basierend auf Fremdauftragspositionen angezeigt.
| Beschreibung | Eine kurze Beschreibung der Produkte, die in der Fremdarbeitsposition bestellt werden. | Kein Wert |
| Leitungstyp | Dieses Feld hat einen Standardwert von **Mengenbasiert**. |Kein Wert |
| Fakturierungsmethode | Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden: **Festpreis** und **Zeit und Material**. | Basierend auf der ausgewählten Abrechnungsmethode wird ein meilensteinbasierter Rechnungsplan für Unterauftragspositionen verfügbar gemacht, wenn die Fakturierungsmethode Festpreis ausgewählt ist. |
| Transaktionsklasse |Dieses Feld hat einen Standardwert von **Zeit**. Um Fremdarbeitspositionen für den Einkauf von Produkten anzulegen, legen Sie im Feld **Transaktionsklasse** **Material** fest.  | Dies zeigt an, dass die Unterauftragsposition verwendet wird, um den Einkauf von Produkten zu erfassen, die für Projekte verwendet werden soll. |
| Produkt auswählen | Wählen Sie aus, ob das gekaufte Produkt im Produktkatalog gepflegt wird oder ein beschreibbares Produkt ist. |Kein Wert |
| Produkt | Wählen Sie ein aktives Produkt aus dem Katalog aus. Dieses Feld ist nur verfügbar, wenn **Ausgewähltes Produkt** auf **Vorhanden** festgelegt ist. |Die Kombination von **Produkt** und **Einheit** wird als Standardwert verwendet oder für den Einheitspreis für die Unterauftragsposition berechnet.
| Manuell einzutragendes Produkt | Geben Sie den Name des manuell einzutragenden Produkts ein. Dieses Feld ist nur verfügbar, wenn **Ausgewähltes Produkt** auf **Manuell eingetragen** festgelegt ist.  |Bei beschreibbaren Produkten wird der Kaufpreis nicht automatisch ausgefüllt.|
| Gewünschtes Lieferdatum | Geben Sie das gewünschte Lieferdatum für die Produkte ein.| Dieses Datum wird auch verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die der Fremdarbeit beigefügt sind. Die Kosten des Produkts in der Fremdarbeitsposition werden dann standardmäßig von dieser Preisliste übernommen. |
| Vertragslieferdatum | Geben Sie das Datum ein, an dem die Lieferung der Produkte vertraglich vereinbart wurde.  |Kein Wert|
| Bestellte Menge | Geben Sie die Menge des Produkts ein, das vom Lieferanten gekauft wird.| Dies wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager diese Menge überzieht.|
| Einheitengruppe | Dieser Wert ist nur für Katalogprodukte voreingestellt. |Wenn **Produkt** und **Angefordertes Lieferdatum** ausgewählt sind, wählt das System die zutreffende Preisliste basierend auf dem Lieferdatum aus. Für das passende Produkt werden die zugehörigen Preislistenpositionen abgefragt. Die Einheits- und Einheitengruppenwerte werden standardmäßig aus dem Setup im Preislistenartikeldatensatz verwendet. |
| Einheit | Dieser Wert entspricht standardmäßig der Einheit, die im Preislistenartikeldatensatz eingerichtet wurde. Sie können dies bei Bedarf auf eine andere Einheit ändern.| Die Kombination aus Produkt und Einheit wird verwendet, um den Einheitspreis in der Fremdadrbeitsposition für vorhandene Katalogprodukte vorzuschlagen. |
| Einheitenpreis | Der Einheitspreis wird standardmäßig unter Verwendung der Kombination aus Produkt und Einheit aus den Preislistenpositionen in Bezug auf die Projektpreisliste verwendet, die für das angeforderte Lieferdatum der Fremdarbeitsposition gilt.  |Kein Wert |
| Zwischensumme | Dieses schreibgeschützte Feld wird als Menge x Stückpreis berechnet, wenn in beide Felder Werte eingegeben wurden. Wenn entweder das Feld **Menge**, das Feld **Stückpreis** oder beide leer sind, können Sie einen Wert manuell eingeben.  |Kein Wert |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerwert ein. |Kein Wert |
| Gesamtbetrag | Dieses berechnete Feld zeigt den Gesamtbetrag der Fremdarbeitsposition nach Einbeziehung der Steuern an. Der Wert in diesem Feld wird als Zwischensumme + Steuer berechnet. |Kein Wert |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
