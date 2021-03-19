---
title: Workflows für die Ausgabenverwaltung einrichten
description: Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.
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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271622"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="63fc1-103">Workflows für die Ausgabenverwaltung einrichten</span><span class="sxs-lookup"><span data-stu-id="63fc1-103">Set up Expense management workflows</span></span>

<span data-ttu-id="63fc1-104">Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="63fc1-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="63fc1-105">Zu den Belegen, für die Workflows definiert werden können, zählen Spesenabrechnungen, Reiseanforderungen und Vorauszahlungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="63fc1-106">Ein Workflow repräsentiert einen Geschäftsprozess.</span><span class="sxs-lookup"><span data-stu-id="63fc1-106">A workflow represents a business process.</span></span> <span data-ttu-id="63fc1-107">Er definiert, wie ein Beleg durch das System geleitet wird, und zeigt an, wer eine Aufgabe ausführen oder einen Beleg genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="63fc1-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="63fc1-108">Die Verwendung des Workflow-Systems in Ihrer Organisation bietet mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="63fc1-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="63fc1-109">**Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Belege wie Bestellanforderungen und Spesenabrechnungen definieren.</span><span class="sxs-lookup"><span data-stu-id="63fc1-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="63fc1-110">Die Nutzung des Workflowsystems hilft, dass Belege auf konsistente und effiziente Weise verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="63fc1-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="63fc1-111">Prozesstransparenz – Sie können den Status, den Verlauf und die Leistungsmetriken einer bestimmten Workflowinstanz verfolgen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="63fc1-112">Dies hilft Ihnen zu bestimmen, ob Änderungen am Workflow vorgenommen werden sollten, um die Effizienz zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="63fc1-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="63fc1-113">Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste anzeigen, um die ihnen zugewiesenen Workflowaufgaben und Genehmigungen zu sehen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="63fc1-114">**Die Arten von Workflows, die Sie erstellen können**</span><span class="sxs-lookup"><span data-stu-id="63fc1-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="63fc1-115">Die folgende Tabelle enthält die Workflow-Typen, die Sie in **Ausgaben** erstellen können.</span><span class="sxs-lookup"><span data-stu-id="63fc1-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="63fc1-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="63fc1-117"><strong>Verwenden Sie diesen Typ, um</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="63fc1-118"><strong>Ausgabenbericht</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="63fc1-119">Erstellen Sie Genehmigungsworkflows für Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="63fc1-120"><strong>Automatische Ausgabenabrechnungen buchen</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="63fc1-121">Buchen Sie automatisch Workflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="63fc1-122"><strong>Ausgabenzeilenelement</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="63fc1-123">Erstellen Sie Genehmigungsworkflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="63fc1-124"><strong>Automatische Buchung von Ausgaben</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="63fc1-125">Erstellen Sie automatische Buchungsworkflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="63fc1-126"><strong>Reiseanforderung</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="63fc1-127">Erstellen Sie Genehmigungsworkflows für Reiseanforderungen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="63fc1-128"><strong>Vorauskassenanfrage</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="63fc1-129">Erstellen Sie Genehmigungsworkflows für Vorauszahlungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="63fc1-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="63fc1-130"><strong>MWsT-Rückforderung</strong></span><span class="sxs-lookup"><span data-stu-id="63fc1-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="63fc1-131">Erstellen Sie Genehmigungsworkflows für die Erstattung der Mehrwertsteuer (MWsT).</span><span class="sxs-lookup"><span data-stu-id="63fc1-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]