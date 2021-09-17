---
title: Fremdarbeitspositionen für Produkte
description: In diesem Thema wird erläutert, wie Sie Fremdarbeitspositionen für Produkte aufzeichnen und die verschiedenen Felder verwenden, um Produktkäufe von Lieferanten zu erfassen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323685"
---
# <a name="subcontract-lines-for-products"></a>Fremdarbeitspositionen für Produkte

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Ein Unterauftrag in Dynamics 365 Project Operations kann eine Fremdarbeiotsposition für Produkte haben. Diese Positionen ermöglichen es einem Projektmanager, Produkte von Lieferanten zu kaufen, die er dann für Projektaufgaben verwenden kann.

Führen Sie die folgenden Schritte aus, um eine Fremdarbeitsposition für Produkte in Project Operations zu erstellen.

1. Wählen Sie auf der Navigationsseite **Fremdarbeiten** aus, und öffnen Sie dann den Unterauftrag, mit dem Sie arbeiten möchten. 
2. Auf der **Fremdarbeitsposition** Registerkarte wählen Sie **+ Neu**, um eine neue Fremdarbeitsposition zu erstellen.
3. Auf der Seite **Schnell erstellen** im Feld **Transaktionsklasse** wählen Sie **Material** und geben die erforderlichen Feldinformationen ein, oder Sie wählen sie aus. 
4. Wählen Sie **Speichern** aus.

Die folgende Tabelle gibt Auskunft über die Felder auf der **Details zu Fremdarbeitspositionen**-Seite und die **Schnell erstellen**-Seite, da sie für den Kauf von Produkten relevant sind.

| Feld | Beschreibung |
| ----- | ----------- |
| Name | Der Name der Fremdarbeitsposition. |
| Beschreibung | Eine kurze Beschreibung der Produkte, die in der Fremdarbeitsposition bestellt werden. |
| Leitungstyp | Dieser Feldwert ist standardmäßig **Mengenbasiert**. |
| Fakturierungsmethode |  Die Aberechnungsmethode der Fremdarbeitsposition. Für Festpreisabrechnungsmethoden steht ein meilensteinbasierter Abrechnungsplan zur Verfügung. |
| Transaktionsklasse | Dieser Feldwert ist standardmäßig **Zeit**. Um Fremdarbeitspositionen für den Einkauf von Produkten anzulegen, wählen Sie im Feld **Transaktionsklasse** **Material** aus. Diese Auswahl gibt an, dass die Fremdarbeitsposition verwendet wird, um einen Einkauf von Produkten zu erfassen, die in Projekten verwendet werden sollen. |
| Produkt auswählen | Wählen Sie aus, ob das gekaufte Produkt im Produktkatalog gepflegt wird oder ein beschreibbares Produkt ist. |
| Produkt | Wählen Sie ein aktives Produkt aus dem Katalog aus. Dieses Feld ist nur verfügbar, wenn **Ausgewähltes Produkt** auf **Vorhanden** festgelegt ist. |
| Manuell einzutragendes Produkt | Geben Sie den Name des manuell einzutragenden Produkts ein. Dieses Feld ist nur verfügbar, wenn **Ausgewähltes Produkt** auf **Manuell eingetragen** festgelegt ist.  |
| Gewünschtes Lieferdatum | Wählen Sie das gewünschte Lieferdatum für die Produkte aus. Dieses Datum wird auch verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die der Fremdarbeit beigefügt sind. Die Kosten des Produkts in der Fremdarbeitsposition werden dann standardmäßig von dieser Preisliste übernommen. |
| Vertragslieferdatum | Wählen Sie das Datum aus, an dem die Lieferung der Produkte vertraglich vereinbart wird.  |
| Bestellte Menge | Geben Sie die Menge des Produkts ein, das vom Lieferanten gekauft wird. Wenn ein Projektmanager diese Menge überzieht, wird eine Warnung ausgegeben. |
| Einheitengruppe | Dieser Wert ist nur für Katalogprodukte voreingestellt. Wenn **Produkt** und **Angefordertes Lieferdatum** ausgewählt sind, wählt das System die zutreffende Preisliste basierend auf dem Lieferdatum aus. Für das passende Produkt werden die zugehörigen Preislistenpositionen abgefragt. Die Einheits- und Einheitengruppenwerte werden standardmäßig aus dem Setup im Preislistenartikeldatensatz verwendet. |
| Einheit | Dieser Wert entspricht standardmäßig der Einheiteneinrichtung im Preislistenartikeldatensatz. Sie können dies bei Bedarf auf eine andere Einheit ändern. Die Kombination aus Produkt und Einheit wird verwendet, um den Einheitspreis in der Fremdadrbeitsposition für vorhandene Katalogprodukte vorzuschlagen. |
| Einheitenpreis | Der Einheitspreis wird standardmäßig unter Verwendung der Kombination aus Produkt und Einheit aus den Preislistenpositionen in Bezug auf die Projektpreisliste verwendet, die für das angeforderte Lieferdatum der Fremdarbeitsposition gilt.  |
| Zwischensumme | Dieses schreibgeschützte Feld wird als Menge x Stückpreis berechnet, wenn in beide Felder Werte eingegeben wurden. Wenn entweder das Feld **Menge**, das Feld **Stückpreis** oder beide leer sind, können Sie einen Wert manuell eingeben.  |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerwert ein. |
| Gesamtbetrag | Dieses berechnete Feld zeigt den Gesamtbetrag der Fremdarbeitsposition nach Einbeziehung der Steuern an. Der Wert in diesem Feld wird als Zwischensumme + Steuer berechnet. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
