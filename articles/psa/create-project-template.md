---
title: Eine Projektvorlage erstellen
description: Erstellen einer Projektvorlage (Project Service)
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076537"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="f6854-103">Erstellen einer Projektvorlage (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f6854-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f6854-104">Projektvorlagen sparen Zeit, wenn Ihr Unternehmen regelmäßig Gebote für ähnliche Typen von Projekten abgibt.</span><span class="sxs-lookup"><span data-stu-id="f6854-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="f6854-105">Sie stellen einen Standardsatz von Rollen und geschätzten Stunden für einen Typ von Projekt bereit.</span><span class="sxs-lookup"><span data-stu-id="f6854-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="f6854-106">Konto- und Projektmanager können auf Basis einer Projektvorlage Projekte erstellen, oder sie können die Vorlage kopieren und selbst eine erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6854-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="f6854-107">Komponenten der Projektvorlage</span><span class="sxs-lookup"><span data-stu-id="f6854-107">Components of project template</span></span>
 <span data-ttu-id="f6854-108">Eine Projektvorlage besteht aus drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="f6854-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="f6854-109">**Projektstrukturplan** : Ein Projektstrukturplan hat in einer Projektvorlage denselben Satz von Elementen wie im Projekt.</span><span class="sxs-lookup"><span data-stu-id="f6854-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="f6854-110">Sie können eine Aufgabenhierarchie erstellen, Rollen zu Aufgaben zuordnen, Zeitplanattribute definieren, Abhängigkeiten festlegen und alle Daten im Gantt-Diagramm anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f6854-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="f6854-111">Der Projektstrukturplan in den Projektvorlagen unterstützt auch Aufgabenmodi für die Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="f6854-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="f6854-112">Es gibt keinen Unterschied zwischen einer Projektvorlage und einem Projekt beim Erstellen eines Arbeitszeitplans.</span><span class="sxs-lookup"><span data-stu-id="f6854-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="f6854-113">**Projektschätzungen** : Projektschätzungen in Vorlagen funktionieren wie in Projekten, abgesehen davon, dass Preislisten für die Standardkosten und die Verkaufspreise immer die Standardkosten und Verkaufspreislisten sind, die in den [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Parametern definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6854-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="f6854-114">Die restlichen Funktionalitäten sind identisch mit einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="f6854-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="f6854-115">**Projektteambildung** : Wenn Sie ein Projektteam für eine Projektvorlage zusammenstellen, können Sie keine benannte Ressource in einer Vorlage buchen.</span><span class="sxs-lookup"><span data-stu-id="f6854-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="f6854-116">Sie können im Projektstrukturplan **Projektteam generieren** verwenden, um einen Satz allgemeiner Ressourcen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="f6854-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="f6854-117">Sie könne auch erforderliche Kompetenzen und Fähigkeiten für allgemeine Ressourcen angeben.</span><span class="sxs-lookup"><span data-stu-id="f6854-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="f6854-118">Sie können keine allgemeine Ressource durch eine buchbare Ressource in den Projektvorlagen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f6854-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="f6854-119">Erstellen eines Projekts aus einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="f6854-119">Create a project from a template</span></span>  
 <span data-ttu-id="f6854-120">Sie können ein Projekt aus einer Vorlage auf die folgenden Arten erstellen:</span><span class="sxs-lookup"><span data-stu-id="f6854-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="f6854-121">Wenn Sie ein Projekt aus einem Angebot erstellen, können Sie eine Projektvorlage im Projektschnellerfassungsformular auswählen.</span><span class="sxs-lookup"><span data-stu-id="f6854-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="f6854-122">Wenn Sie ein Projekt durch Klicken auf **Neues Projekt** erstellen, wird das Projektformular angezeigt, bevor Sie den Datensatz speichern.</span><span class="sxs-lookup"><span data-stu-id="f6854-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="f6854-123">Von hier können Sie auf das Feld **Eine Vorlage auswählen** klicken, um aus der Liste der vordefinierten Projektvorlagen in der Organisation auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f6854-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="f6854-124">Klicken Sie auf **Projekt aus Vorlage erstellen** auf der Seite **Projektvorlage** , um ein Projekt aus der Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6854-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="f6854-125">Kopieren von Komponenten einer Vorlage in ein Projekt:</span><span class="sxs-lookup"><span data-stu-id="f6854-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="f6854-126">Wenn Sie Komponenten einer Vorlage in ein Projekt kopieren, gibt es einige Dinge, die Sie wissen sollten.</span><span class="sxs-lookup"><span data-stu-id="f6854-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="f6854-127">**Kopieren eines Projektstrukturplans** : Wenn Sie den Projektstrukturplan aus einer Projektvorlage kopieren, wenn das Projekt einen anderen Projektkalender als die Vorlage hat, werden die Arbeitsstunden aus dem Kalender des Projekts auf den Aufgabenplan angewendet.</span><span class="sxs-lookup"><span data-stu-id="f6854-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="f6854-128">Dadurch wird der Zeitplan an den zugrundeliegenden Projektkalender angepasst.</span><span class="sxs-lookup"><span data-stu-id="f6854-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="f6854-129">Entsprechend nimmt die erste Aufgabe im Projektstrukturplan das Startdatum des Projekts, sodass der restliche Aufgabenhierarchienzeitplan anhand der Dauer und den Abhängigkeiten aktualisiert wird, die im Projektstrukturplan der Vorlage angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f6854-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="f6854-130">**Kopieren von Projektschätzungen** : Wenn Sie Projektschätzungspositionen kopieren, werden Preislisten anhand der besitzenden Einheit des Projekts für die Kostenpreisliste und Kunden für die Verkaufspreisliste aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f6854-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="f6854-131">Die Einstandspreise die Verkaufspreise der Einheit werden anhand dieser Preisliste für die Projekte bestimmt, die einer Vertriebsentität zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f6854-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="f6854-132">**Kopieren eines Projektteams** : Wenn Sie das Projektteam aus der Vorlage in ein Projekt kopieren, werden die generischen Ressourcen einschließlich der Kompetenzen und Fähigkeiten kopiert, die in der Datenbanktabelle definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f6854-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="f6854-133">Generische Ressourcenzuweisungen werden wie in der Projektvorlage verwaltet.</span><span class="sxs-lookup"><span data-stu-id="f6854-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f6854-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6854-134">See Also</span></span>  
 [<span data-ttu-id="f6854-135">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="f6854-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
