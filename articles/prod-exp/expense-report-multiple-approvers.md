---
title: Mehrere genehmigende Personen in einer Spesenabrechnunng
description: Dieses Thema enthält Informationen zu Spesenabrechnungen, die von mehreren Personen genehmigt werden müssen.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005250"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="fe9a7-103">Mehrere genehmigende Personen in einer Spesenabrechnunng</span><span class="sxs-lookup"><span data-stu-id="fe9a7-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="fe9a7-104">Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine Spesenabrechnung genehmigen, die von einem Mitarbeiter eingereicht wurde.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="fe9a7-105">Wenn Sie den Workflowprozess für die Genehmigung von Ausgabenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Ausgabennabrechnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="fe9a7-106">Beispielsweise können Sie verlangen, dass alle Spesenabrechnungen zunächst vom Manager des Mitarbeiters genehmigt werde müssen, der die Abrechnung eingereicht hat, und dann vom Kreditorenkoordinator.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="fe9a7-107">Wenn Sie mehrere Genehmiger für Ausgabenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="fe9a7-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="fe9a7-108">Fügen Sie ein Genehmigungselement mit einem Schritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-108">Add one approval element that has one step.</span></span> <span data-ttu-id="fe9a7-109">Für den Schritt kann beispielsweise erforderlich sein, dass eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="fe9a7-110">Fügen Sie ein Genehmigungselement mit mehreren Schritten hinzu.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="fe9a7-111">Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="fe9a7-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="fe9a7-112">Der Manager des Mitarbeiters, der die Spesenabrechnung eingereicht hat, genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="fe9a7-113">Der Kreditorenbuchhalter überprüft die Belege und die Spesenabrechnungsposten.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="fe9a7-114">Der Budgetbesitzer genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="fe9a7-115">Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="fe9a7-116">Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="fe9a7-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="fe9a7-117">Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="fe9a7-118">Der Budgetinhaber genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="fe9a7-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]