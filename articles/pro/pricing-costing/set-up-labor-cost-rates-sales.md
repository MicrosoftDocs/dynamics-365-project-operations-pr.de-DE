---
title: Einrichten von Arbeitskostensätzen
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen für Arbeit in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66a254ce4e7c7f25ac3ea303b73a01625988b0d9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076435"
---
# <a name="setting-up-labor-cost-rates"></a><span data-ttu-id="2fcb8-103">Einrichten von Arbeitskostensätzen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-103">Setting up labor cost rates</span></span> 

<span data-ttu-id="2fcb8-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="2fcb8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2fcb8-105">Jede Preisliste enthält eine Reihe von Arbeitssätzen (Rollenpreisen), die mit dem Inhalt und der Datumseffektivität der Preisliste übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-105">Each price list has a set of labor rates (role prices) that align with the content and date effectivity of the price list.</span></span>

1. <span data-ttu-id="2fcb8-106">Erstellen Sie eine Preisliste, und wählen Sie auf der Registerkarte **Rollenpreis** im Unterraster **Neue Rolle** aus.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-106">Create a price list and on the **Role Price** tab, in the sub-grid, select **New Role**.</span></span>
2. <span data-ttu-id="2fcb8-107">Wählen Sie auf der Seite **Schnellerfassung** die Rolle und die Organisationseinheit aus.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-107">On the **Quick Create** page, select the role and organization unit.</span></span>
3. <span data-ttu-id="2fcb8-108">Geben Sie alle erforderlichen Feldinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-108">Enter any other required field information.</span></span>

<span data-ttu-id="2fcb8-109">Die folgende Tabelle enthält einige der Felder, die beim Erstellen von Arbeitssätzen auf einer Einstandspreisliste wichtig sind.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-109">The following table includes some of the fields that are important when creating labor rates on a cost price list.</span></span>

| <span data-ttu-id="2fcb8-110">Feld</span><span class="sxs-lookup"><span data-stu-id="2fcb8-110">Field</span></span> | <span data-ttu-id="2fcb8-111">Position</span><span class="sxs-lookup"><span data-stu-id="2fcb8-111">Location</span></span> | <span data-ttu-id="2fcb8-112">Relevanz, Zweck und Anleitung</span><span class="sxs-lookup"><span data-stu-id="2fcb8-112">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="2fcb8-113">Nachgelagerte Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-113">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="2fcb8-114">Rolle</span><span class="sxs-lookup"><span data-stu-id="2fcb8-114">Role</span></span> | <span data-ttu-id="2fcb8-115">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-115">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-116">Wählen Sie die Rolle aus, für die der Kostensatz gilt.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-116">Select the role that the cost rate applies to.</span></span> | <span data-ttu-id="2fcb8-117">Die Rolle in der eingehenden Vorkalkulation oder der Istwerte wird mit dieser Zeile abgeglichen, um die Kosten der Rolle als Standard festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-117">The role on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="2fcb8-118">Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="2fcb8-118">Resourcing Unit</span></span> | <span data-ttu-id="2fcb8-119">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-119">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-120">Wählen Sie die Organisationseinheit oder die Abteilung des Unternehmens aus, von der aus diese Rolle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-120">Select the organizational unit or division of the company from where this role will be used.</span></span> <span data-ttu-id="2fcb8-121">Zum Beispiel ein Entwickler aus der Robotics-Abteilung von Fabrikam India oder ein Entwickler aus der Software-Abteilung von Fabrikam USA.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-121">For example, a developer from the Robotics division of Fabrikam India or a developer from the Software division of Fabrikam USA.</span></span> | <span data-ttu-id="2fcb8-122">Die Ressourcenzuordnungseinheit in der eingehenden Vorkalkulation oder den Istwerten wird mit dieser Zeile abgeglichen, um den Kostensatz der Rolle als Standard festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-122">The resourcing unit on the incoming estimate or actual will be matched against this line to default the cost of the role.</span></span> |
| <span data-ttu-id="2fcb8-123">Preis</span><span class="sxs-lookup"><span data-stu-id="2fcb8-123">Price</span></span> | <span data-ttu-id="2fcb8-124">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-124">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-125">Richten Sie den Kostensatz für die Kombination aus Rolle, Ressourcenzuordnungsunternehmen und Ressourcenzuordnungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-125">Set up the cost rate for the role, resourcing company, and resourcing unit combination.</span></span> <span data-ttu-id="2fcb8-126">Beispielsweise wird für einen Entwickler von Fabrikam India 1.000 INR oder für einen Entwickler aus Fabrikam Kosten von 150 USD berechnet.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-126">For example, a developer from Fabrikam India costs 1000 INR or a developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="2fcb8-127">Der Preis ist der Kostensatz, der standardmäßig auf den Einzelpreis der eingehenden Vorkalkulation oder der tatsächlichen Zeile für die Transaktionsklasse **Zeit** basiert.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-127">The price is the cost rate that defaults on the per unit cost of the incoming estimate or actual line for **Time** transaction class.</span></span> |
| <span data-ttu-id="2fcb8-128">Währung</span><span class="sxs-lookup"><span data-stu-id="2fcb8-128">Currency</span></span> | <span data-ttu-id="2fcb8-129">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-129">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-130">Standardmäßig stammt der Währungswert aus der Währung in der Kopfzeile der Einstandspreisliste, kann jedoch überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-130">By default, the currency value comes from the currency on the header of the cost price list but can be overridden.</span></span> <span data-ttu-id="2fcb8-131">Zum Beispiel wird für einen Entwickler von Fabrikam India 1000 INR berechnet.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-131">For example, a developer from Fabrikam India costs 1000 INR.</span></span> <span data-ttu-id="2fcb8-132">Ein Entwickler aus Fabrikam USA kostet 150 USD.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-132">A developer from Fabrikam USA costs 150 USD.</span></span> | <span data-ttu-id="2fcb8-133">Diese Währung basiert standardmäßig auf dem Einzelpreis der eingehenden Istwert-Zeile der Transaktionsklasse **Zeit**.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-133">This currency defaults on the per unit cost of the incoming actual cost line for the **Time** transaction class.</span></span> <span data-ttu-id="2fcb8-134">Bei einer Projektvorkalkulation wird der Währungswert in die Projektwährung umgerechnet und in der zeitgesteuerten Ansicht der Vorkalkulation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-134">On a project estimate, the currency value is converted to the project currency and shown on the Time-phased view of the estimate.</span></span> |
| <span data-ttu-id="2fcb8-135">Einheitenzeitplan</span><span class="sxs-lookup"><span data-stu-id="2fcb8-135">Unit Schedule</span></span> | <span data-ttu-id="2fcb8-136">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-136">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-137">Der Einheitenzeitplan ist standardmäßig auf Zeit eingestellt und kann für die Rollenpreisentität nicht geändert werden, da er verwendet wird, um Sätze nach Zeiteinheiten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-137">The unit schedule defaults to Time and can't be changed on the Role price entity because it is used express rates by units of time.</span></span> | <span data-ttu-id="2fcb8-138">Dabei gibt es keine nachgelagerten Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-138">There is no downstream impact.</span></span> |
| <span data-ttu-id="2fcb8-139">Einheit</span><span class="sxs-lookup"><span data-stu-id="2fcb8-139">Unit</span></span> | <span data-ttu-id="2fcb8-140">Die Registerkarte **Allgemein** und die **Schnellerfassungs** -Seiten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-140">**General** tab and **Quick Create** pages</span></span> | <span data-ttu-id="2fcb8-141">Standardmäßig stammt dieser Wert aus dem Feld **Zeiteinheit** im Header der Einstandspreisliste.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-141">By default, the value comes from the **Time Unit** field on the header of the cost price list.</span></span> <span data-ttu-id="2fcb8-142">Der Wert kann überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-142">The value can be overridden.</span></span> <span data-ttu-id="2fcb8-143">Zum Beispiel wird für einen Entwickler von Fabrikam India 1.000 INR pro **Tag in Indien** berechnet.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-143">For example, a developer from Fabrikam India costs 1000 INR per **India Day**.</span></span> <span data-ttu-id="2fcb8-144">Ein Entwickler aus Fabrikam USA kostet 150 USD pro **Tag in den USA**.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-144">A developer from Fabrikam USA costs 150 USD per **US Day**.</span></span> | <span data-ttu-id="2fcb8-145">Das System verwendet das Einheitensystem und die Umrechnung in Basiseinheiten, um den Einzelpreis zu berechnen und den Standardpreis pro Einheit für eine eingehende Vorkalkulations- oder Istwertzeile zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-145">The system uses the system of units and conversion in base units to compute a per unit cost to calculate the default price per unit on an incoming estimate or actual line.</span></span> <span data-ttu-id="2fcb8-146">Zum Beispiel entspricht eine Vorkalkulation für die Arbeit eines Entwicklers aus Indien 10 **Tage in Indien** , und die Einheit **Tag in Indien** ist als 10 Stunden definiert.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-146">For example, an estimate is for 10 **India Days** worth of work for a developer from India, and the unit, **India Day** is defined as 10 hours.</span></span> <span data-ttu-id="2fcb8-147">Bei der Kalkulation dieser Vorkalkulationszeile berechnet die Anwendung die Stückkosten für die Vorkalkulation wie folgt: 1000 INR/10 Stunden = 100 INR pro Stunde, die in USD umgerechnet und als Stückkosten auf der Seite **Projektvorkalkulationen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-147">When costing that estimate line, the application calculates the unit cost on the estimate as: 1000 INR/ 10 hours = 100 INR per hour, which is converted into USD and shown as the unit cost on the **Project Estimates** page.</span></span> |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a><span data-ttu-id="2fcb8-148">Verrechnungspreise und Kosten für Ressourcen außerhalb Ihres Geschäftsbereichs oder Ihrer juristischen Person</span><span class="sxs-lookup"><span data-stu-id="2fcb8-148">Transfer pricing and costs for resources outside of your division or legal entity</span></span>

<span data-ttu-id="2fcb8-149">In projektbasierten Unternehmen ist es üblich, Mitarbeiter aus unterschiedlichen legalen Entitäten oder Abteilungen in Projekten einzusetzen.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-149">In project-based companies, it's common to use employees from different legal entities or divisions on projects.</span></span> <span data-ttu-id="2fcb8-150">Ein Projekt kann von einer juristischen Person ausgeführt werden, aber die Mitarbeiter oder Berater, die an dem Projekt arbeiten, können von derselben oder einer anderen juristischen Person stammen, oder es kann eine Kombination aus beiden geben.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-150">A project can be executed by one legal entity, but the employees or consultants that work on the project could come from the same legal entity or from a different one, or there may be a combination of both.</span></span> <span data-ttu-id="2fcb8-151">In Dynamics 365 Project Operations ist die juristische Person, die für die Bereitstellung des Projekts verantwortlich ist, das **zuständige Unternehmen** und die Abteilung, die für die Bereitstellung verantwortlich ist, die **Vertragseinheit**.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-151">In Dynamics 365 Project Operations, the legal entity that owns the delivery of the project is the **Owning Company** and the division that owns the delivery is the **Contracting Unit**.</span></span> <span data-ttu-id="2fcb8-152">Andere juristische Personen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungsunternehmen** und Abteilungen, die Ressourcen bereitstellen, sind die **Ressourcenzuordnungseinheiten**.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-152">Other legal entities that provide resources are the **Resourcing companies** and divisions that provide resources are the **Resourcing Units**.</span></span> <span data-ttu-id="2fcb8-153">In den meisten Ländern müssen Unternehmen sicherstellen, dass die juristische Person oder Abteilung das zuständige Unternehmen und die Vertragseinheit für die Verwendung der Ressourcen belasten.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-153">In most countries, companies are required to ensure that the resourcing legal entity or division, charge the owning company and the contracting unit for the use of resources.</span></span>

<span data-ttu-id="2fcb8-154">Beispielsweise muss die Fabrikam Corporation sicherstellen, dass Fabrikam India-Robotics eine Kostensatzkarte mit Fabrikam US-Robotics oder Fabrikam UK-Robotics ausgehandelt hat.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-154">For example, the Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate card with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="2fcb8-155">Ein Entwickler von Fabrikam India-Robotic berechnet 100 USD bei einer Überlassung an Fabrikam US-Robotics und 150 USD bei Überlassung an Fabrikam U-Robotics.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-155">A developer from Fabrikam India-Robotic charges $100 when lent to Fabrikam US-Robotics and $150 when lent to Fabrikam U-Robotics.</span></span>

### <a name="set-up-costs-for-outside-resources"></a><span data-ttu-id="2fcb8-156">Kosten für externe Ressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-156">Set up costs for outside resources</span></span>

1. <span data-ttu-id="2fcb8-157">Erstellen Sie eine Einstandspreisliste mit der Bezeichnung *Fabrikam US-Robotics-Kostensätze* , und legen Sie einen effektiven Datumsbereich fest.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-157">Create a cost price list called, *Fabrikam US-Robotics cost rates* and set a date effective range.</span></span>
2. <span data-ttu-id="2fcb8-158">Richten Sie in der Einstandspreisliste die Raten anhand der Informationen aus der folgenden Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-158">In the cost price list, set up rates using information from the following table.</span></span> 

| <span data-ttu-id="2fcb8-159">Rolle</span><span class="sxs-lookup"><span data-stu-id="2fcb8-159">Role</span></span> | <span data-ttu-id="2fcb8-160">Ressourcenzuordnungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-160">Resourcing Company</span></span> | <span data-ttu-id="2fcb8-161">Ressourcenzuordnungseinheit</span><span class="sxs-lookup"><span data-stu-id="2fcb8-161">Resourcing Unit</span></span> | <span data-ttu-id="2fcb8-162">Kostenrate</span><span class="sxs-lookup"><span data-stu-id="2fcb8-162">Cost rate</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="2fcb8-163">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-163">Developer</span></span> | <span data-ttu-id="2fcb8-164">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="2fcb8-164">Fabrikam India</span></span> | <span data-ttu-id="2fcb8-165">Fabrikam India-Robotics</span><span class="sxs-lookup"><span data-stu-id="2fcb8-165">Fabrikam India-Robotics</span></span> | <span data-ttu-id="2fcb8-166">100 €</span><span class="sxs-lookup"><span data-stu-id="2fcb8-166">$100</span></span> |
| <span data-ttu-id="2fcb8-167">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-167">Developer</span></span> | <span data-ttu-id="2fcb8-168">Fabrikam Philippinen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-168">Fabrikam Philippines</span></span> | <span data-ttu-id="2fcb8-169">Fabrikam Philippines-Robotics</span><span class="sxs-lookup"><span data-stu-id="2fcb8-169">Fabrikam Philippines-Robotics</span></span> | <span data-ttu-id="2fcb8-170">90 USD</span><span class="sxs-lookup"><span data-stu-id="2fcb8-170">$90</span></span> |
| <span data-ttu-id="2fcb8-171">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-171">Developer</span></span> | <span data-ttu-id="2fcb8-172">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="2fcb8-172">Fabrikam US</span></span> | <span data-ttu-id="2fcb8-173">Fabrikam US-Robotics</span><span class="sxs-lookup"><span data-stu-id="2fcb8-173">Fabrikam US-Robotics</span></span> | <span data-ttu-id="2fcb8-174">150 USD</span><span class="sxs-lookup"><span data-stu-id="2fcb8-174">$150</span></span> |

3. <span data-ttu-id="2fcb8-175">Fügen Sie diese Einstandspreisliste der Organisationseinheit Fabrikam US-Robotics bei.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-175">Attach this cost price list to the Fabrikam US-Robotics organization unit.</span></span>

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a><span data-ttu-id="2fcb8-176">Die Verrechnungspreise für eine Ressource in der entsprechenden Währung einrichten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-176">Set up transfer pricing for a resource in the appropriate currency</span></span> 

<span data-ttu-id="2fcb8-177">In Project Operations kann die Ressourcenpreisgestaltung in einer beliebigen Währung eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-177">In Project Operations, resource pricing can be set up in any currency.</span></span> <span data-ttu-id="2fcb8-178">Die Währung wird standardmäßig im Preislisten-Header verwendet, kann jedoch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-178">The currency defaults to what is on the price list header, but can be changed.</span></span>

<span data-ttu-id="2fcb8-179">Anhand des Beispiels für die Einrichtung des Transferpreises können die Informationen wie folgt geändert werden:</span><span class="sxs-lookup"><span data-stu-id="2fcb8-179">Using the example for transfer price setup, the information could be changed to:</span></span>

<span data-ttu-id="2fcb8-180">Die Fabrikam Corporation muss sicherstellen, dass Fabrikam India-Robotics eine Kostensatzkarte mit Fabrikam US-Robotics oder Fabrikam UK-Robotics ausgehandelt hat.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-180">Fabrikam corporation must ensure that Fabrikam India-Robotics has a negotiated a cost rate with Fabrikam US-Robotics or Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="2fcb8-181">Ein Entwickler von Fabrikam India-Robotics berechnet 5.000 INR bei einer Überlassung an Fabrikam US-Robotics und 5.500 INR bei Überlassung an Fabrikam UK-Robotics.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-181">A developer from Fabrikam India-Robotics costs 5000 INR when lent to Fabrikam US-Robotics and 5500 INR when lent to Fabrikam UK-Robotics.</span></span>

<span data-ttu-id="2fcb8-182">In der Einstandspreisliste für Fabrikam US-Robotics können die Kostensätze wie folgt dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="2fcb8-182">In the cost price list for Fabrikam US-Robotics, cost rates can be expressed as:</span></span>

| <span data-ttu-id="2fcb8-183">Rolle</span><span class="sxs-lookup"><span data-stu-id="2fcb8-183">Role</span></span> | <span data-ttu-id="2fcb8-184">Ressourcenzuordnungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-184">Resourcing Company</span></span> | <span data-ttu-id="2fcb8-185">Kosten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-185">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2fcb8-186">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-186">Developer</span></span> | <span data-ttu-id="2fcb8-187">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="2fcb8-187">Fabrikam India</span></span> | <span data-ttu-id="2fcb8-188">5.000 INR</span><span class="sxs-lookup"><span data-stu-id="2fcb8-188">5000 INR</span></span> |
| <span data-ttu-id="2fcb8-189">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-189">Developer</span></span> | <span data-ttu-id="2fcb8-190">Fabrikam US</span><span class="sxs-lookup"><span data-stu-id="2fcb8-190">Fabrikam US</span></span> | <span data-ttu-id="2fcb8-191">115 USD</span><span class="sxs-lookup"><span data-stu-id="2fcb8-191">115 USD</span></span> |

<span data-ttu-id="2fcb8-192">In der Einstandspreisliste für Fabrikam UK-Robotics können die Kostensätze wie folgt dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="2fcb8-192">In the cost price list for Fabrikam UK-Robotics, cost rates can be expressed below:</span></span>

| <span data-ttu-id="2fcb8-193">Rolle</span><span class="sxs-lookup"><span data-stu-id="2fcb8-193">Role</span></span> | <span data-ttu-id="2fcb8-194">Ressourcenzuordnungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="2fcb8-194">Resourcing company</span></span> | <span data-ttu-id="2fcb8-195">Kosten</span><span class="sxs-lookup"><span data-stu-id="2fcb8-195">Cost</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2fcb8-196">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-196">Developer</span></span> | <span data-ttu-id="2fcb8-197">Fabrikam India</span><span class="sxs-lookup"><span data-stu-id="2fcb8-197">Fabrikam India</span></span> | <span data-ttu-id="2fcb8-198">5.500 INR</span><span class="sxs-lookup"><span data-stu-id="2fcb8-198">5500 INR</span></span> |
| <span data-ttu-id="2fcb8-199">Developer</span><span class="sxs-lookup"><span data-stu-id="2fcb8-199">Developer</span></span> | <span data-ttu-id="2fcb8-200">Fabrikam UK</span><span class="sxs-lookup"><span data-stu-id="2fcb8-200">Fabrikam UK</span></span> | <span data-ttu-id="2fcb8-201">115 GBP</span><span class="sxs-lookup"><span data-stu-id="2fcb8-201">115 GBP</span></span> |

<span data-ttu-id="2fcb8-202">Die Einstandspreisliste kann Arbeitssätze in mehreren Währungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-202">The cost price list can provide labor rates in multiple currencies.</span></span> <span data-ttu-id="2fcb8-203">Bei der Erstellung eines Kostenvoranschlags für das Projekt konvertiert Project Operations diese Kostensätze in die Projektwährung und zeigt sie dem Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-203">When generating a cost estimate on the project, Project Operations will convert these cost rates into the project currency and display it to the user.</span></span> <span data-ttu-id="2fcb8-204">Wenn ein Zeiteintrag genehmigt und ein tatsächlicher Kostenaufwand erstellt wird, werden die tatsächlichen Kosten in der Währung der entsprechenden Preiszeile für die Rolle in der Einstandspreisliste berechnet.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-204">When a time entry is approved and a cost actual is created, the cost actual is priced in the currency of that matching role price line on the cost price list.</span></span> <span data-ttu-id="2fcb8-205">Die tatsächlichen Kosten für die Zeit eines einzelnen Projekts können in mehreren Währungen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-205">Cost actuals for time on a single project can be recorded in multiple currencies.</span></span> <span data-ttu-id="2fcb8-206">Wenn Sie jedoch die tatsächlichen Arbeitskosten auf Projektebene zusammenfassen, konvertiert Project Operations alle Arbeitskostenbeträge in die Projektwährung, die der Benutzer anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="2fcb8-206">However, when rolling up or summarizing the actual labor costs at the project level, Project Operations will convert all labor cost amounts into the project currency that the user can view.</span></span>