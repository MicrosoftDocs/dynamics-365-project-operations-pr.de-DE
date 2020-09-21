---
title: Projektphasen
description: Dieses Thema enthält Informationen zu Projektphasen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721958"
---
# <a name="project-stages"></a><span data-ttu-id="52d86-103">Projektphasen</span><span class="sxs-lookup"><span data-stu-id="52d86-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52d86-104">Die Projektphasen werden aktualisiert, um den Status des Projekts während seinem Fortschritt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="52d86-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="52d86-105">Der standardmäßige Geschäftsprozessfluss aktualisiert manche Phasen für das Projekt automatisch, wohingegen andere manuell vom Projektmanager aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="52d86-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="52d86-106">Die folgenden Phasen sind im standardmäßigen Geschäftsprozessfluss definiert:</span><span class="sxs-lookup"><span data-stu-id="52d86-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="52d86-107">Neu</span><span class="sxs-lookup"><span data-stu-id="52d86-107">New</span></span>
- <span data-ttu-id="52d86-108">Angebot</span><span class="sxs-lookup"><span data-stu-id="52d86-108">Quote</span></span>
- <span data-ttu-id="52d86-109">Planen</span><span class="sxs-lookup"><span data-stu-id="52d86-109">Plan</span></span>
- <span data-ttu-id="52d86-110">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="52d86-110">Deliver</span></span>
- <span data-ttu-id="52d86-111">Abschließen</span><span class="sxs-lookup"><span data-stu-id="52d86-111">Complete</span></span>
- <span data-ttu-id="52d86-112">Schließen</span><span class="sxs-lookup"><span data-stu-id="52d86-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="52d86-113">Neu</span><span class="sxs-lookup"><span data-stu-id="52d86-113">New</span></span>

<span data-ttu-id="52d86-114">Wenn Sie ein Projekt erstellen, wird die Projektphase auf **Neu** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52d86-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="52d86-115">Wenn das Projekt anhand einer Vorlage erstellt wurde, verfügt es unter Umständen über einen Zeitplan, Schätzungen und Teamdaten.</span><span class="sxs-lookup"><span data-stu-id="52d86-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="52d86-116">Andernfalls handelt es sich lediglich um einen Entwurf des Projekts und die restlichen Komponenten müssen eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="52d86-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="52d86-117">Angebot</span><span class="sxs-lookup"><span data-stu-id="52d86-117">Quote</span></span>

<span data-ttu-id="52d86-118">Wenn Sie ein Projekt einem Angebot zuordnen oder aus einem Angebot ein Projekt erstellen, wird die Projektphase auf **Angebot** festgelegt und die geschätzten Start- und Enddaten werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52d86-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="52d86-119">Während sich das Projekt in der Phase **Angebot** befindet, werden auf der Registerkarte **Vertrieb** auf der Seite **Projektentität** Details zum Angebot angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52d86-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="52d86-120">Planen</span><span class="sxs-lookup"><span data-stu-id="52d86-120">Plan</span></span>

<span data-ttu-id="52d86-121">Wenn Sie für ein Angebot den Zuschlag erhalten, das einem Projekt zugeordnet ist, und das Projekt in die Phase **Vertrag** verschoben wird, wird die Projektphase zu **Planen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52d86-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="52d86-122">Während sich das Projekt in der Phase **Planen** befindet, werden auf der Seite **Projektentität** Details zum Vertrag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="52d86-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="52d86-123">Bereitstellen</span><span class="sxs-lookup"><span data-stu-id="52d86-123">Deliver</span></span>

<span data-ttu-id="52d86-124">Wenn der Projektplan vollständig ist und Sie mit dem Projekt beginnen können, sollte der Projektmanager die Projektphase zu **Bereitstellen** aktualisieren, um anzuzeigen, dass das Projekt gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="52d86-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="52d86-125">Abschließen</span><span class="sxs-lookup"><span data-stu-id="52d86-125">Complete</span></span> 

<span data-ttu-id="52d86-126">Wenn die Arbeit für das Projekt abgeschlossen wurde, kann der Projektmanager die Phase zu **Abgeschlossen** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="52d86-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="52d86-127">Indem er die Projektphase zu **Abgeschlossen** aktualisiert, zeigt der Projektmanager an, dass die Arbeit zwar vollständig abgeschlossen ist, das Projekt aber offen bleibt, damit alle ausstehenden Zeit- oder Ausgabeneingaben erfasst werden können.</span><span class="sxs-lookup"><span data-stu-id="52d86-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="52d86-128">Schließen</span><span class="sxs-lookup"><span data-stu-id="52d86-128">Close</span></span>

<span data-ttu-id="52d86-129">Sobald alle Transaktionen für das Projekt erfasst wurden, kann der Projektmanager die Phase zu **Schließen** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="52d86-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="52d86-130">An diesem Punkt können keine Transaktionen mehr erfasst werden und das Projekt ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52d86-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
