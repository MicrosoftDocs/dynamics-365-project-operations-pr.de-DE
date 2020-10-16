---
title: Zu einem Projekt buchen
description: Dieses Thema enthält Informationen zum Buchen einer Ressource für ein Projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908151"
---
# <a name="book-to-a-project"></a><span data-ttu-id="3873e-103">Zu einem Projekt buchen</span><span class="sxs-lookup"><span data-stu-id="3873e-103">Book to a project</span></span>

<span data-ttu-id="3873e-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3873e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3873e-105">Es gibt Zeiten, in denen ein Projektmanager oder Ressourcenmanager dem Projekt eine Ressource zuweisen muss, ohne dass eine bestimmte Anforderung von einem generischen Teammitglied definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3873e-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="3873e-106">Dies kann auf eine von drei Wegen erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="3873e-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="3873e-107">Buchen aus dem Teammitgliedsraster</span><span class="sxs-lookup"><span data-stu-id="3873e-107">Book from the team member grid</span></span>
- <span data-ttu-id="3873e-108">Über die Zeitplanübersicht buchen</span><span class="sxs-lookup"><span data-stu-id="3873e-108">Book from the schedule board</span></span>
- <span data-ttu-id="3873e-109">Buchen aus dem **Projekt**-Forumar</span><span class="sxs-lookup"><span data-stu-id="3873e-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="3873e-110">Buchen aus dem Teammitgliedsraster</span><span class="sxs-lookup"><span data-stu-id="3873e-110">Book from the team member grid</span></span>

<span data-ttu-id="3873e-111">Wenn Ihre Organisation im hybriden Ressourcenzuweisungsmodus arbeitet, kann der Projektmanager eine Ressource direkt für das Projekt buchen, indem er die folgenden Schritte ausführt.</span><span class="sxs-lookup"><span data-stu-id="3873e-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="3873e-112">Gehen Sie im Projekt zum Teammitgliedsraster und wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="3873e-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="3873e-113">Definieren Sie den Positionsnamen und die Rolle der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3873e-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="3873e-114">Wählen Sie die buchbare Ressourcen aus der verfügbaren Suche.</span><span class="sxs-lookup"><span data-stu-id="3873e-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="3873e-115">Definieren Sie nach Auswahl der Ressource die folgenden Feldinformationen, um die Ressource zu buchen:</span><span class="sxs-lookup"><span data-stu-id="3873e-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="3873e-116">Startdatum</span><span class="sxs-lookup"><span data-stu-id="3873e-116">Start date</span></span>
    - <span data-ttu-id="3873e-117">Fertigstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="3873e-117">Finish date</span></span>
    - <span data-ttu-id="3873e-118">Zuordnungsmethode</span><span class="sxs-lookup"><span data-stu-id="3873e-118">Allocation method</span></span>
    - <span data-ttu-id="3873e-119">Stunden, falls zutreffend</span><span class="sxs-lookup"><span data-stu-id="3873e-119">Hours, if applicable</span></span>
    - <span data-ttu-id="3873e-120">Projektgenehmiger</span><span class="sxs-lookup"><span data-stu-id="3873e-120">Project approver</span></span>

6. <span data-ttu-id="3873e-121">Wählen Sie **Speichern und schließen** aus</span><span class="sxs-lookup"><span data-stu-id="3873e-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="3873e-122">Über die Zeitplanübersicht buchen</span><span class="sxs-lookup"><span data-stu-id="3873e-122">Book from the schedule board</span></span>

<span data-ttu-id="3873e-123">Wenn ein Ressourcenmanager eine Ressource direkt für ein Projekt buchen muss, kann er die Zeitplanübersicht und die Projektanforderungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3873e-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="3873e-124">Die Projektanforderung ist eine Ressourcenanforderung, für die immer gebucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="3873e-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="3873e-125">Um direkt aus der Zeitplanübersicht für ein Projekt zu buchen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3873e-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="3873e-126">Navigieren Sie zur Zeitplanübersicht und filtern Sie auf der linken Seite nach den Ressourcen, die Sie für die Anforderung in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="3873e-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="3873e-127">Wählen Sie im unteren Bereich die Registerkarte **Projekt** aus, um eine Liste der Projektanforderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3873e-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="3873e-128">Ziehen Sie die Anforderung auf eine Ressource und definieren Sie die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="3873e-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="3873e-129">Startdatum</span><span class="sxs-lookup"><span data-stu-id="3873e-129">Start date</span></span>
    - <span data-ttu-id="3873e-130">Fertigstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="3873e-130">Finish date</span></span>
    - <span data-ttu-id="3873e-131">Buchungsstatus</span><span class="sxs-lookup"><span data-stu-id="3873e-131">Booking status</span></span>
    - <span data-ttu-id="3873e-132">Buchungsmethode</span><span class="sxs-lookup"><span data-stu-id="3873e-132">Booking method</span></span>
    - <span data-ttu-id="3873e-133">Dauer</span><span class="sxs-lookup"><span data-stu-id="3873e-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="3873e-134">Buchen aus dem Projekt-Forumar</span><span class="sxs-lookup"><span data-stu-id="3873e-134">Book from the Project form</span></span>

<span data-ttu-id="3873e-135">Als Projektmanager müssen Sie möglicherweise eine Ressource für ein Projekt buchen, kennen jedoch nur die Kriterien und nicht den Namen der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3873e-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="3873e-136">Führen Sie die folgenden Schritte aus, um mithilfe des Zeitplanassistenten eine Ressource basierend auf verfügbaren Attributen der Ressource zu finden.</span><span class="sxs-lookup"><span data-stu-id="3873e-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="3873e-137">Navigieren Sie zum Projekt und wählen Sie **Buchen** aus, um den Zeitplanassistenten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3873e-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="3873e-138">Grenzen Sie die Kriterien mithilfe der Filter auf der linken Seite des Zeitplanassistenten ein und wählen Sie **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="3873e-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="3873e-139">Basierend auf den in den Ergebnissen zurückgegebenen Ressourcen können Sie eine Ressource buchen.</span><span class="sxs-lookup"><span data-stu-id="3873e-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="3873e-140">Diese Methode erstellt keine Buchungen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="3873e-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="3873e-141">Stattdessen wird die Ressource dem Team hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3873e-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="3873e-142">Nachdem das Teammitglied dem Projekt hinzugefügt wurde, kann der Projektmanager Buchungen verwalten oder Buchungen erweitern, um die erforderlichen Buchungen zur Ressource hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3873e-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
