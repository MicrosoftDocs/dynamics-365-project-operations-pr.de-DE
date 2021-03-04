---
title: Allgemeine buchbare Ressourcen einer Aufgabe und einem Projektteam zuweisen
description: Dieses Thema enthält Informationen über die Buchung von generischen Ressourcen für Aufgaben und Projektteams.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145402"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="9b03b-103">Zuweisen von allgemeinen buchbaren Ressourcen zu einer Aufgaben und Erstellen von Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="9b03b-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9b03b-104">Zusätzlich zur Buchung und Zuweisung von benannten oder echten Ressourcen zu Ihrem Projekt können Sie Projektaufgaben allgemeine Ressourcen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="9b03b-105">Diese Ressourcen können als Platzhalter für benannte Ressourcen dienen, bis Sie bereit sind, Ihr Projekt mit benannten Ressourcen auszustatten.</span><span class="sxs-lookup"><span data-stu-id="9b03b-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="9b03b-106">Öffnen Sie in Project Service Automation (PSA) die Seite **Projekt** und geben Sie auf der Registerkarte **Zeitplan** den Positionsnamen der generischen Ressource in der Zelle **Ressource** des Zeitplans ein.</span><span class="sxs-lookup"><span data-stu-id="9b03b-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="9b03b-107">Sie können auch in der Zelle auf das Symbol **Ressource** klicken, um die Ressourcenauswahl zu öffnen, und dann den Namen der allgemeinen Ressource eingeben, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9b03b-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Erstellen und Zuweisen eines allgemeinen Teammitglieds](media/RM-how-to-9.png)

<span data-ttu-id="9b03b-109">Dadurch wird der Bereich **Schnellerfassung: Projektteammitglied** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9b03b-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="9b03b-110">Geben Sie die Rolle und Organisationseinheit des generischen Ressourcenteammitglieds ein und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="9b03b-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Generisches Teammitglied – Schnellerfassung](media/RM-how-to-10.png)

3. <span data-ttu-id="9b03b-112">Nachdem Sie das neue generische Ressourcenteammitglied erstellt haben, wird es der Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="9b03b-113">Sie können diese generische Ressource weiteren Aufgaben im Arbeitsplan zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Zuweisen vorhandener generischer Teammitglieder zu Aufgaben](media/RM-how-to-11.png)

4. <span data-ttu-id="9b03b-115">Nachdem Sie die generische Ressource zugewiesen haben, können Sie eine Ressourcenanforderung generieren und diese erfüllen, indem Sie eine Ressourcenanforderung direkt buchen oder an einen Ressourcen-Manager übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9b03b-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generieren einer Anforderung für ein generisches Teammitglied](media/RM-how-to-12.png)

<span data-ttu-id="9b03b-117">Im Teammitgliedsraster können Sie nicht nur die Ressourcenauswahl wie oben erwähnt verwenden, sondern auch generische Ressourcen direkt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="9b03b-118">Die Ressourcen werden mit einer Ressourcenanforderung hinzugefügt, die auf dem Start- bzw. Enddatum und der Zuordnungsmethode basiert, die im Bereich **Schnellerfassung: Projektteammitglied** angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9b03b-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="9b03b-119">Sie können einen Unterschied feststellen, wenn Sie das generische Teammitglied direkt hinzufügen und der generischen Ressource dann mehr Aufgaben zuweisen, als Stunden angefordert wurden, um diese durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="9b03b-120">Klicken Sie auf **Anforderung generieren**, um die Anforderung zum Abgleichen der erforderlichen Stunden mit den Zuweisungen neu zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9b03b-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="9b03b-121">Sie können auch auf den Link **Ressourcenanforderung** im Teamraster klicken, um die Anforderung zu öffnen und Fähigkeiten, bevorzugte Ressourcen usw. hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9b03b-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Ressourcenanforderung](media/RM-how-to-13.png)

