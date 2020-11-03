---
title: Nachkalkulation produktbasierter Angebotspositionen
description: Dieses Thema enthält Informationen zur Anwendung eines Einstandspreis bei einer produktbasierten Angebotsposition.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076427"
---
# <a name="costing-product-based-quote-lines"></a>Nachkalkulation produktbasierter Angebotspositionen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Produktbasierte Angebotspositionen in Dynamics 365 Project Operations haben auch einen **Einstandspreis** -Feld. Dieses Feld wird verwendet, um den Einstandspreis für das Produkt in der Angebotsposition und für nachgelagerte Rentabilitätsberechnungen zu verfolgen.

Wenn eine produktbasierte Angebotsposition für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Angebotsposition standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet. Das Standardkostenfeld im Produktkatalog wird in der Basiswährung der Organisation eingerichtet. Die Standardstückkosten in der produktbasierten Angebotsposition werden im Angebot in die Verkaufswährung umgerechnet.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Einstandspreis bei einer produktbasierten Angebotsposition

Der Zweck von Einstandspreisen in einer produktbasierten Angebotsposition besteht darin, für jeden Verkauf unterschiedliche Kosten für ein Produkt zu berücksichtigen. Dies ist kein typisches Szenario, aber manchmal können die Kosten des Produkts vom Lieferanten abhängig vom Kunden des endgültigen Verkaufs rabattiert werden.

Beispiel:

Fabrikam Robotics installiert Roboterarme an den Fließbändern der A Datum Corporation. Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Robotics bezogen. Wenn die Installation von Roboterarmen bei A Datum Corporation eine neue vertikale Branche für Treys Roboterarme eröffnet, könnte Trey Fabrikam einen Sonderrabatt für dieses Geschäft gewähren.

In diesem Fall erstellt Fabrikam eine produktbasierte Angebotsposition für Robotic Arms und gibt für dieses Angebot einen Sonderpreis pro Einheit ein. Diese Kosten unterscheiden sich von den Standardkosten für Trey Robotic Arms.
