---
title: Istwerte-Homepage
description: Dieses Thema bietet Informationen darüber, wie in Microsoft Dynamics 365 Project Operations mit Ist-Werten gearbeitet wird.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907317"
---
# <a name="actuals"></a><span data-ttu-id="29c82-103">Tatsächliche Transaktionen</span><span class="sxs-lookup"><span data-stu-id="29c82-103">Actuals</span></span>

<span data-ttu-id="29c82-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="29c82-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="29c82-105">Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="29c82-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="29c82-106">Sie werden als Ergebnis von Zeit- und Kosteneingaben sowie Erfassungseinträgen und Rechnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="29c82-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="29c82-107">Erfassungspositionen und Zeiteinreichung</span><span class="sxs-lookup"><span data-stu-id="29c82-107">Journal lines and time submission</span></span>

<span data-ttu-id="29c82-108">Weitere Informationen zum Zeiteintrag finden Sie unter [Zeiteintragsübersicht](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29c82-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="29c82-109">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="29c82-109">Time and materials</span></span>

<span data-ttu-id="29c82-110">Wenn ein übermittelter Zeiteintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="29c82-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="29c82-111">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-111">Fixed price</span></span>

<span data-ttu-id="29c82-112">Wenn ein eingereichter Zeiteintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.</span><span class="sxs-lookup"><span data-stu-id="29c82-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="29c82-113">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="29c82-113">Default pricing</span></span>

<span data-ttu-id="29c82-114">Die Logik zur Erstellung von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="29c82-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="29c82-115">Die Feldwerte des Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="29c82-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="29c82-116">Diese Werte enthalten das Transaktionsdatum, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="29c82-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="29c82-117">In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="29c82-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="29c82-118">Sie können dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="29c82-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="29c82-119">Wenn Sie möchten, dass der Feldwert an „Ist-Werte“ weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte“ und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="29c82-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="29c82-120">Erfassungspositionen und Einreichung der Grundkosten</span><span class="sxs-lookup"><span data-stu-id="29c82-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="29c82-121">Weitere Informationen zum Ausgabeneintrag finden Sie unter [Ausgabeneintragsübersicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29c82-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="29c82-122">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="29c82-122">Time and materials</span></span>

<span data-ttu-id="29c82-123">Wenn ein übermittelter Grundkosteneintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="29c82-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="29c82-124">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-124">Fixed price</span></span>

<span data-ttu-id="29c82-125">Wenn ein eingereichter Grundkosteneintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.</span><span class="sxs-lookup"><span data-stu-id="29c82-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="29c82-126">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="29c82-126">Default pricing</span></span>

<span data-ttu-id="29c82-127">Die Logik zur Eingabe von Standardpreisen für Ausgaben basiert auf der Ausgabenkategorie.</span><span class="sxs-lookup"><span data-stu-id="29c82-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="29c82-128">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="29c82-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="29c82-129">Für den Preis selbst wird standardmäßig der vom Benutzer eingegebene Betrag jedoch direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29c82-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="29c82-130">Der kategoriebasierte Eintrag von Standardpreisen pro Einheit ist bei Ausgabeneinträgen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="29c82-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="29c82-131">Eintragserfassungen zur Erfassung von Kosten verwenden</span><span class="sxs-lookup"><span data-stu-id="29c82-131">Use entry journals to record costs</span></span>

<span data-ttu-id="29c82-132">Sie können mithilfe von Erfassungenn die Kosten bzw. den Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="29c82-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="29c82-133">Erfassungen können für die folgenden Zwecke verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="29c82-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="29c82-134">Zeichnen Sie die Ist-Kosten der Materialien und Umsätze bei einem Projekt auf.</span><span class="sxs-lookup"><span data-stu-id="29c82-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="29c82-135">Verschieben Sie Transaktions-Istwerte aus einem anderen System in Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="29c82-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="29c82-136">Zeichnen Sie die Kosten auf, die in einem anderen System aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="29c82-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="29c82-137">Diese Kosten können Beschaffungs- oder Fremdarbeitskosten umfassen.</span><span class="sxs-lookup"><span data-stu-id="29c82-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29c82-138">Die Anwendung überprüft weder den Erfassungspositionstyp noch den zugehörigen Preis, der in der Erfassungsposition eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29c82-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="29c82-139">Daher sollte nur ein Benutzer, der sich der Auswirkungen der tatsächlichen Buchhaltung auf das Projekt voll bewusst ist, Eintragserfassungen verwenden, um tatsächliche Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="29c82-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="29c82-140">Aufgrund der Auswirkungen dieses Erfassungstyps sollten Sie sorgfältig auswählen, wer Zugriff zum Erstellen von Eintragserfassungen hat.</span><span class="sxs-lookup"><span data-stu-id="29c82-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="29c82-141">Ist-Werte basierend auf Projektereignissen erfassen</span><span class="sxs-lookup"><span data-stu-id="29c82-141">Record actuals based on project events</span></span>

<span data-ttu-id="29c82-142">Project Operations erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="29c82-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="29c82-143">Diese Transaktionen werden als Ist-Werte aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="29c82-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="29c82-144">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="29c82-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="29c82-145">Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts</span><span class="sxs-lookup"><span data-stu-id="29c82-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29c82-146">Ereignis</span><span class="sxs-lookup"><span data-stu-id="29c82-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29c82-147">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="29c82-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29c82-148">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="29c82-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29c82-149">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="29c82-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29c82-150">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="29c82-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29c82-151">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29c82-152">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="29c82-152">Actuals</span></span></th>
<th><span data-ttu-id="29c82-153">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="29c82-153">Transaction currency</span></span></th>
<th><span data-ttu-id="29c82-154">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-154">Fixed price</span></span></th>
<th><span data-ttu-id="29c82-155">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="29c82-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29c82-156">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="29c82-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29c82-157">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="29c82-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-158">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="29c82-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29c82-159">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="29c82-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29c82-160">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29c82-161">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-161">Cost actual</span></span></td>
<td><span data-ttu-id="29c82-162">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-163">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-164">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="29c82-165">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-166">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-167">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="29c82-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29c82-168">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29c82-169">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29c82-170">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-170">Cost actual</span></span></td>
<td><span data-ttu-id="29c82-171">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-172">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-173">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-174">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-175">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-176">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-177">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-178">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-179">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29c82-180">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29c82-181">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29c82-182">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-183">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="29c82-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-184">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-185">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-187">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="29c82-187">Billed sales</span></span></td>
<td><span data-ttu-id="29c82-188">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29c82-189">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29c82-190">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29c82-191">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-192">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-193">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-194">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-195">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-196">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-197">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-198">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-199">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29c82-200">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="29c82-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29c82-201">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29c82-202">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29c82-203">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="29c82-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29c82-204">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="29c82-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29c82-205">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-206">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-207">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-208">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="29c82-208">Billed sales</span></span></td>
<td><span data-ttu-id="29c82-209">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29c82-210">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="29c82-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29c82-211">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29c82-212">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-213">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-214">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-215">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-216">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="29c82-217">Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet</span><span class="sxs-lookup"><span data-stu-id="29c82-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="29c82-218">Ereignis</span><span class="sxs-lookup"><span data-stu-id="29c82-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="29c82-219">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="29c82-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="29c82-220">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="29c82-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="29c82-221">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="29c82-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="29c82-222">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="29c82-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="29c82-223">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="29c82-224">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="29c82-224">Actuals</span></span></th>
<th><span data-ttu-id="29c82-225">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="29c82-225">Transaction currency</span></span></th>
<th><span data-ttu-id="29c82-226">Festpreis</span><span class="sxs-lookup"><span data-stu-id="29c82-226">Fixed price</span></span></th>
<th><span data-ttu-id="29c82-227">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="29c82-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="29c82-228">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="29c82-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="29c82-229">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="29c82-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-230">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="29c82-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="29c82-231">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="29c82-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="29c82-232">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29c82-233">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-233">Cost actual</span></span></td>
<td><span data-ttu-id="29c82-234">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29c82-235">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29c82-236">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="29c82-237">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="29c82-238">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-239">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="29c82-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="29c82-240">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-241">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29c82-242">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-243">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="29c82-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29c82-244">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="29c82-245">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="29c82-246">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-246">Cost actual</span></span></td>
<td><span data-ttu-id="29c82-247">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-248">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-249">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-250">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-251">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="29c82-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-252">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="29c82-253">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-254">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="29c82-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="29c82-255">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="29c82-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-256">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-257">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-258">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-259">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29c82-260">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29c82-261">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29c82-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-263">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="29c82-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-264">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-265">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="29c82-266">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-267">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="29c82-267">Billed sales</span></span></td>
<td><span data-ttu-id="29c82-268">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29c82-269">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="29c82-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="29c82-270">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="29c82-271">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-272">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-273">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-274">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="29c82-275">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-276">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-277">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-278">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-279">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="29c82-280">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="29c82-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29c82-281">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29c82-282">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="29c82-283">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="29c82-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="29c82-284">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="29c82-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="29c82-285">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-286">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="29c82-287">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="29c82-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-288">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="29c82-288">Billed sales</span></span></td>
<td><span data-ttu-id="29c82-289">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="29c82-290">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="29c82-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="29c82-291">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="29c82-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="29c82-292">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-293">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="29c82-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="29c82-294">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="29c82-295">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="29c82-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="29c82-296">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="29c82-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
