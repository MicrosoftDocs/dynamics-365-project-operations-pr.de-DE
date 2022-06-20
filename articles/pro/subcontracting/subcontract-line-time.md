---
title: Fremdarbeitspositionen für Zeit
description: In diesem Artikel erfahren Sie, wie Sie Zeilen für Unterverträge für Zeit erfassen und den Kauf von Zeit von Lieferanten erfassen.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0295ddd1b36eef9289110c4fe7b51397d81320d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925947"
---
# <a name="subcontract-lines-for-time"></a>Fremdarbeitspositionen für Zeit

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Fremdarbeit in Dynamics 365 Project Operations kann eine Fremdarbeiotsposition für Zeit haben. Fremdarbeitspositionen für Zeit ermöglichen es einem Projektmanager, Zeit für Lieferantenressourcen zu kaufen, um Projektaufgaben und Ressourcenanforderungen zu besetzen.

Führen Sie die folgenden Schritte aus, um in Project Operations eine Fremdarbeitsposition für Zeit zu erstellen.

1. Wählen Sie im Navigationsbereich **Fremdarbeiten** aus und öffnen SIe eine Fremdarbeit.
2. Auf der **Fremdarbeitsposition** Registerkarte wählen Sie **Neu**, um eine neue Fremdarbeitsposition zu erstellen.
3. Wählen Sie auf der **Schnell erstellen** Seite im Feld **Transaktionsklasse** **Zeit** aus.
4. Geben Sie die verbleibenden Feldinformationen ein und wählen Sie anschließend **Speichern**.

  Die folgende Tabelle enthält Informationen zu den Feldern auf der Seite **Fremdauftragsposition** und der Seite **Schnell erstellen**.

| **Feld** | **Beschreibung** | **Funktionsauswirkung** |
| --- | --- | --- |
| Name | Name der Unterauftragsposition, um bei der Identifizierung zu helfen. | Dies wird als erste Spalte in allen Nachschlagevorgängen basierend auf Fremdauftragspositionen angezeigt. |
| Beschreibung | Eine kurze Beschreibung der Dienstleistungen, die in der Fremdarbeitsposition gekauft werden. |Kein Wert |
| Leitungstyp |   Dieses Feld hat einen Standardwert von **Mengenbasiert**.| Kein Wert |
| Fakturierungsmethode | Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden: **Festpreis** und **Zeit und Material**. | Basierend auf der ausgewählten Abrechnungsmethode wird ein meilensteinbasierter Rechnungsplan für Unterauftragspositionen verfügbar gemacht, wenn die Fakturierungsmethode Festpreis ausgewählt ist. |
| Transaktionsklasse | Der Standardwert ist **Zeit**. | Dies zeigt an, dass die Lohnbearbeitungsposition verwendet wird, um einen Einkauf von Lohnbearbeitungszeit zu erfassen. |
| Rolle | Wählen Sie die Rolle der Lohnbearbeiterressourcen aus, deren Zeit eingekauft wird. | Die von den Fremdauftragsressourcen ausgeübte Rolle bestimmt die Kosten des Einkaufs. |
| Gewünschter Start | Geben Sie das Datum ein, an dem die Ressourcen des Fremdbearbeiters benötigt werden, um mit der Arbeit zu beginnen. | Dies wird verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die dem Unterauftrag beigefügt sind. Die Kosten der Rolle in der Lohnbearbeitungsposition stammen aus dieser Preisliste. |
| Gewünschtes Ende | Geben Sie das Datum ein, an dem der Einsatz der Fremdbearbeiterressource endet. | Dies wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager die Kapazität für nach diesem Datum auftretenden Ressourcenbedarf schöpft. |
| Bestellte Menge | Geben Sie die Stundenanzahl der Rolle ein, die vom Lieferanten gekauft wird. | Dies wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager die Kapazität des Ressourcenbedarfs ausschöpft. |
| Einheitengruppe | Der Standardwert ist **Zeiteinheitengruppe**, der nicht geändert werden kann. | Kein Wert|
| Einheit | Der Standardwert für dieses Feld ist die Basiseinheit der Stunden der **Zeiteinheitengruppe**. Sie können diesen Wert ändern, um eine beliebige Einheit der **Zeiteinheitengruppe** zu kaufen, z. B. Tag oder Woche. | Die Kombination von **Rolle** und **Einheit** wird als Standardwert verwendet oder für den Einheitspreis für die Unterauftragsposition berechnet. |
| Einheitenpreis | Der Standardeinheitenpreis verwendet die Kombination der **Rolle** und **Einheit** aus der Kategorie Preise bezogen auf die Projektpreisliste, die für den **gewünschten Beginn** der Unterauftragsposition gilt. | Wenn in der entsprechenden Projektpreisliste der Preis in einer anderen Einheit als der Einheit in der Fremdarbeitsposition eingerichtet ist, verwendet das System die Einheitenumrechnung, um den Preis pro Einheit zu berechnen. |
| Zwischensumme |    Dies ist ein schreibgeschütztes Feld, das als Menge X Stückpreis berechnet wird, wenn sowohl die Mengen- als auch die Stückpreiswerte eingegeben werden. Wenn entweder Menge, Stückpreis oder beides leer ist, können Sie einen Wert manuell in das Feld eingeben. | Kein Wert|
| Mehrwertsteuer |   Geben Sie den Umsatzsteuerbetrag ein. |Kein Wert |
| Gesamtbetrag | Der Gesamtbetrag der Fremdarbeitsposition einschließlich Steuern. Dieses Feld wird als Zwischensumme + Mehrwertsteuer berechnet.|Kein Wert |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
