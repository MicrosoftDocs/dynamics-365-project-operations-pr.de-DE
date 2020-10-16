---
title: Projektbasierte Angebotspositionen (Pro)
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908145"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="ca091-104">Projektbasierte Angebotspositionen (Pro)</span><span class="sxs-lookup"><span data-stu-id="ca091-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="ca091-105">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="ca091-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca091-106">Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="ca091-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="ca091-107">Die Struktur einer projektbasierten Angebotsposition wird für Projektschätzungen um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="ca091-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="ca091-108">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="ca091-108">Billing Method</span></span>
- <span data-ttu-id="ca091-109">Projekt- und Aufgabenzuordnung</span><span class="sxs-lookup"><span data-stu-id="ca091-109">Project and Task Mapping</span></span>
- <span data-ttu-id="ca091-110">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="ca091-110">Included Transaction classes</span></span>
- <span data-ttu-id="ca091-111">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="ca091-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="ca091-112">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="ca091-112">Chargeability setup</span></span>
- <span data-ttu-id="ca091-113">Schätzung unter Verwendung von Angebotspositionsdetails</span><span class="sxs-lookup"><span data-stu-id="ca091-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="ca091-114">Angebotszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="ca091-114">Quote line Customers</span></span>

<span data-ttu-id="ca091-115">Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile.</span><span class="sxs-lookup"><span data-stu-id="ca091-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="ca091-116">Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.</span><span class="sxs-lookup"><span data-stu-id="ca091-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="ca091-117">**Feld**</span><span class="sxs-lookup"><span data-stu-id="ca091-117">**Field**</span></span> | <span data-ttu-id="ca091-118">**Relevanz, Zweck und Anleitung**</span><span class="sxs-lookup"><span data-stu-id="ca091-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="ca091-119">**Downstream-Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="ca091-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ca091-120">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="ca091-120">Name</span></span> | <span data-ttu-id="ca091-121">Der Name der Angebotsposition, mit dessen Hilfe Sie die einzelne Komponente des Angebots identifizieren können, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="ca091-122">Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-123">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="ca091-123">Billing Method</span></span> | <span data-ttu-id="ca091-124">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="ca091-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="ca091-125">Dieses Feld enthält die beiden wichtigsten Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="ca091-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="ca091-126">- Festpreis</span><span class="sxs-lookup"><span data-stu-id="ca091-126">- Fixed price</span></span></br><span data-ttu-id="ca091-127">- Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="ca091-127">- Time and material.</span></span>| <span data-ttu-id="ca091-128">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-129">Project</span><span class="sxs-lookup"><span data-stu-id="ca091-129">Project</span></span> | <span data-ttu-id="ca091-130">Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="ca091-131">Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails.</span><span class="sxs-lookup"><span data-stu-id="ca091-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="ca091-132">Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="ca091-133">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="ca091-134">Eingeschlossene Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-134">Included Tasks</span></span> | <span data-ttu-id="ca091-135">Gibt an, ob diese Angebotsposition für alle oder einige der Projektaufgaben für das ausgewählte Projekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="ca091-136">Dieses Feld weist die möglichen Werte auf:</span><span class="sxs-lookup"><span data-stu-id="ca091-136">This field has the following possible values:</span></span></br><span data-ttu-id="ca091-137">- Alle Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-137">- All project tasks</span></span></br><span data-ttu-id="ca091-138">- Nur ausgewählte Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-138">- Selected project tasks only</span></span></br><span data-ttu-id="ca091-139">Ein leerer Wert in diesem Feld entspricht der Option **Alle Projektaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="ca091-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="ca091-140">Wenn **Nur ausgewählte Projektaufgaben** auf der Projektseite ausgewählt ist, können Sie auf der Registerkarte **Einrichtung der Aufgabenfakturierung** bestimmte Aufgaben auswählen, um sie dieser Angebotsposition zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="ca091-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="ca091-141">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-142">Zeit einschließen</span><span class="sxs-lookup"><span data-stu-id="ca091-142">Include Time</span></span> | <span data-ttu-id="ca091-143">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="ca091-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-144">Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-145">Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ca091-146">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-147">Ausgaben einschließen</span><span class="sxs-lookup"><span data-stu-id="ca091-147">Include Expense</span></span> | <span data-ttu-id="ca091-148">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Ausgaben für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="ca091-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-149">Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-150">Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ca091-151">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-152">Gebühr einschließen</span><span class="sxs-lookup"><span data-stu-id="ca091-152">Include Fee</span></span> | <span data-ttu-id="ca091-153">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="ca091-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-154">Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ca091-155">Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ca091-156">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-157">Angebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="ca091-157">Quoted Amount</span></span> | <span data-ttu-id="ca091-158">Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotsposition prognostizierten Arbeiten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="ca091-159">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="ca091-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="ca091-160">Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ca091-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="ca091-161">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-162">Geschätzte Steuer</span><span class="sxs-lookup"><span data-stu-id="ca091-162">Estimated Tax</span></span> | <span data-ttu-id="ca091-163">Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="ca091-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="ca091-164">Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ca091-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="ca091-165">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-166">Nettoangebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="ca091-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="ca091-167">Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ca091-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="ca091-168">Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet.</span><span class="sxs-lookup"><span data-stu-id="ca091-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="ca091-169">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-170">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="ca091-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="ca091-171">Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca091-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="ca091-172">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ca091-173">Kundenbudget</span><span class="sxs-lookup"><span data-stu-id="ca091-173">Customer Budget</span></span> | <span data-ttu-id="ca091-174">Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca091-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="ca091-175">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="ca091-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="ca091-176">Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen</span><span class="sxs-lookup"><span data-stu-id="ca091-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="ca091-177">**Regel 1**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, ist ein Projekt in der Angebotsposition einbezogen.</span><span class="sxs-lookup"><span data-stu-id="ca091-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="ca091-178">**Regel 2**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ca091-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="ca091-179">**Regel 3**: Wenn das Feld **Eingeschlossene Aufgaben** auf **Nur ausgewählte Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Angebotspositionen eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ca091-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="ca091-180">**Regel 4**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="ca091-181">**Regel 5**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="ca091-182">
                    <strong>Verkaufschance</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="ca091-183">
                    <strong>Angebot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ca091-184">
                    <strong>Angebotsposition</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ca091-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="ca091-186">
                    <strong>Eingeschlossene Aufgaben</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ca091-187">
                    <strong>Zeit einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ca091-188">
                    <strong>Ausgaben einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ca091-189">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ca091-190">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="ca091-191">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="ca091-192">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ca091-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-193">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-194">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-195">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-196">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-197">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-198">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-199">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-200">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-201">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-202">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="ca091-202">Violation of Rule #2.</span></span> <span data-ttu-id="ca091-203">Zeit, Kosten und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-204">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-205">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-206">QL2</span><span class="sxs-lookup"><span data-stu-id="ca091-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-207">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-208">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-209">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-210">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-211">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-212">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-213">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-214">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-215">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-216">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-217">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-218">Nr.</span><span class="sxs-lookup"><span data-stu-id="ca091-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-219">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-220">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-221">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="ca091-221">Violation of Rule #2.</span></span> <span data-ttu-id="ca091-222">Zeit und Gebühren für das P1-Projekt sind in den Angebotszeilen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-223">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-224">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-225">QL2</span><span class="sxs-lookup"><span data-stu-id="ca091-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-226">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-227">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-228">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-229">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-230">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-231">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-232">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-233">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-234">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-235">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-236">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="ca091-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-238">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-239">Gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="ca091-240">Zeit und Gebühren für das P1-Projekt sind in QL1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="ca091-241">Die Kosten für das P1-Projekt sind in QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="ca091-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="ca091-242">Es gibt keine Überlappung in dem, was in jeder Angebotsposition enthalten und gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ca091-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-243">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-244">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-245">QL2</span><span class="sxs-lookup"><span data-stu-id="ca091-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-246">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-247">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-248">Nr.</span><span class="sxs-lookup"><span data-stu-id="ca091-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-249">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-250">Nr.</span><span class="sxs-lookup"><span data-stu-id="ca091-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-251">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-252">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-253">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-254">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-255">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-256">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-257">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-258">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-259">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-260">Verstoß gegen Regel 2 oben</span><span class="sxs-lookup"><span data-stu-id="ca091-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="ca091-261">Q1 enthält Zeit, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="ca091-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ca091-262">QL2 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1 und überschneidet sich mit dem, was in Q1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ca091-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-263">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-264">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-265">QL2</span><span class="sxs-lookup"><span data-stu-id="ca091-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-266">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-267">Blank</span><span class="sxs-lookup"><span data-stu-id="ca091-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-268">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-269">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-270">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-271">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-272">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-273">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-274">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-275">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-276">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-277">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-278">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-279">Gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-280">Gemäß Regel 3 oben</span><span class="sxs-lookup"><span data-stu-id="ca091-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="ca091-281">Q1 enthält Zeit, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="ca091-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ca091-282">QL2 enthält Zeit, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="ca091-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ca091-283">Die einzige zusätzliche Prüfung betrifft die Teilmenge der Aufgaben in QL1, die sich von der Teilmenge der Aufgaben in QL2 unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ca091-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="ca091-284">Dies stellt sicher, dass es keine Überlappungen gibt.</span><span class="sxs-lookup"><span data-stu-id="ca091-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="ca091-285">Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ca091-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-286">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-287">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-288">QL2</span><span class="sxs-lookup"><span data-stu-id="ca091-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-289">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-290">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ca091-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-291">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-292">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-293">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-294">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-295">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-296">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-297">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-298">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="ca091-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-299">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-300">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-301">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ca091-302">Gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-303">Basierend auf Regel 5 sind Q1 und Q2 zwei Angebote für dieselbe Verkaufschance, sodass beide dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="ca091-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-304">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-305">Q2</span><span class="sxs-lookup"><span data-stu-id="ca091-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-306">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-307">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-308">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="ca091-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-309">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-310">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-311">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-312">O1</span><span class="sxs-lookup"><span data-stu-id="ca091-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-313">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-314">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-315">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-316">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="ca091-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-317">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-318">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-319">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ca091-320">Gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ca091-321">Basierend auf Regel 4 sind Q1 und Q2 zwei Angebote für unterschiedliche Verkaufschancen, sodass sie nicht dieselben Komponenten desselben Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="ca091-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ca091-322">O2</span><span class="sxs-lookup"><span data-stu-id="ca091-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ca091-323">Q1</span><span class="sxs-lookup"><span data-stu-id="ca091-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-324">QL1</span><span class="sxs-lookup"><span data-stu-id="ca091-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-325">P1</span><span class="sxs-lookup"><span data-stu-id="ca091-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="ca091-326">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="ca091-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-327">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ca091-328">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ca091-329">Ja</span><span class="sxs-lookup"><span data-stu-id="ca091-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ca091-330">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="ca091-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

