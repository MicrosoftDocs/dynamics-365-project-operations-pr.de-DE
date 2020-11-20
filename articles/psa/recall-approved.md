---
title: Genehmigte Zeit- oder Ausgabeneinträge zurückrufen
description: Dieses Thema enthält Informationen zum Zurückrufen einer zuvor genehmigten Zeit- oder -Ausgabentransaktion.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120542"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="d5bc6-103">Genehmigte Zeit- oder Ausgabeneinträge zurückrufen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d5bc6-104">Ein Projektteammitglied oder eine andere Person, die einen Zeit- oder Ausgabeneintrag übermittelt, kann selbigen nach der Genehmigung wieder zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="d5bc6-105">Das Zurückrufen eines genehmigten Zeit- oder Ausgabeneintrags umfasst zwei Schritte:</span><span class="sxs-lookup"><span data-stu-id="d5bc6-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="d5bc6-106">Ein Antragsteller fordert einen Rückruf an.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="d5bc6-107">Eine genehmigende Person genehmigt den Rückruf.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="d5bc6-108">Anforderung eines Rückrufs</span><span class="sxs-lookup"><span data-stu-id="d5bc6-108">Request a recall</span></span>

<span data-ttu-id="d5bc6-109">Führen Sie die folgenden Schritte aus, um den Rückruf eines zuvor genehmigten Zeit- bzw. Ausgabeneintrags anzufordern.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="d5bc6-110">Navigieren Sie für Zeiteinträge zu **Projekte** \> **Meine Arbeit** \> **Zeiteintrag**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="d5bc6-111">– oder –</span><span class="sxs-lookup"><span data-stu-id="d5bc6-111">–or–</span></span>

    <span data-ttu-id="d5bc6-112">Navigieren Sie für Ausgabeneinträge zu **Projekte** \> **Meine Arbeit** \> **Ausgaben**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="d5bc6-113">Wählen Sie für Zeiteinträge alle Zeiteinträge für eine bestimmte Kombination aus Projekt und Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="d5bc6-114">Alternativ können Sie im Raster die einzelnen Zellen für die Zeit an einem bestimmten Datum für ein bestimmtes Projekt auswählen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="d5bc6-115">– oder –</span><span class="sxs-lookup"><span data-stu-id="d5bc6-115">–or–</span></span>

    <span data-ttu-id="d5bc6-116">Für Ausgabeneinträge wählen Sie die Zeile für den Ausgabeneintrag aus, der zurückgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="d5bc6-117">Klicken Sie auf **Zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-117">Select **Recall**.</span></span> <span data-ttu-id="d5bc6-118">Ein Bestätigungsdialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="d5bc6-119">Falls die ausgewählten Zeit- und Ausgabeneinträge bereits genehmigt wurden, werden Sie aufgefordert, einen Grund für den Rückruf einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="d5bc6-120">Geben Sie einen Grund für den Rückruf ein und wählen Sie dann **OK** aus, um den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="d5bc6-121">Das System sendet eine Anforderung an die Person, von der die Einträge genehmigt wurden, den Rückruf zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="d5bc6-122">Obwohl genehmigte Zeit- und Ausgabeneinträge zurückgerufen werden können, kann keine Rückrufanforderung erstellt werden, falls eine genehmigte Zeit oder Ausgabe dem Kunden bereits in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="d5bc6-123">Ein Benutzer, der versucht, eine Rückrufanforderung zu erstellen, erhält eine Nachricht, die angibt, dass die Zeit oder Ausgabe nicht zurückgerufen werden kann, da sie bereits in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="d5bc6-124">Genehmigen oder Ablehnen einer Rückrufanforderung</span><span class="sxs-lookup"><span data-stu-id="d5bc6-124">Approve or reject a recall request</span></span>

<span data-ttu-id="d5bc6-125">Führen Sie die folgenden Schritte aus, um eine Rückrufanforderung zu genehmigen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="d5bc6-126">Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="d5bc6-127">Ändern Sie auf der Listenseite **Genehmigungen** die Ansicht zu **Rückrufanforderungen zur Genehmigung**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="d5bc6-128">Eine Liste der übermittelten Rückrufanforderungen wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="d5bc6-129">Wählen Sie einen oder mehrere Einträge aus und wählen Sie dann **Genehmigen** oder **Ablehnen** aus.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="d5bc6-130">Wenn Sie **Genehmigen** ausgewählt haben, erhalten Sie eine Warnmeldung, in der die Auswirkungen der Genehmigung erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="d5bc6-131">Wählen Sie **OK** aus, um den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="d5bc6-132">Die Rückrufanforderung wird genehmigt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-132">The recall request is approved.</span></span>

    <span data-ttu-id="d5bc6-133">– oder –</span><span class="sxs-lookup"><span data-stu-id="d5bc6-133">–or–</span></span>

    <span data-ttu-id="d5bc6-134">Wenn Sie **Ablehnen** ausgewählt haben, wird die Rückrufanforderung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="d5bc6-135">Wie bei einer Rückrufanforderung prüft das System auch bei der Genehmigung eines Rückrufs, ob für die Zeit- oder Ausgabeneinträge bereits Rechnungen gestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="d5bc6-136">Wenn ein Eintrag bereits in Rechnung gestellt wurde oder sich auf einem Rechnungsentwurf befindet, erhält die genehmigende Person eine Fehlermeldung, dass für die Zeit oder Ausgabe kein Rückruf genehmigt werden können, da sie bereits in Rechnung gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="d5bc6-137">Auswirkungen einer Rückrufanforderung</span><span class="sxs-lookup"><span data-stu-id="d5bc6-137">Impact of a recall request</span></span>

<span data-ttu-id="d5bc6-138">Das Zurückrufen einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="d5bc6-139">Betriebliche Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-139">Operational impact</span></span>

<span data-ttu-id="d5bc6-140">Wenn eine Rückrufanforderung genehmigt wird, wird der Genehmigungsdatensatz als **Abgelehnt** markiert.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="d5bc6-141">Der Status des Eintrags wird entweder in **Zurückgegeben** oder in **Abgelehnt** geändert, je nachdem, ob es sich um einen Zeiteintrag oder einen Ausgabeneintrag handelt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="d5bc6-142">Das Projektteammitglied kann Einträge anzeigen, bearbeiten, erneut senden oder vollständig löschen.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="d5bc6-143">Wenn eine Rückrufanforderung abgelehnt wird, behält der Eintrag den Status **Genehmigt** und kann vom Projektteammitglied oder der genehmigenden Person für das Projekt nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="d5bc6-144">Finanzielle Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-144">Financial impact</span></span>

<span data-ttu-id="d5bc6-145">Wenn eine Rückrufanforderung genehmigt wird, werden zunächst die entsprechenden Istwerte für Kosten und Vertrieb folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="d5bc6-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="d5bc6-146">Das Feld **Anpassungsstatus** wird zu **Angepasst** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="d5bc6-147">Das Feld **Fakturierungsstatus** wird zu **Storniert** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="d5bc6-148">Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte” erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="d5bc6-149">Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="d5bc6-150">Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="d5bc6-151">Diese Werte werden stattdessen umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-151">These values are reversed instead.</span></span> <span data-ttu-id="d5bc6-152">Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="d5bc6-153">Das Feld **Anpassungsstatus** der umgekehrten Ist-Werte wird auf **Nicht anpassbar** festgelegt und das Feld **Fakturierungsstatus** auf **Storniert**.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="d5bc6-154">Aufgrund dieser Änderungen stellen die erfassten Ausgaben und das Umsatz-Rückstandsprotokoll des Projekts nicht länger die Ist-Werte dar.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="d5bc6-155">Wenn eine Rückrufanforderung abgelehnt wird, hat dies keine finanziellen Auswirkungen auf das Projekt.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="d5bc6-156">Änderungen an Zeiteintragsdatensätzen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-156">Changes to time entry records</span></span>

<span data-ttu-id="d5bc6-157">Die folgende Abbildung zeigt die Änderungen, die für genehmigte Zeiteinträge auftreten, wenn sie zurückgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Statusübergänge für Zeiteinträge](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="d5bc6-159">Änderungen an Ausgabeneintragsdatensätzen</span><span class="sxs-lookup"><span data-stu-id="d5bc6-159">Changes to expense entry records</span></span>

<span data-ttu-id="d5bc6-160">Die folgende Abbildung zeigt die Änderungen, die für genehmigte Ausgabeneinträge auftreten, wenn sie zurückgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5bc6-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Statusübergänge für Ausgabeneinträge](media/ExpenseEntryStateTransitions.png)
