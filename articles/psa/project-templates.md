---
title: Projektvorlagen
description: Dieses Thema enthält Informationen zur Verwendung von Projektvorlagen für die schnelle Projekteinrichtung.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998275"
---
# <a name="project-templates"></a><span data-ttu-id="8f418-103">Projektvorlagen</span><span class="sxs-lookup"><span data-stu-id="8f418-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8f418-104">Eine Projektvorlage ist eine vordefiniertes Framework, mit dessen Hilfe Sie schnell und problemlos ein Projekt starten können.</span><span class="sxs-lookup"><span data-stu-id="8f418-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="8f418-105">Verwenden Sie eine vordefinierte Vorlage, um mit einem Klick ein neues Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8f418-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="8f418-106">Wie für Projekte auch müssen Sie die Voraussetzungen für Projektvorlagen definieren.</span><span class="sxs-lookup"><span data-stu-id="8f418-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="8f418-107">Sie müssen für jede Projektvorlage einen Projektkalender definieren. Außerdem müssen in der Organisation Rollen und Preislisten vordefiniert werden, damit für die Komponenten der Vorlage sinnvolle Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8f418-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="8f418-108">Eine Projektvorlage umfasst drei Komponenten: einen Zeitplan, Projektvorkalkulationen und Projektteammitglieder.</span><span class="sxs-lookup"><span data-stu-id="8f418-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="8f418-109">Zeitplan</span><span class="sxs-lookup"><span data-stu-id="8f418-109">Schedule</span></span>

<span data-ttu-id="8f418-110">Ein Zeitplan in einer Projektvorlage enthält denselben Satz von Elementen wie ein Zeitplan in einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="8f418-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="8f418-111">Sie können eine Aufgabenhierarchie erstellen, Rollen mit Aufgaben verknüpfen, Zeitplanattribute definieren und Abhängigkeiten festlegen.</span><span class="sxs-lookup"><span data-stu-id="8f418-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="8f418-112">Ein Zeitplan in einer Projektvorlage unterstützt außerdem Aufgabenmodi für jede Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8f418-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="8f418-113">Daher unterstützt er das Planungsmodul.</span><span class="sxs-lookup"><span data-stu-id="8f418-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="8f418-114">Sie müssen dem Projekt einen Projektkalender zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8f418-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="8f418-115">Wenn Sie einen Arbeitszeitplan erstellen, gibt es keinen Unterschied zwischen einer Projektvorlage und einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="8f418-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="8f418-116">Projektvorkalkulationen</span><span class="sxs-lookup"><span data-stu-id="8f418-116">Project estimates</span></span>

<span data-ttu-id="8f418-117">Projektvorkalkulationen in einer Projektvorlage funktionieren auf dieselbe Weise wie Projektvorkalkulationen in einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="8f418-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="8f418-118">Allerdings werden die Kosten und Verkaufspreise aus den Standardlisten für Kosten und Verkaufspreise abgerufen, die in den Parametern definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f418-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="8f418-119">Erstellen eines Projekts aus einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="8f418-119">Creating a project from a template</span></span>
 
<span data-ttu-id="8f418-120">Es gibt mehrere Möglichkeiten, aus einer Projektvorlage ein Projekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="8f418-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="8f418-121">Wenn Sie ein Projekt aus einem Angebot erstellen, können Sie im Dialogfeld **Schnellerfassung: Projekt** eine Projektvorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="8f418-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Das Dialogfeld „Schnellerfassung: Projekt“](media/project-11.png)

- <span data-ttu-id="8f418-123">Wenn Sie ein Projekt erstellen, indem Sie **Neues Projekt** auswählen, wird die Seite **Projekt** angezeigt, bevor der Datensatz gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8f418-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="8f418-124">Wählen Sie im Feld **Eine Vorlage auswählen** eine der in der Organisation vordefinierten Projektvorlagen aus.</span><span class="sxs-lookup"><span data-stu-id="8f418-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="8f418-125">Verwenden Sie **Projekt aus einer Vorlage erstellen** auf der Seite **Vorlagenentität** aus.</span><span class="sxs-lookup"><span data-stu-id="8f418-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="8f418-126">Kopieren von Komponenten einer Vorlage in ein Projekt</span><span class="sxs-lookup"><span data-stu-id="8f418-126">Copying components of template to project</span></span>

<span data-ttu-id="8f418-127">Wenn Sie die Komponenten einer Projektvorlage in ein Projekt kopieren, können abhängig von den Einstellungen im Projekt einige Außerkraftsetzungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="8f418-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="8f418-128">Kopieren des Zeitplans</span><span class="sxs-lookup"><span data-stu-id="8f418-128">Copying the schedule</span></span>

<span data-ttu-id="8f418-129">Wenn Sie den Zeitplan aus einer Projektvorlage kopieren und das Projekt einen anderen Projektkalender als die Vorlage hat, werden die Arbeitsstunden aus dem Kalender des Projekts auf den Aufgabenzeitplan angewendet.</span><span class="sxs-lookup"><span data-stu-id="8f418-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="8f418-130">Dadurch wird der Zeitplan an den zugrundeliegenden Projektkalender angepasst.</span><span class="sxs-lookup"><span data-stu-id="8f418-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="8f418-131">Entsprechend übernimmt die erste Aufgabe im Zeitplan das Startdatum des Projekts und der Zeitplan der restlichen Hierarchie wird basierend auf der Dauer und den Abhängigkeiten aktualisiert, die in der Vorlage angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8f418-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="8f418-132">Kopieren der Projektvorkalkulationen</span><span class="sxs-lookup"><span data-stu-id="8f418-132">Copying project estimates</span></span> 

<span data-ttu-id="8f418-133">Wenn Sie Positionen aus der Projektvorkalkulation kopieren, werden die Preislisten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8f418-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="8f418-134">Für die Einstandspreisliste basieren diese Aktualisierungen auf der zuständigen Einheit des Projekts.</span><span class="sxs-lookup"><span data-stu-id="8f418-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="8f418-135">Für die Verkaufspreisliste basieren sie auf dem Kunden.</span><span class="sxs-lookup"><span data-stu-id="8f418-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="8f418-136">Für Projekte, die einer Vertriebsentität zugeordnet sind, werden die Einheitskosten und die Verkaufspreise anhand dieser Preislisten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8f418-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="8f418-137">Kopieren eines Projektteams</span><span class="sxs-lookup"><span data-stu-id="8f418-137">Copying a project team</span></span>

<span data-ttu-id="8f418-138">Wenn ein Projektteam aus einer Projektvorlage in ein Projekt kopiert wird, werden die generischen Ressourcen zusammen mit den Kompetenzen und Fähigkeiten kopiert, die in der Vorlage definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f418-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="8f418-139">Generische Ressourcenzuweisungen werden wie in der Projektvorlage verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8f418-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="8f418-140">Benannte Ressourcen werden in Projektvorlagen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f418-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]