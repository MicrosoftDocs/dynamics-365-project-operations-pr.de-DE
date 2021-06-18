---
title: Vorgeschlagene Ressourcen überprüfen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000750"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="3f825-103">Vorgeschlagene Ressourcen überprüfen</span><span class="sxs-lookup"><span data-stu-id="3f825-103">Review proposed resources</span></span>

<span data-ttu-id="3f825-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3f825-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f825-105">Ressourcenmanager können dem Projektmanager mithilfe einer Ressourcenanfrage eine Ressource vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="3f825-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="3f825-106">Wählen Sie im Anfrageraster oder in der Anfrage selbst **Ressourcen suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f825-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="3f825-107">Wählen Sie auf der Seite **Zeitplan-Assistent** die Ressource aus. Wählen Sie dann im Bereich **Ressourcenbuchung erstellen** im Feld **Buchungsstatus** die Option **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="3f825-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="3f825-108">Die folgenden Statusaktualisierungen finden statt:</span><span class="sxs-lookup"><span data-stu-id="3f825-108">The following status updates occur:</span></span>

- <span data-ttu-id="3f825-109">Auf der Seite **Planungsassistent** werden die Statusanzeigen aktualisiert, um anzuzeigen, dass die Buchung vorgeschlagen ist (nicht fest gebucht).</span><span class="sxs-lookup"><span data-stu-id="3f825-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="3f825-110">In der Ressourcenanforderung wird der Status auf **Überprüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="3f825-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="3f825-111">Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** für das generische Teammitglied in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="3f825-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="3f825-112">Der Projektmanager kann den Vorschlag annehmen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="3f825-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="3f825-113">Zum Verarbeiten von Ressourcenanfragen können Ressourcenmanager einen der folgenden Ansätze auswählen:</span><span class="sxs-lookup"><span data-stu-id="3f825-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="3f825-114">Mehrere Ressourcen vorschlagen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die geforderten Stunden zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3f825-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="3f825-115">Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="3f825-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="3f825-116">In diesem Szenario können sich die Stunden nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="3f825-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="3f825-117">Schlagen Sie weniger Ressourcen als erforderlich vor.</span><span class="sxs-lookup"><span data-stu-id="3f825-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="3f825-118">In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die vom Anforderer angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f825-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="3f825-119">Wenn der Anfragende die vorgeschlagenen Ressourcen akzeptiert, wird daher eine nicht erfüllte Ressourcenanforderung erstellt, um den restlichen Bedarf zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="3f825-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="3f825-120">Mehrere Ressourcen buchen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die Arbeit zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="3f825-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="3f825-121">Weniger Ressourcen buchen als benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f825-121">Book fewer resources than are required.</span></span> <span data-ttu-id="3f825-122">In diesem Szenario sind die gebuchten Stunden geringer als die benötigten Stunden.</span><span class="sxs-lookup"><span data-stu-id="3f825-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="3f825-123">Das System führt Sie durch das Vorschlagen von Ressourcen statt durch Buchungen, damit der Anforderer die verbleibende Nachfrage verifizieren und nachverfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="3f825-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="3f825-124">Ressourcenverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3f825-124">Resource availability</span></span>

<span data-ttu-id="3f825-125">Es ist wichtig, dass Ressourcenmanager die Verfügbarkeit von Ressourcen anzeigen and Buchungen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="3f825-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="3f825-126">In manchen Fällen besteht zwar keine formelle Nachfrage (Ressourcenanfrage), aber ein Ressourcenmanager muss auf eine ungeplante Nachfrage reagieren können, die über Kanäle wie E-Mails, Telefonanrufe oder Sofortnachrichten eingeht.</span><span class="sxs-lookup"><span data-stu-id="3f825-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="3f825-127">Ressourcenmanager verwenden die Zeitplanübersicht, um Ressourcen und Buchungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3f825-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="3f825-128">Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="3f825-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="3f825-129">Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3f825-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="3f825-130">Die Zeitplanübersicht verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3f825-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="3f825-131">Eine Einstellung für die Zeitplanübersicht ermöglicht das Anzeigen einer Legende.</span><span class="sxs-lookup"><span data-stu-id="3f825-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="3f825-132">Wenn neben einer einzelnen buchbaren Ressource in der Zeitplanübersicht ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.</span><span class="sxs-lookup"><span data-stu-id="3f825-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="3f825-133">Da Dynamics 365 Project Operations die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.</span><span class="sxs-lookup"><span data-stu-id="3f825-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="3f825-134">Um mehr Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3f825-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]