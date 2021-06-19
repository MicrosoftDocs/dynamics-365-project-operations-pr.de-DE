---
title: Spesenabrechnungen und mehrere Genehmiger
description: Dieses Thema enthält Informationen zu Ausgabenabrechnungen, die von mehr als einer Person genehmigt werden müssen.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002055"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="cfd78-103">Spesenabrechnungen und mehrere Genehmiger</span><span class="sxs-lookup"><span data-stu-id="cfd78-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="cfd78-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="cfd78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cfd78-105">Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine eingereichte Ausgabenabrechnung genehmigen.</span><span class="sxs-lookup"><span data-stu-id="cfd78-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="cfd78-106">Wenn Sie den Workflowprozess für die Genehmigung von Spesenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Spesenabrechnungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="cfd78-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="cfd78-107">Beispielsweise können Sie verlangen, dass alle Spesenabrechnungen von zwei verschiedenen Personen genehmigt werden, dem Manager des Mitarbeiters, der den Bericht eingereicht hat, und dem Kreditorenkontenkoordinator.</span><span class="sxs-lookup"><span data-stu-id="cfd78-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="cfd78-108">Wenn Sie mehrere Genehmiger für Spesenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="cfd78-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="cfd78-109">Fügen Sie ein Genehmigungselement mit einem Schritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="cfd78-109">Add one approval element that has one step.</span></span> <span data-ttu-id="cfd78-110">Für den Schritt kann beispielsweise erforderlich sein, dass eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt wird.</span><span class="sxs-lookup"><span data-stu-id="cfd78-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="cfd78-111">Fügen Sie ein Genehmigungselement mit mehreren Schritten hinzu.</span><span class="sxs-lookup"><span data-stu-id="cfd78-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="cfd78-112">Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="cfd78-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="cfd78-113">Der Manager des Mitarbeiters, der die Spesenabrechnung eingereicht hat, genehmigt sie.</span><span class="sxs-lookup"><span data-stu-id="cfd78-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="cfd78-114">Der Kreditorenbuchhalter überprüft die Belege und die Spesenabrechnungsposten.</span><span class="sxs-lookup"><span data-stu-id="cfd78-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="cfd78-115">Der Budgetbesitzer genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="cfd78-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="cfd78-116">Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat.</span><span class="sxs-lookup"><span data-stu-id="cfd78-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="cfd78-117">Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="cfd78-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="cfd78-118">Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="cfd78-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="cfd78-119">Der Budgetinhaber genehmigt die Ausgabenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="cfd78-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]