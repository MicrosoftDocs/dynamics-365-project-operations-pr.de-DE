---
title: Zeitzonen verwalten
description: Wenn ein Projekt erstellt wird, basiert dessen Zeitzone auf der Zeitzone, die in der angewendeten Arbeitszeitvorlage definiert ist.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076462"
---
# <a name="manage-time-zones"></a><span data-ttu-id="afc2d-103">Zeitzonen verwalten</span><span class="sxs-lookup"><span data-stu-id="afc2d-103">Manage time zones</span></span>

<span data-ttu-id="afc2d-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="afc2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="afc2d-105">Projekte</span><span class="sxs-lookup"><span data-stu-id="afc2d-105">Projects</span></span>

<span data-ttu-id="afc2d-106">Wenn ein Projekt erstellt wird, basiert dessen Zeitzone auf der Zeitzone, die in der angewendeten Arbeitszeitvorlage definiert ist.</span><span class="sxs-lookup"><span data-stu-id="afc2d-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="afc2d-107">Im entsprechenden **Projekt** beziehen sich die Daten immer auf die Zeitzone des Benutzers, der auf jeder Registerkarte angemeldet ist, mit Ausnhame der Registerkarte **Aufgabe**. Wenn Sie den Projektstrukturplan anzeigen, werden die Daten immer in der Zeitzone des Projekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afc2d-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="afc2d-108">Tasks</span><span class="sxs-lookup"><span data-stu-id="afc2d-108">Tasks</span></span>

<span data-ttu-id="afc2d-109">Wenn eine Aufgabe erstellt wird, werden Startzeit, Endzeit und Stunden/Tag durch die Arbeitsstunden des Projekts gesteuert.</span><span class="sxs-lookup"><span data-stu-id="afc2d-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="afc2d-110">Wenn beispielsweise eine Aufgabe mit einem Projekt erstellt wird, dessen Zeitzone -8 PST ist und Arbeitszeiten von montags bis freitags von 9:00 bis 17:00 Uhr aufweist, berücksichtigt jede Aufgabe, die ohne Abeitsauftrag erstellt wurde, die Startzeit und Endzeit des Projektkalenders.</span><span class="sxs-lookup"><span data-stu-id="afc2d-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="afc2d-111">Ressourcen mit Zeitzonen verwalten</span><span class="sxs-lookup"><span data-stu-id="afc2d-111">Manage resources with time zones</span></span>

<span data-ttu-id="afc2d-112">Um genaue und vorhersehbare Ergebnisse bei der Verwendung von **Buchung erweitern** zu erzielen, gibt es zwei wichtige Voraussetzungen, die erfüllt sein müssen:</span><span class="sxs-lookup"><span data-stu-id="afc2d-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="afc2d-113">Der Benutzer muss die Zeitzone seines Geräts so konfigurieren, dass sie mit den Zeitzonen überinstimmt, die in den **Personalisierungseinstellungen** des Systems definiert sind.</span><span class="sxs-lookup"><span data-stu-id="afc2d-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Zeitzoneneinstellungen in Windows 10](media/reconcile-assignments-03.png)

  ![Zeitzoneneinstellungen in den Personalisierungseinstellungen](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="afc2d-116">Die buchbare Ressource muss mindestens eine Minute Arbeitszeit haben, die sich mit den Konturen überschneidet, die zum Definieren der angeforderten Erweiterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afc2d-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="afc2d-117">Nehmen wir als Beispiel die folgenden Ressourcen mit Arbeitszeiten, die zwischen 9:00 und 19:00 Uhr liegen.</span><span class="sxs-lookup"><span data-stu-id="afc2d-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Vergleich der Ressourcenkonturen](media/reconcile-assignments-05.png)

<span data-ttu-id="afc2d-119">Die folgende Tabelle zeigt:</span><span class="sxs-lookup"><span data-stu-id="afc2d-119">The following table shows:</span></span>

- <span data-ttu-id="afc2d-120">Eine Projektkalendervorlage</span><span class="sxs-lookup"><span data-stu-id="afc2d-120">A project calendar template</span></span>
- <span data-ttu-id="afc2d-121">Ressource A: Diese Ressource verfügt über denselben Kalender und befindet sich in derselben Zeitzone wie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="afc2d-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="afc2d-122">Die Buchung beginnt um 9:00 Uhr.</span><span class="sxs-lookup"><span data-stu-id="afc2d-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="afc2d-123">Ressource B: Diese Ressource befindet sich in einer anderen Zeitzone als das Projekt und beginnt um 7:00 Uhr in ihrer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="afc2d-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="afc2d-124">Die Buchungen beginnen jedoch um 9:00 Uhr, da dies der früheste Startzeitpunkt der Zuordnungskontur ist.</span><span class="sxs-lookup"><span data-stu-id="afc2d-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="afc2d-125">Ressourcen C und D: Die Ressourcen befinden sich in unterschiedlichen Zeitzonen, die sich voneinander und vom Projekt unterscheiden, und ihre Buchungen beginnen nicht früher als die jeweils verfügbaren Startzeiten.</span><span class="sxs-lookup"><span data-stu-id="afc2d-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="afc2d-126">Entität</span><span class="sxs-lookup"><span data-stu-id="afc2d-126">Entity</span></span>  |<span data-ttu-id="afc2d-127">Kalender</span><span class="sxs-lookup"><span data-stu-id="afc2d-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="afc2d-128">Projektkalendervorlage</span><span class="sxs-lookup"><span data-stu-id="afc2d-128">Project calendar template</span></span>   | ![Projektkalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="afc2d-130">Ressource A</span><span class="sxs-lookup"><span data-stu-id="afc2d-130">Resource A</span></span>  | ![Kalender Ressource A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="afc2d-132">Ressource B</span><span class="sxs-lookup"><span data-stu-id="afc2d-132">Resource B</span></span>  |  ![Kalender Ressource B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="afc2d-134">Ressource C</span><span class="sxs-lookup"><span data-stu-id="afc2d-134">Resource C</span></span>  |  ![Kalender Ressource C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="afc2d-136">Ressource D</span><span class="sxs-lookup"><span data-stu-id="afc2d-136">Resource D</span></span>  | ![Kalender Ressource D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="afc2d-138">Wenn Sie zur Ansicht **Abstimmung** navigieren, werden die Ressourcenzuweisungen und die damit verbundenen Buchungsverluste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afc2d-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Abstimmungssicht vor Erweiterung](media/reconcile-assignments-10.png)

<span data-ttu-id="afc2d-140">Nachdem die Funktion zum Erweitern der Buchung für jede Ressource verwendet wurde, werden die Buchungen für jede Ressource erfolgreich erweitert, da sich die Arbeitszeiten jeder Ressource mit den Konturen des Verlusts überschneiden.</span><span class="sxs-lookup"><span data-stu-id="afc2d-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Abstimmungssicht nach Buchungsverlängerung](media/reconcile-assignments-11.png) 

<span data-ttu-id="afc2d-142">Beachten Sie, dass ein genauerer Blick auf die Details der Buchungen Unterschiede in der Startzeit der Buchungen zeigt.</span><span class="sxs-lookup"><span data-stu-id="afc2d-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="afc2d-143">Die Buchungen beginnen frühestens zur Startzeit der Zuordnungskontur und frühestens zur verfügbaren Startzeit der Ressource.</span><span class="sxs-lookup"><span data-stu-id="afc2d-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Neue Buchungen der Ressourcen in der Zeitplantafel](media/reconcile-assignments-12.png)
