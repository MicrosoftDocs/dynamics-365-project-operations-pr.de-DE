---
title: Erweiterte Verträge für die Abrechnung basierend auf dem Fortschritt erstellen
description: In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Kunden basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076653"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="af16a-103">Erweiterte Verträge für die Abrechnung basierend auf dem Fortschritt erstellen</span><span class="sxs-lookup"><span data-stu-id="af16a-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="af16a-104">In diesem Thema wird erläutert, wie Sie Projektverträge erstellen, damit Sie Rechnungen für Kunden basierend auf einem Prozentsatz der abgeschlossenen Arbeit erstellen können.</span><span class="sxs-lookup"><span data-stu-id="af16a-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="af16a-105">Rechnungsbeträge werden automatisch für die Budgetkategorien der Arbeit berechnet, die Sie für ein Projekt eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="af16a-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="af16a-106">Der Rechnungszeitpunkt wird festgelegt, wenn Sie den Projektvertrag mit dem Kunden aushandeln.</span><span class="sxs-lookup"><span data-stu-id="af16a-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="af16a-107">Verwenden Sie die Verfahren in diesem Thema, um einen Vertrag, ein zugehöriges Projekt und die Fakturierungsregeln einzurichten, mit denen Rechnungsbeträge für die Budgetkategorien der Arbeit berechnet werden, die Sie für das Projekt eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="af16a-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="af16a-108">Nachdem Sie den Vertrag und das Projekt erstellt haben, können Sie die Details des Projekts einrichten.</span><span class="sxs-lookup"><span data-stu-id="af16a-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="af16a-109">Sie können beispielsweise Aktivitäten definieren und dem Projekt Mitarbeiter zuweisen.</span><span class="sxs-lookup"><span data-stu-id="af16a-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="af16a-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="af16a-110">Example</span></span>

<span data-ttu-id="af16a-111">Ihre Organisation ist eine Softwareentwicklungsfirma.</span><span class="sxs-lookup"><span data-stu-id="af16a-111">Your organization is a software development firm.</span></span> <span data-ttu-id="af16a-112">Sie erklären sich damit einverstanden, ein Lohnbuchhaltungspaket für einen Kunden für eine Gesamtgebühr von 20.000 US-Dollar (USD) zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="af16a-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="af16a-113">Ihre Organisation erklärt sich damit einverstanden, dem Kunden eine Rechnung zu stellen, wenn Sie bestimmte Prozentsätze des Projekts abschließen.</span><span class="sxs-lookup"><span data-stu-id="af16a-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="af16a-114">Sie richten die folgenden Projektkategorien für die Arbeit ein, damit Sie sie im Fakturierungsprozess verwenden können:</span><span class="sxs-lookup"><span data-stu-id="af16a-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="af16a-115">Beratung</span><span class="sxs-lookup"><span data-stu-id="af16a-115">Consulting</span></span>
- <span data-ttu-id="af16a-116">Entwurf</span><span class="sxs-lookup"><span data-stu-id="af16a-116">Design</span></span>
- <span data-ttu-id="af16a-117">Installation</span><span class="sxs-lookup"><span data-stu-id="af16a-117">Installation</span></span>

<span data-ttu-id="af16a-118">Sie richten auch Fakturierungsregeln ein, die automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Projektarbeit in jeder Kategorie berechnen.</span><span class="sxs-lookup"><span data-stu-id="af16a-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="af16a-119">Der Budgetmanager erstellt ein Budget für die Projektkategorien.</span><span class="sxs-lookup"><span data-stu-id="af16a-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="af16a-120">Die Menge der abgeschlossenen Arbeit wird automatisch als Prozentsatz der tatsächlichen Arbeit im Vergleich zu den budgetierten Beträgen berechnet.</span><span class="sxs-lookup"><span data-stu-id="af16a-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="af16a-121">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af16a-121">Prerequisites</span></span>

<span data-ttu-id="af16a-122">Bevor Sie ein Projekt erstellen, das Fakturierungsregeln verwendet, müssen Sie die Nummernfolgen für Abrechnungsregeln und ein Gebührenjournal einrichten, mit dem statusbasierte Abrechnungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="af16a-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="af16a-123">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Einrichtung** \> **Projektmanagement- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="af16a-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="af16a-124">Richten Sie auf der Seite **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Nummernsequenzen** die Nummernsequenz ein, die Sie beim Erstellen von Fakturierungsregeln verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="af16a-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="af16a-125">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Journale** \> **Gebühr**.</span><span class="sxs-lookup"><span data-stu-id="af16a-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="af16a-126">Wählen Sie auf der Seite **Gebührenjournal** die Option **Neu** aus, und geben Sie den Journalnamen ein.</span><span class="sxs-lookup"><span data-stu-id="af16a-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="af16a-127">Einen Vertrag für statusbasierte Abrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="af16a-127">Create a contract for progress billings</span></span>

<span data-ttu-id="af16a-128">Verwenden Sie dieses Verfahren, um einen Projektvertrag für ein Festpreisprojekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af16a-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="af16a-129">Sie erstellen eine Projektrechnung, wenn die am Projekt abgeschlossene Arbeit einen bestimmten Prozentsatz erreicht.</span><span class="sxs-lookup"><span data-stu-id="af16a-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="af16a-130">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="af16a-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="af16a-131">Wählen Sie auf der Seite **Projektverträge** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="af16a-132">Legen Sie im Dialogfeld **Neuer Projektvertrag** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="af16a-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="af16a-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="af16a-133">**Name**</span></span>
    - <span data-ttu-id="af16a-134">**Finanzierungstyp**</span><span class="sxs-lookup"><span data-stu-id="af16a-134">**Funding type**</span></span>
    - <span data-ttu-id="af16a-135">**Finanzierungsquelle**</span><span class="sxs-lookup"><span data-stu-id="af16a-135">**Funding source**</span></span>
    - <span data-ttu-id="af16a-136">**Verkaufswährung** – Standardmäßig wird diese Währung für Kundenrechnungen verwendet, die dem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af16a-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="af16a-137">Sie können jedoch die Verkaufswährung auf einer bestimmten Kundenrechnung ändern.</span><span class="sxs-lookup"><span data-stu-id="af16a-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="af16a-138">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="af16a-138">Select **OK**.</span></span> <span data-ttu-id="af16a-139">Die Informationen werden in den Header der Seite **Projektverträge** kopiert.</span><span class="sxs-lookup"><span data-stu-id="af16a-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="af16a-140">Füllen Sie auf der Seite **Projektverträge** den Rest der erforderlichen Informationen für das Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="af16a-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="af16a-141">Ein Projekt für statusbasierte Abrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="af16a-141">Create a project for progress billings</span></span>

<span data-ttu-id="af16a-142">Befolgen Sie diese Schritte, um ein Projekt und alle Teilprojekte zu erstellen, die einem Projektvertrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af16a-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="af16a-143">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="af16a-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="af16a-144">Wählen Sie auf der Seite **Alle Projekte** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="af16a-145">Wählen Sie im Dialogfeld **Neues Projekt** im Feld **Projekttyp** **Zeit und Material** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="af16a-146">Wählen Sie eine Projektgruppe aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-146">Select a project group.</span></span> <span data-ttu-id="af16a-147">Eine Projektgruppe definiert die Buchungsinformationen für die Projekte, die der Gruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="af16a-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="af16a-148">Wählen Sie **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-148">Select **Create project**.</span></span>
6. <span data-ttu-id="af16a-149">Legen Sie nach dem Erstellen des Projekts die Projektphase auf **In Bearbeitung** fest.</span><span class="sxs-lookup"><span data-stu-id="af16a-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="af16a-150">Ein Budget für ein Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="af16a-150">Create a budget for a project</span></span>

<span data-ttu-id="af16a-151">Budgetkategorien werden verwendet, um automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Arbeit für jede Kategorie zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="af16a-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="af16a-152">Befolgen Sie diese Schritte, um Budgetkategorien für die vorkalkulierten Kosten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af16a-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="af16a-153">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Alle Projekte**.</span><span class="sxs-lookup"><span data-stu-id="af16a-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="af16a-154">Wählen Sie auf der Seite **Alle Projekte** aus, und öffnen Sie das gewünschte Projekt.</span><span class="sxs-lookup"><span data-stu-id="af16a-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="af16a-155">Wählen Sie auf der Seite **Projekte** im Aktionsbereich auf der Registerkarte **Plan** in der Gruppe **Budget** die Option **Projektbudget** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="af16a-156">Geben Sie auf der Seite **Projektbudget** die vorkalkulierten Kosten für jede Kategorie im Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="af16a-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="af16a-157">Fakturierungsregeln für statusbasierte Abrechnungen erstellen</span><span class="sxs-lookup"><span data-stu-id="af16a-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="af16a-158">Navigieren Sie zu **Projektmanagement und -buchhaltung** \> **Projekte** \> **Projektverträge**.</span><span class="sxs-lookup"><span data-stu-id="af16a-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="af16a-159">Wählen Sie auf der Seite **Projektverträge** einen Projektvertrag aus, und öffnen Sie diesen.</span><span class="sxs-lookup"><span data-stu-id="af16a-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="af16a-160">Wählen Sie auf der Projektvertragsseite im Inforegister **Fakturierungsregeln** die Option **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="af16a-161">Wählen Sie auf der Seite **Fakturierungsregel** im Feld **Zeilentyp** die Option **Status** aus.</span><span class="sxs-lookup"><span data-stu-id="af16a-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="af16a-162">Geben Sie im Inforegister **Details der Fakturierungsregelpositionen** im Feld **Vertragswert** den Gesamtbetrag des Vertrags ein.</span><span class="sxs-lookup"><span data-stu-id="af16a-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="af16a-163">Wählen Sie im Feld **Kategorie** die Kategorie aus, in die die Gebührentransaktion gebucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="af16a-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="af16a-164">Wählen Sie im Feld **Projekt** das Projekt aus, dass diese Fakturierungsregel verwendet.</span><span class="sxs-lookup"><span data-stu-id="af16a-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="af16a-165">Optional: Weisen Sie weiteren Projekten Fakturierungsregeln zu.</span><span class="sxs-lookup"><span data-stu-id="af16a-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="af16a-166">Wählen Sie im Inforegister **Projekt** im Abschnitt **Verfügbare Projekte** ein Projekt aus. Wählen Sie dann die Schaltfläche mit dem Rechtspfeil aus, um das Projekt dem Abschnitt **Ausgewählte Projekte** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="af16a-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="af16a-167">Optional: Berechnen Sie den Prozentsatz, den der Kunde von Zahlungen auf einer Rechnung einbehält.</span><span class="sxs-lookup"><span data-stu-id="af16a-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="af16a-168">Wählen Sie im Inforegister **Bedingungen für Einbehaltung der Zahlung** die Finanzierungsquelle aus, und geben Sie dann im Feld **Prozentsatz der Einbehaltung** den Prozentsatz der Einbehaltung ein.</span><span class="sxs-lookup"><span data-stu-id="af16a-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="af16a-169">Wiederholen Sie diese Schritte, um zusätzliche Fakturierungsregeln für den Projektvertrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af16a-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
