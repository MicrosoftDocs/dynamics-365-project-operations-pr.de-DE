---
title: Tatsächliche Transaktionen
description: Dieses Thema enthält Informationen zum Arbeiten mit Istwerten in Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291798"
---
# <a name="actuals"></a><span data-ttu-id="8c134-103">Tatsächliche Transaktionen</span><span class="sxs-lookup"><span data-stu-id="8c134-103">Actuals</span></span> 

<span data-ttu-id="8c134-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="8c134-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8c134-105">Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde.</span><span class="sxs-lookup"><span data-stu-id="8c134-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="8c134-106">Sie werden als Ergebnis von Zeit- und Kosteneingaben sowie Erfassungseinträgen und Rechnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c134-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="8c134-107">Erfassungspositionen und Zeiteinreichung</span><span class="sxs-lookup"><span data-stu-id="8c134-107">Journal lines and time submission</span></span>

<span data-ttu-id="8c134-108">Weitere Informationen zum Zeiteintrag finden Sie unter [Zeiteintragsübersicht](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c134-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="8c134-109">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="8c134-109">Time and materials</span></span>

<span data-ttu-id="8c134-110">Wenn ein übermittelter Zeiteintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="8c134-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="8c134-111">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-111">Fixed price</span></span>

<span data-ttu-id="8c134-112">Wenn ein eingereichter Zeiteintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.</span><span class="sxs-lookup"><span data-stu-id="8c134-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="8c134-113">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="8c134-113">Default pricing</span></span>

<span data-ttu-id="8c134-114">Die Logik zur Erstellung von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="8c134-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="8c134-115">Die Feldwerte des Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="8c134-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="8c134-116">Diese Werte enthalten das Transaktionsdatum, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="8c134-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="8c134-117">In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8c134-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="8c134-118">Sie können dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8c134-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="8c134-119">Wenn Sie möchten, dass der Feldwert an „Ist-Werte“ weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte“ und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.</span><span class="sxs-lookup"><span data-stu-id="8c134-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="8c134-120">Erfassungspositionen und Einreichung der Grundkosten</span><span class="sxs-lookup"><span data-stu-id="8c134-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="8c134-121">Weitere Informationen zum Ausgabeneintrag finden Sie unter [Ausgabeneintragsübersicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c134-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="8c134-122">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="8c134-122">Time and materials</span></span>

<span data-ttu-id="8c134-123">Wenn ein übermittelter Grundkosteneintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="8c134-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="8c134-124">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-124">Fixed price</span></span>

<span data-ttu-id="8c134-125">Wenn ein eingereichter Grundkosteneintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.</span><span class="sxs-lookup"><span data-stu-id="8c134-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="8c134-126">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="8c134-126">Default pricing</span></span>

<span data-ttu-id="8c134-127">Die Logik zur Eingabe von Standardpreisen für Ausgaben basiert auf der Ausgabenkategorie.</span><span class="sxs-lookup"><span data-stu-id="8c134-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="8c134-128">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c134-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="8c134-129">Für den Preis selbst wird standardmäßig der vom Benutzer eingegebene Betrag jedoch direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8c134-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="8c134-130">Der kategoriebasierte Eintrag von Standardpreisen pro Einheit ist bei Ausgabeneinträgen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c134-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="8c134-131">Eintragserfassungen zur Erfassung von Kosten verwenden</span><span class="sxs-lookup"><span data-stu-id="8c134-131">Use entry journals to record costs</span></span>

<span data-ttu-id="8c134-132">Sie können mithilfe von Erfassungenn die Kosten bzw. den Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="8c134-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="8c134-133">Erfassungen können für die folgenden Zwecke verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="8c134-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="8c134-134">Zeichnen Sie die Ist-Kosten der Materialien und Umsätze bei einem Projekt auf.</span><span class="sxs-lookup"><span data-stu-id="8c134-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="8c134-135">Importieren Sie Transaktions-Istwerte aus einem anderen System nach Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8c134-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="8c134-136">Zeichnen Sie die Kosten auf, die in einem anderen System aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="8c134-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="8c134-137">Diese Kosten können Beschaffungs- oder Fremdarbeitskosten umfassen.</span><span class="sxs-lookup"><span data-stu-id="8c134-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c134-138">Die Anwendung überprüft weder den Erfassungspositionstyp noch den zugehörigen Preis, der in der Erfassungsposition eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c134-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="8c134-139">Daher sollte nur ein Benutzer, der sich der Auswirkungen der tatsächlichen Buchhaltung auf das Projekt voll bewusst ist, Eintragserfassungen verwenden, um tatsächliche Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c134-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="8c134-140">Aufgrund der Auswirkungen dieses Erfassungstyps sollten Sie sorgfältig auswählen, wer Zugriff zum Erstellen von Eintragserfassungen hat.</span><span class="sxs-lookup"><span data-stu-id="8c134-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="8c134-141">Ist-Werte basierend auf Projektereignissen erfassen</span><span class="sxs-lookup"><span data-stu-id="8c134-141">Record actuals based on project events</span></span>

<span data-ttu-id="8c134-142">Project Operations erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="8c134-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="8c134-143">Diese Transaktionen werden als Ist-Werte aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8c134-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="8c134-144">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="8c134-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="8c134-145">Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts</span><span class="sxs-lookup"><span data-stu-id="8c134-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8c134-146">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8c134-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8c134-147">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="8c134-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8c134-148">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="8c134-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8c134-149">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="8c134-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8c134-150">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="8c134-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8c134-151">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8c134-152">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="8c134-152">Actuals</span></span></th>
<th><span data-ttu-id="8c134-153">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="8c134-153">Transaction currency</span></span></th>
<th><span data-ttu-id="8c134-154">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-154">Fixed price</span></span></th>
<th><span data-ttu-id="8c134-155">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="8c134-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8c134-156">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c134-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8c134-157">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="8c134-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-158">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="8c134-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8c134-159">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="8c134-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8c134-160">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8c134-161">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-161">Cost actual</span></span></td>
<td><span data-ttu-id="8c134-162">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-163">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-164">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="8c134-165">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-166">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-167">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="8c134-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8c134-168">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8c134-169">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8c134-170">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-170">Cost actual</span></span></td>
<td><span data-ttu-id="8c134-171">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-172">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-173">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-174">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-175">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-176">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-177">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-178">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-179">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8c134-180">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8c134-181">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8c134-182">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-183">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="8c134-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-184">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-185">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-187">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="8c134-187">Billed sales</span></span></td>
<td><span data-ttu-id="8c134-188">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8c134-189">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8c134-190">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8c134-191">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-192">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-193">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-194">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-195">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-196">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-197">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-198">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-199">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8c134-200">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8c134-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8c134-201">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8c134-202">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8c134-203">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="8c134-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8c134-204">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="8c134-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8c134-205">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-206">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-207">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-208">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="8c134-208">Billed sales</span></span></td>
<td><span data-ttu-id="8c134-209">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8c134-210">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="8c134-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8c134-211">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8c134-212">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-213">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-214">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-215">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-216">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="8c134-217">Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet</span><span class="sxs-lookup"><span data-stu-id="8c134-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8c134-218">Ereignis</span><span class="sxs-lookup"><span data-stu-id="8c134-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8c134-219">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="8c134-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8c134-220">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="8c134-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8c134-221">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="8c134-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8c134-222">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="8c134-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8c134-223">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8c134-224">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="8c134-224">Actuals</span></span></th>
<th><span data-ttu-id="8c134-225">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="8c134-225">Transaction currency</span></span></th>
<th><span data-ttu-id="8c134-226">Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c134-226">Fixed price</span></span></th>
<th><span data-ttu-id="8c134-227">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="8c134-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8c134-228">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="8c134-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8c134-229">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="8c134-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-230">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="8c134-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8c134-231">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="8c134-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8c134-232">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8c134-233">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-233">Cost actual</span></span></td>
<td><span data-ttu-id="8c134-234">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8c134-235">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8c134-236">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8c134-237">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8c134-238">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-239">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="8c134-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8c134-240">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-241">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8c134-242">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-243">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="8c134-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8c134-244">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8c134-245">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8c134-246">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-246">Cost actual</span></span></td>
<td><span data-ttu-id="8c134-247">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-248">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-249">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-250">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-251">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="8c134-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-252">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8c134-253">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-254">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="8c134-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8c134-255">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="8c134-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-256">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-257">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-258">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-259">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8c134-260">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8c134-261">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8c134-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-263">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="8c134-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-264">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-265">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8c134-266">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-267">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="8c134-267">Billed sales</span></span></td>
<td><span data-ttu-id="8c134-268">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8c134-269">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8c134-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8c134-270">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8c134-271">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-272">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-273">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-274">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8c134-275">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-276">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-277">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-278">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-279">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8c134-280">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8c134-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8c134-281">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8c134-282">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8c134-283">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="8c134-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8c134-284">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="8c134-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8c134-285">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-286">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8c134-287">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="8c134-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-288">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="8c134-288">Billed sales</span></span></td>
<td><span data-ttu-id="8c134-289">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8c134-290">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="8c134-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8c134-291">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="8c134-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8c134-292">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-293">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="8c134-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8c134-294">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8c134-295">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="8c134-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8c134-296">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="8c134-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]