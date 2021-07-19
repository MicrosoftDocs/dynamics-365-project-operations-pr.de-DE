---
title: Projektbasierte Vertragszeilen – Übersicht
description: Dieses Thema enthält Informationen zur Arbeit mit projektbasierten Vertragszeilen.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369915"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="03645-103">Projektbasierte Vertragszeilen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="03645-103">Project-based contract lines overview</span></span>

<span data-ttu-id="03645-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="03645-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03645-105">Projektbasierte Vertragszeilen in Dynamics 365 Project Operations dienen dazu, die Kostenvoranschlags- und Abrechnungsvereinbarungen für bestimmte Komponenten der Projektarbeit an einem Auftrag zu speichern.</span><span class="sxs-lookup"><span data-stu-id="03645-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="03645-106">Die Struktur einer projektbasierten Vertragszeile wird für Projektschätzungen und Abrechnungsszenarien um folgende Konzepte erweitert:</span><span class="sxs-lookup"><span data-stu-id="03645-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="03645-107">Abrechnungsmethode</span><span class="sxs-lookup"><span data-stu-id="03645-107">Billing method</span></span>
- <span data-ttu-id="03645-108">Projekt‑ und Aufgabenzuordnung</span><span class="sxs-lookup"><span data-stu-id="03645-108">Project and task mapping</span></span>
- <span data-ttu-id="03645-109">Eingeschlossene Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="03645-109">Included transaction classes</span></span>
- <span data-ttu-id="03645-110">Nicht zu überschreitender Grenzwert</span><span class="sxs-lookup"><span data-stu-id="03645-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="03645-111">Fakturierbarkeitseinrichtung</span><span class="sxs-lookup"><span data-stu-id="03645-111">Chargeability setup</span></span>
- <span data-ttu-id="03645-112">Schätzungen unter Verwendung von Vertragszeilendetails</span><span class="sxs-lookup"><span data-stu-id="03645-112">Estimates using contract line details</span></span>
- <span data-ttu-id="03645-113">Vertragszeilenkunden</span><span class="sxs-lookup"><span data-stu-id="03645-113">Contract line customers</span></span>

<span data-ttu-id="03645-114">Die folgende Tabelle enthält die Felder auf der **Allgemein**-Registerkarte mit projektbasierten Vertragszeilen, mit deren Hilfe die Grundlage für eine detaillierte, grundlegende Schätzung und Abrechnungsmodalitäten für projektbasierte Arbeiten geschaffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="03645-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="03645-115">Feld</span><span class="sxs-lookup"><span data-stu-id="03645-115">Field</span></span> | <span data-ttu-id="03645-116">Beschreibung des Dataflows</span><span class="sxs-lookup"><span data-stu-id="03645-116">Description</span></span> | <span data-ttu-id="03645-117">Nachgelagerte Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="03645-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="03645-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="03645-118">**Name**</span></span> | <span data-ttu-id="03645-119">Name der Vertragszeile.</span><span class="sxs-lookup"><span data-stu-id="03645-119">Name of the contract line.</span></span> <span data-ttu-id="03645-120">Dies identifiziert die diskrete Komponente des Vertrags, die geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="03645-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="03645-121">Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Wert der projektbasierten Angebotszeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="03645-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="03645-122">Der Name, der in die Projektrechnungszeile kopiert wird, die aus dieser Vertragszeile erstellt wird, wenn die Rechnung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="03645-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="03645-123">**Fakturierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="03645-123">**Billing Method**</span></span> | <span data-ttu-id="03645-124">Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="03645-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="03645-125">Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="03645-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="03645-126">- **Festpreis**</span><span class="sxs-lookup"><span data-stu-id="03645-126">- **Fixed Price**</span></span></br><span data-ttu-id="03645-127">- **Zeit und Materialien**</span><span class="sxs-lookup"><span data-stu-id="03645-127">- **Time and Material**</span></span> | <span data-ttu-id="03645-128">Basierend auf der Abrechnungsmethode der referenzierten Vertragszeile wird die eigentliche Transaktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="03645-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="03645-129">Wenn die Vertragszeile, auf die sich der Istwert bezieht, über eine Zeit- und Materialabrechnungsmethode verfügt, werden Kosten- und nicht abgerechnete Umsatzdatensätze erstellt.</span><span class="sxs-lookup"><span data-stu-id="03645-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="03645-130">Wenn die Vertragszeile, auf die der Istwert verweist, eine Abrechnungsmethode zum Festpreis hat, wird nur ein Istpreis erstellt.</span><span class="sxs-lookup"><span data-stu-id="03645-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="03645-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="03645-131">**Project**</span></span> | <span data-ttu-id="03645-132">Verwenden Sie dieses Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03645-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="03645-133">Dieser Wert wird in Verbindung mit **Eingeschlossene Aufgaben** und **Eingeschlossene Transaktionsklassen** verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="03645-134">**Eingeschlossene Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="03645-134">**Included Tasks**</span></span> | <span data-ttu-id="03645-135">Gibt an, ob diese Vertragszeile alle Projektaufgaben für das ausgewählte Projekt oder nur eine Teilmenge der Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="03645-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="03645-136">Dies ist ein Optionssatz, der über die folgenden möglichen Werte verfügt:</span><span class="sxs-lookup"><span data-stu-id="03645-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="03645-137">- **Alle Projektaufgaben**</span><span class="sxs-lookup"><span data-stu-id="03645-137">- **All Project Tasks**</span></span></br><span data-ttu-id="03645-138">- **Nur ausgewählte Projektaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="03645-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="03645-139">Ein leerer Wert in diesem Feld entspricht der Auswahl **Alle Projektaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="03645-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="03645-140">Wenn **Nur ausgewählte Aufgaben** ausgewählt ist, können Sie bestimmte Aufgaben auswählen und dieser Vertragszeile auf der **Einrichtung der Aufgabenabrechnung**-Registerkarte auf der **Projekt**-Seite zuordnen.</span><span class="sxs-lookup"><span data-stu-id="03645-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="03645-141">Der Wert wird in Verbindung mit **Projekt** und **Eingeschlossene Transaktionsklassen** verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="03645-142">**Zeit einschließen**</span><span class="sxs-lookup"><span data-stu-id="03645-142">**Include Time**</span></span> | <span data-ttu-id="03645-143">Ein Wert von **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="03645-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="03645-144">Ein **Nein**-Wert zeigt an, dass die Zeittransaktionen oder Arbeitskosten in dieser Vertragszeile enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="03645-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="03645-145">Ein **Ja**-Wert gibt an, dass sie enthalten sind</span><span class="sxs-lookup"><span data-stu-id="03645-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="03645-146">Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="03645-147">**Ausgaben einschließen**</span><span class="sxs-lookup"><span data-stu-id="03645-147">**Include Expense**</span></span> | <span data-ttu-id="03645-148">Ein Wert von **Ja**/**Nein** gibt an, ob die Ausgabenkosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="03645-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="03645-149">Ein **Nein**-Wert zeigt an, dass die Ausgabenkosten in dieser Vertragszeile nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="03645-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="03645-150">Ein **Ja**-Wert gibt an, dass sie enthalten sind</span><span class="sxs-lookup"><span data-stu-id="03645-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="03645-151">Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="03645-152">**Materialien einschließen**</span><span class="sxs-lookup"><span data-stu-id="03645-152">**Include Materials**</span></span> | <span data-ttu-id="03645-153">Ein Wert von **Ja**/**Nein** gibt an, ob die Materialkosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="03645-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="03645-154">Ein Wert von **Nein** gibt an, dass die Materialkosten nicht in dieser Vertragszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="03645-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="03645-155">Ein **Ja**-Wert gibt an, dass sie enthalten sind</span><span class="sxs-lookup"><span data-stu-id="03645-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="03645-156">Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="03645-157">**Gebühr einschließen**</span><span class="sxs-lookup"><span data-stu-id="03645-157">**Include Fee**</span></span> | <span data-ttu-id="03645-158">Ein Wert von **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="03645-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="03645-159">Ein **Nein**-Wert zeigt an, dass Gebühren in dieser Vertragszeile nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="03645-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="03645-160">Ein **Ja**-Wert gibt an, dass sie enthalten sind</span><span class="sxs-lookup"><span data-stu-id="03645-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="03645-161">Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="03645-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="03645-162">**Vertraglicher Betrag**</span><span class="sxs-lookup"><span data-stu-id="03645-162">**Contracted Amount**</span></span> | <span data-ttu-id="03645-163">Bei einer Festpreisvertragszeile ist dieser Betrag der vereinbarte Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="03645-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="03645-164">Bei einer Zeit- und Materialtransaktionenvertragszeile ist dieser Betrag ein geschätzter Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="03645-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="03645-165">Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="03645-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="03645-166">Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Vertragszeilendetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="03645-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="03645-167">Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Beträge in den Zeilendetails geändert werden.</span><span class="sxs-lookup"><span data-stu-id="03645-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="03645-168">In einer Festpreisvertragszeile wird dieser Wert verwendet, um den Betrag vor Steuern für periodische Abrechnungsmeilensteine zu generieren.</span><span class="sxs-lookup"><span data-stu-id="03645-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="03645-169">**Geschätzte Steuer**</span><span class="sxs-lookup"><span data-stu-id="03645-169">**Estimated Tax**</span></span> | <span data-ttu-id="03645-170">Der Benutzer kann dieses Feld bearbeiten, um den geschätzten Steuerbetrag in die Vertragszeile einzugeben.</span><span class="sxs-lookup"><span data-stu-id="03645-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="03645-171">Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Vertragszeilendetails zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="03645-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="03645-172">Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Steuerbeträge in den Zeilendetails geändert werden.</span><span class="sxs-lookup"><span data-stu-id="03645-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="03645-173">In einer Festpreisvertragszeile wird dieser Wert verwendet, um die Steuern für periodische Abrechnungsmeilensteine zu generieren.</span><span class="sxs-lookup"><span data-stu-id="03645-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="03645-174">**Vertraglicher Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="03645-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="03645-175">Der vertragliche Nettobetrag.</span><span class="sxs-lookup"><span data-stu-id="03645-175">The contract line amount after tax.</span></span> <span data-ttu-id="03645-176">Dieses Feld ist schreibgeschützt und wird berechnet als **Vertraglicher Betrag + Steuer**.</span><span class="sxs-lookup"><span data-stu-id="03645-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="03645-177">In einer Festpreisvertragszeile wird dieser Wert verwendet, um die periodische Abrechnungsmeilensteine zu generieren.</span><span class="sxs-lookup"><span data-stu-id="03645-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="03645-178">**Nicht zu überschreitender Grenzwert**</span><span class="sxs-lookup"><span data-stu-id="03645-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="03645-179">Der Benutzer kann dieses Feld bearbeiten und es ist nur in projektbasierten Vertragszeilen verfügbar, für die die Abrechnungsmethode als Zeit und Material festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03645-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="03645-180">Der Benutzer kann dieses Feld bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="03645-180">The user can edit this field.</span></span> <span data-ttu-id="03645-181">Wenn ein Istwert für Zeit und Material auf diese Vertragszeile für Zeit und Material verweist, wird der Betrag auf dem Istwert anhand der nicht zu überschreitenden Grenze in der Vertragszeile bewertet.</span><span class="sxs-lookup"><span data-stu-id="03645-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="03645-182">Diese Bewertung wird abgeschlossen, nachdem die bereits ausgegebenen und zugesagten Beträge berücksichtigt wurden.</span><span class="sxs-lookup"><span data-stu-id="03645-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="03645-183">**Kundenbudget**</span><span class="sxs-lookup"><span data-stu-id="03645-183">**Customer Budget**</span></span> | <span data-ttu-id="03645-184">Dieses Feld kann bearbeitet werden und wird aus dem entsprechenden Feld der Angebotszeile kopiert, wenn der Vertrag aus einem Angebot erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="03645-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="03645-185">Dieses Feld wird nur zur Information verwendet und hat keine nachgelagerte Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="03645-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="03645-186">Validierungsregeln für die Optionen auf der Registerkarte „Allgemein“ der projektbasierten Vertragszeilen</span><span class="sxs-lookup"><span data-stu-id="03645-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="03645-187">Regel 1: Wenn das **Enthaltene Aufgaben**-Feld leer oder auf **Alle Projektaufgaben** gesetzt ist, sind alle Aufgaben des Projekts in der Vertragszeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="03645-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="03645-188">Regel 2: Wenn das **Enthaltene Aufgaben**-Feld leer oder explizit auf **Alle Projektaufgaben** gesetzt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Vertragszeile eines Vertrags enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="03645-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="03645-189">Regel 3: Wenn das **Enthaltene Aufgaben**-Feld leer oder explizit auf **Nur ausgewählte Projektaufgaben** gesetzt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Vertragszeilen eines Vertrags enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="03645-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="03645-190">
                    <strong>Vertrag</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="03645-191">
                    <strong>Vertragszeile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="03645-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="03645-193">
                    <strong>Eingeschlossene Aufgaben</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="03645-194">
                    <strong>Zeit einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="03645-195">
                    <strong>Ausgaben einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="03645-196">
                    <strong>Materialien einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="03645-197">
                    <strong>Einschließen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="03645-198">
                    <strong>Gebühr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="03645-199">
                    <strong>Gültig/Nicht gültig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="03645-200">
                    <strong>Grund</strong>
                </span><span class="sxs-lookup"><span data-stu-id="03645-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-201">C1</span><span class="sxs-lookup"><span data-stu-id="03645-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-202">CL1</span><span class="sxs-lookup"><span data-stu-id="03645-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-203">P1</span><span class="sxs-lookup"><span data-stu-id="03645-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-204">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-205">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-206">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-207">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-208">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-209">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="03645-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-210">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="03645-210">Violation of Rule #2.</span></span> <span data-ttu-id="03645-211">Zeit, Kosten und Materialien für das P1-Projekt sind in den Vertragszeilen CL1 und CL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="03645-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-212">C1</span><span class="sxs-lookup"><span data-stu-id="03645-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-213">CL2</span><span class="sxs-lookup"><span data-stu-id="03645-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-214">P1</span><span class="sxs-lookup"><span data-stu-id="03645-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-215">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-216">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-217">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-218">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-219">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-220">C1</span><span class="sxs-lookup"><span data-stu-id="03645-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-221">CL1</span><span class="sxs-lookup"><span data-stu-id="03645-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-222">P1</span><span class="sxs-lookup"><span data-stu-id="03645-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-223">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-224">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-225">Nr.</span><span class="sxs-lookup"><span data-stu-id="03645-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-226">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-227">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-228">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="03645-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-229">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="03645-229">Violation of Rule #2.</span></span> <span data-ttu-id="03645-230">Zeit, Materialien und Gebühren für das P1-Projekt sind in den Vertragszeilen CL1 und CL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="03645-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-231">C1</span><span class="sxs-lookup"><span data-stu-id="03645-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-232">CL2</span><span class="sxs-lookup"><span data-stu-id="03645-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-233">P1</span><span class="sxs-lookup"><span data-stu-id="03645-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-234">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-235">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-236">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-237">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-238">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-239">C1</span><span class="sxs-lookup"><span data-stu-id="03645-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-240">CL1</span><span class="sxs-lookup"><span data-stu-id="03645-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-241">P1</span><span class="sxs-lookup"><span data-stu-id="03645-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-242">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-243">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-244">Nr.</span><span class="sxs-lookup"><span data-stu-id="03645-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-245">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-246">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-247">Gültig</span><span class="sxs-lookup"><span data-stu-id="03645-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-248">Zeit, Materialien und Gebühren für das P1-Projekt sind in CL1 enthalten.</span><span class="sxs-lookup"><span data-stu-id="03645-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="03645-249">Die Kosten für das P1-Projekt sind in CL2 enthalten.</span><span class="sxs-lookup"><span data-stu-id="03645-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="03645-250">Keine Überlappung in dem, was in jeder Vertragszeile enthalten ist und daher gültig ist.</span><span class="sxs-lookup"><span data-stu-id="03645-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-251">C1</span><span class="sxs-lookup"><span data-stu-id="03645-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-252">CL2</span><span class="sxs-lookup"><span data-stu-id="03645-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-253">P1</span><span class="sxs-lookup"><span data-stu-id="03645-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-254">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="03645-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-256">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-257">Nr.</span><span class="sxs-lookup"><span data-stu-id="03645-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-258">Nr.</span><span class="sxs-lookup"><span data-stu-id="03645-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-259">C1</span><span class="sxs-lookup"><span data-stu-id="03645-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-260">CL1</span><span class="sxs-lookup"><span data-stu-id="03645-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-261">P1</span><span class="sxs-lookup"><span data-stu-id="03645-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-262">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="03645-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-263">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-264">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-265">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-266">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-267">Nicht gültig</span><span class="sxs-lookup"><span data-stu-id="03645-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-268">Verstoß gegen Regel 2</span><span class="sxs-lookup"><span data-stu-id="03645-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="03645-269">C1 umfasst Zeit, Materialien, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="03645-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="03645-270">CL2 enthält Zeit, Materialien, Ausgaben und Gebühren für das gesamte Projekt P1 und überschneidet sich daher mit dem, was in C1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="03645-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-271">C1</span><span class="sxs-lookup"><span data-stu-id="03645-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-272">CL2</span><span class="sxs-lookup"><span data-stu-id="03645-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-273">P1</span><span class="sxs-lookup"><span data-stu-id="03645-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-274">Leer</span><span class="sxs-lookup"><span data-stu-id="03645-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-275">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-276">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-277">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-278">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-279">C1</span><span class="sxs-lookup"><span data-stu-id="03645-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-280">CL1</span><span class="sxs-lookup"><span data-stu-id="03645-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-281">P1</span><span class="sxs-lookup"><span data-stu-id="03645-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-282">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="03645-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-283">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-284">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-285">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-286">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-287">Gültig</span><span class="sxs-lookup"><span data-stu-id="03645-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="03645-288">Gemäß Regel 3</span><span class="sxs-lookup"><span data-stu-id="03645-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="03645-289">C1 umfasst Zeit, Ausgaben, Materialien und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="03645-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="03645-290">CL2 umfasst Zeit, Ausgaben, Materialien und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.</span><span class="sxs-lookup"><span data-stu-id="03645-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="03645-291">Die einzige zusätzliche Validierung betrifft die Teilmenge der Aufgaben in CL1, die sich von der Teilmenge der Aufgaben in CL2 unterscheidet, um sicherzustellen, dass es keine Überlappung gibt.</span><span class="sxs-lookup"><span data-stu-id="03645-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="03645-292">Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="03645-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="03645-293">C1</span><span class="sxs-lookup"><span data-stu-id="03645-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="03645-294">CL2</span><span class="sxs-lookup"><span data-stu-id="03645-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-295">P1</span><span class="sxs-lookup"><span data-stu-id="03645-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="03645-296">Nur ausgewählte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="03645-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-297">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="03645-298">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-299">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="03645-300">Ja</span><span class="sxs-lookup"><span data-stu-id="03645-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
