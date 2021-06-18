---
title: Zuweisen einer Ressource zu einer Aufgabe
description: In diesem Thema finden Sie Informationen zum Zuweisen von Ressourcen zu Aufgaben.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a348130ee5760196b2f008ea811e7a81758dd73e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993235"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="7f94b-103">Eine Ressource einer Aufgabe zuweisen</span><span class="sxs-lookup"><span data-stu-id="7f94b-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7f94b-104">Es gibt drei Möglichkeiten, einer Aufgabe in Microsoft Dynamics 365 Project Service Automation eine Ressource zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="7f94b-105">Sie können eine Ressource als Teammitglied buchen und dann einer Aufgabe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="7f94b-106">Mit dieser Methode fügen Sie eine Ressource dem Projektteam hinzu. Anschließend weisen Sie Aufgaben der Ressource im Projektzeitplan zu.</span><span class="sxs-lookup"><span data-stu-id="7f94b-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="7f94b-107">Fügen Sie auf der Registerkarte **Teammitglied** ein neues Teammitglied hinzu, indem Sie **Neu** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="7f94b-108">Der Bereich **Schnellerfassung: Teammitglied** wird geöffnet. Hier können Sie den Namen der buchbaren Ressource auswählen und eine Rolle festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="7f94b-109">Wählen Sie eine der folgenden Zuordnungsmethoden für die Buchung der Ressource aus:</span><span class="sxs-lookup"><span data-stu-id="7f94b-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="7f94b-110">**Volle Kapazität** bucht die Kapazität der vollständige Ressource zum angegebenen Datumsangaben aus und nach.</span><span class="sxs-lookup"><span data-stu-id="7f94b-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="7f94b-111">**Kapazität in Prozent** Bucht die Ressource für einen Prozentsatz der Kapazität der Ressource für das angegebene von Datumsangaben und nach.</span><span class="sxs-lookup"><span data-stu-id="7f94b-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="7f94b-112">**Nach Stunden gleichmäßig verteilen** Bucht die Ressource für eine bestimmte Anzahl und Stunden und verteilt diese gleichmäßig pro Tag zwischen dem angegebenen Start- und Enddatum.</span><span class="sxs-lookup"><span data-stu-id="7f94b-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="7f94b-113">**Nach Stunden von vorn nach hinten verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden von vorn nach hinten und verteilt sie zu angegebenen Daten aus und nach.</span><span class="sxs-lookup"><span data-stu-id="7f94b-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="7f94b-114">Wählen Sie andernfalls **Keine**, da die Ressource dem Team hinzugefügt wird, aber keine Anmeldungen erstellt, um die Kapazität der Ressource zu absorbieren.</span><span class="sxs-lookup"><span data-stu-id="7f94b-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="7f94b-115">Wählen Sie im **Zeitplanraster** einer Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle und wählen Sie anschließend unter **Teammitglieder** das Teammitglied aus, das Sie soeben hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="7f94b-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="7f94b-116">Auf den Registerkarten **Teammitglied** und **Abstimmung** weist die Ressource die gebuchten und zugewiesenen Stunden auf.</span><span class="sxs-lookup"><span data-stu-id="7f94b-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="7f94b-117">Die Stunden sollten gleich sein, dies ist jedoch nicht erforderlich, da Buchungen und Zuweisungen nicht fest miteinander gekoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="7f94b-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="7f94b-118">Auf der Registerkarte **Abstimmung** werden Details angezeigt, wenn sich diese unterscheiden, z. B. wenn Sie einer Ressource mehr Stunden zuweisen, als Sie gebucht haben.</span><span class="sxs-lookup"><span data-stu-id="7f94b-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="7f94b-119">Bei Bedarf können Sie die Informationen korrigieren, indem Sie die Buchungen der Ressource erweitern oder die Zuweisung ändern.</span><span class="sxs-lookup"><span data-stu-id="7f94b-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="7f94b-120">Erstellen eines generischen Teammitglieds über die Aufgabenzuweisung</span><span class="sxs-lookup"><span data-stu-id="7f94b-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="7f94b-121">Wenn Sie ein generisches Teammitglied durch Aufgabenzuweisung erstellen, erstellen Sie einen Platzhalter oder eine generische Ressource, die die Merkmale der benannten Ressource beschreibt, die letztendlich die Aufgaben durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="7f94b-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="7f94b-122">Anschließend generieren Sie eine Anforderung (oder übermittelnd eine Anforderung mithilfe der Anforderung), die zum Suchen und Buchen der genannten Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f94b-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="7f94b-123">Wählen Sie im **Zeitplanraster** für eine Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle aus.</span><span class="sxs-lookup"><span data-stu-id="7f94b-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="7f94b-124">Geben Sie einen Namen als Namen für die Platzhalterressource ein.</span><span class="sxs-lookup"><span data-stu-id="7f94b-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="7f94b-125">Zum Beispiel Projektleiter.</span><span class="sxs-lookup"><span data-stu-id="7f94b-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="7f94b-126">Wählen Sie **Erstellen** aus und legen Sie im Feld **Schnellerfassung: Projektteammitglied** die Rolle für die allgemeine Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="7f94b-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="7f94b-127">Sie können dieser Platzhalterressource weitere Aufgaben zuweisen, indem Sie die Ressource in der **Ressourcenauswahl** für die Aufgabe auswählen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="7f94b-128">Sie sind unter **Teammitglieder** aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7f94b-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="7f94b-129">Wenn Sie die allgemeine Ressource zugewiesen haben, wählen Sie sie auf der Registerkarte **Team** aus und wählen Sie dann **Anforderung erstellen**, um eine Ressourcenanforderung für die generische Ressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="7f94b-130">Wählen Sie **Buchen** für die allgemeine Ressource.</span><span class="sxs-lookup"><span data-stu-id="7f94b-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="7f94b-131">Mithilfe der Zeitplanübersicht können Sie echte Ressourcen suchen und buchen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="7f94b-132">Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden.</span><span class="sxs-lookup"><span data-stu-id="7f94b-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="7f94b-133">Wenn die allgemeine Ressource mit einer benannten Ressource erfüllt ist, wird die aufgewendete allgemeine Ressource aus dem Team entfert und die Aufgabenzuordnungen für die allgemeine Ressource werden der benannten Ressource zugewiesen, mit dem generische Ressourcenanforderungen für der Ressource erfüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="7f94b-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="7f94b-134">Zuweisen einer benannten Ressource aus der Liste aller buchbaren Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f94b-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="7f94b-135">Sie können das Suchfeld in der **Ressourcenauswahl** verwenden, um alle buchbaren Ressourcen zu durchsuchen und einer Aufgabe zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f94b-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="7f94b-136">Auf diese Weise zugewiesene Ressourcen werden dem Team ohne Buchungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7f94b-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="7f94b-137">Dies ist dem Hinzufügen eines Teammitglieds und dem Auswählen von „Keine” als Zuweisungsmethode ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7f94b-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="7f94b-138">Die Ressource wird auf den Registerkarten **Team** und **Abstimmung** als Ressource mit nur Zuweisungen und einem Buchungsdefizit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f94b-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="7f94b-139">Buchen Sie sie, wenn Sie die Verfügbarkeit verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="7f94b-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="7f94b-140">Wählen Sie im **Zeitplanraster** für eine Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle aus.</span><span class="sxs-lookup"><span data-stu-id="7f94b-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="7f94b-141">Starten Sie mit dem Eingeben des Namens.</span><span class="sxs-lookup"><span data-stu-id="7f94b-141">Start typing a name.</span></span> <span data-ttu-id="7f94b-142">Die Suchergebnisse für den Namen werden in die **Ressourcenauswahl** unter **Weitere Ressourcen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f94b-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="7f94b-143">Wählen Sie die Ressource aus, die Sie der Aufgabe zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="7f94b-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]