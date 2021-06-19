---
title: Nachkalkulation produktbasierter Angebotspositionen
description: Dieses Thema enthält Informationen zur Anwendung eines Einstandspreis bei einer produktbasierten Angebotsposition.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003450"
---
# <a name="costing-product-based-quote-lines"></a>Nachkalkulation produktbasierter Angebotspositionen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Produktbasierte Angebotspositionen in Dynamics 365 Project Operations verfügen auch über ein **Einstandspreis**-Feld. Dieses Feld wird verwendet, um den Einstandspreis für das Produkt in der Angebotsposition und für nachgelagerte Rentabilitätsberechnungen zu verfolgen.

Wenn eine produktbasierte Angebotsposition für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Angebotsposition standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet. Das Standardkostenfeld im Produktkatalog wird in der Basiswährung der Organisation eingerichtet. Die Standardstückkosten in der produktbasierten Angebotsposition werden im Angebot in die Verkaufswährung umgerechnet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Einstandspreis bei einer produktbasierten Angebotsposition

Der Zweck von Einstandspreisen in einer produktbasierten Angebotsposition besteht darin, für jeden Verkauf unterschiedliche Kosten für ein Produkt zu berücksichtigen. Dies ist kein typisches Szenario, aber manchmal können die Kosten des Produkts vom Lieferanten abhängig vom Kunden des endgültigen Verkaufs rabattiert werden.

Beispiel:

Fabrikam Robotics installiert Roboterarme an den Fließbändern der A Datum Corporation. Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Robotics bezogen. Wenn die Installation von Roboterarmen bei A Datum Corporation eine neue vertikale Branche für Treys Roboterarme eröffnet, könnte Trey Fabrikam einen Sonderrabatt für dieses Geschäft gewähren.

In diesem Fall erstellt Fabrikam eine produktbasierte Angebotsposition für Robotic Arms und gibt für dieses Angebot einen Sonderpreis pro Einheit ein. Diese Kosten unterscheiden sich von den Standardkosten für Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]