---
title: Erstellen eines Projekts
description: Erstellen eines Projekt (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076536"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="2e9a9-103">Erstellen eines Projekts (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2e9a9-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2e9a9-104">Erstellen Sie ein Projekt unter Verwendung der [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Funktionen in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], wenn Sie eine Verkaufschance, ein Angebot oder einen Vertrag für projektbasierte Services schaffen möchten.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="2e9a9-105">Die [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Funktionen helfen Ihnen, Ihr Projekt von der Verkaufschance bis hin zum Abschluss zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="2e9a9-106">Wenn Sie ein Projekt erstellen, erstellen Sie auch einen Projektstrukturplan, der Ihre Angebote, Kosteneinschätzungen und das Ressourcenmanagement beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="2e9a9-107">Wechseln Sie zu **Project Service > Projekte**.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="2e9a9-108">Klicken Sie auf **Neues Projekt**.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="2e9a9-109">Im Bereich **Zusammenfassung** tragen Sie einen Namen für Ihr Projekt ein und füllen dann so viele Details aus, wie Sie können.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="2e9a9-110">Erforderliche Elemente sind durch ein rotes Sternchen (\*) gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="2e9a9-111">Klicken Sie auf **Speichern** , um Ihr Projekt zu erstellen, sodass Sie mit der Bearbeitung fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="2e9a9-112">Als Nächstes erstellen Sie einen Projektstrukturplan für Ihr Projekt, um die Aufgaben, das Timing und die Ressourcenrollen zu definieren, die für das Projekt benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="2e9a9-113">Bei der Planung berücksichtigt Project Service Automation die Zeitzone der angewendeten Vorlage **Arbeitsstunde**.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="2e9a9-114">Beim Anzeigen der Zeitplanaufgaben werden jedoch das Start- und Enddatum einer Aufgabe in der Zeitzone des Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="2e9a9-115">Dies gilt auch für andere zeitgesteuerte Ansichten im Formular **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="2e9a9-116">Wenn die Zeitzone des Benutzers nicht mit der Zeitzone der auf das Projekt angewendeten Arbeitsstundenvorlage übereinstimmt, wird eine Warnung angezeigt, die den Unterschied erklärt.</span><span class="sxs-lookup"><span data-stu-id="2e9a9-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="2e9a9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e9a9-117">See Also</span></span>  
 [<span data-ttu-id="2e9a9-118">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="2e9a9-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)