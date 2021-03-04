---
title: Tatsächliche Transaktionen – Übersicht
description: Dieses Thema enthält Informationen zu Projekt-Istwerten.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146122"
---
# <a name="actuals-overview"></a><span data-ttu-id="fef04-103">Tatsächliche Transaktionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="fef04-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fef04-104">Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="fef04-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="fef04-105">Projekt-Istwerte können zu ihren Quelldokumenten zurückverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="fef04-106">Diese Quelldokumente umfassen Zeit-, Ausgaben- und Journaleinträge und auch Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="fef04-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![So werden Projekt-Istwerte zu den Quelldokumenten zurückverfolgt](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="fef04-108">Übermitteln eines Zeiteintrags</span><span class="sxs-lookup"><span data-stu-id="fef04-108">Submitting a time entry</span></span>

<span data-ttu-id="fef04-109">Wenn in PSA ein Zeiteintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="fef04-110">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="fef04-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="fef04-111">Wenn ein Zeiteintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="fef04-112">Die Logik zur Eingabe von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="fef04-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="fef04-113">Alle Feldwerte eines Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="fef04-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="fef04-114">Diese Felder enthalten das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="fef04-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="fef04-115">In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, wird standardmäßig ein entsprechender Preis in die Erfassungsposition eingegeben.</span><span class="sxs-lookup"><span data-stu-id="fef04-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="fef04-116">Wenn Sie dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen und möchten, dass der Feldwert an „Ist-Werte” weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte” und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="fef04-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="fef04-117">Übermitteln eines Ausgabeneintrags</span><span class="sxs-lookup"><span data-stu-id="fef04-117">Submitting an expense entry</span></span>

<span data-ttu-id="fef04-118">Wenn in PSA ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="fef04-119">Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb.</span><span class="sxs-lookup"><span data-stu-id="fef04-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="fef04-120">Wenn ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="fef04-121">Die Logik zur Eingabe von Standardpreisen basiert auf der Ausgabenkategorie, die auf der Seite **Ausgabeneintrag** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="fef04-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="fef04-122">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="fef04-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="fef04-123">Für den Preis selbst wird der vom Benutzer eingegebene Betrag jedoch standardmäßig direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fef04-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="fef04-124">In der aktuellen Version von PSA ist der kategoriebasierte Eintrag von Standardpreisen pro Einheit bei Ausgabeneinträgen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fef04-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="fef04-125">Verwenden von Eintragserfassungen zum Erfassen von Kosten</span><span class="sxs-lookup"><span data-stu-id="fef04-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="fef04-126">In PSA können Sie mithilfe von Eintragserfassungen Kosten bzw. Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="fef04-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="fef04-127">Ein Journal enthält eine Kopfzeile, Zeilen und eine Aktion **Bestätigen**.</span><span class="sxs-lookup"><span data-stu-id="fef04-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="fef04-128">Hier finden Sie einige Szenarien, in denen Sie möglicherweise ein Journal verwenden:</span><span class="sxs-lookup"><span data-stu-id="fef04-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="fef04-129">Bei einem Projekt müssen Sie die tatsächlichen Materialkosten und -umsätze erfassen.</span><span class="sxs-lookup"><span data-stu-id="fef04-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="fef04-130">Sie müssen Transaktions-Istwerte aus einem anderen System in PSA importieren.</span><span class="sxs-lookup"><span data-stu-id="fef04-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="fef04-131">Sie müssen Kosten erfassen, die in einem anderen System angefallen sind, z. B. Beschaffungskosten oder Kosten für Unteraufträge.</span><span class="sxs-lookup"><span data-stu-id="fef04-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fef04-132">Istwerte sollten nur mithilfe von Eintragsjournalen erstellt werden, wenn dem Benutzer die buchhalterische Auswirkung der Istwerte auf das Projekt voll bewusst ist.</span><span class="sxs-lookup"><span data-stu-id="fef04-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="fef04-133">Dies liegt daran, dass die Anwendung den Erfassungsposition oder den zugehörigen Preis, der in der Erfassungsposition eingegeben wird, nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fef04-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="fef04-134">Seien Sie aufgrund der Auswirkungen dieses Erfassungstyps entsprechend vorsichtig dabei, wer Zugriff auf die Erstellung von Eintragserfassungen erhält.</span><span class="sxs-lookup"><span data-stu-id="fef04-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="fef04-135">Erfassen von Ist-Werten basierend auf Projektereignissen</span><span class="sxs-lookup"><span data-stu-id="fef04-135">Recording actuals based on project events</span></span>

<span data-ttu-id="fef04-136">PSA erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="fef04-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="fef04-137">Diese Transaktionen werden als **Ist-Werte** aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fef04-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="fef04-138">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="fef04-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="fef04-139">**Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts**</span><span class="sxs-lookup"><span data-stu-id="fef04-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="fef04-140">Ereignis</span><span class="sxs-lookup"><span data-stu-id="fef04-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="fef04-141">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="fef04-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="fef04-142">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="fef04-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="fef04-143">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="fef04-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="fef04-144">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="fef04-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="fef04-145">Festpreis</span><span class="sxs-lookup"><span data-stu-id="fef04-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fef04-146">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="fef04-146">Actuals</span></span></th>
<th><span data-ttu-id="fef04-147">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="fef04-147">Transaction currency</span></span></th>
<th><span data-ttu-id="fef04-148">Festpreis</span><span class="sxs-lookup"><span data-stu-id="fef04-148">Fixed price</span></span></th>
<th><span data-ttu-id="fef04-149">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="fef04-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fef04-150">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="fef04-151">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="fef04-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-152">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fef04-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="fef04-153">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="fef04-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fef04-154">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fef04-155">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-155">Cost actual</span></span></td>
<td><span data-ttu-id="fef04-156">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-157">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-158">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="fef04-159">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-160">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-161">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="fef04-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="fef04-162">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fef04-163">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fef04-164">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-164">Cost actual</span></span></td>
<td><span data-ttu-id="fef04-165">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-166">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-167">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-168">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-169">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-170">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-171">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-172">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-173">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fef04-174">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fef04-175">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fef04-176">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-177">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="fef04-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-178">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-179">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-180">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-181">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="fef04-181">Billed sales</span></span></td>
<td><span data-ttu-id="fef04-182">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fef04-183">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fef04-184">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fef04-185">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-187">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-188">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-189">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-190">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-191">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-192">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-193">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fef04-194">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fef04-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fef04-195">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fef04-196">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="fef04-197">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="fef04-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="fef04-198">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="fef04-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="fef04-199">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-200">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-201">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-202">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="fef04-202">Billed sales</span></span></td>
<td><span data-ttu-id="fef04-203">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fef04-204">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fef04-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fef04-205">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fef04-206">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-207">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-208">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-209">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-210">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fef04-211">**Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet**</span><span class="sxs-lookup"><span data-stu-id="fef04-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="fef04-212">Ereignis</span><span class="sxs-lookup"><span data-stu-id="fef04-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="fef04-213">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="fef04-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="fef04-214">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="fef04-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="fef04-215">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="fef04-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="fef04-216">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="fef04-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="fef04-217">Festpreis</span><span class="sxs-lookup"><span data-stu-id="fef04-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="fef04-218">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="fef04-218">Actuals</span></span></th>
<th><span data-ttu-id="fef04-219">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="fef04-219">Transaction currency</span></span></th>
<th><span data-ttu-id="fef04-220">Festpreis</span><span class="sxs-lookup"><span data-stu-id="fef04-220">Fixed price</span></span></th>
<th><span data-ttu-id="fef04-221">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="fef04-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fef04-222">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="fef04-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="fef04-223">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="fef04-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-224">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fef04-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="fef04-225">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="fef04-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="fef04-226">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fef04-227">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-227">Cost actual</span></span></td>
<td><span data-ttu-id="fef04-228">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="fef04-229">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="fef04-230">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="fef04-231">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="fef04-232">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-233">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="fef04-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="fef04-234">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-235">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="fef04-236">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-237">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="fef04-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="fef04-238">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="fef04-239">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="fef04-240">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-240">Cost actual</span></span></td>
<td><span data-ttu-id="fef04-241">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-242">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-243">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-244">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-245">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="fef04-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-246">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="fef04-247">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-248">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="fef04-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="fef04-249">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="fef04-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-250">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-251">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-252">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-253">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fef04-254">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fef04-255">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fef04-256">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-257">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="fef04-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-258">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-259">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="fef04-260">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-261">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="fef04-261">Billed sales</span></span></td>
<td><span data-ttu-id="fef04-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fef04-263">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fef04-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="fef04-264">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="fef04-265">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-266">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-267">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-268">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="fef04-269">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-270">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-271">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-272">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-273">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="fef04-274">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fef04-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fef04-275">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fef04-276">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="fef04-277">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="fef04-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="fef04-278">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="fef04-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="fef04-279">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-280">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="fef04-281">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="fef04-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-282">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="fef04-282">Billed sales</span></span></td>
<td><span data-ttu-id="fef04-283">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="fef04-284">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="fef04-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="fef04-285">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="fef04-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="fef04-286">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-287">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="fef04-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="fef04-288">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fef04-289">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="fef04-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="fef04-290">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="fef04-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
