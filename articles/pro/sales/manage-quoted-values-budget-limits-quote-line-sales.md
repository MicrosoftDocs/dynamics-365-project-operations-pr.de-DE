---
title: Projektbasierte Angebotspositionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994855"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="96cb2-103">Projektbasierte Angebotspositionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="96cb2-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="96cb2-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_</span><span class="sxs-lookup"><span data-stu-id="96cb2-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96cb2-105">Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen.</span><span class="sxs-lookup"><span data-stu-id="96cb2-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="96cb2-106">Die Struktur einer projektbasierten Angebotsposition wird für Projektvorkalkulationen um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="96cb2-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="96cb2-107">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="96cb2-107">Billing Method</span></span>
- <span data-ttu-id="96cb2-108">Projekt- und Aufgabenzuordnung</span><span class="sxs-lookup"><span data-stu-id="96cb2-108">Project and Task Mapping</span></span>
- <span data-ttu-id="96cb2-109">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="96cb2-109">Included Transaction classes</span></span>
- <span data-ttu-id="96cb2-110">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="96cb2-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="96cb2-111">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="96cb2-111">Chargeability setup</span></span>
- <span data-ttu-id="96cb2-112">Schätzung unter Verwendung von Angebotspositionsdetails</span><span class="sxs-lookup"><span data-stu-id="96cb2-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="96cb2-113">Angebotszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="96cb2-113">Quote line Customers</span></span>

<span data-ttu-id="96cb2-114">Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile.</span><span class="sxs-lookup"><span data-stu-id="96cb2-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="96cb2-115">Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.</span><span class="sxs-lookup"><span data-stu-id="96cb2-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="96cb2-116">**Feld**</span><span class="sxs-lookup"><span data-stu-id="96cb2-116">**Field**</span></span> | <span data-ttu-id="96cb2-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96cb2-117">**Description**</span></span> | <span data-ttu-id="96cb2-118">**Downstream-Auswirkungen**</span><span class="sxs-lookup"><span data-stu-id="96cb2-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="96cb2-119">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="96cb2-119">Name</span></span> | <span data-ttu-id="96cb2-120">Der Name der Angebotszeile, mit dessen Hilfe Sie die diskrete Komponente des Angebots identifizieren können, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="96cb2-121">Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-122">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="96cb2-122">Billing Method</span></span> | <span data-ttu-id="96cb2-123">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="96cb2-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="96cb2-124">Dieses Feld enthält die beiden Haupt-Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="96cb2-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="96cb2-125">- Festpreis</span><span class="sxs-lookup"><span data-stu-id="96cb2-125">- Fixed price</span></span></br><span data-ttu-id="96cb2-126">- Zeit und Materialien</span><span class="sxs-lookup"><span data-stu-id="96cb2-126">- Time and material.</span></span>| <span data-ttu-id="96cb2-127">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-128">Project</span><span class="sxs-lookup"><span data-stu-id="96cb2-128">Project</span></span> | <span data-ttu-id="96cb2-129">Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="96cb2-130">Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails.</span><span class="sxs-lookup"><span data-stu-id="96cb2-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="96cb2-131">Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="96cb2-132">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="96cb2-133">Eingeschlossene Aufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-133">Included Tasks</span></span> | <span data-ttu-id="96cb2-134">Gibt an, ob diese Angebotsposition für alle oder einige der Projektaufgaben für das ausgewählte Projekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="96cb2-135">Dieses Feld weist die möglichen Werte auf:</span><span class="sxs-lookup"><span data-stu-id="96cb2-135">This field has the following possible values:</span></span></br><span data-ttu-id="96cb2-136">- Alle Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-136">- All project tasks</span></span></br><span data-ttu-id="96cb2-137">- Nur ausgewählte Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-137">- Selected project tasks only</span></span></br><span data-ttu-id="96cb2-138">Ein leerer Wert in diesem Feld entspricht der Option **Alle Projektaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="96cb2-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="96cb2-139">Wenn **Nur ausgewählte Projektaufgaben** auf der Projektseite ausgewählt wurde, können Sie auf der **Einrichtung der Aufgabenfakturierung**-Registerkarte bestimmte Aufgaben auswählen, um sie dieser Angebotszeile zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="96cb2-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="96cb2-140">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-141">Zeit einschließen</span><span class="sxs-lookup"><span data-stu-id="96cb2-141">Include Time</span></span> | <span data-ttu-id="96cb2-142">Ein Wert von **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-143">Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-144">Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96cb2-145">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-146">Ausgaben einschließen</span><span class="sxs-lookup"><span data-stu-id="96cb2-146">Include Expense</span></span> | <span data-ttu-id="96cb2-147">Ein Wert von **Ja**/**Nein** gibt an, ob die Ausgabenkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-148">Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-149">Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96cb2-150">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-151">Material einschließen</span><span class="sxs-lookup"><span data-stu-id="96cb2-151">Include Material</span></span> | <span data-ttu-id="96cb2-152">Ein Wert von **Ja**/**Nein** gibt an, ob die Materialkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-153">Ein Wert von **Nein** gibt an, dass die Materialkosten nicht in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-154">Ein Wert von **Ja** gibt an, dass die Materialkosten in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96cb2-155">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-156">Gebühr einschließen</span><span class="sxs-lookup"><span data-stu-id="96cb2-156">Include Fee</span></span> | <span data-ttu-id="96cb2-157">Ein Wert von **Ja**/**Nein** gibt an, ob die Gebühren für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="96cb2-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-158">Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="96cb2-159">Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="96cb2-160">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-161">Angebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="96cb2-161">Quoted Amount</span></span> | <span data-ttu-id="96cb2-162">Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotszeile prognostizierten Arbeiten angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="96cb2-163">Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert.</span><span class="sxs-lookup"><span data-stu-id="96cb2-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="96cb2-164">Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="96cb2-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="96cb2-165">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-166">Geschätzte Steuer</span><span class="sxs-lookup"><span data-stu-id="96cb2-166">Estimated Tax</span></span> | <span data-ttu-id="96cb2-167">Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann.</span><span class="sxs-lookup"><span data-stu-id="96cb2-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="96cb2-168">Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="96cb2-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="96cb2-169">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-170">Nettoangebotsbetrag</span><span class="sxs-lookup"><span data-stu-id="96cb2-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="96cb2-171">Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="96cb2-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="96cb2-172">Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet.</span><span class="sxs-lookup"><span data-stu-id="96cb2-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="96cb2-173">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-174">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="96cb2-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="96cb2-175">Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96cb2-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="96cb2-176">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="96cb2-177">Kundenbudget</span><span class="sxs-lookup"><span data-stu-id="96cb2-177">Customer Budget</span></span> | <span data-ttu-id="96cb2-178">Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="96cb2-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="96cb2-179">Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="96cb2-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="96cb2-180">Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen</span><span class="sxs-lookup"><span data-stu-id="96cb2-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="96cb2-181">**Regel 1**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, ist ein Projekt in der Angebotsposition einbezogen.</span><span class="sxs-lookup"><span data-stu-id="96cb2-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="96cb2-182">**Regel 2**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="96cb2-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="96cb2-183">**Regel 3**: Wenn das Feld **Eingeschlossene Aufgaben** auf **Nur ausgewählte Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Angebotspositionen eines Angebots enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="96cb2-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="96cb2-184">**Regel 4**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="96cb2-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="96cb2-185">**Regel 5**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="96cb2-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="96cb2-186">
                    <strong>Verkaufschance</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="96cb2-187">
                    <strong>Angebot</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="96cb2-188">
                    <strong>Angebotsposition</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="96cb2-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="96cb2-190">
                    <strong>Eingeschlossene Aufgaben</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="96cb2-191">
                    <strong>Zeit einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="96cb2-192">
                    <strong>Ausgaben einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="96cb2-193">
                    <strong>Material einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="96cb2-194">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="96cb2-195">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="96cb2-196">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="96cb2-197">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="96cb2-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-198">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-199">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-200">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-201">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-202">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-203">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-204">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-205">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-206">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-207">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-208">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="96cb2-208">Violation of Rule #2.</span></span> <span data-ttu-id="96cb2-209">Zeit, Kosten und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="96cb2-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-210">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-211">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-212">QL2</span><span class="sxs-lookup"><span data-stu-id="96cb2-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-213">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-214">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-215">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-216">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-217">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-218">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-218">Yes</span></span> </p>
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
<span data-ttu-id="96cb2-219">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-220">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-221">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-222">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-223">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-224">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="96cb2-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-226">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-227">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-228">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-229">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="96cb2-229">Violation of Rule #2.</span></span> <span data-ttu-id="96cb2-230">Zeit, Material und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="96cb2-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-231">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-232">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-233">QL2</span><span class="sxs-lookup"><span data-stu-id="96cb2-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-234">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-235">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-236">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-237">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-238">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-239">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-239">Yes</span></span> </p>
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
<span data-ttu-id="96cb2-240">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-241">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-242">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-243">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-244">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-245">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="96cb2-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-247">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-248">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-249">Gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-250">Zeit, Material und Gebühren für das P1-Projekt sind in QL1 enthalten</span><span class="sxs-lookup"><span data-stu-id="96cb2-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="96cb2-251">Die Kosten für das P1-Projekt sind in QL2 enthalten</span><span class="sxs-lookup"><span data-stu-id="96cb2-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="96cb2-252">Keine Überlappung in dem, was in jeder Angebotszeile enthalten ist und daher gültig ist.</span><span class="sxs-lookup"><span data-stu-id="96cb2-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-253">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-254">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-255">QL2</span><span class="sxs-lookup"><span data-stu-id="96cb2-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-256">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-257">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="96cb2-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-259">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-260">Nr.</span><span class="sxs-lookup"><span data-stu-id="96cb2-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="96cb2-261">No</span></span> </p>
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
<span data-ttu-id="96cb2-262">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-263">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-264">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-265">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-266">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-267">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-268">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-269">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-270">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-271">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-272">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="96cb2-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="96cb2-273">Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="96cb2-274">QL2 enthält Zeit, Ausgaben und Gebühren für das gesamte Projekt P1 und überschneidet sich daher mit dem, was in Q1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96cb2-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-275">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-276">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-277">QL2</span><span class="sxs-lookup"><span data-stu-id="96cb2-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-278">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-279">Leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-280">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-281">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-282">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-283">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-283">Yes</span></span> </p>
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
<span data-ttu-id="96cb2-284">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-285">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-286">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-287">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-288">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-289">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-290">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-291">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-292">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-293">Gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-294">Gemäß Regel 3,</span><span class="sxs-lookup"><span data-stu-id="96cb2-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="96cb2-295">Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="96cb2-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="96cb2-296">QL2 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="96cb2-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="96cb2-297">Die einzige zusätzliche Validierung betrifft die Teilmenge der Aufgaben in QL1, die sich von der Teilmenge der Aufgaben in QL2 unterscheidet, um sicherzustellen, dass es keine Überlappung gibt.</span><span class="sxs-lookup"><span data-stu-id="96cb2-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="96cb2-298">Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="96cb2-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-299">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-300">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-301">QL2</span><span class="sxs-lookup"><span data-stu-id="96cb2-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-302">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-303">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="96cb2-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-304">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-305">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-306">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-307">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-307">Yes</span></span> </p>
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
<span data-ttu-id="96cb2-308">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-309">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-310">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-311">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-312">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-313">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-314">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-315">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-316">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-317">Gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-318">Gemäß Regel 5 sind Q1 und Q2 zwei Anführungszeichen für dieselbe Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="96cb2-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-319">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-320">Q2</span><span class="sxs-lookup"><span data-stu-id="96cb2-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-321">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-322">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-323">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-324">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-325">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-326">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-327">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-327">Yes</span></span> </p>
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
<span data-ttu-id="96cb2-328">O1</span><span class="sxs-lookup"><span data-stu-id="96cb2-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-329">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-330">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-331">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-332">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-333">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-334">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-335">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-336">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-337">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="96cb2-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="96cb2-338">Gemäß Regel 4 sind Q1 und Q2 zwei Anführungszeichen für verschiedene Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.</span><span class="sxs-lookup"><span data-stu-id="96cb2-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="96cb2-339">O2</span><span class="sxs-lookup"><span data-stu-id="96cb2-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="96cb2-340">Q1</span><span class="sxs-lookup"><span data-stu-id="96cb2-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="96cb2-341">QL1</span><span class="sxs-lookup"><span data-stu-id="96cb2-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-342">P1</span><span class="sxs-lookup"><span data-stu-id="96cb2-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="96cb2-343">Alle Projektaufgaben oder leer</span><span class="sxs-lookup"><span data-stu-id="96cb2-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="96cb2-344">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="96cb2-345">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="96cb2-346">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="96cb2-347">Ja</span><span class="sxs-lookup"><span data-stu-id="96cb2-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
