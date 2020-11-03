---
title: Navigieren in der Benutzeroberfläche
description: Dieses Thema enthält Informationen zur Projektverwaltung in Dynamics 365 Project Vorgängen.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076442"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="e79e7-103">Navigieren in der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="e79e7-103">Navigating the user interface</span></span>

<span data-ttu-id="e79e7-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="e79e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="e79e7-105">Überblick</span><span class="sxs-lookup"><span data-stu-id="e79e7-105">Overview</span></span>

<span data-ttu-id="e79e7-106">Das Hauptprojektformular ist in mehrere Registerkarten unterteilt.</span><span class="sxs-lookup"><span data-stu-id="e79e7-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="e79e7-107">Jede Registerkarte repräsentiert eine andere Detailebene innerhalb des Projekts.</span><span class="sxs-lookup"><span data-stu-id="e79e7-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="e79e7-108">**Zusammenfassung** : Bietet eine Beschreibung des Projekts und aggregiert sowohl die geplante als auch die tatsächliche Projektleistung.</span><span class="sxs-lookup"><span data-stu-id="e79e7-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Registerkarte und Felder der Zusammenfassung](media/navigation7.png)

- <span data-ttu-id="e79e7-110">**Aufgaben** : Enthält die Details zum Projektstrukturplan, die durch eine Rasteransicht, eine Übersicht und ein Gantt dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e79e7-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Registerkarte und Felder der Aufgaben](media/navigation8.png)

- <span data-ttu-id="e79e7-112">**Team** : Enthält Details zu den Projektteilnehmern</span><span class="sxs-lookup"><span data-stu-id="e79e7-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="e79e7-113">In dieser Ansicht wird auch der zugewiesene Aufwand jedes Teammitglieds zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e79e7-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Registerkarte und Felder des Teams](media/navigation9.png)

- <span data-ttu-id="e79e7-115">**Ressourcenzuweisungen** : Bietet eine zeitgesteuerte Ansicht des Aufwands für jede Ressource in einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="e79e7-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Registerkarte und Felder für Ressourcenzuweisungen](media/navigation10.png)

- <span data-ttu-id="e79e7-117">**Ressourcenabstimmung** : Bietet eine zeitgesteuerte Ansicht der Unterschiede zwischen den Zuweisungen der einzelnen benannten Ressourcen und ihren Buchungen.</span><span class="sxs-lookup"><span data-stu-id="e79e7-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Registerkarte und Felder für die Abstimmung](media/navigation11.png)

- <span data-ttu-id="e79e7-119">**Schätzungen** : Bietet eine zeitgesteuerte Ansicht der Kosten- und Umsatzschätzungen eines Projekts</span><span class="sxs-lookup"><span data-stu-id="e79e7-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Registerkarte und Felder der Schätzung](media/navigation12.png)

- <span data-ttu-id="e79e7-121">**Verfolgung** : Bietet eine Ansicht, die den Fortschritt von Aufgaben in der Projektstrukturplan für Aufwand, Kosten und Umsatz anzeigt</span><span class="sxs-lookup"><span data-stu-id="e79e7-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Registerkarte und Felder der Verfolgung](media/navigation13.png)

- <span data-ttu-id="e79e7-123">**Vertrieb** : Bietet Deep Links zu Angeboten und Verträgen, die mit dem Projekt verbunden sind</span><span class="sxs-lookup"><span data-stu-id="e79e7-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="e79e7-124">**Ausgabenschätzungen** : Stellt ein Raster bereit, das die Projektkosten basierend auf den Kategorien der Organisationskosten definiert</span><span class="sxs-lookup"><span data-stu-id="e79e7-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Registerkarte und Felder der Ausgabenschätzungen](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="e79e7-126">Rastersteuerungen</span><span class="sxs-lookup"><span data-stu-id="e79e7-126">Grid controls</span></span>

<span data-ttu-id="e79e7-127">Im Folgenden finden Sie eine kurze Übersicht über die typischen Steuerelemente auf den verschiedenen Registerkarten für die Projektplanung.</span><span class="sxs-lookup"><span data-stu-id="e79e7-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="e79e7-128">Refresh</span><span class="sxs-lookup"><span data-stu-id="e79e7-128">Refresh</span></span>

<span data-ttu-id="e79e7-129">**Aktualisierung** : Ruft die neuesten Daten vom Server ab, wenn nach dem Laden des Rasters Änderungen aufgetreten sind</span><span class="sxs-lookup"><span data-stu-id="e79e7-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Schaltfläche „Aktualisieren“](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="e79e7-131">Gruppieren nach</span><span class="sxs-lookup"><span data-stu-id="e79e7-131">Group by</span></span>

<span data-ttu-id="e79e7-132">**Gruppieren nach** : Aktualisiert die Gruppierung der Zeilen im Raster, um entweder Ressourcen, Rollen oder Kategorien entsprechend den Anforderungen des Benutzers wiederzugeben</span><span class="sxs-lookup"><span data-stu-id="e79e7-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Nach Schaltfläche gruppieren](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="e79e7-134">Zurück/Weiter</span><span class="sxs-lookup"><span data-stu-id="e79e7-134">Previous/Next</span></span>

<span data-ttu-id="e79e7-135">**Zurück**/**Weiter** : Aktualisieren Sie die sichtbaren Zeiträume in den zeitgesteuerten Rastern.</span><span class="sxs-lookup"><span data-stu-id="e79e7-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Schaltflächen „Zurück“ und „Weiter“](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="e79e7-137">Zeitskala</span><span class="sxs-lookup"><span data-stu-id="e79e7-137">Timescale</span></span>

<span data-ttu-id="e79e7-138">**Zeitskala** : Ändern Sie die Aggregation der zeitlich gesteuerten Daten zwischen Tagen, Wochen, Monaten und Jahren.</span><span class="sxs-lookup"><span data-stu-id="e79e7-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Schaltfläche „Zeitskala“](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="e79e7-140">Aufklappen</span><span class="sxs-lookup"><span data-stu-id="e79e7-140">Expand</span></span>

<span data-ttu-id="e79e7-141">**Erweitern** : Rendern Sie das sichtbare Raster im Vollbildmodus, um zusätzliche Rollen besser erkennen zu können.</span><span class="sxs-lookup"><span data-stu-id="e79e7-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Schaltfläche 'Erweitern'](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="e79e7-143">Zeitphase bis</span><span class="sxs-lookup"><span data-stu-id="e79e7-143">Time-phase by</span></span>

<span data-ttu-id="e79e7-144">**Zeitphase bis** : Aktualisieren Sie die Gruppierung der Zeilen im Raster, um Kostenschätzungen für Umsatzschätzungen widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="e79e7-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="e79e7-145">Diese Steuerung gilt auch für das Schätzungsskript und das Verfolgungsraster.</span><span class="sxs-lookup"><span data-stu-id="e79e7-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Zeitphase nach Schaltfläche](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="e79e7-147">Spalte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e79e7-147">Add column</span></span>

<span data-ttu-id="e79e7-148">**Spalte hinzufügen** : Ermöglicht dem Benutzer, die sichtbaren Spalten im Raster zu definieren</span><span class="sxs-lookup"><span data-stu-id="e79e7-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="e79e7-149">Zu den Rastern im Formular **Projektplanung** können nur Standardspalten hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e79e7-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Schaltfläche „Spalte hinzufügen“](media/navigation5.png)
