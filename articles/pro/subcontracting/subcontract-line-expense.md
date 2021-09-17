---
title: Fremdarbeitspositionen für Ausgabenkategorien
description: In diesem Thema wird erläutert, wie Sie Fremdarbeitspositionen für Ausgaben aufzeichnen und die Felder verwenden, um den Zeiteinkauf von Lieferanten zu erfassen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323820"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Fremdarbeitspositionen für Ausgabenkategorien

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Fremdarbeit in Dynamics 365 Project Operations kann eine Position für Ausgabenkategorien haben. Fremdarbeitspositionen für Ausgabenkategorien ermöglichen es einem Projektmanager, Kategorien von Dienstleistungen oder Produkten von Lieferanten zu kaufen, die er einem Projekt in Rechnung stellen kann.

Führen Sie die folgenden Schritte aus, um in Project Operations eine Fremdarbeitsposition für Ausgabenkategorien zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus, und öffnen Sie die Fremdarbeit, mit der Sie arbeiten möchten.
2. Auf der **Fremdarbeitsposition**-Registerkarte wählen Sie **Neu**, um eine neue Position zu erstellen.
3. Auf der Seite **Schnell erstellen** im Feld **Transaktionsklasse** wählen Sie **Ausgabe** und geben alle anderen erforderlichen Feldinformationen ein, oder Sie wählen sie aus.

Die folgende Tabelle enthält Informationen zu den Feldern auf der Detailseite **Fremdauftragsposition** und der Seite **Schnell erstellen**.

| **Feld** |  **Beschreibung** |
| ----------| ---------------- |
| Name | Der Name der Fremdarbeitsposition. |
| Beschreibung | Eine kurze Beschreibung der Service- und Produktkategorien, die in der Fremdarbeitsposition gekauft werden. |
| Leitungstyp | Dieses Feld hat einen Standardwert von **Mengenbasiert**.  |
| Fakturierungsmethode | Die Aberechnungsmethode der Fremdarbeitsposition. Basierend auf der Abrechnungsmethode der Position ist für die Abrechnungsmethode Festpreis ein meilensteinbasierter Rechnungsplan verfügbar.  |
| Transaktionsklasse | Dieses Feld hat einen Standardwert von **Zeit**. Um Fremdarbeitspositionen für den Einkauf von Produkten anzulegen, legen Sie im Feld **Transaktionsklasse** **Ausgabe** fest. Dieser Feldwert gibt an, dass die Fremdarbeitsposition verwendet wird, um einen Einkauf einer Kategorie von Produkten oder Services zu erfassen, die in Projekten verwendet werden sollen. |
| Transaktionskategorie | Wählen Sie die Transaktionskategorie aus. |
| Gewünschter Start | Das Datum, an dem die Kaufkategorien beim Lieferanten verfügbar sein müssen. Der gewünschte Start wird verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die der Fremdarbeit beigefügt sind. Die Kosten der Kategorie in der Fremdarbeitsposition werden standardmäßig von dieser Preisliste übernommen. |
| Gewünschtes Ende | Das Datum, an dem die Kaufkategorien nicht mehr benötigt werden. Dieses Datum ruft eine Warnung auf, wenn ein Projektmanager diese Fremdarbeitsposition mit bestimmten Kostenschätzungen für Projekte verknüpft, die nach diesem Datum datieren. |
| Bestellte Menge | Die Menge der Kategorie, die vom Lieferanten gekauft wird. Wenn ein Projektmanager die gekaufte Menge überzieht, wird eine Warnung ausgegeben.  |
| Einheitengruppe | Dieser Feldwert basiert auf der Standardeinheitengruppe, die für die ausgewählte Kategorie eingerichtet ist. |
| Einheit | Dieser Feldwert basiert auf der Standardeinheit, die für die ausgewählte Kategorie eingerichtet ist. Die Kombination aus Kategorie und Einheit wird als Standardwert für den Einheitspreis für die Fremdarbeitsposition verwendet. |
| Einheitenpreis | Der Einheitspreis-Feldwert wird standardmäßig aus der Kombination von Kategorie und Einheit aus den Kategoriepreisen in Bezug auf die Projektpreisliste verwendet, die für das angeforderte Startdatum der Fremdarbeitsposition gilt.  |
| Zwischensumme | Dieses schreibgeschützte Feld, wird automatisch als Mengenstückpreis berechnet, wenn sowohl die Mengen- als auch die Einheitspreiswerte eingegeben werden. Wenn entweder eins der Felder leer ist oder beide leer sind, können Sie manuell einen Wert in dieses Feld eingeben.  |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein.  |
| Gesamtbetrag | Der Gesamtbetrag der Fremdarbeitsposition einschließlich Steuern. Dieses Feld wird als Zwischensumme + Mehrwertsteuer berechnet.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
