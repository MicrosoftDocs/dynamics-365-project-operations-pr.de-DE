---
title: Projektbasierte Angebotspositionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369870"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="a8447-103">Projektbasierte Angebotspositionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a8447-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="a8447-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_</span><span class="sxs-lookup"><span data-stu-id="a8447-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a8447-105">Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="a8447-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="a8447-106">Die Struktur einer projektbasierten Angebotsposition wird für Projektvorkalkulationen um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="a8447-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="a8447-107">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="a8447-107">Billing Method</span></span>
- <span data-ttu-id="a8447-108">Projekt- und Aufgabenzuordnung</span><span class="sxs-lookup"><span data-stu-id="a8447-108">Project and Task Mapping</span></span>
- <span data-ttu-id="a8447-109">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="a8447-109">Included Transaction classes</span></span>
- <span data-ttu-id="a8447-110">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="a8447-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="a8447-111">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="a8447-111">Chargeability setup</span></span>
- <span data-ttu-id="a8447-112">Schätzung unter Verwendung von Angebotspositionsdetails</span><span class="sxs-lookup"><span data-stu-id="a8447-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="a8447-113">Angebotszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="a8447-113">Quote line Customers</span></span>

<span data-ttu-id="a8447-114">Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile.</span><span class="sxs-lookup"><span data-stu-id="a8447-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="a8447-115">Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.</span><span class="sxs-lookup"><span data-stu-id="a8447-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="a8447-116">**Feld**</span><span class="sxs-lookup"><span data-stu-id="a8447-116">**Field**</span></span> | <span data-ttu-id="a8447-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8447-117">**Description**</span></span> | <span data-ttu-id="a8447-118">**Downstream-Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="a8447-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a8447-119">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="a8447-119">Name</span></span> | <span data-ttu-id="a8447-120">Der Name der Angebotszeile, mit dessen Hilfe Sie die diskrete Komponente des Angebots identifizieren können, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="a8447-121">Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-122">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="a8447-122">Billing Method</span></span> | <span data-ttu-id="a8447-123">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="a8447-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="a8447-124">Dieses Feld enthält die beiden Haupt-Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="a8447-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="a8447-125">- Festpreis</span><span class="sxs-lookup"><span data-stu-id="a8447-125">- Fixed price</span></span></br><span data-ttu-id="a8447-126">- Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="a8447-126">- Time and material.</span></span>| <span data-ttu-id="a8447-127">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-128">Project</span><span class="sxs-lookup"><span data-stu-id="a8447-128">Project</span></span> | <span data-ttu-id="a8447-129">Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="a8447-130">Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails.</span><span class="sxs-lookup"><span data-stu-id="a8447-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="a8447-131">Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="a8447-132">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="a8447-133">Eingeschlossene Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-133">Included Tasks</span></span> | <span data-ttu-id="a8447-134">Gibt an, ob diese Angebotsposition für alle oder einige der Projektaufgaben für das ausgewählte Projekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="a8447-135">Dieses Feld weist die möglichen Werte auf:</span><span class="sxs-lookup"><span data-stu-id="a8447-135">This field has the following possible values:</span></span></br><span data-ttu-id="a8447-136">- Alle Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-136">- All project tasks</span></span></br><span data-ttu-id="a8447-137">- Nur ausgewählte Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-137">- Selected project tasks only</span></span></br><span data-ttu-id="a8447-138">Ein leerer Wert in diesem Feld entspricht der Option **Alle Projektaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="a8447-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="a8447-139">Wenn **Nur ausgewählte Projektaufgaben** auf der Projektseite ausgewählt wurde, können Sie auf der **Einrichtung der Aufgabenfakturierung**-Registerkarte bestimmte Aufgaben auswählen, um sie dieser Angebotszeile zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a8447-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="a8447-140">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-141">Zeit einschließen</span><span class="sxs-lookup"><span data-stu-id="a8447-141">Include Time</span></span> | <span data-ttu-id="a8447-142">Ein Wert von **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-143">Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-144">Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a8447-145">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-146">Ausgaben einschließen</span><span class="sxs-lookup"><span data-stu-id="a8447-146">Include Expense</span></span> | <span data-ttu-id="a8447-147">Ein Wert von **Ja**/**Nein** gibt an, ob die Ausgabenkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-148">Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-149">Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a8447-150">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-151">Material einschließen</span><span class="sxs-lookup"><span data-stu-id="a8447-151">Include Material</span></span> | <span data-ttu-id="a8447-152">Ein Wert von **Ja**/**Nein** gibt an, ob die Materialkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-153">Ein Wert von **Nein** gibt an, dass die Materialkosten nicht in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-154">Ein Wert von **Ja** gibt an, dass die Materialkosten in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a8447-155">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-156">Gebühr einschließen</span><span class="sxs-lookup"><span data-stu-id="a8447-156">Include Fee</span></span> | <span data-ttu-id="a8447-157">Ein Wert von **Ja**/**Nein** gibt an, ob die Gebühren für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="a8447-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-158">Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a8447-159">Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a8447-160">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-161">Angebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="a8447-161">Quoted Amount</span></span> | <span data-ttu-id="a8447-162">Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotszeile prognostizierten Arbeiten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="a8447-163">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="a8447-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="a8447-164">Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a8447-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="a8447-165">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-166">Geschätzte Steuer</span><span class="sxs-lookup"><span data-stu-id="a8447-166">Estimated Tax</span></span> | <span data-ttu-id="a8447-167">Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="a8447-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="a8447-168">Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a8447-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="a8447-169">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-170">Nettoangebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="a8447-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="a8447-171">Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a8447-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="a8447-172">Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet.</span><span class="sxs-lookup"><span data-stu-id="a8447-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="a8447-173">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-174">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="a8447-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="a8447-175">Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8447-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="a8447-176">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a8447-177">Kundenbudget</span><span class="sxs-lookup"><span data-stu-id="a8447-177">Customer Budget</span></span> | <span data-ttu-id="a8447-178">Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8447-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="a8447-179">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="a8447-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="a8447-180">Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen</span><span class="sxs-lookup"><span data-stu-id="a8447-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="a8447-181">**Regel 1**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, ist ein Projekt in der Angebotsposition einbezogen.</span><span class="sxs-lookup"><span data-stu-id="a8447-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="a8447-182">**Regel 2**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a8447-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="a8447-183">**Regel 3**: Wenn das Feld **Eingeschlossene Aufgaben** auf **Nur ausgewählte Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Angebotspositionen eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a8447-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="a8447-184">**Regel 4**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8447-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="a8447-185">**Regel 5**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8447-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="a8447-186">
                    <strong>Verkaufschance</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="a8447-187">
                    <strong>Angebot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="a8447-188">
                    <strong>Angebotsposition</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="a8447-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="a8447-190">
                    <strong>Eingeschlossene Aufgaben</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="a8447-191">
                    <strong>Zeit einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="a8447-192">
                    <strong>Ausgaben einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="a8447-193">
                    <strong>Material einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="a8447-194">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a8447-195">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="a8447-196">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="a8447-197">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a8447-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-198">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-199">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-200">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-201">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-202">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-203">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-204">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-205">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-206">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-207">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-208">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="a8447-208">Violation of Rule #2.</span></span> <span data-ttu-id="a8447-209">Zeit, Kosten und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="a8447-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-210">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-211">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-212">QL2</span><span class="sxs-lookup"><span data-stu-id="a8447-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-213">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-214">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-215">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-216">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-217">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-218">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-219">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-220">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-221">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-222">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-223">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-224">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="a8447-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-226">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-227">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-228">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-229">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="a8447-229">Violation of Rule #2.</span></span> <span data-ttu-id="a8447-230">Zeit, Material und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="a8447-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-231">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-232">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-233">QL2</span><span class="sxs-lookup"><span data-stu-id="a8447-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-234">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-235">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-236">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-237">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-238">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-239">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-240">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-241">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-242">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-243">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-244">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-245">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="a8447-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-247">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-248">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-249">Gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-250">Zeit, Material und Gebühren für das P1-Projekt sind in QL1 enthalten</span><span class="sxs-lookup"><span data-stu-id="a8447-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="a8447-251">Die Kosten für das P1-Projekt sind in QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="a8447-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="a8447-252">Keine Überlappung in dem, was in jeder Angebotszeile enthalten ist und daher gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a8447-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-253">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-254">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-255">QL2</span><span class="sxs-lookup"><span data-stu-id="a8447-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-256">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-257">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="a8447-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-259">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-260">Nr.</span><span class="sxs-lookup"><span data-stu-id="a8447-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="a8447-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-262">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-263">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-264">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-265">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-266">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-267">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-268">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-269">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-270">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-271">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-272">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="a8447-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="a8447-273">Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1</span><span class="sxs-lookup"><span data-stu-id="a8447-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="a8447-274">QL2 enthält Zeit, Ausgaben und Gebühren für das gesamte Projekt P1 und überschneidet sich daher mit dem, was in Q1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a8447-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-275">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-276">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-277">QL2</span><span class="sxs-lookup"><span data-stu-id="a8447-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-278">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-279">Leer</span><span class="sxs-lookup"><span data-stu-id="a8447-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-280">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-281">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-282">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-283">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-284">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-285">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-286">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-287">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-288">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-289">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-290">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-291">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-292">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-293">Gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-294">Gemäß Regel 3,</span><span class="sxs-lookup"><span data-stu-id="a8447-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="a8447-295">Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="a8447-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a8447-296">QL2 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="a8447-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a8447-297">Die einzige zusätzliche Validierung betrifft die Teilmenge der Aufgaben in QL1, die sich von der Teilmenge der Aufgaben in QL2 unterscheidet, um sicherzustellen, dass es keine Überlappung gibt.</span><span class="sxs-lookup"><span data-stu-id="a8447-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="a8447-298">Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a8447-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-299">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-300">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-301">QL2</span><span class="sxs-lookup"><span data-stu-id="a8447-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-302">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-303">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="a8447-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-304">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-305">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-306">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-307">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-308">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-309">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-310">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-311">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-312">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="a8447-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-313">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-314">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-315">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-316">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-317">Gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-318">Gemäß Regel 5 sind Q1 und Q2 zwei Anführungszeichen für dieselbe Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="a8447-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-319">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-320">Q2</span><span class="sxs-lookup"><span data-stu-id="a8447-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-321">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-322">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-323">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="a8447-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-324">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-325">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-326">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-327">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-328">O1</span><span class="sxs-lookup"><span data-stu-id="a8447-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-329">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-330">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-331">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-332">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="a8447-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-333">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-334">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-335">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-336">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-337">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="a8447-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a8447-338">Gemäß Regel 4 sind Q1 und Q2 zwei Anführungszeichen für verschiedene Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="a8447-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="a8447-339">O2</span><span class="sxs-lookup"><span data-stu-id="a8447-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="a8447-340">Q1</span><span class="sxs-lookup"><span data-stu-id="a8447-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="a8447-341">QL1</span><span class="sxs-lookup"><span data-stu-id="a8447-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-342">P1</span><span class="sxs-lookup"><span data-stu-id="a8447-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="a8447-343">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="a8447-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="a8447-344">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="a8447-345">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="a8447-346">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a8447-347">Ja</span><span class="sxs-lookup"><span data-stu-id="a8447-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
