---
title: Projektverträge
description: Dieses Thema enthält Beispiele für die Projektverträge, die Sie für verschiedene Arten von Projekten und Finanzierungsquellen erstellen können, sowie für die Verwaltung von Verträgen und die Rechnungsstellung von Projektkunden.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999760"
---
# <a name="project-contracts"></a><span data-ttu-id="a70bd-103">Projektverträge</span><span class="sxs-lookup"><span data-stu-id="a70bd-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a70bd-104">Dieser Artikel enthält Beispiele für die Projektverträge, die Sie für verschiedene Arten von Projekten und Finanzierungsquellen erstellen können, sowie für die Verwaltung von Verträgen und die Rechnungsstellung von Projektkunden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="a70bd-105">Die Art des Projekts, das Sie für einen Projektvertrag erstellen, bestimmt die Methode, mit der den Projektkunden Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="a70bd-106">Sie können einen Projektvertrag und das zugehörige Projekt ändern, aber Sie können den Projekttyp nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="a70bd-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="a70bd-107">Mit einem Projektvertrag können Sie ein oder mehrere Projekte gleichzeitig in Rechnung stellen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="a70bd-108">Projektverträge tragen auch dazu bei, für jedes Teilprojekt einer Projektstruktur ein einheitliches Rechnungsverfahren zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="a70bd-109">Jedes in Rechnung gestellte Projekt muss einem Projektvertrag zugehörig sein.</span><span class="sxs-lookup"><span data-stu-id="a70bd-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="a70bd-110">Die Einstellungen für Projektverträge gelten für alle Projekte und Teilprojekte, die dem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a70bd-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="a70bd-111">In einem Projektvertrag können eine oder mehrere Finanzierungsquellen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="a70bd-112">Daher können Sie die Abrechnung auf mehrere Geldgeber aufteilen, Finanzierungsgrenzwertes festlegen, damit Finanzierungsquellen nicht mehr als einen bestimmten Betrag in Rechnung stellen, und Finanzierungsregeln für die Erhebung von Ausgaben konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a70bd-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="a70bd-113">Finanzierung von Projektverträgen</span><span class="sxs-lookup"><span data-stu-id="a70bd-113">Funding for project contracts</span></span>
<span data-ttu-id="a70bd-114">In einigen Projektverträgen ist festgelegt, dass mehrere Parteien die Verantwortung für die Finanzierung der Projektkosten teilen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="a70bd-115">Hier sehen Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="a70bd-115">Here are some examples:</span></span>

-   <span data-ttu-id="a70bd-116">Ein großer Kunde mit mehreren Abteilungen verlangt, dass die Finanzierung eines Projekts nach Abteilungen aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="a70bd-117">Ihr Unternehmen teilt die Kosten eines Großprojekts mit einer externen Organisation.</span><span class="sxs-lookup"><span data-stu-id="a70bd-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="a70bd-118">Ein Straßenprojekt wird von zwei Gemeinden kofinanziert.</span><span class="sxs-lookup"><span data-stu-id="a70bd-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="a70bd-119">Ein Brückenprojekt wird durch einen staatlichen Zuschuss und ein privates Unternehmen finanziert.</span><span class="sxs-lookup"><span data-stu-id="a70bd-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="a70bd-120">In Dynamics 365 Finance können Sie die Abrechnung für eine einzelne Transaktion oder ein gesamtes Projekt auf mehrere Kunden, Zuschüsse oder Organisationen aufteilen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="a70bd-121">In Projekten mit mehreren Geldgebern werden alle Parteien, die zur Finanzierung eines fortgeschrittenen Finanzierungsprojekts beitragen, als Finanzierungsquellen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a70bd-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="a70bd-122">Nachdem ein Kunde, eine Organisation oder ein Zuschuss als Finanzierungsquelle definiert wurde, kann er einer oder mehreren Finanzierungsregeln zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="a70bd-123">Die Finanzierungsregeln enthalten die Kriterien, die bestimmen, wie die Gebühren den verschiedenen Finanzierungsquellen für ein Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="a70bd-124">Da vorrätige Artikel, wie sie beispielsweise in Bestellanforderungen und Bestellungen enthalten sind, nicht aufgeteilt werden können, kann der Kostenbetrag zum Zeitpunkt der Verteilung nicht auf mehrere Finanzierungsquellen aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="a70bd-125">Daher bleibt der Wert der Finanzierungsquelle 0 (Null), bis das Inventarproblem gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="a70bd-126">Wenn das Inventarproblem gebucht wird, wird der Kostenbetrag gemäß den Kontoverteilungsregeln für das Projekt verteilt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="a70bd-127">Hier sind einige Schritte, die Sie unternehmen können, um die Aufteilung auf mehrere Finanzierungsquellen zu vereinfachen:</span><span class="sxs-lookup"><span data-stu-id="a70bd-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="a70bd-128">Geben Sie an, dass alle Transaktionen, die für ein Projekt eingegeben werden, dieselbe Verkaufswährung wie der Projektvertrag verwenden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="a70bd-129">Richten Sie Finanzierungslimits ein, damit einer Finanzierungsquelle nicht mehr als ein bestimmter Betrag für ein Projekt in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="a70bd-130">Konfigurieren Sie Finanzierungsregeln und Finanzierungslimits für jeden Mitarbeiter, Artikel, Kategorie, Kategoriegruppe und Transaktionstyp (oder für alle Transaktionstypen).</span><span class="sxs-lookup"><span data-stu-id="a70bd-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="a70bd-131">Wählen Sie optionale Start- und Enddaten aus, um den Zeitraum zu definieren, in dem jede Finanzierungsregel gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="a70bd-132">Geben Sie den Prozentsatz an, für den jede Finanzierungsquelle verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="a70bd-133">Geben Sie an, welche Finanzierungsquelle für Rundungsdifferenzen verantwortlich ist, die durch Berechnungen der Mittelzuweisung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="a70bd-134">Richten Sie Regeln ein, die festlegen, wie Projektkosten externen Kunden und internen Organisationen in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="a70bd-135">Erfassen Sie Transaktionen auf einem gehaltenen Finanzierungskonto, bis zusätzliche Mittel verfügbar sind oder bis Sie sich entscheiden, die Kosten intern zu tragen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="a70bd-136">Um zu bestimmen, welche Steuergruppe einer Transaktion zugeordnet werden soll, wird das Projekt nach einer Steuergruppenzuordnung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="a70bd-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="a70bd-137">Wenn auf Projektebene keine Steuergruppenzuordnung vorgenommen wurde, wird der Projektvertrag durchsucht.</span><span class="sxs-lookup"><span data-stu-id="a70bd-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="a70bd-138">Beispiel: Mehrere Finanzierungsquellen (einfach)</span><span class="sxs-lookup"><span data-stu-id="a70bd-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="a70bd-139">Die folgende Tabelle enthält Szenarien zum Verwalten der Mittelzuweisung auf mehrere Finanzierungsquellen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="a70bd-140">Diese Szenarien basieren auf folgenden Annahmen:</span><span class="sxs-lookup"><span data-stu-id="a70bd-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="a70bd-141">Prioritätseinstellungen werden bei der Zuweisung von Mitteln berücksichtigt, bevor andere Kriterien für Finanzierungsregeln angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="a70bd-142">Es wurde kein Datumsbereich angegeben, um den Zeitraum d zu definieren, in dem die Finanzierungsregel gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a70bd-143"><strong>Szenario</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="a70bd-144"><strong>Finanzierungsquelle</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="a70bd-145"><strong>Zuordnungsprozentsatz</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="a70bd-146"><strong>Zuweisungspriorität</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70bd-147">Sie möchten die Kosten einer Finanzierungsquelle zuordnen, bis die Mittel aufgebraucht sind, die Kosten einer zweiten Finanzierungsquelle zuordnen, bis die Mittel aufgebraucht sind, und schließlich die verbleibenden Kosten einer dritten Finanzierungsquelle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-148">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="a70bd-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="a70bd-149">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="a70bd-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="a70bd-150">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="a70bd-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-151">100%</span><span class="sxs-lookup"><span data-stu-id="a70bd-151">100%</span></span></li>
<li><span data-ttu-id="a70bd-152">100%</span><span class="sxs-lookup"><span data-stu-id="a70bd-152">100%</span></span></li>
<li><span data-ttu-id="a70bd-153">100%</span><span class="sxs-lookup"><span data-stu-id="a70bd-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-154">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-154">1</span></span></li>
<li><span data-ttu-id="a70bd-155">2</span><span class="sxs-lookup"><span data-stu-id="a70bd-155">2</span></span></li>
<li><span data-ttu-id="a70bd-156">3</span><span class="sxs-lookup"><span data-stu-id="a70bd-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a70bd-157">Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent einer zweiten Finanzierungsquelle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a70bd-158">Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten von einer dritten Finanzierungsquelle bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-159">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="a70bd-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="a70bd-160">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="a70bd-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="a70bd-161">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="a70bd-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-162">75 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-162">75%</span></span></li>
<li><span data-ttu-id="a70bd-163">25 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-163">25%</span></span></li>
<li><span data-ttu-id="a70bd-164">100%</span><span class="sxs-lookup"><span data-stu-id="a70bd-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-165">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-165">1</span></span></li>
<li><span data-ttu-id="a70bd-166">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-166">1</span></span></li>
<li><span data-ttu-id="a70bd-167">2</span><span class="sxs-lookup"><span data-stu-id="a70bd-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70bd-168">Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent einer zweiten Finanzierungsquelle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="a70bd-169">Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten zwischen einer dritten und einer vierte Finanzierungsquelle aufteilen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-170">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="a70bd-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="a70bd-171">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="a70bd-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="a70bd-172">Finanzierungsquelle 3</span><span class="sxs-lookup"><span data-stu-id="a70bd-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="a70bd-173">Finanzierungsquelle 4</span><span class="sxs-lookup"><span data-stu-id="a70bd-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-174">75 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-174">75%</span></span></li>
<li><span data-ttu-id="a70bd-175">25 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-175">25%</span></span></li>
<li><span data-ttu-id="a70bd-176">50 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-176">50%</span></span></li>
<li><span data-ttu-id="a70bd-177">50 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-178">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-178">1</span></span></li>
<li><span data-ttu-id="a70bd-179">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-179">1</span></span></li>
<li><span data-ttu-id="a70bd-180">2</span><span class="sxs-lookup"><span data-stu-id="a70bd-180">2</span></span></li>
<li><span data-ttu-id="a70bd-181">2</span><span class="sxs-lookup"><span data-stu-id="a70bd-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a70bd-182">Sie möchten die ersten 25 Prozent der Kosten einer Finanzierungsquelle und den Rest einer zweiten Finanzierungsquelle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-183">Finanzierungsquelle 1</span><span class="sxs-lookup"><span data-stu-id="a70bd-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="a70bd-184">Finanzierungsquelle 2</span><span class="sxs-lookup"><span data-stu-id="a70bd-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-185">25 %</span><span class="sxs-lookup"><span data-stu-id="a70bd-185">25%</span></span></li>
<li><span data-ttu-id="a70bd-186">100%</span><span class="sxs-lookup"><span data-stu-id="a70bd-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a70bd-187">1</span><span class="sxs-lookup"><span data-stu-id="a70bd-187">1</span></span></li>
<li><span data-ttu-id="a70bd-188">2</span><span class="sxs-lookup"><span data-stu-id="a70bd-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="a70bd-189">Beispiel: Mehrere Finanzierungsquellen (complex)</span><span class="sxs-lookup"><span data-stu-id="a70bd-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="a70bd-190">Sie haben drei Finanzierungsquellen, die Sie in der folgenden Reihenfolge verwenden möchten:</span><span class="sxs-lookup"><span data-stu-id="a70bd-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="a70bd-191">Verwenden Sie Finanzierungsquelle 2 und Finanzierungsquelle 3 gleichermaßen, bis die Finanzierungsquelle 2 erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="a70bd-192">Verwenden Sie weiterhin Finanzierungsquelle 3, bis diese erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="a70bd-193">Verwenden Sie die Finanzierungsquelle 1, nachdem die Finanzierungsquelle 3 erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="a70bd-194">Um dieses Ziel zu erreichen, müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a70bd-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="a70bd-195">Legen Sie Finanzierungslimits für Finanzierungsquelle 2 und Finanzierungsquelle 3 für ihre jeweiligen Beträge fest.</span><span class="sxs-lookup"><span data-stu-id="a70bd-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="a70bd-196">Erstellen Sie die folgenden Finanzierungsregeln:</span><span class="sxs-lookup"><span data-stu-id="a70bd-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="a70bd-197">Regel 1 (Priorität 1): Ordnen Sie 50 Prozent der Transaktionen der Finanzierungsquelle 2 und 50 Prozent der Finanzierungsquelle 3 zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="a70bd-198">Regel 2 (Priorität 2): Ordnen Sie 100 Prozent der Transaktionen der Finanzierungsquelle 3 zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="a70bd-199">Regel 3 (Priorität 3): Ordnen Sie 100 Prozent der Transaktionen der Finanzierungsquelle 1 zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="a70bd-200">Dieses Setup funktioniert, da Transaktionen anhand von Regeln und Grenzwerten überprüft werden, um festzustellen, ob sie für die Transaktion gelten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="a70bd-201">Wenn für die Transaktion keine spezifischen Regeln oder Beschränkungen gelten, gilt die Regel „Alle Transaktionen“.</span><span class="sxs-lookup"><span data-stu-id="a70bd-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="a70bd-202">Die Regel „Alle Transaktionen“ stimmt mit allen Transaktionen überein.</span><span class="sxs-lookup"><span data-stu-id="a70bd-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="a70bd-203">Wenn eine Regel gefunden wird, die mit einer Transaktion übereinstimmt, wird der Prozentsatz, der in dieser Regel zugewiesen wurde, zuerst angewendet, jedoch erst, nachdem die Übereinstimmungen mit den festgelegten Grenzwerten verglichen wurden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="a70bd-204">Wenn ein Limit erreicht wurde und die Mittel einer Finanzierungsquelle erschöpft sind, wird die mit dem Finanzierungslimit verbundene Finanzierungsregel nicht berücksichtigt und das Programm prüft, ob die nächste Regel gilt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="a70bd-205">In einigen Fällen kann nur ein Teil einer Transaktion unter einer Regel zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="a70bd-206">Dies kann passieren, weil bei der Zuweisung der Transaktion ein Limit erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="a70bd-207">In diesem Fall wird nach dieser Regel nur ein bestimmter Betrag zugewiesen, z. B. 50 Prozent für jede Finanzierungsquelle.</span><span class="sxs-lookup"><span data-stu-id="a70bd-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="a70bd-208">Dies ist in Regel 1 der Fall, die weiter oben in diesem Abschnitt beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="a70bd-209">Der Rest wird gemäß der nächsten Regel in der Sequenz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="a70bd-210">Die Tabelle unten überprüft dieses Szenario genauer.</span><span class="sxs-lookup"><span data-stu-id="a70bd-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a70bd-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="a70bd-212"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="a70bd-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70bd-213">Finanzierungsregeln</span><span class="sxs-lookup"><span data-stu-id="a70bd-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-214">Regel 1 (Priorität 1): Alle Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="a70bd-215">Weisen Sie Finanzierungsquelle 2 zu 50 % und Finanzierungsquelle 3 zu 50 % zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="a70bd-216">Regel 2 (Priorität 2): Alle Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="a70bd-217">Weisen Sie die Finanzierungsquelle 3 zu 100 % zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="a70bd-218">Regel 3 (Priorität 2): Alle Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="a70bd-219">Weisen Sie die Finanzierungsquelle 1 zu 100 % zu.</span><span class="sxs-lookup"><span data-stu-id="a70bd-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a70bd-220">Finanzierungslimits</span><span class="sxs-lookup"><span data-stu-id="a70bd-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-221">Limit für Finanzierungsquelle 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="a70bd-222">Limit für Finanzierungsquelle 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="a70bd-223">Limit für Finanzierungsquelle 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70bd-224">Transaktion 1</span><span class="sxs-lookup"><span data-stu-id="a70bd-224">Transaction 1</span></span></td>
<td><span data-ttu-id="a70bd-225"><strong>Transaktionshöhe:</strong> 100,00<strong>Finanzierung:</strong> Die Transaktion wird nur gemäß Regel 1 bezahlt, da die Transaktion nach Anwendung von Regel 1 vollständig bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="a70bd-226">Die Transaktion wird zu gleichen Teilen zwischen Finanzierungsquelle 2 und Finanzierungsquelle 3 finanziert.</span><span class="sxs-lookup"><span data-stu-id="a70bd-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="a70bd-227">Finanzierungsquelle 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="a70bd-228">Finanzierungsquelle 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a70bd-229">Transaktion 2</span><span class="sxs-lookup"><span data-stu-id="a70bd-229">Transaction 2</span></span></td>
<td><span data-ttu-id="a70bd-230"><strong>Transaktionshöhe:</strong> 5.000,00<strong>Finanzierung:</strong> Die Transaktion wird nach allen drei Regeln bezahlt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="a70bd-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="a70bd-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="a70bd-232">Finanzierungsquelle 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="a70bd-233">Finanzierungsquelle 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="a70bd-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="a70bd-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="a70bd-235">Finanzierungsquelle 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="a70bd-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="a70bd-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="a70bd-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="a70bd-237">Finanzierungsquelle 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="a70bd-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a70bd-238">Gesamtmittel, die für jede Finanzierungsquelle verteilt werden</span><span class="sxs-lookup"><span data-stu-id="a70bd-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="a70bd-239">Finanzierungsquelle 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="a70bd-240">Finanzierungsquelle 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="a70bd-241">Finanzierungsquelle 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="a70bd-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="a70bd-242">Abrechnungsregeln</span><span class="sxs-lookup"><span data-stu-id="a70bd-242">Billing rules</span></span>
<span data-ttu-id="a70bd-243">Wenn Sie einen Projektvertrag mit einem Kunden aushandeln, legen Sie fest, wie und wann Sie dem Kunden die Arbeit an einem Projekt in Rechnung stellen können.</span><span class="sxs-lookup"><span data-stu-id="a70bd-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="a70bd-244">Nachdem Sie den Projektvertrag und das Projekt eingerichtet haben, können Sie Abrechnungsregeln für das Projekt einrichten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="a70bd-245">Die Abrechnungsregeln basieren auf den im Projektvertrag festgelegten Projektbedingungen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="a70bd-246">Die Abrechnungsregeln, die Sie erstellen können, hängen von den Bedingungen des Projektvertrags und der Projektart ab, z. B. Zeit und Material oder Festpreis, die Sie der Abrechnungsregel zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="a70bd-247">Sie können mehr als eine Abrechnungsregel für einen Projektvertrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="a70bd-248">Sie können auch mehreren Projekten, die demselben Projektvertrag zugeordnet sind und ähnliche Abrechnungsbedingungen haben, eine Abrechnungsregel zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="a70bd-249">Sie können die folgenden Typen der Abrechnungsregeln einrichten:</span><span class="sxs-lookup"><span data-stu-id="a70bd-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="a70bd-250">**Liefereinheit** – Stellen Sie einem Kunden eine Rechnung, wenn Sie eine Liefereinheit fertiggestellt haben.</span><span class="sxs-lookup"><span data-stu-id="a70bd-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="a70bd-251">Die Liefereinheiten definieren Sie im Vertrag.</span><span class="sxs-lookup"><span data-stu-id="a70bd-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="a70bd-252">**Fortschritt** – Stellen Sie einem Kunden eine Rechnung, wenn Sie einen bestimmten Prozentsatz des Projekts abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="a70bd-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="a70bd-253">Sie können eine Abrechnungsregel einrichten, um den Prozentsatz der abgeschlossenen Arbeit automatisch zu berechnen, oder Sie können den Prozentsatz der abgeschlossenen Arbeit und den Rechnungsbetrag für den Kunden manuell berechnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="a70bd-254">**Meilenstein** – Rechnungsstellung eines Kunden über den vollen Betrag eines Projektmeilensteins, wenn der Meilenstein erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="a70bd-255">**Gebühr** – Rechnungsstellung eines Kunden für Ihre Dienstleistungen zuzüglich einer Verwaltungsgebühr, die in der Regel einen Prozentsatz der Kosten für Dienstleistungen ausmacht.</span><span class="sxs-lookup"><span data-stu-id="a70bd-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="a70bd-256">**Aufwand** – Berechnen Sie einem Kunden den Wert des Aufwands, der für ein Projekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="a70bd-257">Für alle Arten von Abrechnungsregeln können Sie einen Aufbewahrungsprozentsatz angeben, der von den Kundenrechnungen abgezogen wird, bis ein Projekt eine vereinbarte Phase erreicht.</span><span class="sxs-lookup"><span data-stu-id="a70bd-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="a70bd-258">Der Prozentsatz der Zahlungsaufbewahrung ist im Projektvertrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="a70bd-259">Der Betrag wird basierend auf dem Gesamtwert der Zeilen in einer Kundenrechnung berechnet und von diesem abgezogen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="a70bd-260">Für die Abrechnungsregeln **Aufwand** und **Fortschritt** können Sie kostenpflichtige Kategorien zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="a70bd-261">Kostenpflichtige Kategorien geben die Transaktionen an, die in Kundenrechnungen enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="a70bd-262">Wenn Sie bereit sind, dem Kunden eine Rechnung zu stellen, wird der Rechnungsbetrag für das Projekt basierend auf den Abrechnungsregeln berechnet und ein Projektrechnungsvorschlag generiert.</span><span class="sxs-lookup"><span data-stu-id="a70bd-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="a70bd-263">In den folgenden Abschnitten finden Sie Beispiele zum Einrichten und Verwalten von Abrechnungsregeln für ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="a70bd-264">Beispiel: Erstellen Sie eine Abrechnungsregel, die auf der Anzahl der gelieferten Einheiten basiert</span><span class="sxs-lookup"><span data-stu-id="a70bd-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="a70bd-265">Ihre Organisation schließt eine Vereinbarung über die Bereitstellung von insgesamt fünf Schulungssitzungen für die Mitarbeiter eines Kunden zu einem Preis von 10.000 pro Schulungssitzung.</span><span class="sxs-lookup"><span data-stu-id="a70bd-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="a70bd-266">Sie stellen dem Kunden nach jeder Schulung eine Rechnung.</span><span class="sxs-lookup"><span data-stu-id="a70bd-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="a70bd-267">Wenn Sie die Abrechnungsregeln für den Vertrag einrichten, verwenden Sie die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="a70bd-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="a70bd-268">Die Liefereinheit ist eine Schulungssitzung.</span><span class="sxs-lookup"><span data-stu-id="a70bd-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="a70bd-269">Der Stückpreis beträgt 10.000 pro Schulungseinheit.</span><span class="sxs-lookup"><span data-stu-id="a70bd-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="a70bd-270">Die Gesamtzahl der Einheiten beträgt fünf Schulungseinheiten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="a70bd-271">Wenn Sie eine Schulungssitzung abgeschlossen haben, können Sie für die erste gelieferte Einheit eine Rechnung über 10.000 erstellen und die Rechnung an den Kunden senden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="a70bd-272">Beispiel: Erstellen Sie eine Abrechnungsregel, die auf einem bestimmten Prozentsatz des Projektabschlusses basiert (manuelle Berechnung)</span><span class="sxs-lookup"><span data-stu-id="a70bd-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="a70bd-273">Ihre Organisation, ein Software-Beratungsunternehmen, schließt mit einem Kunden eine Vereinbarung über die Entwicklung eines Teils eines Produkts, das der Kunde entwickelt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="a70bd-274">Ihre Organisation verpflichtet sich, den Software-Code über einen Zeitraum von sechs Monaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="a70bd-275">Der Kunde verpflichtet sich, Ihrer Organisation insgesamt 100.000 für die Arbeit zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="a70bd-276">Sie erstellen eine Abrechnungsregel, um dem Kunden eine Rechnung zu stellen, die auf dem im Vertrag angegebenen Prozentsatz der im Projekt abgeschlossenen Arbeiten basiert.</span><span class="sxs-lookup"><span data-stu-id="a70bd-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="a70bd-277">Am Ende des ersten Monats treffen Sie sich mit dem Kunden, um den Prozentsatz der abgeschlossenen Arbeiten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="a70bd-278">Nachdem Sie und der Kunde das Projekt überprüft haben, entscheiden Sie, dass das Projekt zu 15 Prozent abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a70bd-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="a70bd-279">Sie erstellen eine Rechnung für 15.000 (15 Prozent von 100.000) und senden sie an den Kunden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="a70bd-280">Beispiel: Erstellen Sie eine Abrechnungsregel, die auf einem bestimmten Prozentsatz des Projektabschlusses basiert (automatische Berechnung)</span><span class="sxs-lookup"><span data-stu-id="a70bd-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="a70bd-281">Ihre Organisation, eine Softwareentwicklungsfirma, erklärt sich bereit, ein Lohnbuchhaltungspaket für einen Kunden für 30.000 zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="a70bd-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="a70bd-282">Der Kunde verpflichtet sich, Ihre Organisation basierend auf der in Prozent abgeschlossenen Arbeit zu bezahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="a70bd-283">Sie schätzen, dass die Projektkosten 20.000 betragen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="a70bd-284">Der Projektvertrag legt die Arbeitskategorien fest, die Sie im Abrechnungsprozess verwenden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="a70bd-285">Sie richten Abrechnungsregeln ein, die automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Arbeit für jede Kategorie berechnen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="a70bd-286">Sie richten für jede Kategorie ein Budget ein:</span><span class="sxs-lookup"><span data-stu-id="a70bd-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="a70bd-287">**Entwicklung** – Kosten von 15.000 und Einnahmen von 20.000</span><span class="sxs-lookup"><span data-stu-id="a70bd-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="a70bd-288">**Entwicklung** – Kosten von 5.000 und Umsatz von 10.000</span><span class="sxs-lookup"><span data-stu-id="a70bd-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="a70bd-289">Wenn Sie zum ersten Mal eine Kundenrechnung erstellen, wird der Rechnungsbetrag automatisch anhand der folgenden Informationen berechnet:</span><span class="sxs-lookup"><span data-stu-id="a70bd-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="a70bd-290">Nach einem Monat legt der Projektmitarbeiter eine Arbeitszeittabelle für das Projekt vor.</span><span class="sxs-lookup"><span data-stu-id="a70bd-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="a70bd-291">Die Arbeitsstunden betragen 5.000 für die Entwicklung und 1.000 für die Installation.</span><span class="sxs-lookup"><span data-stu-id="a70bd-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="a70bd-292">Die Entwicklungsarbeiten sind zu 33 Prozent abgeschlossen (5.000 tatsächliche Kosten/15.000 Budgetkosten) und die Installationsarbeiten zu 20 Prozent abgeschlossen (1.000 tatsächliche Kosten/5.000 Budgetkosten).</span><span class="sxs-lookup"><span data-stu-id="a70bd-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="a70bd-293">Der Rechnungsbetrag von 8.667 wird automatisch berechnet (33 Prozent von 20.000 + 20 Prozent von 10.000).</span><span class="sxs-lookup"><span data-stu-id="a70bd-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="a70bd-294">Sie erstellen eine Rechnung für 8667 und senden sie an den Kunden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="a70bd-295">Beispiel: Erstellen Sie eine Abrechnungsregel, die auf vereinbarten Meilensteinen basiert</span><span class="sxs-lookup"><span data-stu-id="a70bd-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="a70bd-296">Ihre Organisation, eine Unternehmensberatung, erklärt sich bereit, Marktforschungen für ein Verbraucherprodukt durchzuführen, das der Kunde verkaufen möchte.</span><span class="sxs-lookup"><span data-stu-id="a70bd-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="a70bd-297">Der Kunde verpflichtet sich, Ihre Dienste ab März für einen Zeitraum von drei Monaten zu nutzen, und verpflichtet sich, Ihrer Organisation 50.000 zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="a70bd-298">Das Projekt hat drei Meilensteine:</span><span class="sxs-lookup"><span data-stu-id="a70bd-298">The project has three milestones:</span></span>

-   <span data-ttu-id="a70bd-299">Meilenstein 1: Verbraucherdaten sammeln – 31. März</span><span class="sxs-lookup"><span data-stu-id="a70bd-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="a70bd-300">Meilenstein 2: Verbraucherdaten analysieren – 30. April</span><span class="sxs-lookup"><span data-stu-id="a70bd-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="a70bd-301">Meilenstein 3: Vorlage eines Vorschlags zur Produktlebensfähigkeit – 31. Mai</span><span class="sxs-lookup"><span data-stu-id="a70bd-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="a70bd-302">Der Kunde verpflichtet sich, Ihrer Organisation 10.000 für den ersten Meilenstein, 20.000 für den zweiten Meilenstein und 20.000 für den dritten Meilenstein zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="a70bd-303">Wenn Sie den Projektvertrag einrichten, erklären Sie sich damit einverstanden, dem Kunden den Meilenstein in Rechnung zu stellen, der abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a70bd-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="a70bd-304">Das Einrichten der Abrechnungsregeln umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="a70bd-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="a70bd-305">Projektmeilensteine definieren.</span><span class="sxs-lookup"><span data-stu-id="a70bd-305">Define the project milestones.</span></span>
-   <span data-ttu-id="a70bd-306">Definieren Sie den Betrag, der dem Kunden nach Abschluss jedes Meilensteins in Rechnung gestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a70bd-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="a70bd-307">Wenn der erste Meilenstein am 31. März abgeschlossen ist, markieren Sie den Meilenstein als abgeschlossen, erstellen eine Rechnung über 10.000 und senden sie an den Kunden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="a70bd-308">Sie können keine Rechnung für einen Meilenstein erstellen, bis Sie den Meilenstein als abgeschlossen markiert haben.</span><span class="sxs-lookup"><span data-stu-id="a70bd-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="a70bd-309">Beispiel: Erstellen Sie eine Abrechnungsregel, die auf Services zuzüglich einer Verwaltungsgebühr basiert</span><span class="sxs-lookup"><span data-stu-id="a70bd-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="a70bd-310">Ihre Organisation, eine Unternehmensberatung, erklärt sich bereit, Marktforschungen durchzuführen, um die Lebensfähigkeit eines Produkts zu bewerten, das der Kunde, ein Einzelhandelsunternehmen, entwickelt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="a70bd-311">In den Vertragsbedingungen ist festgelegt, dass Sie die Dienste Ihrer drei wichtigsten Unternehmensberater erbringen, die die Recherchen zeit- und materialbezogen durchführen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="a70bd-312">Der Kunde verpflichtet sich, 100 pro Stunde zuzüglich einer Verwaltungsgebühr von 10 Prozent für die dem Projekt in Rechnung gestellten Beratungsstunden zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a70bd-313">Erstellen Sie beim Einrichten des Projektvertrags eine Abrechnungsregel, um eine Verwaltungsgebühr von 10 Prozent zu den Beratungsstunden hinzuzufügen, die dem Projekt in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="a70bd-314">Wenn Sie eine Rechnung für den Kunden erstellen, wird dem Kunden eine Verwaltungsgebühr von 10 Prozent zuzüglich der Kosten für die Beratungsstunden in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="a70bd-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="a70bd-315">Wenn die drei Berater beispielsweise insgesamt 200 Stunden an dem Projekt gearbeitet haben, wird auf der Grundlage der folgenden Berechnung eine Rechnung über 22.000 erstellt:</span><span class="sxs-lookup"><span data-stu-id="a70bd-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="a70bd-316">200 Stunden bei 100 pro Stunde = 20.000</span><span class="sxs-lookup"><span data-stu-id="a70bd-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="a70bd-317">10 Prozent Verwaltungsgebühr = 2.000</span><span class="sxs-lookup"><span data-stu-id="a70bd-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="a70bd-318">Gesamtbetrag = 22.000</span><span class="sxs-lookup"><span data-stu-id="a70bd-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="a70bd-319">Wenn für einen Kunden Gebühren steuerpflichtig sind und Sie im Projektvertrag eine Umsatzsteuergruppe auswählen, wird die Umsatzsteuergruppe automatisch in eine Abrechnungsregel für Gebühren eingetragen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="a70bd-320">Beispiel: Erstellen Sie eine Abrechnungsregel für den Wert von Zeit und Material</span><span class="sxs-lookup"><span data-stu-id="a70bd-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="a70bd-321">Ihre Organisation, eine Softwareberatungsfirma, verpflichtet sich, fünf technische Berater zur Verfügung zu stellen, die für die nächsten sechs Monate an einem Softwareentwicklungsprojekt für einen Kunden arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="a70bd-322">Der Kunde verpflichtet sich, 150 pro Beratungsstunde zuzüglich der Kosten für Büromaterial zu zahlen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="a70bd-323">Ihre Organisation sendet am Ende eines jeden Monats eine Rechnung an den Kunden.</span><span class="sxs-lookup"><span data-stu-id="a70bd-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="a70bd-324">Wenn Sie den Projektvertrag abschließen, erklären Sie sich damit einverstanden, dem Kunden jeden Monat Zeit und Material für das Projekt in Rechnung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a70bd-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="a70bd-325">Sie erstellen eine Abrechnungsregel, die folgende Informationen enthält:</span><span class="sxs-lookup"><span data-stu-id="a70bd-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="a70bd-326">Die Vertragslaufzeit beträgt sechs Monate.</span><span class="sxs-lookup"><span data-stu-id="a70bd-326">The contract period is six months.</span></span>
-   <span data-ttu-id="a70bd-327">Die Beratungszeit wird mit 150 pro Stunde berechnet.</span><span class="sxs-lookup"><span data-stu-id="a70bd-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="a70bd-328">Büromaterial wird zu Anschaffungskosten in Rechnung gestellt, und die Gesamtkosten für das Projekt dürfen 10.000 nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="a70bd-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="a70bd-329">Sie erstellen am Ende jedes Kalendermonats während des Projekts eine Kundenrechnung.</span><span class="sxs-lookup"><span data-stu-id="a70bd-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="a70bd-330">Im ersten Monat werden von den Beratern des Projekts insgesamt 800 Stunden aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a70bd-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="a70bd-331">Die Kosten für Büromaterial, das dem Projekt in Rechnung gestellt wird, betragen 2.000.</span><span class="sxs-lookup"><span data-stu-id="a70bd-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="a70bd-332">Daher erstellen Sie am Monatsende eine Rechnung über 122.000, die als 800 Stunden bei 150 pro Stunde plus 2.000 für Büromaterial berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="a70bd-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]