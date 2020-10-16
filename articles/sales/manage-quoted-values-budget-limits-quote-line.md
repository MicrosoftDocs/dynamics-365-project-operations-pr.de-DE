---
title: Projektbasierte Angebotspositionen
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906171"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="8c967-103">Projektbasierte Angebotspositionen</span><span class="sxs-lookup"><span data-stu-id="8c967-103">Project-based quote lines</span></span>

<span data-ttu-id="8c967-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="8c967-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8c967-105">Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="8c967-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="8c967-106">Die Struktur einer projektbasierten Angebotsposition wird für Projektschätzungen um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="8c967-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="8c967-107">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="8c967-107">Billing Method</span></span>
- <span data-ttu-id="8c967-108">Projektzuordnung</span><span class="sxs-lookup"><span data-stu-id="8c967-108">Project Mapping</span></span>
- <span data-ttu-id="8c967-109">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="8c967-109">Included Transaction classes</span></span>
- <span data-ttu-id="8c967-110">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="8c967-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="8c967-111">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="8c967-111">Chargeability setup</span></span>
- <span data-ttu-id="8c967-112">Schätzung unter Verwendung von Angebotspositionsdetails</span><span class="sxs-lookup"><span data-stu-id="8c967-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="8c967-113">Angebotszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="8c967-113">Quote line Customers</span></span>

<span data-ttu-id="8c967-114">Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile.</span><span class="sxs-lookup"><span data-stu-id="8c967-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="8c967-115">Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.</span><span class="sxs-lookup"><span data-stu-id="8c967-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="8c967-116">**Feld**</span><span class="sxs-lookup"><span data-stu-id="8c967-116">**Field**</span></span> | <span data-ttu-id="8c967-117">**Relevanz, Zweck und Anleitung**</span><span class="sxs-lookup"><span data-stu-id="8c967-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="8c967-118">**Downstream-Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="8c967-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8c967-119">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="8c967-119">Name</span></span> | <span data-ttu-id="8c967-120">Der Name der Angebotsposition, mit dessen Hilfe Sie die einzelne Komponente des Angebots identifizieren können, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="8c967-121">Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-122">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="8c967-122">Billing Method</span></span> | <span data-ttu-id="8c967-123">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="8c967-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="8c967-124">Dieses Feld enthält die beiden wichtigsten Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="8c967-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="8c967-125">- Festpreis</span><span class="sxs-lookup"><span data-stu-id="8c967-125">- Fixed price</span></span></br><span data-ttu-id="8c967-126">- Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="8c967-126">- Time and material.</span></span>| <span data-ttu-id="8c967-127">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-128">Project</span><span class="sxs-lookup"><span data-stu-id="8c967-128">Project</span></span> | <span data-ttu-id="8c967-129">Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="8c967-130">Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails.</span><span class="sxs-lookup"><span data-stu-id="8c967-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="8c967-131">Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="8c967-132">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-133">Zeit einschließen</span><span class="sxs-lookup"><span data-stu-id="8c967-133">Include Time</span></span> | <span data-ttu-id="8c967-134">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="8c967-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-135">Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-136">Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8c967-137">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-138">Ausgaben einschließen</span><span class="sxs-lookup"><span data-stu-id="8c967-138">Include Expense</span></span> | <span data-ttu-id="8c967-139">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Ausgaben für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="8c967-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-140">Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-141">Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8c967-142">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-143">Gebühr einschließen</span><span class="sxs-lookup"><span data-stu-id="8c967-143">Include Fee</span></span> | <span data-ttu-id="8c967-144">Die Kennzeichnung **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="8c967-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-145">Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="8c967-146">Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="8c967-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="8c967-147">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-148">Angebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="8c967-148">Quoted Amount</span></span> | <span data-ttu-id="8c967-149">Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotsposition prognostizierten Arbeiten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="8c967-150">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="8c967-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="8c967-151">Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="8c967-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="8c967-152">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-153">Geschätzte Steuer</span><span class="sxs-lookup"><span data-stu-id="8c967-153">Estimated Tax</span></span> | <span data-ttu-id="8c967-154">Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="8c967-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="8c967-155">Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="8c967-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="8c967-156">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-157">Nettoangebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="8c967-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="8c967-158">Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8c967-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="8c967-159">Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet.</span><span class="sxs-lookup"><span data-stu-id="8c967-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="8c967-160">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-161">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="8c967-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="8c967-162">Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c967-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="8c967-163">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="8c967-164">Kundenbudget</span><span class="sxs-lookup"><span data-stu-id="8c967-164">Customer Budget</span></span> | <span data-ttu-id="8c967-165">Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8c967-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="8c967-166">Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="8c967-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="8c967-167">Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen</span><span class="sxs-lookup"><span data-stu-id="8c967-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="8c967-168">**Regel 1**: Eine bestimmte Transaktionsklasse für das ausgewählte Projekt kann nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="8c967-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="8c967-169">**Regel 2**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="8c967-170">**Regel 3**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="8c967-171">
                    <strong>Verkaufschance</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="8c967-172">
                    <strong>Angebot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8c967-173">
                    <strong>Angebotsposition</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8c967-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8c967-175">
                    <strong>Zeit einbeziehen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8c967-176">
                    <strong>Ausgabe einbeziehen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8c967-177">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="8c967-178">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="8c967-179">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="8c967-180">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8c967-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-181">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-182">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-183">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-184">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-185">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-186">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-187">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-188">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-189">Verstoß gegen Regel 1</span><span class="sxs-lookup"><span data-stu-id="8c967-189">Violation of Rule #1.</span></span> <span data-ttu-id="8c967-190">Zeit, Kosten und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-191">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-192">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-193">QL2</span><span class="sxs-lookup"><span data-stu-id="8c967-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-194">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-195">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-196">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-197">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-197">Yes</span></span> </p>
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
<span data-ttu-id="8c967-198">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-199">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-200">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-201">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-202">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-203">Nr.</span><span class="sxs-lookup"><span data-stu-id="8c967-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-204">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-205">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-206">Verstoß gegen Regel 1</span><span class="sxs-lookup"><span data-stu-id="8c967-206">Violation of Rule #1.</span></span> <span data-ttu-id="8c967-207">Zeit und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-208">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-209">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-210">QL2</span><span class="sxs-lookup"><span data-stu-id="8c967-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-211">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-212">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-213">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-214">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-214">Yes</span></span> </p>
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
<span data-ttu-id="8c967-215">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-216">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-217">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-218">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-219">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-220">Nr.</span><span class="sxs-lookup"><span data-stu-id="8c967-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-221">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-222">Gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="8c967-223">Zeit und Gebühren für das P1-Projekt sind in QL1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="8c967-224">Die Kosten für das P1-Projekt sind in QL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c967-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="8c967-225">Es gibt keine Überlappung in dem, was in jeder Angebotsposition enthalten ist, sodass es gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8c967-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-226">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-227">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-228">QL2</span><span class="sxs-lookup"><span data-stu-id="8c967-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-229">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-230">Nr.</span><span class="sxs-lookup"><span data-stu-id="8c967-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-231">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="8c967-232">No</span></span> </p>
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
<span data-ttu-id="8c967-233">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-234">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-235">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-236">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-237">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-238">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-239">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-240">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-241">Verstoß gegen Regel 1 oben</span><span class="sxs-lookup"><span data-stu-id="8c967-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="8c967-242">Q1 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="8c967-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8c967-243">QL2 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1 und überschneidet sich mit dem, was in Q1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8c967-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-244">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-245">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-246">QL2</span><span class="sxs-lookup"><span data-stu-id="8c967-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-247">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-248">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-249">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-250">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-250">Yes</span></span> </p>
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
<span data-ttu-id="8c967-251">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-252">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-253">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-254">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-255">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-256">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-257">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8c967-258">Gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-259">Basierend auf Regel 2 sind Q1 und Q2 zwei Angebote für dieselbe Verkaufschance, sodass beide dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="8c967-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-260">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-261">Q2</span><span class="sxs-lookup"><span data-stu-id="8c967-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-262">QL1 in Q2</span><span class="sxs-lookup"><span data-stu-id="8c967-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-263">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-264">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-265">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-266">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-266">Yes</span></span> </p>
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
<span data-ttu-id="8c967-267">O1</span><span class="sxs-lookup"><span data-stu-id="8c967-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-268">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-269">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-270">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-271">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-272">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-273">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8c967-274">Gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8c967-275">Basierend auf Regel 3 sind Q1 und Q2 zwei Angebote für unterschiedliche Verkaufschancen, sodass sie nicht dieselben Komponenten desselben Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="8c967-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="8c967-276">O2</span><span class="sxs-lookup"><span data-stu-id="8c967-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="8c967-277">Q1</span><span class="sxs-lookup"><span data-stu-id="8c967-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-278">QL1</span><span class="sxs-lookup"><span data-stu-id="8c967-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-279">P1</span><span class="sxs-lookup"><span data-stu-id="8c967-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-280">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8c967-281">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8c967-282">Ja</span><span class="sxs-lookup"><span data-stu-id="8c967-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="8c967-283">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="8c967-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

