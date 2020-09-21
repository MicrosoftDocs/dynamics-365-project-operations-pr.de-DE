---
title: Wie weise ich einer Aufgabe in der Web-App eine buchbare Ressource zu?
description: Eine Übersicht über die Möglichkeiten, buchbare Ressourcen zuzuweisen.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722067"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="938b6-103">Wie weise ich eine Projektressourcenrolle einer Aufgabe in der Internet-App zu (Project Service-App v2.x)?</span><span class="sxs-lookup"><span data-stu-id="938b6-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="938b6-104">Es gibt zwei Möglichkeiten, eine Ressource zu einer Aufgabe in Project Service zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="938b6-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="938b6-105">Sie können eine Ressource als Teammitglied planen und dann einer Aufgabe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="938b6-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="938b6-106">Oder Sie können ein allgemeines Teammitglied durch Rollenzuweisung zu Aufgaben erstellen, ein Team erstellen, und dann die Anforderungen mit einer benannten Ressource abdecken.</span><span class="sxs-lookup"><span data-stu-id="938b6-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="938b6-107">Beachten Sie, dass Sie, wenn Sie eine buchbare Ressource einer Aufgabe zuweisen möchten, das buchbare Rssourcenteammitglied ausreichend verfügbare Anmeldungen haben muss.</span><span class="sxs-lookup"><span data-stu-id="938b6-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="938b6-108">Der Status der Anmeldung muss festgeleger Übernahmetyp und Status festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="938b6-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="938b6-109">Falls nicht ausreichend Anmeldungen für die Ressource vorhanden sind, entfernt Project Service die Zuweisung und die folgende Fehlermeldung ‏wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="938b6-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="938b6-110">*Die Ressource kann der Aufgabe nicht zugewiesen werden - folgende Ressourcen verfügen nicht über ausreichend gebuchte Zeiten für das Projekt*</span><span class="sxs-lookup"><span data-stu-id="938b6-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="938b6-111">Sie können eine Ressource als Teammitglied planen und dann einer Aufgabe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="938b6-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="938b6-112">Mit dieser Methode fügen Sie eine Ressource dem Projektteam hinzu. Anschließend weisen Sie Aufgaben der Ressource im Projektzeitplan zu.</span><span class="sxs-lookup"><span data-stu-id="938b6-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="938b6-113">So führen Sie diese Aufgabe aus:</span><span class="sxs-lookup"><span data-stu-id="938b6-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="938b6-114">Klicken Sie im Teammitgliedsraster und fügen Sie ein neues Teammitglied hinzu, indem Sie **Neu** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="938b6-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="938b6-115">Auf dem Teammitglied, das der Bildschirm erstellen, aktivieren Sie den buchbaren Ressourcennamen und legen die Rolle fest.</span><span class="sxs-lookup"><span data-stu-id="938b6-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="938b6-116">Wählen Sie die **Von**- und **An**-Daten aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="938b6-117">![Screenshot des Hinzufügens eines Teammitglieds](media/FAQ-Resources-to-Tasks2-1.png "Screenshot des Hinzufügens eines Teammitglieds")</span><span class="sxs-lookup"><span data-stu-id="938b6-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="938b6-118">Dann wählen Sie eine der folgenden Zuordnungsmethoden für die Buchung der Ressource aus:</span><span class="sxs-lookup"><span data-stu-id="938b6-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="938b6-119">**Volle Kapazität** bucht die Kapazität der vollständige Ressource zum angegebenen Datumsangaben aus und nach.</span><span class="sxs-lookup"><span data-stu-id="938b6-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="938b6-120">**Kapazität in Prozent** Bucht die Ressource für einen Prozentsatz der Kapazität der Ressource für das angegebene von Datumsangaben und nach.</span><span class="sxs-lookup"><span data-stu-id="938b6-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="938b6-121">**Nach Stunden gleichmäßig verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden gleichmäßig sie verteilt um die zum angegebenen Datumsangaben aus und nach.</span><span class="sxs-lookup"><span data-stu-id="938b6-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="938b6-122">**Nach Stunden von vorn nach hinten verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden von vorn nach hinten und verteilt sie zu angegebenen Daten aus und nach.</span><span class="sxs-lookup"><span data-stu-id="938b6-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="938b6-123">Wählen Sie andernfalls **Keine**, da die Ressource dem Team hinzugefügt wird, aber erstellt keine Anmeldungen erstellt, um die Kapazität der Ressource zu absorbieren.</span><span class="sxs-lookup"><span data-stu-id="938b6-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="938b6-124">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-124">Select **Save**.</span></span>

    <span data-ttu-id="938b6-125">Beachten Sie, dass die Stunden der Anmeldung ausreichend sein, um die Aufwandsstunden und die Datumsbereiche der Aufgaben auch wirklich abzudecken, die Sie diesen Ressource zuweisen.</span><span class="sxs-lookup"><span data-stu-id="938b6-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="938b6-126">Wenn sie nicht ausgerichtet sind, können Sie die Ressource nicht mehr der Aufgabe zuweisen.</span><span class="sxs-lookup"><span data-stu-id="938b6-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="938b6-127">Im Projektstrukturplan (WBS) für die Aufgaben, klicken Sie auf das Dropdown-Menü Ressourcenzellen</span><span class="sxs-lookup"><span data-stu-id="938b6-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="938b6-128">dann:</span><span class="sxs-lookup"><span data-stu-id="938b6-128">Then:</span></span> 

    1. <span data-ttu-id="938b6-129">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-129">Select **Add**.</span></span>
    2. <span data-ttu-id="938b6-130">Wählen Sie das Dropdown-Listenfeld aus unter **Ressourcen** und wählen Sie das Teammitglied aus, das Sie oben hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="938b6-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="938b6-131">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-131">Select **OK**.</span></span> <span data-ttu-id="938b6-132">Das Teammitglied ist nun der Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="938b6-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="938b6-133">![Screenshot des Hinzufügens von Ressourcen mit WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot des Hinzufügens von Ressourcen mit WBS")</span><span class="sxs-lookup"><span data-stu-id="938b6-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="938b6-134">Klicken Sie im Teammitgliedsraster und Sie finden im Aggregat der Ressource zugewiesene Stunden mit zugeteilten Stunden.</span><span class="sxs-lookup"><span data-stu-id="938b6-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="938b6-135">Sie ist kleiner oder gleich der gebuchten Stunden für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="938b6-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="938b6-136">![Screenshot der zugewiesenen Stunden für eine Ressource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot der zugewiesenen Stunden für eine Ressource")</span><span class="sxs-lookup"><span data-stu-id="938b6-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="938b6-137">Wenn die Aufgabe, die Sie gerade der Ressource zuweisen möchten nach dem Enddatum der gebuchten Ressourcen beginnt, erscheint die Ressource nicht im Dropdown-Menü.</span><span class="sxs-lookup"><span data-stu-id="938b6-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="938b6-138">Beachten Sie, dass Sie eine Ressource zu mehr Stunden als die gebuchten Stunden zuweisen können, wenn die Ressource verbleibende nicht zugewiesene Kapazität hat.</span><span class="sxs-lookup"><span data-stu-id="938b6-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="938b6-139">In diesem Fall wird die Ressource nur teilweise bei Anmeldungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="938b6-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="938b6-140">Sie können die restlichen nicht zugewiesene Aufgabenstunden anzeigen, indem Sie in der Unstaffed-Stundenspalte den Projektstrukturplan hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="938b6-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="938b6-141">Wenn Ressourcen den gebuchten Stunden zugewiesen werden (die gebuchten Stunden entsprechen den zugewiesenen Stunden), wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, weitere Aufgaben zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="938b6-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="938b6-142">*Die Ressource kann der Aufgabe nicht zugewiesen werden - folgende Ressourcen verfügen nicht über ausreichend gebuchte Zeiten für das Projekt*</span><span class="sxs-lookup"><span data-stu-id="938b6-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="938b6-143">Außerdem wird das Standardprojekt Teammitglied verwalten, dem Team hinzugefügt, wenn Sie das Projekt erstellen, ohne die Anmeldungen hinzuzufügen und kann nicht zu einer dieser Aufgaben zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="938b6-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="938b6-144">Sie werden nicht im Ressourcendropdown-Menü für Aufgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="938b6-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="938b6-145">Wenn Sie diese Ressourcen zuweisen möchten, müssen Sie sie vom Team entfernen und dann mit einer Zuordnungsmethode außer keine erneut hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="938b6-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="938b6-146">Der Grund, wieso Sie dem Team hinzugefügt werden, wenn das Projekt erstellt wird ist, weil ein Projekt mindestens einen Projektgenehmiger standardmäßig hat.</span><span class="sxs-lookup"><span data-stu-id="938b6-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="938b6-147">Erstellen Sie ein allgemeins Teammitglied durch Rollenzuweisung auf Aufgaben</span><span class="sxs-lookup"><span data-stu-id="938b6-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="938b6-148">Diese Methode, gewährleistet, dass genügend Anmeldungen für Aufgaben bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="938b6-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="938b6-149">Erstellen Sie zunächst einen Platzhalter oder eine allgemeine Ressource, die die Eigenschaften der benannten Ressource beschreiben, die Sie letztendlich bearbeiten möchten, indem Sie ein Team erstellen, nachdem Sie Rollen an Aufgaben zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="938b6-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="938b6-150">So führen Sie diese Aufgabe aus:</span><span class="sxs-lookup"><span data-stu-id="938b6-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="938b6-151">Im Projektstrukturplan wählen Sie eine Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="938b6-152">Wählen Sie das Symbol **Zugewiesene Rolle** in der Ressourcenzelle aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="938b6-153">Wählen Sie das **Rolle** Dropdown-Listenfeld und die Rolle für die allgemeine Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="938b6-154">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="938b6-155">![Screenshot des Hinzufügens von Ressourcen mithilfe von WBS](media/FAQ-Resources-to-Tasks2-4.png "Screenshot des Hinzufügens von Ressourcen mithilfe von WBS")</span><span class="sxs-lookup"><span data-stu-id="938b6-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="938b6-156">Wenn Sie Rollen zu den Aufgaben einem Benutzer im PSP zuweisen abgeschlossen haben, wählen Sie **Projektteam generieren** aus.</span><span class="sxs-lookup"><span data-stu-id="938b6-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="938b6-157">Project Service erstellt die Mindestanzahl von Teammitgliedern basierend auf den Rollen, den Beschaffungsorganisationseinheiten und dem Projektkalender, indem Sie die Aufgabenzuordnungen zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="938b6-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="938b6-158">![Screenshot der Erstellung eines Projektteams](media/FAQ-Resources-to-Tasks2-5.png "Screenshot der Erstellung eines Projektteams")</span><span class="sxs-lookup"><span data-stu-id="938b6-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="938b6-159">Klicken Sie im Teammitgliedsraster und suchen Sie die Ressourcen des generischen Ressourcentyps mit den rollen und Positionsnamen.</span><span class="sxs-lookup"><span data-stu-id="938b6-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="938b6-160">Wenn zwei Ressourcen erforderlich sind, damit eine Rolle abgeschlossen werden kann, erstellt die Teamfunktion zwei Teammitglieder und verwendet Positionsnamen, um Sie zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="938b6-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="938b6-161">![Screenshot des Hinzufügens von zwei allgemeinen Ressourcen](media/FAQ-Resources-to-Tasks2-6.png "Screenshot des Hinzufügens von zwei allgemeinen Ressourcen")</span><span class="sxs-lookup"><span data-stu-id="938b6-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="938b6-162">Sie können die unterstützende Ressourcenanforderung für das allgemeine Teammitglied öffnen, indem Sie den Link mit Ressourcenanforderungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="938b6-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="938b6-163">![Screenshot vom Öffnen von unterstützenden Ressourcenanforderung](media/FAQ-Resources-to-Tasks2-7.png "Screenshot vom Öffnen von unterstützenden Ressourcenanforderung")</span><span class="sxs-lookup"><span data-stu-id="938b6-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="938b6-164">**Buchen** wählen Sie für die allgemeine Ressource und dann können Sie die Zeitplanübersicht verwenden, um eine echte Ressource zu suchen und zu buchen.</span><span class="sxs-lookup"><span data-stu-id="938b6-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="938b6-165">Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden, indem Sie **Übermittlungsanfrage** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="938b6-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="938b6-166">Wenn die allgemeine Ressource mit einer benannten Ressource erfüllt ist, wird die aufgewendete allgemeine Ressource aus dem Team entfert und die Aufgabenzuordnungen für die allgemeine Ressource werden der benannten Ressource zugewiesen, mit dem generische Ressourcenanforderungen für der Ressource erfüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="938b6-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

