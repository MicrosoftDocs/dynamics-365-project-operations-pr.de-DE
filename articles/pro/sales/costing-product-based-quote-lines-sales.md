---
title: Nachkalkulation produktbasierter Angebotspositionen
description: Dieser Artikel enthält Informationen über die Anwendung eines Selbstkostenpreises auf eine produktbasierte Angebotszeile.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825610"
---
# <a name="costing-product-based-quote-lines"></a>Nachkalkulation produktbasierter Angebotspositionen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Produktbasierte Angebotspositionen in Dynamics 365 Project Operations verfügen auch über ein **Einstandspreis**-Feld. Dieses Feld wird verwendet, um den Einstandspreis für das Produkt in der Angebotsposition und für nachgelagerte Rentabilitätsberechnungen zu verfolgen.

Wenn eine produktbasierte Angebotsposition für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Angebotsposition standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet. Das Standardkostenfeld im Produktkatalog wird in der Basiswährung der Organisation eingerichtet. Die Standardstückkosten in der produktbasierten Angebotsposition werden im Angebot in die Verkaufswährung umgerechnet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Einstandspreis bei einer produktbasierten Angebotsposition

Der Zweck von Einstandspreisen in einer produktbasierten Angebotsposition besteht darin, für jeden Verkauf unterschiedliche Kosten für ein Produkt zu berücksichtigen. Dies ist kein typisches Szenario, aber manchmal können die Kosten des Produkts vom Lieferanten abhängig vom Kunden des endgültigen Verkaufs rabattiert werden.

Beispiel:

Fabrikam Robotics installiert Roboterarme an den Fließbändern der A Datum Corporation. Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Robotics bezogen. Wenn die Installation von Roboterarmen bei A Datum Corporation eine neue vertikale Branche für Treys Roboterarme eröffnet, könnte Trey Fabrikam einen Sonderrabatt für dieses Geschäft gewähren.

In diesem Fall erstellt Fabrikam eine produktbasierte Angebotsposition für Robotic Arms und gibt für dieses Angebot einen Sonderpreis pro Einheit ein. Diese Kosten unterscheiden sich von den Standardkosten für Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
