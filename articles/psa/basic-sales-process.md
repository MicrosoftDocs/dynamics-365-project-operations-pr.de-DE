---
title: Vertriebsprozesse
description: Dieses Thema enthält Informationen zu den grundlegenden Vertriebsprozessen.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f09b30fe6d842faaf896cb97f44b060ec4049213
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076638"
---
# <a name="sales-processes"></a><span data-ttu-id="56a58-103">Vertriebsprozesse</span><span class="sxs-lookup"><span data-stu-id="56a58-103">Sales processes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="56a58-104">Die Vertriebsprozesse, die in einer projektbasierten Organisation verwendet werden, unterscheiden sich von jenen, die in einer produktbasierten Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-104">The sales processes that are used in a project-based organization differ from the sales processes that are used in a product-based organization.</span></span> <span data-ttu-id="56a58-105">Der Grund für diesen Unterschied ist, dass die Vertriebszyklen für projektbasierte Organisationen länger sind und zum Analysieren und Erstellen von Angeboten für jeden Auftrag benutzerdefinierter Schätzungstechniken bedürfen.</span><span class="sxs-lookup"><span data-stu-id="56a58-105">This difference occurs because the sales cycles for project-based organizations are longer and require customized estimation techniques to analyze and create quotes for each deal.</span></span> <span data-ttu-id="56a58-106">Dynamics 365 Project Service Automation verwendet zum Teil die gleichen Funktionen, die im Vertriebsprozess für Dynamics 365 Sales verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-106">Dynamics 365 Project Service Automation uses some of the same functionality that is used in the sales process for Dynamics 365 Sales.</span></span> <span data-ttu-id="56a58-107">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="56a58-107">Here are some examples:</span></span>

- <span data-ttu-id="56a58-108">Eine Lead-Entität wird zur Nachverfolgung des Vertriebsprozesses verwendet.</span><span class="sxs-lookup"><span data-stu-id="56a58-108">A Lead entity is used to track the sales process.</span></span>
- <span data-ttu-id="56a58-109">Qualifizierte Leads werden als Verkaufschancen nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="56a58-109">Qualifying leads are tracked as opportunities.</span></span> <span data-ttu-id="56a58-110">Der Vertriebsprozess kann auch mit einer Verkaufschance beginnen.</span><span class="sxs-lookup"><span data-stu-id="56a58-110">The sales process can also start with opportunity.</span></span>
- <span data-ttu-id="56a58-111">Es wird auf alle zugehörigen Artefakte einer Verkaufschance zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="56a58-111">All related artifacts for an opportunity are accessed.</span></span> <span data-ttu-id="56a58-112">Diese Artefakte umfassen das Vertriebsteam, die Stakeholder, die Wahrscheinlichkeit, die Bewertung, die Vertriebsphasen und Geschäftsprozesse.</span><span class="sxs-lookup"><span data-stu-id="56a58-112">These artifacts include the sales team, stakeholders, probability, rating, sales stages, and business processes.</span></span>
- <span data-ttu-id="56a58-113">Für eine Verkaufschance werden mehrere Angebote erstellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-113">Multiple quotes are created for an opportunity.</span></span>
- <span data-ttu-id="56a58-114">Ein Angebot wird als **Als gewonnen geschlossen** markiert, um einen Vertriebsauftrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-114">A quote is marked **Closed as Won** to create a sales order.</span></span> <span data-ttu-id="56a58-115">In PSA wird der Vertriebsauftrag angepasst und als Projektvertrag bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="56a58-115">In PSA, the sales order is customized and is called a project contract.</span></span>

<span data-ttu-id="56a58-116">Die folgende Abbildung zeigt einen typischen Vertriebsprozess in einer projektbasierten Organisation.</span><span class="sxs-lookup"><span data-stu-id="56a58-116">The following illustration shows a typical sales process in a project-based organization.</span></span>

> ![Vertriebsprozess in einer projektbasierten Organisation](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a><span data-ttu-id="56a58-118">Einschätzung eines Verkaufs</span><span class="sxs-lookup"><span data-stu-id="56a58-118">Estimating a sale</span></span>
<span data-ttu-id="56a58-119">Der Wert eines Verkaufs kann auf der Grundlage von zuvor gelieferten Projekten und der Komplexität von Projekten geschätzt werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-119">The value of a sale can be estimated based on projects that have previously been delivered and the complexity of projects.</span></span> <span data-ttu-id="56a58-120">Für Projekte, bei denen es sich um Erweiterungen von vorherigen Projekten handelt, oder Projekte, bei denen der Zulieferer über hohe Fachkenntnisse verfügt und bekannte Arbeitsvorlagen verwendet werden, können Sie einen einfacheren Schätzungsprozess verwenden.</span><span class="sxs-lookup"><span data-stu-id="56a58-120">For projects that involve extensions to previous projects, or projects where the vendor's expertise is high and well-known work templates are used, you can use a simpler estimation process.</span></span> <span data-ttu-id="56a58-121">Komplexere Projekte haben normalerweise einen längeren Kaufvorgang.</span><span class="sxs-lookup"><span data-stu-id="56a58-121">More complex projects usually have a longer purchase process.</span></span> <span data-ttu-id="56a58-122">Daher gibt es mehr Phasen in der Vertriebsvorkalkulation.</span><span class="sxs-lookup"><span data-stu-id="56a58-122">Therefore, there are more stages in the sales estimation process.</span></span> <span data-ttu-id="56a58-123">Zu Beginn des Prozesses verwendet das Vertriebsteam die Beiträge von Account Managern und Fachleuten (SMEs – Subject Matter Experts), um eine allgemeine Schätzung für jede einzelne angebotene Arbeitskomponente zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-123">Early in the process, the sales team uses the input of account managers and subject matter experts (SMEs) to start to create a high-level estimate for each distinct component of work that is quoted.</span></span> <span data-ttu-id="56a58-124">Diese Arbeitskomponenten werden durch Angebotszeilen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-124">These components of work are represented by quote lines.</span></span> 

<span data-ttu-id="56a58-125">Sie können eine allgemeine Schätzung des Angebots erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-125">You can create a high-level estimate of the quote.</span></span> <span data-ttu-id="56a58-126">Anschließend wird diese allgemeine Schätzung durch eine detailliertere Schätzung ersetzt, die auf einem Projektplan beruht, den Sie mithilfe der standardisierten Projektvorlagen erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-126">Eventually, this high-level estimate will be replaced by a more detailed estimate that is based on a project plan that you create by using the standardized project templates.</span></span> <span data-ttu-id="56a58-127">Mithilfe dieser Vorlagen können Sie einen Zeitplan erstellen und Geldbeträge für das Angebot und seine Komponenten (Angebotszeilen) ermitteln.</span><span class="sxs-lookup"><span data-stu-id="56a58-127">These templates help you build a schedule and determine monetary values on the quote and its components (quote lines).</span></span> 

<span data-ttu-id="56a58-128">Sie können für ein Projekt mehrere Angebote erstellen und sie unter einem Verkaufschancen-Entitätstyp gruppieren.</span><span class="sxs-lookup"><span data-stu-id="56a58-128">You can create multiple quotes for a project and group them under a single opportunity entity type.</span></span> <span data-ttu-id="56a58-129">Schließlich wird eines dieser Angebote als **Als gewonnen geschlossen** markiert, und ein Projektvertrag oder eine Leistungsbeschreibung (SOW, Statement of Work) wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-129">Eventually, one of those quotes is marked **Closed as Won** , and a project contract or statement of work (SOW) is created.</span></span> <span data-ttu-id="56a58-130">Ein Projektvertrag enthält den vertraglich vereinbarten Wert für jede Komponente (Vertragszeile), die vom Kunden zur Lieferung angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="56a58-130">A project contract holds the contracted value for each component (contract line) that is accepted by the customer for delivery.</span></span> <span data-ttu-id="56a58-131">Eine Leistungsbeschreibung wird normalerweise in der Form eines Microsoft Word-Dokuments erstellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-131">An SOW is usually created as a Microsoft Word document.</span></span> <span data-ttu-id="56a58-132">Alle Rechnungen, die dem Kunden im Laufe der Projektlieferung gesendet werden, verweisen auf den Projektvertrag oder die Leistungsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="56a58-132">All invoices that are sent to the customer over the course of the project's delivery reference the project contract or SOW.</span></span>

<span data-ttu-id="56a58-133">Sie können auch andere Angebote unter einem Verkaufschancen-Entitätstyp erstellen oder das System so konfigurieren, dass ein Projektvertrag erstellt wird, wenn ein Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="56a58-133">You can also create alternate quotes under one opportunity entity type or set up the system so that a project contract is created when a quote is won.</span></span> <span data-ttu-id="56a58-134">In diesem Fall können Sie dem Projektvertragsdatensatz ein Word-Dokument anfügen, das die Leistungsbeschreibung darstellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-134">In this case, you can attach a Word document that represents the SOW to the project contract record.</span></span>

![Schließen eines Angebots, um einen Projektvertrag zu erstellen](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a><span data-ttu-id="56a58-136">Konfigurieren des Vertriebsprozesses</span><span class="sxs-lookup"><span data-stu-id="56a58-136">Configuring the sales process</span></span>
<span data-ttu-id="56a58-137">Sie können Geschäftsprozessflüsse (BPFs, Business Process Flows) in Microsoft Dynamics 365 verwenden, um Ihren Vertriebsprozess zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="56a58-137">You can use business process flows (BPFs) in Microsoft Dynamics 365 to configure your sales process.</span></span> <span data-ttu-id="56a58-138">BPFs bieten dem Vertriebspersonal eine intuitive visuelle Sichtschnittstelle, mit der sie Geschäftsabschlüsse durch die für Ihr Unternehmen typischen Phasen vorantreiben können.</span><span class="sxs-lookup"><span data-stu-id="56a58-138">BPFs give your sales staff a guided visual interface that they can use to move deals forward through the stages that are typical for your company.</span></span>

<span data-ttu-id="56a58-139">Beispielsweise verfügt Ihr Unternehmen über die folgenden sechs Phasen im Vertriebsprozess:</span><span class="sxs-lookup"><span data-stu-id="56a58-139">For example, your company might have the following six stages in the sales process:</span></span>

1. <span data-ttu-id="56a58-140">Qualifizieren</span><span class="sxs-lookup"><span data-stu-id="56a58-140">Qualify</span></span>
2. <span data-ttu-id="56a58-141">Schätzung</span><span class="sxs-lookup"><span data-stu-id="56a58-141">Estimate</span></span>
3. <span data-ttu-id="56a58-142">Interne Prüfung</span><span class="sxs-lookup"><span data-stu-id="56a58-142">Internal review</span></span>
4. <span data-ttu-id="56a58-143">Vertrag</span><span class="sxs-lookup"><span data-stu-id="56a58-143">Contract</span></span>
5. <span data-ttu-id="56a58-144">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="56a58-144">Deliver</span></span>
6. <span data-ttu-id="56a58-145">Schließen</span><span class="sxs-lookup"><span data-stu-id="56a58-145">Close</span></span>

<span data-ttu-id="56a58-146">Diese sechs Phasen werden durch Doppelpfeile (\>) dargestellt, die Sie auswählen, um sie in jedem von Ihnen erstellten Verkaufschancen-Entitätstyp zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="56a58-146">These six stages are represented by chevrons (\>) that you select to expand in each opportunity entity type that you create.</span></span>

![Konfigurieren eines Geschäftsprozesses in Dynamics 365](media/basic-guide-3.png)
 
<span data-ttu-id="56a58-148">Ihre Organisation verwendet möglicherweise verschiedene Entitäten zur Darstellung des gleichen Auftrags, wie er sich entwickelt.</span><span class="sxs-lookup"><span data-stu-id="56a58-148">Your organization might use different entities to represent the same deal as it evolves.</span></span> <span data-ttu-id="56a58-149">Zu Beginn des Vertriebsprozesses wird ein Auftrag durch die Verkaufschancenentität dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56a58-149">Early in the sales process, a deal is represented by the Opportunity entity.</span></span> <span data-ttu-id="56a58-150">Im Laufe der Zeit und wenn weitere Details bekannt werden, können Sie allgemeine Schätzungen verwenden, um ein oder mehrere Angebote zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-150">As time passes and more details emerge, you might use high-level estimates to create one or more quotes.</span></span> <span data-ttu-id="56a58-151">Wenn eines dieser Angebote von den internen und kundenseitigen Stakeholdern überprüft wird, stellt die Angebotsentität den Auftrag dar.</span><span class="sxs-lookup"><span data-stu-id="56a58-151">If one of these quotes is reviewed by internal and customer stakeholders, the Quote entity represents the deal.</span></span> <span data-ttu-id="56a58-152">Nachdem der Kunde das Angebot angenommen hat, wird der Auftrag durch einen Projektvertrag oder eine Leistungsbeschreibung repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="56a58-152">After the customer accepts the quote, a project contract or SOW represents the deal.</span></span> <span data-ttu-id="56a58-153">Um dieses Verhalten zu unterstützen, sind BPFs so strukturiert, dass jede Phase des Prozesses mit einer anderen Datenbanktabelle verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="56a58-153">To support this behavior, BPFs are structured so that each stage in the process is linked to a different database table.</span></span>

<span data-ttu-id="56a58-154">Die Phase **Qualifizieren** im Vertriebsprozess kann durch eine Verkaufschancenentität unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-154">The **Qualify** stage in the sales process can be backed by an Opportunity entity.</span></span> <span data-ttu-id="56a58-155">Die Phasen **Schätzung** und **Interne Prüfung** können von einer Angebotsentität unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-155">The **Estimate** and **Internal Review** stages can be backed by a Quote entity.</span></span> <span data-ttu-id="56a58-156">Die Phasen **Vertrag** , **Lieferung** und **Schließen** können über eine Projektvertragsentität unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-156">The **Contract** , **Delivery** , and **Close** stages can be backed by a Project Contract entity.</span></span>

<span data-ttu-id="56a58-157">Beim Vorantreiben der Geschäfte durch die Phasen werden Sie aufgefordert, den entsprechenden Entitätsdatensatz zu erstellen, der Sie durch den Prozess führt und unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56a58-157">As you move deals through the stages, you're prompted to create the appropriate entity record to help and guide you through the process.</span></span> <span data-ttu-id="56a58-158">Die Phasen können bedingt sein.</span><span class="sxs-lookup"><span data-stu-id="56a58-158">The stages can be conditional.</span></span> <span data-ttu-id="56a58-159">Wenn Sie beispielsweise nur dann eine interne Überprüfung eines Angebots benötigen, wenn im Angebot eine benutzerdefinierte Preisliste verwendet wird, können Sie diese Bedingung in der entsprechenden Phase des Geschäftsprozesses konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="56a58-159">For example, if you require an internal review of a quote only if the quote uses a custom price list, you can configure that condition in the appropriate stage of the business process.</span></span> <span data-ttu-id="56a58-160">Die Phase **Interne Prüfung** wird dann nur für Angebote angezeigt, in denen eine benutzerdefinierte Preisliste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56a58-160">The **Internal Review** stage is then shown only for quotes that use a custom price list.</span></span> <span data-ttu-id="56a58-161">Bei allen anderen Geschäftsabschlüssen und Angeboten folgt auf die Phase **Schätzung** die Phase **Vertrag**.</span><span class="sxs-lookup"><span data-stu-id="56a58-161">For all other deals and quotes, the **Estimate** stage is followed by the **Contract** stage.</span></span>

> [!NOTE]
> <span data-ttu-id="56a58-162">PSA bietet spezifische Seiten für die Entitäten Verkaufschance, Angebot, Auftrag und Rechnung.</span><span class="sxs-lookup"><span data-stu-id="56a58-162">PSA has specific pages for the Opportunity, Quote, Order, and Invoice entities.</span></span> <span data-ttu-id="56a58-163">Sie müssen für diese Entitäten mithilfe der Projektinformationsseiten Project Service-Verkaufschancen, Angebote, Aufträge und Rechnungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-163">You must create project service opportunities, quotes, orders, and invoices using the project information pages for these entities.</span></span> <span data-ttu-id="56a58-164">Wenn Sie zum Erstellen eines Datensatzes eine andere Seite verwenden, können Sie den Datensatz nicht über die Seite **Projektinformationen** öffnen.</span><span class="sxs-lookup"><span data-stu-id="56a58-164">If you use another page to create a record, you won't be able to open the record from the **Project Information** page.</span></span> <span data-ttu-id="56a58-165">Wenn Sie einen Datensatz über die Seite **Projektinformationen** öffnen möchten, müssen Sie den Datensatz löschen und über die Seite **Projektinformationen** neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-165">If you want to open a record from the **Project Information** page, you must delete the record and recreate it using the **Project Information** page.</span></span> <span data-ttu-id="56a58-166">Auf der Seite **Projektinformationen** sorgt die Geschäftslogik für jeden dieser Entitätstypen dafür, dass das Feld **Typ** des Datensatzes korrekt festgelegt ist und alle erforderlichen Konzepte ordnungsgemäß initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-166">On the **Project Information** page, business logic for each of these entity types ensures that the **Type** field of the record is set correctly, and all of the mandatory concepts are properly initialized.</span></span>

> ![Projektinformationen für einen neuen Auftrag](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a><span data-ttu-id="56a58-168">Unterschiede zwischen Project Service Automation und Vertrieb</span><span class="sxs-lookup"><span data-stu-id="56a58-168">Differences between Project Service Automation and Sales</span></span>
<span data-ttu-id="56a58-169">Der Vertriebsprozess in PSA nutzt zwar die grundlegenden Funktionen des Vertriebsprozesses in Sales, weist jedoch einige wesentliche Unterschiede auf, da die Geschäftspraktiken projektbasierter Organisationen unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="56a58-169">Although the sales process in PSA uses the basic capabilities of the sales process in Sales, it does have some key differences because of variations in the business practices of project-based organizations.</span></span> <span data-ttu-id="56a58-170">Im Folgenden finden Sie einige Beispiele hierfür:</span><span class="sxs-lookup"><span data-stu-id="56a58-170">Here are some examples:</span></span>

- <span data-ttu-id="56a58-171">**Projektangebote** – In Project Service Automation wird ein Angebot geschlossen, nachdem ein Projektvertrag aus einem Angebot erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="56a58-171">**Project quotes** – In Project Service Automation, a quote is closed after a project contract is created from a quote.</span></span> <span data-ttu-id="56a58-172">In Sales können Sie ein Angebot offen halten, nachdem Sie es gewonnen haben.</span><span class="sxs-lookup"><span data-stu-id="56a58-172">In Sales, you can keep a quote open after you've won it.</span></span> <span data-ttu-id="56a58-173">Der Grund für diesen Unterschied ist, dass eine Übereinstimmung zwischen einem Angebot und einem Projektvertrag für projektbasierte Organisationen besser ist.</span><span class="sxs-lookup"><span data-stu-id="56a58-173">The reason for this difference is that a match between a quote and a project contract is better for project-based organizations.</span></span> 
- <span data-ttu-id="56a58-174">**Aktivierung und Überarbeitungen** – In PSA werden die Aktivierung und Überarbeitung von Projektangeboten nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56a58-174">**Activation and revisions** – In PSA, activation and revisions aren't supported for project quotes.</span></span> <span data-ttu-id="56a58-175">In Sales kann ein Angebot gesperrt werden, um weitere Bearbeitungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="56a58-175">In Sales, a quote can be locked to prevent additional edits.</span></span>
- <span data-ttu-id="56a58-176">**Schließen eines Angebots als verloren oder gewonnen** – Wenn in PSA ein Projektangebot als gewonnen oder verloren geschlossen wird, bleibt die Verkaufschance offen.</span><span class="sxs-lookup"><span data-stu-id="56a58-176">**Closing a quote as lost or won** – In PSA, when a project quote is closed as won or lost, the opportunity remains open.</span></span> <span data-ttu-id="56a58-177">Alle anderen Angebote für die Verkaufschance werden als verloren geschlossen.</span><span class="sxs-lookup"><span data-stu-id="56a58-177">All other quotes on the opportunity are closed as lost.</span></span> <span data-ttu-id="56a58-178">Wenn in Sales ein Angebot als gewonnen oder verloren geschlossen wird, wird der Benutzer aufgefordert, bei der Verkaufschance eine Aktion zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="56a58-178">In Sales, when a quote is closed as won or lost, the user is prompted to take an action on the opportunity.</span></span> <span data-ttu-id="56a58-179">Je nach Benutzereingabe kann die zugrundeliegende Verkaufschance geschlossen oder offen gelassen werden.</span><span class="sxs-lookup"><span data-stu-id="56a58-179">Depending on the user input, the underlying opportunity might be closed or left open.</span></span>

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a><span data-ttu-id="56a58-180">Nachverfolgen von Überarbeitungen von Angeboten und Projektplänen im Verkaufszyklus</span><span class="sxs-lookup"><span data-stu-id="56a58-180">Tracking revisions to quotes and project plans in the sales cycle</span></span>
<span data-ttu-id="56a58-181">In PSA ist es nicht möglich, Überarbeitungen an einem Angebot nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="56a58-181">In PSA, you can't track revisions that are made to a quote.</span></span> <span data-ttu-id="56a58-182">Stattdessen müssen Sie das vorhandene Angebot als **Als verloren geschlossen** markieren und dann ein neues Angebot erstellen.</span><span class="sxs-lookup"><span data-stu-id="56a58-182">Instead, you must mark the existing quote **Closed as Lost** and then create a new quote.</span></span> <span data-ttu-id="56a58-183">Mit PSA können Sie ein Angebot kopieren oder ein projektbasiertes Angebot klonen.</span><span class="sxs-lookup"><span data-stu-id="56a58-183">You can copy a quote or clone a project-based quote by using PSA.</span></span>

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a><span data-ttu-id="56a58-184">Nachverfolgungskommentare und Genehmigungen von Angeboten und Projektverträgen</span><span class="sxs-lookup"><span data-stu-id="56a58-184">Tracking comments and approvals of quotes and project contracts</span></span>
<span data-ttu-id="56a58-185">Sie können die Überprüfung und Genehmigung von Angeboten und Projektverträgen mithilfe der Datensatzpinnwand und Beiträge verwalten.</span><span class="sxs-lookup"><span data-stu-id="56a58-185">You can manage the review and approval of quotes and project contracts by using the record wall and posts.</span></span> <span data-ttu-id="56a58-186">Ihre Organisation kann benutzerdefinierte Workflows und Plug-Ins erstellen, um Benachrichtigungen zu Überprüfungs- und Genehmigungsarbeitselementen zuzuweisen, umzuleiten, zu eskalieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="56a58-186">Your organization can create custom workflows and plug-ins to assign, redirect, escalate, and manage notifications of review and approval work items.</span></span>