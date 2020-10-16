---
title: Teammitglieder verwalten
description: Diese Thema enthält Informationen zum Buchen benannter Ressourcen für Projektteams und zum Zuweisen dieser Ressourcen zu Aufgaben.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961865"
---
# <a name="maintain-team-members"></a><span data-ttu-id="e63ec-103">Teammitglieder verwalten</span><span class="sxs-lookup"><span data-stu-id="e63ec-103">Maintain team members</span></span>

<span data-ttu-id="e63ec-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="e63ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e63ec-105">Sie können Ihrem Projektteam eine benannte Ressource hinzufügen, indem Sie diese direkt für das Team buchen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="e63ec-106">Wechseln Sie in Dynamics 365 Project Operations zu **Projekte**, wählen Sie das Projekt aus, für das Sie buchen möchten und öffnen Sie es.</span><span class="sxs-lookup"><span data-stu-id="e63ec-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="e63ec-107">Wählen Sie auf der Seite **Projekt** auf der Registerkarte **Team** **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="e63ec-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="e63ec-108">Wählen Sie im Dialogfeld **Schnellerfassung: Projektteammitglied** die buchbare Ressource aus.</span><span class="sxs-lookup"><span data-stu-id="e63ec-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="e63ec-109">Das Feld **Rolle** wird mit der Standardrolle der Ressource vorausgefüllt, sofern eine zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="e63ec-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="e63ec-110">Sie können die Rolle ändern.</span><span class="sxs-lookup"><span data-stu-id="e63ec-110">You can change the role.</span></span> 
4. <span data-ttu-id="e63ec-111">Wählen Sie das Start- und Enddatum aus, an denen die Ressource benötigt wird, und wählen Sie die Zuweisungsmethode für die Ressourcenkapazität aus.</span><span class="sxs-lookup"><span data-stu-id="e63ec-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="e63ec-112">Wählen Sie im Feld **Projektgenehmiger** **Ja** aus, wenn das Teammitglied ein Projektgenehmiger sein soll.</span><span class="sxs-lookup"><span data-stu-id="e63ec-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="e63ec-113">Das Teammitglied kann übermittelte Zeit- und Ausgabeneinträge für dieses Projekt genehmigen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="e63ec-114">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e63ec-114">Select **Save**.</span></span>

<span data-ttu-id="e63ec-115">Sie können die gebuchte Ressource nun Aufgaben im Projekt zuweisen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="e63ec-116">Weisen Sie auf der Seite **Projekt** auf die Registerkarte **Zeitplan** der neuen Ressource Aufgaben zu.</span><span class="sxs-lookup"><span data-stu-id="e63ec-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="e63ec-117">Die Ressourcenauswahl, die über das Feld **Ressourcen** im Aufgabenraster gestartet wird, zeigt die Teammitglieder an, die Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="e63ec-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="e63ec-118">Im Project Operations sind Ressourcenbuchungen und Aufgabenzuweisungen nicht eng miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="e63ec-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="e63ec-119">Wenn Sie also die Ressourcenauswahl im Zeitplan verwenden, können Sie Teammitgliedern Aufgaben für mehr Stunden zuweisen, als ihre Buchungen für das Projekt umfassen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="e63ec-120">Die Unterschiede zwischen Buchungen und Zuweisungen von Teammitgliedern werden auf den Registerkarten **Team** und **Ressourcenabstimmung** gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e63ec-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="e63ec-121">Sie können die Unterschiede zwischen Buchungen und Zuweisungen für Ressourcen auch detaillierter abgleichen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="e63ec-122">Verwenden Sie die Ressourcenauswahl auf der Registerkarte **Zeitplan**, um nach buchbaren Ressourcen zu suchen und sie auszuwählen, die nicht bereits Teil des Projektteams sind.</span><span class="sxs-lookup"><span data-stu-id="e63ec-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="e63ec-123">Diese Ressourcen werden in der Ressourcenauswahl als **Weitere Ressourcen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e63ec-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="e63ec-124">Wenn Sie eine Auswahl treffen, wird die Ressource dem Projektteam hinzugefügt und der Aufgabe zugewiesen, es werden jedoch keine Buchungen generiert.</span><span class="sxs-lookup"><span data-stu-id="e63ec-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="e63ec-125">Mithilfe der Funktion „Buchung erweitern” auf der Registerkarte **Abstimmung** oder der **Zeitplanübersicht** können Sie die Kapazität der Ressource für das Projekt buchen.</span><span class="sxs-lookup"><span data-stu-id="e63ec-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="e63ec-126">Nachdem ein Teammitglied für Ihr Projekt gebucht wurde, können Sie **Buchungen verwalten** oder die **Zeitplanübersicht** zum direkten Verwalten der Buchungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e63ec-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
