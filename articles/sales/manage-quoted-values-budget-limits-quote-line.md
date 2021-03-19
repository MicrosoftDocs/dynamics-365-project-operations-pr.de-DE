---
title: Projektbasierte Angebotspositionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277787"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="e5385-103">Projektbasierte Angebotspositionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="e5385-103">Project-based quote lines overview</span></span>

<span data-ttu-id="e5385-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="e5385-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e5385-105">Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="e5385-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e5385-106">Die Struktur einer projektbasierten Angebotsposition wird für Projektschätzungen um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="e5385-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e5385-107">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="e5385-107">Billing Method</span></span>
- <span data-ttu-id="e5385-108">Projektzuordnung</span><span class="sxs-lookup"><span data-stu-id="e5385-108">Project Mapping</span></span>
- <span data-ttu-id="e5385-109">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="e5385-109">Included Transaction classes</span></span>
- <span data-ttu-id="e5385-110">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="e5385-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e5385-111">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="e5385-111">Chargeability setup</span></span>
- <span data-ttu-id="e5385-112">Schätzung unter Verwendung von Angebotspositionsdetails</span><span class="sxs-lookup"><span data-stu-id="e5385-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e5385-113">Angebotszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="e5385-113">Quote line Customers</span></span>

<span data-ttu-id="e5385-114">Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile.</span><span class="sxs-lookup"><span data-stu-id="e5385-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e5385-115">Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.</span><span class="sxs-lookup"><span data-stu-id="e5385-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e5385-116">**Feld**</span><span class="sxs-lookup"><span data-stu-id="e5385-116">**Field**</span></span> | <span data-ttu-id="e5385-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5385-117">**Description**</span></span> | <span data-ttu-id="e5385-118">**Downstream-Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="e5385-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e5385-119">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="e5385-119">Name</span></span> | <span data-ttu-id="e5385-120">Der Name der Angebotsposition, mit dessen Hilfe Sie die einzelne Komponente des Angebots identifizieren können, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e5385-121">Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-122">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="e5385-122">Billing Method</span></span> | <span data-ttu-id="e5385-123">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5385-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e5385-124">Dieses Feld enthält die beiden Haupt-Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="e5385-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e5385-125">- Festpreis</span><span class="sxs-lookup"><span data-stu-id="e5385-125">- Fixed price</span></span></br><span data-ttu-id="e5385-126">- Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="e5385-126">- Time and material.</span></span>| <span data-ttu-id="e5385-127">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-128">Project</span><span class="sxs-lookup"><span data-stu-id="e5385-128">Project</span></span> | <span data-ttu-id="e5385-129">Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e5385-130">Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails.</span><span class="sxs-lookup"><span data-stu-id="e5385-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e5385-131">Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e5385-132">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-133">Zeit einschließen</span><span class="sxs-lookup"><span data-stu-id="e5385-133">Include Time</span></span> | <span data-ttu-id="e5385-134">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e5385-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-135">Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-136">Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e5385-137">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-138">Ausgaben einschließen</span><span class="sxs-lookup"><span data-stu-id="e5385-138">Include Expense</span></span> | <span data-ttu-id="e5385-139">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Ausgaben für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e5385-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-140">Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-141">Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e5385-142">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-143">Gebühr einschließen</span><span class="sxs-lookup"><span data-stu-id="e5385-143">Include Fee</span></span> | <span data-ttu-id="e5385-144">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e5385-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-145">Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e5385-146">Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="e5385-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e5385-147">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-148">Angebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="e5385-148">Quoted Amount</span></span> | <span data-ttu-id="e5385-149">Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotsposition prognostizierten Arbeiten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e5385-150">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5385-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e5385-151">Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e5385-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e5385-152">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-153">Geschätzte Steuer</span><span class="sxs-lookup"><span data-stu-id="e5385-153">Estimated Tax</span></span> | <span data-ttu-id="e5385-154">Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="e5385-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e5385-155">Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e5385-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e5385-156">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-157">Nettoangebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="e5385-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="e5385-158">Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e5385-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e5385-159">Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet.</span><span class="sxs-lookup"><span data-stu-id="e5385-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e5385-160">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-161">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="e5385-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="e5385-162">Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e5385-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e5385-163">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e5385-164">Kundenbudget</span><span class="sxs-lookup"><span data-stu-id="e5385-164">Customer Budget</span></span> | <span data-ttu-id="e5385-165">Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5385-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e5385-166">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="e5385-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e5385-167">Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen</span><span class="sxs-lookup"><span data-stu-id="e5385-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e5385-168">**Regel 1**: Eine bestimmte Transaktionsklasse für das ausgewählte Projekt kann nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="e5385-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e5385-169">**Regel 2**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e5385-170">**Regel 3**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="e5385-171">
                    <strong>Verkaufschance</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e5385-172">
                    <strong>Angebot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e5385-173">
                    <strong>Angebotsposition</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e5385-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e5385-175">
                    <strong>Zeit einbeziehen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e5385-176">
                    <strong>Ausgabe einbeziehen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e5385-177">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e5385-178">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="e5385-179">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="e5385-180">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e5385-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-181">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-182">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-183">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-184">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-185">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-186">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-187">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-188">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-189">Verstoß gegen Regel 1</span><span class="sxs-lookup"><span data-stu-id="e5385-189">Violation of Rule #1.</span></span> <span data-ttu-id="e5385-190">Zeit, Kosten und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-191">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-192">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-193">QL2</span><span class="sxs-lookup"><span data-stu-id="e5385-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-194">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-195">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-196">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-197">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-197">Yes</span></span> </p>
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
<span data-ttu-id="e5385-198">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-199">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-200">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-201">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-202">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-203">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5385-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-204">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-205">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-206">Verstoß gegen Regel 1</span><span class="sxs-lookup"><span data-stu-id="e5385-206">Violation of Rule #1.</span></span> <span data-ttu-id="e5385-207">Zeit und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-208">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-209">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-210">QL2</span><span class="sxs-lookup"><span data-stu-id="e5385-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-211">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-212">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-213">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-214">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-214">Yes</span></span> </p>
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
<span data-ttu-id="e5385-215">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-216">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-217">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-218">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-219">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-220">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5385-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-221">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-222">Gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="e5385-223">Zeit und Gebühren für das P1-Projekt sind in QL1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="e5385-224">Die Kosten für das P1-Projekt sind in QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5385-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="e5385-225">Es gibt keine Überlappung in dem, was in jeder Angebotsposition enthalten ist, sodass es gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e5385-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-226">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-227">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-228">QL2</span><span class="sxs-lookup"><span data-stu-id="e5385-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-229">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-230">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5385-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-231">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="e5385-232">No</span></span> </p>
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
<span data-ttu-id="e5385-233">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-234">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-235">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-236">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-237">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-238">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-239">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-240">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-241">Verstoß gegen Regel 1 oben</span><span class="sxs-lookup"><span data-stu-id="e5385-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="e5385-242">Q1 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="e5385-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e5385-243">QL2 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1 und überschneidet sich mit dem, was in Q1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e5385-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-244">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-245">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-246">QL2</span><span class="sxs-lookup"><span data-stu-id="e5385-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-247">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-248">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-249">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-250">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-250">Yes</span></span> </p>
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
<span data-ttu-id="e5385-251">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-252">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-253">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-254">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-255">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-256">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-257">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e5385-258">Gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-259">Basierend auf Regel 2 sind Q1 und Q2 zwei Angebote für dieselbe Verkaufschance, sodass beide dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="e5385-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-260">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-261">Q2</span><span class="sxs-lookup"><span data-stu-id="e5385-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-262">QL1 in Q2</span><span class="sxs-lookup"><span data-stu-id="e5385-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-263">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-264">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-265">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-266">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-266">Yes</span></span> </p>
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
<span data-ttu-id="e5385-267">O1</span><span class="sxs-lookup"><span data-stu-id="e5385-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-268">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-269">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-270">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-271">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-272">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-273">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e5385-274">Gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e5385-275">Basierend auf Regel 3 sind Q1 und Q2 zwei Angebote für unterschiedliche Verkaufschancen, sodass sie nicht dieselben Komponenten desselben Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="e5385-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e5385-276">O2</span><span class="sxs-lookup"><span data-stu-id="e5385-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e5385-277">Q1</span><span class="sxs-lookup"><span data-stu-id="e5385-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-278">QL1</span><span class="sxs-lookup"><span data-stu-id="e5385-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-279">P1</span><span class="sxs-lookup"><span data-stu-id="e5385-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-280">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e5385-281">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e5385-282">Ja</span><span class="sxs-lookup"><span data-stu-id="e5385-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e5385-283">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="e5385-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]