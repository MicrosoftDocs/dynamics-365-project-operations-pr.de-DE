---
title: Kostensätze und Verkaufsraten für Ausgaben einrichten
description: In diesem Artikel erfahren Sie, wie Sie die Sätze für Transaktionen und Ausgabenkategorien festlegen können.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911871"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Kostensätze und Verkaufsraten für Ausgaben einrichten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können in Dynamics 365 Project Operations Kosten- und Verkaufspreise für Transaktionskategorien einrichten. Da die Kosten- und Verkaufspreise für Ausgaben ausgelegt sind, muss jede Transaktionskategorie, die diese enthält, auch als Ausgabenkategorie eingerichtet werden. Diese Einrichtung stellt die Genauigkeit der nachgeschalteten Funktionalität sicher. Kosten- und Verkaufspreise für Transaktionskategorien können nur in einer Währung aufgeführt werden, die die Währung im Preislisten-Header sein muss.

Führen Sie die folgenden Schritte aus, um Kostensätze und Verkaufsraten für Transaktionskategorien einzurichten. 

1. Gehen Sie zu **Vertrieb** > **Kunden** > **Preisliste**.
2. Um eine neue Preisiste zu erstellen, wählen Sie **Neu** aus. 
3. Wählen Sie unter **Kategoriepreise** im Unterraster-Menü die Option **Neuer Kategoriepreis**. 
4. Geben Sie auf der Seite **Schnellerfassung** die Transaktionskategorie und -einheit ein, für die Sie den neuen Preis erstellen.

In der folgenden Tabelle sind die Felder auf der Registerkarte **Allgemein** und **Schnellerfassung** einer Kategoriepreiszeile aufgeführt, die Sie beim Erstellen von Kategoriepreisen in einer Verkaufs- oder Einstandspreisliste berücksichtigen sollten.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Transaktionskategorie | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Wählen Sie die Transaktionskategorie aus, für die Sie einen Verkaufs- oder Einstandspreis erstellen. | Die Transaktionskategorie in der eingehenden Vorkalkulation oder in den Istwerten für Ausgaben wird mit dieser Zeile abgeglichen, um die Kostensätze oder Verkaufsraten der Transaktionskategorie als Standard festzulegen. |
| Einheitenzeitplan | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Der Einheitenzeitplan entspricht standardmäßig dem Einheitenzeitplan der Transaktionskategorie. | Es gibt keine nachgelagerten Auswirkungen über dieses Feld. |
| Einheit | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Wählen Sie die Einheit aus, für die die Raten eingerichtet werden. | Die Einheit in der eingehenden Vorkalkulation oder in den Istwerten wird mit der Einheit in dieser Zeile abgeglichen, um den Satz in der Ausgabenvorkalkulation oder in den Istwerten als Standard festzulegen. |
| Preisberechnungsmeth. | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Mögliche Werte des Feldes **Preisberechnungsmethode** sind **Einzelpreis**, **Zum Einstandswert** und **Aufschlag auf Kosten**. | Durch Auswahl von **Einzelpreis** während der Preiseinrichtung wird das Feld **Prozent** in der Kategoriepreiszeile gesperrt. Wenn **Zum Einstandswert** ausgewählt ist, sind die Felder **Preis** und **Prozent** in der Verkaufspreisliste gesperrt. Durch die Auswahl von **Aufschlag auf Kosten** wird das Feld **Preis** in der Verkaufspreisliste gesperrt. In einer eingehenden Zeile mit tatsächlichen Werten für Ausgaben führt die Preismethode **Zum Einstandswert** oder **Aufschlag auf Kosten** dazu, dass der entsprechenden nicht fakturierten Verkaufszeile ein Preis zugewiesen wird, der dem Preis in den tatsächlichen Kosten entspricht oder als Aufschlag auf den Preis berechnet wird. |
| Preis | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Richten Sie einen Preis pro Einheit für die Kombination aus Transaktionskategorie und Einheit ein. Beispielsweise beträgt der Kilometerstand 10 USD pro Meile und 8 USD pro Kilometer. | Der Satz für Kilometerleistung, der standardmäßig auf dem Einzelpreis der eingehenden Zeile der Vorkalkulation oder Istwerte für eine Ausgabentransaktionsklasse basiert.|
| Prozent | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Richten Sie einen Prozentsatz für Kosten für die Kombination aus Transaktionskategorie und Einheit ein. Beispielsweise sollte die Flugverkaufsrate um 10 Prozent über den Kosten der angefallenen Flugkosten liegen. | Dieser Prozentsatz auf Kosten ist nur in einer Verkaufspreisliste anwendbar, wenn die Preisberechnungsmethode **Aufschlag auf Kosten** ausgewählt ist. |
| Währung | Die Registerkarte **Allgemein** und die **Schnellerfassungs**-Seiten | Standardmäßig stammt dieser Wert aus der Währung in der Kopfzeile der Preisliste. Bei der Preisgestaltung für Transaktionskategorien kann die Währung nicht überschrieben werden. | Diese Währung basiert standardmäßig auf dem Einzelpreis der eingehenden Zeile mit Istwerten der Ausgabentransaktionsklasse für Kosten und Umsatz. |

## <a name="pricing-methods-for-expenses"></a>Preisberechnungsmethoden für Ausgaben

Wenn Sie Kategoriepreise einrichten, die nur im Zusammenhang mit der Kostenberechnung relevant sind, können Sie eine der folgenden drei Preisberechnungsmethoden verwenden:

- **Einzelpreis**
- **Zum Einstandswert**
- **Aufschlag auf Kosten**

### <a name="price-per-unit"></a>Einzelpreis
Wenn diese Preisberechnungsmethode für eine Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit sowohl in der Vorkalkulation als auch in den Istwerten verwendet. Die Vorkalkulation bezieht sich auf die Projektvorkalkulationszeilen für Ausgaben, das Angebotszeilendetail und das Vertragszeilendetail für Ausgaben.

### <a name="at-cost"></a>Zum Einstandswert
Wenn diese Preisberechnungsmethode in der Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit nur für die Istwerte der Ausgaben verwendet. Beispielsweise nicht fakturierte Umsatz-Istwerte für die Ausgabentransaktionsklasse. Der Stückpreis wird auf den nicht abgerechneten tatsächlichen Umsatz aus dem Stückpreis auf die tatsächlichen Kosten für diese Spesen festgelegt. Die Standard-Preisberechnung basierend auf Kosten wird nicht anhand von Projektvorkalkulationen für Ausgaben oder der Angebots- und Vertragszeilendetails für Ausgaben vorgenommen.

### <a name="markup-over-cost"></a>Aufschlag auf Kosten
Wenn diese Preisberechnungsmethode in der Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit nur für die Istwerte der Ausgaben verwendet. Beispielsweise nicht fakturierte Umsatz-Istwerte für die Ausgabentransaktionsklasse. Dieser Preis pro Einheit wird auf den nicht fakturierten tatsächlichen Umsatz auf einen berechneten Wert aus dem Preis pro Einheit in den tatsächlichen Kosten für diesen Aufwand gesetzt, nachdem der definierte Aufschlagsprozentsatz angewendet wurde. Die Standand-Preisberechnung basierend auf Kosten wird nicht anhand von Projektvorkalkulationen für Ausgaben oder der Angebots- und Vertragszeilendetails für Ausgaben vorgenommen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
