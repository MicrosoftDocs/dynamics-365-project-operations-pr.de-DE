---
title: Upgrade-Überlegungen für den Projektstrukturplan
description: Dieses Thema enthält Informationen zum Aktualisieren des Projektstrukturplans von Project Service Automation 2.x auf 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951343"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="52caf-103">Upgrade-Überlegungen für den Projektstrukturplan</span><span class="sxs-lookup"><span data-stu-id="52caf-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="52caf-104">Dieses Thema enthält Informationen zum Aktualisieren des Projektstrukturplans von Project Service Automation 2.x auf 3.x.</span><span class="sxs-lookup"><span data-stu-id="52caf-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="52caf-105">Dieses Thema definiert den fehlerfreien Status eines Projekts in Project Service Automation (PSA), der für ein erfolgreiches Upgrade erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="52caf-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="52caf-106">Es gibt auch Informationen über die allgemeinen Sperrbedingungen, die zum Fehlschlag eines Upgrades führen können.</span><span class="sxs-lookup"><span data-stu-id="52caf-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="52caf-107">Weitere Informationen über das Definieren von Projektaufgaben und deren Funktionen innerhalb eines Projektzeitplans finden Sie unter [Projektzeitpläne](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="52caf-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="52caf-108">Schlüsselentitäten</span><span class="sxs-lookup"><span data-stu-id="52caf-108">Key entities</span></span>
<span data-ttu-id="52caf-109">Für einen akkuraten Projektstrukturplan, für den bereits Ressourcen geladen sind, sind die folgenden Entitäten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="52caf-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="52caf-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="52caf-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="52caf-111">Projektteam</span><span class="sxs-lookup"><span data-stu-id="52caf-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="52caf-112">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="52caf-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="52caf-113">Ressourcenzuweisungen</span><span class="sxs-lookup"><span data-stu-id="52caf-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="52caf-114">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="52caf-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="52caf-115">Buchbare Ressourcen</span><span class="sxs-lookup"><span data-stu-id="52caf-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="52caf-116">Um eine Ressource zu definieren, die in einen Projektstrukturplan geladen wird, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="52caf-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="52caf-117">Erstellen Sie ein neues Projekt.</span><span class="sxs-lookup"><span data-stu-id="52caf-117">Create a new project.</span></span> <span data-ttu-id="52caf-118">Weitere Informationen darüber, wie ein neues Projekt erstellt wird, finden Sie unter [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="52caf-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="52caf-119">Erstellen Sie mindestens eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="52caf-119">Create one or more tasks.</span></span> <span data-ttu-id="52caf-120">Weitere Informationen darüber, wie Sie eine Aufgabe erstellen, finden Sie unter [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="52caf-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="52caf-121">Definieren Sie die Aufgabenabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="52caf-121">Define the task dependencies.</span></span> <span data-ttu-id="52caf-122">Weitere Informationen finden Sie unter [Projektaufgabenabhängigkeit](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="52caf-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="52caf-123">Weisen Sie dem Projekt Projektteam-Mitglieder zu.</span><span class="sxs-lookup"><span data-stu-id="52caf-123">Assign project team members to the project.</span></span> <span data-ttu-id="52caf-124">Weitere Informationen finden Sie unter [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="52caf-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="52caf-125">Weisen Sie den Aufgaben Projektteam-Mitglieder zu.</span><span class="sxs-lookup"><span data-stu-id="52caf-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="52caf-126">Weitere Informationen finden Sie unter [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="52caf-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="52caf-127">Projektteambeziehungen</span><span class="sxs-lookup"><span data-stu-id="52caf-127">Project team relationships</span></span>

<span data-ttu-id="52caf-128">Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:</span><span class="sxs-lookup"><span data-stu-id="52caf-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="52caf-129">Alle Projektteam-Mitglieder müssen einer buchbaren Ressource zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="52caf-130">Alle Projektteam-Mitglieder müssen demselben Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="52caf-131">Projektaufgabenbeziehungen</span><span class="sxs-lookup"><span data-stu-id="52caf-131">Project task relationships</span></span>
<span data-ttu-id="52caf-132">Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:</span><span class="sxs-lookup"><span data-stu-id="52caf-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="52caf-133">Alle zugehörigen Aufgaben müssen demselben Projekt zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="52caf-134">Jede Positionsaufgabe muss eine übergeordnete Aufgabe haben.</span><span class="sxs-lookup"><span data-stu-id="52caf-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="52caf-135">Jede Aufgabe muss ein übergeordnetes Projekt haben.</span><span class="sxs-lookup"><span data-stu-id="52caf-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="52caf-136">Gültige Bedingungen</span><span class="sxs-lookup"><span data-stu-id="52caf-136">Valid conditions</span></span>

- <span data-ttu-id="52caf-137">Alle Aufgabendauern müssen größer oder gleich (>=) eine Stunde und weniger als 1.800.000 Minuten (1.250 Tage) sein.\*</span><span class="sxs-lookup"><span data-stu-id="52caf-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="52caf-138">Alle Aufgaben müssen ein Startdatum haben, das nicht vor dem 01.01.2000 liegen darf.\*</span><span class="sxs-lookup"><span data-stu-id="52caf-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="52caf-139">Alle Aufgaben müssen ein Startdatum haben, das nicht mehr als 17 Jahre nach dem heutigen Tag liegen darf.\*</span><span class="sxs-lookup"><span data-stu-id="52caf-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="52caf-140">Alle Aufgaben müssen ein Startdatum haben, das gleich ihrem Abschlussdatum ist oder vor diesem liegt.</span><span class="sxs-lookup"><span data-stu-id="52caf-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="52caf-141">Alle Transaktionstypen für Klassifizierungen (Ausgaben, Material, Steuern und Zeit) müssen über Werte für **Standardeinheit** und **Einheitengruppe** verfügen.</span><span class="sxs-lookup"><span data-stu-id="52caf-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="52caf-142">Datumsformate mit Buchstaben sollten vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="52caf-143">Potentielle Risikominderungsschritte</span><span class="sxs-lookup"><span data-stu-id="52caf-143">Potential mitigation steps</span></span>
- <span data-ttu-id="52caf-144">Verwenden Sie die erweiterte Suche, um Projektaufgaben zu identifizieren, die keine Projekt-ID enthalten.</span><span class="sxs-lookup"><span data-stu-id="52caf-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="52caf-145">Verwenden Sie die erweiterte Suche, um Projektaufgaben zu identifizieren, deren geplante Dauer größer als> 1.800.000 ist.</span><span class="sxs-lookup"><span data-stu-id="52caf-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="52caf-146">Bevor Sie Datenänderungen vornehmen, sollten Sie Anpassungen untersuchen, die der Entität zugeordnet sind und dazu geführt haben, dass die Daten möglicherweise in einen fehlerhaften Zustand versetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="52caf-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="52caf-147">Diese Anpassungen sollten behoben werden, bevor Sie mit datenbezogenen Aktualisierungen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="52caf-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="52caf-148">Erwägen Sie für die identifizierten Aufgaben, die verwaist sind, das Löschen dieser Aufgaben, wenn sie nicht benötigt werden oder dem richtigen übergeordneten Projekt zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52caf-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="52caf-149">Bei Aufgaben mit einer Dauer von mehr als 1.250 Tagen sollten Sie mehrere Aufgaben hinzufügen, um die Gesamtdauer darzustellen, sofern dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="52caf-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="52caf-150">Elemente, die mit einem Sternchen (\*) markiert sind, haben Begrenzungen, die daran liegen, dass die Kundenbeziehungsverwaltung (CRM) nur 7.320 Serienerweiterungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52caf-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="52caf-151">Sie müssen unter diesem Grenzwert bleiben.</span><span class="sxs-lookup"><span data-stu-id="52caf-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="52caf-152">Ressourcenarbeitsauftragbeziehungen</span><span class="sxs-lookup"><span data-stu-id="52caf-152">Resource Assignment relationships</span></span>
<span data-ttu-id="52caf-153">Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:</span><span class="sxs-lookup"><span data-stu-id="52caf-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="52caf-154">Alle Ressourcenarbeitsaufträge in einem Projektstrukturplan müssen mit demselben Projekt verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="52caf-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="52caf-155">Alle Ressourcenarbeitsaufträge in einem Projektstrukturplan müssen Projektteam-Mitgliedern im selben Projekt zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="52caf-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="52caf-156">Potentielle Risikominderungsschritte</span><span class="sxs-lookup"><span data-stu-id="52caf-156">Potential mitigation steps</span></span>
- <span data-ttu-id="52caf-157">Identifizieren Sie alle Aufgaben, die außerhalb der oben beschriebenen Bedingungen liegen.</span><span class="sxs-lookup"><span data-stu-id="52caf-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="52caf-158">Alle Ressourcenarbeitsaufträge, die nicht mehr gültig sind, sollten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="52caf-159">Projektaufgaben-Abhängigkeitsbeziehungen</span><span class="sxs-lookup"><span data-stu-id="52caf-159">Project task dependency relationships</span></span>
<span data-ttu-id="52caf-160">Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:</span><span class="sxs-lookup"><span data-stu-id="52caf-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="52caf-161">Alle Projektaufgabenabhängigkeiten müssen mit demselben Projekt verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="52caf-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="52caf-162">Auf eine Aufgabe kann nicht mehrmals dieselbe Abhängigkeit verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="52caf-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]