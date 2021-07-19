---
title: Produktbasierte Angebotspositionen – Lite
description: Dieses Thema enthält Informationen zur Arbeit mit produktbasierten Angebotszeilen.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369825"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="8d390-103">Produktbasierte Angebotspositionen – Lite</span><span class="sxs-lookup"><span data-stu-id="8d390-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="8d390-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="8d390-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d390-105">Sie können produktbasierte Angebotspositionen in Dynamics 365 Project Operations erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d390-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="8d390-106">Bei Angebotspositionen kann es sich um manuell hinzugefügte Positionen oder Elemente aus dem Produktkatalog handeln.</span><span class="sxs-lookup"><span data-stu-id="8d390-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="8d390-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="8d390-107">Product catalog</span></span>

<span data-ttu-id="8d390-108">Jedes Produkt im Produktkatalog weist eine Standardeinheit und eine Einheitengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="8d390-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="8d390-109">Falls mehrere Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst.</span><span class="sxs-lookup"><span data-stu-id="8d390-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="8d390-110">Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für unterschiedliche Arten von Software.</span><span class="sxs-lookup"><span data-stu-id="8d390-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="8d390-111">Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:</span><span class="sxs-lookup"><span data-stu-id="8d390-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="8d390-112">Anzahl von Benutzern</span><span class="sxs-lookup"><span data-stu-id="8d390-112">Number of users</span></span>
- <span data-ttu-id="8d390-113">Eine Abonnementdauer in Monaten</span><span class="sxs-lookup"><span data-stu-id="8d390-113">A subscription duration measured in months</span></span>

<span data-ttu-id="8d390-114">Um diese Art von Katalog zu verwalten, erstellen sie eine Produktfamilie mit der Bezeichnung **Abonnement-Software** und fügen die Anzahl der Benutzer und die Abonnementdauer als Attribute hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d390-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="8d390-115">Im nächsten Schritt können Sie der **Abonnement-Software**-Produktfamilie einzelne Produkte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d390-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="8d390-116">Hinzufügen von Produktkatalogelementen zu einer Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="8d390-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="8d390-117">Die Seiten **Projektangebot** und **Projektvertrag** weisen Abschnitte für projektbasierte Positionen und produktbasierte Positionen auf.</span><span class="sxs-lookup"><span data-stu-id="8d390-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="8d390-118">Für produktbasierte Positionen enthält die Dropdownliste in der Angebotsposition oder in der Projektvertragsposition alle Produkte und Einheiten in der Produktpreisliste.</span><span class="sxs-lookup"><span data-stu-id="8d390-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="8d390-119">Sie können auch Produkte hinzufügen, die nicht Teil der Produktpreisliste sind.</span><span class="sxs-lookup"><span data-stu-id="8d390-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="8d390-120">Darüber hinaus können Sie Produkte aus anderen Preislisten oder Produkte direkt aus dem Produktkatalog auswählen.</span><span class="sxs-lookup"><span data-stu-id="8d390-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="8d390-121">Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8d390-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="8d390-122">Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="8d390-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="8d390-123">Wenn eine Angebotsposition auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Angebotsposition überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8d390-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="8d390-124">Eine Angebotszeile im **Preisgestaltung**-Feld mit zwei verfügbaren Werten:</span><span class="sxs-lookup"><span data-stu-id="8d390-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="8d390-125">**Preise überschreiben**</span><span class="sxs-lookup"><span data-stu-id="8d390-125">**Override Pricing**</span></span>
- <span data-ttu-id="8d390-126">**Standard verwenden**</span><span class="sxs-lookup"><span data-stu-id="8d390-126">**Use Default**</span></span>

<span data-ttu-id="8d390-127">Wenn Sie **Preise überschreiben** auswählen, ist der Standardpreis nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d390-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="8d390-128">Sie müssen stattdessen einen Preis für das Produkt in der Angebotsposition eingeben.</span><span class="sxs-lookup"><span data-stu-id="8d390-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="8d390-129">Wenn Sie **Standard verwenden** auswählen, wird der Standardverkaufspreis verwendet und das Feld für die Bearbeitung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="8d390-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="8d390-130">Es werden die Standardverkaufspreise in den produktbasierten Positionen in einem Angebot eingegeben.</span><span class="sxs-lookup"><span data-stu-id="8d390-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="8d390-131">Das Feld **Preise** wird dann auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Angebotspositionen bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="8d390-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="8d390-132">Dies ist eine Project Operations-spezifische Überschreibung des produktbasierten Zeilenverhaltens in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8d390-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]