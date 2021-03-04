---
title: Nachkalkulation produktbasierter Vertragszeilen – Lite
description: Dieses Thema enthält Informationen zum Erstellen.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764458"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="695d4-103">Nachkalkulation produktbasierter Vertragszeilen – Lite</span><span class="sxs-lookup"><span data-stu-id="695d4-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="695d4-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="695d4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="695d4-105">Produktbasierte Vertragszeilen in Dynamics 365 Project Operations umfassen das Feld **Selbstkostenpreis**, in dem der Selbstkostenpreis des Produkts für nachgelagerte Rentabilitätsberechnungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="695d4-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="695d4-106">Wenn für ein Katalogprodukt eine produktbasierte Vertragszeile erstellt wird, werden die Kosten für die Zeile standardmäßig aus dem Feld **Standardkosten** im Produktkatalog übernommen.</span><span class="sxs-lookup"><span data-stu-id="695d4-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="695d4-107">Das Feld **Standardkosten** im Produktkatalog wird in der Basiswährung der Organisation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="695d4-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="695d4-108">Wenn die Stückkosten in der Vertragszeile standardmäßig sind, werden sie im Vertrag in die Verkaufswährung umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="695d4-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="695d4-109">Einstandspreis bei einer produktbasierten Vertragszeile</span><span class="sxs-lookup"><span data-stu-id="695d4-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="695d4-110">Ein Einstandspreis in einer produktbasierten Vertragszeile ermöglicht unterschiedliche Kosten für jeden Kauf einer Einheit.</span><span class="sxs-lookup"><span data-stu-id="695d4-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="695d4-111">Obwohl dies nicht immer erforderlich ist, gibt es bestimmte Szenarien, in denen die Kosten des Produkts vom Lieferanten für den Kunden abgezogen werden können.</span><span class="sxs-lookup"><span data-stu-id="695d4-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="695d4-112">Betrachten Sie folgendes Szenario:</span><span class="sxs-lookup"><span data-stu-id="695d4-112">Consider the following scenario:</span></span>

<span data-ttu-id="695d4-113">Fabrikam Robotics installiert Roboterarme an den Fließbändern der Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="695d4-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="695d4-114">Fabrikam bietet Installationsservices an, die Roboterarme stammen jedoch von Trey Research.</span><span class="sxs-lookup"><span data-stu-id="695d4-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="695d4-115">Wenn die Installation von Roboterarmen bei Adatum Corporation eine neue vertikale Branche für Trey Research eröffnet, könnten sie einen Sonderrabatt für dieses Geschäft gewähren.</span><span class="sxs-lookup"><span data-stu-id="695d4-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="695d4-116">In diesem Fall erstellt Fabrikam eine produktbasierte Vertragslinie für Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="695d4-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="695d4-117">Für diesen Vertrag werden Kosten pro Einheit eingegeben.</span><span class="sxs-lookup"><span data-stu-id="695d4-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="695d4-118">Die Kosten unterscheiden sich von den Kosten für Roboterarme von Trey Research.</span><span class="sxs-lookup"><span data-stu-id="695d4-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
