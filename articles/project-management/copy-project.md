---
title: Ein Projekt kopieren
description: Dieses Thema enthält Informationen zum Kopieren von Projekten in Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479518"
---
# <a name="copy-a-project"></a><span data-ttu-id="55967-103">Ein Projekt kopieren</span><span class="sxs-lookup"><span data-stu-id="55967-103">Copy a project</span></span>

<span data-ttu-id="55967-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="55967-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55967-105">Mithilfe von Dynamics 365 Project Operations können Sie schnell neue Projekte erstellen, indem Sie **Projekt kopieren** im Formular **Projekte** auswählen.</span><span class="sxs-lookup"><span data-stu-id="55967-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="55967-106">Um ein Projekt zu kopieren, öffnen Sie das zu kopierende Projekt, und wählen Sie dann **Projekt kopieren** aus.</span><span class="sxs-lookup"><span data-stu-id="55967-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="55967-107">Die Aktion kopiert:</span><span class="sxs-lookup"><span data-stu-id="55967-107">The action will copy:</span></span>

- <span data-ttu-id="55967-108">Projekteigenschaften (das geschätzte Startdatum wird aus dem Quellprojekt übernommen)</span><span class="sxs-lookup"><span data-stu-id="55967-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="55967-109">Die Projektstrukturplan</span><span class="sxs-lookup"><span data-stu-id="55967-109">The Work breakdown structure</span></span>
- <span data-ttu-id="55967-110">Projektteammitglieder</span><span class="sxs-lookup"><span data-stu-id="55967-110">Project team members</span></span>
- <span data-ttu-id="55967-111">Projektschätzungen</span><span class="sxs-lookup"><span data-stu-id="55967-111">Project estimates</span></span>
- <span data-ttu-id="55967-112">Projektausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="55967-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="55967-113">Projekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="55967-113">Project properties</span></span>

<span data-ttu-id="55967-114">Beim Kopieren des Projekts werden die Werte in den folgenden Feldern kopiert:</span><span class="sxs-lookup"><span data-stu-id="55967-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="55967-115">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="55967-115">Name</span></span>
- <span data-ttu-id="55967-116">Beschreibung des Dataflows</span><span class="sxs-lookup"><span data-stu-id="55967-116">Description</span></span>
- <span data-ttu-id="55967-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="55967-117">Customer</span></span>
- <span data-ttu-id="55967-118">Kalendervorlage</span><span class="sxs-lookup"><span data-stu-id="55967-118">Calendar Template</span></span>
- <span data-ttu-id="55967-119">Währung</span><span class="sxs-lookup"><span data-stu-id="55967-119">Currency</span></span>
- <span data-ttu-id="55967-120">Vertragseinheit</span><span class="sxs-lookup"><span data-stu-id="55967-120">Contracting Unit</span></span>
- <span data-ttu-id="55967-121">Projektmanager</span><span class="sxs-lookup"><span data-stu-id="55967-121">Project Manager</span></span>
- <span data-ttu-id="55967-122">Status</span><span class="sxs-lookup"><span data-stu-id="55967-122">Status</span></span>
- <span data-ttu-id="55967-123">Gesamtprojektstatus</span><span class="sxs-lookup"><span data-stu-id="55967-123">Overall Project Status</span></span>
- <span data-ttu-id="55967-124">Kommentare</span><span class="sxs-lookup"><span data-stu-id="55967-124">Comments</span></span>
- <span data-ttu-id="55967-125">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="55967-125">Estimates</span></span>
- <span data-ttu-id="55967-126">Voraussichtliches Startdatum</span><span class="sxs-lookup"><span data-stu-id="55967-126">Estimated Start Date</span></span>
- <span data-ttu-id="55967-127">Fertigstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="55967-127">Finish Date</span></span>
- <span data-ttu-id="55967-128">Aufwand (Stunden)</span><span class="sxs-lookup"><span data-stu-id="55967-128">Effort (Hours)</span></span>
- <span data-ttu-id="55967-129">Geschätzte Arbeitskosten</span><span class="sxs-lookup"><span data-stu-id="55967-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="55967-130">Geschätzte Ausgabenkosten</span><span class="sxs-lookup"><span data-stu-id="55967-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="55967-131">Projektstrukturplan</span><span class="sxs-lookup"><span data-stu-id="55967-131">Work breakdown structure</span></span>

<span data-ttu-id="55967-132">Beim Kopieren des Projekts wird die gesamte ressourcenintensive Projektstrukturplan kopiert.</span><span class="sxs-lookup"><span data-stu-id="55967-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="55967-133">Benannte Ressourcen werden durch generische Ressourcen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="55967-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="55967-134">Wenn die benannten Ressourcen nicht die gleichen Arbeitszeiten wie die generische Ressource haben, wird der Zeitplan neu berechnet und die Aufgabendauer kann sich ändern.</span><span class="sxs-lookup"><span data-stu-id="55967-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="55967-135">Projektteammitglieder</span><span class="sxs-lookup"><span data-stu-id="55967-135">Project team members</span></span>

<span data-ttu-id="55967-136">Wenn ein Projektteam aus dem Quellprojekt kopiert wird, werden die generischen Ressourcen kopiert.</span><span class="sxs-lookup"><span data-stu-id="55967-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="55967-137">Generische Ressourcenzuweisungen werden wie im Quellprojekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="55967-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="55967-138">Benannte Ressourcen werden in generische Teammitglieder konvertiert.</span><span class="sxs-lookup"><span data-stu-id="55967-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="55967-139">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="55967-139">Estimates</span></span>

<span data-ttu-id="55967-140">Wenn das Projekt kopiert wird, werden sowohl Ressourcen- als auch Ausgabenschätzungszeilen aus dem Quellprojekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="55967-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="55967-141">Informationen zum programmgesteuerten Zugriff auf „Projekt kopieren“ finden Sie unter [Projektvorlagen mit „Projekt kopieren“ entwickeln](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="55967-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
