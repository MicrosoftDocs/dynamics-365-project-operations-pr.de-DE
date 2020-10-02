---
title: Allgemeine Ressourcenanforderungserfüllung
description: Dieses Thema enthält Informationen zum Buchen von benannten Ressourcen für eine generische Ressourcenanforderung.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897585"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="6d476-103">Allgemeine Ressourcenanforderungserfüllung</span><span class="sxs-lookup"><span data-stu-id="6d476-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="6d476-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="6d476-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6d476-105">Sie können eine benannte Ressource buchen, um eine allgemeine Ressource zu ersetzen, die über eine Ressourcenanforderung verfügt.</span><span class="sxs-lookup"><span data-stu-id="6d476-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="6d476-106">Auf der Seite **Projekte** wählen Sie die Registerkarte **Team**.</span><span class="sxs-lookup"><span data-stu-id="6d476-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="6d476-107">Wählen Sie in der Liste die allgemeine Ressource aus, die eine Ressourcenanforderung enthält, und wählen Sie **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="6d476-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="6d476-108">Alternativ öffnen Sie die Ressourcenanforderungen und wählen **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="6d476-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="6d476-109">Wählen Sie auf der Seite **Zeitplan-Assistent** eine benannte Ressource aus, um sie für Ihr Projektteam zu buchen, und wählen Sie anschließend **Buchen**.</span><span class="sxs-lookup"><span data-stu-id="6d476-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="6d476-110">Wenn die Buchung abgeschlossen und von einer benannten Ressource ausgeführt wurde, wird die generische Ressource durch die benannte Ressource ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6d476-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="6d476-111">Die Zuweisungen im Zeitplan werden mit der benannten Ressource ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6d476-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="6d476-112">Erfüllen einer generischen Ressource mit mehreren benannten Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d476-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="6d476-113">Das Erfüllen einer Anforderungen für eine generische Ressource mit mehreren benannten Ressourcen ähnelt dem Zuweisen einer einzelnen benannten Ressource.</span><span class="sxs-lookup"><span data-stu-id="6d476-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="6d476-114">Zum Beispiel gibt es eine Aufgabe mit einer Dauer von fünf Tagen und einem Aufwand von 120 Stunden.</span><span class="sxs-lookup"><span data-stu-id="6d476-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="6d476-115">Diese Aufgabe kann nicht von einer Ressource ausgeführt werden, die einen typischen Acht-Stunden-Tag über eine Fünf-Tage-Woche hat.</span><span class="sxs-lookup"><span data-stu-id="6d476-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="6d476-116">Die Anforderung lautet 120 Stunden Robotertechnik an fünf Tagen, also 24 Stunden am Tag.</span><span class="sxs-lookup"><span data-stu-id="6d476-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="6d476-117">Dies ist ein Beispiel für den Fall, dass mehrere benannte Ressourcen benötigt werden, um eine generische Ressourcenanforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6d476-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="6d476-118">Sie müssen mehrere Ressourcen buchen, um die Anforderung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6d476-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="6d476-119">Der Hauptunterschied in diesem Szenario besteht darin, dass die generische Ressource bei dem der Aufgabe zugewiesenen Team bleibt und die gebuchten Mitglieder des benannten Ressourcenteams nicht als Teil der Position zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6d476-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="6d476-120">Der Projektmanager kann die Arbeit den genannten Ressourcen entsprechend zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6d476-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="6d476-121">Die Ansicht **Abstimmung** unterstützt einen Projektmanager bei der Aufteilung der Buchungen auf mehrere Ressourcen zu Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="6d476-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="6d476-122">Dies erfolgt nicht automatisch, da in jedem Szenario, das komplizierter ist als das obige einfache Beispiel, z. B. wenn Sie ein Bündel von Aufgaben haben, aus denen die Anforderung oder die Absicht besteht, wie der Projektmanager sie zuweisen möchte, vom System angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6d476-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="6d476-123">Da das System Absichten nicht verstehen kann, weichen die Annahmen höchstwahrscheinlich von den Absichten ab und ein falsches oder unvorhersehbares Ergebnis tritt auf.</span><span class="sxs-lookup"><span data-stu-id="6d476-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="6d476-124">Das vorhersagbare Ergebnis ist, dass die generische Ressource zugewiesen bleibt, bis der Projektmanager mit Hilfe der Ansicht **Abstimmung** willentlich Zuweisungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d476-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


