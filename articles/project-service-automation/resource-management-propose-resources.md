---
title: Projektressourcen vorschlagen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722051"
---
# <a name="propose-project-resources"></a><span data-ttu-id="ade9c-103">Projektressourcen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="ade9c-103">Propose project resources</span></span>

<span data-ttu-id="ade9c-104">Ressourcenmanager können dem Projektmanager mithilfe einer Ressourcenanfrage eine Ressource vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="ade9c-105">Wählen Sie im Anfrageraster oder in der Anfrage selbst **Ressourcen suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="ade9c-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="ade9c-106">Wählen Sie auf der Seite **Zeitplan-Assistent** die Ressource aus. Wählen Sie dann im Bereich **Ressourcenbuchung erstellen** im Feld **Buchungsstatus** die Option **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="ade9c-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Ausgewählte vorgeschlagene Ressource](media/Resource-Management-image62.png)

<span data-ttu-id="ade9c-108">Die folgenden Statusupdates erfolgen:</span><span class="sxs-lookup"><span data-stu-id="ade9c-108">The following status updates occur:</span></span>

- <span data-ttu-id="ade9c-109">Auf der Seite **Zeitplan-Assistent** werden die Statusbezeichner aktualisiert, um anzuzeigen, dass es sich um eine vorgeschlagene und nicht um eine verbindliche Buchung handelt.</span><span class="sxs-lookup"><span data-stu-id="ade9c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusbezeichner für vorgeschlagene Buchung auf der Seite „Zeitplan-Assistent“](media/Resource-Management-image63.png)

- <span data-ttu-id="ade9c-111">Für die Ressourcenanfrage wird der Status in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="ade9c-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![In „Prüfung erforderlich“ geänderter Status der Ressourcenanfrage](media/Resource-Management-image64.png)

- <span data-ttu-id="ade9c-113">Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** für das generische Teammitglied in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="ade9c-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Anforderungsstatus des generischen Teammitglieds auf der Registerkarte „Team“ geändert in „Prüfung erforderlich“](media/Resource-Management-image48.png)

<span data-ttu-id="ade9c-115">Der Projektmanager kann den Vorschlag annehmen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="ade9c-116">Zum Verarbeiten von Ressourcenanfragen können Ressourcenmanager einen der folgenden Ansätze auswählen:</span><span class="sxs-lookup"><span data-stu-id="ade9c-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="ade9c-117">Schlagen Sie mehrere Ressourcen vor, um die Nachfrage zu befriedigen, falls zur Erfüllung der erforderlichen Stunden keine einzelne Ressource verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ade9c-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="ade9c-118">Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="ade9c-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="ade9c-119">In diesem Szenario können sich die Stunden nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="ade9c-120">Schlagen Sie weniger Ressourcen als erforderlich vor.</span><span class="sxs-lookup"><span data-stu-id="ade9c-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="ade9c-121">In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die vom Anforderer angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="ade9c-122">Daher wird, wenn der Anforderer die vorgeschlagenen Ressourcen annimmt, eine nicht erfüllte Ressourcenanforderung erstellt, um die restliche Nachfrage zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="ade9c-123">Buchen Sie mehrere Ressourcen, um die Nachfrage zu befriedigen, falls zum Abschließen der Arbeit keine einzelne Ressource verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ade9c-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="ade9c-124">Buchen Sie weniger Ressourcen als erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ade9c-124">Book fewer resources than are required.</span></span> <span data-ttu-id="ade9c-125">In diesem Szenario sind die gebuchten Stunden weniger als die erforderlichen Stunden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="ade9c-126">Das System führt Sie durch das Vorschlagen von Ressourcen statt durch Buchungen, damit der Anforderer die verbleibende Nachfrage verifizieren und nachverfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="ade9c-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="ade9c-127">Abrechenbare Nutzung</span><span class="sxs-lookup"><span data-stu-id="ade9c-127">Billable utilization</span></span>

<span data-ttu-id="ade9c-128">Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf.</span><span class="sxs-lookup"><span data-stu-id="ade9c-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="ade9c-129">Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ade9c-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="ade9c-130">Nutzungsberechnungen basieren auf den tatsächlichen Stunden, die von Ressourcen über genehmigte Zeiteinträge gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="ade9c-131">Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:</span><span class="sxs-lookup"><span data-stu-id="ade9c-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="ade9c-132">Abrechenbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="ade9c-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="ade9c-133">Nicht abrechenbare Nutzung = tatsächliche Zeit mit Abrechnungstyp-ID = nicht fakturierbare, komplementäre oder nicht verfügbare Stunden ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="ade9c-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="ade9c-134">Intern = tatsächliche Zeit ohne Vertriebsvertrag ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="ade9c-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="ade9c-135">Ressourcenkapazität = Ressourcenarbeitszeiten – arbeitsfreie Tage – Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="ade9c-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="ade9c-136">Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="ade9c-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Ansicht „Ressourcennutzung“](media/Resource-Management-image65.png)

<span data-ttu-id="ade9c-138">Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat.</span><span class="sxs-lookup"><span data-stu-id="ade9c-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="ade9c-139">Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:</span><span class="sxs-lookup"><span data-stu-id="ade9c-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="ade9c-140">**Grün:** Abrechenbare Nutzung \>= Zielnutzung für die Ressource</span><span class="sxs-lookup"><span data-stu-id="ade9c-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="ade9c-141">**Gelb:** Zielnutzung – 20 \<= abrechenbare Nutzung \< Zielnutzung</span><span class="sxs-lookup"><span data-stu-id="ade9c-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="ade9c-142">**Rot:** abrechenbare Nutzung \< Zielnutzung – 20</span><span class="sxs-lookup"><span data-stu-id="ade9c-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="ade9c-143">Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="ade9c-144">Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource.</span><span class="sxs-lookup"><span data-stu-id="ade9c-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="ade9c-145">Navigieren Sie hierfür zu **Ressourcen** \> **Ressourcenrollen**.</span><span class="sxs-lookup"><span data-stu-id="ade9c-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="ade9c-146">Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="ade9c-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="ade9c-147">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="ade9c-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="ade9c-148">Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ade9c-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="ade9c-149">Sie können zusätzliche Rollen hinzufügen, für die **Ist-Standard = Nein** gilt.</span><span class="sxs-lookup"><span data-stu-id="ade9c-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="ade9c-150">Die Rolle mit **Ist Standard = Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="ade9c-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Festgelegte Standardrolle](media/Resource-Management-image67.png)

<span data-ttu-id="ade9c-152">Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="ade9c-153">Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.</span><span class="sxs-lookup"><span data-stu-id="ade9c-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="ade9c-154">Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.</span><span class="sxs-lookup"><span data-stu-id="ade9c-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="ade9c-155">Ressourcenverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ade9c-155">Resource availability</span></span>

<span data-ttu-id="ade9c-156">Es ist wichtig, dass Ressourcenmanager die Verfügbarkeit von Ressourcen anzeigen and Buchungen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="ade9c-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="ade9c-157">In manchen Fällen besteht zwar keine formelle Nachfrage (Ressourcenanfrage), aber ein Ressourcenmanager muss auf eine ungeplante Nachfrage reagieren können, die über Kanäle wie E-Mails, Telefonanrufe oder Sofortnachrichten eingeht.</span><span class="sxs-lookup"><span data-stu-id="ade9c-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="ade9c-158">Ressourcenmanager verwenden die Zeitplanübersicht, um Ressourcen und Buchungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ade9c-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="ade9c-159">Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="ade9c-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="ade9c-160">Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-160">Resource bookings consume the capacity of the resources.</span></span>

![Zeitplanübersicht](media/Resource-Management-image68.png)

<span data-ttu-id="ade9c-162">Die Zeitplanübersicht verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="ade9c-163">Eine Einstellung für die Zeitplanübersicht ermöglicht das Anzeigen einer Legende.</span><span class="sxs-lookup"><span data-stu-id="ade9c-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="ade9c-164">Wenn neben einer einzelnen buchbaren Ressource in der Zeitplanübersicht ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.</span><span class="sxs-lookup"><span data-stu-id="ade9c-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Erweiterte buchbare Ressource in der Zeitplanübersicht](media/Resource-Management-image69.png)

<span data-ttu-id="ade9c-166">Da Dynamics 365 Project Service Automation die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.</span><span class="sxs-lookup"><span data-stu-id="ade9c-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Details zu Ressourcenbuchungen für Projekte und Arbeitsaufträge](media/Resource-Management-image70.png)

<span data-ttu-id="ade9c-168">Um mehr Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ade9c-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Ressourcenkarte](media/Resource-Management-image71.png)
