---
title: Änderungen bei der Ressourcenverwaltung (Project Service Automation 3.x)
description: Dieses Thema enthält Informationen zu den Änderungen am Ressourcenverwaltungsbereich.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076715"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="3d172-103">Änderungen bei der Ressourcenverwaltung (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="3d172-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="3d172-104">Die Abschnitte dieses Themas bieten Informationen zu den Änderungen, die am Ressourcenverwaltungsbereich von Dynamics 365 Project Service Automation Version 3.x vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="3d172-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="3d172-105">Projektschätzungen</span><span class="sxs-lookup"><span data-stu-id="3d172-105">Project estimates</span></span>

<span data-ttu-id="3d172-106">Statt auf der Entität **msdyn\_projecttask** ( **Projektaufgabe** ) basieren Projektvorkalkulationen auf der Entität **msdyn\_resourceassignment** ( **Ressourcenzuweisung** ).</span><span class="sxs-lookup"><span data-stu-id="3d172-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="3d172-107">Ressourcenzuweisungen haben sich zur „Quelle der Wahrheit“ für Aufgabenplanung und Preisberechnung entwickelt.</span><span class="sxs-lookup"><span data-stu-id="3d172-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="3d172-108">Positionsaufgaben</span><span class="sxs-lookup"><span data-stu-id="3d172-108">Line tasks</span></span>

<span data-ttu-id="3d172-109">In PSA 3.x sind Positionsaufgaben veraltet.</span><span class="sxs-lookup"><span data-stu-id="3d172-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="3d172-110">Zuweisungen zeigen jetzt auf die gesamte Aufgabe statt auf die Positionsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="3d172-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="3d172-111">Das folgende Beispiel zeigt, wie eine Aufgabe mit der Bezeichnung „Testaufgabe“ in früheren Versionen von PSA und in PSA 3.x den Teammitgliedern A und B zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3d172-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="3d172-112">**Vor PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="3d172-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="3d172-113">Testaufgabe</span><span class="sxs-lookup"><span data-stu-id="3d172-113">Test task</span></span>

        - <span data-ttu-id="3d172-114">Testaufgabe – Positionsaufgabe 1</span><span class="sxs-lookup"><span data-stu-id="3d172-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="3d172-115">Zuweisung zu A</span><span class="sxs-lookup"><span data-stu-id="3d172-115">Assignment to A</span></span>

        - <span data-ttu-id="3d172-116">Testaufgabe – Positionsaufgabe 2</span><span class="sxs-lookup"><span data-stu-id="3d172-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="3d172-117">Zuweisung zu B</span><span class="sxs-lookup"><span data-stu-id="3d172-117">Assignment to B</span></span>

- <span data-ttu-id="3d172-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="3d172-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="3d172-119">Testaufgabe</span><span class="sxs-lookup"><span data-stu-id="3d172-119">Test task</span></span>

        - <span data-ttu-id="3d172-120">Zuweisung zu A</span><span class="sxs-lookup"><span data-stu-id="3d172-120">Assignment to A</span></span>
        - <span data-ttu-id="3d172-121">Zuweisung zu B</span><span class="sxs-lookup"><span data-stu-id="3d172-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="3d172-122">Nicht zugewiesene Zuweisung</span><span class="sxs-lookup"><span data-stu-id="3d172-122">Unassigned assignment</span></span>

<span data-ttu-id="3d172-123">In PSA 3.x handelt es sich bei einer nicht zugewiesenen Zuweisung um eine Zuweisung, die einem Teammitglied **NULL** und einer Ressource **NULL** zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3d172-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="3d172-124">Nicht zugewiesene Zuweisungen können in verschiedenen Szenarien auftreten:</span><span class="sxs-lookup"><span data-stu-id="3d172-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="3d172-125">Wenn eine Aufgabe erstellt wurde, die bisher noch keinem Teammitglied zugewiesen wurde, wird immer eine nicht zugewiesene Zuweisung erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d172-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="3d172-126">Wenn alle Zugewiesenen für eine Aufgabe entfernt werden, wird für diese Aufgabe eine nicht zugewiesene Zuweisung erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d172-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="3d172-127">Planungsfelder auf der Projektaufgabenentität</span><span class="sxs-lookup"><span data-stu-id="3d172-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="3d172-128">Die Felder auf der Entität **msdyn\_projecttask** sind veraltet oder wurden zur Entität **msdyn\_resourceassignment** verschoben oder werden jetzt von der Entität **msdyn\_projectteam** ( **Projektteammitglied** ) referenziert.</span><span class="sxs-lookup"><span data-stu-id="3d172-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="3d172-129">Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe)</span><span class="sxs-lookup"><span data-stu-id="3d172-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="3d172-130">Neues Feld auf msdyn\_resourceassignment (Ressourcenzuweisung)</span><span class="sxs-lookup"><span data-stu-id="3d172-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="3d172-131">Kommentar</span><span class="sxs-lookup"><span data-stu-id="3d172-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="3d172-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="3d172-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="3d172-133">Keine</span><span class="sxs-lookup"><span data-stu-id="3d172-133">None</span></span> | |
| <span data-ttu-id="3d172-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="3d172-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="3d172-135">Keine</span><span class="sxs-lookup"><span data-stu-id="3d172-135">None</span></span> | |
| <span data-ttu-id="3d172-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="3d172-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="3d172-137">Keine</span><span class="sxs-lookup"><span data-stu-id="3d172-137">None</span></span> | |
| <span data-ttu-id="3d172-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="3d172-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="3d172-139">Keine</span><span class="sxs-lookup"><span data-stu-id="3d172-139">None</span></span> | |
| <span data-ttu-id="3d172-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="3d172-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="3d172-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="3d172-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="3d172-142">Das Format der Datenstruktur JavaScript Object Notation (JSON), die im Feld gespeichert ist, wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="3d172-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="3d172-143">Zeitplankontur</span><span class="sxs-lookup"><span data-stu-id="3d172-143">Schedule contour</span></span>

<span data-ttu-id="3d172-144">Die Zeitplankontur wird im Feld **Geplante Arbeit** ( **msdyn\_plannedwork** ) der einzelnen Entitäten **Ressourcenzuweisung** ( **msdyn\_resourceassignment** ) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3d172-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="3d172-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="3d172-145">Structure</span></span>

<span data-ttu-id="3d172-146">Die neue Struktur der Zeitplankontur besteht aus flexiblen Zeiterfassungen, die für jeden Tag des Zeitplans definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3d172-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="3d172-147">Jede Zeiterfassung hat folgende Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3d172-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="3d172-148">**Start**  – Der Start der Arbeitsstunden für den Tag laut Projektkalender.</span><span class="sxs-lookup"><span data-stu-id="3d172-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="3d172-149">**Ende**  – Das Ende der Arbeitsstunden für den Tag laut Projektkalender.</span><span class="sxs-lookup"><span data-stu-id="3d172-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="3d172-150">**Stunden**  – Die Stundenzahl, die am Tag zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3d172-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="3d172-151">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3d172-151">**Example**</span></span>

<span data-ttu-id="3d172-152">In diesem Beispiel wird ein Projektkalender wird ein Arbeitstag von 9:00 Uhr bis 17:00 Uhr in der UTC-8-Zeitzone verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d172-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="3d172-153">Automatische und manuelle Zeitplanung</span><span class="sxs-lookup"><span data-stu-id="3d172-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="3d172-154">Wenn die Zeitplanung für eine Aufgabe automatisch erfolgt, werden die Stunden vorab geladen und die Aufgabendauer kann sich verkürzen.</span><span class="sxs-lookup"><span data-stu-id="3d172-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="3d172-155">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3d172-155">**Example**</span></span>

<span data-ttu-id="3d172-156">Die folgende Aufgabe wurde automatisch für 18 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).</span><span class="sxs-lookup"><span data-stu-id="3d172-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="3d172-157">Wenn eine Aufgabe manuell geplant wird, werden die Stunden gleichmäßig auf alle Tage verteilt.</span><span class="sxs-lookup"><span data-stu-id="3d172-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="3d172-158">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3d172-158">**Example**</span></span>

<span data-ttu-id="3d172-159">Die folgende Aufgabe wurde manuell für 18 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).</span><span class="sxs-lookup"><span data-stu-id="3d172-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="3d172-160">Zuweisungseinheit</span><span class="sxs-lookup"><span data-stu-id="3d172-160">Assignment unit</span></span>

<span data-ttu-id="3d172-161">Die Zuweisungseinheit ist in PSA 3.x. veraltet.</span><span class="sxs-lookup"><span data-stu-id="3d172-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="3d172-162">Die Aufgabenaufwandsstunden wurden pro Tag gleichmäßig unter allen zugewiesenen Ressourcen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="3d172-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="3d172-163">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="3d172-163">**Example**</span></span>

<span data-ttu-id="3d172-164">In diesem Beispiel wird die Aufgabe zwei Ressourcen zugewiesen und automatisch für 36 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).</span><span class="sxs-lookup"><span data-stu-id="3d172-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="3d172-165">Zuweisung 1:</span><span class="sxs-lookup"><span data-stu-id="3d172-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="3d172-166">Zuweisung 2:</span><span class="sxs-lookup"><span data-stu-id="3d172-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="3d172-167">Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="3d172-167">Pricing dimensions</span></span>

<span data-ttu-id="3d172-168">In PSA 3.x wurden Preisdimensions-Felder (z. B. **Rolle** und **Organisationseinheit** ) aus der Entität **msdyn\_projecttask** entfernt.</span><span class="sxs-lookup"><span data-stu-id="3d172-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="3d172-169">Diese Felder können jetzt vom entsprechenden Projektteammitglied ( **msdyn\_projectteam** ) der Ressourcenzuweisung ( **msdyn\_resourceassignment** ) abgerufen werden, wenn Projektvorkalkulationen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="3d172-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="3d172-170">Das neue Feld **msdyn\_organizationalunit** wurde der Entität **msdyn\_projectteam** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3d172-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="3d172-171">Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe)</span><span class="sxs-lookup"><span data-stu-id="3d172-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="3d172-172">Feld von msdyn\_projectteam (Projektteammitglied), das stattdessen verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3d172-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="3d172-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="3d172-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="3d172-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="3d172-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="3d172-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="3d172-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="3d172-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="3d172-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="3d172-177">Konturen</span><span class="sxs-lookup"><span data-stu-id="3d172-177">Contours</span></span>

<span data-ttu-id="3d172-178">Die Konturfelder für die Preisberechnung und die Vorkalkulationen sind auf der Entität **msdyn\_projecttask** nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3d172-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="3d172-179">Sie wurden zur Entität **msdyn\_resourceassignment** verschoben.</span><span class="sxs-lookup"><span data-stu-id="3d172-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="3d172-180">Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe)</span><span class="sxs-lookup"><span data-stu-id="3d172-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="3d172-181">Neues Feld auf msdyn\_resourceassignment (Ressourcenzuweisung)</span><span class="sxs-lookup"><span data-stu-id="3d172-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="3d172-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="3d172-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="3d172-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="3d172-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="3d172-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="3d172-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="3d172-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="3d172-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="3d172-186">Die folgenden Felder wurden der Entität **msdyn\_resourceassignment** hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3d172-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="3d172-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3d172-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="3d172-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3d172-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="3d172-189">Die folgenden Felder für geplante, tatsächliche und verbleibende Kosten und Vertrieb auf der Entität **msdyn\_projecttask** bleiben unverändert:</span><span class="sxs-lookup"><span data-stu-id="3d172-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="3d172-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="3d172-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="3d172-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="3d172-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="3d172-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="3d172-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="3d172-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="3d172-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="3d172-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="3d172-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="3d172-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="3d172-195">msdyn\_remainingsales</span></span>
