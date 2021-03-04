---
title: Projektressourcen vorschlagen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147517"
---
# <a name="propose-project-resources"></a><span data-ttu-id="67ddd-103">Projektressourcen vorschlagen</span><span class="sxs-lookup"><span data-stu-id="67ddd-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="67ddd-104">Ressourcenmanager können dem Projektmanager mithilfe einer Ressourcenanfrage eine Ressource vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="67ddd-105">Wählen Sie im Anfrageraster oder in der Anfrage selbst **Ressourcen suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="67ddd-106">Wählen Sie auf der Seite **Zeitplan-Assistent** die Ressource aus. Wählen Sie dann im Bereich **Ressourcenbuchung erstellen** im Feld **Buchungsstatus** die Option **Buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="67ddd-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Ausgewählte vorgeschlagene Ressource](media/Resource-Management-image62.png)

<span data-ttu-id="67ddd-108">Die folgenden Statusupdates erfolgen:</span><span class="sxs-lookup"><span data-stu-id="67ddd-108">The following status updates occur:</span></span>

- <span data-ttu-id="67ddd-109">Auf der Seite **Zeitplan-Assistent** werden die Statusbezeichner aktualisiert, um anzuzeigen, dass es sich um eine vorgeschlagene und nicht um eine verbindliche Buchung handelt.</span><span class="sxs-lookup"><span data-stu-id="67ddd-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Statusbezeichner für vorgeschlagene Buchung auf der Seite „Zeitplan-Assistent“](media/Resource-Management-image63.png)

- <span data-ttu-id="67ddd-111">Für die Ressourcenanfrage wird der Status in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="67ddd-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![In „Prüfung erforderlich“ geänderter Status der Ressourcenanfrage](media/Resource-Management-image64.png)

- <span data-ttu-id="67ddd-113">Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** für das generische Teammitglied in **Prüfung erforderlich** geändert.</span><span class="sxs-lookup"><span data-stu-id="67ddd-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Anforderungsstatus des generischen Teammitglieds auf der Registerkarte „Team“ geändert in „Prüfung erforderlich“](media/Resource-Management-image48.png)

<span data-ttu-id="67ddd-115">Der Projektmanager kann den Vorschlag annehmen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="67ddd-116">Zum Verarbeiten von Ressourcenanfragen können Ressourcenmanager einen der folgenden Ansätze auswählen:</span><span class="sxs-lookup"><span data-stu-id="67ddd-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="67ddd-117">Mehrere Ressourcen vorschlagen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die geforderten Stunden zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="67ddd-118">Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="67ddd-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="67ddd-119">In diesem Szenario können sich die Stunden nicht überschneiden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="67ddd-120">Schlagen Sie weniger Ressourcen als erforderlich vor.</span><span class="sxs-lookup"><span data-stu-id="67ddd-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="67ddd-121">In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die vom Anforderer angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="67ddd-122">Wenn der Anfragende die vorgeschlagenen Ressourcen akzeptiert, wird daher eine nicht erfüllte Ressourcenanforderung erstellt, um den restlichen Bedarf zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="67ddd-123">Mehrere Ressourcen buchen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die Arbeit zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="67ddd-124">Weniger Ressourcen buchen als benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-124">Book fewer resources than are required.</span></span> <span data-ttu-id="67ddd-125">In diesem Szenario sind die gebuchten Stunden geringer als die benötigten Stunden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="67ddd-126">Das System führt Sie durch das Vorschlagen von Ressourcen statt durch Buchungen, damit der Anforderer die verbleibende Nachfrage verifizieren und nachverfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="67ddd-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="67ddd-127">Abrechenbare Nutzung</span><span class="sxs-lookup"><span data-stu-id="67ddd-127">Billable utilization</span></span>

<span data-ttu-id="67ddd-128">Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf.</span><span class="sxs-lookup"><span data-stu-id="67ddd-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="67ddd-129">Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt.</span><span class="sxs-lookup"><span data-stu-id="67ddd-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="67ddd-130">Nutzungsberechnungen basieren auf den tatsächlichen Stunden, die von Ressourcen über genehmigte Zeiteinträge gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="67ddd-131">Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:</span><span class="sxs-lookup"><span data-stu-id="67ddd-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="67ddd-132">Abrechenbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="67ddd-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="67ddd-133">Nicht abrechenbare Nutzung = tatsächliche Zeit mit Abrechnungstyp-ID = nicht fakturierbare, komplementäre oder nicht verfügbare Stunden ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="67ddd-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="67ddd-134">Intern = tatsächliche Zeit ohne Vertriebsvertrag ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="67ddd-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="67ddd-135">Ressourcenkapazität = Ressourcenarbeitszeiten – arbeitsfreie Tage – Abwesenheit</span><span class="sxs-lookup"><span data-stu-id="67ddd-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="67ddd-136">Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="67ddd-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Ansicht „Ressourcennutzung“](media/Resource-Management-image65.png)

<span data-ttu-id="67ddd-138">Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat.</span><span class="sxs-lookup"><span data-stu-id="67ddd-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="67ddd-139">Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:</span><span class="sxs-lookup"><span data-stu-id="67ddd-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="67ddd-140">**Grün:** Abrechenbare Nutzung \>= Zielnutzung für die Ressource</span><span class="sxs-lookup"><span data-stu-id="67ddd-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="67ddd-141">**Gelb:** Zielnutzung – 20 \<= abrechenbare Nutzung \< Zielnutzung</span><span class="sxs-lookup"><span data-stu-id="67ddd-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="67ddd-142">**Rot:** abrechenbare Nutzung \< Zielnutzung – 20</span><span class="sxs-lookup"><span data-stu-id="67ddd-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="67ddd-143">Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="67ddd-144">Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource.</span><span class="sxs-lookup"><span data-stu-id="67ddd-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="67ddd-145">Navigieren Sie hierfür zu **Ressourcen** \> **Ressourcenrollen**.</span><span class="sxs-lookup"><span data-stu-id="67ddd-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="67ddd-146">Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="67ddd-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="67ddd-147">Navigieren Sie zu **Ressourcen** \> **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="67ddd-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="67ddd-148">Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="67ddd-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="67ddd-149">Sie können zusätzliche Rollen hinzufügen, für die **Ist-Standard = Nein** gilt.</span><span class="sxs-lookup"><span data-stu-id="67ddd-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="67ddd-150">Die Rolle mit **Ist Standard = Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="67ddd-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Festgelegte Standardrolle](media/Resource-Management-image67.png)

<span data-ttu-id="67ddd-152">Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="67ddd-153">Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.</span><span class="sxs-lookup"><span data-stu-id="67ddd-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="67ddd-154">Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.</span><span class="sxs-lookup"><span data-stu-id="67ddd-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="67ddd-155">Ressourcenverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="67ddd-155">Resource availability</span></span>

<span data-ttu-id="67ddd-156">Es ist wichtig, dass Ressourcenmanager die Verfügbarkeit von Ressourcen anzeigen and Buchungen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="67ddd-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="67ddd-157">In manchen Fällen besteht zwar keine formelle Nachfrage (Ressourcenanfrage), aber ein Ressourcenmanager muss auf eine ungeplante Nachfrage reagieren können, die über Kanäle wie E-Mails, Telefonanrufe oder Sofortnachrichten eingeht.</span><span class="sxs-lookup"><span data-stu-id="67ddd-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="67ddd-158">Ressourcenmanager verwenden die Zeitplanübersicht, um Ressourcen und Buchungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="67ddd-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="67ddd-159">Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet.</span><span class="sxs-lookup"><span data-stu-id="67ddd-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="67ddd-160">Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-160">Resource bookings consume the capacity of the resources.</span></span>

![Zeitplanübersicht](media/Resource-Management-image68.png)

<span data-ttu-id="67ddd-162">Die Zeitplanübersicht verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="67ddd-163">Eine Einstellung für die Zeitplanübersicht ermöglicht das Anzeigen einer Legende.</span><span class="sxs-lookup"><span data-stu-id="67ddd-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="67ddd-164">Wenn neben einer einzelnen buchbaren Ressource in der Zeitplanübersicht ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.</span><span class="sxs-lookup"><span data-stu-id="67ddd-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Erweiterte buchbare Ressource in der Zeitplanübersicht](media/Resource-Management-image69.png)

<span data-ttu-id="67ddd-166">Da Dynamics 365 Project Service Automation die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.</span><span class="sxs-lookup"><span data-stu-id="67ddd-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Details zu Ressourcenbuchungen für Projekte und Arbeitsaufträge](media/Resource-Management-image70.png)

<span data-ttu-id="67ddd-168">Um mehr Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="67ddd-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Ressourcenkarte](media/Resource-Management-image71.png)
