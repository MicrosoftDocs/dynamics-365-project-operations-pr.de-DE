---
title: Ein Projekt kopieren
description: Dieses Thema enthält Informationen zum Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091253"
---
# <a name="copy-a-project"></a><span data-ttu-id="c0aa0-103">Ein Projekt kopieren</span><span class="sxs-lookup"><span data-stu-id="c0aa0-103">Copy a project</span></span>

<span data-ttu-id="c0aa0-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="c0aa0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0aa0-105">Mithilfe von Dynamics 365 Project Operations können Sie schnell neue Projekte erstellen, indem Sie **Projekt kopieren** im Formular **Projekte** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="c0aa0-106">Um ein Projekt zu kopieren, öffnen Sie das zu kopierende Projekt, und wählen Sie dann **Projekt kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="c0aa0-107">Die Aktion kopiert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c0aa0-107">The action will copy the following:</span></span>

- <span data-ttu-id="c0aa0-108">Projekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0aa0-108">Project properties</span></span> 
- <span data-ttu-id="c0aa0-109">Projektstrukturplan</span><span class="sxs-lookup"><span data-stu-id="c0aa0-109">Work breakdown structure</span></span>
- <span data-ttu-id="c0aa0-110">Projektteammitglieder</span><span class="sxs-lookup"><span data-stu-id="c0aa0-110">Project team members</span></span>
- <span data-ttu-id="c0aa0-111">Projektschätzungen</span><span class="sxs-lookup"><span data-stu-id="c0aa0-111">Project estimates</span></span>
- <span data-ttu-id="c0aa0-112">Projektausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="c0aa0-112">Project expense estimates</span></span>
- <span data-ttu-id="c0aa0-113">Materialschätzungen Projekte</span><span class="sxs-lookup"><span data-stu-id="c0aa0-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="c0aa0-114">Projekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0aa0-114">Project properties</span></span>

<span data-ttu-id="c0aa0-115">Beim Kopieren des Projekts werden die Werte in den folgenden Feldern kopiert:</span><span class="sxs-lookup"><span data-stu-id="c0aa0-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="c0aa0-116">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="c0aa0-116">Name</span></span>
- <span data-ttu-id="c0aa0-117">Beschreibung des Dataflows</span><span class="sxs-lookup"><span data-stu-id="c0aa0-117">Description</span></span>
- <span data-ttu-id="c0aa0-118">Kunde</span><span class="sxs-lookup"><span data-stu-id="c0aa0-118">Customer</span></span>
- <span data-ttu-id="c0aa0-119">Kalendervorlage</span><span class="sxs-lookup"><span data-stu-id="c0aa0-119">Calendar Template</span></span>
- <span data-ttu-id="c0aa0-120">Währung</span><span class="sxs-lookup"><span data-stu-id="c0aa0-120">Currency</span></span>
- <span data-ttu-id="c0aa0-121">Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="c0aa0-121">Contracting Unit</span></span>
- <span data-ttu-id="c0aa0-122">Projektmanager</span><span class="sxs-lookup"><span data-stu-id="c0aa0-122">Project Manager</span></span>
- <span data-ttu-id="c0aa0-123">Status</span><span class="sxs-lookup"><span data-stu-id="c0aa0-123">Status</span></span>
- <span data-ttu-id="c0aa0-124">Gesamtprojektstatus</span><span class="sxs-lookup"><span data-stu-id="c0aa0-124">Overall Project Status</span></span>
- <span data-ttu-id="c0aa0-125">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c0aa0-125">Comments</span></span>
- <span data-ttu-id="c0aa0-126">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="c0aa0-126">Estimates</span></span>
- <span data-ttu-id="c0aa0-127">Geschätztes Startdatum: Dies ist das Datum, an dem das Projekt aus der Kopie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="c0aa0-128">Voraussichtliches Enddatum: Dieses Datum wird basierend auf dem Startdatum des neuen Projekts angepasst, das aus der Kopie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="c0aa0-129">Aufwand (Stunden)</span><span class="sxs-lookup"><span data-stu-id="c0aa0-129">Effort (Hours)</span></span>
- <span data-ttu-id="c0aa0-130">Geschätzte Arbeitskosten</span><span class="sxs-lookup"><span data-stu-id="c0aa0-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="c0aa0-131">Geschätzte Ausgabenkosten</span><span class="sxs-lookup"><span data-stu-id="c0aa0-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="c0aa0-132">Geschätzte Materialkosten</span><span class="sxs-lookup"><span data-stu-id="c0aa0-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="c0aa0-133">Projekt kopieren ist ein lang andauernder Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-133">Copy project is a long running operation.</span></span> <span data-ttu-id="c0aa0-134">Projektdatensätze, ihre relevanten Attribute und viele zugehörige Entitäten werden ebenfalls kopiert.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="c0aa0-135">Aufgrund der langen Laufzeit des Vorgangs wird die Zielprojektseite nach dem Start des Kopiervorgangs für die Bearbeitung gesperrt, bis der Kopiervorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="c0aa0-136">Projektstrukturplan</span><span class="sxs-lookup"><span data-stu-id="c0aa0-136">Work breakdown structure</span></span>

<span data-ttu-id="c0aa0-137">Beim Kopieren des Projekts wird die gesamte ressourcenintensive Projektstrukturplan kopiert.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="c0aa0-138">Benannte Ressourcen werden durch generische Ressourcen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="c0aa0-139">Wenn die benannten Ressourcen nicht die gleichen Arbeitszeiten wie die generische Ressource haben, wird der Zeitplan neu berechnet und die Aufgabendauer kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="c0aa0-140">Projektteammitglieder</span><span class="sxs-lookup"><span data-stu-id="c0aa0-140">Project team members</span></span>

<span data-ttu-id="c0aa0-141">Wenn ein Projektteam aus dem Quellprojekt kopiert wird, werden die generischen Ressourcen kopiert.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="c0aa0-142">Generische Ressourcenzuweisungen werden wie im Quellprojekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="c0aa0-143">Benannte Ressourcen werden in generische Teammitglieder konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="c0aa0-144">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="c0aa0-144">Estimates</span></span>

<span data-ttu-id="c0aa0-145">Beim Kopieren des Projekts werden Ressourcen-, Aufwands- und Materialkalkulationszeilen aus dem Quellprojekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="c0aa0-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="c0aa0-146">Informationen zum programmgesteuerten Zugriff auf „Projekt kopieren“ finden Sie unter [Projektvorlagen mit „Projekt kopieren“ entwickeln](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa0-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
