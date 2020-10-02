---
title: Spesenabrechnungen und mehrere Genehmiger
description: Dieses Thema enthält Informationen zu Ausgabenabrechnungen, die von mehr als einer Person genehmigt werden müssen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897090"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="48dc3-103">Spesenabrechnungen und mehrere Genehmiger</span><span class="sxs-lookup"><span data-stu-id="48dc3-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="48dc3-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="48dc3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48dc3-105">Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine eingereichte Ausgabenabrechnung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="48dc3-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="48dc3-106">Wenn Sie den Workflowprozess für die Genehmigung von Ausgabenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Ausgabennabrechnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="48dc3-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="48dc3-107">Beispielsweise können Sie verlangen, dass alle Ausgabenabrechnungen von zwei verschiedenen Personen genehmigt werden, dem Manager des Mitarbeiters, der den Bericht eingereicht hat, und dem Kreditorenkoordinator.</span><span class="sxs-lookup"><span data-stu-id="48dc3-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="48dc3-108">Wenn Sie mehrere Genehmiger für Ausgabenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="48dc3-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="48dc3-109">Fügen Sie ein Genehmigungselement mit einem Schritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="48dc3-109">Add one approval element that has one step.</span></span> <span data-ttu-id="48dc3-110">Für den Schritt muss beispielsweise eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="48dc3-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="48dc3-111">Fügen Sie ein Genehmigungselement hinzu, die verschiedene Schritte hat.</span><span class="sxs-lookup"><span data-stu-id="48dc3-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="48dc3-112">Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="48dc3-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="48dc3-113">Der Manager des Mitarbeiters, der die Ausgabenrechnung eingereicht hat, genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="48dc3-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="48dc3-114">Der Kreditorenbuchhalter überprüft die Belege und die Ausgabenabrechnungsposten.</span><span class="sxs-lookup"><span data-stu-id="48dc3-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="48dc3-115">Der Budgetinhaber genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="48dc3-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="48dc3-116">Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat.</span><span class="sxs-lookup"><span data-stu-id="48dc3-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="48dc3-117">Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="48dc3-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="48dc3-118">Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="48dc3-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="48dc3-119">Der Budgetinhaber genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="48dc3-119">The budget owner approves the expense report.</span></span>
