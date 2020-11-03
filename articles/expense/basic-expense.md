---
title: Ausgabeneintrag (Lite)
description: Dieses Thema enthält Informationen zum Arbeiten mit Ausgabeneintrag in einer Lite-Bereitstellung.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076408"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="11c3d-103">Ausgabeneintrag (Lite)</span><span class="sxs-lookup"><span data-stu-id="11c3d-103">Expense entry (lite)</span></span>

<span data-ttu-id="11c3d-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="11c3d-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11c3d-105">Basic oder Lite, die Ausgabenverwaltung ist die Fähigkeit, einfache Ausgaben zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="11c3d-106">Sie können Ausgaben für ein Projekt erfassen, und der Projektgenehmiger überprüft und genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="11c3d-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="11c3d-107">Weitere Informationen zu den Ausgabefunktionen in Dynamics 365 Project Operations finden Sie unter [Ausgabenübersicht](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11c3d-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="11c3d-108">Eine Grundausgabe erfassen</span><span class="sxs-lookup"><span data-stu-id="11c3d-108">Capture a basic expense</span></span>

<span data-ttu-id="11c3d-109">Sie können Ihre Ausgaben erfassen, um sie dem Genehmigenden vorzulegen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="11c3d-110">Wechseln Sie zu **Ausgaben** und wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="11c3d-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="11c3d-111">Geben Sie auf der Seite **Neue Ausgabe** die erforderlichen Ausgabeinformationen ein, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="11c3d-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="11c3d-112">Eine Grundausgabe einreichen</span><span class="sxs-lookup"><span data-stu-id="11c3d-112">Submit a basic expense</span></span>

<span data-ttu-id="11c3d-113">Nachdem Sie alle Ihre Ausgaben erfasst haben und bereit sind, sie genehmigen zu lassen, müssen Sie sie einreichen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="11c3d-114">Wechseln Sie zu **Ausgaben** und wählen Sie eine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="11c3d-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="11c3d-115">Oder wählen Sie alle Ausgaben aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="11c3d-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="11c3d-116">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="11c3d-116">Select **Submit**.</span></span> <span data-ttu-id="11c3d-117">Das System verarbeitet die ausgewählten Einträge und erstellt dann Kostengenehmigungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="11c3d-118">Eine Grundausgabe zurückrufen</span><span class="sxs-lookup"><span data-stu-id="11c3d-118">Recall a basic expense</span></span>

<span data-ttu-id="11c3d-119">Wenn Sie versehentlich eine Ausgabe einreichen, können Sie diese zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="11c3d-120">Die Zeit, die erforderlich ist, um eine Ausgabenabrechnung zurückzurufen, hängt von der Genehmigungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="11c3d-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="11c3d-121">Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="11c3d-122">Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="11c3d-123">Wechseln Sie zu **Ausgaben** und wählen Sie dann in der Liste der Ausgaben die zurückzurufende Ausgaben aus.</span><span class="sxs-lookup"><span data-stu-id="11c3d-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="11c3d-124">Klicken Sie auf **Zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="11c3d-124">Select **Recall**.</span></span> <span data-ttu-id="11c3d-125">Wenn der Ausgabeneintrag noch nicht genehmigt wurde, ruft das System sie sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="11c3d-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="11c3d-126">Wenn der Ausgabeneintrag bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie die Ausgabe stornieren möchten.</span><span class="sxs-lookup"><span data-stu-id="11c3d-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="11c3d-127">Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11c3d-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="11c3d-128">Eine Grundausgabe löschen</span><span class="sxs-lookup"><span data-stu-id="11c3d-128">Delete a basic expense</span></span>

<span data-ttu-id="11c3d-129">Noch nicht eingereichte Ausgaben können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="11c3d-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="11c3d-130">Um eine bereits eingereichte Ausgabe zu löschen, müssen Sie sie zunächst zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="11c3d-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="11c3d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c3d-131">See also</span></span>

- [<span data-ttu-id="11c3d-132">Genehmigungen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="11c3d-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
