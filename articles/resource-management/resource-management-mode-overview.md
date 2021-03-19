---
title: Ressourcenverwaltungsmodi – Übersicht
description: Dieses Thema enthält Informationen zur Ressourcenverwaltungsfunktionalität in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279452"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="ac436-103">Ressourcenverwaltungsmodi – Übersicht</span><span class="sxs-lookup"><span data-stu-id="ac436-103">Resource management modes overview</span></span>

<span data-ttu-id="ac436-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="ac436-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ac436-105">Dynamics 365 Project Operations unterstützt zwei Modi, mit denen Sie den gesamten Buchungsflow ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ac436-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="ac436-106">Der Verwaltungsmodus ist als Projektparameter definiert und kann geändert werden, wenn sich Ihre Geschäftsanforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="ac436-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="ac436-107">Zentraler Modus</span><span class="sxs-lookup"><span data-stu-id="ac436-107">Central mode</span></span>
<span data-ttu-id="ac436-108">Für Organisationen, die die Zuweisung von Ressourcen zu Projekten zentralisieren, bietet der Zentralmodus eine Möglichkeit, um sicherzustellen, dass Projektmanager Ressourcenanforderungen auf Projektebene definieren können.</span><span class="sxs-lookup"><span data-stu-id="ac436-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="ac436-109">Die Erfüllung der Ressourcenanforderungen wird an einen Ressourcenmanager delegiert.</span><span class="sxs-lookup"><span data-stu-id="ac436-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="ac436-110">Projektmanager können Ressourcen akzeptieren oder ablehnen, die vom Ressourcenmanager vorgeschlagen werden.</span><span class="sxs-lookup"><span data-stu-id="ac436-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Zentraler Modus](./media/resource-management-central.png)

<span data-ttu-id="ac436-112">Informationen zum Verwalten von Ressourcen im zentralen Modus finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="ac436-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="ac436-113">Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="ac436-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="ac436-114">Benannte Ressourcen aus Ressourcenanforderungen buchen</span><span class="sxs-lookup"><span data-stu-id="ac436-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="ac436-115">Eine Ressourcenanforderung übermitteln</span><span class="sxs-lookup"><span data-stu-id="ac436-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="ac436-116">Eine Ressourcenanfrage erfüllen</span><span class="sxs-lookup"><span data-stu-id="ac436-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="ac436-117">Eine vorgeschlagene Projektressource aus einer Ressourcenanfrage annehmen oder ablehnen</span><span class="sxs-lookup"><span data-stu-id="ac436-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="ac436-118">Hybridmodus</span><span class="sxs-lookup"><span data-stu-id="ac436-118">Hybrid mode</span></span>
<span data-ttu-id="ac436-119">Für Organisationen, die Flexibilität bei der Zuweisung von Ressourcen benötigen, bietet der Hybridmodus sowohl Projektmanagern als auch Ressourcenmanagern die Möglichkeit, Ressourcen zu buchen.</span><span class="sxs-lookup"><span data-stu-id="ac436-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridmodus](./media/resource-management-hybrid.png)

<span data-ttu-id="ac436-121">Weitere Informationen zum Verwalten aller anderen unterstützten Buchungsabläufe im Hybridmodus finden Sie neben dem unterstützten Prozess im zentralen Modus in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="ac436-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="ac436-122">Eine Ressource direkt auf ein Projekt buchen:</span><span class="sxs-lookup"><span data-stu-id="ac436-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="ac436-123">Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen</span><span class="sxs-lookup"><span data-stu-id="ac436-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="ac436-124">Eine Ressource aus einer Ressourcenanforderung buchen:</span><span class="sxs-lookup"><span data-stu-id="ac436-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="ac436-125">Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen</span><span class="sxs-lookup"><span data-stu-id="ac436-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="ac436-126">Benannte Ressourcen aus Ressourcenanforderungen buchen</span><span class="sxs-lookup"><span data-stu-id="ac436-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]