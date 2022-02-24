---
title: Produktpreislisten
description: Dieses Thema enthält Informationen zu den Preislisten in der Katalogpreisgestaltung, die für Projektangebote und Verträge verwendet werden.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877489"
---
# <a name="product-price-lists"></a>Produktpreislisten

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

 In Project Operations unterstützen **Produktpreislisten** und zugehörige Preislisten-Artikeleinheiten Funktionen zur Preisgestaltung von Produkten in produktbasierten Angebots- und Vertragszeilen. Für Produkte, die für Projekte verwendet werden, werden die Preislistenelementdatensätze für Projektpreislisten verwendet. 

Produkte sollten so eingerichtet werden, dass sie Standardkosten und Preislisten im Produktkatalog haben. Verwenden Sie den Listenpreis, die Standardkosten und die aktuellen Kosten, um Standardkosten und Listenpreise zu konfigurieren. Die Standardlistenpreise werden nur auf einer Angebotszeile oder Projektvertragszeile verwendet, wenn das System keine Preislistenzeile für das Produkt in der Produktpreisliste für das Angebots- oder den Projektvertrag finden kann.

Der Einstandspreis von Produktkatalogzeilen kann zwischen Angeboten geändert werden. Diese Funktion ist wichtig, weil, wenn Sie Kosten nicht genau verfolgen, Sie Betriebsgewinne auf Projektengagements nicht ermitteln können. Standardmäßig werden die Standardkosten des Produkts als Einstandspreis verwendet. Allerdings kann der Standardeinstandspreis auf der Angebotszeile aktualisiert werden, wenn es einen anderen Einstandspreis für dieses Angebot gibt.

## <a name="price-list-items"></a>Preislistenelemente

Sie können Produkte aus einem Produktkatalog zu verschiedenen Preislisten hinzufügen. Preislistenzeilen für Produkte verweisen immer eine bestimmte Einheit. Preise für ein Produkt auf Preislistenelementen können als Währungsbetrag konfiguriert werden. Alternativ kann es als Funktion des Listenpreises, der aktuellen Kosten oder Standardkosten konfiguriert werden.

Preiskalkulationsfunktionen unterstützen verschiedene Rundungsoptionen, wenn Produktpreise als Funktion des Listenpreises, der Standardkosten oder aktuellen Kosten konfiguriert werden. Neben dem Nutzen von mehreren Preisberechnungsmethoden und Rundungsoptionen können Sie Preislistenelementen Rabattlisten zuordnen. 

 
## <a name="default-product-price-list"></a>Standardproduktpreisliste
Jeder Kundendatensatz hat ein Feld **Standardpreisliste**, in dem Sie eine Preisliste angeben können, die der Währung des Kunden entspricht. Es wird kein Standardwert automatisch in dieses Feld eingefügt. Wenn ein benutzerdefiniertes Preisabkommen mit einem bestimmten Kunden besteht, können Sie das Feld verwenden, um diesem Kunden eine Preisliste zuzuordnen.

Die Verkaufschance, das Angebot und die Entitäten des Projektvertrags verwenden die folgende Reihenfolge zur Eingabe von Standardproduktpreislisten. Die gleiche Reihenfolge wird für Projektpreislisten wird verwendet.

1.  Angebot
2.  Verkaufschance
3.  Kunde
4.  Globale Einstellungen 

Standardmäßig werden im Feld **Produkt** auf der Angebotszeile alle aktiven Produkte in der Produktpreisliste des Angebots aufgeführt. Wenn ein Produkt inaktiviert wurde oder wenn es ein Entwurfsprodukt wurde, wird es nicht angezeigt, wenn es in der Preisliste ist. 

Produktkatalogzeilen werden auf der ersten Rechnung, die für einen Projektvertrag erstellt wird, als Rechnungszeilen hinzugefügt. Auf einer Entwurfsrechnung können diese Rechnungszeilen gelöscht werden. In diesem Fall erscheinen die Zeilen auf einer nachfolgenden Rechnung, bis sie in Rechnung gestellt werden oder die Rechnung an den Kunden gesendet wird. Sie können Sie keine Teilmenge einer Produktrechnungszeile in Rechnung stellen. Wenn die Produktlinien aus dem Projektvertrag in Rechnung gestellt werden, werden Ist-Werte erstellt. Allerdings werden diese Ist-Werte nicht mit der zugehörigen Projektentität verknüpft. Das bedeutet, produktbasierte Projektvertragszeilen sind unabhängig von jeglicher projektbasierten Verwendung. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
