---
title: Eine Vertriebspreisliste einrichten
description: Dieses Thema bietet Informationen zu Vertriebspreislisten für Projektpreise.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 952d518fb58b5be46c4b1cf4ed57b2494fdfdad85e7fe6fb0d622367bc071b5f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997605"
---
# <a name="set-up-a-sales-price-list"></a>Eine Vertriebspreisliste einrichten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Für Projektangebote und -verträge enthält eine Projektpreisliste ein anderes Preisaußerkraftsetzungsmuster als eine Produktpreisliste. Bei einer produktkatalogbasierten Angebotszeile können Sie den Preis für Rollen und Kategorien direkt in der Angebotszeile überschreiben, da jede Angebotszeile genau auf ein Katalogelement verweist. Allerdings können Sie bei einer projektbasierten Angebotszeile den Preis für Rollen und Kategorien nicht direkt in der Angebotszeile überschreiben. Sie können die Projektpreisliste verwenden, um mit den beiden unterschiedlichen Überschreibungsmustern zu arbeiten.

> [!NOTE]
> Wir empfehlen Ihnen, dass Sie aufgrund der Verhaltensunterschiede zwischen den zwei beim Überschreiben der Preisgestaltung eine separate Preisliste für Ihre Projektressourcen und Ihre Katalogelemente einrichten.

Jeder der folgenden Entitäten kann eine oder mehrere Vertriebspreislisten für die Projektpreisberechnung zugewiesen werden:

- Kunde (Konto) 
- Verkaufschance 
- Angebot 
- Projektvertrag

Die Zuordnung dieser Entitäten mit einer Preisliste wird anhand der Projektpreislisten angegeben. Sie können eine oder mehrere Preislisten den Vertriebsentitäten Kunde, Verkaufschance, Angebot und Projekt zuordnen.

Eine Standardprojektpreisliste wird nicht automatisch in einen Kundendatensatz eingegeben. Sie können jedoch eine Projektpreisliste manuell dem Kundendatensatz anfügen. Dennoch sollten Sie eine Projektpreisliste nur manuell anfügen, wenn Sie eine benutzerdefinierte Preisvereinbarung mit dem Kunden haben. 

Wenn eine Projektpreisliste einer Vertriebsentität angefügt ist, werden die folgenden Informationen überprüft:

- Die Preisliste hat einen Kontext **Vertrieb**. 
- Die Währung der Preisliste stimmt mit der Währung des Kunden überein. 

Bei einem Projektvertrag wird die folgende Rangfolge verwendet, um verwandte Projektpreislisten automatisch festzulegen:

1. Angebot
2. Verkaufschance
3. Kunde 
4. Globale Einstellungen 

Wenn eine Projektpreisliste standardmäßig angegeben ist, prüft das System, dass die Währung mit der Währung des Kunden übereinstimmt, und dass die Standardpreislisten, die eingegeben wurden, den Kontext **Vertrieb** haben.

Sie können mehrere Projektpreislisten den Entitäten Kunde, Verkaufschance, Angebot und Projektvertrag zuordnen. Diese Funktion unterstützt datumsspezifische Standardpreise für einen Projektvertrag mit langer Laufzeit, bei dem mehr als eine Preisliste erforderlich ist, um Preisaktualisierungen zu berücksichtigen, die aufgrund von Inflation auftreten. Wenn die Preislisten, die Sie der Entität Kunden, Verkaufschance, Angebot oder Projektvertrag zuordnen, eine überlappende Datumsgültigkeit haben, sind die Standardpreise unter Umständen falsch. Sie sollten deshalb sicherstellen, dass Projektpreislisten, die eine überlappende Datumsgültigkeit haben, nicht diesen Entitäten zugewiesen sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]