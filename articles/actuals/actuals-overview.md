---
title: Tatsächliche Transaktionen
description: Dieses Thema enthält Informationen zum Arbeiten mit Istwerten in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368610"
---
# <a name="actuals"></a><span data-ttu-id="237d2-103">Tatsächliche Transaktionen</span><span class="sxs-lookup"><span data-stu-id="237d2-103">Actuals</span></span> 

<span data-ttu-id="237d2-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="237d2-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="237d2-105">Die tatsächlichen Werte repräsentieren den überprüften und genehmigten finanziellen und geplanten Fortschritt eines Projekts.</span><span class="sxs-lookup"><span data-stu-id="237d2-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="237d2-106">Sie werden als Ergebnis der Genehmigung von Zeit-, Kosten-, Materialverbrauchseinträgen sowie Journaleinträgen und Rechnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="237d2-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="237d2-107">Erfassungspositionen und Zeiteinreichung</span><span class="sxs-lookup"><span data-stu-id="237d2-107">Journal lines and time submission</span></span>

<span data-ttu-id="237d2-108">Weitere Informationen zum Zeiteintrag finden Sie unter [Zeiteintragsübersicht](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="237d2-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="237d2-109">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="237d2-109">Time and materials</span></span>

<span data-ttu-id="237d2-110">Wenn ein übermittelter Zeiteintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="237d2-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="237d2-111">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-111">Fixed price</span></span>

<span data-ttu-id="237d2-112">Wenn ein eingereichter Zeiteintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.</span><span class="sxs-lookup"><span data-stu-id="237d2-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="237d2-113">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="237d2-113">Default pricing</span></span>

<span data-ttu-id="237d2-114">Die Logik zur Erstellung von Standardpreisen befindet sich in der Journalposition.</span><span class="sxs-lookup"><span data-stu-id="237d2-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="237d2-115">Die Feldwerte des Zeiteintrags werden in die Erfassungsposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="237d2-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="237d2-116">Diese Werte enthalten das Transaktionsdatum, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.</span><span class="sxs-lookup"><span data-stu-id="237d2-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="237d2-117">Die Felder, die sich auf die Standardpreise wie etwa **Rolle** und **Ressourceneinheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen.</span><span class="sxs-lookup"><span data-stu-id="237d2-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="237d2-118">Sie können dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="237d2-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="237d2-119">Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**.</span><span class="sxs-lookup"><span data-stu-id="237d2-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="237d2-120">Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="237d2-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="237d2-121">Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="237d2-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="237d2-122">Erfassungspositionen und Einreichung der Grundkosten</span><span class="sxs-lookup"><span data-stu-id="237d2-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="237d2-123">Weitere Informationen zum Ausgabeneintrag finden Sie unter [Ausgabeneintragsübersicht](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="237d2-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="237d2-124">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="237d2-124">Time and materials</span></span>

<span data-ttu-id="237d2-125">Wenn ein übermittelter Grundkosteneintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="237d2-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="237d2-126">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-126">Fixed price</span></span>

<span data-ttu-id="237d2-127">Wenn ein übertragener Basisausgabeneintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Journalzeile für Kosten.</span><span class="sxs-lookup"><span data-stu-id="237d2-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="237d2-128">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="237d2-128">Default pricing</span></span>

<span data-ttu-id="237d2-129">Die Logik zur Eingabe von Standardpreisen für Ausgaben basiert auf der Ausgabenkategorie.</span><span class="sxs-lookup"><span data-stu-id="237d2-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="237d2-130">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="237d2-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="237d2-131">Die Felder, die sich auf die Standardpreise wie etwa **Transaktionskategorie** und **Einheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen.</span><span class="sxs-lookup"><span data-stu-id="237d2-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="237d2-132">Dies funktioniert jedoch nur, wenn die Preismethode in der Preisliste **Preis pro Einheit** lautet.</span><span class="sxs-lookup"><span data-stu-id="237d2-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="237d2-133">Wenn die Preismethode **Zum Einstandswert** oder **Aufschlag auf Kosten** lautet, wird der bei der Erstellung der Spesenbuchung eingegebene Preis für die Kosten verwendet und der Preis in der Verkaufsjournalzeile wird anhand der Preismethode berechnet.</span><span class="sxs-lookup"><span data-stu-id="237d2-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="237d2-134">Sie können der Spesenbuchung ein benutzerdefiniertes Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="237d2-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="237d2-135">Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**.</span><span class="sxs-lookup"><span data-stu-id="237d2-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="237d2-136">Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="237d2-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="237d2-137">Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="237d2-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="237d2-138">Übermittlung von Journalzeilen und Materialverwendungsprotokollen</span><span class="sxs-lookup"><span data-stu-id="237d2-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="237d2-139">Weitere Informationen zur Kostenerfassung finden Sie unter [Materialverbrauchsprotokoll](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="237d2-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="237d2-140">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="237d2-140">Time and materials</span></span>

<span data-ttu-id="237d2-141">Wenn ein übermittelter Materialverwendungsprotokolleintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Journalzeilen, eine für Kosten und eine für nicht abgerechnete Verkäufe.</span><span class="sxs-lookup"><span data-stu-id="237d2-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="237d2-142">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-142">Fixed price</span></span>

<span data-ttu-id="237d2-143">Wenn ein übertragenes Materialverbrauchsprotokoll mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Journalzeile für Kosten.</span><span class="sxs-lookup"><span data-stu-id="237d2-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="237d2-144">Standardpreise</span><span class="sxs-lookup"><span data-stu-id="237d2-144">Default pricing</span></span>

<span data-ttu-id="237d2-145">Die Logik zur Eingabe von Standardpreisen für Material basiert auf der Produkt- und Einheitenkombination.</span><span class="sxs-lookup"><span data-stu-id="237d2-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="237d2-146">Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="237d2-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="237d2-147">Die Felder, die sich auf die Standardpreise wie etwa **Produkt-ID** und **Einheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen.</span><span class="sxs-lookup"><span data-stu-id="237d2-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="237d2-148">Dies funktioniert jedoch nur für Katalogprodukte.</span><span class="sxs-lookup"><span data-stu-id="237d2-148">However, this only works for catalog products.</span></span> <span data-ttu-id="237d2-149">Bei manuell einzutragenden Produkten wird der Preis, der bei der Erstellung des Materialverbrauchsprotokolleintrags eingegeben wurde, für Kosten und Verkaufspreis in den Journalzeilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="237d2-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="237d2-150">Sie können dem **Materialverbrauchsprotokoll** ein benutzerdefiniertes Feld hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="237d2-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="237d2-151">Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**.</span><span class="sxs-lookup"><span data-stu-id="237d2-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="237d2-152">Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="237d2-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="237d2-153">Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="237d2-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="237d2-154">Eintragserfassungen zur Erfassung von Kosten verwenden</span><span class="sxs-lookup"><span data-stu-id="237d2-154">Use entry journals to record costs</span></span>

<span data-ttu-id="237d2-155">Sie können mithilfe von Erfassungenn die Kosten bzw. den Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen.</span><span class="sxs-lookup"><span data-stu-id="237d2-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="237d2-156">Erfassungen können für die folgenden Zwecke verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="237d2-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="237d2-157">Importieren Sie Transaktions-Istwerte aus einem anderen System nach Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="237d2-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="237d2-158">Zeichnen Sie die Kosten auf, die in einem anderen System aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="237d2-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="237d2-159">Diese Kosten können Beschaffungs- oder Fremdarbeitskosten umfassen.</span><span class="sxs-lookup"><span data-stu-id="237d2-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="237d2-160">Die Anwendung überprüft weder den Erfassungspositionstyp noch den zugehörigen Preis, der in der Erfassungsposition eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="237d2-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="237d2-161">Daher sollte nur ein Benutzer, der sich der Auswirkungen der tatsächlichen Buchhaltung auf das Projekt voll bewusst ist, Eintragserfassungen verwenden, um tatsächliche Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="237d2-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="237d2-162">Aufgrund der Auswirkungen dieses Erfassungstyps sollten Sie sorgfältig auswählen, wer Zugriff zum Erstellen von Eintragserfassungen hat.</span><span class="sxs-lookup"><span data-stu-id="237d2-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="237d2-163">Ist-Werte basierend auf Projektereignissen erfassen</span><span class="sxs-lookup"><span data-stu-id="237d2-163">Record actuals based on project events</span></span>

<span data-ttu-id="237d2-164">Project Operations erfasst die Finanztransaktionen, die während eines Projekts stattfinden.</span><span class="sxs-lookup"><span data-stu-id="237d2-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="237d2-165">Diese Transaktionen werden als Ist-Werte aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="237d2-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="237d2-166">Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.</span><span class="sxs-lookup"><span data-stu-id="237d2-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="237d2-167">Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts</span><span class="sxs-lookup"><span data-stu-id="237d2-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="237d2-168">Ereignis</span><span class="sxs-lookup"><span data-stu-id="237d2-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="237d2-169">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="237d2-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="237d2-170">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="237d2-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="237d2-171">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="237d2-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="237d2-172">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="237d2-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="237d2-173">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="237d2-174">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="237d2-174">Actuals</span></span></th>
<th><span data-ttu-id="237d2-175">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="237d2-175">Transaction currency</span></span></th>
<th><span data-ttu-id="237d2-176">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-176">Fixed price</span></span></th>
<th><span data-ttu-id="237d2-177">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="237d2-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="237d2-178">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="237d2-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="237d2-179">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="237d2-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-180">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="237d2-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="237d2-181">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="237d2-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="237d2-182">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="237d2-183">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-183">Cost actual</span></span></td>
<td><span data-ttu-id="237d2-184">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-185">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-186">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="237d2-187">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-188">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-189">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="237d2-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="237d2-190">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="237d2-191">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="237d2-192">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-192">Cost actual</span></span></td>
<td><span data-ttu-id="237d2-193">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-194">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-195">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-196">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-197">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-198">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-199">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-200">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-201">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="237d2-202">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="237d2-203">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="237d2-204">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-205">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="237d2-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-206">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-207">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-208">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-209">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="237d2-209">Billed sales</span></span></td>
<td><span data-ttu-id="237d2-210">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="237d2-211">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="237d2-212">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="237d2-213">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-214">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-215">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-216">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-217">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-218">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-219">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-220">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-221">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="237d2-222">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="237d2-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="237d2-223">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="237d2-224">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="237d2-225">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="237d2-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="237d2-226">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="237d2-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="237d2-227">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-228">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-229">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-230">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="237d2-230">Billed sales</span></span></td>
<td><span data-ttu-id="237d2-231">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="237d2-232">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="237d2-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="237d2-233">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="237d2-234">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-235">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-236">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-237">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-238">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="237d2-239">Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet</span><span class="sxs-lookup"><span data-stu-id="237d2-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="237d2-240">Ereignis</span><span class="sxs-lookup"><span data-stu-id="237d2-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="237d2-241">Abrechenbares oder verkauftes Projekt</span><span class="sxs-lookup"><span data-stu-id="237d2-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="237d2-242">Projekt in der Vorverkaufsphase</span><span class="sxs-lookup"><span data-stu-id="237d2-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="237d2-243">Internes Projekt</span><span class="sxs-lookup"><span data-stu-id="237d2-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="237d2-244">Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="237d2-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="237d2-245">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="237d2-246">Ist-Werte</span><span class="sxs-lookup"><span data-stu-id="237d2-246">Actuals</span></span></th>
<th><span data-ttu-id="237d2-247">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="237d2-247">Transaction currency</span></span></th>
<th><span data-ttu-id="237d2-248">Festpreis</span><span class="sxs-lookup"><span data-stu-id="237d2-248">Fixed price</span></span></th>
<th><span data-ttu-id="237d2-249">Transaktionswährung</span><span class="sxs-lookup"><span data-stu-id="237d2-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="237d2-250">Ein Zeiteintrag wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="237d2-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="237d2-251">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="237d2-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-252">Ein Zeiteintrag wird übermittelt.</span><span class="sxs-lookup"><span data-stu-id="237d2-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="237d2-253">Keine Aktivität in der Entität „Ist-Werte”</span><span class="sxs-lookup"><span data-stu-id="237d2-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="237d2-254">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="237d2-255">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-255">Cost actual</span></span></td>
<td><span data-ttu-id="237d2-256">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="237d2-257">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="237d2-258">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="237d2-259">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="237d2-260">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-261">Nicht fakturierter Umsatz-Istwert – Fakturierbar</span><span class="sxs-lookup"><span data-stu-id="237d2-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="237d2-262">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-263">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="237d2-264">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-265">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="237d2-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="237d2-266">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="237d2-267">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="237d2-268">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-268">Cost actual</span></span></td>
<td><span data-ttu-id="237d2-269">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-270">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-271">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-272">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-273">Kosten-Istwert</span><span class="sxs-lookup"><span data-stu-id="237d2-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-274">Kosten der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="237d2-275">Währung der Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-276">Organisationsübergreifender Umsatz</span><span class="sxs-lookup"><span data-stu-id="237d2-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="237d2-277">Währung der Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="237d2-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-278">Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-279">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-280">Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-281">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="237d2-282">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="237d2-283">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="237d2-284">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-285">Abgerechnete Umsätze für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="237d2-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-286">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-287">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="237d2-288">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-289">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="237d2-289">Billed sales</span></span></td>
<td><span data-ttu-id="237d2-290">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="237d2-291">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</span><span class="sxs-lookup"><span data-stu-id="237d2-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="237d2-292">Nicht fakturierte Umsatzumkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="237d2-293">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-294">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-295">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-296">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="237d2-297">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-298">Abgerechneter Umsatz – Fakturierbar für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-299">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-300">Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-301">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="237d2-302">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="237d2-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="237d2-303">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="237d2-304">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="237d2-305">Abgerechnete Umsatzumkehrung für Meilenstein</span><span class="sxs-lookup"><span data-stu-id="237d2-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="237d2-306">Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></span><span class="sxs-lookup"><span data-stu-id="237d2-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="237d2-307">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-308">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="237d2-309">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="237d2-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-310">Fakturierte Umsätze</span><span class="sxs-lookup"><span data-stu-id="237d2-310">Billed sales</span></span></td>
<td><span data-ttu-id="237d2-311">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="237d2-312">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</span><span class="sxs-lookup"><span data-stu-id="237d2-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="237d2-313">Abgerechneter Umsatz – Umkehrung</span><span class="sxs-lookup"><span data-stu-id="237d2-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="237d2-314">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-315">Abgerechneter Umsatz für die neue Menge</span><span class="sxs-lookup"><span data-stu-id="237d2-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="237d2-316">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="237d2-317">Nicht fakturierte Umsätze – Fakturierbar für die Differenz</span><span class="sxs-lookup"><span data-stu-id="237d2-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="237d2-318">Währung des Projektvertrags</span><span class="sxs-lookup"><span data-stu-id="237d2-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
