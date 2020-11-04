---
title: Wichtige Konzepte – Projektverträge
description: Dieses Thema enthält Informationen zu den wichtigen Konzepten von Projektverträgen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4ab43a9de6b27f0f0e9b8cbe6ea8b613ce81e08d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076460"
---
# <a name="key-concepts---project-contracts"></a><span data-ttu-id="f6c99-103">Wichtige Konzepte – Projektverträge</span><span class="sxs-lookup"><span data-stu-id="f6c99-103">Key concepts - Project contracts</span></span>

<span data-ttu-id="f6c99-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="f6c99-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f6c99-105">Dieses Thema stellt wichtige Konzepte vor, die beachtet werden sollten, bevor Sie Projektverträge in Dynamics 365 Project Operations verwenden:</span><span class="sxs-lookup"><span data-stu-id="f6c99-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="owning-company"></a><span data-ttu-id="f6c99-106">Zuständiges Unternehmen</span><span class="sxs-lookup"><span data-stu-id="f6c99-106">Owning Company</span></span>

<span data-ttu-id="f6c99-107">Das zuständige Unternehmen ist die juristischen Person aus dem Modul **Projektmanagement und -buchhaltung** für Project Operations aus Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f6c99-107">The owning company is the legal entity from the **Project management and accounting** module for Project Operations from Dynamics 365 Finance.</span></span> <span data-ttu-id="f6c99-108">Das zuständige Unternehmen repräsentiert die juristische Person, die die Kosten und den Umsatz aus einem Geschäft berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f6c99-108">The owning company represents the legal entity that will account for the cost and revenue that accrues from a deal.</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="f6c99-109">Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="f6c99-109">Contracting Unit</span></span>

<span data-ttu-id="f6c99-110">Die Vertragseinheit repräsentiert die Abteilung oder Praxis, der die Projektbereitstellung gehört.</span><span class="sxs-lookup"><span data-stu-id="f6c99-110">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="f6c99-111">Sie können Ressourcenkosten für jede Vertragseinheit einrichten.</span><span class="sxs-lookup"><span data-stu-id="f6c99-111">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="f6c99-112">Wenn Sie die Ressourcenkosten für eine Ressource angeben, können Sie auch unterschiedliche Kostensätze für Ressourcen einrichten.</span><span class="sxs-lookup"><span data-stu-id="f6c99-112">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="f6c99-113">Diese Vertragseinheit leiht diese Ressourcen von anderen Abteilungen oder Verfahren innerhalb des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="f6c99-113">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="f6c99-114">Die Kostensätze für die Ressourcen werden als Verrechnungspreise, Ausleihe von Ressourcen oder Wechselkurse bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f6c99-114">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="f6c99-115">Wenn Sie die Kostensätze für das Ausleihen von Ressourcen aus anderen Geschäftsbereichen festlegen, verwenden Sie die Währung der ausleihenden Abteilung.</span><span class="sxs-lookup"><span data-stu-id="f6c99-115">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="f6c99-116">Kostenwährung</span><span class="sxs-lookup"><span data-stu-id="f6c99-116">Cost Currency</span></span>

<span data-ttu-id="f6c99-117">Die Kostenwährung ist die Währung, in der die Kosten auf dem Bildschirm gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-117">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="f6c99-118">Diese Währung leitet sich von der Währung ab, die dem Feld **Vertragseinheit** im Vertrag und Projekt beigefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f6c99-118">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="f6c99-119">Kosten können in jeder Währung für ein Projekt protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-119">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="f6c99-120">Es erfolgt jedoch eine Währungsumrechnung aus der Währung, in der die Kosten erfasst wurden, in die Kostenwährung des Projekts, wenn dies auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c99-120">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="f6c99-121">Da die Wechselkurse auf der Common Data Service-(CDS-)Plattform nicht datumsabhängig sein können, können sich die auf dem Bildschirm angezeigten Kostensummen im Laufe der Zeit ändern, wenn Sie die Wechselkurse aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f6c99-121">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="f6c99-122">Die in der Datenbank erfassten Kosten bleiben jedoch unverändert, da die Beträge in der Währung gespeichert werden, in der sie angefallen sind.</span><span class="sxs-lookup"><span data-stu-id="f6c99-122">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="f6c99-123">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="f6c99-123">Sales Currency</span></span>

<span data-ttu-id="f6c99-124">Die Verkaufswährung in Project Operations ist die Währung, in der die geschätzten und tatsächlichen Verkaufsbeträge erfasst und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-124">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="f6c99-125">Die Verkaufswährung ist auch die Währung, in der dem Kunden das Geschäft in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c99-125">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="f6c99-126">Bei einem Projektvertrag wird die Verkaufswährung standardmäßig aus dem Kunden- oder Kontodatensatz übernommen und kann beim Erstellen des Vertrags geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-126">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="f6c99-127">Wenn ein Vertrag durch Schließen eines Angebots als gewonnen erstellt wird, ist die Währung im Vertrag standardmäßig die Währung aus dem Angebot.</span><span class="sxs-lookup"><span data-stu-id="f6c99-127">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="f6c99-128">Wenn Sie einen Projektvertrag von Grund auf neu erstellen, kann das Feld **Verkaufswährung** nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-128">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="f6c99-129">Produkt- und Projektpreislisten basieren standardmäßig auf dieser Währung im Vertrag.</span><span class="sxs-lookup"><span data-stu-id="f6c99-129">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="f6c99-130">Im Gegensatz zu Kosten können Verkaufswerte nur in der Verkaufswährung erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="f6c99-130">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="f6c99-131">Fakturierungsmethode</span><span class="sxs-lookup"><span data-stu-id="f6c99-131">Billing Method</span></span>

<span data-ttu-id="f6c99-132">Es gibt in der Regel zwei Arten von Vertragsmodellen für Projekte, feste Gebühren und verbrauchsabhängige Kosten.</span><span class="sxs-lookup"><span data-stu-id="f6c99-132">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="f6c99-133">Diese Modelle werden in Project Operations als Fakturierungsmethoden mit zwei möglichen Werten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="f6c99-133">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="f6c99-134">Zeit und Material: Ein verbrauchsabhängiges Vertragsmodell, bei dem alle angefallenen Kosten durch entsprechende Umsätze gedeckt sind.</span><span class="sxs-lookup"><span data-stu-id="f6c99-134">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="f6c99-135">Wenn Sie mehr Kosten schätzen oder verursachen, steigt auch der entsprechende geschätzte und tatsächliche Umsatz.</span><span class="sxs-lookup"><span data-stu-id="f6c99-135">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="f6c99-136">Geben Sie nicht zu überschreitende Grenzwerte in Vertragszeilen ein, die diese Fakturierungsmethode aufweisen, bei der der tatsächliche Umsatz begrenzt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c99-136">Specify not-to-exceed limits on contract lines that have this billing method, which caps off the actual revenue.</span></span> <span data-ttu-id="f6c99-137">Der geschätzte Umsatz wird nicht durch nicht zu überschreitende Grenzwerte beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="f6c99-137">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="f6c99-138">Festpreis: Ein Vertragsmodell mit festen Gebühren, das angibt, dass die Verkaufswerte unabhängig von den angefallenen Kosten sind.</span><span class="sxs-lookup"><span data-stu-id="f6c99-138">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="f6c99-139">Der Verkaufswert ist fest und ändert sich nicht, wenn Sie weitere Kosten schätzen oder verursachen.</span><span class="sxs-lookup"><span data-stu-id="f6c99-139">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="f6c99-140">Projektpreislisten</span><span class="sxs-lookup"><span data-stu-id="f6c99-140">Project Price lists</span></span>

<span data-ttu-id="f6c99-141">Projektpreislisten werden als Standardpreise und nicht als Kostensätze für Zeit, Kosten und andere projektbezogene Komponenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6c99-141">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="f6c99-142">Es kann mehrere Preislisten geben.</span><span class="sxs-lookup"><span data-stu-id="f6c99-142">There can be multiple prices lists.</span></span> <span data-ttu-id="f6c99-143">Jede Preisliste hat für jeden Projektvertrag ein eigenes Datum.</span><span class="sxs-lookup"><span data-stu-id="f6c99-143">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="f6c99-144">Die überlappende Datumseffektivität wird in Projektpreislisten in Project Operations nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6c99-144">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="f6c99-145">Wenn ein Projektvertrag durch den Gewinn eines Projektangebots erstellt wird, werden Projektpreislisten mit dem Vertragsnamen und dem darin enthaltenen Datum kopiert.</span><span class="sxs-lookup"><span data-stu-id="f6c99-145">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="f6c99-146">Das Kopieren dieser Informationen stellt eine benutzerdefinierte Preisgestaltung für Projektkomponenten in diesem Projektvertrag dar.</span><span class="sxs-lookup"><span data-stu-id="f6c99-146">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="f6c99-147">Transaktionsklassen</span><span class="sxs-lookup"><span data-stu-id="f6c99-147">Transaction Classes</span></span>

<span data-ttu-id="f6c99-148">Project Operations unterstützt vier Arten von Transaktionsklassen:</span><span class="sxs-lookup"><span data-stu-id="f6c99-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="f6c99-149">Zeit</span><span class="sxs-lookup"><span data-stu-id="f6c99-149">Time</span></span>
- <span data-ttu-id="f6c99-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6c99-150">Expense</span></span>
- <span data-ttu-id="f6c99-151">Material</span><span class="sxs-lookup"><span data-stu-id="f6c99-151">Material</span></span>
- <span data-ttu-id="f6c99-152">Gebühr</span><span class="sxs-lookup"><span data-stu-id="f6c99-152">Fee</span></span>

<span data-ttu-id="f6c99-153">Kosten- und Verkaufswerte können für die Transaktionsklassen Zeit, Kosten und Material geschätzt werden und anfallen.</span><span class="sxs-lookup"><span data-stu-id="f6c99-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="f6c99-154">Eine Gebühr ist eine reine Umsatzklasse.</span><span class="sxs-lookup"><span data-stu-id="f6c99-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="f6c99-155">Arbeits- und Fakturierungsentitäten</span><span class="sxs-lookup"><span data-stu-id="f6c99-155">Work entities and Billing entities</span></span>

<span data-ttu-id="f6c99-156">Entitäten, die Arbeit darstellen, sind Projekte und Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="f6c99-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="f6c99-157">Entitäten, die Fakturierungsaspekte darstellen, sind Vertragszeilen.</span><span class="sxs-lookup"><span data-stu-id="f6c99-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="f6c99-158">Sie können verschiedene Arbeitsentitäten mit Fakturierungsoptionen verknüpfen, indem Sie sie Vertragszeilen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f6c99-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="f6c99-159">Geschäfte mit mehreren Kunden</span><span class="sxs-lookup"><span data-stu-id="f6c99-159">Multi-customer deals</span></span>

<span data-ttu-id="f6c99-160">Bei Geschäften mit mehreren Kunden gibt es mehr als einen Kunden, dem bei einem Geschäft eine Rechnung gestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f6c99-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="f6c99-161">Hierzu zählen folgende gängige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="f6c99-161">Common examples of this include:</span></span>

- <span data-ttu-id="f6c99-162">OEM-Unternehmen und ihre Partner: Partner und Wiederverkäufer verkaufen ein Produkt mit einigen Mehrwertdiensten, die in der Regel einen bestimmten Vertrag mit einem Kunden beinhalten.</span><span class="sxs-lookup"><span data-stu-id="f6c99-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="f6c99-163">Der OEM bietet an, einen Teil des Projekts zu finanzieren.</span><span class="sxs-lookup"><span data-stu-id="f6c99-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="f6c99-164">Projekte des öffentlichen Sektors: Mehrere Abteilungen einer lokalen Regierung vereinbaren die Finanzierung eines Projekts und werden gemäß einer zuvor vereinbarten Aufteilung in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="f6c99-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="f6c99-165">Beispielsweise vereinbaren ein Schulbezirk oder die lokale Regierungsabteilung, den Bau eines Schwimmbades zu finanzieren.</span><span class="sxs-lookup"><span data-stu-id="f6c99-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="f6c99-166">Rechnungszeitpläne</span><span class="sxs-lookup"><span data-stu-id="f6c99-166">Invoice Schedules</span></span>

<span data-ttu-id="f6c99-167">Rechnungszeitpläne sind für jede Vertragszeile spezifisch und erforderlich, damit die automatische Rechnungsstellung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f6c99-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="f6c99-168">Rechnungszeitpläne werden basierend auf bestimmten Start- und Enddaten und der Rechnungshäufigkeit erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6c99-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="f6c99-169">Die Zeitpläne werden in der Vertragsphase verwendet, wenn der automatische Rechnungserstellungsprozess konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f6c99-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="f6c99-170">Wenn aus einem Angebot ein Projektvertrag erstellt wird, wird der Rechnungszeitplan aus dem Angebot in den Projektvertrag kopiert.</span><span class="sxs-lookup"><span data-stu-id="f6c99-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-dynamics-365-sales-orders"></a><span data-ttu-id="f6c99-171">Änderungen gegenüber dem Dynamics 365 Sales-Auftrag</span><span class="sxs-lookup"><span data-stu-id="f6c99-171">Changes from Dynamics 365 Sales Orders</span></span>

<span data-ttu-id="f6c99-172">Verträge in Project Operations basieren auf Aufträgen in Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f6c99-172">Contracts in Project Operations are built on Orders in Dynamics 365 Sales.</span></span> <span data-ttu-id="f6c99-173">Es gibt jedoch wichtige Abweichungen und Unterschiede in der Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="f6c99-173">However, there are important deviations and differences in functionality.</span></span> <span data-ttu-id="f6c99-174">Verträge haben ihre eigenen Formular- und Benutzeroberflächenelemente, Geschäftsregeln, eine Geschäftslogik in Plug-Ins und clientseitige Skripte, die sie bei Aufträgen einzigartig machen.</span><span class="sxs-lookup"><span data-stu-id="f6c99-174">Contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Orders.</span></span> <span data-ttu-id="f6c99-175">Tauschen Sie aus diesen Gründen einen Verkaufsauftrag nicht gegen einen Project Operations-Vertrag aus.</span><span class="sxs-lookup"><span data-stu-id="f6c99-175">For these reasons, don't use a Sales order and Project Operations contract interchangeably.</span></span>