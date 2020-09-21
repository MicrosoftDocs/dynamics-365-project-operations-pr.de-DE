---
title: Planen Sie ein Projekt mit einem Projektstrukturplan
description: Planen Sie ein Projekt mit einem Projektstrukturplan (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722024"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="c8d0d-103">Planen Sie ein Projekt mit einem Projektstrukturplan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c8d0d-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c8d0d-104">Ein Projektzeitplan teilt mit, welche Arbeit durchgeführt werden muss, welche Ressourcen die Arbeit durchführen und in welchem Zeitrahmen diese Arbeit abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="c8d0d-105">Der Projektzeitplan reflektiert die ganze Arbeit, die mit dem rechtzeitigen Liefern des Projektes verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="c8d0d-106">Einer der ersten Schritte in der Anfangsphase des Projektes ist, einen Projektzeitplan zu finden.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="c8d0d-107">Um einen Projektzeitplan zu erstellen, müssen Sie einen Projektstrukturplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="c8d0d-108">Erstellen Sie eine Projektstruktur mit einem Projektstrukturplan, der Ihnen bei Folgendem hilft:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="c8d0d-109">Gliedern der Arbeit in verwaltbare Aufgaben</span><span class="sxs-lookup"><span data-stu-id="c8d0d-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="c8d0d-110">Schätzen der Zeit, die erforderlich ist, um eine Aufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="c8d0d-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="c8d0d-111">Festlegen von Aufgabenabhängigkeiten und Aufgabendauer</span><span class="sxs-lookup"><span data-stu-id="c8d0d-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="c8d0d-112">Bestimmen der Rollen, die erforderlich sind, um jede Aufgabe abzuschließen</span><span class="sxs-lookup"><span data-stu-id="c8d0d-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="c8d0d-113">Der Projektzeitplan im Projektstrukturplan hat ein vertrautes Aussehen und Gefühl, einschließlich einem interaktiven Gantt-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="c8d0d-114">Erstellen eines Projektstrukturplans für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="c8d0d-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="c8d0d-115">Erstellen Sie einen Projektstrukturplan, um die Reihenfolge von Aufgaben in einem Projekt darzustellen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="c8d0d-116">Der Projektstrukturplan umfasst Aufgaben, Anforderungen für jede Aufgabe und Umsdatz- und Kosteninformationen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="c8d0d-117">In Ihrem Projektstrukturplan können Sie Folgendes hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="c8d0d-118">Die Reihenfolge von Aufgaben in einer Hierarchie</span><span class="sxs-lookup"><span data-stu-id="c8d0d-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="c8d0d-119">Andere Aufgaben, sofern vorhanden, die abgeschlossen werden müssen, bevor eine Aufgabe begonnen werden kann</span><span class="sxs-lookup"><span data-stu-id="c8d0d-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="c8d0d-120">Das Anfangsdatum, Enddatum und Dauer einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c8d0d-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="c8d0d-121">Die Anzahl von Stunden, die für eine Aufgabe erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="c8d0d-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="c8d0d-122">Alle erforderlichen Arbeitskraftfähigkeiten und -ausbildung</span><span class="sxs-lookup"><span data-stu-id="c8d0d-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="c8d0d-123">Die Arbeitskräfte, die einer Aufgabe zugewiesen werden</span><span class="sxs-lookup"><span data-stu-id="c8d0d-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="c8d0d-124">Geschätzter Umsatz und Kosten</span><span class="sxs-lookup"><span data-stu-id="c8d0d-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="c8d0d-125">Aufgabentypen</span><span class="sxs-lookup"><span data-stu-id="c8d0d-125">Task types</span></span>  
<span data-ttu-id="c8d0d-126">Sie benutzen die folgenden Aufgabentypen, wenn Ihr Projektstrukturplan erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="c8d0d-127">**Projektstammknoten**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-127">**Project root node**</span></span> | <span data-ttu-id="c8d0d-128">Die auf höchster Ebene zusammengefasste Aufgabe für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-128">The top-level summary task for the project.</span></span> <span data-ttu-id="c8d0d-129">Alle weiteren Projektaufgaben werden darunter erstellt.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-129">All other project tasks are created under it.</span></span> <span data-ttu-id="c8d0d-130">Der Name der Stammaufgabe ist der Projektname.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-130">The name of the root task is the project name.</span></span> <span data-ttu-id="c8d0d-131">Der Aufwand, die Daten und die Dauer des Stammknotens basieren auf den Werten auf der Hierarchie darunter.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="c8d0d-132">Sie können Stammknoteneigenschaften nicht bearbeiten oder den Stammnoten löschen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="c8d0d-133">**Zusammenfassende oder Behälteraufgaben**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-133">**Summary or container tasks**</span></span> | <span data-ttu-id="c8d0d-134">Eine zusammenfassende Aufgabe ist eine Aufgabe, die Teilaufgaben umfasst.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="c8d0d-135">Eine zusammenfassende Aufgabe hat keinen eigenen Arbeitsaufwand oder keine eigenen Kosten.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="c8d0d-136">Der Arbeitsaufwand und die Kosten sind ein Rollup der Teilaufgaben.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="c8d0d-137">Sie können den Namen einer zusammenfassenden Aufgabe ändern, aber Sie können den Aufwand, die Daten oder die Dauer nicht ändern, weil die automatisch berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="c8d0d-138">Das Löschen einer zusammenfassenden Aufgabe löscht die Aufgabe und alle Teilaufgaben.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="c8d0d-139">**Blattknotenaufgaben**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-139">**Leaf node tasks**</span></span> | <span data-ttu-id="c8d0d-140">Eine Blattknotenaufgabe stellt die Detailarbeit im Projekt dar.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="c8d0d-141">Sie hat einen geschätzten Aufwand, eine geplante Anzahl von Ressourcen, geplante Start- und Enddaten und eine Dauer.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="c8d0d-142">Aufgabenhierarchie</span><span class="sxs-lookup"><span data-stu-id="c8d0d-142">Task hierarchy</span></span>  
 <span data-ttu-id="c8d0d-143">Sie haben die folgenden Optionen, wenn Sie eine Aufgabenhierarchie erstellen:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="c8d0d-144">**Aufgabe hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-144">**Add task**.</span></span>   <span data-ttu-id="c8d0d-145">Sie können eine Aufgabe an einer Position hinzufügen, die Sie in der Aufgabenhierarchie auswählen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="c8d0d-146">Wenn Sie keine Position auswählen, erscheint Ihre neue Aufgabe am Ende.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="c8d0d-147">**Aufgabe herunterstufen**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-147">**Indent task**.</span></span>   <span data-ttu-id="c8d0d-148">Stufen Sie eine Aufgabe herunter, um eine untergeordnete Aufgabe von der darüber daraus zu machen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="c8d0d-149">**Aufgabe heraufstufen**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-149">**Outdent task**.</span></span>   <span data-ttu-id="c8d0d-150">Stufen Sie eine Aufgabe herauf, damit Sie keine Teilaufgabe der ursprünglichen übergeordneten Aufgabe mehr ist.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="c8d0d-151">**Nach oben oder unten verschieben**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-151">**Move up and Move down**.</span></span>   <span data-ttu-id="c8d0d-152">Verschieben Sie Aufgaben in der Hierarchie seiner übergeordneten Aufgaben hoch- und herunter.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="c8d0d-153">Das hoch und herunter Verschieben einer Aufgabe hat keinen Effekt auf Aufwand, Kosten, Daten oder Dauer.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="c8d0d-154">Aufgabenattribute</span><span class="sxs-lookup"><span data-stu-id="c8d0d-154">Task attributes</span></span>  
 <span data-ttu-id="c8d0d-155">Ein Aufgabenname beschreibt die Arbeit, die abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="c8d0d-156">Sie verwenden verschiedene Aufgabenattribute, um den Zeitplan und die Personalanforderungen für die Aufgabe zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="c8d0d-157">Zeitplanattribute.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-157">Schedule attributes</span></span>

 - <span data-ttu-id="c8d0d-158">Weisen Sie **Aufwandsstunden**, **Anzahl der Ressourcen**, **Startdatum**, **Enddatum** und **Dauer** Werte zu, um den Zeitplan für die Aufgabe zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="c8d0d-159">**Audwand** ist eine Schätzung der Stunden, die für den Abschluss der Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="c8d0d-160">**Anzahl der Ressourcen** ist eine Schätzung, die der Projektleiter für die Aufgabe angibt, um den bestmöglichen Zeitplan zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="c8d0d-161">**Dauer** (in Tagen) zeigt die Anzahl von Arbeitstagen an, die für den Abschluss der Aufgabe erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="c8d0d-162">Personalattributen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-162">Staffing attributes</span></span>

 - <span data-ttu-id="c8d0d-163">**Rollen**, **Organisationseinheit der Ressource**, **Anzahl der Ressourcen** und **Ressourcen** beschreiben die Personalanforderungen für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="c8d0d-164">**Rolle** beschreibt die Art der Ressource, die benötigt wird, um die Aufgabe durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="c8d0d-165">**Organisationseinheit der Ressource** zeigt die Organisationseinheit an, aus der Ressourcen für diese Aufgabe mit Personal besetzt werden sollten. Dies wirkt sich auch auf die Kosten und die Umsatzschätzung der Aufgabe aus, da es von Bedeutung ist, wenn der Verkaufspreis pro Einheit für die Ressource bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="c8d0d-166">**Ressourcen** enthält eine generische Ressource oder eine benannte Ressource, wenn eine gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="c8d0d-167">Aufgabenabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="c8d0d-167">Task dependencies</span></span>  
 <span data-ttu-id="c8d0d-168">Sie können Beziehungen zwischen einer oder mehreren vorherigen Aktivitäten im Projektstrukturplan erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="c8d0d-169">Sie können eine oder mehrere Werte für das Feld für vorherige Aktivitäten bei Aufgaben einstellen, um die Aufgaben anzuzeigen, von denen sie abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="c8d0d-170">Wenn Sie einer Aufgabe einen Wert für vorherige Aufgaben zuweisen, kann die Aufgabe nur beginnen, wenn alle vorherigen Aktivitäten abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="c8d0d-171">Die Einstellung dieser Abhängigkeit von einer Aufgabe ergibt die Neuberechnung des geplanten Anfangsdatums der Aufgabe als das späteste Ende von aller vorherigen Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="c8d0d-172">Auswirkungen durch vorherige Aktivitäten auf einen Zeitplan werden nicht durch den Aufgabenmodus begrenzt, der für die Aufgabe definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="c8d0d-173">Aufgabenmodus</span><span class="sxs-lookup"><span data-stu-id="c8d0d-173">Task mode</span></span>  
 <span data-ttu-id="c8d0d-174">Der Aufgabenmodus ist einer der wichtigen Faktoren bei der Bestimmung des Zeitplans für Blattknotenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="c8d0d-175">Es gibt zwei Aufgabenmodi für jede Aufgabe: automatischer Zeitplanmodus und manueller Zeitplanmodus.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="c8d0d-176">**Automatische Planung**</span><span class="sxs-lookup"><span data-stu-id="c8d0d-176">**Auto scheduling**.</span></span>   <span data-ttu-id="c8d0d-177">Wenn Sie den Aufgabenmodus auf "Automatisch geplant" einstellen, verwendet die Aufgabenplanungsengine die Zeitplanregeln für die folgenden Aufgabenattribute, um den Zeitplan für die Aufgabe zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="c8d0d-178">Vorherige Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="c8d0d-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="c8d0d-179">Aufwand</span><span class="sxs-lookup"><span data-stu-id="c8d0d-179">Effort</span></span>  
  
    -   <span data-ttu-id="c8d0d-180">Anzahl der Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8d0d-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="c8d0d-181">Start- und Enddatum</span><span class="sxs-lookup"><span data-stu-id="c8d0d-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="c8d0d-182">**Meine Buchungsregeln**</span><span class="sxs-lookup"><span data-stu-id="c8d0d-182">**Scheduling rules**.</span></span>   <span data-ttu-id="c8d0d-183">Das Startdatum der Blattknotenaufgabe ohne vorherige Aktivitäten ist standardmäßig das geplante Anfangsdatum des Projektes.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="c8d0d-184">Die Dauer einer Blattknotenaufgabe wird immer als die Anzahl der Werktage zwischen seinem Anfangs- und Enddaten berechnet.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="c8d0d-185">Wenn eine Aufgabe automatisch geplant wird, folgt die Planungsengine den Regeln unten:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="c8d0d-186">Start- und Enddaten einer Aufgabe müssen immer Werktage entsprechend dem Planungskalender des Projektes sein</span><span class="sxs-lookup"><span data-stu-id="c8d0d-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="c8d0d-187">Das Startdatum einer Aufgabe mit vorherigen Aktivitäten entspricht standardmäßig dem spätesten Enddatum seiner vorherigen Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="c8d0d-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="c8d0d-188">Aufwand = Anzahl der Menschen \* Dauer \* Stunden an einem Standardwerktag des Projektkalenders</span><span class="sxs-lookup"><span data-stu-id="c8d0d-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="c8d0d-189">**Planmanager**</span><span class="sxs-lookup"><span data-stu-id="c8d0d-189">**Manual scheduling**.</span></span>   <span data-ttu-id="c8d0d-190">In einigen Fällen sollten Sie von diesen Regeln abweichen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="c8d0d-191">In diesen Fällen können Sie den Aufgabenmodus auf manuelle Planung einstellen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="c8d0d-192">Das hindert die Planungsengine an der Berechnung der Werte für andere Planungsattribute.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="c8d0d-193">Das Einstellen von vorherigen Aktivitäten für Aufgaben wirkt sich immer auf das Startdatum der abhängigen Aufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="c8d0d-194">Erstellen eines Projektstrukturplans</span><span class="sxs-lookup"><span data-stu-id="c8d0d-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="c8d0d-195">Wechseln Sie zu **Project Service > Projekte**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="c8d0d-196">Klicken Sie auf das gewünschte Projekt.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="c8d0d-197">Wählen Sie auf der Leiste oben auf dem Bildschirm den Abwärtspfeil neben dem Projektnamen, und klicken Sie dann auf "Projektstrukturplan".</span><span class="sxs-lookup"><span data-stu-id="c8d0d-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="c8d0d-198">Um eine Aufgabe hinzuzufügen, klicken Sie auf **Aufgabe hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="c8d0d-199">Füllen Sie die Felder für die Aufgabe aus, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="c8d0d-200">Fügen Sie weiter Aufgaben hinzu, bis Ihr Projektstrukturplan vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="c8d0d-201">Bei der Erstellung Ihres Projektstrukturplans können Sie Folgendes tun, um Ihre Aufgaben zu organisieren:</span><span class="sxs-lookup"><span data-stu-id="c8d0d-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="c8d0d-202">Wählen Sie eine Aufgabe aus, und klicken Sie auf **Herunterstufen**, um sie unter eine andere Aufgabe zu verschieben oder klicken Sie auf "Höherstufen" , um sie eine ebene heraus zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="c8d0d-203">Wählen Sie eine Aufgabe aus, und klicken Sie auf **Nach oben** oder **Nach unten**, um sie in der Liste auf oder ab zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="c8d0d-204">Klicken Sie auf **Gantt ausblenden**, um das Gantt-Diagramm zu verbergen, und klicken Sie auf **Gantt anzeigen**, um es wieder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="c8d0d-205">Wählen Sie einen anderen Zeitabschnitt für das Gantt-Diagramm auf der **Zeitskala** aus.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="c8d0d-206">Um die Rollen hinzuzufügen, die Sie in Ihrem Projektstrukturplan für Ihre Projektteammitglieder angegeben haben, klicken Sie auf **Projektteam generieren**.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="c8d0d-207">Wenn Sie fertig mit den Änderungen sind, klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="c8d0d-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c8d0d-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8d0d-208">See Also</span></span>  
 [<span data-ttu-id="c8d0d-209">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="c8d0d-209">Project manager guide</span></span>](../project-service/project-manager-guide.md)
