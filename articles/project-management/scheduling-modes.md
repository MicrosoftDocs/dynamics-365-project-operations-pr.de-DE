---
title: Planungsmodi
description: In diesem Thema werden Planungsmodi erläutert.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116706"
---
# <a name="scheduling-modes"></a><span data-ttu-id="7a919-103">Planungsmodi</span><span class="sxs-lookup"><span data-stu-id="7a919-103">Scheduling modes</span></span>

<span data-ttu-id="7a919-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="7a919-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7a919-105">Dynamics 365 Project Operations bietet Organisationen die Möglichkeit zu definieren, wie sie Änderungen an Schlüsselvariablen in Aufgaben innerhalb der Projektstrukturplan verwalten.</span><span class="sxs-lookup"><span data-stu-id="7a919-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="7a919-106">Basierend auf den spezifischen Anforderungen der Organisation können Projektmanager Änderungen am Planungsmodus vornehmen, wenn ein Projekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a919-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="7a919-107">In Project Operations stehen drei Planungsmodi zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="7a919-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="7a919-108">Feste Dauer (dies ist der Standardmodus)</span><span class="sxs-lookup"><span data-stu-id="7a919-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="7a919-109">Fester Aufwand (*Arbeit)*</span><span class="sxs-lookup"><span data-stu-id="7a919-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="7a919-110">Feste Einheiten</span><span class="sxs-lookup"><span data-stu-id="7a919-110">Fixed units</span></span>

<span data-ttu-id="7a919-111">Die Werte, die von der Definition eines bestimmten Planungsmodus betroffen sind, werden durch die folgende Formel bestimmt:</span><span class="sxs-lookup"><span data-stu-id="7a919-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="7a919-112">Anstrengung = Dauer x Einheiten</span><span class="sxs-lookup"><span data-stu-id="7a919-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="7a919-113">Wenn Sie den Planungsmodus eines Projekts definieren, legen Sie einen dieser Werte fest, der dann nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a919-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="7a919-114">Wenn Sie diesen Wert als Konstante halten, wird diesem Wert Priorität eingeräumt. Dadurch wird das System benachrichtigt, ihn nicht zu ändern, wenn sich die beiden anderen Werte ändern.</span><span class="sxs-lookup"><span data-stu-id="7a919-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="7a919-115">Die folgende Tabelle enthält Informationen zu den Auswirkungen der Auswahl eines bestimmten Modus.</span><span class="sxs-lookup"><span data-stu-id="7a919-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="7a919-116">**In dieser Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="7a919-116">**In this task**</span></span>             | <span data-ttu-id="7a919-117">**Wenn Sie Einheiten überarbeiten**</span><span class="sxs-lookup"><span data-stu-id="7a919-117">**If you revise units**</span></span>   | <span data-ttu-id="7a919-118">**Wenn Sie Dauer überarbeiten**</span><span class="sxs-lookup"><span data-stu-id="7a919-118">**If you revise duration**</span></span> | <span data-ttu-id="7a919-119">**Wenn Sie Aufwand überarbeiten**</span><span class="sxs-lookup"><span data-stu-id="7a919-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="7a919-120">Feste Einheiten-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7a919-120">Fixed units task</span></span>     | <span data-ttu-id="7a919-121">Die Dauer wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-121">Duration is recalculated.</span></span> | <span data-ttu-id="7a919-122">Der Aufwand wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-122">Effort is recalculated.</span></span>    | <span data-ttu-id="7a919-123">Die Dauer wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="7a919-124">Fester Aufwand - Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7a919-124">Fixed effort task</span></span>    | <span data-ttu-id="7a919-125">Die Dauer wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-125">Duration is recalculated.</span></span> | <span data-ttu-id="7a919-126">Einheiten werden neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-126">Units are recalculated.</span></span>    | <span data-ttu-id="7a919-127">Die Dauer wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="7a919-128">Feste Dauer - Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7a919-128">Fixed duration task</span></span>  | <span data-ttu-id="7a919-129">Der Aufwand wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-129">Effort is recalculated.</span></span>   | <span data-ttu-id="7a919-130">Der Aufwand wird neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-130">Effort is recalculated.</span></span>    | <span data-ttu-id="7a919-131">Einheiten werden neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="7a919-131">Units are recalculated.</span></span>   |

<span data-ttu-id="7a919-132">Weitere Informationen zu den Auswirkungen eines bestimmten Modus finden Sie unter [ Ändern des Aufgabentyps für eine genauere Planung](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="7a919-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="7a919-133">In der Thema wird der Begriff **Arbeit** anstelle von **Aufwand** verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a919-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="7a919-134">Ändern Sie den Planungsmodus der Organisation</span><span class="sxs-lookup"><span data-stu-id="7a919-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="7a919-135">Führen Sie die folgenden Schritte aus, um den Planungsmodus einer Organisation zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7a919-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="7a919-136">Gehen Sie zu **Einstellungen**\> **Allgemein** \>**Parameter** und wählen Sie dann den Projektparameter aus.</span><span class="sxs-lookup"><span data-stu-id="7a919-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="7a919-137">Auf der Seite **Projektparameter** wählen Sie den Standardplanungsmodus für die Organisation aus und definieren Sie dann die Fähigkeit des Projektmanagers, die Einstellung beim Erstellen eines neuen Projekts zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="7a919-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="7a919-138">Ändern Sie die Planungsmoduseinstellung für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="7a919-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="7a919-139">Wenn eine Organisation dem Projektmanager erlaubt, den Standardplanungsmodus zu überschreiben, kann der Projektmanager diese Änderung vornehmen, wenn er ein neues Projekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a919-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="7a919-140">Nachdem das Projekt gespeichert wurde, kann der Planungsmodus jedoch nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7a919-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="7a919-141">Kopierte Projekte</span><span class="sxs-lookup"><span data-stu-id="7a919-141">Copied projects</span></span>

<span data-ttu-id="7a919-142">Da beim Ausführen der Aktion "Projekt kopieren" ein Projekt erstellt wird, kann der Projektmanager den Planungsmodus nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a919-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="7a919-143">Das Zielprojekt verwendet standardmäßig immer den auf Organisationsebene definierten Modus.</span><span class="sxs-lookup"><span data-stu-id="7a919-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="7a919-144">Kopierte Aufgaben</span><span class="sxs-lookup"><span data-stu-id="7a919-144">Copied tasks</span></span>

<span data-ttu-id="7a919-145">Wenn eine Aufgabe von einem Projekt in ein anderes kopiert wird, erbt die Aufgabe den Planungsmodus des Zielprojekts.</span><span class="sxs-lookup"><span data-stu-id="7a919-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
