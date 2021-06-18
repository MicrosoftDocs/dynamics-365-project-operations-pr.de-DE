---
title: Erstellen einer Projektbuchung aus der Zeitplanübersicht
description: Dieses Thema enthält Informationen über die Erstellung einer Projektbuchung aus der Zeitplanübersicht.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992965"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="675d9-103">Erstellen einer Projektbuchung aus der Zeitplanübersicht</span><span class="sxs-lookup"><span data-stu-id="675d9-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="675d9-104">Sie können eine Ressource direkt auf der Registerkarte **Team** des Projekts für ein Projekt buchen oder eine Ressourcenanforderung aus einer allgemeinen Teammitgliedzuweisung generieren und dann die generierte Anforderung mit einem Projektteammitglied erfüllen.</span><span class="sxs-lookup"><span data-stu-id="675d9-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="675d9-105">Sie können eine Ressource für ein Projekt auch über die Zeitplanübersicht buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="675d9-106">Dafür stehen drei Möglichkeiten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="675d9-106">There are three ways to do this:</span></span>

- <span data-ttu-id="675d9-107">**Von einer generierten Ressourcenanforderung buchen:** Sie können eine Ressourcenanforderung generieren, nachdem Sie eine generische Ressource erstellt und Aufgaben innerhalb eines Projekts zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="675d9-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="675d9-108">**Von der primären Anforderung buchen:** Die primären Anforderungen werden in der Zeitplanübersicht auf der Registerkarte **Projekt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="675d9-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="675d9-109">**Von einer neuen Ressourcenanforderungen buchen:** Sie können eine Ressourcenanforderung von Grund auf neu erstellen und sie einem Projekt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="675d9-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="675d9-110">Auf der Zeitplanübersicht werden diese Ressourcenanforderungen auf der Registerkarte **Offene Anforderungen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="675d9-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="675d9-111">Von einer generierten Ressourcenanforderung buchen</span><span class="sxs-lookup"><span data-stu-id="675d9-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="675d9-112">Sie können eine allgemeine Ressource erstellen und diesen einer oder mehreren Aufgaben innerhalb eines Projekts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="675d9-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="675d9-113">Anschließend können Sie aus dem generischen Teammitglied eine Ressourcenanforderung generieren.</span><span class="sxs-lookup"><span data-stu-id="675d9-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="675d9-114">Auf der Zeitplanübersicht wird diese Ressource auf der Registerkarte **Offene Anforderungen** angezeigt. Gegebenenfalls muss der Spaltenfilter im Raster verwendet werden, wenn Sie viele geöffnete Anforderungen haben.</span><span class="sxs-lookup"><span data-stu-id="675d9-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="675d9-115">![Registerkarte Anforderungen auf der Zeitplanübersicht](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot der Anmeldungen und Zuweisungstabellen")</span><span class="sxs-lookup"><span data-stu-id="675d9-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="675d9-116">Wählen Sie die erforderliche Anforderung aus.</span><span class="sxs-lookup"><span data-stu-id="675d9-116">Select the requirement.</span></span> <span data-ttu-id="675d9-117">Die Registerkarte **Verfügbarkeit durchsuchen** wird oben in der ausgewählten Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="675d9-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="675d9-118">Beim Auswählen der Registerkarte wird der Zeitplanassistent-Modus der Zeitplanübersicht geöffnet und die verfügbaren Ressourcen gefiltert, um die Ressourcenanforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="675d9-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="675d9-119">Danach können Sie eine Ressource buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="675d9-120">Sie können die ausgewählte Zeile auch vom unteren Rand der Zeitplanübersicht in eine Ressourcenzelle im Raster darüber ziehen und dort ablegen.</span><span class="sxs-lookup"><span data-stu-id="675d9-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="675d9-121">Dadurch wird der **Anmeldungsbereich erstellen** rechts geöffnet.</span><span class="sxs-lookup"><span data-stu-id="675d9-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="675d9-122">**Buchen** auswählen, um die Ressource im Projektteam zu buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-122">Selecting **Book** books the resource onto the project team.</span></span>

![Ressourcen-Anmeldungsbereich erstellen](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="675d9-124">Buch der primären Anforderung</span><span class="sxs-lookup"><span data-stu-id="675d9-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="675d9-125">Ein Projekt in Project Service erstellen erstellt automatisch eine Ressourcenanforderung, die die primäre Anforderung genannt wird.</span><span class="sxs-lookup"><span data-stu-id="675d9-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="675d9-126">Dies ist eine leere Anforderung, mit der eine Ressource schnell über die Zeitplanübersicht gebucht werden kann, ohne eine Anforderung zu generieren oder von Grund auf neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="675d9-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="675d9-127">Da die Anforderung leer ist, müssen Sie die Termine und -stunden (falls zutreffend) sowie die Zuordnungsmethode angeben.</span><span class="sxs-lookup"><span data-stu-id="675d9-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="675d9-128">Um eine Ressource mit einer primären Anforderung zu buchen, wählen Sie auf der Zeitplanübersicht die Registerkarte **Projekt** aus. Möglicherweise müssen Sie den Spaltenfilter auf der Spalte **Projekt** verwenden, wenn Sie viele Projekte haben.</span><span class="sxs-lookup"><span data-stu-id="675d9-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="675d9-129">![Spaltenfilter auf der Zeitplanübersicht anzeigen](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot der Anmeldungen und Zuweisungstabellen")</span><span class="sxs-lookup"><span data-stu-id="675d9-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="675d9-130">Wählen Sie die Anforderung aus, die nur den Projektnamen als Namen und eine Dauer von Null (0) hat.</span><span class="sxs-lookup"><span data-stu-id="675d9-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="675d9-131">Wählen Sie die Registerkarte **Verfügbarkeit durchsuchen**, die oben in der ausgewählten Zeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="675d9-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="675d9-132">Dies hat zur Folge, dass die Zeitplanübersicht in den Zeitplanassistentenmodus wechselt und die verfügbaren Ressourcen anzeigt, die für das Projekt gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="675d9-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="675d9-133">Da eine **Primäre Anforderung** eine leere Anforderung mit einer Dauer von Null (0) ist, müssen Sie die Dauer im Bereich **Ressourcenbuchung erstellen** festlegen, wenn Sie eine Ressource auswählen und buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="675d9-134">Sie können die **Primäre Projektanforderung** am unteren Rand der Zeitplanübersicht auswählen, auf eine Ressource ziehen und dort ablegen, um sie zu zu buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="675d9-135">Da die **Primäre Anforderung** eine leere Anforderung mit einer Dauer von Null (0) ist, müssen Sie die Dauer im Bereich **Ressourcenbuchung erstellen** festlegen, wenn Sie eine Ressource auswählen und buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="675d9-136">Wenn Sie eine Ressource über die **Primäre Anforderung** in der Zeitplanübersicht buchen, fügen Sie sie dem Projektteam ohne Zuweisungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="675d9-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="675d9-137">Von einer neuen Ressourcenanforderung buchen</span><span class="sxs-lookup"><span data-stu-id="675d9-137">Book from a new resource requirement</span></span>
<span data-ttu-id="675d9-138">Führen Sie die folgenden Schritte aus, um aus einer neuen Ressourcenanforderung zu buchen.</span><span class="sxs-lookup"><span data-stu-id="675d9-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="675d9-139">Gehen Sie zu **Ressourcenanforderungen** und wählen Sie dann **Neu** aus, um eine neue Ressourcenanforderung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="675d9-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="675d9-140">Wählen Sie auf der Registerkarte **Projekt** ein Projekt aus, um die Anforderung dem Projekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="675d9-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="675d9-141">Auf der Zeitplanübersicht wird diese neue Anforderung als **Offene Anforderung** angezeigt, die Sie erfüllen können.</span><span class="sxs-lookup"><span data-stu-id="675d9-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="675d9-142">Buchen Sie die Ressource, um sie dem Projektteam hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="675d9-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="675d9-143">Nachdem die Ressource gebucht wurde, müssen Sie Aufgaben manuell zuweisen.</span><span class="sxs-lookup"><span data-stu-id="675d9-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]