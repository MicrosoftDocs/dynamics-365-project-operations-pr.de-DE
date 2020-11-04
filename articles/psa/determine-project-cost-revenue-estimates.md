---
title: Schätzungen bezüglich Arbeit, Kosten und Umsatz für ein Projekt bestimmen
description: Bestimmen von Projektkosten- und Umsatzschätzungen (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1652b39b6c8a703bf198a990eb9047eff9dc9f4c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076532"
---
# <a name="determine-project-cost-and-revenue-estimates"></a><span data-ttu-id="632f7-103">Schätzungen bezüglich Arbeit, Kosten und Umsatz für ein Projekt bestimmen</span><span class="sxs-lookup"><span data-stu-id="632f7-103">Determine project cost and revenue estimates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="632f7-104">Projekteinschätzungen stellen die Finanzansicht für die Arbeit bereit, die in der Projektstrukturplan des Projektes geschätzt und geplant wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-104">Project estimates provide the financial view for the work estimated and scheduled in the project’s work breakdown structure.</span></span> <span data-ttu-id="632f7-105">Die Schätzungsansicht informiert Sie über die Kosten und die Umsatzauswirkungen der geplanten Arbeit.</span><span class="sxs-lookup"><span data-stu-id="632f7-105">The estimates view informs you of the cost and revenue impact of the planned work.</span></span> <span data-ttu-id="632f7-106">Die Schätzungsansicht liefert ein Werkzeug, um die Informationen zu einer Reihe vorher festgelegter Dimensionen anzuzeigen, um Sie am besten über die Finanzauswirkung des Projektes zu informieren.</span><span class="sxs-lookup"><span data-stu-id="632f7-106">The estimates view provides a tool to see the information on a number of pre-defined dimensions to best inform you of the financial impact of the project.</span></span>  
  
## <a name="cost-and-sales-value-of-the-project"></a><span data-ttu-id="632f7-107">Kosten und Vertriebswert des Projektes</span><span class="sxs-lookup"><span data-stu-id="632f7-107">Cost and sales value of the project</span></span>  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="632f7-108">-Preislisten definieren die Kosten und die Rechnungssätze für Rollen, die in Projekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-108">price lists define the cost and bill rates for roles projects use.</span></span> <span data-ttu-id="632f7-109">Basierend auf den Rollen, die mit den Aufgaben in der Projektstrukturplan des Projektes verbunden sind, können Sie die Kosten und die Umsatzauswirkung der betroffenen Arbeit bestimmen.</span><span class="sxs-lookup"><span data-stu-id="632f7-109">Based on the roles associated with the tasks in the project’s work breakdown structure, you can determine the cost and revenue impact of the work involved.</span></span>  
  
## <a name="cost-price-defaulting"></a><span data-ttu-id="632f7-110">Standard-Einstandspreis</span><span class="sxs-lookup"><span data-stu-id="632f7-110">Cost price defaulting</span></span>  
<span data-ttu-id="632f7-111">Jedes Projekt gehört einer Organisation an (angezeigt in **Zuständige Einheit** im Projekt).</span><span class="sxs-lookup"><span data-stu-id="632f7-111">Every project belongs to an organization (indicated in **Owning Unit** in the project).</span></span> <span data-ttu-id="632f7-112">Die Preisliste, die mit der zuständigen Organisationseinheit verbunden ist, bestimmt den Einheitsselbstkostenpreis.</span><span class="sxs-lookup"><span data-stu-id="632f7-112">The price list associated with the owning organizational unit determines the unit cost price.</span></span> <span data-ttu-id="632f7-113">Die [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] bestimmen Kostenpreise für Rollen, indem nach der Kombination der Rolle, der Einheit und der Organisationseinheit in der Kostenpreisliste gesucht wird, um den korrekten Kostenpreises für das Datum zu erhalten, das auf Vorkalkulationspositionen wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-113">The [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] determine cost prices for roles by searching for the combination of role, unit, and organizational unit in the cost price list to get the correct cost price for the date effective on estimate lines.</span></span>  
  
<span data-ttu-id="632f7-114">Wenn die Kombination von Rolle, Einheit</span><span class="sxs-lookup"><span data-stu-id="632f7-114">If the combination of role, unit.</span></span> <span data-ttu-id="632f7-115">und Organisationseinheit keinen Kostenpreis aus der zuständigen Einheitspreisliste ergibt, wird die Einheit zugunsten der Kombination der Rolle und der Organisationseinheit verworfen.</span><span class="sxs-lookup"><span data-stu-id="632f7-115">and organizational unit doesn’t result in a cost price from the owning unit’s price list, the unit is disregarded in favor of the combination of role and organizational unit.</span></span> <span data-ttu-id="632f7-116">Wenn es einen Kostenpreis gibt, wird dieser Preis in die Einheit umgewandelt, die Sie auf der Vorkalkulationsposition ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="632f7-116">If there is a cost price, this price is converted to the unit you chose on the estimate line.</span></span>  
  
<span data-ttu-id="632f7-117">Wenn die Kombination der Rolle und der Organisationseinheit keinen Kostenpreis ergibt, wird die Organisationseinheit zugunsten der Rollen- und Einheitskombination verworfen, und der Preis wird auf den Standard zurückgesetzt, nachdem alle erforderlichen Umwandlungen angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="632f7-117">If the combination of role and organizational unit doesn’t result in a cost price, the organizational unit is disregarded in favor of the role and unit combination, and the price is defaulted after applying any conversion, if required.</span></span>  
  
 <span data-ttu-id="632f7-118">Wenn es keinen Preis für die Rolle gibt, dann wird der Kostenpreis standardmäßig auf 0,00 auf der Vorkalkulationsposition gesetzt.</span><span class="sxs-lookup"><span data-stu-id="632f7-118">If there isn’t a price for the role, then the cost price defaults to 0.00 on the estimate line.</span></span>  
  
 <span data-ttu-id="632f7-119">Alle Kostenmengen auf Kostenvorkalkulationsposition des Projekts werden in der Währung der zuständigen Organisationseinheit angegeben.</span><span class="sxs-lookup"><span data-stu-id="632f7-119">All cost amounts on project cost estimate lines are in the currency of the owning organizational unit.</span></span>  
  
## <a name="sales-price-defaulting"></a><span data-ttu-id="632f7-120">Standard-Vertriebspreis</span><span class="sxs-lookup"><span data-stu-id="632f7-120">Sales price defaulting</span></span>  
<span data-ttu-id="632f7-121">Die Vertriebspreisliste basiert auf der Vertriebsentität, die das Projekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="632f7-121">The sales price list is based on the sales entity that the project is attached to.</span></span> <span data-ttu-id="632f7-122">Die Vertriebspreisliste, die mit dem Angebot oder dem Vertrag verbunden ist, bestimmt den Einheitsvertriebskostenpreis.</span><span class="sxs-lookup"><span data-stu-id="632f7-122">The sales price list associated with the quote or contract determines the unit sales price.</span></span> <span data-ttu-id="632f7-123">Wenn das Angebot oder der Vertrag eine benutzerdefinierte Preisliste hat, ist dies die Standardvertriebspreisliste für Projektschätzungen.</span><span class="sxs-lookup"><span data-stu-id="632f7-123">If the quote or contract has a custom price list, this will be the default sales price list for project estimates.</span></span> <span data-ttu-id="632f7-124">Wenn es keine Vereinigung zu den Verkaufsentitäten gibt, dann ist die Standardverkaufspreisliste, die in den Parametereinstellungen konfiguriert ist, die Standardverkaufspreisliste für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="632f7-124">If there is no association to the sales entities, then the default sales price list configured in parameters settings will be the default sales price list for the project.</span></span> <span data-ttu-id="632f7-125">Jeder Vorkalkulationsposition ist eine Organisationseinheit der Ressource zugewiesen, um die Organisationseinheit anzuzeigen, von der die Ressourcen für den Abschluss der Aufgabe gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-125">Each estimate line has a resource organizational unit associated to indicate the organizational unit from which the resources will be booked for completing the task.</span></span> <span data-ttu-id="632f7-126">Der Vertriebspreis für die zugewiesenen Rollen, wird bestimmt, indem nach der Kombination der Rolle, der Einheit und der Organisationseinheit der Ressource in der Vertriebspreisliste gesucht wird, um den korrekten Vertriebspreises für das Datum zu erhalten, das auf Schätzungslinien wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-126">The sales price for the associated roles is determined by searching for the combination of role, unit, and resource organizational unit in the sales price list to get the correct sales price for the date effective on the estimate lines.</span></span>  
  
<span data-ttu-id="632f7-127">Wenn die Kombination der Rolle, der Einheit und der Organisationseinheit der Ressource keinen Vertriebspreis aus der Vertriebspreisliste ergibt, verwirft das System die Einheit und sucht nach der Kombination aus Rolle und Organisationseinheit der Ressource.</span><span class="sxs-lookup"><span data-stu-id="632f7-127">If the combination of role, unit, and resource organizational unit doesn’t result in a sales price from the sales price list, the system will disregard unit and search for the combination of role and resource organizational unit.</span></span> <span data-ttu-id="632f7-128">Wenn ein Vertriebspreis gefunden wird, wird dieser in die Einheit umgewandelt, die Sie auf der Vertriebsvorkalkulationsposition ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="632f7-128">If a sales price is found, this will be converted to the unit you chose on the sales estimate line.</span></span>  
  
<span data-ttu-id="632f7-129">Wenn das System keinen Preis für die Rolle findet, dann muss der Vertriebspreis standardmäßig auf 0,00 auf der Vorkalkulationsposition gesetzt.</span><span class="sxs-lookup"><span data-stu-id="632f7-129">If the system doesn’t find a price for the role, then the sales price must default to 0.00 on the estimate line.</span></span>  
  
<span data-ttu-id="632f7-130">Die Vorkalkulationsansicht hat eine Gitteransicht, die ein flaches Gitter von Vorkalkulationspositionen mit Einheit und Gesamtkosten und Vertriebspreis anzeigt.</span><span class="sxs-lookup"><span data-stu-id="632f7-130">The estimates view has a grid view that displays a flat grid of estimate lines with unit and total cost and sales price.</span></span>  
  
## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="632f7-131">Zeitphasenansicht von Projektschätzungen</span><span class="sxs-lookup"><span data-stu-id="632f7-131">Time-phased view of project estimates</span></span>  
<span data-ttu-id="632f7-132">In der Zeitphasenansicht für Projektschätzungen werden die Schätzungsdaten von der Gitteransicht standardmäßig durch die Rolle kreuzgefiltert und zeigt eine Tabelle der Schätzungsdaten über der Zeitachse im ausgesuchten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="632f7-132">In the time-phased view for project estimates, the estimates data from the grid view is pivoted by default by role, and shows a spread of estimate data across the timeline in the chosen timescale.</span></span>  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a><span data-ttu-id="632f7-133">Aufwandabschätzungsverteilung basierend auf Aufgabenmodus</span><span class="sxs-lookup"><span data-stu-id="632f7-133">Effort estimate allocation based on task mode</span></span>  
<span data-ttu-id="632f7-134">In der Zeitphasenansicht wird der Gesamtaufwand, der für die Aufgabe geschätzt wird, zugewiesen, indem eine bestimmte Anzahl von Aufwandsstunden pro Einheitszeitraum des ausgesuchten Zeitraums zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-134">In the time-phased view, total effort estimated for the task is distributed by allocating a certain number of effort hours per unit time period of the chosen timescale.</span></span> <span data-ttu-id="632f7-135">Im Project Service bestimmt der Aufgabenmodus, wie der Aufwand über die Dauer der Aufgabe zugeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-135">In project service, the task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="632f7-136">Die zwei Arten der Verteilung sind gleichmäßige Zuteilung und auf Arbeitsstunden basierte Zuteilung</span><span class="sxs-lookup"><span data-stu-id="632f7-136">The two kinds of allocation are even allocation and work hours based allocation</span></span>  
  
## <a name="work-hours-based-allocation"></a><span data-ttu-id="632f7-137">Arbeitsstunden basierte Zuteilung</span><span class="sxs-lookup"><span data-stu-id="632f7-137">Work hours based allocation</span></span>  
<span data-ttu-id="632f7-138">Der automatische Aufgabenzeitplanmodus regelt den für die Anzahl von Ressourcen, die für die Aufgabe geschätzt werden, sie werden für die vollen Arbeitsstunden pro Tag geschätzt.</span><span class="sxs-lookup"><span data-stu-id="632f7-138">Auto scheduling task mode for a task governs that for the number of resources estimated on the task, they are estimated to be utilized for the full work hours per day.</span></span> <span data-ttu-id="632f7-139">Dies trifft auch zu, wenn die Zuweisung des Aufwands durch Aufteilung über der Dauer der Aufgaben in der Zeitphasenansicht erfolgt.</span><span class="sxs-lookup"><span data-stu-id="632f7-139">This applies when allocating the effort by splitting it across the duration of tasks in the time phased view as well.</span></span> <span data-ttu-id="632f7-140">Zum Beispiel: Bei einem ein „Tag”-Zeitraum für eine Aufgabe, die durch eine Ressource abgeschlossen werden soll, übersteigt der zugewiesene Aufwand pro Tag nicht die Arbeitsstunden pro Tag, die im Kalender des Projektes definiert werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-140">For instance, on a ‘Day’ timescale, for a task estimated to be completed by one resource, the effort allocated per day will not exceed work hours per day defined in the project’s calendar.</span></span> <span data-ttu-id="632f7-141">Deshalb garantiert die Aufwandszuweisung immer, dass die Ressourcen so geschätzt werden, dass sie den ganzen Tages verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-141">Therefore, the effort allocation always ensures that the resources are estimated to be utilized for the full day.</span></span>  
  
## <a name="even-distribution"></a><span data-ttu-id="632f7-142">Gleichmäßige Verteilung</span><span class="sxs-lookup"><span data-stu-id="632f7-142">Even distribution</span></span>  
<span data-ttu-id="632f7-143">Manuell geplanter Aufgabenmodus zieht die Arbeitsstunden, den Projektkalender oder die Anzahl der Ressourcen, die für die Aufgabe definiert werden, nicht in Betracht.</span><span class="sxs-lookup"><span data-stu-id="632f7-143">Manually scheduled task mode doesn't honor the work hours, project calendar, or number of resources defined on the task.</span></span> <span data-ttu-id="632f7-144">Der Arbeitsplan basiert auf Benutzereingaben.</span><span class="sxs-lookup"><span data-stu-id="632f7-144">The task schedule is based on user input.</span></span> <span data-ttu-id="632f7-145">Für solche Aufgaben hat die Aufwandszuteilung pro Einheitszeitraum des ausgesuchten Zeitraums keine Begrenzungsfaktoren.</span><span class="sxs-lookup"><span data-stu-id="632f7-145">For such tasks, the effort allocation per unit time period of the chosen timescale doesn't have any limiting factors.</span></span> <span data-ttu-id="632f7-146">Der Gesamtaufwand für die Aufgabe wird gleichmäßig auf jeden Einheitszeitraum im ausgesuchten Zeitraum aufgeteilt und zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="632f7-146">The total effort on the task is equally split and allocated for each unit time period on the chosen timescale.</span></span>  
  
<span data-ttu-id="632f7-147">Auf diese Art bestimmt der Aufgabenmodus für die Aufgabe die Aufwandsverteilung oder die Verteilung des Aufwands pro Einheitszeitraum in Zeitphasenschätzungen.</span><span class="sxs-lookup"><span data-stu-id="632f7-147">In this way, the task mode defined on the task determines the effort distribution or allocation of effort per unit time period in time-phased estimates.</span></span>  
  
## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="632f7-148">Gruppierung und Zeitphasenoptionen</span><span class="sxs-lookup"><span data-stu-id="632f7-148">Grouping and time-phasing options</span></span>  
<span data-ttu-id="632f7-149">Diese Ansicht hilft Ihnen, die Verteilung des Aufwands, der Kosten und der Vertriebsschätzungen auf Tages-, Wochen-, Monats- oder Jahresbasis zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="632f7-149">This view helps you understand the distribution of the effort, cost, and sales estimates on a per day, week, month, or year basis.</span></span> <span data-ttu-id="632f7-150">Die Option „Gruppieren nach” erlaubt das Kreuzfiltern der Schätzungsdaten auf zwei anderer Dimensionen: Kategorie und Ressource.</span><span class="sxs-lookup"><span data-stu-id="632f7-150">The Group By option allows pivoting the estimates data on two other dimensions: category and resource.</span></span> <span data-ttu-id="632f7-151">Auf der Gitteransicht und der Zeitphasenansicht können Sie die Felder auswählen, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="632f7-151">On both the grid view and the time-phased view you can choose the fields to be displayed.</span></span> <span data-ttu-id="632f7-152">Summen für jeden der Zeitblöcke werden unten angezeigt, und geben die Summe des geschätzten Aufwands und der Kosten an.</span><span class="sxs-lookup"><span data-stu-id="632f7-152">Totals for each of the time blocks is displayed at the bottom indicating the total estimated effort, cost.</span></span> <span data-ttu-id="632f7-153">und der Verkäufe für den Tag, die Woche, den Monat oder das Jahr.</span><span class="sxs-lookup"><span data-stu-id="632f7-153">and sales for the day, week, month, or year.</span></span>  
  
<span data-ttu-id="632f7-154">Die Kosten- und Vertriebspreisstandard ist das Datum der Wirksamkeit – Wenn sich die Sätze für die Rollen ändern, sind sie in der Zeitphasenansicht transparenter, wenn Schätzungsdaten, die auf „Ressource” gefiltert und mit wöchentlicher Zeitphase angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-154">The cost and sales price defaulting takes is date effective—when the rates for the roles change it will be more transparent in the time-phased view when viewing estimate data pivoted on ‘Resource’ and time-phased by week.</span></span>  
  
## <a name="expense-estimates"></a><span data-ttu-id="632f7-155">Ausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="632f7-155">Expense estimates</span></span>  
<span data-ttu-id="632f7-156">Jede Ausgabe im Projekt, die nicht direkt mit der verbrauchten Arbeit zusammenhängt, kann in den Projektschätzungen in der Gitteransicht notiert werden.</span><span class="sxs-lookup"><span data-stu-id="632f7-156">Any expense that will be incurred in the project that is notdirectly related to labor to be expended can be recorded in the project estimates in the grid view.</span></span> <span data-ttu-id="632f7-157">Unter Verwendung der **Neue Ausgabenvorkalkulation hinzufügen** -Option in der Gitteransicht, können Sie dies erreichen.</span><span class="sxs-lookup"><span data-stu-id="632f7-157">Using the **Add expense estimate** option in the grid view, you can accomplish this.</span></span> <span data-ttu-id="632f7-158">Die Ausgabenschätzungen können für eine spezifische Aufgabe oder für das gesamte Projekt notiert werden; Sie können Ausgabenkategorien auf diesen Positionen auswählen und ein vorläufiges Datum auswählen, wann die Ausgabe erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="632f7-158">The expense estimates can be recorded for a specific task or for the entire project;you can choose expense categories on these lines and choose a tentative date when the expense is expected to be incurred.</span></span> <span data-ttu-id="632f7-159">Wenn die verbundenen Kosten und die Vertriebspreisliste Standardpreise oder die Aufschlagprozentsätze, die für Ausgabenkategorien definiert werden, haben, sind sie standardmäßig auf der Vorkalkulationsposition der Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="632f7-159">If the associated cost and sales price list have default prices, or markup percentages defined for expense categories, it will be defaulted on the estimate line on association.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="632f7-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="632f7-160">See Also</span></span>  
 [<span data-ttu-id="632f7-161">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="632f7-161">Project Manager Guide</span></span>](../psa/project-manager-guide.md)