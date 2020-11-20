---
title: Ausgabeneintrag (Lite)
description: Dieses Thema enthält Informationen zum Arbeiten mit Ausgabeneintrag in einer Lite-Bereitstellung.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121082"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="f8ad2-103">Ausgabeneintrag (Lite)</span><span class="sxs-lookup"><span data-stu-id="f8ad2-103">Expense entry (lite)</span></span>

<span data-ttu-id="f8ad2-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="f8ad2-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8ad2-105">Basic oder Lite, die Ausgabenverwaltung ist die Fähigkeit, einfache Ausgaben zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="f8ad2-106">Sie können Ausgaben für ein Projekt erfassen, und der Projektgenehmiger überprüft und genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="f8ad2-107">Weitere Informationen zu den Ausgabefunktionen in Dynamics 365 Project Operations finden Sie unter [Ausgabenübersicht](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8ad2-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="f8ad2-108">Eine Grundausgabe erfassen</span><span class="sxs-lookup"><span data-stu-id="f8ad2-108">Capture a basic expense</span></span>

<span data-ttu-id="f8ad2-109">Sie können Ihre Ausgaben erfassen, um sie dem Genehmigenden vorzulegen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="f8ad2-110">Wechseln Sie zu **Ausgaben** und wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="f8ad2-111">Geben Sie auf der Seite **Neue Ausgabe** die erforderlichen Ausgabeinformationen ein, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="f8ad2-112">Eine Grundausgabe einreichen</span><span class="sxs-lookup"><span data-stu-id="f8ad2-112">Submit a basic expense</span></span>

<span data-ttu-id="f8ad2-113">Nachdem Sie alle Ihre Ausgaben erfasst haben und bereit sind, sie genehmigen zu lassen, müssen Sie sie einreichen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="f8ad2-114">Wechseln Sie zu **Ausgaben** und wählen Sie eine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="f8ad2-115">Oder wählen Sie alle Ausgaben aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="f8ad2-116">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-116">Select **Submit**.</span></span> <span data-ttu-id="f8ad2-117">Das System verarbeitet die ausgewählten Einträge und erstellt dann Kostengenehmigungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="f8ad2-118">Eine Grundausgabe zurückrufen</span><span class="sxs-lookup"><span data-stu-id="f8ad2-118">Recall a basic expense</span></span>

<span data-ttu-id="f8ad2-119">Wenn Sie versehentlich eine Ausgabe einreichen, können Sie diese zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="f8ad2-120">Die Zeit, die erforderlich ist, um eine Ausgabenabrechnung zurückzurufen, hängt von der Genehmigungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="f8ad2-121">Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="f8ad2-122">Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="f8ad2-123">Wechseln Sie zu **Ausgaben** und wählen Sie dann in der Liste der Ausgaben die zurückzurufende Ausgaben aus.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="f8ad2-124">Klicken Sie auf **Zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-124">Select **Recall**.</span></span> <span data-ttu-id="f8ad2-125">Wenn der Ausgabeneintrag noch nicht genehmigt wurde, ruft das System sie sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="f8ad2-126">Wenn der Ausgabeneintrag bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie die Ausgabe stornieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="f8ad2-127">Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="f8ad2-128">Eine Grundausgabe löschen</span><span class="sxs-lookup"><span data-stu-id="f8ad2-128">Delete a basic expense</span></span>

<span data-ttu-id="f8ad2-129">Noch nicht eingereichte Ausgaben können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="f8ad2-130">Um eine bereits eingereichte Ausgabe zu löschen, müssen Sie sie zunächst zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="f8ad2-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8ad2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8ad2-131">See also</span></span>

- [<span data-ttu-id="f8ad2-132">Genehmigungen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="f8ad2-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
