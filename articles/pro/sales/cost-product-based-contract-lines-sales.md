---
title: Nachkalkulation produktbasierter Vertragszeilen
description: Dieses Thema enthält Informationen zum Erstellen.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4076755"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="3a87a-103">Nachkalkulation produktbasierter Vertragszeilen</span><span class="sxs-lookup"><span data-stu-id="3a87a-103">Costing product-based contract lines</span></span>

<span data-ttu-id="3a87a-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3a87a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3a87a-105">Produktbasierte Vertragszeilen in Dynamics 365 Project Operations umfassen das Feld **Einstandspreis** , in dem der Einstandspreis des Produkts für nachgelagerte Rentabilitätsberechnungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3a87a-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3a87a-106">Wenn eine produktbasierte Vertragszeile für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Vertragszeile standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet.</span><span class="sxs-lookup"><span data-stu-id="3a87a-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3a87a-107">Das Feld **Standardkosten** im Produktkatalog wird in der Basiswährung der Organisation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3a87a-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3a87a-108">Wenn die Stückkosten in der Vertragszeile standardmäßig sind, werden sie im Vertrag in die Verkaufswährung umgerechnet.</span><span class="sxs-lookup"><span data-stu-id="3a87a-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3a87a-109">Einstandspreis bei einer produktbasierten Vertragszeile</span><span class="sxs-lookup"><span data-stu-id="3a87a-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3a87a-110">Ein Einstandspreis in einer produktbasierten Vertragszeile ermöglicht unterschiedliche Kosten für jeden Kauf einer Einheit.</span><span class="sxs-lookup"><span data-stu-id="3a87a-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3a87a-111">Obwohl dies nicht immer erforderlich ist, gibt es bestimmte Szenarien, in denen die Kosten des Produkts vom Lieferanten für den Kunden abgezogen werden können.</span><span class="sxs-lookup"><span data-stu-id="3a87a-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3a87a-112">Betrachten Sie folgendes Szenario:</span><span class="sxs-lookup"><span data-stu-id="3a87a-112">Consider the following scenario:</span></span>

<span data-ttu-id="3a87a-113">Fabrikam Robotics installiert Roboterarme an den Fließbändern der Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3a87a-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3a87a-114">Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Research bezogen.</span><span class="sxs-lookup"><span data-stu-id="3a87a-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3a87a-115">Wenn die Installation von Roboterarmen bei Adatum Corporation eine neue vertikale Branche für Trey Research eröffnet, könnten sie einen Sonderrabatt für dieses Geschäft gewähren.</span><span class="sxs-lookup"><span data-stu-id="3a87a-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3a87a-116">In diesem Fall erstellt Fabrikam eine produktbasierte Vertragszeile für Roboterarme und gibt für diesen Vertrag den Einzelpreis ein, der sich von den Standardkosten für Roboterarme von Trey Research unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="3a87a-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>