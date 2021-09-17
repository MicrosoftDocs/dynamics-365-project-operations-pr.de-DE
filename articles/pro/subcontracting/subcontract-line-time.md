---
title: Fremdarbeitspositionen für Zeit
description: In diesem Thema wird erläutert, wie Sie Fremdarbeitspositionen für Zeit und den Einkauf von Zeit von Lieferanten aufzeichnen.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323865"
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

| **Feld** | **Beschreibung** |
| --- | --- |
| Name | Der Name der Fremdarbeitsposition. |
| Beschreibung | Eine kurze Beschreibung der Dienstleistungen, die in der Fremdarbeitsposition gekauft werden. | 
| Leitungstyp | Dieses Feld ist ein Standardwert.  |
| Fakturierungsmethode | Wählen Sie die Abrechnungsmethode aus. Basierend auf der Abrechnungsmethode der referenzierten Fremdarbeitsposition wird für die Abrechnungsmethode Festpreis ein meilensteinbasierter Rechnungsplan zur Verfügung gestellt. |
| Transaktionsklasse | Dieses Feld ist ein Standardwert, der angibt, ob die Fremdarbeitsposition verwendet wird, um einen Einkauf von Fremdarbeitszeit zu erfassen. |
| Rolle | Die Rolle der Fremdarbeitsressourcen, deren Zeit eingekauft wird. Die den Fremdarbeitsressourcen zugeordnete Rolle bestimmt die Kosten des Einkaufs. |
| Gewünschter Start | Das Datum, an dem die Subunternehmer-Ressourcen benötigt werden, um mit der Arbeit zu beginnen. Der gewünschte Start wird verwendet, um eine Projektpreisliste aus den Projektpreislisten auszuwählen, die der Fremdarbeit beigefügt sind. Die Kosten der Rolle in der Fremdarbeitsposition werden dann standardmäßig von dieser Preisliste übernommen. |
| Gewünschtes Ende | Das Datum, an dem die Zuweisung der Subunternehmer-Ressourcen endet. Dieses Datum wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager diese Kapazität für nach diesem Datum auftretenden Ressourcenbedarf in Anspruch nimmt. |
| Bestellte Menge | Die Anzahl der vom Anbieter erworbenen Rollenstunden. Dieser Wert wird verwendet, um Warnungen anzuzeigen, wenn ein Projektmanager diese Kapazität für Ressourcenbedarf überzieht. |
| Einheitengruppe | Dieser Feldwert entspricht standardmäßig der Gruppe Zeiteinheit und kann nicht geändert werden.  |
| Einheit | In diesem Feld wird standardmäßig die Basiseinheit Stunden aus der Gruppe Zeiteinheit verwendet. Sie können diesen Wert ändern, um eine beliebige Einheit der Gruppe Zeiteinheiten zu kaufen, z. B. Tag oder Woche. Die Kombination aus Rolle und Einheit wird verwendet, um den Einheitspreis für die Fremdarbeitsposition zu berechnen. |
| Einheitenpreis | Der Einheitspreis stammt standardmäßig aus der Kombination aus Rolle und Einheit aus der Projektpreisliste, die für das angeforderte Startdatum der Fremdarbeitsposition gilt. Wenn in der entsprechenden Projektpreisliste der Preis in einer anderen Einheit als der Einheit in der Fremdarbeitsposition eingerichtet ist, verwendet das System die Einheitenumrechnung, um den Preis pro Einheit zu berechnen. |
| Zwischensumme | Dies ist ein schreibgeschütztes Feld, das automatisch als **Menge x Stückpreis** berechnet wird, wenn sowohl die Mengen- als auch die Einheitspreiswerte eingegeben werden. Wenn entweder Menge, Stückpreis oder beides leer ist, können Sie einen Wert manuell in das Feld eingeben. |
| Mehrwertsteuer |  Geben Sie den Umsatzsteuerbetrag ein. |
| Gesamtbetrag | Der Gesamtbetrag der Fremdarbeitsposition nach Einbeziehung der Steuern. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
