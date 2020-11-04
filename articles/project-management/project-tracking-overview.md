---
title: Projektverfolgung – Übersicht
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektfortschritts und des Kostenverbrauchs.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076375"
---
# <a name="project-tracking-overview"></a><span data-ttu-id="b2fab-103">Projektverfolgung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="b2fab-103">Project tracking overview</span></span>

<span data-ttu-id="b2fab-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="b2fab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2fab-105">Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche.</span><span class="sxs-lookup"><span data-stu-id="b2fab-105">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="b2fab-106">Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-106">Some industries track at a granular level, where other industries track at a higher level.</span></span> <span data-ttu-id="b2fab-107">Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-107">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="b2fab-108">Aufwandsnachverfolgungsansicht</span><span class="sxs-lookup"><span data-stu-id="b2fab-108">Effort tracking view</span></span>

<span data-ttu-id="b2fab-109">Die Ansicht **Aufwandsnachverfolgung** verfolgt den Fortschritt von Aufgaben im Zeitplan, indem die für eine Aufgabe aufgewendeten tatsächlichen Arbeitsstunden mit den geplanten Arbeitsstunden der Aufgabe verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b2fab-109">The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="b2fab-110">Dynamics 365 Project Operations verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="b2fab-110">Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="b2fab-111">**Fortschritt in Prozent** : Tatsächlicher bisheriger Aufwand ÷ Schätzung bei Fertigstellung (EAC)</span><span class="sxs-lookup"><span data-stu-id="b2fab-111">**Progress percentage** : Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="b2fab-112">**Schätzung bis Abschluss (ETC)** : Geplanter Aufwand – tatsächlicher bisheriger Aufwand</span><span class="sxs-lookup"><span data-stu-id="b2fab-112">**Estimate to complete (ETC)** : Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="b2fab-113">**EAC** : Verbleibender Aufwand + Tatsächlicher bisheriger Aufwand</span><span class="sxs-lookup"><span data-stu-id="b2fab-113">**EAC** : Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="b2fab-114">**Hochgerechnete Aufwandsabweichung** : Geplanter Aufwand – EAC</span><span class="sxs-lookup"><span data-stu-id="b2fab-114">**Projected effort variance** : Planned effort – EAC</span></span>

<span data-ttu-id="b2fab-115">Project Operations zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="b2fab-115">Project Operations shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="b2fab-116">Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird und hinter dem Zeitplan zurückliegt.</span><span class="sxs-lookup"><span data-stu-id="b2fab-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule.</span></span> <span data-ttu-id="b2fab-117">Wenn die EAC kleiner ist als der geplante Aufwand, wird prognostiziert, dass die Aufgabe kürzer als ursprünglich geplant dauern wird und vor dem Zeitplan liegt.</span><span class="sxs-lookup"><span data-stu-id="b2fab-117">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="b2fab-118">Erneute Hochrechnung des Aufwands</span><span class="sxs-lookup"><span data-stu-id="b2fab-118">Reprojecting effort</span></span>

<span data-ttu-id="b2fab-119">Projektmanager überprüfen häufig die ursprünglichen Vorkalkulationen für eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="b2fab-119">Project managers often revise the original estimates on a task.</span></span> <span data-ttu-id="b2fab-120">Erneute Hochrechnungen für ein Projekt spiegeln die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider.</span><span class="sxs-lookup"><span data-stu-id="b2fab-120">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="b2fab-121">Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b2fab-121">However, we don't recommend that project managers change the baseline numbers.</span></span> <span data-ttu-id="b2fab-122">Dies hängt damit zusammen, dass die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.</span><span class="sxs-lookup"><span data-stu-id="b2fab-122">This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="b2fab-123">Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für Aufgaben durchführen kann:</span><span class="sxs-lookup"><span data-stu-id="b2fab-123">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="b2fab-124">Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-124">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="b2fab-125">Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-125">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="b2fab-126">Jeder Ansatz führt zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="b2fab-126">Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="b2fab-127">Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.</span><span class="sxs-lookup"><span data-stu-id="b2fab-127">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="b2fab-128">Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="b2fab-128">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="b2fab-129">Der Aufwand für Zusammenfassungsaufgaben oder Containeraufgaben kann erneut hochgerechnet werden.</span><span class="sxs-lookup"><span data-stu-id="b2fab-129">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="b2fab-130">Unabhängig davon, ob der Benutzer eine erneute Hochrechnung für die Zusammenfassungsaufgaben anhand des verbleibenden Aufwands oder des Fortschritts in Prozent durchführt, müssen folgende Berechnungen durchgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b2fab-130">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="b2fab-131">Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.</span><span class="sxs-lookup"><span data-stu-id="b2fab-131">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="b2fab-132">Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.</span><span class="sxs-lookup"><span data-stu-id="b2fab-132">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="b2fab-133">Die neuen BK für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet.</span><span class="sxs-lookup"><span data-stu-id="b2fab-133">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="b2fab-134">Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten werden die ETC und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="b2fab-134">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="b2fab-135">Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="b2fab-135">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="b2fab-136">Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="b2fab-136">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="b2fab-137">Die Ansicht „Kostennachverfolgung“</span><span class="sxs-lookup"><span data-stu-id="b2fab-137">Cost tracking view</span></span> 

<span data-ttu-id="b2fab-138">Die Ansicht **Kostennachverfolgung** vergleicht die tatsächlichen Kosten für eine Aufgabe mit den geplanten Kosten dieser Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="b2fab-138">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="b2fab-139">Diese Ansicht enthält ausschließlich Arbeitskosten und keine Kosten aus den Ausgabenschätzungen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-139">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> <span data-ttu-id="b2fab-140">Project Operations verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:</span><span class="sxs-lookup"><span data-stu-id="b2fab-140">Project Operations uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="b2fab-141">**Verbrauchte Kosten in Prozent** : Tatsächliche bisherige Kosten ÷ Geschätzte Kosten bei Abschluss</span><span class="sxs-lookup"><span data-stu-id="b2fab-141">**Percentage of cost consumed** : Actual cost spent to date ÷ Estimated cost at completion</span></span>
- <span data-ttu-id="b2fab-142">**Kosten bis Abschluss (CTC)** : Geplante Kosten – Tatsächliche bisherige Kosten</span><span class="sxs-lookup"><span data-stu-id="b2fab-142">**Cost to complete (CTC)** : Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="b2fab-143">**EAC** : Verbleibende Kosten + Istkosten, die bis heute bezahlt wurden</span><span class="sxs-lookup"><span data-stu-id="b2fab-143">**EAC** : Remaining cost + Actual cost spent to date</span></span>
- <span data-ttu-id="b2fab-144">**Hochgerechnete Kostenabweichung** : Geplante Kosten – EAC</span><span class="sxs-lookup"><span data-stu-id="b2fab-144">**Projected cost variance** : Planned cost – EAC</span></span>

<span data-ttu-id="b2fab-145">Eine Hochrechnung der Kostenabweichung für die Aufgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2fab-145">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="b2fab-146">Wenn die EAC größer als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe mehr als ursprünglich geplant kosten wird.</span><span class="sxs-lookup"><span data-stu-id="b2fab-146">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="b2fab-147">Daher tendiert sie zu einer Überschreitung des Budgets.</span><span class="sxs-lookup"><span data-stu-id="b2fab-147">Therefore, it's trending over budget.</span></span> <span data-ttu-id="b2fab-148">Wenn die EAC niedriger als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe weniger als ursprünglich geplant kosten wird.</span><span class="sxs-lookup"><span data-stu-id="b2fab-148">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="b2fab-149">Daher tendiert sie zu einer Unterschreitung des Budgets.</span><span class="sxs-lookup"><span data-stu-id="b2fab-149">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="b2fab-150">Erneute Kostenhochrechnung des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="b2fab-150">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="b2fab-151">Wenn für den Aufwand eine erneute Hochrechnung durchgeführt wird, werden die CTC, die BK, die verbrauchten Kosten in Prozent und die hochgerechnete Kostenabweichung in der Ansicht **Kostennachverfolgung** neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="b2fab-151">When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="b2fab-152">Zusammenfassung des Projektstatus</span><span class="sxs-lookup"><span data-stu-id="b2fab-152">Project status summary</span></span>

<span data-ttu-id="b2fab-153">Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an.</span><span class="sxs-lookup"><span data-stu-id="b2fab-153">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="b2fab-154">Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.</span><span class="sxs-lookup"><span data-stu-id="b2fab-154">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="b2fab-155">Felder der Statuszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="b2fab-155">Status summary fields</span></span>

<span data-ttu-id="b2fab-156">Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an.</span><span class="sxs-lookup"><span data-stu-id="b2fab-156">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="b2fab-157">Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-157">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="b2fab-158">Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben.</span><span class="sxs-lookup"><span data-stu-id="b2fab-158">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="b2fab-159">Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b2fab-159">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="b2fab-160">Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b2fab-160">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="b2fab-161">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-161">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="b2fab-162">Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.</span><span class="sxs-lookup"><span data-stu-id="b2fab-162">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>