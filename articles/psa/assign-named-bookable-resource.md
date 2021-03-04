---
title: Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen
description: Dieses Thema enthält Informationen zum Buchen benannter Ressourcen für Projektteams und zum Zuweisen dieser Ressourcen zu Aufgaben.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145357"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="2d2c2-103">Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen</span><span class="sxs-lookup"><span data-stu-id="2d2c2-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2d2c2-104">Sie können Ihrem Projektteam eine benannte Ressource hinzufügen, indem Sie diese direkt für das Team buchen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="2d2c2-105">Führen Sie dazu folgende Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="2d2c2-106">Wechseln Sie in Project Service Automation zu **Projekte**, wählen Sie das Projekt aus, für das Sie buchen möchten und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="2d2c2-107">Klicken Sie auf der Seite **Projekt** auf der Registerkarte **Team** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Hinzufügen eines Teammitglieds über die Registerkarte „Team”](media/RM-how-to-1.png)

3. <span data-ttu-id="2d2c2-109">Wählen Sie im Dialogfeld **Schnellerfassung: Projektteammitglied** die buchbare Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="2d2c2-110">Das Feld **Rolle** wird mit der Standardrolle der Ressource vorausgefüllt, sofern eine zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="2d2c2-111">Sie können die Rolle bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="2d2c2-112">Wählen Sie das Start- und Enddatum aus, an denen die Ressource benötigt wird, und wählen Sie die Zuweisungsmethode für die Ressourcenkapazität aus.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="2d2c2-113">Wenn das Teammitglied ein Projektgenehmiger sein soll, wählen Sie im Feld **Projektgenehmiger** **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="2d2c2-114">Dies bedeutet, dass das Teammitglied übermittelte Zeit- und Ausgabeneinträge für dieses Projekt genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="2d2c2-115">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-115">Click **Save**.</span></span>

![Hinzufügen eines Teammitglieds über das Formular „Schnellerfassung”](media/RM-how-to-2.png)


<span data-ttu-id="2d2c2-117">Sie können die gebuchte Ressource nun Aufgaben im Projekt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="2d2c2-118">Klicken Sie auf der Seite **Projekt** auf die Registerkarte **Zeitplan**, um der neuen Ressource Aufgaben zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="2d2c2-119">Die Ressourcenauswahl, die über das Feld **Ressourcen** im Aufgabenraster gestartet wird, zeigt die Teammitglieder an, die Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Zuweisen eines Teammitglieds einer Aufgabe über die Registerkarte „Zeitplan”](media/RM-how-to-3.png)

<span data-ttu-id="2d2c2-121">In Version 3 von Project Service Automation (PSA) sind Ressourcenbuchungen und Aufgabenzuweisungen nicht eng miteinander verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="2d2c2-122">Wenn Sie also die Ressourcenauswahl im Zeitplan verwenden, können Sie Teammitgliedern Aufgaben für mehr Stunden zuweisen, als ihre Buchungen für das Projekt umfassen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="2d2c2-123">Sie sehen die Unterschiede zwischen Buchungen und Zuweisungen von Teammitgliedern auf der Registerkarte **Team** oder auf der Registerkarte **Ressourcenabstimmung**. Sie können die Unterschiede zwischen Buchungen und Zuweisungen für Ressourcen auch im Einzelnen abstimmen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Registerkarte „Ressourcenabstimmung”](media/RM-how-to-4.png)

<span data-ttu-id="2d2c2-125">Sie können auch die Ressourcenauswahl auf der Registerkarte **Zeitplan** verwenden, um nach buchbaren Ressourcen zu suchen und sie auszuwählen, die nicht bereits Teil des Projektteams sind.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="2d2c2-126">Diese werden in der Ressourcenauswahl als **Weitere Ressourcen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Zuweisen einer Nicht-Teammitgliedressource zu einer Aufgabe](media/RM-how-to-5.png)

<span data-ttu-id="2d2c2-128">Dabei wird die Ressource dem Projektteam hinzugefügt und der Aufgabe zugewiesen, es werden jedoch keine Buchungen generiert.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Teammitglied mit Zuweisungen und ohne Buchungen](media/RM-how-to-6.png)

<span data-ttu-id="2d2c2-130">Mithilfe der Funktion „Buchung erweitern” auf der Registerkarte **Abstimmung** oder der **Zeitplanübersicht** können Sie die Kapazität der Ressource für das Projekt buchen.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![„Buchungen erweitern” für ein Teammitglied auf der Registerkarte „Ressourcenabstimmung”](media/RM-how-to-7.png)

<span data-ttu-id="2d2c2-132">Nachdem ein Teammitglied für Ihr Projekt gebucht wurde, können Sie zum Verwalten seiner Buchungen die Funktion „Buchungen verwalten” oder die Zeitplanübersicht direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d2c2-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
