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
# <a name="product-price-lists"></a><span data-ttu-id="2e25f-103">Produktpreislisten</span><span class="sxs-lookup"><span data-stu-id="2e25f-103">Product price lists</span></span>

<span data-ttu-id="2e25f-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="2e25f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="2e25f-105">In Project Operations unterstützen **Produktpreislisten** und zugehörige Preislisten-Artikeleinheiten Funktionen zur Preisgestaltung von Produkten in produktbasierten Angebots- und Vertragszeilen.</span><span class="sxs-lookup"><span data-stu-id="2e25f-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="2e25f-106">Für Produkte, die für Projekte verwendet werden, werden die Preislistenelementdatensätze für Projektpreislisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e25f-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="2e25f-107">Produkte sollten so eingerichtet werden, dass sie Standardkosten und Preislisten im Produktkatalog haben.</span><span class="sxs-lookup"><span data-stu-id="2e25f-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="2e25f-108">Verwenden Sie den Listenpreis, die Standardkosten und die aktuellen Kosten, um Standardkosten und Listenpreise zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2e25f-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="2e25f-109">Die Standardlistenpreise werden nur auf einer Angebotszeile oder Projektvertragszeile verwendet, wenn das System keine Preislistenzeile für das Produkt in der Produktpreisliste für das Angebots- oder den Projektvertrag finden kann.</span><span class="sxs-lookup"><span data-stu-id="2e25f-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="2e25f-110">Der Einstandspreis von Produktkatalogzeilen kann zwischen Angeboten geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="2e25f-111">Diese Funktion ist wichtig, weil, wenn Sie Kosten nicht genau verfolgen, Sie Betriebsgewinne auf Projektengagements nicht ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="2e25f-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="2e25f-112">Standardmäßig werden die Standardkosten des Produkts als Einstandspreis verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e25f-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="2e25f-113">Allerdings kann der Standardeinstandspreis auf der Angebotszeile aktualisiert werden, wenn es einen anderen Einstandspreis für dieses Angebot gibt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="2e25f-114">Preislistenelemente</span><span class="sxs-lookup"><span data-stu-id="2e25f-114">Price list items</span></span>

<span data-ttu-id="2e25f-115">Sie können Produkte aus einem Produktkatalog zu verschiedenen Preislisten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2e25f-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="2e25f-116">Preislistenzeilen für Produkte verweisen immer eine bestimmte Einheit.</span><span class="sxs-lookup"><span data-stu-id="2e25f-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="2e25f-117">Preise für ein Produkt auf Preislistenelementen können als Währungsbetrag konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="2e25f-118">Alternativ kann es als Funktion des Listenpreises, der aktuellen Kosten oder Standardkosten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="2e25f-119">Preiskalkulationsfunktionen unterstützen verschiedene Rundungsoptionen, wenn Produktpreise als Funktion des Listenpreises, der Standardkosten oder aktuellen Kosten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="2e25f-120">Neben dem Nutzen von mehreren Preisberechnungsmethoden und Rundungsoptionen können Sie Preislistenelementen Rabattlisten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="2e25f-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="2e25f-121">Standardproduktpreisliste</span><span class="sxs-lookup"><span data-stu-id="2e25f-121">Default product price list</span></span>
<span data-ttu-id="2e25f-122">Jeder Kundendatensatz hat ein Feld **Standardpreisliste**, in dem Sie eine Preisliste angeben können, die der Währung des Kunden entspricht.</span><span class="sxs-lookup"><span data-stu-id="2e25f-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="2e25f-123">Es wird kein Standardwert automatisch in dieses Feld eingefügt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="2e25f-124">Wenn ein benutzerdefiniertes Preisabkommen mit einem bestimmten Kunden besteht, können Sie das Feld verwenden, um diesem Kunden eine Preisliste zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="2e25f-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="2e25f-125">Die Verkaufschance, das Angebot und die Entitäten des Projektvertrags verwenden die folgende Reihenfolge zur Eingabe von Standardproduktpreislisten.</span><span class="sxs-lookup"><span data-stu-id="2e25f-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="2e25f-126">Die gleiche Reihenfolge wird für Projektpreislisten wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e25f-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="2e25f-127">Angebot</span><span class="sxs-lookup"><span data-stu-id="2e25f-127">Quote</span></span>
2.  <span data-ttu-id="2e25f-128">Verkaufschance</span><span class="sxs-lookup"><span data-stu-id="2e25f-128">Opportunity</span></span>
3.  <span data-ttu-id="2e25f-129">Kunde</span><span class="sxs-lookup"><span data-stu-id="2e25f-129">Customer</span></span>
4.  <span data-ttu-id="2e25f-130">Globale Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2e25f-130">Global settings</span></span> 

<span data-ttu-id="2e25f-131">Standardmäßig werden im Feld **Produkt** auf der Angebotszeile alle aktiven Produkte in der Produktpreisliste des Angebots aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="2e25f-132">Wenn ein Produkt inaktiviert wurde oder wenn es ein Entwurfsprodukt wurde, wird es nicht angezeigt, wenn es in der Preisliste ist.</span><span class="sxs-lookup"><span data-stu-id="2e25f-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="2e25f-133">Produktkatalogzeilen werden auf der ersten Rechnung, die für einen Projektvertrag erstellt wird, als Rechnungszeilen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="2e25f-134">Auf einer Entwurfsrechnung können diese Rechnungszeilen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="2e25f-135">In diesem Fall erscheinen die Zeilen auf einer nachfolgenden Rechnung, bis sie in Rechnung gestellt werden oder die Rechnung an den Kunden gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e25f-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="2e25f-136">Sie können Sie keine Teilmenge einer Produktrechnungszeile in Rechnung stellen.</span><span class="sxs-lookup"><span data-stu-id="2e25f-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="2e25f-137">Wenn die Produktlinien aus dem Projektvertrag in Rechnung gestellt werden, werden Ist-Werte erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="2e25f-138">Allerdings werden diese Ist-Werte nicht mit der zugehörigen Projektentität verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2e25f-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="2e25f-139">Das bedeutet, produktbasierte Projektvertragszeilen sind unabhängig von jeglicher projektbasierten Verwendung.</span><span class="sxs-lookup"><span data-stu-id="2e25f-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
