---
title: Ausgabenverwaltungsworkflow
description: In diesem Thema wird erläutert, wie Sie das Workflow-System in Microsoft Dynamics 365 Finance verwenden können, um einen Überprüfungsprozess für Spesenabrechnungen in der Ausgabenverwaltung einzurichten.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076679"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="56bf1-103">Ausgabenverwaltungsworkflow</span><span class="sxs-lookup"><span data-stu-id="56bf1-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56bf1-104">Sie können das Workflow-System verwenden, um einen Überprüfungsprozess für Spesenabrechnungen in der Ausgabenverwaltung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="56bf1-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="56bf1-105">Sie können einen Workflow einrichten, der anhand der folgenden Kriterien ermittelt, wer Spesenabrechnungen genehmigt:</span><span class="sxs-lookup"><span data-stu-id="56bf1-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="56bf1-106">Die Mitarbeiterberichtshierarchie und vordefinierte Genehmigungsgrenzen</span><span class="sxs-lookup"><span data-stu-id="56bf1-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="56bf1-107">Mehrstufige Genehmigung, die vorläufige genehmigende Personen und eine endgültige genehmigende Person unterstützt</span><span class="sxs-lookup"><span data-stu-id="56bf1-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="56bf1-108">Finanzielle Dimensionen und Projektverantwortung</span><span class="sxs-lookup"><span data-stu-id="56bf1-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="56bf1-109">Zuordnung zu bestimmten Benutzern oder Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="56bf1-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="56bf1-110">Workflow-Genehmigungen können für Spesenabrechnungen, Reiseanforderungen, Bargeldvorschüsse und die Erstattung von Mehrwertsteuer (MwSt.) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="56bf1-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="56bf1-111">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="56bf1-111">**Example**</span></span>

<span data-ttu-id="56bf1-112">Der folgende Prozess ist ein Beispiel für den Workflow der Kostenverwaltung für eine Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="56bf1-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="56bf1-113">Ein Mitarbeiter erstellt und speichert eine Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="56bf1-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="56bf1-114">Der Mitarbeiter reicht die Spesenabrechnung zur Genehmigung ein.</span><span class="sxs-lookup"><span data-stu-id="56bf1-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="56bf1-115">Die genehmigende Person wird anhand der Regeln identifiziert, die beim Einrichten des Workflows definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56bf1-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="56bf1-116">Die genehmigende Person erhält eine Benachrichtigung, dass eine Spesenabrechnung zur Genehmigung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="56bf1-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="56bf1-117">Die genehmigende Person überprüft die Spesenabrechnung und stellt sicher, dass die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="56bf1-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="56bf1-118">Die Ausgaben verstoßen nicht gegen Ausgabenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="56bf1-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="56bf1-119">Wenn eine Ausgabe gegen eine Richtlinie verstößt, überprüft die genehmigende Person, ob die Spesenabrechnung eine gültige geschäftliche Begründung enthält.</span><span class="sxs-lookup"><span data-stu-id="56bf1-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="56bf1-120">Elektronische Belege sind der Spesenabrechnung beigefügt.</span><span class="sxs-lookup"><span data-stu-id="56bf1-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="56bf1-121">Die genehmigende Person genehmigt die Spesenabrechnung.</span><span class="sxs-lookup"><span data-stu-id="56bf1-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="56bf1-122">Die Spesenabrechnung wird dem Kreditorenkoordinator zur Buchung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="56bf1-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="56bf1-123">Je nachdem, ob die automatische Buchung konfiguriert ist, wird einer der folgenden Schritte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="56bf1-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="56bf1-124">Wenn die automatische Buchung konfiguriert ist, wird die Spesenabrechnung zur Zahlung verarbeitet und der Status der Spesenabrechnung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="56bf1-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="56bf1-125">Wenn die automatische Buchung nicht konfiguriert ist, überprüft der Kreditorenkoordinator, ob alle Originalbelege übermittelt wurden und ob die Belege mit den Ausgaben in der Spesenabrechnung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56bf1-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="56bf1-126">Alle Steuerkennzeichen, die in der Spesenabrechnung eingegeben wurden, müssen ebenfalls als korrekt überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="56bf1-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="56bf1-127">Nachdem diese Anforderungen überprüft wurden, wird die Spesenabrechnung gebucht.</span><span class="sxs-lookup"><span data-stu-id="56bf1-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="56bf1-128">Nachdem die Spesenabrechnung gebucht wurde, wird die Zahlung für die Spesenabrechnung autorisiert und der Mitarbeiter erhält eine Rückerstattung.</span><span class="sxs-lookup"><span data-stu-id="56bf1-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>