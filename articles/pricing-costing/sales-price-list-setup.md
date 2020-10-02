---
title: Preislisten für den Vertrieb einrichten
description: Dieses Thema bietet Informationen zu Vertriebspreislisten für Projektpreise.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896460"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="3dd2d-103">Preislisten für den Vertrieb einrichten</span><span class="sxs-lookup"><span data-stu-id="3dd2d-103">Sales price list setup</span></span>

<span data-ttu-id="3dd2d-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3dd2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3dd2d-105">Für Projektangebote und -verträge enthält eine Projektpreisliste ein anderes Preisaußerkraftsetzungsmuster als eine Produktpreisliste.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="3dd2d-106">Bei einer produktkatalogbasierten Angebotszeile können Sie den Preis für Rollen und Kategorien direkt in der Angebotszeile überschreiben, da jede Angebotszeile genau auf ein Katalogelement verweist.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="3dd2d-107">Allerdings können Sie bei einer projektbasierten Angebotszeile den Preis für Rollen und Kategorien nicht direkt in der Angebotszeile überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="3dd2d-108">Sie können die Projektpreisliste verwenden, um mit den beiden unterschiedlichen Überschreibungsmustern zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="3dd2d-109">Wir empfehlen Ihnen, dass Sie aufgrund der Verhaltensunterschiede zwischen den zwei beim Überschreiben der Preisgestaltung eine separate Preisliste für Ihre Projektressourcen und Ihre Katalogelemente einrichten.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="3dd2d-110">Jeder der folgenden Entitäten kann eine oder mehrere Vertriebspreislisten für die Projektpreisberechnung zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="3dd2d-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="3dd2d-111">Kunde (Konto)</span><span class="sxs-lookup"><span data-stu-id="3dd2d-111">Customer (account)</span></span> 
- <span data-ttu-id="3dd2d-112">Verkaufschance</span><span class="sxs-lookup"><span data-stu-id="3dd2d-112">Opportunity</span></span> 
- <span data-ttu-id="3dd2d-113">Angebot</span><span class="sxs-lookup"><span data-stu-id="3dd2d-113">Quote</span></span> 
- <span data-ttu-id="3dd2d-114">Projektvertrag</span><span class="sxs-lookup"><span data-stu-id="3dd2d-114">Project Contract</span></span>

<span data-ttu-id="3dd2d-115">Die Zuordnung dieser Entitäten mit einer Preisliste wird anhand der Projektpreislisten angegeben.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="3dd2d-116">Sie können eine oder mehrere Preislisten den Vertriebsentitäten Kunde, Verkaufschance, Angebot und Projekt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="3dd2d-117">Eine Standardprojektpreisliste wird nicht automatisch in einen Kundendatensatz eingegeben.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="3dd2d-118">Sie können jedoch eine Projektpreisliste manuell dem Kundendatensatz anfügen.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="3dd2d-119">Dennoch sollten Sie eine Projektpreisliste nur manuell anfügen, wenn Sie eine benutzerdefinierte Preisvereinbarung mit dem Kunden haben.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="3dd2d-120">Wenn eine Projektpreisliste einer Vertriebsentität angefügt ist, werden die folgenden Informationen überprüft:</span><span class="sxs-lookup"><span data-stu-id="3dd2d-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="3dd2d-121">Die Preisliste hat einen Kontext **Vertrieb**.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="3dd2d-122">Die Währung der Preisliste stimmt mit der Währung des Kunden überein.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="3dd2d-123">Bei einem Projektvertrag wird die folgende Rangfolge verwendet, um verwandte Projektpreislisten automatisch festzulegen:</span><span class="sxs-lookup"><span data-stu-id="3dd2d-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="3dd2d-124">Angebot</span><span class="sxs-lookup"><span data-stu-id="3dd2d-124">Quote</span></span>
2. <span data-ttu-id="3dd2d-125">Verkaufschance</span><span class="sxs-lookup"><span data-stu-id="3dd2d-125">Opportunity</span></span>
3. <span data-ttu-id="3dd2d-126">Kunde</span><span class="sxs-lookup"><span data-stu-id="3dd2d-126">Customer</span></span> 
4. <span data-ttu-id="3dd2d-127">Globale Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3dd2d-127">Global settings</span></span> 

<span data-ttu-id="3dd2d-128">Wenn eine Projektpreisliste standardmäßig angegeben ist, prüft das System, dass die Währung mit der Währung des Kunden übereinstimmt, und dass die Standardpreislisten, die eingegeben wurden, den Kontext **Vertrieb** haben.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="3dd2d-129">Sie können mehrere Projektpreislisten den Entitäten Kunde, Verkaufschance, Angebot und Projektvertrag zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="3dd2d-130">Diese Funktion unterstützt datumsspezifische Standardpreise für einen Projektvertrag mit langer Laufzeit, bei dem mehr als eine Preisliste erforderlich ist, um Preisaktualisierungen zu berücksichtigen, die aufgrund von Inflation auftreten.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="3dd2d-131">Wenn die Preislisten, die Sie der Entität Kunden, Verkaufschance, Angebot oder Projektvertrag zuordnen, eine überlappende Datumsgültigkeit haben, sind die Standardpreise unter Umständen falsch.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="3dd2d-132">Sie sollten deshalb sicherstellen, dass Projektpreislisten, die eine überlappende Datumsgültigkeit haben, nicht diesen Entitäten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
