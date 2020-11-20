---
title: Richten Sie Workflows für die Ausgabenverwaltung ein
description: Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127697"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="c721f-103">Richten Sie Workflows für die Ausgabenverwaltung ein</span><span class="sxs-lookup"><span data-stu-id="c721f-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="c721f-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="c721f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c721f-105">Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="c721f-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="c721f-106">Sie können Workflows für Ausgabenabrechnungen, Reiseanforderungen und Vorauszahlungen definieren.</span><span class="sxs-lookup"><span data-stu-id="c721f-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="c721f-107">Ein Workflow stellt einen Geschäftsprozess dar und definiert, wie ein Dokument durch das System fließt.</span><span class="sxs-lookup"><span data-stu-id="c721f-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="c721f-108">Der Workflow gibt auch an, wer eine Aufgabe ausführen oder ein Dokument genehmigen muss.</span><span class="sxs-lookup"><span data-stu-id="c721f-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="c721f-109">Die Verwendung des Workflow-Systems in Ihrer Organisation bietet mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="c721f-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="c721f-110">**Konsistente Prozesse**: Sie können den Genehmigungsprozess für bestimmte Dokumente wie Bestellanforderungen und Spesenabrechnungen definieren.</span><span class="sxs-lookup"><span data-stu-id="c721f-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="c721f-111">Die Nutzung des Workflowsystems hiflt, dass Dokumente auf konsistente und effiziente Weise verarbeitet und genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="c721f-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="c721f-112">**Prozesstransparenz**: Sie können den Status, den Verlauf und die Leistungsmetriken einer bestimmten Workflowinstanz verfolgen.</span><span class="sxs-lookup"><span data-stu-id="c721f-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="c721f-113">Dies hilft Ihnen zu bestimmen, ob Änderungen am Workflow vorgenommen werden sollten, um die Effizienz zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c721f-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="c721f-114">**Zentralisierte Arbeitsliste**: Benutzer können eine zentralisierte Arbeitsliste anzeigen, um die ihnen zugewiesenen Workflowaufgaben und Genehmigungen zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c721f-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="c721f-115">Workflowregeln</span><span class="sxs-lookup"><span data-stu-id="c721f-115">Workflow types</span></span>

<span data-ttu-id="c721f-116">Die folgende Tabelle enthält die Workflow-Typen, die Sie in der **Ausgabenverwaltung** erstellen können.</span><span class="sxs-lookup"><span data-stu-id="c721f-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="c721f-117"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="c721f-118"><strong>Verwenden Sie diesen Typ, um</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="c721f-119"><strong>Ausgabenberichte automatisch genehmigen</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="c721f-120">Erstellen Sie Genehmigungsworkflows für Spesenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="c721f-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="c721f-121"><strong>Automatische Ausgabenabrechnungen buchen</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="c721f-122">Buchen Sie automatisch Workflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="c721f-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="c721f-123"><strong>Ausgabenzeilenelement</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="c721f-124">Erstellen Sie Genehmigungsworkflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="c721f-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="c721f-125"><strong>Automatische Buchung von Ausgaben</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="c721f-126">Erstellen Sie automatische Buchungsworkflows für Ausgabenabrechnungen.</span><span class="sxs-lookup"><span data-stu-id="c721f-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="c721f-127"><strong>Reiseanforderung</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="c721f-128">Erstellen Sie Genehmigungsworkflows für Reiseanforderungen.</span><span class="sxs-lookup"><span data-stu-id="c721f-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="c721f-129"><strong>Vorauskassenanfrage</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="c721f-130">Erstellen Sie Genehmigungsworkflows für Vorauszahlungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="c721f-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="c721f-131"><strong>MWsT-Rückforderung</strong></span><span class="sxs-lookup"><span data-stu-id="c721f-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="c721f-132">Erstellen Sie Genehmigungsworkflows für die Erstattung der Mehrwertsteuer (MWsT).</span><span class="sxs-lookup"><span data-stu-id="c721f-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
