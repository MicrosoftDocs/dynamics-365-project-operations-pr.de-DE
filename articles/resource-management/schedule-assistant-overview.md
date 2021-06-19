---
title: Ansicht für Zeitplan-Assistent
description: Dieses Thema enthält Informationen zur Arbeit mit dem Zeitplan-Assistenten zum Buchen von Ressourcen.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014115"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="d1518-103">Ansicht für Zeitplan-Assistent</span><span class="sxs-lookup"><span data-stu-id="d1518-103">Schedule assistant overview</span></span>

<span data-ttu-id="d1518-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="d1518-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1518-105">Mit dem Zeitplan-Assistenten werden Ressourcen basierend auf den vom Projektmanager festgelegten Anforderungen gebucht.</span><span class="sxs-lookup"><span data-stu-id="d1518-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="d1518-106">Der Zeitplan-Assistent stützt sich auf die in der Ressourcenanforderung angegebenen Parameter, um die Ressource zu finden.</span><span class="sxs-lookup"><span data-stu-id="d1518-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="d1518-107">Der Zeitplan-Assistent empfiehlt Ressourcen, die den relevanten Anforderungen entsprechen, z. B. Zeitfenster oder erforderliche Fähigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d1518-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="d1518-108">Nachdem geeignete Ressourcen identifiziert wurden, kann der Ressourcen- oder Projektmanager die Ressource für die Arbeit buchen.</span><span class="sxs-lookup"><span data-stu-id="d1518-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d1518-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d1518-109">Prerequisites</span></span>

<span data-ttu-id="d1518-110">Der Zeitplan-Assistent ist Teil der Universal Resource Scheduling-Lösung.</span><span class="sxs-lookup"><span data-stu-id="d1518-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="d1518-111">Diese Lösung ist im Lieferumfang enthalten und wird mit Dynamics 365 Project Operations, Dynamics 365 Field Service und Dynamics 365 Customer Service installiert.</span><span class="sxs-lookup"><span data-stu-id="d1518-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="d1518-112">Übereinsteimmende Anforderungen und Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1518-112">Matching requirements and resources</span></span>

<span data-ttu-id="d1518-113">Ein generierter Ressourcenbedarf basiert auf Details wie:</span><span class="sxs-lookup"><span data-stu-id="d1518-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="d1518-114">Merkmale</span><span class="sxs-lookup"><span data-stu-id="d1518-114">Characteristics</span></span>
-   <span data-ttu-id="d1518-115">Rollen</span><span class="sxs-lookup"><span data-stu-id="d1518-115">Roles</span></span>
-   <span data-ttu-id="d1518-116">Unternehmenseinheiten</span><span class="sxs-lookup"><span data-stu-id="d1518-116">Business units</span></span>
-   <span data-ttu-id="d1518-117">Bevorzugte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1518-117">Resource preferences</span></span>
-   <span data-ttu-id="d1518-118">Aufwandskonturen</span><span class="sxs-lookup"><span data-stu-id="d1518-118">Effort contours</span></span>
-   <span data-ttu-id="d1518-119">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="d1518-119">Time zone</span></span>

<span data-ttu-id="d1518-120">Der Zeitplan-Assistent verwendet diese Details, um Ressourcen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d1518-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="d1518-121">Den Zeitplan-Assistenten starten</span><span class="sxs-lookup"><span data-stu-id="d1518-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="d1518-122">Es gibt zwei Möglichkeiten, wie der Zeitplan-Assistent gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d1518-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="d1518-123">Wenn Sie den Hybridmodus verwenden, können Sie im Teammitgliedsraster jedes Teammitglied mit einem nicht erfüllten Ressourcenbedarf und dann **Buchen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="d1518-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="d1518-124">Wenn Sie den zentralen Modus verwenden, findet der Ressourcenmanager die Ressource und wählt sie aus.</span><span class="sxs-lookup"><span data-stu-id="d1518-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="d1518-125">Zeitplan-Assistent-Filter</span><span class="sxs-lookup"><span data-stu-id="d1518-125">Schedule assistant filters</span></span>

<span data-ttu-id="d1518-126">Nachdem der Zeitplan-Assistent ausgeführt wurde, werden die Details aus der Ressourcenanforderung als gefilterte Werte im linken Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1518-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="d1518-127">Der Ressourcenmanager oder der Projektmanager kann die Ergebnisse optimieren, indem er die Filter an die Planungsanforderungen anpasst.</span><span class="sxs-lookup"><span data-stu-id="d1518-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="d1518-128">Im Filterbereich werden arbeitsbezogene Optionen angezeigt, darunter:</span><span class="sxs-lookup"><span data-stu-id="d1518-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="d1518-129">Arbeitsstart- und Enddatum</span><span class="sxs-lookup"><span data-stu-id="d1518-129">Work start and end</span></span>
-   <span data-ttu-id="d1518-130">Merkmale</span><span class="sxs-lookup"><span data-stu-id="d1518-130">Characteristics</span></span>
-   <span data-ttu-id="d1518-131">Rollen</span><span class="sxs-lookup"><span data-stu-id="d1518-131">Roles</span></span>
-   <span data-ttu-id="d1518-132">Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="d1518-132">Organizational units</span></span>
-   <span data-ttu-id="d1518-133">Ressourcenzuordnungsunternehmen</span><span class="sxs-lookup"><span data-stu-id="d1518-133">Resourcing company</span></span>
-   <span data-ttu-id="d1518-134">Ressourcentypen</span><span class="sxs-lookup"><span data-stu-id="d1518-134">Resource types</span></span>
-   <span data-ttu-id="d1518-135">Bevorzugte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d1518-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]