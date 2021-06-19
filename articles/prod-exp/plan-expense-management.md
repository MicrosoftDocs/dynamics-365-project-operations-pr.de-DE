---
title: Ausgabenverwaltung konfigurieren
description: Dieser Artikel beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses treffen müssen, bevor Sie die Ausgabenverwaltung in Microsoft Dynamics 365 Finance konfigurieren können.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005385"
---
# <a name="configure-expense-management"></a><span data-ttu-id="62132-103">Ausgabenverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="62132-103">Configure expense management</span></span>

<span data-ttu-id="62132-104">Dieses Thema beschreibt die Überlegungen und Entscheidungen, die Sie während des Planungsprozesses treffen müssen, bevor Sie Ihre Ausgabenverwaltung konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="62132-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="62132-105">In der Ausgabenverwaltung können Sie Informationen zu Zahlungsmethoden, Reiseanforderungen, Spesenabrechnungen, Richtlinien usw. speichern.</span><span class="sxs-lookup"><span data-stu-id="62132-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="62132-106">Da viele der Entscheidungen, die Sie bei der Planung Ihrer Konfiguration für die Ausgabenverwaltung treffen, auf der Hierarchie und Finanzstruktur Ihres Unternehmens basieren, müssen Sie sich auf die Planungsdokumente für diese Bereiche beziehen.</span><span class="sxs-lookup"><span data-stu-id="62132-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="62132-107">Intercompany-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62132-107">Intercompany expenses</span></span>

<span data-ttu-id="62132-108">Wenn Sie konzerninterne Ausgaben aktivieren, können juristische Personen und Mitarbeiter im Namen einer anderen juristischen Person Kosten verursachen und Zahlungen von der juristischen Person der Beschäftigung in Ihrer Organisation einziehen.</span><span class="sxs-lookup"><span data-stu-id="62132-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="62132-109">Beispielsweise schließt ein Mitarbeiter der juristischen Person A ein Projekt für die juristische Person B ab, und für das Projekt fallen reisebezogene Kosten an.</span><span class="sxs-lookup"><span data-stu-id="62132-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="62132-110">Wenn konzerninterne Ausgaben aktiviert sind, kann der Mitarbeiter eine Spesenabrechnung einreichen, in der die Ausgaben an die juristische Person B gebucht werden. Die Ausgaben müssen dann von der juristischen Person A bezahlt werden. Wenn Ihre Organisation nicht über mehrere juristische Personen verfügt, müssen Sie dies nicht tun. Es müssen keine konzerninternen Ausgaben aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="62132-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="62132-111">**Entscheidung:** Möchten Sie konzerninterne Ausgaben aktivieren?</span><span class="sxs-lookup"><span data-stu-id="62132-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="62132-112">Finanzverwaltung</span><span class="sxs-lookup"><span data-stu-id="62132-112">Financial management</span></span>

<span data-ttu-id="62132-113">Die Ausgabenverwaltung ist eng in die Finanzverwaltung Ihrer Organisation integriert.</span><span class="sxs-lookup"><span data-stu-id="62132-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="62132-114">Ein Großteil Ihrer Konfiguration für die Ausgabenverwaltung basiert auf den Entscheidungen, die Sie über die Finanzen Ihres Unternehmens getroffen haben.</span><span class="sxs-lookup"><span data-stu-id="62132-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="62132-115">In den folgenden Abschnitten werden die verschiedenen Bereiche beschrieben, die Planung und Entscheidungen erfordern, basierend auf den finanziellen Entscheidungen Ihres Unternehmens und den Anweisungen Ihres Führungsteams.</span><span class="sxs-lookup"><span data-stu-id="62132-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="62132-116">Pro Tag</span><span class="sxs-lookup"><span data-stu-id="62132-116">Per diems</span></span>

<span data-ttu-id="62132-117">Sie müssen die von Ihrer Organisation bereitgestellten Mitarbeiter-Tagessätze definieren.</span><span class="sxs-lookup"><span data-stu-id="62132-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="62132-118">Da Tagessätze normalerweise zur Deckung von Spesen wie für Mahlzeiten, Unterkunft und anderen Nebenkosten verwendet werden, können Sie Regeln erstellen, die Ihr Unternehmen für Tagessätze vorsieht.</span><span class="sxs-lookup"><span data-stu-id="62132-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="62132-119">Die Tagessätze können von der Jahreszeit, dem Reiseziel oder beidem abhängen.</span><span class="sxs-lookup"><span data-stu-id="62132-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="62132-120">Wenn Sie eine Tagessatzregel festlegen, können Sie einen Prozentsatz des Tagessatzes angeben, der einbehalten wird, wenn ein Arbeitnehmer kostenlose Mahlzeiten oder Dienstleistungen erhält.</span><span class="sxs-lookup"><span data-stu-id="62132-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="62132-121">Sie können auch Tagessatzstufen definieren, um eine minimale und maximale Anzahl von Stunden festzulegen, für die der Tagessatz für die Reise eines Arbeitnehmers gelten kann.</span><span class="sxs-lookup"><span data-stu-id="62132-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="62132-122">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-122">**Decisions:**</span></span>

- <span data-ttu-id="62132-123">Standard-Tagessatzregeln für den ersten und letzten Tag:</span><span class="sxs-lookup"><span data-stu-id="62132-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="62132-124">Wie viele Stunden kann ein Mitarbeiter mindestens für einen Tag beanspruchen und trotzdem einen Tagessatz erhalten?</span><span class="sxs-lookup"><span data-stu-id="62132-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="62132-125">Gibt es eine Reduzierung des Betrags, der für Mahlzeiten am ersten und letzten Tag angeboten wird?</span><span class="sxs-lookup"><span data-stu-id="62132-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="62132-126">Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?</span><span class="sxs-lookup"><span data-stu-id="62132-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="62132-127">Gibt es eine Reduzierung des Betrags, der für ein Hotel am ersten und letzten Tag angeboten wird?</span><span class="sxs-lookup"><span data-stu-id="62132-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="62132-128">Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?</span><span class="sxs-lookup"><span data-stu-id="62132-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="62132-129">Gibt es eine Reduzierung des Betrags, der für andere Ausgaben angeboten wird, die am ersten und am letzten Tag anfallen?</span><span class="sxs-lookup"><span data-stu-id="62132-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="62132-130">Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung?</span><span class="sxs-lookup"><span data-stu-id="62132-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="62132-131">Standard-Tagessatzregeln:</span><span class="sxs-lookup"><span data-stu-id="62132-131">Default per diem rules:</span></span>

    - <span data-ttu-id="62132-132">Gibt es für jede Mahlzeit eine prozentuale Ermäßigung des Tagessatzes, wenn die Mahlzeit z. B. kostenlos ist?</span><span class="sxs-lookup"><span data-stu-id="62132-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="62132-133">Wenn es eine Reduzierung gibt, wie hoch ist der Prozentsatz der Reduzierung für jede Mahlzeit?</span><span class="sxs-lookup"><span data-stu-id="62132-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="62132-134">Wird die Reduzierung der Mahlzeiten pro Tag, pro Reise oder anhand der Anzahl der Mahlzeiten pro Tag berechnet?</span><span class="sxs-lookup"><span data-stu-id="62132-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="62132-135">Sollten die Beträge der Tagessätze regelmäßig gerundet oder aufgerundet werden?</span><span class="sxs-lookup"><span data-stu-id="62132-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="62132-136">Werden Tagessätze für einen Zeitraum von 24 Stunden oder an einem Kalendertag berechnet?</span><span class="sxs-lookup"><span data-stu-id="62132-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="62132-137">Tagessatzregeln, die auf dem Standort basieren:</span><span class="sxs-lookup"><span data-stu-id="62132-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="62132-138">Variieren die Tagessätze je nach Standort?</span><span class="sxs-lookup"><span data-stu-id="62132-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="62132-139">Welche Standorte sind enthalten?</span><span class="sxs-lookup"><span data-stu-id="62132-139">What locations are included?</span></span>
    - <span data-ttu-id="62132-140">Wenn die Tagessätze je nach Standort variieren, wird für jeden Standort der prozentuale Betrag für die folgenden Arten von Ausgaben bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="62132-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="62132-141">Mahlzeiten</span><span class="sxs-lookup"><span data-stu-id="62132-141">Meals</span></span>
        - <span data-ttu-id="62132-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="62132-142">Hotel</span></span>
        - <span data-ttu-id="62132-143">Andere Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62132-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="62132-144">Ausgabenverwaltungs-Journale und -Konten</span><span class="sxs-lookup"><span data-stu-id="62132-144">Expense management journals and accounts</span></span>

<span data-ttu-id="62132-145">Für die Ausgabenverwaltung müssen Sie mehrere Journale und Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="62132-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="62132-146">Sie müssen beispielsweise entscheiden, ob dasselbe Konto für Bargeldvorschüsse und Kreditkartenstreitigkeiten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="62132-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="62132-147">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-147">**Decisions:**</span></span>

- <span data-ttu-id="62132-148">In welche Sachkontoerfassung werden genehmigte Spesenabrechnungen gebucht?</span><span class="sxs-lookup"><span data-stu-id="62132-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="62132-149">Welches Konto wird für Bargeldvorschüsse verwendet?</span><span class="sxs-lookup"><span data-stu-id="62132-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="62132-150">Sollten Bargeldvorschüsse sofort gebucht werden?</span><span class="sxs-lookup"><span data-stu-id="62132-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="62132-151">Zahlungsmethoden</span><span class="sxs-lookup"><span data-stu-id="62132-151">Payment methods</span></span>

<span data-ttu-id="62132-152">Wenn Sie Mitarbeitern erlauben, im Namen Ihres Unternehmens Kosten zu verursachen, müssen Sie die Zahlungsmethoden definieren, die Mitarbeiter verwenden dürfen.</span><span class="sxs-lookup"><span data-stu-id="62132-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="62132-153">Zum Beispiel könnten Sie den Mitarbeitern erlauben, Bargeld oder eine Firmenkreditkarte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="62132-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="62132-154">Sie können den Mitarbeitern auch erlauben, persönliche Kreditkarten zu verwenden und ihnen diese Ausgaben dann zurückzuerstatten.</span><span class="sxs-lookup"><span data-stu-id="62132-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="62132-155">Sie müssen die folgenden Entscheidungen für jede Zahlungsmethode treffen, die Sie zulassen.</span><span class="sxs-lookup"><span data-stu-id="62132-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="62132-156">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-156">**Decisions:**</span></span>

- <span data-ttu-id="62132-157">Welche Zahlungsmethoden sind erlaubt?</span><span class="sxs-lookup"><span data-stu-id="62132-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="62132-158">Wer ist für die Kosten der Zahlungsmethode verantwortlich?</span><span class="sxs-lookup"><span data-stu-id="62132-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="62132-159">Gibt es einen Gegenkontotyp?</span><span class="sxs-lookup"><span data-stu-id="62132-159">Is there an offset account type?</span></span> <span data-ttu-id="62132-160">Wenn es einen Gegenkontotyp gibt, um welchen handelt es sich?</span><span class="sxs-lookup"><span data-stu-id="62132-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="62132-161">Wenn es einen Gegenkontotyp gibt, wie lautet das Konto?</span><span class="sxs-lookup"><span data-stu-id="62132-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="62132-162">Wenn es sich bei der Zahlungsmethode um eine Kreditkarte handelt, sollte die Zahlungsmethode nur bei importierten Transaktionen verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="62132-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="62132-163">Ausgabenkategorien und gemeinsame Kategorien</span><span class="sxs-lookup"><span data-stu-id="62132-163">Expense categories and shared categories</span></span>

<span data-ttu-id="62132-164">Wenn Mitarbeiter eine Spesenabrechnung erstellen, muss jede von ihnen erfasste Ausgabe einer Ausgabenkategorie zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="62132-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="62132-165">Ausgabenkategorien werden aus gemeinsam genutzten Kategorien abgeleitet, die von den juristischen Personen in Ihrer Organisation gemeinsam genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="62132-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="62132-166">Diese Kategorien können auch im Projektmanagement und in der Projektbuchhaltung verwendet werden, abhängig von der Art und Weise, wie Ihre Organisation definiert ist.</span><span class="sxs-lookup"><span data-stu-id="62132-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="62132-167">Legen Sie basierend auf der Definition Ihrer Organisation und den Anweisungen des Implementierungsteams fest, ob die in der Ausgabenverwaltung verwendeten Kategorien nur in der Ausgabenverwaltung verwendet werden oder zwischen dem Projektmanagement, der Buchhaltung und der Ausgabenverwaltung gemeinsam genutzt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="62132-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="62132-168">Beachten Sie, dass diese Kategorien zwischen Projekt und Ausgaben oder Projekt und Produktion gemeinsam genutzt werden können, jedoch nicht zwischen Ausgaben und Produktion.</span><span class="sxs-lookup"><span data-stu-id="62132-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="62132-169">Sie müssen für jede Ausgabenkategorie die folgenden Entscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="62132-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="62132-170">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-170">**Decisions:**</span></span>

- <span data-ttu-id="62132-171">Was ist die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="62132-171">What is the expense category?</span></span> <span data-ttu-id="62132-172">Beispiele sind Kategorien für Flüge, Hotel oder Kilometerstand.</span><span class="sxs-lookup"><span data-stu-id="62132-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="62132-173">Kann die Ausgabenkategorie auch im Projektmanagement und in der Buchhaltung verwendet werden?</span><span class="sxs-lookup"><span data-stu-id="62132-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="62132-174">Was ist der Ausgabentyp?</span><span class="sxs-lookup"><span data-stu-id="62132-174">What is the expense type?</span></span>
- <span data-ttu-id="62132-175">Was ist die Standardzahlungsmethode für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="62132-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="62132-176">Müssen Ausgaben in der Ausgabenkategorie aufgelistet werden?</span><span class="sxs-lookup"><span data-stu-id="62132-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="62132-177">Was ist das Haupt-Standardkonto für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="62132-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="62132-178">Was ist die Standard-Artikel-Mehrwertsteuergruppe für die Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="62132-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="62132-179">Sind zusätzliche Zahlungsmethoden für die Ausgabenkategorie zulässig?</span><span class="sxs-lookup"><span data-stu-id="62132-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="62132-180">Welche zusätzlichen Zahlungsmethoden sind zulässig?</span><span class="sxs-lookup"><span data-stu-id="62132-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="62132-181">Gibt es Unterkategorien in dieser Ausgabenkategorie?</span><span class="sxs-lookup"><span data-stu-id="62132-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="62132-182">Falls es Unterkategorien gibt, müssen Sie auch die folgenden Entscheidungen treffen:</span><span class="sxs-lookup"><span data-stu-id="62132-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="62132-183">Sind einige der Unterkategorien von der Steuerrückerstattung ausgeschlossen?</span><span class="sxs-lookup"><span data-stu-id="62132-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="62132-184">Was ist die Artikel-Mehrwertsteuergruppe der Unterkategorien?</span><span class="sxs-lookup"><span data-stu-id="62132-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="62132-185">Wenn die Ausgabenkategorie auch im Projektmanagement und in der Buchhaltung verwendet wird, beantworten Sie die verbleibenden Fragen.</span><span class="sxs-lookup"><span data-stu-id="62132-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="62132-186">Andernfalls können Sie mit dem nächsten Abschnitt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="62132-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="62132-187">Welche Kostenkonten werden für die folgenden Ausgaben verwendet?</span><span class="sxs-lookup"><span data-stu-id="62132-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="62132-188">Kosten</span><span class="sxs-lookup"><span data-stu-id="62132-188">Cost</span></span>
    - <span data-ttu-id="62132-189">Lohnzuweisung</span><span class="sxs-lookup"><span data-stu-id="62132-189">Payroll allocation</span></span>
    - <span data-ttu-id="62132-190">WIP-Einstandswert</span><span class="sxs-lookup"><span data-stu-id="62132-190">WIP-cost value</span></span>
    - <span data-ttu-id="62132-191">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="62132-191">Cost-item</span></span>
    - <span data-ttu-id="62132-192">WIP-Einstandswertelement</span><span class="sxs-lookup"><span data-stu-id="62132-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="62132-193">Antizipierter Verlust</span><span class="sxs-lookup"><span data-stu-id="62132-193">Accrued loss</span></span>
    - <span data-ttu-id="62132-194">WIP - Antizipierter Verlust</span><span class="sxs-lookup"><span data-stu-id="62132-194">WIP-accrued loss</span></span>

- <span data-ttu-id="62132-195">Welche Umsatzkonten werden für Folgendes verwendet?</span><span class="sxs-lookup"><span data-stu-id="62132-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="62132-196">Rechnungsumsatz</span><span class="sxs-lookup"><span data-stu-id="62132-196">Invoiced revenue</span></span>
    - <span data-ttu-id="62132-197">Antizipierter Umsatzerlös - Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="62132-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="62132-198">RIF – Verkaufswert</span><span class="sxs-lookup"><span data-stu-id="62132-198">WIP-sales value</span></span>
    - <span data-ttu-id="62132-199">Antizipierter Umsatzerlös – Produktion</span><span class="sxs-lookup"><span data-stu-id="62132-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="62132-200">RIF – Fertigung</span><span class="sxs-lookup"><span data-stu-id="62132-200">WIP-production</span></span>
    - <span data-ttu-id="62132-201">Antizipierter Umsatzerlös – Gewinn</span><span class="sxs-lookup"><span data-stu-id="62132-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="62132-202">WIP - Gewinn</span><span class="sxs-lookup"><span data-stu-id="62132-202">WIP-profit</span></span>
    - <span data-ttu-id="62132-203">Antizipierter Umsatz - Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="62132-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="62132-204">WIP - Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="62132-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="62132-205">Steuern</span><span class="sxs-lookup"><span data-stu-id="62132-205">Taxes</span></span>

<span data-ttu-id="62132-206">Für kostenbezogene Steuern müssen Sie festlegen, was in den Spesenabrechnungen enthalten oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="62132-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="62132-207">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-207">**Decisions:**</span></span>

- <span data-ttu-id="62132-208">Ist die Umsatzsteuer in den Aufwandsbeträgen enthalten?</span><span class="sxs-lookup"><span data-stu-id="62132-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="62132-209">Sollte die Steuerrückerstattung für Ausgaben ermöglicht werden?</span><span class="sxs-lookup"><span data-stu-id="62132-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="62132-210">Wenn Sie bei der Planung der Finanzbuchhaltung beschlossen haben, die US-Umsatzsteuer und Steuerregeln anzuwenden, können Sie die Steuerrückerstattung für Ausgaben nicht aktivieren.</span><span class="sxs-lookup"><span data-stu-id="62132-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="62132-211">(Um die US-Umsatzsteuer und Steuervorschriften zu verwenden, legen Sie die Option **Mehrwertsteuerregeln anwenden** auf **Ja** fest.)</span><span class="sxs-lookup"><span data-stu-id="62132-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="62132-212">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="62132-212">Policies</span></span>

<span data-ttu-id="62132-213">Durch das Erstellen von Richtlinien für Spesenabrechnungen können Sie Ihrem Unternehmen helfen, Zeit und Geld zu sparen, wenn Mitarbeiter im Namen des Unternehmens Ausgaben tätigen.</span><span class="sxs-lookup"><span data-stu-id="62132-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="62132-214">Richtlinien tragen dazu bei, dass die Mitarbeiter im Budget bleiben, alle erforderlichen Informationen bereitstellen und Geld nur dann ausgeben, wenn sie es benötigen.</span><span class="sxs-lookup"><span data-stu-id="62132-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="62132-215">Sie müssen die folgenden Entscheidungen für jede Spesenabrechnungsrichtlinie und jede von Ihnen erstellte Spesenabrechnungsgenehmigungsrichtlinie treffen.</span><span class="sxs-lookup"><span data-stu-id="62132-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="62132-216">**Entscheidungen:**</span><span class="sxs-lookup"><span data-stu-id="62132-216">**Decisions:**</span></span>

- <span data-ttu-id="62132-217">Wie lautet der Name der Richtlinie?</span><span class="sxs-lookup"><span data-stu-id="62132-217">What is the name of the policy?</span></span>
- <span data-ttu-id="62132-218">Wofür gilt die Ausgabenrichtlinie?</span><span class="sxs-lookup"><span data-stu-id="62132-218">What is the expense policy for?</span></span>
- <span data-ttu-id="62132-219">Wenn Sie zuvor beschlossen haben, konzerninterne Ausgaben zu aktivieren, für welche Unternehmen in Ihrer Organisation gilt diese Richtlinie?</span><span class="sxs-lookup"><span data-stu-id="62132-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="62132-220">Wann tritt die Richtlinie in Kraft?</span><span class="sxs-lookup"><span data-stu-id="62132-220">When does the policy become effective?</span></span>
- <span data-ttu-id="62132-221">Wann läuft die Richtlinie ab?</span><span class="sxs-lookup"><span data-stu-id="62132-221">When does the policy expire?</span></span>
- <span data-ttu-id="62132-222">Wie lautet die Richtlinienregel?</span><span class="sxs-lookup"><span data-stu-id="62132-222">What is the policy rule?</span></span>
- <span data-ttu-id="62132-223">Was ist das Ergebnis der Richtlinienregel?</span><span class="sxs-lookup"><span data-stu-id="62132-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]