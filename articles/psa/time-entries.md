---
title: Zeiteinträge erstellen
description: Dieses Thema bietet Informationen zur Vorgehensweise beim Erstellen von Zeiteinträgen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 520d3a6e6cc3d486d778c66c2ef7fd3ff20cd582
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149677"
---
# <a name="create-time-entries"></a><span data-ttu-id="c539e-103">Zeiteinträge erstellen</span><span class="sxs-lookup"><span data-stu-id="c539e-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c539e-104">In früheren Versionen von Dynamics 365 Project Service Automation wurden Zeiteintragungen wöchentlich eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c539e-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="c539e-105">In Version 3 von Project Service Automation werden Zeiteinträge täglich eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c539e-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="c539e-106">Nachdem einige Zeiteinträge erstellt wurden, können Sie allerdings Massenerstellungen oder -kopiervorgänge vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c539e-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="c539e-107">Einen Zeiteintrag erstellen</span><span class="sxs-lookup"><span data-stu-id="c539e-107">Create a time entry</span></span>

<span data-ttu-id="c539e-108">Führen Sie die folgenden Schritte aus, um einen Zeiteintrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c539e-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="c539e-109">Wählen Sie auf der Seite **Zeiteinträge** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="c539e-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="c539e-110">Geben Sie im Dialogfeld **Schnellerfassung: Zeiteintrag** die Dauer des Zeiteintrags in Minuten, Stunden oder Tagen ein.</span><span class="sxs-lookup"><span data-stu-id="c539e-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="c539e-111">Die Dauer muss im folgenden Format eingegeben werden: *x* Minuten, *x* Stunden oder *x* Tage.</span><span class="sxs-lookup"><span data-stu-id="c539e-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="c539e-112">Stunden und Tagen können auch als Dezimalwerte eingegeben werden, z. B. *x.x* Stunden oder *x.x* Tage.</span><span class="sxs-lookup"><span data-stu-id="c539e-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="c539e-113">Wählen Sie den Typ des Zeiteintrags und das Projekt aus, für das Sie den Zeiteintrag vornehmen.</span><span class="sxs-lookup"><span data-stu-id="c539e-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="c539e-114">Suchen Sie im Feld **Projektaufgabe** die Aufgabe für diesen Zeiteintrag.</span><span class="sxs-lookup"><span data-stu-id="c539e-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c539e-115">Wenn Sie einen Zeiteintrag für eine Aufgabe erstellen, die keinem Benutzer zugewiesen ist, wählen Sie im Feld **Projektaufgabe** die Schaltfläche **Suchen** aus, wählen Sie **Ansicht ändern** aus, und wählen Sie dann **Alle aktiven Projektaufgaben** aus, um alle Aufgaben aufzuführen.</span><span class="sxs-lookup"><span data-stu-id="c539e-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="c539e-116">Geben Sie eine Beschreibung ein, wenn eine Beschreibung erforderlich ist, und wählen Sie dann **Speichern und schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="c539e-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="c539e-117">Nachdem der Zeiteintrag erstellt und gespeichert ist, können Sie ihn im Zeiteintragsraster bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="c539e-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="c539e-118">Das Zeiteintragsraster unterstützt zwei Formate:</span><span class="sxs-lookup"><span data-stu-id="c539e-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="c539e-119">Sie können Zeiteinträge im Format **hh:mm** eingeben.</span><span class="sxs-lookup"><span data-stu-id="c539e-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="c539e-120">Dieses Format wird dann in Stunden und Bruchteile konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c539e-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="c539e-121">Sie können Stunden und Bruchteile direkt eingeben.</span><span class="sxs-lookup"><span data-stu-id="c539e-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="c539e-122">Beachten Sie, dass Bruchteile einer Stunde keine Minuten sind.</span><span class="sxs-lookup"><span data-stu-id="c539e-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="c539e-123">Daher stellen 1,5 Stunden 1 Stunde und 30 Minuten dar.</span><span class="sxs-lookup"><span data-stu-id="c539e-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="c539e-124">Dieselbe Regel gilt für Bruchteile eines Tags.</span><span class="sxs-lookup"><span data-stu-id="c539e-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="c539e-125">Ein Tag besteht aus 24 Stunden, und 0,5 Tage stehen für 12 Stunden.</span><span class="sxs-lookup"><span data-stu-id="c539e-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="c539e-126">Massenerstellung von Zeiteinträgen</span><span class="sxs-lookup"><span data-stu-id="c539e-126">Bulk create time entries</span></span>

<span data-ttu-id="c539e-127">Nachdem einige Zeiteinträge erstellt wurden, können Sie diese kopieren, um eine Massenerstellung zusätzlicher Zeiteinträge vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c539e-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="c539e-128">Wählen Sie auf der Seite **Zeiteinträge** die Option **Woche kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c539e-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="c539e-129">In der Feldgruppe **Zeitraum von** in den Feldern **Startdatum** und **Enddatum** definieren Sie den Datumsbereich, von dem Zeiteinträge kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c539e-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="c539e-130">In der Feldgruppe **Zeitraum bis** im Feld **Startdatum** geben Sie das Datum ein, für das Zeiteinträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c539e-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="c539e-131">Wählen Sie **Kopieren** aus, um eine Kopie für die Zeiteinträge zu erstellen, die dem Wochentag entsprechen, der in der Feldgruppe **Zeitraum bis** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c539e-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="c539e-132">Beispielsweise wird der Zeiteintrag für Montag letzter Woche zu Montag dieser Woche kopiert, der in der Feldgruppe **Zeitraum bis** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c539e-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="c539e-133">Daten für Zeiteinträge importieren</span><span class="sxs-lookup"><span data-stu-id="c539e-133">Import data for time entries</span></span>

<span data-ttu-id="c539e-134">Sie können Daten aus Projektbuchungen und Arbeitsaufträgen importieren.</span><span class="sxs-lookup"><span data-stu-id="c539e-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="c539e-135">Wenn Sie Daten importieren, können Sie den Datumsbereich der Buchungen angeben, die importiert werden sollen und dann explizit die Buchungen auswählen, die als **Entwurf**-Zeiteinträge erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c539e-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="c539e-136">Funktionen zum Gruppieren nach, Sortieren, Suchen und Filtern</span><span class="sxs-lookup"><span data-stu-id="c539e-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="c539e-137">Sie können Zeiteinträge nach den Dimensionen gruppieren und filtern, die in den Spalten angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c539e-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="c539e-138">Wählen Sie im Feld **Gruppieren nach** die Dimension aus, mithilfe der Zeiteinträge gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c539e-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="c539e-139">Sie können auch die Zeiteintragdatensätze in aufsteigender oder absteigender Reihenfolge sortieren, indem Sie den Sortierpfeil in den Spaltenüberschriften verwenden.</span><span class="sxs-lookup"><span data-stu-id="c539e-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="c539e-140">Zudem können Sie durch Auswahl der Schaltfläche **Filtern** in den Spaltenüberschriften Einträge ein- oder ausblenden. Dann können Sie im Feld **Suchen** den Text eingeben, der für die Suche von Zeiteinträgen anhand von Projektname, Projektaufgabe, Zeiteintrag oder Ressource verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c539e-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
