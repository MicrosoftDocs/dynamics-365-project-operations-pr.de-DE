---
title: Eine projektbasierte Vertragszeile kalkulieren
description: Dieses Thema enthält Informationen zur Schätzung von projektbasierten Vertragszeilen.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180461"
---
# <a name="estimate-a-projectbased-contract-line"></a><span data-ttu-id="d6714-103">Eine projektbasierte Vertragszeile kalkulieren</span><span class="sxs-lookup"><span data-stu-id="d6714-103">Estimate a project–based contract line</span></span>

<span data-ttu-id="d6714-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="d6714-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span> 

<span data-ttu-id="d6714-105">In Dynamics 365 Project Operations enthält eine projektbasierte Vertragszeile Details, mit deren Hilfe die Kosten und potenziellen Einnahmen der für die Lieferung der Vertragszeile erforderlichen Arbeiten geschätzt werden können.</span><span class="sxs-lookup"><span data-stu-id="d6714-105">In Dynamics 365 Project Operations, a project-based contract line has details that help estimate the cost and potential revenue of the work involved to deliver the contract line.</span></span>

<span data-ttu-id="d6714-106">Um eine projektbasierte Vertragszeile zu schätzen, gehen Sie zur **Vertragszeilendetail**-Registerkarte auf der projektbasierten **Vertragszeile**.</span><span class="sxs-lookup"><span data-stu-id="d6714-106">To estimate a project-based contract line, go to the **Contract Line Detail** tab on the project-based **Contract Line**.</span></span>  <span data-ttu-id="d6714-107">Es gibt zwei Möglichkeiten, eine Schätzung für eine projektbasierte Vertragszeile zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d6714-107">There are two ways to create an estimate on a project-based contract line:</span></span>

   - <span data-ttu-id="d6714-108">Erstellen Sie einen Kostenvoranschlag direkt in der Vertragszeile, indem Sie die Vertragszeilendetails manuell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d6714-108">Create an estimate directly on the contract line by manually adding contract line details.</span></span>
   - <span data-ttu-id="d6714-109">Erstellen Sie ein Projekt und einen Projektplan und ordnen Sie das Projekt und die Aufgaben der Vertragszeile des Projekts zu.</span><span class="sxs-lookup"><span data-stu-id="d6714-109">Create a project and a project plan, and then associate the project and tasks to the project's contract line.</span></span> <span data-ttu-id="d6714-110">Dies ermöglicht den Prozess, mit dem Sie die Projektplanschätzung basierend auf den in der Vertragszeile enthaltenen Komponenten in die Vertragszeile importieren können.</span><span class="sxs-lookup"><span data-stu-id="d6714-110">This enables the process by which you can import the project plan estimate into the contract line based on the components included on the contract line.</span></span>

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a><span data-ttu-id="d6714-111">Eine Schätzung direkt für eine projektbasierte Vertragszeile erstellen</span><span class="sxs-lookup"><span data-stu-id="d6714-111">Create an estimate directly on a project–based contract line</span></span>

1. <span data-ttu-id="d6714-112">Gehen Sie zur Vertragszeile und wählen Sie die **Vertragszeilendetail**-Registerkarte aus. Die Zeilen, die Sie auf dieser Registerkarte erstellen, werden zusammengefasst und als **Vertragswert** für die **Vertragszeile** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6714-112">Go to the contract line and select the **Contract Line Detail** tab. The lines you create on this tab are summarized and display as the **Contracted Value** for this **Contract Line**.</span></span> 
2. <span data-ttu-id="d6714-113">Im **Vertragszeilendetails**-Unterraster wählen Sie **+ Neues Vertragszeilendetail**.</span><span class="sxs-lookup"><span data-stu-id="d6714-113">In the **Contract Line Details** subgrid, select **+ New Contract Line Detail**.</span></span> <span data-ttu-id="d6714-114">Ein Schnellschieberegler wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d6714-114">A quick-create slider opens.</span></span> <span data-ttu-id="d6714-115">Die folgenden Felder sind im **Vertragszeilendetails**-Formular verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d6714-115">The following fields are available on the **Contract Line Details** form:</span></span>

| <span data-ttu-id="d6714-116">Feld</span><span class="sxs-lookup"><span data-stu-id="d6714-116">Field</span></span> | <span data-ttu-id="d6714-117">Position</span><span class="sxs-lookup"><span data-stu-id="d6714-117">Location</span></span> | <span data-ttu-id="d6714-118">Beschreibung des Dataflows</span><span class="sxs-lookup"><span data-stu-id="d6714-118">Description</span></span> | <span data-ttu-id="d6714-119">Nachgelagerte Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="d6714-119">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="d6714-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6714-120">**Description**</span></span> | <span data-ttu-id="d6714-121">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-121">**Quick Create**</span></span> | <span data-ttu-id="d6714-122">Eine Beschreibung der bestimmten Schätzung.</span><span class="sxs-lookup"><span data-stu-id="d6714-122">A description of the specific estimate.</span></span> | <span data-ttu-id="d6714-123">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-123">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-124">**Transaktionsklasse**</span><span class="sxs-lookup"><span data-stu-id="d6714-124">**Transaction Class**</span></span> | <span data-ttu-id="d6714-125">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-125">**Quick Create**</span></span> | <span data-ttu-id="d6714-126">Diese Dropdown-Liste enthält eine Liste der Transaktionsklassen, die auf der **Allgemein**-Registerkarte der projektbasierten Vertragszeile enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d6714-126">This drop-down is a list of transaction classes included on the **General** tab of the project-based contract line.</span></span> | <span data-ttu-id="d6714-127">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-127">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-128">**Rolle**</span><span class="sxs-lookup"><span data-stu-id="d6714-128">**Role**</span></span> | <span data-ttu-id="d6714-129">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-129">**Quick Create**</span></span> | <span data-ttu-id="d6714-130">Die Rolle der Person, die diese Arbeit ausführt oder diese Kosten verursacht.</span><span class="sxs-lookup"><span data-stu-id="d6714-130">The role of the person who is performing this work or incurring this expense.</span></span> | <span data-ttu-id="d6714-131">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-131">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-132">**Kategorie**</span><span class="sxs-lookup"><span data-stu-id="d6714-132">**Category**</span></span> | <span data-ttu-id="d6714-133">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-133">**Quick Create**</span></span> | <span data-ttu-id="d6714-134">Die Kategorie der Arbeit oder Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d6714-134">The category of the work or expense.</span></span> | <span data-ttu-id="d6714-135">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-135">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-136">**Startdatum**</span><span class="sxs-lookup"><span data-stu-id="d6714-136">**Start Date**</span></span> | <span data-ttu-id="d6714-137">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-137">**Quick Create**</span></span> | <span data-ttu-id="d6714-138">Das Startdatum der Arbeit.</span><span class="sxs-lookup"><span data-stu-id="d6714-138">The start date of the work.</span></span> | <span data-ttu-id="d6714-139">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-139">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-140">**Enddatum**</span><span class="sxs-lookup"><span data-stu-id="d6714-140">**End Date**</span></span> | <span data-ttu-id="d6714-141">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-141">**Quick Create**</span></span> | <span data-ttu-id="d6714-142">Das Enddatum der Arbeit.</span><span class="sxs-lookup"><span data-stu-id="d6714-142">The end date of the work.</span></span> | <span data-ttu-id="d6714-143">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-143">This field defaults to the related contract line detail for the cost that is automatically created.</span></span> |
| <span data-ttu-id="d6714-144">**Ressourcenzuordnungsunternehmen**</span><span class="sxs-lookup"><span data-stu-id="d6714-144">**Resourcing Company**</span></span> | <span data-ttu-id="d6714-145">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-145">**Quick Create**</span></span> | <span data-ttu-id="d6714-146">Das Beschaffungsunternehmen oder die juristische Person, die diese Kosten verursachen und die Ressource bereitstellen, um daran zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6714-146">The resourcing company or legal entity that is incurring this cost and providing the resource to work on it.</span></span> | <span data-ttu-id="d6714-147">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-147">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="d6714-148">Dieses Feld wird auch zum Abrufen von Einstandspreisen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6714-148">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="d6714-149">**Ressourcenzuordnungseinheit**</span><span class="sxs-lookup"><span data-stu-id="d6714-149">**Resourcing Unit**</span></span> | <span data-ttu-id="d6714-150">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-150">**Quick Create**</span></span> | <span data-ttu-id="d6714-151">Die Ressourceneinheit , die diese Kosten verursacht und die Ressource bereitstellt, um daran zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6714-151">The resourcing unit that incurs this cost and provies the resource to work on it.</span></span> | <span data-ttu-id="d6714-152">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-152">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="d6714-153">Dieses Feld wird auch zum Abrufen von Einstandspreisen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6714-153">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="d6714-154">**Einheitenzeitplan**</span><span class="sxs-lookup"><span data-stu-id="d6714-154">**Unit schedule**</span></span> | <span data-ttu-id="d6714-155">**Schnellerfassung**</span><span class="sxs-lookup"><span data-stu-id="d6714-155">**Quick create**</span></span> | <span data-ttu-id="d6714-156">Die Einheitsgruppe der Arbeit oder des Aufwands.</span><span class="sxs-lookup"><span data-stu-id="d6714-156">The unit group of the work or expense.</span></span> <span data-ttu-id="d6714-157">Einheiten gehören zu einem Einheitenplan oder einer Gruppe von Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d6714-157">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="d6714-158">Zum Beispiel *Meilen* und *Kilometer (km)* sind Einheiten, die zu einer Gruppe von Einheiten gehören, die die Entfernung beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d6714-158">For example, *miles* and *kilometers (Kms)* are units that belong to a group of units that describe distance.</span></span> | <span data-ttu-id="d6714-159">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-159">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-160">**Einheit**</span><span class="sxs-lookup"><span data-stu-id="d6714-160">**Unit**</span></span> | <span data-ttu-id="d6714-161">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-161">**Quick Create**</span></span> | <span data-ttu-id="d6714-162">Die Einheit der Arbeit oder des Aufwands.</span><span class="sxs-lookup"><span data-stu-id="d6714-162">The unit of work or expense.</span></span> | <span data-ttu-id="d6714-163">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-163">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-164">**Menge**</span><span class="sxs-lookup"><span data-stu-id="d6714-164">**Quantity**</span></span> | <span data-ttu-id="d6714-165">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-165">**Quick Create**</span></span> | <span data-ttu-id="d6714-166">Die Menge der Arbeit oder des Aufwands.</span><span class="sxs-lookup"><span data-stu-id="d6714-166">The quantity of work or expense.</span></span> | <span data-ttu-id="d6714-167">In diesem Feld werden standardmäßig die zugehörigen Vertragszeilendetails für Kosten verwendet, die automatisch erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-167">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d6714-168">**Einheitenpreis**</span><span class="sxs-lookup"><span data-stu-id="d6714-168">**Unit price**</span></span> | <span data-ttu-id="d6714-169">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-169">**Quick Create**</span></span> | <span data-ttu-id="d6714-170">Der Rechnungssatz der Rolle, die die Arbeit ausführt, oder der Verkaufspreis der Ausgabenkategorie.</span><span class="sxs-lookup"><span data-stu-id="d6714-170">The bill rate of the role that is performing the work or the sales price of the expense category.</span></span> <span data-ttu-id="d6714-171">Dieses Feld wird standardmäßig für die **Zeit** basierend auf der Kombination aus Rolle und Ressourceneinheit in der Projektpreisliste verwendet, die für das Startdatum gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6714-171">This field defaults for **Time** based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="d6714-172">Für Ausgaben stammt die Standardeinstellung dieses Felds aus der Preiseinstellung für die Transaktionskategorie in der Projektpreisliste, die für das Startdatum gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6714-172">For expenses, this field's default is from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="d6714-173">Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht **Preis pro Einheit** ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer.</span><span class="sxs-lookup"><span data-stu-id="d6714-173">If the pricing method for the transaction category is not **price-per-unit**, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="d6714-174">Der Kostensatz der Rolle, die die Arbeit ausführt, oder die Kosten pro Einheit der Ausgabenkategorie.</span><span class="sxs-lookup"><span data-stu-id="d6714-174">The cost rate of the role that is performing the work, or the cost per unit of the expense category.</span></span> <span data-ttu-id="d6714-175">Dieses Feld ist standardmäßig auf **Zeit basierend auf der Rolle** und die Kombination der Ressourceneinheiten in der Rollenpreislinie der Kostenpreisliste, die der Vertragseinheit zum Stichtag beigefügt ist, eingestellt.</span><span class="sxs-lookup"><span data-stu-id="d6714-175">This field defaults for **Time based on the role** and the resourcing unit combination on the role price line of the cost price list attached to the contracting unit effective for the start date.</span></span> <span data-ttu-id="d6714-176">Für Ausgaben basiert die Standardeinstellung dieses Felds auf der Kategoriepreiszeile der Einstandspreisliste, die der Vertragseinheit zugeordnet und für das Startdatum gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6714-176">For expenses, this field's default is based on the category price line of the cost price list attached to the contracting unit that is effective for the start date.</span></span> <span data-ttu-id="d6714-177">Wenn die Preisberechnungsmethode für die Transaktionskategorie nicht Preis pro Einheit ist, gibt es keine Standardeinstellung, und dieses Feld bleibt leer.</span><span class="sxs-lookup"><span data-stu-id="d6714-177">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="d6714-178">**Geschätzte Steuer**</span><span class="sxs-lookup"><span data-stu-id="d6714-178">**Estimated Tax**</span></span> | <span data-ttu-id="d6714-179">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-179">**Quick Create**</span></span> | <span data-ttu-id="d6714-180">Die geschätzte Steuer für diese Arbeit oder Ausgabe, wie vom Benutzer eingegeben.</span><span class="sxs-lookup"><span data-stu-id="d6714-180">The estimated tax for this work or expense as input by the user.</span></span> | <span data-ttu-id="d6714-181">Die geschätzte Steuer für diese Arbeit oder Ausgabe, wie vom Benutzer eingegeben.</span><span class="sxs-lookup"><span data-stu-id="d6714-181">The estimated tax for this work or expense as input by the user.</span></span> |
| <span data-ttu-id="d6714-182">**Betrag**</span><span class="sxs-lookup"><span data-stu-id="d6714-182">**Amount**</span></span> | <span data-ttu-id="d6714-183">**Schnellertellung**</span><span class="sxs-lookup"><span data-stu-id="d6714-183">**Quick Create**</span></span> | <span data-ttu-id="d6714-184">Dieser Wert in diesem Feld kann vom Benutzer hinzugefügt werden, wenn die Felder **Menge** und **Preis** leer bleiben.</span><span class="sxs-lookup"><span data-stu-id="d6714-184">This value in this field can be added by the user if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="d6714-185">Wenn **Menge** und **Preis** gefüllt sind, ist das **Menge**-Feld schreibgeschützt und wird als **(Menge \* Stückpreis) + Steuern** berechnet.</span><span class="sxs-lookup"><span data-stu-id="d6714-185">If **Quantity** and **Price** are filled, the **Amount** field is read-only and is calculated as **(Quantity \* Unit price) + Tax**.</span></span> | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a><span data-ttu-id="d6714-186">Aktualisieren Sie die Preise für Vertragsdetails</span><span class="sxs-lookup"><span data-stu-id="d6714-186">Update prices on contract line details</span></span>

<span data-ttu-id="d6714-187">Wenn Sie die Preise in der Projektpreisliste ändern, die dem Vertrag beigefügt ist, oder in der Kostenpreisliste der Vertragseinheit, können Sie die Preise in den einzelnen Vertragszeilendetails aktualisieren, um die Änderung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d6714-187">If you change prices on the project price list that is attached to the contract or the cost price list of the contracting unit, you can refresh the prices on the individual contract line details to reflect the change.</span></span> <span data-ttu-id="d6714-188">Wählen Sie auf der **Vertrag**-Seite **Neu berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="d6714-188">On the **Contract** page, select **Recalculate**.</span></span> <span data-ttu-id="d6714-189">Eine Warnung informiert Sie darüber, dass die Preise für alle Vertragszeilen in diesem Vertrag zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d6714-189">A warning opens to inform you that prices for all contract lines on this contract are reset.</span></span> <span data-ttu-id="d6714-190">Wählen Sie **Ja**, um die Preise sowohl für Verkaufs- als auch für Kostenvertragsdetails zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d6714-190">Select **Yes** to refresh prices for both sales and cost contract line details.</span></span>

## <a name="access-contract-line-details-for-cost"></a><span data-ttu-id="d6714-191">Greifen Sie auf die Kosten der Vertragszeile zu</span><span class="sxs-lookup"><span data-stu-id="d6714-191">Access contract line details for cost</span></span>

<span data-ttu-id="d6714-192">Auf der **Vertragszeilendetails**-Registerkarte wählen Sie eine Zeile im Raster aus, um Aktionen in der Symbolleiste des Unterrasters anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6714-192">On the **Contract Line Details** tab, select a row in the grid to display actions on the toolbar of the subgrid.</span></span> <span data-ttu-id="d6714-193">Die erste Aktion in der Symbolleiste des Unterrasters ist **Kostendetail öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d6714-193">The first action on the subgrid tool bar is **Open Cost Detail**.</span></span> <span data-ttu-id="d6714-194">Wählen Sie **Kostendetail öffnen** aus, um den entsprechenden Kostensatz und den entsprechenden Betrag für diese Vertragszeilendetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d6714-194">To see the related cost rate and amount for this contract line detail, select **Open Cost Detail**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d6714-195">Durch das Ändern des Ressourcenzuordnungsunternehmen, der Ressourceneinheit, der Menge, der Daten, der Rolle oder der Kategoriewerte in den Vertragszeilendetails für **Kosten** werden auch die entsprechenden Werte im Vertragszeilendetail für **Vertrieb** geändert.</span><span class="sxs-lookup"><span data-stu-id="d6714-195">Changing the resourcing company, resourcing unit, quantity, dates, role, or category values on the contract line detail for **Cost** also changes the corresponding values on the contract line detail for **Sales**.</span></span>

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a><span data-ttu-id="d6714-196">Angaben zur Währung in der Vertragszeile für Kosten und Umsatz</span><span class="sxs-lookup"><span data-stu-id="d6714-196">Currency on contract line details for cost and sales</span></span>

<span data-ttu-id="d6714-197">Das Vertragszeilendetail für **Vertrieb** legt die Standardwährung aus der Projektpreisliste fest, die für das Startdatum des Vertragszeilendetails gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6714-197">The contract line detail for **Sales** sets the default currency from the project price list that is effective for the start date of the contract line detail.</span></span>

<span data-ttu-id="d6714-198">Das Vertragszeilendetail für **Kosten** legt die Standardwährung aus der Preisliste der Vertragseinheit des Vertrags fest, die für das Startdatum des Vertragszeilendetails für **Kosten** gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d6714-198">The contract line detail for **Cost** sets the default currency from the price list of the contracting unit of the contract that is effective for the start date of the contract line detail for **Cost**.</span></span>

<span data-ttu-id="d6714-199">Rentabilitätsberechnungen konvertieren die Beträge für die Vertragszeilendetails für **Kosten** und **Vertrieb** in die Basiswährung der Umgebung, um die tatsächlichen und geschätzten Gesamtmargen des Vertrags zu melden.</span><span class="sxs-lookup"><span data-stu-id="d6714-199">Profitability calculations convert the amounts for the contract line details for **Cost** and **Sales** into the base currency of the environment to report the overall actual and estimated margins on the contract.</span></span>

> [!NOTE]
> <span data-ttu-id="d6714-200">Währungsrundungsfehler und geänderte Margen können aufgrund fehlender datumswirksamer Wechselkurse auftreten.</span><span class="sxs-lookup"><span data-stu-id="d6714-200">Currency rounding errors and changed margins could occur because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="d6714-201">Verwenden Sie diese Berechnungen für Projektverträge nur als Näherungswerte und nicht für tatsächliche gesetzliche oder andere Berichte, die eine höhere Rundungsgenauigkeit und Kenntnis der Datumseffektivität für Wechselkurse erfordern.</span><span class="sxs-lookup"><span data-stu-id="d6714-201">Use these calculations on project contracts only as approximations and not for actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>