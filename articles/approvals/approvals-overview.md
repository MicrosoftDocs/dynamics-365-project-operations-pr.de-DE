---
title: Genehmigungen – Übersicht
description: Dieses Thema bietet Informationen zur Arbeit mit Genehmigungen in Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076384"
---
# <a name="approvals-overview"></a><span data-ttu-id="9ba9c-103">Genehmigungen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="9ba9c-103">Approvals overview</span></span>

<span data-ttu-id="9ba9c-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="9ba9c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9ba9c-105">Zeit- und Kostenübermittlungen durchlaufen einen Genehmigungs-Workflow.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="9ba9c-106">Nachdem die Einträge genehmigt wurden, werden Transaktionen in tatsächlichen Daten erfasst oder die Zeit wird im Zeitplan gebucht.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="9ba9c-107">Genehmigungs-lWorkflow</span><span class="sxs-lookup"><span data-stu-id="9ba9c-107">Approvals workflow</span></span>
<span data-ttu-id="9ba9c-108">Wenn Sie einen Zeit- oder Kosteneintrag erstellen und senden, wird ein Genehmigungseintrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="9ba9c-109">Der Projektgenehmiger oder Ihr Manager überprüft und genehmigt Ihren Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="9ba9c-110">Wenn sich der Eintrag auf ein Projekt bezieht und dessen Genehmigung vorliegt, werden die Ist-Daten erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="9ba9c-111">Dadurch können die Kosten und die Abrechnung nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="9ba9c-112">Einen Eintrag genehmigen</span><span class="sxs-lookup"><span data-stu-id="9ba9c-112">Approve an entry</span></span>
<span data-ttu-id="9ba9c-113">Mit dem **Genehmigungen** -Formular können Sie zwischen verschiedenen Ansichten wechseln, um die verschiedenen Arten von Genehmigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="9ba9c-114">Wechseln Sie zum **Genehmigungen** -Formular und wählen Sie **Ausgaben** , **Zeit** oder **Rückrufe**.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="9ba9c-115">Überprüfen Sie jede Genehmigung und wählen Sie diejenigen aus, die Sie genehmigen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="9ba9c-116">Wählen Sie **Genehmigen** , um die ausgewählten Einträge zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="9ba9c-117">Das System verarbeitet diese Einträge und erstellt Ist-Daten oder eine Buchung.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="9ba9c-118">Einen Eintrag ablehnen</span><span class="sxs-lookup"><span data-stu-id="9ba9c-118">Reject an entry</span></span>
<span data-ttu-id="9ba9c-119">Als Projektgenehmiger müssen Sie möglicherweise einen Eintrag zur Korrektur an einen Benutzer zurücksenden.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="9ba9c-120">Wechseln Sie zum **Genehmigungen** -Formular und wählen Sie den Eintrag aus, den Sie ablehnen möchten.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="9ba9c-121">Wählen **Ablehnen**.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-121">Select **Reject**.</span></span>
3. <span data-ttu-id="9ba9c-122">Optional – Fügen Sie einen Kommentar in den **Ablehnungskommentare** -Dialog ein, um den Benutzer darüber zu informieren, warum der Eintrag abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="9ba9c-123">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-123">Select **OK**.</span></span> <span data-ttu-id="9ba9c-124">Der Eintrag wird an den Benutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="9ba9c-125">Einträge zurückrufen</span><span class="sxs-lookup"><span data-stu-id="9ba9c-125">Recall entries</span></span>
<span data-ttu-id="9ba9c-126">Irgendwann müssen Sie möglicherweise einen übermittelten Eintrag zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="9ba9c-127">Wenn der Eintrag nicht genehmigt wurde, wird er sofort zurückgesandt.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="9ba9c-128">Ein genehmigter Eintrag kann jedoch wesentliche Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="9ba9c-129">Der Projektgenehmiger muss den Rückruf genehmigen, um die Transaktion in Ist-Daten zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="9ba9c-130">Projektgenehmiger angeben</span><span class="sxs-lookup"><span data-stu-id="9ba9c-130">Specify Project approvers</span></span>
<span data-ttu-id="9ba9c-131">Jedes Projekt hat eine Reihe von Projektteammitgliedern.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-131">Each project has a number of project team members.</span></span> <span data-ttu-id="9ba9c-132">Sie können angeben, welche Teammitglieder auch Projektgenehmiger sind.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="9ba9c-133">Wechseln Sie zum **Projekte** -Formular und öffnen Sie das Projekt aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="9ba9c-134">Auf der **Team** -Registerkarte wählen Sie das Teammitglied aus, das als Projektgenehmiger fungieren soll, und wählen Sie dann aus **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="9ba9c-135">Legen Sie das Feld **Projektgenehmiger** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="9ba9c-136">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-136">Select **Save**.</span></span>
5. <span data-ttu-id="9ba9c-137">Wiederholen Sie die Schritte 2 bis 4, um weitere Projektgenehmiger hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="9ba9c-138">Den Manager des Benutzers konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9ba9c-138">Configure the user's manager</span></span>

1. <span data-ttu-id="9ba9c-139">Gehen Sie zu **Einstellungen** > **Sicherheit** > **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="9ba9c-140">Wählen Sie den Benutzer, dem Sie einen Manager zuweisen, und im Bereich **Organisationsinformationen** wählen Sie den Manager aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="9ba9c-141">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="9ba9c-141">Select **Save**.</span></span>

