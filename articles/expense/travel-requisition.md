---
title: Reiseanforderungen
description: Dieses Thema enthält Informationen zu Reiseanforderungen.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906168"
---
# <a name="travel-requisitions"></a><span data-ttu-id="4f4e7-103">Reiseanforderungen</span><span class="sxs-lookup"><span data-stu-id="4f4e7-103">Travel requisitions</span></span>

<span data-ttu-id="4f4e7-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="4f4e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4f4e7-105">Eine Reiseanforderung listet die Kosten auf, die zum Zweck der Reise anfallen.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="4f4e7-106">Eine Reiseanforderung wird zur Überprüfung eingereicht und kann zur Autorisierung von Ausgaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="4f4e7-107">Möglicherweise müssen Sie eine Reiseanforderung einreichen, bevor Ihnen Kosten entstehen, die der Organisation in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="4f4e7-108">Diese Anforderung gilt unabhängig davon, ob Sie Ausgaben von einer Unternehmenskreditkarte belasten, Bargeld ausgeben, das Sie aus einem Vorschuss erhalten haben, oder Auslagen, die von der Organisation erstattet werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="4f4e7-109">Reiseanforderungen und -richtlinien können zur Verwaltung der Organisationsausgaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="4f4e7-110">Wenn Ihre Organisation beispielsweise an einem Festpreisprojekt arbeitet, für das Reisen erforderlich sind, müssen die Reisekosten der Teammitglieder des Projekts in das Projektbudget passen.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="4f4e7-111">Durch die Anforderung, dass Reisekosten genehmigt werden müssen, bevor sie anfallen, kann die Organisation dazu beitragen, dass das Projekt innerhalb des Budgets bleibt.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="4f4e7-112">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4f4e7-112">Configuration</span></span> 

<span data-ttu-id="4f4e7-113">Reiseanforderungen können als „obligatorisch“ konfiguriert werden, indem der Parameter „Eine Vorautorisierung der Reise ist obligatorisch“ in den Kostenverwaltungsparametern aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="4f4e7-114">Eine Reiseanforderung erstellen und einreichen</span><span class="sxs-lookup"><span data-stu-id="4f4e7-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="4f4e7-115">Navigieren Sie zu **Meine Ausgaben: Reiseanforderung**, und wählen Sie **Neue Reiseanforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="4f4e7-116">Geben Sie einen Zweck und ein Ziel für die Anforderung ein.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="4f4e7-117">Geben Sie im Feld **Reisebeschreibung** zusätzliche Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="4f4e7-118">Erstellen Sie für jede der erwarteten Ausgaben, z. B. Flug, Mahlzeiten oder Mietwagen, eine Ausgabenposition.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="4f4e7-119">Geben Sie für jede Ausgabe das geschätzte Datum, den geschätzten Betrag und die Währung an.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="4f4e7-120">Wenn Sie die erwarteten Ausgaben hinzugefügt haben, wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="4f4e7-121">Wenn Sie bereit sind, die Reiseanforderung einzureichen, wählen Sie **Workflow** > **Einreichen** aus.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="4f4e7-122">Sie können Ihre genehmigten Reiseanforderungen unter **Meine Ausgaben: Reiseanforderung** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="4f4e7-123">Verfügbare Reiseanforderungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="4f4e7-123">View available travel requisitions</span></span>

<span data-ttu-id="4f4e7-124">Sie können Ihre gesamten Reiseanforderungen unter **Meine Ausgaben: Reiseanforderungen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="4f4e7-125">Reiseanforderungen genehmigen</span><span class="sxs-lookup"><span data-stu-id="4f4e7-125">Approve travel requisitions</span></span>

<span data-ttu-id="4f4e7-126">Wählen Sie die Reiseanforderung aus, die Sie genehmigen möchten, und dann **Workflow** > **Genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="4f4e7-127">Eine Spesenabrechnung mit Ihrer genehmigten Reiseanforderung einreichen</span><span class="sxs-lookup"><span data-stu-id="4f4e7-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="4f4e7-128">Erstellen Sie eine neue Spesenabrechnung, und wählen Sie im Kopf der Spesenabrechnung sowie aus der Liste der genehmigten Reiseanforderungen die Option **Zu Reiseanforderung zuordnen** aus.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="4f4e7-129">Das Feld **Reiseanforderungsbetrag** wird im Spesenabrechnungskopf automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="4f4e7-130">Fügen Sie alle für die Reise anfallenden Kosten hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="4f4e7-131">Wenn das Feld **Vorautorisiert** aktiviert ist, werden der abgestimmte Betrag und der genehmigte Betrag für die jeweilige Ausgabenkategorie aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="4f4e7-132">Wenn Sie eine Spesenabrechnung einer genehmigten Reiseanforderung zuordnen, darf der Transaktionsbetrag nicht größer als der autorisierte Betrag sein.</span><span class="sxs-lookup"><span data-stu-id="4f4e7-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
