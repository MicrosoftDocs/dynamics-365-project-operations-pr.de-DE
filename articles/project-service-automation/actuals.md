---
title: Ist-Werte
description: Dieses Thema enthält Informationen zu Projekt-Istwerten.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722037"
---
# <a name="actuals"></a><span data-ttu-id="a17b5-103">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="a17b5-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a17b5-104">Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="a17b5-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a17b5-105">Projekt-Istwerte können zu ihren Quelldokumenten zurückverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a17b5-106">Diese Quelldokumente umfassen Zeit-, Ausgaben- und Journaleinträge und auch Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![So werden Projekt-Istwerte zu den Quelldokumenten zurückverfolgt](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a17b5-108">Übermitteln eines Zeiteintrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-108">Submitting a time entry</span></span>

<span data-ttu-id="a17b5-109">Wenn in PSA ein Zeiteintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a17b5-110">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="a17b5-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a17b5-111">Wenn ein Zeiteintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a17b5-112">Die Logik zur Eingabe von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="a17b5-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a17b5-113">Alle Feldwerte eines Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="a17b5-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a17b5-114">Diese Felder enthalten das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="a17b5-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a17b5-115">In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, wird standardmäßig ein entsprechender Preis in die Erfassungsposition eingegeben.</span><span class="sxs-lookup"><span data-stu-id="a17b5-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a17b5-116">Wenn Sie dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen und möchten, dass der Feldwert an „Ist-Werte” weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte” und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="a17b5-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a17b5-117">Übermitteln eines Ausgabeneintrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-117">Submitting an expense entry</span></span>

<span data-ttu-id="a17b5-118">Wenn in PSA ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a17b5-119">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="a17b5-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a17b5-120">Wenn ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a17b5-121">Die Logik zur Eingabe von Standardpreisen basiert auf der Ausgabenkategorie, die auf der Seite **Ausgabeneintrag** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a17b5-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a17b5-122">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="a17b5-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a17b5-123">Für den Preis selbst wird der vom Benutzer eingegebene Betrag jedoch standardmäßig direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a17b5-124">In der aktuellen Version von PSA ist der kategoriebasierte Eintrag von Standardpreisen pro Einheit bei Ausgabeneinträgen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a17b5-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="a17b5-125">Verwenden von Journalen zur Erfassung von Kosten</span><span class="sxs-lookup"><span data-stu-id="a17b5-125">Using journals to record costs</span></span>

<span data-ttu-id="a17b5-126">In PSA können Sie mithilfe von Journalen Kosten bzw. Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a17b5-127">Ein Journal enthält eine Kopfzeile, Zeilen und eine Aktion **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="a17b5-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a17b5-128">Hier finden Sie einige Szenarien, in denen Sie möglicherweise ein Journal verwenden:</span><span class="sxs-lookup"><span data-stu-id="a17b5-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a17b5-129">Bei einem Projekt müssen Sie die tatsächlichen Materialkosten und -umsätze erfassen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a17b5-130">Sie müssen Transaktions-Istwerte aus einem anderen System in PSA importieren.</span><span class="sxs-lookup"><span data-stu-id="a17b5-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a17b5-131">Sie müssen Kosten erfassen, die in einem anderen System angefallen sind, z. B. Beschaffungskosten oder Kosten für Unteraufträge.</span><span class="sxs-lookup"><span data-stu-id="a17b5-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a17b5-132">Erfassen von Ist-Werten basierend auf Projektereignissen</span><span class="sxs-lookup"><span data-stu-id="a17b5-132">Recording actuals based on project events</span></span>

<span data-ttu-id="a17b5-133">PSA erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a17b5-134">Diese Transaktionen werden als **Ist-Werte** aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a17b5-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a17b5-135">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="a17b5-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a17b5-136">**Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts**</span><span class="sxs-lookup"><span data-stu-id="a17b5-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a17b5-137">Ereignis</span><span class="sxs-lookup"><span data-stu-id="a17b5-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a17b5-138">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="a17b5-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a17b5-139">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="a17b5-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a17b5-140">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="a17b5-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a17b5-141">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="a17b5-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a17b5-142">Festpreis</span><span class="sxs-lookup"><span data-stu-id="a17b5-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a17b5-143">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="a17b5-143">Actuals</span></span></th>
<th><span data-ttu-id="a17b5-144">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="a17b5-144">Transaction currency</span></span></th>
<th><span data-ttu-id="a17b5-145">Festpreis</span><span class="sxs-lookup"><span data-stu-id="a17b5-145">Fixed price</span></span></th>
<th><span data-ttu-id="a17b5-146">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="a17b5-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a17b5-147">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a17b5-148">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="a17b5-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-149">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a17b5-150">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="a17b5-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a17b5-151">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a17b5-152">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-152">Cost actual</span></span></td>
<td><span data-ttu-id="a17b5-153">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-154">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-155">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a17b5-156">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-157">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-158">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a17b5-159">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a17b5-160">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a17b5-161">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-161">Cost actual</span></span></td>
<td><span data-ttu-id="a17b5-162">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-163">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-164">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-165">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-166">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-167">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-168">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-169">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-170">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a17b5-171">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a17b5-172">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a17b5-173">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-174">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="a17b5-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-175">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-176">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-177">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-178">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="a17b5-178">Billed sales</span></span></td>
<td><span data-ttu-id="a17b5-179">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a17b5-180">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a17b5-181">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a17b5-182">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-183">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-184">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-185">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-187">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-188">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-189">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-190">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a17b5-191">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a17b5-192">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a17b5-193">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a17b5-194">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="a17b5-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a17b5-195">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="a17b5-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a17b5-196">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-197">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-198">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-199">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="a17b5-199">Billed sales</span></span></td>
<td><span data-ttu-id="a17b5-200">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a17b5-201">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="a17b5-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a17b5-202">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a17b5-203">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-204">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-205">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-206">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-207">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a17b5-208">**Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet**</span><span class="sxs-lookup"><span data-stu-id="a17b5-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a17b5-209">Ereignis</span><span class="sxs-lookup"><span data-stu-id="a17b5-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a17b5-210">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="a17b5-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a17b5-211">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="a17b5-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a17b5-212">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="a17b5-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a17b5-213">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="a17b5-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a17b5-214">Festpreis</span><span class="sxs-lookup"><span data-stu-id="a17b5-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a17b5-215">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="a17b5-215">Actuals</span></span></th>
<th><span data-ttu-id="a17b5-216">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="a17b5-216">Transaction currency</span></span></th>
<th><span data-ttu-id="a17b5-217">Festpreis</span><span class="sxs-lookup"><span data-stu-id="a17b5-217">Fixed price</span></span></th>
<th><span data-ttu-id="a17b5-218">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="a17b5-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a17b5-219">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a17b5-220">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="a17b5-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-221">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a17b5-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a17b5-222">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="a17b5-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a17b5-223">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a17b5-224">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-224">Cost actual</span></span></td>
<td><span data-ttu-id="a17b5-225">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a17b5-226">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a17b5-227">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a17b5-228">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a17b5-229">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-230">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a17b5-231">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-232">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a17b5-233">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-234">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="a17b5-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a17b5-235">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a17b5-236">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a17b5-237">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-237">Cost actual</span></span></td>
<td><span data-ttu-id="a17b5-238">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-239">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-240">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-241">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-242">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="a17b5-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-243">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a17b5-244">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-245">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="a17b5-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a17b5-246">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="a17b5-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-247">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-248">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-249">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-250">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a17b5-251">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a17b5-252">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a17b5-253">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-254">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="a17b5-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-255">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-256">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a17b5-257">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-258">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="a17b5-258">Billed sales</span></span></td>
<td><span data-ttu-id="a17b5-259">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a17b5-260">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a17b5-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a17b5-261">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a17b5-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-263">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-264">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-265">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a17b5-266">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-267">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-268">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-269">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-270">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a17b5-271">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="a17b5-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a17b5-272">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a17b5-273">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a17b5-274">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="a17b5-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a17b5-275">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="a17b5-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a17b5-276">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-277">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a17b5-278">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="a17b5-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-279">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="a17b5-279">Billed sales</span></span></td>
<td><span data-ttu-id="a17b5-280">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a17b5-281">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="a17b5-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a17b5-282">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="a17b5-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a17b5-283">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-284">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="a17b5-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a17b5-285">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a17b5-286">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="a17b5-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a17b5-287">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="a17b5-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
