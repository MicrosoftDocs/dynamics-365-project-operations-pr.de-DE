---
title: Buchen von benannten Ressourcen aus Ressourcenanforderungen
description: Dieses Thema enthält Informationen zum Buchen von benannten Ressourcen für eine generische Ressourcenanforderung.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076729"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="c7152-103">Buchen von benannten Ressourcen aus Ressourcenanforderungen</span><span class="sxs-lookup"><span data-stu-id="c7152-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c7152-104">Sie können eine benannte Ressource buchen, um eine allgemeine Ressource zu ersetzen, die über eine Ressourcenanforderung verfügt.</span><span class="sxs-lookup"><span data-stu-id="c7152-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c7152-105">Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**.</span><span class="sxs-lookup"><span data-stu-id="c7152-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="c7152-106">Wählen Sie in der Liste die allgemeine Ressource aus, die eine Ressourcenanforderung enthält, und klicken Sie dann auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="c7152-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="c7152-107">Alternativ öffnen Sie die Ressourcenanforderungen und klicken Sie dann auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="c7152-107">Or, open the resource requirement and then click **Book**.</span></span>


![Buchen eines generischen Teammitglieds](media/RM-how-to-14.png)


3. <span data-ttu-id="c7152-109">Wählen Sie auf der Seite **Zeitplan-Assistent** eine benannte Ressource aus, um sie für Ihr Projektteam zu buchen, und klicken Sie anschließend auf **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="c7152-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Buchen eines generischen Teammitglieds mithilfe des Zeitplan-Assistenten](media/RM-how-to-15.png)

<span data-ttu-id="c7152-111">Wenn die Buchung abgeschlossen und von einer benannten Ressource ausgeführt wurde, wird die generische Ressource durch die benannte Ressource ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c7152-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Benanntes Teammitglied, das ein generisches Teammitglied ersetzt](media/RM-how-to-16.png)

<span data-ttu-id="c7152-113">Die Zuweisungen im Zeitplan werden mit der benannten Ressource ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c7152-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Benanntes Teammitglied, das Projektaufgaben zugewiesen ist](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c7152-115">Erfüllen einer generischen Ressource mit mehreren benannten Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c7152-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c7152-116">Das Erfüllen einer Anforderungen für eine generische Ressource mit mehreren benannten Ressourcen ähnelt dem Zuweisen einer einzelnen benannten Ressource.</span><span class="sxs-lookup"><span data-stu-id="c7152-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c7152-117">Zum Beispiel gibt es eine Aufgabe mit einer Dauer von fünf Tagen und einem Aufwand von 120 Stunden.</span><span class="sxs-lookup"><span data-stu-id="c7152-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c7152-118">Diese Aufgabe kann nicht von einer Ressource ausgeführt werden, die einen typischen Acht-Stunden-Tag über eine Fünf-Tage-Woche hat.</span><span class="sxs-lookup"><span data-stu-id="c7152-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Aufgabe, die einen Aufwand von 120 Stunden über fünf Tage erfordert](media/RM-how-to-21.png)

<span data-ttu-id="c7152-120">Die Anforderung lautet 120 Stunden Robotertechnik an fünf Tagen, also 24 Stunden am Tag.</span><span class="sxs-lookup"><span data-stu-id="c7152-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Anforderung pro Tag](media/RM-how-to-22.png)

<span data-ttu-id="c7152-122">Dies ist ein Beispiel für den Fall, dass mehrere benannte Ressourcen benötigt werden, um eine generische Ressourcenanforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c7152-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c7152-123">Sie müssen mehrere Ressourcen buchen, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c7152-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Buchen von mehreren Ressourcen, um die Anforderung zu erfüllen](media/RM-how-to-23.png)

<span data-ttu-id="c7152-125">Der Hauptunterschied in diesem Szenario besteht darin, dass die generische Ressource bei dem der Aufgabe zugewiesenen Team bleibt und die gebuchten Mitglieder des benannten Ressourcenteams nicht als Teil der Position zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c7152-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c7152-126">Der Projektmanager kann die Arbeit den genannten Ressourcen entsprechend zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c7152-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c7152-127">Die Ansicht **Abstimmung** unterstützt einen Projektmanager bei der Aufteilung der Buchungen auf mehrere Ressourcen zu Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="c7152-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c7152-128">Dies erfolgt nicht automatisch, da in jedem Szenario, das komplizierter ist als das obige einfache Beispiel, z. B. wenn Sie ein Bündel von Aufgaben haben, aus denen die Anforderung besteht, muss die Absicht, wie der Projektmanager sie zuweisen möchte, vom System angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c7152-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c7152-129">Da das System Absichten nicht verstehen kann, ist es wahrscheinlich, dass die Annahmen anders als beabsichtigt sind und ein falsches oder unvorhersagbares Ergebnis auftritt.</span><span class="sxs-lookup"><span data-stu-id="c7152-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="c7152-130">Das vorhersagbare Ergebnis ist, dass die generische Ressource zugewiesen bleibt, bis der Projektmanager mit Hilfe der Ansicht **Abstimmung** willentlich Zuweisungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7152-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


