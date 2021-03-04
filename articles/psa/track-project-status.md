---
title: So verfolgen Sie ein Projektstatus
description: Nachverfolgen eines Projektstatus (Project Service)
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149587"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="33ac3-103">Nachverfolgen eines Projektstatus (Project Service)</span><span class="sxs-lookup"><span data-stu-id="33ac3-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="33ac3-104">Verwenden Sie [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], um den Fortschritt des Projektes eines Kunden nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="33ac3-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="33ac3-105">Wenn das Engagement voranschreitet, werden die Projektphasen aktualisiert, um die Phase des Engagements darzustellen:</span><span class="sxs-lookup"><span data-stu-id="33ac3-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="33ac3-106">**Neu**</span><span class="sxs-lookup"><span data-stu-id="33ac3-106">**New**</span></span>    | <span data-ttu-id="33ac3-107">Wenn Sie ein Projekt erstellen, wird die Phase auf **Neu** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33ac3-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="33ac3-108">Wenn Sie das Projekt aus einer Vorlage erstellt haben, verfügt das Projekt zu diesem Zeitpunkt möglicherweise über einen Zeitplan, Schätzungen und Teamdaten.</span><span class="sxs-lookup"><span data-stu-id="33ac3-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="33ac3-109">Andernfalls ist es der Entwurf des Projektes, und Sie müssen den Rest der Projektkomponenten manuell eintragen.</span><span class="sxs-lookup"><span data-stu-id="33ac3-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="33ac3-110">**Angebot**</span><span class="sxs-lookup"><span data-stu-id="33ac3-110">**Quote**</span></span>   |      <span data-ttu-id="33ac3-111">Wenn Sie ein Projekt einem Angebot zuweisen oder es aus einem Angebot erstellen, wird die Projektphase auf **Angebot** festgelegt, und auch die geschätzten Start- und Enddaten werden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="33ac3-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="33ac3-112">Wenn das Projekt in der Angebotsphase ist, werden die Angebotsdetails auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33ac3-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="33ac3-113">**Planen**</span><span class="sxs-lookup"><span data-stu-id="33ac3-113">**Plan**</span></span>   |                                     <span data-ttu-id="33ac3-114">Wenn Sie ein Angebot gewinnen, das einem Projekt zugewiesen ist, und wenn das Engagement bis zur Vertragsphase fortschreitet, wird die Projektphase auf **Planen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="33ac3-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="33ac3-115">Vertragsdetails werden auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33ac3-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="33ac3-116">**Abschließen**</span><span class="sxs-lookup"><span data-stu-id="33ac3-116">**Complete**</span></span> |                    <span data-ttu-id="33ac3-117">Wenn die Projektarbeit abgeschlossen ist, können Sie die Phase auf **Abgeschlossen** ändern.</span><span class="sxs-lookup"><span data-stu-id="33ac3-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="33ac3-118">Wenn die Projektphase auf "Abgeschlossen" festgelegt ist, ist die Arbeit zu 100 % abgeschlossen, aber das Projekt bleibt offen, damit alle ausstehenden Zeit- oder Ausgabeneingaben notiert werden können.</span><span class="sxs-lookup"><span data-stu-id="33ac3-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="33ac3-119">**Schließen**</span><span class="sxs-lookup"><span data-stu-id="33ac3-119">**Close**</span></span>   |           <span data-ttu-id="33ac3-120">Wenn alle Transaktionen auf dem Projekt aufgezeichnet worden sind und Sie keine weiteren mehr erwartet werden, können Sie die Phase manuell auf **Schließen** festlegen.</span><span class="sxs-lookup"><span data-stu-id="33ac3-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="33ac3-121">Wenn das Projekt auf **Schließen** festlegen, können Sie keine weiteren Geschäfte auf dem Projekt aufzeichnen und das Projekt nur lesen.</span><span class="sxs-lookup"><span data-stu-id="33ac3-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="33ac3-122">So verfolgen Sie ein Projektstatus</span><span class="sxs-lookup"><span data-stu-id="33ac3-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="33ac3-123">Wechseln Sie zu **Project Service > Projekte**.</span><span class="sxs-lookup"><span data-stu-id="33ac3-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="33ac3-124">Klicken Sie auf das gewünschte Projekt.</span><span class="sxs-lookup"><span data-stu-id="33ac3-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="33ac3-125">Wählen Sie auf der Leiste oben auf dem Bildschirm den Abwärtspfeil neben dem Projektnamen, und klicken Sie dann auf **Projektnachverfolgung**.</span><span class="sxs-lookup"><span data-stu-id="33ac3-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="33ac3-126">Wählen Sie **Aufwandsnachverfolgung** oder **Kostennachverfolgung** in der Dropdownliste über der Aufgabenliste aus.</span><span class="sxs-lookup"><span data-stu-id="33ac3-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="33ac3-127">Doppelklicken Sie auf jede Aufgabe, um sie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="33ac3-127">Double-click any task to edit it.</span></span> <span data-ttu-id="33ac3-128">Sie können die Balken im Gantt-Diagramm auch bewegen oder die Größe anpassen, um die Zeit und den Fortschritt für eine Aufgabe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="33ac3-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="33ac3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33ac3-129">See Also</span></span>  
 [<span data-ttu-id="33ac3-130">Handbuch des Projektmanagers</span><span class="sxs-lookup"><span data-stu-id="33ac3-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
