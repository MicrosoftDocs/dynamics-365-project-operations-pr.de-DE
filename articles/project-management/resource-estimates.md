---
title: Ressourcenschätzungen
description: Dieses Thema enthält Informationen zum Berechnen der Ressourcenschätzungen in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076444"
---
# <a name="resource-estimates"></a><span data-ttu-id="b92e7-103">Ressourcenschätzungen</span><span class="sxs-lookup"><span data-stu-id="b92e7-103">Resource estimates</span></span>

<span data-ttu-id="b92e7-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="b92e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b92e7-105">Ressourcenschätzungen basieren auf zeitlich abgestuftem Aufwand, der in der Projektstrukturplan zusammen mit den geltenden Preisdimensionen definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b92e7-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="b92e7-106">In der Regel lautet die Berechnung **Rate/Stunde für jede Rolle x Stunden.**</span><span class="sxs-lookup"><span data-stu-id="b92e7-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="b92e7-107">Der zeitlich abgestufte Aufwand für jede Ressource wird im Ressourcenzuweisungsdatensatz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b92e7-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="b92e7-108">Die Preisgestaltung wird in einer vordefinierten Preisliste gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b92e7-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="b92e7-109">Die Umrechnung der Einheiten erfolgt auf der Grundlage der geltenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="b92e7-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ressourcenschätzungen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="b92e7-111">Standardeinstandspreis und Kostenwährung</span><span class="sxs-lookup"><span data-stu-id="b92e7-111">Default cost price and cost currency</span></span>

<span data-ttu-id="b92e7-112">Die Einstandspreise werden standardmäßig von der Organisationseinheit übernommen.</span><span class="sxs-lookup"><span data-stu-id="b92e7-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="b92e7-113">Standardrechnungsrate und Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="b92e7-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="b92e7-114">Verkaufspreise werden einmal pro Geschäft angewendet.</span><span class="sxs-lookup"><span data-stu-id="b92e7-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="b92e7-115">Die Hierarchie für die Standardeinstellung der Verkaufspreisliste lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b92e7-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="b92e7-116">Organisation</span><span class="sxs-lookup"><span data-stu-id="b92e7-116">Organization</span></span>
2. <span data-ttu-id="b92e7-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="b92e7-117">Customer</span></span>
3. <span data-ttu-id="b92e7-118">Angebot/Vertrag</span><span class="sxs-lookup"><span data-stu-id="b92e7-118">Quote/contract</span></span>
