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
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="35028-103">Nachkalkulation produktbasierter Angebotspositionen</span><span class="sxs-lookup"><span data-stu-id="35028-103">Costing product-based quote lines</span></span>

<span data-ttu-id="35028-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="35028-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="35028-105">Produktbasierte Angebotspositionen in Dynamics 365 Project Operations haben auch einen **Einstandspreis** -Feld.</span><span class="sxs-lookup"><span data-stu-id="35028-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="35028-106">Dieses Feld wird verwendet, um den Einstandspreis für das Produkt in der Angebotsposition und für nachgelagerte Rentabilitätsberechnungen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="35028-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="35028-107">Wenn eine produktbasierte Angebotsposition für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Angebotsposition standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet.</span><span class="sxs-lookup"><span data-stu-id="35028-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="35028-108">Das Standardkostenfeld im Produktkatalog wird in der Basiswährung der Organisation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="35028-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="35028-109">Die Standardstückkosten in der produktbasierten Angebotsposition werden im Angebot in die Verkaufswährung umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="35028-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="35028-110">Einstandspreis bei einer produktbasierten Angebotsposition</span><span class="sxs-lookup"><span data-stu-id="35028-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="35028-111">Der Zweck von Einstandspreisen in einer produktbasierten Angebotsposition besteht darin, für jeden Verkauf unterschiedliche Kosten für ein Produkt zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="35028-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="35028-112">Dies ist kein typisches Szenario, aber manchmal können die Kosten des Produkts vom Lieferanten abhängig vom Kunden des endgültigen Verkaufs rabattiert werden.</span><span class="sxs-lookup"><span data-stu-id="35028-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="35028-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="35028-113">For example:</span></span>

<span data-ttu-id="35028-114">Fabrikam Robotics installiert Roboterarme an den Fließbändern der A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="35028-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="35028-115">Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Robotics bezogen.</span><span class="sxs-lookup"><span data-stu-id="35028-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="35028-116">Wenn die Installation von Roboterarmen bei A Datum Corporation eine neue vertikale Branche für Treys Roboterarme eröffnet, könnte Trey Fabrikam einen Sonderrabatt für dieses Geschäft gewähren.</span><span class="sxs-lookup"><span data-stu-id="35028-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="35028-117">In diesem Fall erstellt Fabrikam eine produktbasierte Angebotsposition für Robotic Arms und gibt für dieses Angebot einen Sonderpreis pro Einheit ein.</span><span class="sxs-lookup"><span data-stu-id="35028-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="35028-118">Diese Kosten unterscheiden sich von den Standardkosten für Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="35028-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>