---
title: Projektfortschritt und Kostenverbrauch
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektfortschritts und des Kostenverbrauchs.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722034"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="97316-103">Projektfortschritt und Kostenverbrauch</span><span class="sxs-lookup"><span data-stu-id="97316-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="97316-104">Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche.</span><span class="sxs-lookup"><span data-stu-id="97316-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="97316-105">Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen.</span><span class="sxs-lookup"><span data-stu-id="97316-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="97316-106">Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="97316-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="97316-107">Aufwandsnachverfolgungsansicht</span><span class="sxs-lookup"><span data-stu-id="97316-107">Effort tracking view</span></span>

<span data-ttu-id="97316-108">Die Ansicht **Aufwandsnachverfolgung** nachverfolgt den Fortschritt von Aufgaben im Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="97316-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="97316-109">Sie vergleicht die tatsächlichen Aufwandsstunden für eine Aufgabe mit den geplanten Aufwandsstunden für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="97316-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="97316-110">PSA verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="97316-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="97316-111">Fortschritt in % = tatsächlicher bisheriger Aufwand ÷ geplanter Aufwand für die Aufgabe</span><span class="sxs-lookup"><span data-stu-id="97316-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="97316-112">Schätzung bis Abschluss (ETC) = geplanter Aufwand – tatsächlicher bisheriger Aufwand</span><span class="sxs-lookup"><span data-stu-id="97316-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="97316-113">Schätzung bei Abschluss (EAC) = verbleibender Aufwand + tatsächlicher bisheriger Aufwand</span><span class="sxs-lookup"><span data-stu-id="97316-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="97316-114">Hochgerechnete Aufwandsabweichung = geplanter Aufwand – EAC</span><span class="sxs-lookup"><span data-stu-id="97316-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="97316-115">PSA zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="97316-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="97316-116">Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird.</span><span class="sxs-lookup"><span data-stu-id="97316-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="97316-117">Daher liegt die Aufgabe im Zeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="97316-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="97316-118">Wenn die EAC kürzer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe schneller als ursprünglich geplant abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="97316-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="97316-119">Daher ist die Aufgabe im Zeitplan voraus.</span><span class="sxs-lookup"><span data-stu-id="97316-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="97316-120">Erneute Hochrechnung des Aufwands</span><span class="sxs-lookup"><span data-stu-id="97316-120">Re-projecting effort</span></span>

<span data-ttu-id="97316-121">Es ist üblich, das ein Projektmanager die ursprünglichen Vorkalkulationen für eine Aufgabe erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="97316-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="97316-122">Die erneute Hochrechnung für ein Projekt spiegelt die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider.</span><span class="sxs-lookup"><span data-stu-id="97316-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="97316-123">Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern, da die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.</span><span class="sxs-lookup"><span data-stu-id="97316-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="97316-124">Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für eine Aufgabe durchführen kann:</span><span class="sxs-lookup"><span data-stu-id="97316-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="97316-125">Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="97316-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="97316-126">Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="97316-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="97316-127">Jeder dieser Ansätze führt zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="97316-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="97316-128">Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.</span><span class="sxs-lookup"><span data-stu-id="97316-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="97316-129">Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="97316-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="97316-130">Der Aufwand für Zusammenfassungsaufgaben oder Behälteraufgaben kann erneut hochgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="97316-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="97316-131">Unabhängig davon, ob der Benutzer eine erneute Hochrechnung für die Zusammenfassungsaufgaben anhand des verbleibenden Aufwands oder des Fortschritts in Prozent durchführt, müssen folgende Berechnungen durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="97316-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="97316-132">Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.</span><span class="sxs-lookup"><span data-stu-id="97316-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="97316-133">Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.</span><span class="sxs-lookup"><span data-stu-id="97316-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="97316-134">Die neue EAC für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet.</span><span class="sxs-lookup"><span data-stu-id="97316-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="97316-135">Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten werden die ETC und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="97316-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="97316-136">Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="97316-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="97316-137">Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="97316-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="97316-138">Die Ansicht „Kostennachverfolgung“</span><span class="sxs-lookup"><span data-stu-id="97316-138">Cost tracking view</span></span> 

<span data-ttu-id="97316-139">Die Ansicht **Kostennachverfolgung** vergleicht die tatsächlichen Kosten für eine Aufgabe mit den geplanten Kosten dieser Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="97316-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="97316-140">Diese Ansicht enthält ausschließlich Arbeitskosten und keine Kosten aus den Ausgabenschätzungen.</span><span class="sxs-lookup"><span data-stu-id="97316-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="97316-141">PSA verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="97316-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="97316-142">Verbrauchte Kosten in Prozent = tatsächliche bisherige Kosten ÷ geplante Kosten für die Aufgabe</span><span class="sxs-lookup"><span data-stu-id="97316-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="97316-143">Kosten bis Abschluss (CTC) = geplante Kosten – tatsächliche bisherige Kosten</span><span class="sxs-lookup"><span data-stu-id="97316-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="97316-144">EAC = CTC + tatsächliche bisherige Kosten</span><span class="sxs-lookup"><span data-stu-id="97316-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="97316-145">Hochgerechnete Kostenabweichung = geplante Kosten – EAC</span><span class="sxs-lookup"><span data-stu-id="97316-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="97316-146">Eine Hochrechnung der Kostenabweichung für die Aufgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="97316-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="97316-147">Wenn die EAC größer als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe mehr als ursprünglich geplant kosten wird.</span><span class="sxs-lookup"><span data-stu-id="97316-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="97316-148">Daher tendiert sie zu einer Überschreitung des Budgets.</span><span class="sxs-lookup"><span data-stu-id="97316-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="97316-149">Wenn die EAC niedriger als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe weniger als ursprünglich geplant kosten wird.</span><span class="sxs-lookup"><span data-stu-id="97316-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="97316-150">Daher tendiert sie zu einer Unterschreitung des Budgets.</span><span class="sxs-lookup"><span data-stu-id="97316-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="97316-151">Erneute Kostenhochrechnung des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="97316-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="97316-152">Wenn für den Aufwand eine erneute Hochrechnung durchgeführt wird, werden die CTC, die EAC, die verbrauchten Kosten in Prozent und die hochgerechnete Kostenabweichung in der Ansicht **Kostennachverfolgung** neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="97316-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="97316-153">Zusammenfassung des Projektstatus</span><span class="sxs-lookup"><span data-stu-id="97316-153">Project status summary</span></span>

<span data-ttu-id="97316-154">Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an.</span><span class="sxs-lookup"><span data-stu-id="97316-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="97316-155">Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.</span><span class="sxs-lookup"><span data-stu-id="97316-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="97316-156">Felder der Statuszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="97316-156">Status summary fields</span></span>

<span data-ttu-id="97316-157">Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an.</span><span class="sxs-lookup"><span data-stu-id="97316-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="97316-158">Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="97316-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="97316-159">Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben.</span><span class="sxs-lookup"><span data-stu-id="97316-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="97316-160">Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="97316-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="97316-161">Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97316-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="97316-162">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="97316-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="97316-163">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="97316-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
