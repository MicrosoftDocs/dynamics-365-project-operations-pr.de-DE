---
title: Projektphasen
description: Dieses Thema enthält Informationen zu den Projektphasen, die in Microsoft Dynamics Project Operations verfügbar sind.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076651"
---
# <a name="project-stages"></a><span data-ttu-id="d2557-103">Projektphasen</span><span class="sxs-lookup"><span data-stu-id="d2557-103">Project stages</span></span>

<span data-ttu-id="d2557-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="d2557-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d2557-105">Projektphasen sind so konzipiert, dass sie den Status des Projekts während seines Fortschritts widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d2557-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="d2557-106">Anpassungen können verwendet werden, um die Phasen automatisch mit Geschäftsprozessflüssen, Power Automate oder Plug-In-Erweiterungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d2557-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="d2557-107">Die folgenden Phasen sind standardmäßig im Geschäftsprozessfluss definiert:</span><span class="sxs-lookup"><span data-stu-id="d2557-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="d2557-108">Neu</span><span class="sxs-lookup"><span data-stu-id="d2557-108">New</span></span>
- <span data-ttu-id="d2557-109">Angebot</span><span class="sxs-lookup"><span data-stu-id="d2557-109">Quote</span></span>
- <span data-ttu-id="d2557-110">Plan</span><span class="sxs-lookup"><span data-stu-id="d2557-110">Plan</span></span>
- <span data-ttu-id="d2557-111">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d2557-111">Deliver</span></span>
- <span data-ttu-id="d2557-112">Abschließen</span><span class="sxs-lookup"><span data-stu-id="d2557-112">Complete</span></span>
- <span data-ttu-id="d2557-113">Schließen</span><span class="sxs-lookup"><span data-stu-id="d2557-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="d2557-114">Neu</span><span class="sxs-lookup"><span data-stu-id="d2557-114">New</span></span>

<span data-ttu-id="d2557-115">Wenn Sie ein Projekt erstellen, wird die Projektphase auf **Neu** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d2557-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="d2557-116">Wenn das Projekt anhand einer Vorlage erstellt wurde, verfügt es unter Umständen über einen Zeitplan, Schätzungen und Teamdaten.</span><span class="sxs-lookup"><span data-stu-id="d2557-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="d2557-117">Andernfalls handelt es sich lediglich um einen Entwurf des Projekts und die restlichen Komponenten müssen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d2557-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="d2557-118">Angebot</span><span class="sxs-lookup"><span data-stu-id="d2557-118">Quote</span></span>

<span data-ttu-id="d2557-119">Wenn Sie ein Projekt einem Angebot zuordnen oder aus einem Angebot ein Projekt erstellen, wird die Projektphase auf **Angebot** festgelegt und die geschätzten Start- und Enddaten werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d2557-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="d2557-120">Während sich das Projekt in der Phase **Angebot** befindet, werden auf der Registerkarte **Vertrieb** auf der Seite **Projektentität** Details zum Angebot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2557-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="d2557-121">Planen</span><span class="sxs-lookup"><span data-stu-id="d2557-121">Plan</span></span>

<span data-ttu-id="d2557-122">Wenn Sie für ein Angebot den Zuschlag erhalten, das einem Projekt zugeordnet ist, und das Projekt in die Phase **Vertrag** verschoben wird, wird die Projektphase zu **Planen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d2557-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="d2557-123">Während sich das Projekt in der Phase **Planen** befindet, werden auf der Seite **Projektentität** Details zum Vertrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2557-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="d2557-124">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d2557-124">Deliver</span></span>

<span data-ttu-id="d2557-125">Wenn der Projektplan vollständig ist und Sie mit dem Projekt beginnen können, sollte der Projektmanager die Projektphase zu **Bereitstellen** aktualisieren, um anzuzeigen, dass das Projekt gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2557-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="d2557-126">Abschließen</span><span class="sxs-lookup"><span data-stu-id="d2557-126">Complete</span></span> 

<span data-ttu-id="d2557-127">Wenn die Arbeit für das Projekt abgeschlossen wurde, kann der Projektmanager die Phase zu **Abgeschlossen** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d2557-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="d2557-128">Indem er die Projektphase zu **Abgeschlossen** aktualisiert, zeigt der Projektmanager an, dass die Arbeit zwar vollständig abgeschlossen ist, das Projekt aber offen bleibt, damit alle ausstehenden Zeit- oder Ausgabeneingaben erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="d2557-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="d2557-129">Schließen</span><span class="sxs-lookup"><span data-stu-id="d2557-129">Close</span></span>

<span data-ttu-id="d2557-130">Sobald alle Transaktionen für das Projekt erfasst wurden, kann der Projektmanager die Phase zu **Schließen** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d2557-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="d2557-131">An diesem Punkt können keine Transaktionen mehr erfasst werden und das Projekt ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d2557-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

