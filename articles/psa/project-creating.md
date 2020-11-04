---
title: Projektzeitpläne
description: Dieses Thema bietet Informationen zur Vorgehensweise beim Erstellen von Zeitplänen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076559"
---
# <a name="project-schedules"></a><span data-ttu-id="9df4a-103">Projektzeitpläne</span><span class="sxs-lookup"><span data-stu-id="9df4a-103">Project schedules</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9df4a-104">Ein Projektzeitplan teilt mit, welche Arbeit durchgeführt werden muss, welche Ressourcen die Arbeit durchführen und in welchem Zeitrahmen diese Arbeit abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="9df4a-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="9df4a-105">Der Projektzeitplan reflektiert die gesamte Arbeit, die mit dem rechtzeitigen Liefern des Projektes verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="9df4a-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="9df4a-106">In Dynamics 365 Project Service Automation, erstellen Sie einen Projektzeitplan, indem Sie den Arbeitsumfang in überschaubaren Aufgaben einteilen, die für jede Aufgabe erforderliche Zeit schätzen, Aufgabenabhängigkeiten festlegen, Aufgabendauern einstellen und die allgemeine Ressourcen abschätzen, die die Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="9df4a-107">Der Projektzeitplan wird auf der Registerkarte **Zeitplan** der Projektseite erstellt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="9df4a-108">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="9df4a-108">Tasks</span></span>

<span data-ttu-id="9df4a-109">Der erste Schritt beim Erstellen eines Projektzeitplans ist die Aufteilung der Arbeit in überschaubare Portionen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="9df4a-110">Der Zeitplan in PSA unterstützt die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="9df4a-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="9df4a-111">Projektstammknoten.</span><span class="sxs-lookup"><span data-stu-id="9df4a-111">Project root node</span></span>
- <span data-ttu-id="9df4a-112">Zusammenfassende oder Behälteraufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-112">Summary or container tasks</span></span>
- <span data-ttu-id="9df4a-113">Blattknotenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="9df4a-114">Projektstammknoten.</span><span class="sxs-lookup"><span data-stu-id="9df4a-114">Project root node</span></span>

<span data-ttu-id="9df4a-115">Der Projektstammknoten ist die Aufgabenzusammenfassung auf oberster Ebene für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="9df4a-116">Alle weiteren Projektaufgaben werden darunter erstellt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-116">All other project tasks are created under it.</span></span> <span data-ttu-id="9df4a-117">Der Name der Stammknotens ist immer auf den Projektnamen eingestellt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="9df4a-118">Der Aufwand, die Termine und die Dauer des Stammknotens werden, basierend auf den Werten auf der Hierarchie darunter, zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="9df4a-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="9df4a-119">Sie können die Eigenschaften des Stammknotens nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9df4a-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="9df4a-120">Sie können den Stammknoten auch nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="9df4a-121">Zusammenfassende oder Behälteraufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-121">Summary or container tasks</span></span> 

<span data-ttu-id="9df4a-122">Zusammenfassende Aufgaben haben Unteraufgaben oder Containeraufgaben darunter.</span><span class="sxs-lookup"><span data-stu-id="9df4a-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="9df4a-123">Sie haben keinen eigenen Arbeitsaufwand oder Kosten.</span><span class="sxs-lookup"><span data-stu-id="9df4a-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="9df4a-124">Stattdessen sind ihr Arbeitsaufwand und die Kosten ein Rollup der Arbeitsaufwands und der Kosten ihrer Containeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="9df4a-125">Das Startdatum der zusammenfassenden Aufgabe ist das Startdatum der Containeraufgaben, und das Enddatum ist das Enddatum der Containeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="9df4a-126">Der Name einer zusammenfassenden Aufgabe kann bearbeitet werden aber Zeitplanungseigenschaften (Aufwand,Termine und Dauer) können nicht bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="9df4a-127">Wenn Sie eine zusammenfassende Aufgabe löschen, dann löschen Sie auch all ihre Containeraufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="9df4a-128">Blattknotenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-128">Leaf node tasks</span></span>

<span data-ttu-id="9df4a-129">Blattknotenaufgaben stellt die Detailarbeit im Projekt dar.</span><span class="sxs-lookup"><span data-stu-id="9df4a-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="9df4a-130">Sie haben einen geschätzten Aufwand, geschätzte Ressourcen, geplante Start- und Enddaten und eine Dauer.</span><span class="sxs-lookup"><span data-stu-id="9df4a-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="9df4a-131">Erstellen einer Aufgabenhierarchie</span><span class="sxs-lookup"><span data-stu-id="9df4a-131">Creating a task hierarchy</span></span>

<span data-ttu-id="9df4a-132">Sie haben die folgenden Optionen zum Erstellen einer Aufgabenhierarchie:</span><span class="sxs-lookup"><span data-stu-id="9df4a-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="9df4a-133">**Aufgabe hinzufügen** Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9df4a-133">**Add task** button</span></span>
- <span data-ttu-id="9df4a-134">**Aufgabe einrücken** Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9df4a-134">**Indent task** button</span></span>
- <span data-ttu-id="9df4a-135">**Aufgabe ausücken** Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9df4a-135">**Outdent task** button</span></span>
- <span data-ttu-id="9df4a-136">**Nach oben verschieben** und **Nach unten verschieben** Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="9df4a-137">Barrierefreiheit und Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="9df4a-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="9df4a-138">Aufgabe hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9df4a-138">Add task</span></span>

<span data-ttu-id="9df4a-139">Mit der Schaltfläche **Aufgabe hinzufügen** können Sie eine neue Aufgabe in der Hierarchie erstellen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="9df4a-140">Wenn Sie keine Position auswählen, wird Ihre Aufgabe am Ende eingefügt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="9df4a-141">Eine Zeitplan-ID ist jeder Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="9df4a-142">Die Zeitplan-ID stellt die Tiefe der Aufgabe und Position in der Hierarchie dar.</span><span class="sxs-lookup"><span data-stu-id="9df4a-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="9df4a-143">Sie verwendet Gliederungsnummerierung.</span><span class="sxs-lookup"><span data-stu-id="9df4a-143">It uses outline numbering.</span></span> <span data-ttu-id="9df4a-144">Für Aufgaben in der ersten Ebene unter dem Projektstammknoten wird ein Nummerierungsschema von 1, 2, 3 usw. verwendet.</span><span class="sxs-lookup"><span data-stu-id="9df4a-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="9df4a-145">Für Aufgaben unter der ersten Ebene wird ein Nummerierungsschema von 1.1, 1.2, 1.3 usw. verwendet.</span><span class="sxs-lookup"><span data-stu-id="9df4a-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="9df4a-146">Aufgabe einrücken.</span><span class="sxs-lookup"><span data-stu-id="9df4a-146">Indent task</span></span>

<span data-ttu-id="9df4a-147">Wenn eine Aufgabe eingerückt ist, wird es ein untergeordnetes Element der direkt darüberstehenden Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9df4a-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="9df4a-148">Die Zeitplan-ID der Aufgabe wird dann neu berechnet, damit sie auf der Zeitplan-ID seines neuen übergeordneten Elements basiert und dem Gliederungsnummerierungsschema folgt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="9df4a-149">Die übergeordnete Aufgabe ist jetzt eine zusammenfassende Aufgabe oder eine Containeraufgabe.</span><span class="sxs-lookup"><span data-stu-id="9df4a-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="9df4a-150">Daher wird es ein Rollup der untergeordneten Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="9df4a-151">Aufgabe ausrücken.</span><span class="sxs-lookup"><span data-stu-id="9df4a-151">Outdent task</span></span> 

<span data-ttu-id="9df4a-152">Wenn eine Aufgabe ausgerückt wird, ist sie nicht mehr ein untergeordnetes Element der Aufgabe, die ihr übergeordnetes Element war.</span><span class="sxs-lookup"><span data-stu-id="9df4a-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="9df4a-153">Die Zeitplan-ID wird dann neu berechnet, sodass sie die aktualisierte Tiefe und Position der Aufgabe in der Hierarchie widergibt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="9df4a-154">Der Aufwand, die Kosten und Datumsangaben der vorherigen übergeordneten Aufgabe werden neu berechnet, damit sie diese Aufgabe nicht mit einschließen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="9df4a-155">Nach oben und Nach unten verschieben</span><span class="sxs-lookup"><span data-stu-id="9df4a-155">Move up and Move down</span></span> 

<span data-ttu-id="9df4a-156">Die Schaltflächen **Nach oben** und **Nach unten** ändern die Position einer Aufgabe in ihrer übergeordneten Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="9df4a-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="9df4a-157">Änderungen dieser Art betreffen nicht den Aufwand, die Kosten, Datumsangaben oder Dauer der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9df4a-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="9df4a-158">Nur die Zeitplan-ID der Aufgabe ist betroffen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="9df4a-159">Die Zeitplan-ID wird neu berechnet, sodass sie die neue Position der Aufgabe in der übergeordneten Liste der untergeordneten Aufgaben widergibt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="9df4a-160">Barrierefreiheit und Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="9df4a-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="9df4a-161">Auf das Raster **Zeitplan** kann vollständig zugegriffen werden, und es kann mit Bildschirmlesern wie Narrator, JAWS oder NVDA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="9df4a-162">Sie können durch den Rasterbereich navigieren, indem Sie die Pfeiltasten (wie in Microsoft Excel) verwenden. Sie können die TAB-TASTE verwenden, um über die interaktiven Benutzeroberflächenelemente zu navigieren, und Sie können den ABWÄRTSPFEIL, die EINGABETASTE oder LEERTASTE verwenden, um die Dropdownmenüs auszuwählen und aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="9df4a-163">Die Spaltenüberschriften sind auch interaktiv.</span><span class="sxs-lookup"><span data-stu-id="9df4a-163">The column headers are also interactive.</span></span> <span data-ttu-id="9df4a-164">Sie können Spalten ausblenden und einblenden; verwenden Sie die TAB-TASTE und die PFEILTASTEN, um durch die Spaltenüberschriften zu navigieren, verwenden Sie die interaktiven Schaltflächen auf der Menüleiste.</span><span class="sxs-lookup"><span data-stu-id="9df4a-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="9df4a-165">Außerdem können Sie folgende Tastaturkürzel verwenden:</span><span class="sxs-lookup"><span data-stu-id="9df4a-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="9df4a-166">**Aktualisieren** : ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="9df4a-166">**Refresh** : ALT+SHIFT+F5</span></span>
- <span data-ttu-id="9df4a-167">**Hinzufügen** : ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="9df4a-167">**Add** : ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="9df4a-168">**Löschen** : ALT+SHIFT+Delete</span><span class="sxs-lookup"><span data-stu-id="9df4a-168">**Delete** : ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="9df4a-169">**Verschieben auf/ab** : ALT+SHIFT+Up-/Downpfeile</span><span class="sxs-lookup"><span data-stu-id="9df4a-169">**Move up/down** : ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="9df4a-170">**Einrücken/Ausrücken** : ALT_SHIFT+Links-/Rechtspfeile</span><span class="sxs-lookup"><span data-stu-id="9df4a-170">**Indent/Outdent** : ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="9df4a-171">**Hierarchien Erweitern/Reduzieren/** : ALT+SHIFT+Plus-/Minustasten</span><span class="sxs-lookup"><span data-stu-id="9df4a-171">**Expand/Collapse Hierarchies** : ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="9df4a-172">Aufgabenattribute</span><span class="sxs-lookup"><span data-stu-id="9df4a-172">Task attributes</span></span>

<span data-ttu-id="9df4a-173">Ein Aufgabenname beschreibt die Arbeit, die abgeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="9df4a-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="9df4a-174">In PSA beschreiben die Attribute, die einer Aufgabe zugeordnet sein, den Zeitplan der Aufgabe und das erforderliche Personal.</span><span class="sxs-lookup"><span data-stu-id="9df4a-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![Aufgabenattribute](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="9df4a-176">Zeitplanattribute.</span><span class="sxs-lookup"><span data-stu-id="9df4a-176">Schedule attributes</span></span>

<span data-ttu-id="9df4a-177">Die Attribute **Aufwand** , **Startdatum** , **Enddatum** und **Dauer** definieren den Zeitplan für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9df4a-177">The **Effort** , **Start date** , **End date** , and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="9df4a-178">Weitere Zeitplanattribute enthalten:</span><span class="sxs-lookup"><span data-stu-id="9df4a-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="9df4a-179">**Aufwandsstunden** : Geben Sie eine geschätzte Anzahl der Stunden ein, die erforderlich sind, um die Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-179">**Effort hours** : Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="9df4a-180">**Dauer** : Geben Sie die Anzahl der Arbeitstage an, die erforderlich sind, um die Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-180">**Duration** : Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="9df4a-181">**Zeitplan-ID** : Diese automatisch generierte ID wird verwendet, um Aufgaben in der Hierarchie anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-181">**Schedule ID** : This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="9df4a-182">Abhängigkeiten zwischen den Aufgaben verwalten die tatsächliche Reihenfolge, in der die Aufgaben bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="9df4a-183">Personalattributen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-183">Staffing attributes</span></span>

<span data-ttu-id="9df4a-184">Attribute der Personalbesetzung werden durch das Feld **Ressourcen** im Zeitplan angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="9df4a-185">Sie können entweder nach einer bestehenden Ressource suchen oder auf **Erstellen** klicken und im Fenster **Schnellerfassung** ein Projektteammitglied als neue Ressourcen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="9df4a-186">Die Felder **Rolle** , **Ressourcenzuordnungseinheit** und **Positionsname** werden verwendet, um die Personalanforderungen für die Aufgabe zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-186">The **Role** , **Resourcing Unit** , and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="9df4a-187">Diese Stellenbesetzungsattribute zusammen mit dem Aufgabenplan werden verwendet, um verfügbare Ressourcen zu finden, um diese Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="9df4a-188">**Rolle** – Geben Sie die Art der Ressource an, die für die Aufgabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9df4a-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="9df4a-189">**Ressourcenzuordnungseinheit** – Geben Sie die Einheit an, von der Ressourcen für die Aufgabe zugewiesen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="9df4a-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="9df4a-190">Dieses Attribut betrifft die Kosten- und Umsatzschätzung für die Aufgaben, wenn der Kosten- und Berechnungssatz für die Ressource auf Beschaffungseinheiten basieren.</span><span class="sxs-lookup"><span data-stu-id="9df4a-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="9df4a-191">**Positionsname** – Geben Sie einen Anzeigenamen für die allgemeine Ressource ein, der als Platzhalter für die Ressource dient, die letztendlich die Arbeit ausführen wird.</span><span class="sxs-lookup"><span data-stu-id="9df4a-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="9df4a-192">Das Feld **Ressourcen** enthält den Positionsnamen der generischen Ressource oder einer benannten Ressource , wenn eine gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="9df4a-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="9df4a-193">Das Feld **Kategorie** enthält die Werte, die eine breitere Art der Arbeit angeben, in denen die Aufgabe kategorisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9df4a-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="9df4a-194">Dieses Feld betrifft nicht die Zeitplanung oder die Stellenbesetzung.</span><span class="sxs-lookup"><span data-stu-id="9df4a-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="9df4a-195">Es wird nur für die Berichterstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9df4a-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="9df4a-196">Aufgabenabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="9df4a-196">Task dependencies</span></span> 

<span data-ttu-id="9df4a-197">Sie können den Zeitplan in PSA verwenden, um Vorgängerbeziehungen zwischen Aufgaben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="9df4a-198">Das Feld **Vorgänger** unter **Aufgaben** akzeptiert einen oder mehrere Werte, um die Aufgaben anzugeben, von denen eine Aufgabe abhängt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="9df4a-199">Wenn Vorgängerwerte einer Aufgabe zugewiesen werden, kann die Aufgabe nur beginnen, nachdem alle vorherigen Aufgaben abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="9df4a-200">Aufgrund der Abhängigkeit wird das geplante Startdatum der Aufgabe auf das Datum zurückgesetzt, an dem die Vorgängeraufgaben abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="9df4a-201">Der Aufgabenmodus hat keine Auswirkungen auf die Updates, die für das Start- und Enddatum vonVorgängern/abhängigen Aufgaben gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="9df4a-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="9df4a-202">Aufgabenmodus</span><span class="sxs-lookup"><span data-stu-id="9df4a-202">Task mode</span></span> 

<span data-ttu-id="9df4a-203">Der Aufgabenmodus bestimmt die Zeitplanung von Blattknotenaufgaben.</span><span class="sxs-lookup"><span data-stu-id="9df4a-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="9df4a-204">PSA unterstützt zwei Aufgabenmodi für jede Aufgabe: automatischer Zeitplanung und manuelle Zeitplanung.</span><span class="sxs-lookup"><span data-stu-id="9df4a-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="9df4a-205">Automatische Zeitplanung</span><span class="sxs-lookup"><span data-stu-id="9df4a-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="9df4a-206">Wenn der Aufgabenmodus auf **Automatisch geplant** für eine Aufgabe eingestellt ist, verwendet die Aufgabenzeitplanungsengine die Zeitplanungsregeln für die Aufgabenattribute, um den Zeitplan für die Aufgabe zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="9df4a-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="9df4a-207">Zeitplanungsregeln</span><span class="sxs-lookup"><span data-stu-id="9df4a-207">Scheduling rules</span></span>

<span data-ttu-id="9df4a-208">Wenn eine Blattknotenaufgabe keine Vorgänger hat, wird ihr Startdatum standardmäßig auf das geplante Startdatum des Projekts gesetzt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="9df4a-209">Die Dauer einer Blattknotenaufgabe wird immer als die Anzahl der Werktage zwischen seinem Anfangs- und Enddaten berechnet.</span><span class="sxs-lookup"><span data-stu-id="9df4a-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="9df4a-210">Wenn eine Aufgabe automatisch terminiert wird, folgt die Zeitplanungsengine diesen Regeln:</span><span class="sxs-lookup"><span data-stu-id="9df4a-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="9df4a-211">Start- und Enddaten der Aufgabe müssen Werktage entsprechend dem Terminplanungskalender des Projektes sein.</span><span class="sxs-lookup"><span data-stu-id="9df4a-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="9df4a-212">Für alle Aufgaben, die Vorgängeraufgaben haben, wird das Startdatum automatisch auf das späteste Enddatum seiner Vorgänger gesetzt.</span><span class="sxs-lookup"><span data-stu-id="9df4a-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="9df4a-213">Der Aufwand wird berechnet, indem diese Formel verwendet wird: Anzahl der Personen × Dauer × Stunden an einem Standardarbeitstag im Projektkalender.</span><span class="sxs-lookup"><span data-stu-id="9df4a-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="9df4a-214">Manuelle Terminierung</span><span class="sxs-lookup"><span data-stu-id="9df4a-214">Manual scheduling</span></span>

<span data-ttu-id="9df4a-215">Wenn die Regeln zur automatischen Zeitplanung Ihre Bedingungen nicht erfüllen, können Sie den Aufgabenmodus der Aufgabe auf **Manuell geplant** setzen.</span><span class="sxs-lookup"><span data-stu-id="9df4a-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="9df4a-216">Diese Einstellung stoppt die Zeitplanungsengine an der Berechnung der Werte anderer Zeitplanungsattribute.</span><span class="sxs-lookup"><span data-stu-id="9df4a-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="9df4a-217">Wenn Sie unabhängig vom Aufgabenmodus die Vorgänger auf Aufgaben einstellen, beeinflussen Sie immer das Startdatum der abhängigen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="9df4a-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>