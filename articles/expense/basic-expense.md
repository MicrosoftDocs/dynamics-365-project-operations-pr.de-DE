---
title: Ausgabeneintrag (Lite)
description: Dieses Thema enthält Informationen zum Arbeiten mit Ausgabeneintrag in einer Lite-Bereitstellung.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276752"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="414c0-103">Ausgabeneintrag (Lite)</span><span class="sxs-lookup"><span data-stu-id="414c0-103">Expense entry (lite)</span></span>

<span data-ttu-id="414c0-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="414c0-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="414c0-105">Basic oder Lite, die Ausgabenverwaltung ist die Fähigkeit, einfache Ausgaben zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="414c0-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="414c0-106">Sie können Ausgaben gegen ein Projekt aufzeichnen, und der Projektgenehmiger wird sie dann überprüfen und genehmigen.</span><span class="sxs-lookup"><span data-stu-id="414c0-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="414c0-107">Weitere Informationen zu Kostenfunktionen in Dynamics 365 Project Operations finden Sie unter [Ausgaben – Übersicht](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="414c0-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="414c0-108">Eine Grundausgabe erfassen</span><span class="sxs-lookup"><span data-stu-id="414c0-108">Capture a basic expense</span></span>

<span data-ttu-id="414c0-109">Sie können Ihre Ausgaben erfassen, um sie dem Genehmigenden vorzulegen.</span><span class="sxs-lookup"><span data-stu-id="414c0-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="414c0-110">Wechseln Sie zu **Ausgaben** und wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="414c0-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="414c0-111">Geben Sie auf der Seite **Neue Ausgabe** die erforderlichen Ausgabeinformationen ein, und wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="414c0-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="414c0-112">Eine Grundausgabe einreichen</span><span class="sxs-lookup"><span data-stu-id="414c0-112">Submit a basic expense</span></span>

<span data-ttu-id="414c0-113">Nachdem Sie alle Ihre Ausgaben erfasst haben und bereit sind, sie genehmigen zu lassen, müssen Sie sie einreichen.</span><span class="sxs-lookup"><span data-stu-id="414c0-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="414c0-114">Wechseln Sie zu **Ausgaben** und wählen Sie eine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="414c0-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="414c0-115">Oder wählen Sie alle Ausgaben aus, indem Sie das Kontrollkästchen in der Kopfzeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="414c0-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="414c0-116">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="414c0-116">Select **Submit**.</span></span> <span data-ttu-id="414c0-117">Das System verarbeitet die ausgewählten Einträge und erstellt dann Kostengenehmigungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="414c0-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="414c0-118">Anlage hinzufügen</span><span class="sxs-lookup"><span data-stu-id="414c0-118">Add an attachment</span></span>

<span data-ttu-id="414c0-119">Möglicherweise müssen Sie dem Genehmigenden zusätzliche Unterlagen zu Ihren Ausgaben vorlegen.</span><span class="sxs-lookup"><span data-stu-id="414c0-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="414c0-120">Sie können eine Quittung in der Zeitleiste der Spesenbuchung anhängen.</span><span class="sxs-lookup"><span data-stu-id="414c0-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="414c0-121">Wählen Sie **Bearbeiten** und im Bereich **Zeitleiste** dann das Büroklammersymbol aus, um Ihre Quittung anzuhängen.</span><span class="sxs-lookup"><span data-stu-id="414c0-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="414c0-122">Eine Grundausgabe zurückrufen</span><span class="sxs-lookup"><span data-stu-id="414c0-122">Recall a basic expense</span></span>

<span data-ttu-id="414c0-123">Wenn Sie versehentlich eine Ausgabe einreichen, können Sie diese zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="414c0-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="414c0-124">Die Zeit, die erforderlich ist, um eine Ausgabenabrechnung zurückzurufen, hängt von der Genehmigungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="414c0-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="414c0-125">Wenn der Genehmigende den Eintrag noch nicht genehmigt hat, kann der Rückruf sofort erfolgen.</span><span class="sxs-lookup"><span data-stu-id="414c0-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="414c0-126">Wenn der Eintrag jedoch bereits genehmigt wurde, wird der Genehmigende gebeten, den Rückruf zu genehmigen und die Transaktionen rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="414c0-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="414c0-127">Wechseln Sie zu **Ausgaben** und wählen Sie dann in der Liste der Ausgaben die zurückzurufende Ausgaben aus.</span><span class="sxs-lookup"><span data-stu-id="414c0-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="414c0-128">Klicken Sie auf **Zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="414c0-128">Select **Recall**.</span></span> <span data-ttu-id="414c0-129">Wenn der Ausgabeneintrag noch nicht genehmigt wurde, ruft das System sie sofort zurück.</span><span class="sxs-lookup"><span data-stu-id="414c0-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="414c0-130">Wenn der Ausgabeneintrag bereits genehmigt wurde, wird eine Rückrufanforderung erstellt, um den Genehmigenden darüber zu informieren, dass Sie die Ausgabe stornieren möchten.</span><span class="sxs-lookup"><span data-stu-id="414c0-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="414c0-131">Der Genehmigende bestätigt dann, dass die Stornierung durchgeführt werden kann, und der Eintrag wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="414c0-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="414c0-132">Eine Grundausgabe löschen</span><span class="sxs-lookup"><span data-stu-id="414c0-132">Delete a basic expense</span></span>

<span data-ttu-id="414c0-133">Noch nicht eingereichte Ausgaben können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="414c0-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="414c0-134">Um eine bereits eingereichte Ausgabe zu löschen, müssen Sie sie zunächst zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="414c0-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="414c0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="414c0-135">See also</span></span>

- [<span data-ttu-id="414c0-136">Genehmigungen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="414c0-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]