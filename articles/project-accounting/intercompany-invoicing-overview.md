---
title: Intercompany-Rechnungsstellung – Übersicht
description: Dieses Thema enthält Informationen und Beispiele zur Intercompany-Rechnungsstellung für Projekte.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002640"
---
# <a name="intercompany-invoicing-overview"></a>Intercompany-Rechnungsstellung – Übersicht

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Ihre Organisation verfügt möglicherweise über mehrere Abteilungen, Tochterunternehmen und andere juristische Personen, die Produkte und Dienstleistungen für Projekte untereinander übertragen. Die juristische Person, die die Dienstleistung oder das Produkt erbringt, wird als *kreditgebende juristische Person* bezeichnet. Die juristische Person, die die Dienstleistung oder das Produkt erhält, wird als *kreditnehmende juristische Person* bezeichnet.

Die folgende Abbildung zeigt ein typisches Szenario, in dem zwei juristische Personen Contoso Robotics USA (die kreditnehmende juristische Person) und Contoso Robotics UK (die verleihende juristische Person) Ressourcen teilen, um ein Projekt für den Kunden zu liefern, Adventure works. Für dieses Szenario wird Contoso Robotics USA beauftragt, die Arbeit an Adventure Works zu liefern.

![Intercompany-Rechnungsstellung](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations verwendet den folgenden Ablauf, um Intercompany-Transaktionen zu verarbeiten:

1. Ressourcen der kreditgebenden juristischen Person erfassen Intercompany-Zeit- oder -Aufwandsvorgänge, indem sie Zeit und Kosten für Projekte in der kreditnehmenden juristischen Person buchen.
2. Zeit- und Kostenkosten werden im kreditgebenden Unternehmen anhand der Stückkostenpreisliste des kreditnehmenden Unternehmens erfasst.
3. Nicht in Rechnung gestellte Intercompany-Vertriebstransaktionen werden im kreditgebenden Unternehmen anhand der Stückkostenpreisliste des kreditnehmenden Unternehmens erfasst.
4. Nicht in Rechnung gestellte Einnahmen werden im kreditnehmenden Unternehmen anhand der Verkaufspreisliste für Projektverträge erfasst. Dem Kunden kann eine Rechnung gestellt werden, wenn nicht abgerechnete Einnahmen erfasst werden. Der Kunde muss nicht warten, bis die Intercompany-Rechnungsverarbeitung abgeschlossen ist.
5. Intercompany-Kundenrechnungen werden regelmäßig im kreditgebenden Unternehmen erstellt. Die Rechnungen werden manuell oder in regelmäßigen Abständen erstellt. Für jede kreditnehmende juristische Person kann eine einzelne Rechnung erstellt werden, oder es können separate Rechnungen pro Projekt erstellt werden.
6. Wenn die Intercompany-Debitorenrechnung in der kreditgebenden juristischen Person gebucht wird, wird die entsprechende ausstehende Kreditorenrechnung in der kreditnehmenden juristischen Person gebucht. Die Kosten in der ausstehenden Kreditorenrechnung werden bei der Buchung der Rechnung im Nebenbuch des Projekts erfasst.

Das folgende Diagramm zeigt die Intercompany-Rechnungsstellung in Bezug auf Buchhaltungsereignisse und erwartete Buchungen im Hauptbuch.

![Intercompany-Flow](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Intercompany-Rechnungsstellung konfigurieren](configure-intercompany-invoicing.md)
- [Intercompany-Transaktionen aufzeichnen](create-intercompany-transactions.md)
- [Intercompany-Debitoren- und -Kreditorenrechnungen erstellen](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]