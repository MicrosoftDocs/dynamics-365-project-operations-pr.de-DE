---
title: Stornieren zuvor genehmigter Zeit- bzw. Ausgabeneinträge
description: Dieses Thema enthält Informationen zum Stornieren einer genehmigten Projektzeit- und -Ausgabentransaktion.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150577"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="91a43-103">Stornieren zuvor genehmigter Zeit- bzw. Ausgabeneinträge</span><span class="sxs-lookup"><span data-stu-id="91a43-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="91a43-104">In der aktuellen Version von Dynamics 365 Project Service Automation können Genehmiger Zeit- bzw. Ausgabeneinträge stornieren, die sie zuvor genehmigt haben.</span><span class="sxs-lookup"><span data-stu-id="91a43-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="91a43-105">Stornieren eines zuvor genehmigten Zeit- bzw. Ausgabeneintrags</span><span class="sxs-lookup"><span data-stu-id="91a43-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="91a43-106">Führen Sie die folgenden Schritte aus, um einen zuvor genehmigten Zeit- bzw. Ausgabeneintrag zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="91a43-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="91a43-107">Wechseln Sie zu **Projekte** \> **Meine Arbeit** \> **Genehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="91a43-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="91a43-108">Ändern Sie auf der Listenseite **Genehmigungen** die Ansicht in **Meine letzten Genehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="91a43-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="91a43-109">Eine Liste der zuvor genehmigten Zeit- und Ausgabeneinträge wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91a43-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="91a43-110">Wählen Sie einen oder mehrere Einträge aus, und wählen Sie dann **Genehmigung stornieren** aus.</span><span class="sxs-lookup"><span data-stu-id="91a43-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="91a43-111">Sie erhalten eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="91a43-111">You receive a warning message.</span></span>
4. <span data-ttu-id="91a43-112">Wählen Sie **OK** aus, um die Genehmigung zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="91a43-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="91a43-113">Grundlegendes zum Stornierens einer Genehmigung für Zeit- oder Ausgabeneinträge</span><span class="sxs-lookup"><span data-stu-id="91a43-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="91a43-114">Das Stornieren einer Genehmigung hat sowohl betriebliche als auch finanzielle Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="91a43-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="91a43-115">Betriebliche Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="91a43-115">Operational impact</span></span>

<span data-ttu-id="91a43-116">Auf der betrieblichen Seite wird der Status des Datensatzes beim Stornieren einer Genehmigung auf **Entwurf** zurückgesetzt, und die Genehmigung wird in der Ansicht **Meine letzten Genehmigungen** nicht mehr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91a43-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="91a43-117">Stattdessen wird die stornierte Genehmigung entweder in der Ansicht **Zeiteinträge zur Genehmigung** oder in der Ansicht **Ausgabeneinträge zur Genehmigung** angezeigt, je nachdem, ob es sich um einen Zeit- oder einen Ausgabeneintrag handelte.</span><span class="sxs-lookup"><span data-stu-id="91a43-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="91a43-118">Darüber hinaus wird der Status des zugehörigen Zeit- bzw. Ausgabeneintrags in **Gesendet** geändert, sodass der zugehörige Eintrag mit Genehmigungen im Status **Entwurf** konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="91a43-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="91a43-119">Als Genehmiger können Sie einige Felder einer Genehmigung bearbeiten, die den Status **Entwurf** aufweist.</span><span class="sxs-lookup"><span data-stu-id="91a43-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="91a43-120">Diese Felder sind **Fakturierungstyp** und **Abrechenbare Stunden für Zeiteinträge**.</span><span class="sxs-lookup"><span data-stu-id="91a43-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="91a43-121">Nachdem Sie Änderungen vorgenommen haben, können Sie den Datensatz erneut genehmigen.</span><span class="sxs-lookup"><span data-stu-id="91a43-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="91a43-122">Alternativ können Sie den Eintrag ablehnen.</span><span class="sxs-lookup"><span data-stu-id="91a43-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="91a43-123">Wenn Sie die Genehmigung eines Zeiteintrags ablehnen, wird der Status des Eintrags in **Zurückgegeben** geändert.</span><span class="sxs-lookup"><span data-stu-id="91a43-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="91a43-124">Wenn Sie die Genehmigung eines Ausgabeneintrags ablehnen, wird der Status des Eintrags in **Abgelehnt** geändert.</span><span class="sxs-lookup"><span data-stu-id="91a43-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="91a43-125">In Bezug auf ihre Funktion verhalten sich sowohl zurückgegebene als auch abgelehnte Einträge wie ein Eintrag mit dem Status **Entwurf**.</span><span class="sxs-lookup"><span data-stu-id="91a43-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="91a43-126">Ein Projektteammitglied kann entweder die erforderlichen Änderungen am Eintrag vornehmen und ihn dann erneut zur Genehmigung einreichen oder den Eintrag vollständig löschen.</span><span class="sxs-lookup"><span data-stu-id="91a43-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="91a43-127">Finanzielle Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="91a43-127">Financial impact</span></span>

<span data-ttu-id="91a43-128">Das Stornieren einer Genehmigung wirkt sich auch finanziell auf das Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="91a43-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="91a43-129">Zunächst werden die entsprechenden Istwerte für Kosten und Vertrieb folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="91a43-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="91a43-130">Der Anpassungsstatus wird auf **Angepasst** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91a43-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="91a43-131">Der Fakturierungsstatus wird auf **Storniert** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91a43-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="91a43-132">Als Nächstes werden Umkehrungseinträge in der Tabelle „Ist-Werte” erstellt.</span><span class="sxs-lookup"><span data-stu-id="91a43-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="91a43-133">Zum Erstellen von Umkehrungseinträgen kopiert das System die Feldwerte aus den ursprünglichen Ist-Werten.</span><span class="sxs-lookup"><span data-stu-id="91a43-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="91a43-134">Die einzigen Werte, die nicht übernommen werden, sind die Mengenwerte.</span><span class="sxs-lookup"><span data-stu-id="91a43-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="91a43-135">Diese Werte werden stattdessen umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="91a43-135">These values are reversed instead.</span></span> <span data-ttu-id="91a43-136">Umgekehrte Ist-Werte werden sowohl für **Kosten** als auch für Ist-Werte von **Nicht fakturierten Umsätzen** erstellt.</span><span class="sxs-lookup"><span data-stu-id="91a43-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="91a43-137">Das Feld **Anpassungsstatus** des umgekehrten Ist-Werts wird auf **Nicht anpassbar** festgelegt, und der Fakturierungsstatus wird auf **Storniert** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="91a43-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="91a43-138">Nachdem diese Änderungen vorgenommen wurden, stellen der Betrag, der als für das Projekt ausgegeben erfasst wurde, und das Umsatz-Rückstandsprotokoll des Projekts nicht mehr die Ist-Werte dar.</span><span class="sxs-lookup"><span data-stu-id="91a43-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
