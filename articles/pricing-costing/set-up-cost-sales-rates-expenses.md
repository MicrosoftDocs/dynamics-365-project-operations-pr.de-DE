---
title: Kostensätze und Verkaufsraten für Ausgaben einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Transaktions- und Ausgabenkategorien.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076443"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a><span data-ttu-id="633d8-103">Kostensätze und Verkaufsraten für Ausgaben einrichten</span><span class="sxs-lookup"><span data-stu-id="633d8-103">Set up cost and sales rates for expenses</span></span>

<span data-ttu-id="633d8-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="633d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="633d8-105">Sie können Kosten- und Verkaufspreise für Transaktionskategorien in Dynamics 365 Project Operations einrichten.</span><span class="sxs-lookup"><span data-stu-id="633d8-105">You can set up cost and sales prices for transaction categories in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="633d8-106">Da die Kosten- und Verkaufspreise für Ausgaben ausgelegt sind, muss jede Transaktionskategorie, die diese enthält, auch als Ausgabenkategorie eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="633d8-106">Because the cost and sales prices are designed for Expenses, each transaction category that includes these, must also be set up as an expense category.</span></span> <span data-ttu-id="633d8-107">Diese Einrichtung stellt die Genauigkeit der nachgeschalteten Funktionalität sicher.</span><span class="sxs-lookup"><span data-stu-id="633d8-107">This set up ensures accuracy in downstream functionality.</span></span> <span data-ttu-id="633d8-108">Kosten- und Verkaufspreise für Transaktionskategorien können nur in einer Währung aufgeführt werden, die die Währung im Preislisten-Header sein muss.</span><span class="sxs-lookup"><span data-stu-id="633d8-108">Cost and sales prices for transaction categories can only be listed in one currency, which must be the currency on the price list header.</span></span>

<span data-ttu-id="633d8-109">Führen Sie die folgenden Schritte aus, um Kostensätze und Verkaufsraten für Transaktionskategorien einzurichten.</span><span class="sxs-lookup"><span data-stu-id="633d8-109">To set up cost and sales rates for transaction categories, complete the following steps.</span></span> 

1. <span data-ttu-id="633d8-110">Erstellen Sie eine Preisliste basierend auf dem Preislisten-Header.</span><span class="sxs-lookup"><span data-stu-id="633d8-110">Create a price list based on the price list header.</span></span> 
2. <span data-ttu-id="633d8-111">Wählen Sie in **Kategoriepreise** im Unterrastermenü **+ Neuer Kategoriepreis** aus.</span><span class="sxs-lookup"><span data-stu-id="633d8-111">On the **Category Prices** , on the sub-grid menu, select **+ New Category Price**.</span></span> 
3. <span data-ttu-id="633d8-112">Geben Sie auf der Seite **Schnellerfassung** die Transaktionskategorie und -einheit ein, für die Sie den neuen Preis erstellen.</span><span class="sxs-lookup"><span data-stu-id="633d8-112">On the **Quick Create** page, enter the transaction category and unit that you are creating the new price for.</span></span>

<span data-ttu-id="633d8-113">In der folgenden Tabelle sind die Felder auf der Registerkarte **Allgemein** und **Schnellerfassung** einer Kategoriepreiszeile aufgeführt, die Sie beim Erstellen von Kategoriepreisen in einer Verkaufs- oder Einstandspreisliste berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="633d8-113">The following table lists the fields on the **General** tab and **Quick Create** page of a category price line that you should keep in mind as you create category prices on a sales or cost price list.</span></span>

| <span data-ttu-id="633d8-114">Feld</span><span class="sxs-lookup"><span data-stu-id="633d8-114">Field</span></span> | <span data-ttu-id="633d8-115">Position</span><span class="sxs-lookup"><span data-stu-id="633d8-115">Location</span></span> | <span data-ttu-id="633d8-116">Relevanz, Zweck und Anleitung</span><span class="sxs-lookup"><span data-stu-id="633d8-116">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="633d8-117">Nachgelagerte Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="633d8-117">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="633d8-118">Transaktionskategorie</span><span class="sxs-lookup"><span data-stu-id="633d8-118">Transaction Category</span></span> | <span data-ttu-id="633d8-119">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-119">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-120">Wählen Sie die Transaktionskategorie aus, für die Sie einen Verkaufs- oder Einstandspreis erstellen.</span><span class="sxs-lookup"><span data-stu-id="633d8-120">Select the transaction category you are creating a sales or cost price for.</span></span> | <span data-ttu-id="633d8-121">Die Transaktionskategorie in der eingehenden Vorkalkulation oder in den Istwerten für Ausgaben wird mit dieser Zeile abgeglichen, um die Kostensätze oder Verkaufsraten der Transaktionskategorie als Standard festzulegen.</span><span class="sxs-lookup"><span data-stu-id="633d8-121">The transaction category on the incoming estimate or actual for Expense will be matched against this line to default the cost or sales rate of the transaction category.</span></span> |
| <span data-ttu-id="633d8-122">Einheitenzeitplan</span><span class="sxs-lookup"><span data-stu-id="633d8-122">Unit Schedule</span></span> | <span data-ttu-id="633d8-123">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-123">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-124">Der Einheitenzeitplan entspricht standardmäßig dem Einheitenzeitplan der Transaktionskategorie.</span><span class="sxs-lookup"><span data-stu-id="633d8-124">The unit schedule defaults from the unit schedule of the transaction category.</span></span> | <span data-ttu-id="633d8-125">Es gibt keine nachgelagerten Auswirkungen über dieses Feld.</span><span class="sxs-lookup"><span data-stu-id="633d8-125">There is no downstream impact from this field.</span></span> |
| <span data-ttu-id="633d8-126">Einheit</span><span class="sxs-lookup"><span data-stu-id="633d8-126">Unit</span></span> | <span data-ttu-id="633d8-127">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-127">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-128">Wählen Sie die Einheit aus, für die die Raten eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="633d8-128">Select the unit for which the rates are being set up.</span></span> | <span data-ttu-id="633d8-129">Die Einheit in der eingehenden Vorkalkulation oder in den Istwerten wird mit der Einheit in dieser Zeile abgeglichen, um den Satz in der Ausgabenvorkalkulation oder in den Istwerten als Standard festzulegen.</span><span class="sxs-lookup"><span data-stu-id="633d8-129">The unit on the incoming estimate or actual is matched against the unit on this line to default the rate on the expense estimate or actual.</span></span> |
| <span data-ttu-id="633d8-130">Preisberechnungsmeth.</span><span class="sxs-lookup"><span data-stu-id="633d8-130">Pricing Method</span></span> | <span data-ttu-id="633d8-131">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-131">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-132">Mögliche Werte des Feldes **Preisberechnungsmethode** sind **Einzelpreis** , **Zum Einstandswert** und **Aufschlag auf Kosten**.</span><span class="sxs-lookup"><span data-stu-id="633d8-132">Possible values of the **Pricing Method** field are, **Price Per Unit** , **At Cost** , and **Markup Over Cost**.</span></span> | <span data-ttu-id="633d8-133">Durch Auswahl von **Einzelpreis** während der Preiseinrichtung wird das Feld **Prozent** in der Kategoriepreiszeile gesperrt.</span><span class="sxs-lookup"><span data-stu-id="633d8-133">During price setup, selecting **Price Per Unit** locks the **Percent** field on the category price line.</span></span> <span data-ttu-id="633d8-134">Wenn **Zum Einstandswert** ausgewählt ist, sind die Felder **Preis** und **Prozent** in der Verkaufspreisliste gesperrt.</span><span class="sxs-lookup"><span data-stu-id="633d8-134">If **At cost** is selected, the **Price** and **Percent** fields are locked on the sales price list.</span></span> <span data-ttu-id="633d8-135">Durch die Auswahl von **Aufschlag auf Kosten** wird das Feld **Preis** in der Verkaufspreisliste gesperrt.</span><span class="sxs-lookup"><span data-stu-id="633d8-135">Selecting **Markup Over Cost** locks the **Price** field on the sales price list.</span></span> <span data-ttu-id="633d8-136">In einer eingehenden Zeile mit tatsächlichen Werten für Ausgaben führt die Preismethode **Zum Einstandswert** oder **Aufschlag auf Kosten** dazu, dass der entsprechenden nicht fakturierten Verkaufszeile ein Preis zugewiesen wird, der dem Preis in den tatsächlichen Kosten entspricht oder als Aufschlag auf den Preis berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="633d8-136">On an incoming actual line for expense, the **At cost** or **Markup Over Cost** pricing method results in the corresponding unbilled sales line being assigned a price that is equal to the price on the cost actual or calculated as a markup over the price.</span></span> |
| <span data-ttu-id="633d8-137">Preis</span><span class="sxs-lookup"><span data-stu-id="633d8-137">Price</span></span> | <span data-ttu-id="633d8-138">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-138">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-139">Richten Sie einen Preis pro Einheit für die Kombination aus Transaktionskategorie und Einheit ein.</span><span class="sxs-lookup"><span data-stu-id="633d8-139">Set up a per unit rate for the transaction category and unit combination.</span></span> <span data-ttu-id="633d8-140">Beispielsweise beträgt der Kilometerstand 10 USD pro Meile und 8 USD pro Kilometer.</span><span class="sxs-lookup"><span data-stu-id="633d8-140">For example, the rate for mileage is 10 USD per mile and 8 USD per Kilometer.</span></span> | <span data-ttu-id="633d8-141">Der Satz für Kilometerleistung, der standardmäßig auf dem Einzelpreis der eingehenden Zeile der Vorkalkulation oder Istwerte für eine Ausgabentransaktionsklasse basiert.</span><span class="sxs-lookup"><span data-stu-id="633d8-141">The mileage rate will be the rate that defaults on the per unit price or cost of the incoming estimate or actual line for an expense transaction class.</span></span>|
| <span data-ttu-id="633d8-142">Prozent</span><span class="sxs-lookup"><span data-stu-id="633d8-142">Percent</span></span> | <span data-ttu-id="633d8-143">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-143">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-144">Richten Sie einen Prozentsatz für Kosten für die Kombination aus Transaktionskategorie und Einheit ein.</span><span class="sxs-lookup"><span data-stu-id="633d8-144">Set up percent over cost for the transaction category and unit combination.</span></span> <span data-ttu-id="633d8-145">Beispielsweise sollte die Flugverkaufsrate um 10 Prozent über den Kosten der angefallenen Flugkosten liegen.</span><span class="sxs-lookup"><span data-stu-id="633d8-145">For example, the airfare sales rate should be marked up 10 percent over the cost of the incurred airfare expense.</span></span> | <span data-ttu-id="633d8-146">Dieser Prozentsatz auf Kosten ist nur in einer Verkaufspreisliste anwendbar, wenn die Preisberechnungsmethode **Aufschlag auf Kosten** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="633d8-146">This percent over cost is only applicable on a sales price list when the pricing method selected is **Markup Over Cost**.</span></span> |
| <span data-ttu-id="633d8-147">Währung</span><span class="sxs-lookup"><span data-stu-id="633d8-147">Currency</span></span> | <span data-ttu-id="633d8-148">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="633d8-148">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="633d8-149">Standardmäßig stammt dieser Wert aus der Währung in der Kopfzeile der Preisliste.</span><span class="sxs-lookup"><span data-stu-id="633d8-149">By default, this value comes from the currency on the header of the price list.</span></span> <span data-ttu-id="633d8-150">Bei der Preisgestaltung für Transaktionskategorien kann die Währung nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="633d8-150">For transaction category pricing, the currency can't be overridden.</span></span> | <span data-ttu-id="633d8-151">Diese Währung basiert standardmäßig auf dem Einzelpreis der eingehenden Zeile mit Istwerten der Ausgabentransaktionsklasse für Kosten und Umsatz.</span><span class="sxs-lookup"><span data-stu-id="633d8-151">This currency defaults on the per unit price of the incoming actual line for the expense transaction class for cost and sales.</span></span> |

## <a name="pricing-methods-for-expenses"></a><span data-ttu-id="633d8-152">Preisberechnungsmethoden für Ausgaben</span><span class="sxs-lookup"><span data-stu-id="633d8-152">Pricing methods for expenses</span></span>

<span data-ttu-id="633d8-153">Wenn Sie Kategoriepreise einrichten, die nur im Zusammenhang mit der Kostenberechnung relevant sind, können Sie eine der folgenden drei Preisberechnungsmethoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="633d8-153">When you set up category prices that are only relevant in the context of expense pricing, you can use one of the following three pricing methods:</span></span>

- <span data-ttu-id="633d8-154">**Einzelpreis**</span><span class="sxs-lookup"><span data-stu-id="633d8-154">**Price per unit**</span></span>
- <span data-ttu-id="633d8-155">**Zum Einstandswert**</span><span class="sxs-lookup"><span data-stu-id="633d8-155">**At cost**</span></span>
- <span data-ttu-id="633d8-156">**Aufschlag auf Kosten**</span><span class="sxs-lookup"><span data-stu-id="633d8-156">**Markup over cost**</span></span>

### <a name="price-per-unit"></a><span data-ttu-id="633d8-157">Einzelpreis</span><span class="sxs-lookup"><span data-stu-id="633d8-157">Price per unit</span></span>
<span data-ttu-id="633d8-158">Wenn diese Preisberechnungsmethode für eine Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit sowohl in der Vorkalkulation als auch in den Istwerten verwendet.</span><span class="sxs-lookup"><span data-stu-id="633d8-158">When this pricing method is selected on a category price line that is linked to a sales price list, the price defaults for the category and unit combination in both the estimate and the actual.</span></span> <span data-ttu-id="633d8-159">Die Vorkalkulation bezieht sich auf die Projektvorkalkulationszeilen für Ausgaben, das Angebotszeilendetail und das Vertragszeilendetail für Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="633d8-159">Estimate refers to the project estimate lines for expenses, the quote line detail, and the contract line detail for expenses.</span></span>

### <a name="at-cost"></a><span data-ttu-id="633d8-160">Zum Einstandswert</span><span class="sxs-lookup"><span data-stu-id="633d8-160">At cost</span></span>
<span data-ttu-id="633d8-161">Wenn diese Preisberechnungsmethode in der Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit nur für die Istwerte der Ausgaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="633d8-161">When this pricing method is selected on the category price line that is linked to a sales price list, the price defaults for the category and unit combination only for the expense actual.</span></span> <span data-ttu-id="633d8-162">Beispielsweise nicht fakturierte Umsatz-Istwerte für die Ausgabentransaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="633d8-162">For example, unbilled sales actuals for the expense transaction class.</span></span> <span data-ttu-id="633d8-163">Der Preis pro Einheit wird auf den nicht fakturierten tatsächlichen Umsatz aus dem Preis pro Einheit im tatsächlichen Kostenwert für diese Ausgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="633d8-163">The unit price is set on the unbilled sales actual from the unit price on the cost actual for that expense.</span></span> <span data-ttu-id="633d8-164">Die Standard-Preisberechnung basierend auf Kosten wird nicht anhand von Projektvorkalkulationen für Ausgaben oder der Angebots- und Vertragszeilendetails für Ausgaben vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="633d8-164">Price defaulting based on cost isn't done on project estimates for expenses or the quote line and contract line details for expenses.</span></span>

### <a name="markup-over-cost"></a><span data-ttu-id="633d8-165">Aufschlag auf Kosten</span><span class="sxs-lookup"><span data-stu-id="633d8-165">Markup over cost</span></span>
<span data-ttu-id="633d8-166">Wenn diese Preisberechnungsmethode in der Kategoriepreiszeile ausgewählt wird, die mit einer Verkaufspreisliste verknüpft ist, wird der Preis für die Kombination aus Kategorie und Einheit nur für die Istwerte der Ausgaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="633d8-166">When this pricing method is selected on the category price line that is linked to a sales price list, the price defaults for the category and unit combination only for an expense actual.</span></span> <span data-ttu-id="633d8-167">Beispielsweise nicht fakturierte Umsatz-Istwerte für die Ausgabentransaktionsklasse.</span><span class="sxs-lookup"><span data-stu-id="633d8-167">For example, unbilled sales actuals for the expense transaction class.</span></span> <span data-ttu-id="633d8-168">Dieser Preis pro Einheit wird auf den nicht fakturierten tatsächlichen Umsatz auf einen berechneten Wert aus dem Preis pro Einheit in den tatsächlichen Kosten für diesen Aufwand gesetzt, nachdem der definierte Aufschlagsprozentsatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="633d8-168">This unit price is set on the unbilled sales actual to a calculated value from the unit price on the cost actual for that expense after the defined markup percent is applied.</span></span> <span data-ttu-id="633d8-169">Die Standand-Preisberechnung basierend auf Kosten wird nicht anhand von Projektvorkalkulationen für Ausgaben oder der Angebots- und Vertragszeilendetails für Ausgaben vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="633d8-169">Price defaulting based on cost isn't done in on project estimates for expenses or quote line and contract line details for expenses.</span></span>