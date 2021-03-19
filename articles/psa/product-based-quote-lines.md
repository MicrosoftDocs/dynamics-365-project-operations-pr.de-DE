---
title: Produktbasierte Angebotspositionen
description: Dieses Thema enthält Informationen zu produktbasierten Angebotspositionen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284087"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="4ba71-103">Produktbasierte Angebotspositionen</span><span class="sxs-lookup"><span data-stu-id="4ba71-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="4ba71-104">Sie können produktbasierte Angebotspositionen in Dynamics 365 Project Service Automation erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4ba71-105">Bei Angebotspositionen kann es sich um manuell einzutragende Positionen oder Elemente aus dem Produktkatalog handeln.</span><span class="sxs-lookup"><span data-stu-id="4ba71-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4ba71-106">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="4ba71-106">Product catalog</span></span>

<span data-ttu-id="4ba71-107">Die Produkte im Dynamics 365-Produktkatalog weisen eine Standardeinheit und eine Einheitengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="4ba71-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="4ba71-108">Falls verschiedene Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst.</span><span class="sxs-lookup"><span data-stu-id="4ba71-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="4ba71-109">Alle Produkte in einer Produktfamilie erben denselben Satz von Attributen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="4ba71-110">Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für eine Vielzahl von Software.</span><span class="sxs-lookup"><span data-stu-id="4ba71-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="4ba71-111">Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:</span><span class="sxs-lookup"><span data-stu-id="4ba71-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4ba71-112">Anzahl der Benutzer</span><span class="sxs-lookup"><span data-stu-id="4ba71-112">Number of users</span></span> 
- <span data-ttu-id="4ba71-113">Abonnementdauer (in Monaten)</span><span class="sxs-lookup"><span data-stu-id="4ba71-113">Subscription duration (in months)</span></span>

<span data-ttu-id="4ba71-114">Eine gute Möglichkeit, diese Art von Katalog zu verwalten, besteht darin, eine Produktfamilie mit der Bezeichnung **Abonnement-Software** mit den Attributen **Anzahl der Benutzer** und **Abonnementdauer** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="4ba71-115">Sie können dann einzelne Produkte, z. B. **Dynamics 365 Sales** oder **Dynamics 365 Field Service**, der Produktfamilie **Abonnement-Software** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4ba71-116">Hinzufügen von Produktkatalogelementen zu einer Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="4ba71-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="4ba71-117">Projektpositions- und Projektvertragsseiten weisen zwei Abschnitte für zwei Arten von Positionen auf: projektbasierte Positionen und produktbasierte Positionen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="4ba71-118">Bei produktbasierten Positionen wird Dynamics 365 verwendet, um einer Position Elemente aus einem Produktkatalog hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="4ba71-119">Die Dropdownliste in der Angebotsposition oder in der Projektvertragsposition enthält alle Produkte und Einheiten in der Produktpreisliste, die dem Angebot oder dem Projektvertrag angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="4ba71-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="4ba71-120">Sie können auch Produkte hinzufügen, die nicht Teil der Produktpreisliste des Angebots sind.</span><span class="sxs-lookup"><span data-stu-id="4ba71-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="4ba71-121">Darüber hinaus können Sie Produkte aus anderen Preislisten oder Produkte direkt aus dem Produktkatalog auswählen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="4ba71-122">Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4ba71-123">Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="4ba71-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="4ba71-124">Wenn eine Angebotsposition auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Angebotsposition überschreiben.</span><span class="sxs-lookup"><span data-stu-id="4ba71-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4ba71-125">Beachten Sie, dass eine Angebotsposition in Dynamics 365 ein Feld mit der Bezeichnung **Preise** aufweist.</span><span class="sxs-lookup"><span data-stu-id="4ba71-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="4ba71-126">Zwei Werte sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="4ba71-126">Two values are available:</span></span>

- <span data-ttu-id="4ba71-127">Preise überschreiben</span><span class="sxs-lookup"><span data-stu-id="4ba71-127">Override pricing</span></span>  
- <span data-ttu-id="4ba71-128">Standard verwenden</span><span class="sxs-lookup"><span data-stu-id="4ba71-128">Use default</span></span>

<span data-ttu-id="4ba71-129">Wenn Sie dieses Feld auf **Preise überschreiben** festlegen, setzt Dynamics 365 keinen Standardpreis fest.</span><span class="sxs-lookup"><span data-stu-id="4ba71-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="4ba71-130">Sie müssen einen Preis für das Produkt in der Angebotsposition eingeben.</span><span class="sxs-lookup"><span data-stu-id="4ba71-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4ba71-131">Wenn Sie dieses Feld auf **Standard verwenden** festlegen, verwendet Dynamics 365 den Standardverkaufspreis und sperrt das Feld, um eine Bearbeitung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4ba71-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="4ba71-132">Nachdem Sie PSA installiert haben, werden die Verkaufspreise in den produktbasierten Positionen in einem Angebot eingegeben.</span><span class="sxs-lookup"><span data-stu-id="4ba71-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="4ba71-133">Das Feld **Preise** wird dann auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Angebotspositionen bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="4ba71-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Festlegen der Preisüberschreibung](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="4ba71-135">Mengenfaktoren für Produkte</span><span class="sxs-lookup"><span data-stu-id="4ba71-135">Quantity factors for products</span></span>

<span data-ttu-id="4ba71-136">PSA verwendet Mengenfaktoren, um den Verkauf von Abonnement-basierten Produkten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4ba71-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4ba71-137">Für Abonnement-basierte Produkte wird die Menge im Angebot oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ba71-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="4ba71-138">Normalerweise wird der Preis der Abonnement-Software im Katalog als Preis pro Benutzer pro Monat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4ba71-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4ba71-139">Sie können jedoch auch andere Zeitbeschreibungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ba71-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="4ba71-140">Während des Vertriebsprozesses wird der Preis in der Angebotsposition in der Regel als Preis pro Benutzer pro Monat angegeben, der vom IT-Vertriebsmitarbeiter verhandelt und diskontiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ba71-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4ba71-141">Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate.</span><span class="sxs-lookup"><span data-stu-id="4ba71-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4ba71-142">Die Menge, die verwendet wird, um die Menge der Angebotszeile zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.</span><span class="sxs-lookup"><span data-stu-id="4ba71-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4ba71-143">Um diese Art des Verkaufs zu unterstützen, hat PSA das Konzept der Mengenfaktoren eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4ba71-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="4ba71-144">Mengenfaktoren basieren auf den Produktattributen in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4ba71-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4ba71-145">Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, kennzeichnet PSA eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren.</span><span class="sxs-lookup"><span data-stu-id="4ba71-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="4ba71-146">PSA stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ba71-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4ba71-147">Wenn einem Produkt, dass für Mengenfaktoren konfiguriert wurde, eine Angebotsposition hinzugefügt wird, ist das Feld **Menge** in der Angebotsposition ein schreibgeschütztes Feld.</span><span class="sxs-lookup"><span data-stu-id="4ba71-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="4ba71-148">Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, berechnet PSA die Menge der Angebotsposition.</span><span class="sxs-lookup"><span data-stu-id="4ba71-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="4ba71-149">Beispielsweise kann Dynamics 365 die folgenden Eigenschaften aufweisen:</span><span class="sxs-lookup"><span data-stu-id="4ba71-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="4ba71-150">**Anzahl der Benutzer** – Die Anzahl der Benutzer</span><span class="sxs-lookup"><span data-stu-id="4ba71-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="4ba71-151">**Anzahl der Monate** – Die Anzahl der Abonnementmonate</span><span class="sxs-lookup"><span data-stu-id="4ba71-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="4ba71-152">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="4ba71-152">**Product SKU**</span></span> 

<span data-ttu-id="4ba71-153">Die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** können durch Bearbeitung der Produktposition als Mengenfaktoren gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4ba71-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Kennzeichnen von Anzahl der Benutzer und Anzahl der Monate als Mengenfaktoren](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]