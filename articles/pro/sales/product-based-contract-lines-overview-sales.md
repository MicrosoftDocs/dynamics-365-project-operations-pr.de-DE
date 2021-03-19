---
title: Übersicht über produktbasierte Vertragszeilen – Lite
description: Dieses Thema enthält Informationen zu produktbasierten Vertragszeilen.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272657"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="a0108-103">Übersicht über produktbasierte Vertragszeilen – Lite</span><span class="sxs-lookup"><span data-stu-id="a0108-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="a0108-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="a0108-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a0108-105">Sie können produktbasierte Vertragspositionen in Dynamics 365 Project Operations erstellen.</span><span class="sxs-lookup"><span data-stu-id="a0108-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="a0108-106">Bei Vertragszeilen kann es sich um manuell einzutragende Positionen oder Elemente aus dem Produktkatalog handeln.</span><span class="sxs-lookup"><span data-stu-id="a0108-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="a0108-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="a0108-107">Product catalog</span></span>

<span data-ttu-id="a0108-108">Die Produkte im Produktkatalog weisen eine Standardeinheit und eine Einheitengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="a0108-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="a0108-109">Falls verschiedene Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst.</span><span class="sxs-lookup"><span data-stu-id="a0108-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="a0108-110">Alle Produkte in einer Produktfamilie erben denselben Satz von Attributen.</span><span class="sxs-lookup"><span data-stu-id="a0108-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="a0108-111">Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für unterschiedliche Arten von Software.</span><span class="sxs-lookup"><span data-stu-id="a0108-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="a0108-112">Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:</span><span class="sxs-lookup"><span data-stu-id="a0108-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="a0108-113">Anzahl von Benutzern</span><span class="sxs-lookup"><span data-stu-id="a0108-113">Number of users</span></span>
- <span data-ttu-id="a0108-114">Abonnementdauer (in Monaten)</span><span class="sxs-lookup"><span data-stu-id="a0108-114">Subscription duration (in months)</span></span>

<span data-ttu-id="a0108-115">Um diese Art von Katalog zu verwalten, erstellen Sie eine Produktfamilie mit dem Namen **Software-Abonnement**.</span><span class="sxs-lookup"><span data-stu-id="a0108-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="a0108-116">Fügen Sie der Produktfamilie die Attribute **Anzahl von Benutzern** und **Abonnementdauer** hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0108-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="a0108-117">Fügen Sie dann der Produktfamilie **Software-Abonnement** einzelne Produkte hinzu.</span><span class="sxs-lookup"><span data-stu-id="a0108-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="a0108-118">Einem Vertrag Produktkatalogelemente hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a0108-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="a0108-119">Projektverträge weisen Abschnitte für zwei Arten von Positionen auf: projektbasierte Positionen und produktbasierte Positionen.</span><span class="sxs-lookup"><span data-stu-id="a0108-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="a0108-120">Produktbasierte Zeilen enthalten alle Produkte und Einheiten in der Produktpreisliste des Vertrags.</span><span class="sxs-lookup"><span data-stu-id="a0108-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="a0108-121">Produkte, die nicht Teil der Produktpreisliste des Vertrags sind, können hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a0108-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="a0108-122">Sie können Produkte aus anderen Preislisten oder direkt aus dem Produktkatalog auswählen.</span><span class="sxs-lookup"><span data-stu-id="a0108-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="a0108-123">Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a0108-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="a0108-124">Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="a0108-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="a0108-125">Wenn eine Vertragszeile auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Zeile überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a0108-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="a0108-126">Eine Vertragszeile besitzt das Feld **Preise** mit den zwei Werten:</span><span class="sxs-lookup"><span data-stu-id="a0108-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="a0108-127">**Preise überschreiben**</span><span class="sxs-lookup"><span data-stu-id="a0108-127">**Override pricing**</span></span>
- <span data-ttu-id="a0108-128">**Standard verwenden**</span><span class="sxs-lookup"><span data-stu-id="a0108-128">**Use default**</span></span>

<span data-ttu-id="a0108-129">Wenn Sie das Feld **Preise** auf **Preise überschreiben** festlegen, wurde der Standardpreis nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0108-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="a0108-130">Geben Sie einen Preis für das Produkt in die Vertragszeile ein.</span><span class="sxs-lookup"><span data-stu-id="a0108-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="a0108-131">Wenn Sie das Feld auf **Standard verwenden** festlegen, wird der Standardverkaufspreis verwendet und das Feld kann nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a0108-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="a0108-132">Nachdem Sie Project Operations installiert haben, werden die Verkaufspreise in den produktbasierten Positionen in einem Vertrag eingegeben.</span><span class="sxs-lookup"><span data-stu-id="a0108-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="a0108-133">Das Feld **Preise** ist auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Vertragszeilen bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a0108-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="a0108-134">Dies ist eine Project Operation-spezifische Überschreibung des produktbasierten Zeilenverhaltens in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a0108-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]