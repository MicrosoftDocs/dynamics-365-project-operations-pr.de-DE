---
title: Tatsächliche Transaktionen – Übersicht
description: Dieses Thema enthält Informationen zu Projekt-Istwerten.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
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
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368160"
---
# <a name="actuals-overview"></a><span data-ttu-id="295df-103">Tatsächliche Transaktionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="295df-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="295df-104">Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="295df-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="295df-105">Projekt-Istwerte können zu ihren Quelldokumenten zurückverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="295df-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="295df-106">Diese Quelldokumente umfassen Zeit-, Ausgaben- und Journaleinträge und auch Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="295df-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![So werden Projekt-Istwerte zu den Quelldokumenten zurückverfolgt](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="295df-108">Übermitteln eines Zeiteintrags</span><span class="sxs-lookup"><span data-stu-id="295df-108">Submitting a time entry</span></span>

<span data-ttu-id="295df-109">Wenn in PSA ein Zeiteintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="295df-110">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="295df-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="295df-111">Wenn ein Zeiteintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="295df-112">Die Logik zur Eingabe von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="295df-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="295df-113">Alle Feldwerte eines Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="295df-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="295df-114">Diese Felder enthalten das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="295df-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="295df-115">In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, wird standardmäßig ein entsprechender Preis in die Erfassungsposition eingegeben.</span><span class="sxs-lookup"><span data-stu-id="295df-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="295df-116">Wenn Sie dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen und möchten, dass der Feldwert an „Ist-Werte” weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte” und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="295df-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="295df-117">Übermitteln eines Ausgabeneintrags</span><span class="sxs-lookup"><span data-stu-id="295df-117">Submitting an expense entry</span></span>

<span data-ttu-id="295df-118">Wenn in PSA ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="295df-119">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="295df-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="295df-120">Wenn ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="295df-121">Die Logik zur Eingabe von Standardpreisen basiert auf der Ausgabenkategorie, die auf der Seite **Ausgabeneintrag** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="295df-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="295df-122">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="295df-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="295df-123">Für den Preis selbst wird der vom Benutzer eingegebene Betrag jedoch standardmäßig direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="295df-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="295df-124">In der aktuellen Version von PSA ist der kategoriebasierte Eintrag von Standardpreisen pro Einheit bei Ausgabeneinträgen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="295df-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="295df-125">Verwenden von Eintragserfassungen zum Erfassen von Kosten</span><span class="sxs-lookup"><span data-stu-id="295df-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="295df-126">In PSA können Sie mithilfe von Eintragserfassungen Kosten bzw. Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="295df-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="295df-127">Ein Journal enthält eine Kopfzeile, Zeilen und eine Aktion **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="295df-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="295df-128">Hier finden Sie einige Szenarien, in denen Sie möglicherweise ein Journal verwenden:</span><span class="sxs-lookup"><span data-stu-id="295df-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="295df-129">Bei einem Projekt müssen Sie die tatsächlichen Materialkosten und -umsätze erfassen.</span><span class="sxs-lookup"><span data-stu-id="295df-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="295df-130">Sie müssen Transaktions-Istwerte aus einem anderen System in PSA importieren.</span><span class="sxs-lookup"><span data-stu-id="295df-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="295df-131">Sie müssen Kosten erfassen, die in einem anderen System angefallen sind, z. B. Beschaffungskosten oder Kosten für Unteraufträge.</span><span class="sxs-lookup"><span data-stu-id="295df-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="295df-132">Istwerte sollten nur mithilfe von Eintragsjournalen erstellt werden, wenn dem Benutzer die buchhalterische Auswirkung der Istwerte auf das Projekt voll bewusst ist.</span><span class="sxs-lookup"><span data-stu-id="295df-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="295df-133">Dies liegt daran, dass die Anwendung den Erfassungsposition oder den zugehörigen Preis, der in der Erfassungsposition eingegeben wird, nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="295df-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="295df-134">Seien Sie aufgrund der Auswirkungen dieses Erfassungstyps entsprechend vorsichtig dabei, wer Zugriff auf die Erstellung von Eintragserfassungen erhält.</span><span class="sxs-lookup"><span data-stu-id="295df-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="295df-135">Erfassen von Ist-Werten basierend auf Projektereignissen</span><span class="sxs-lookup"><span data-stu-id="295df-135">Recording actuals based on project events</span></span>

<span data-ttu-id="295df-136">PSA erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="295df-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="295df-137">Diese Transaktionen werden als **Ist-Werte** aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="295df-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="295df-138">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="295df-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="295df-139">**Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts**</span><span class="sxs-lookup"><span data-stu-id="295df-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="295df-140">Ereignis</span><span class="sxs-lookup"><span data-stu-id="295df-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="295df-141">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="295df-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="295df-142">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="295df-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="295df-143">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="295df-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="295df-144">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="295df-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="295df-145">Festpreis</span><span class="sxs-lookup"><span data-stu-id="295df-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="295df-146">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="295df-146">Actuals</span></span></th>
<th><span data-ttu-id="295df-147">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="295df-147">Transaction currency</span></span></th>
<th><span data-ttu-id="295df-148">Festpreis</span><span class="sxs-lookup"><span data-stu-id="295df-148">Fixed price</span></span></th>
<th><span data-ttu-id="295df-149">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="295df-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="295df-150">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="295df-151">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="295df-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-152">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="295df-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="295df-153">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="295df-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="295df-154">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="295df-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="295df-155">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-155">Cost actual</span></span></td>
<td><span data-ttu-id="295df-156">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-157">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-158">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="295df-159">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-160">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-161">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="295df-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="295df-162">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="295df-163">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="295df-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="295df-164">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-164">Cost actual</span></span></td>
<td><span data-ttu-id="295df-165">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-166">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-167">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-168">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-169">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-170">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="295df-171">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-172">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-173">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="295df-174">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="295df-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="295df-175">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="295df-176">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-177">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="295df-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-178">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-179">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-180">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-181">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="295df-181">Billed sales</span></span></td>
<td><span data-ttu-id="295df-182">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="295df-183">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="295df-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="295df-184">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="295df-185">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-187">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-188">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-189">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-190">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="295df-191">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-192">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-193">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="295df-194">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="295df-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="295df-195">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="295df-196">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="295df-197">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="295df-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="295df-198">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="295df-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="295df-199">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-200">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-201">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-202">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="295df-202">Billed sales</span></span></td>
<td><span data-ttu-id="295df-203">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="295df-204">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="295df-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="295df-205">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="295df-206">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-207">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="295df-208">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-209">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-210">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="295df-211">**Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet**</span><span class="sxs-lookup"><span data-stu-id="295df-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="295df-212">Ereignis</span><span class="sxs-lookup"><span data-stu-id="295df-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="295df-213">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="295df-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="295df-214">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="295df-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="295df-215">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="295df-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="295df-216">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="295df-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="295df-217">Festpreis</span><span class="sxs-lookup"><span data-stu-id="295df-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="295df-218">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="295df-218">Actuals</span></span></th>
<th><span data-ttu-id="295df-219">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="295df-219">Transaction currency</span></span></th>
<th><span data-ttu-id="295df-220">Festpreis</span><span class="sxs-lookup"><span data-stu-id="295df-220">Fixed price</span></span></th>
<th><span data-ttu-id="295df-221">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="295df-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="295df-222">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="295df-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="295df-223">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="295df-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-224">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="295df-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="295df-225">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="295df-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="295df-226">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="295df-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="295df-227">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-227">Cost actual</span></span></td>
<td><span data-ttu-id="295df-228">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="295df-229">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="295df-230">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="295df-231">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="295df-232">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-233">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="295df-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="295df-234">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-235">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="295df-236">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-237">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="295df-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="295df-238">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="295df-239">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="295df-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="295df-240">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-240">Cost actual</span></span></td>
<td><span data-ttu-id="295df-241">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-242">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-243">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-244">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-245">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="295df-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-246">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="295df-247">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-248">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="295df-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="295df-249">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="295df-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-250">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="295df-251">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-252">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-253">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="295df-254">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="295df-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="295df-255">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="295df-256">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-257">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="295df-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-258">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-259">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="295df-260">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-261">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="295df-261">Billed sales</span></span></td>
<td><span data-ttu-id="295df-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="295df-263">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="295df-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="295df-264">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="295df-265">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-266">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-267">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-268">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="295df-269">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-270">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="295df-271">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-272">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-273">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="295df-274">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="295df-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="295df-275">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="295df-276">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="295df-277">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="295df-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="295df-278">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="295df-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="295df-279">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-280">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="295df-281">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="295df-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-282">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="295df-282">Billed sales</span></span></td>
<td><span data-ttu-id="295df-283">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="295df-284">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="295df-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="295df-285">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="295df-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="295df-286">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-287">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="295df-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="295df-288">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="295df-289">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="295df-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="295df-290">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="295df-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]