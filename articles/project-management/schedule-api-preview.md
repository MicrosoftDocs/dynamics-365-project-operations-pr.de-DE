---
title: Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen
description: Dieses Thema enthält Informationen und Beispiele für die Verwendung von Zeitplan-APIs.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116796"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="b4e86-103">Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen</span><span class="sxs-lookup"><span data-stu-id="b4e86-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="b4e86-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="b4e86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b4e86-105">Einige oder alle der in diesem Thema genannten Funktionen stehen im Rahmen einer Vorschauversion zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b4e86-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="b4e86-106">Inhalt und Funktionalität können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="b4e86-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="b4e86-107">Planungsentitäten</span><span class="sxs-lookup"><span data-stu-id="b4e86-107">Scheduling entities</span></span>

<span data-ttu-id="b4e86-108">Zeitplan-APIs bieten die Möglichkeit, Erstellungs-, Aktualisierungs- und Löschvorgänge mit **Planungsentitäten** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="b4e86-109">Diese Entitäten werden über das Planungsmodul in Project für das Web verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b4e86-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="b4e86-110">Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten** wurden in früheren Version von Dynamics 365 Project Operations eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="b4e86-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="b4e86-111">Die folgende Tabelle enthält eine vollständige Liste der **Planungsentitäten**.</span><span class="sxs-lookup"><span data-stu-id="b4e86-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="b4e86-112">Entitätsname</span><span class="sxs-lookup"><span data-stu-id="b4e86-112">Entity name</span></span>  | <span data-ttu-id="b4e86-113">Logischer Entitätsname</span><span class="sxs-lookup"><span data-stu-id="b4e86-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="b4e86-114">Project</span><span class="sxs-lookup"><span data-stu-id="b4e86-114">Project</span></span> | <span data-ttu-id="b4e86-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b4e86-115">msdyn_project</span></span> |
| <span data-ttu-id="b4e86-116">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="b4e86-116">Project Task</span></span>  | <span data-ttu-id="b4e86-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="b4e86-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="b4e86-118">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="b4e86-118">Project Task Dependency</span></span>  | <span data-ttu-id="b4e86-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="b4e86-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="b4e86-120">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="b4e86-120">Resource Assignment</span></span> | <span data-ttu-id="b4e86-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="b4e86-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="b4e86-122">Projekt-Bucket</span><span class="sxs-lookup"><span data-stu-id="b4e86-122">Project Bucket</span></span>  | <span data-ttu-id="b4e86-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="b4e86-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="b4e86-124">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="b4e86-124">Project Team Member</span></span> | <span data-ttu-id="b4e86-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="b4e86-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="b4e86-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="b4e86-126">OperationSet</span></span>

<span data-ttu-id="b4e86-127">OperationSet ist ein Arbeitseinheitsmuster, das verwendet werden kann, wenn innerhalb einer Transaktion mehrere zeitplanbezogene Anforderungen verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="b4e86-128">Zeitplan-APIs</span><span class="sxs-lookup"><span data-stu-id="b4e86-128">Schedule APIs</span></span>

<span data-ttu-id="b4e86-129">Im Folgenden finden Sie eine Liste der aktuellen Zeitplan-APIs.</span><span class="sxs-lookup"><span data-stu-id="b4e86-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="b4e86-130">**msdyn_CreateProjectV1**: Mit dieser API kann ein Projekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="b4e86-131">Der Projekt- und Standardprojekt-Bucket wird sofort erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4e86-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="b4e86-132">**msdyn_CreateTeamMemberV1**: Mit dieser API kann ein Projektteammitglied erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="b4e86-133">Der Teammitgliedsdatensatz wird sofort erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4e86-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="b4e86-134">**msdyn_CreateOperationSetV1**: Mit dieser API können mehrere Anforderungen geplant werden, die innerhalb einer Transaktion ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="b4e86-135">**msdyn_PSSCreateV1**: Mit dieser API kann eine Entität erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="b4e86-136">Die Entität kann eine der Planungsentitäten sein, die den Erstellungsvorgang unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="b4e86-137">**msdyn_PSSUpdateV1**: Mit dieser API kann eine Entität aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="b4e86-138">Die Entität kann eine der Planungsentitäten sein, die den Aktualisierungsvorgang unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="b4e86-139">**msdyn_PSSDeleteV1**: Mit dieser API kann eine Entität gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="b4e86-140">Die Entität kann eine der Planungsentitäten sein, die den Löschvorgang unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="b4e86-141">**msdyn_ExecuteOperationSetV1**: Diese API wird verwendet, um alle Operationen innerhalb des angegebenen Operationssatzes auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="b4e86-142">Verwenden von Zeitplan-APIs mit OperationSet</span><span class="sxs-lookup"><span data-stu-id="b4e86-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="b4e86-143">Weil Aufzeichnungen sowohl mit **CreateProjectV1** als auch **CreateTeamMemberV1** sofort erstellt werden, können diese APIs nicht direkt im **OperationSet** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="b4e86-144">Sie können jedoch die API verwenden, um die erforderlichen Datensätze zu erstellen, ein **OperationSet** zu erstellen und dann diese vorab erstellten Datensätze im **OperationSet** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="b4e86-145">Unterstützte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="b4e86-145">Supported operations</span></span>

| <span data-ttu-id="b4e86-146">Planungsentität</span><span class="sxs-lookup"><span data-stu-id="b4e86-146">Scheduling entity</span></span> | <span data-ttu-id="b4e86-147">Erstellen</span><span class="sxs-lookup"><span data-stu-id="b4e86-147">Create</span></span> | <span data-ttu-id="b4e86-148">Update</span><span class="sxs-lookup"><span data-stu-id="b4e86-148">Update</span></span> | <span data-ttu-id="b4e86-149">Entf</span><span class="sxs-lookup"><span data-stu-id="b4e86-149">Delete</span></span> | <span data-ttu-id="b4e86-150">Wichtige Überlegungen</span><span class="sxs-lookup"><span data-stu-id="b4e86-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="b4e86-151">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="b4e86-151">Project task</span></span> | <span data-ttu-id="b4e86-152">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-152">Yes</span></span> | <span data-ttu-id="b4e86-153">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-153">Yes</span></span> | <span data-ttu-id="b4e86-154">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-154">Yes</span></span> | <span data-ttu-id="b4e86-155">Kein Wert</span><span class="sxs-lookup"><span data-stu-id="b4e86-155">None</span></span> |
| <span data-ttu-id="b4e86-156">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="b4e86-156">Project task dependency</span></span> | <span data-ttu-id="b4e86-157">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-157">Yes</span></span> | <span data-ttu-id="b4e86-158">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-158">Yes</span></span> | | <span data-ttu-id="b4e86-159">Abhängigkeitsdatensätze für Projektaufgaben werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4e86-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="b4e86-160">Stattdessen kann ein alter Datensatz gelöscht und ein neuer Datensatz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b4e86-161">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="b4e86-161">Resource assignment</span></span> | <span data-ttu-id="b4e86-162">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-162">Yes</span></span> | <span data-ttu-id="b4e86-163">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-163">Yes</span></span> | | <span data-ttu-id="b4e86-164">Vorgänge mit den folgenden Feldern werden nicht unterstützt: **BookableResourceID**, **Aufwand**, **EffortCompleted**, **EffortRemaining** und **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="b4e86-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="b4e86-165">Ressourcenzuweisungsdatensätze werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4e86-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="b4e86-166">Stattdessen kann der alte Datensatz gelöscht und ein neuer Datensatz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="b4e86-167">Projekt-Bucket</span><span class="sxs-lookup"><span data-stu-id="b4e86-167">Project bucket</span></span> | <span data-ttu-id="b4e86-168">N/V</span><span class="sxs-lookup"><span data-stu-id="b4e86-168">N/A</span></span> | <span data-ttu-id="b4e86-169">N/V</span><span class="sxs-lookup"><span data-stu-id="b4e86-169">N/A</span></span> | <span data-ttu-id="b4e86-170">N/V</span><span class="sxs-lookup"><span data-stu-id="b4e86-170">N/A</span></span> | <span data-ttu-id="b4e86-171">Der Standard-Bucket wird mit der **CreateProjectV1**-API erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4e86-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="b4e86-172">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="b4e86-172">Project team member</span></span> | <span data-ttu-id="b4e86-173">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-173">Yes</span></span> | <span data-ttu-id="b4e86-174">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-174">Yes</span></span> | <span data-ttu-id="b4e86-175">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-175">Yes</span></span> | <span data-ttu-id="b4e86-176">Verwenden Sie für den Erstellungsvorgang die **CreateTeamMemberV1**-API.</span><span class="sxs-lookup"><span data-stu-id="b4e86-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="b4e86-177">Project</span><span class="sxs-lookup"><span data-stu-id="b4e86-177">Project</span></span> | <span data-ttu-id="b4e86-178">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-178">Yes</span></span> | <span data-ttu-id="b4e86-179">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-179">Yes</span></span> | <span data-ttu-id="b4e86-180">N/V</span><span class="sxs-lookup"><span data-stu-id="b4e86-180">N/A</span></span> | <span data-ttu-id="b4e86-181">Vorgänge mit den folgenden Feldern werden nicht unterstützt: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Aufwand**, **EffortCompleted**, **EffortRemaining**, **Fortschritt**, **Fertigstellen**, **TaskEarliestStart** und **Dauer**.</span><span class="sxs-lookup"><span data-stu-id="b4e86-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="b4e86-182">Diese APIs können mit Entitätsobjekten aufgerufen werden, die benutzerdefinierte Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4e86-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="b4e86-183">Diese ID-Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="b4e86-183">The ID property is optional.</span></span> <span data-ttu-id="b4e86-184">Wenn sie bereitgestellt wird, versucht das System, sie zu verwenden, und löst eine Ausnahme aus, wenn sie nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4e86-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="b4e86-185">Wenn sie nicht bereitgestellt wird, generiert das System sie.</span><span class="sxs-lookup"><span data-stu-id="b4e86-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="b4e86-186">Eingeschränkte Felder</span><span class="sxs-lookup"><span data-stu-id="b4e86-186">Restricted fields</span></span>

<span data-ttu-id="b4e86-187">In den folgenden Tabellen werden die Felder definiert, für die **Erstellen** und **Bearbeiten** eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="b4e86-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="b4e86-188">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="b4e86-188">Project task</span></span>

| <span data-ttu-id="b4e86-189">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="b4e86-189">**Logical name**</span></span>                       | <span data-ttu-id="b4e86-190">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="b4e86-190">**Can create**</span></span> | <span data-ttu-id="b4e86-191">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b4e86-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="b4e86-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="b4e86-193">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-193">no</span></span>             | <span data-ttu-id="b4e86-194">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-194">no</span></span>               |
| <span data-ttu-id="b4e86-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="b4e86-196">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-196">no</span></span>             | <span data-ttu-id="b4e86-197">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-197">no</span></span>               |
| <span data-ttu-id="b4e86-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="b4e86-198">msdyn_actualend</span></span>                        | <span data-ttu-id="b4e86-199">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-199">no</span></span>             | <span data-ttu-id="b4e86-200">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-200">no</span></span>               |
| <span data-ttu-id="b4e86-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="b4e86-202">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-202">no</span></span>             | <span data-ttu-id="b4e86-203">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-203">no</span></span>               |
| <span data-ttu-id="b4e86-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b4e86-205">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-205">no</span></span>             | <span data-ttu-id="b4e86-206">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-206">no</span></span>               |
| <span data-ttu-id="b4e86-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="b4e86-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="b4e86-208">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-208">no</span></span>             | <span data-ttu-id="b4e86-209">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-209">no</span></span>               |
| <span data-ttu-id="b4e86-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="b4e86-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="b4e86-211">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-211">no</span></span>             | <span data-ttu-id="b4e86-212">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-212">no</span></span>               |
| <span data-ttu-id="b4e86-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="b4e86-214">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-214">no</span></span>             | <span data-ttu-id="b4e86-215">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-215">no</span></span>               |
| <span data-ttu-id="b4e86-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b4e86-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="b4e86-217">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-217">no</span></span>             | <span data-ttu-id="b4e86-218">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-218">no</span></span>               |
| <span data-ttu-id="b4e86-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b4e86-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b4e86-220">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-220">no</span></span>             | <span data-ttu-id="b4e86-221">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-221">no</span></span>               |
| <span data-ttu-id="b4e86-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b4e86-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="b4e86-223">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-223">no</span></span>             | <span data-ttu-id="b4e86-224">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-224">no</span></span>               |
| <span data-ttu-id="b4e86-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="b4e86-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="b4e86-226">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-226">no</span></span>             | <span data-ttu-id="b4e86-227">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-227">no</span></span>               |
| <span data-ttu-id="b4e86-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="b4e86-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="b4e86-229">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-229">no</span></span>             | <span data-ttu-id="b4e86-230">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-230">no</span></span>               |
| <span data-ttu-id="b4e86-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="b4e86-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="b4e86-232">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-232">no</span></span>             | <span data-ttu-id="b4e86-233">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-233">no</span></span>               |
| <span data-ttu-id="b4e86-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="b4e86-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="b4e86-235">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-235">no</span></span>             | <span data-ttu-id="b4e86-236">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-236">no</span></span>               |
| <span data-ttu-id="b4e86-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="b4e86-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="b4e86-238">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-238">no</span></span>             | <span data-ttu-id="b4e86-239">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-239">no</span></span>               |
| <span data-ttu-id="b4e86-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="b4e86-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="b4e86-241">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-241">no</span></span>             | <span data-ttu-id="b4e86-242">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-242">no</span></span>               |
| <span data-ttu-id="b4e86-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="b4e86-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="b4e86-244">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-244">no</span></span>             | <span data-ttu-id="b4e86-245">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-245">no</span></span>               |
| <span data-ttu-id="b4e86-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="b4e86-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="b4e86-247">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-247">no</span></span>             | <span data-ttu-id="b4e86-248">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-248">no</span></span>               |
| <span data-ttu-id="b4e86-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b4e86-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="b4e86-250">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-250">no</span></span>             | <span data-ttu-id="b4e86-251">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-251">no</span></span>               |
| <span data-ttu-id="b4e86-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="b4e86-253">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-253">no</span></span>             | <span data-ttu-id="b4e86-254">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-254">no</span></span>               |
| <span data-ttu-id="b4e86-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="b4e86-256">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-256">no</span></span>             | <span data-ttu-id="b4e86-257">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-257">no</span></span>               |
| <span data-ttu-id="b4e86-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b4e86-259">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-259">no</span></span>             | <span data-ttu-id="b4e86-260">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-260">no</span></span>               |
| <span data-ttu-id="b4e86-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b4e86-262">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-262">no</span></span>             | <span data-ttu-id="b4e86-263">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-263">no</span></span>               |
| <span data-ttu-id="b4e86-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="b4e86-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="b4e86-265">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-265">no</span></span>             | <span data-ttu-id="b4e86-266">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-266">no</span></span>               |
| <span data-ttu-id="b4e86-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b4e86-267">msdyn_progress</span></span>                         | <span data-ttu-id="b4e86-268">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-268">no</span></span>             | <span data-ttu-id="b4e86-269">nein (ja für P4W)</span><span class="sxs-lookup"><span data-stu-id="b4e86-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="b4e86-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b4e86-271">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-271">no</span></span>             | <span data-ttu-id="b4e86-272">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-272">no</span></span>               |
| <span data-ttu-id="b4e86-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b4e86-274">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-274">no</span></span>             | <span data-ttu-id="b4e86-275">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-275">no</span></span>               |
| <span data-ttu-id="b4e86-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b4e86-277">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-277">no</span></span>             | <span data-ttu-id="b4e86-278">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-278">no</span></span>               |
| <span data-ttu-id="b4e86-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b4e86-280">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-280">no</span></span>             | <span data-ttu-id="b4e86-281">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-281">no</span></span>               |
| <span data-ttu-id="b4e86-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="b4e86-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="b4e86-283">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-283">no</span></span>             | <span data-ttu-id="b4e86-284">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-284">no</span></span>               |
| <span data-ttu-id="b4e86-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b4e86-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="b4e86-286">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-286">no</span></span>             | <span data-ttu-id="b4e86-287">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-287">no</span></span>               |
| <span data-ttu-id="b4e86-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="b4e86-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="b4e86-289">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-289">no</span></span>             | <span data-ttu-id="b4e86-290">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-290">no</span></span>               |
| <span data-ttu-id="b4e86-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b4e86-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="b4e86-292">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-292">no</span></span>             | <span data-ttu-id="b4e86-293">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-293">no</span></span>               |
| <span data-ttu-id="b4e86-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="b4e86-295">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-295">no</span></span>             | <span data-ttu-id="b4e86-296">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-296">no</span></span>               |
| <span data-ttu-id="b4e86-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="b4e86-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="b4e86-298">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-298">no</span></span>             | <span data-ttu-id="b4e86-299">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-299">no</span></span>               |
| <span data-ttu-id="b4e86-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b4e86-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="b4e86-301">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-301">no</span></span>             | <span data-ttu-id="b4e86-302">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-302">no</span></span>               |
| <span data-ttu-id="b4e86-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="b4e86-304">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-304">no</span></span>             | <span data-ttu-id="b4e86-305">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-305">no</span></span>               |
| <span data-ttu-id="b4e86-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b4e86-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b4e86-307">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-307">no</span></span>             | <span data-ttu-id="b4e86-308">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-308">no</span></span>               |
| <span data-ttu-id="b4e86-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b4e86-310">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-310">no</span></span>             | <span data-ttu-id="b4e86-311">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-311">no</span></span>               |
| <span data-ttu-id="b4e86-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="b4e86-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="b4e86-313">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-313">no</span></span>             | <span data-ttu-id="b4e86-314">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-314">no</span></span>               |
| <span data-ttu-id="b4e86-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="b4e86-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="b4e86-316">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-316">no</span></span>             | <span data-ttu-id="b4e86-317">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-317">no</span></span>               |
| <span data-ttu-id="b4e86-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="b4e86-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="b4e86-319">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-319">no</span></span>             | <span data-ttu-id="b4e86-320">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-320">no</span></span>               |
| <span data-ttu-id="b4e86-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b4e86-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b4e86-322">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-322">no</span></span>             | <span data-ttu-id="b4e86-323">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-323">no</span></span>               |
| <span data-ttu-id="b4e86-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="b4e86-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="b4e86-325">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-325">no</span></span>             | <span data-ttu-id="b4e86-326">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-326">no</span></span>               |
| <span data-ttu-id="b4e86-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="b4e86-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="b4e86-328">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-328">no</span></span>             | <span data-ttu-id="b4e86-329">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-329">no</span></span>               |
| <span data-ttu-id="b4e86-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="b4e86-330">msdyn_summary</span></span>                          | <span data-ttu-id="b4e86-331">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-331">no</span></span>             | <span data-ttu-id="b4e86-332">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-332">no</span></span>               |
| <span data-ttu-id="b4e86-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="b4e86-334">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-334">no</span></span>             | <span data-ttu-id="b4e86-335">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-335">no</span></span>               |
| <span data-ttu-id="b4e86-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="b4e86-337">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-337">no</span></span>             | <span data-ttu-id="b4e86-338">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="b4e86-339">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="b4e86-339">Project task dependency</span></span>

| <span data-ttu-id="b4e86-340">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="b4e86-340">**Logical name**</span></span>              | <span data-ttu-id="b4e86-341">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="b4e86-341">**Can create**</span></span> | <span data-ttu-id="b4e86-342">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b4e86-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="b4e86-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="b4e86-343">msdyn_linktype</span></span>                | <span data-ttu-id="b4e86-344">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-344">no</span></span>             | <span data-ttu-id="b4e86-345">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-345">no</span></span>           |
| <span data-ttu-id="b4e86-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="b4e86-346">msdyn_linktypename</span></span>            | <span data-ttu-id="b4e86-347">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-347">no</span></span>             | <span data-ttu-id="b4e86-348">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-348">no</span></span>           |
| <span data-ttu-id="b4e86-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="b4e86-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="b4e86-350">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-350">yes</span></span>            | <span data-ttu-id="b4e86-351">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-351">no</span></span>           |
| <span data-ttu-id="b4e86-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="b4e86-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="b4e86-353">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-353">yes</span></span>            | <span data-ttu-id="b4e86-354">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-354">no</span></span>           |
| <span data-ttu-id="b4e86-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="b4e86-355">msdyn_project</span></span>                 | <span data-ttu-id="b4e86-356">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-356">yes</span></span>            | <span data-ttu-id="b4e86-357">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-357">no</span></span>           |
| <span data-ttu-id="b4e86-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="b4e86-358">msdyn_projectname</span></span>             | <span data-ttu-id="b4e86-359">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-359">yes</span></span>            | <span data-ttu-id="b4e86-360">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-360">no</span></span>           |
| <span data-ttu-id="b4e86-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="b4e86-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="b4e86-362">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-362">yes</span></span>            | <span data-ttu-id="b4e86-363">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-363">no</span></span>           |
| <span data-ttu-id="b4e86-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="b4e86-364">msdyn_successortask</span></span>           | <span data-ttu-id="b4e86-365">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-365">yes</span></span>            | <span data-ttu-id="b4e86-366">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-366">no</span></span>           |
| <span data-ttu-id="b4e86-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="b4e86-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="b4e86-368">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-368">yes</span></span>            | <span data-ttu-id="b4e86-369">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="b4e86-370">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="b4e86-370">Resource assignment</span></span>

| <span data-ttu-id="b4e86-371">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="b4e86-371">**Logical name**</span></span>             | <span data-ttu-id="b4e86-372">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="b4e86-372">**Can create**</span></span> | <span data-ttu-id="b4e86-373">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b4e86-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="b4e86-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="b4e86-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="b4e86-375">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-375">yes</span></span>            | <span data-ttu-id="b4e86-376">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-376">no</span></span>           |
| <span data-ttu-id="b4e86-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="b4e86-378">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-378">yes</span></span>            | <span data-ttu-id="b4e86-379">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-379">no</span></span>           |
| <span data-ttu-id="b4e86-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="b4e86-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="b4e86-381">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-381">no</span></span>             | <span data-ttu-id="b4e86-382">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-382">no</span></span>           |
| <span data-ttu-id="b4e86-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="b4e86-384">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-384">no</span></span>             | <span data-ttu-id="b4e86-385">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-385">no</span></span>           |
| <span data-ttu-id="b4e86-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="b4e86-386">msdyn_committype</span></span>             | <span data-ttu-id="b4e86-387">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-387">no</span></span>             | <span data-ttu-id="b4e86-388">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-388">no</span></span>           |
| <span data-ttu-id="b4e86-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="b4e86-389">msdyn_committypename</span></span>         | <span data-ttu-id="b4e86-390">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-390">no</span></span>             | <span data-ttu-id="b4e86-391">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-391">no</span></span>           |
| <span data-ttu-id="b4e86-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b4e86-392">msdyn_effort</span></span>                 | <span data-ttu-id="b4e86-393">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-393">no</span></span>             | <span data-ttu-id="b4e86-394">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-394">no</span></span>           |
| <span data-ttu-id="b4e86-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b4e86-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="b4e86-396">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-396">no</span></span>             | <span data-ttu-id="b4e86-397">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-397">no</span></span>           |
| <span data-ttu-id="b4e86-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b4e86-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="b4e86-399">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-399">no</span></span>             | <span data-ttu-id="b4e86-400">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-400">no</span></span>           |
| <span data-ttu-id="b4e86-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b4e86-401">msdyn_finish</span></span>                 | <span data-ttu-id="b4e86-402">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-402">no</span></span>             | <span data-ttu-id="b4e86-403">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-403">no</span></span>           |
| <span data-ttu-id="b4e86-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="b4e86-405">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-405">no</span></span>             | <span data-ttu-id="b4e86-406">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-406">no</span></span>           |
| <span data-ttu-id="b4e86-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="b4e86-408">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-408">no</span></span>             | <span data-ttu-id="b4e86-409">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-409">no</span></span>           |
| <span data-ttu-id="b4e86-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b4e86-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="b4e86-411">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-411">no</span></span>             | <span data-ttu-id="b4e86-412">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-412">no</span></span>           |
| <span data-ttu-id="b4e86-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="b4e86-414">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-414">no</span></span>             | <span data-ttu-id="b4e86-415">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-415">no</span></span>           |
| <span data-ttu-id="b4e86-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="b4e86-417">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-417">no</span></span>             | <span data-ttu-id="b4e86-418">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-418">no</span></span>           |
| <span data-ttu-id="b4e86-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b4e86-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="b4e86-420">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-420">no</span></span>             | <span data-ttu-id="b4e86-421">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-421">no</span></span>           |
| <span data-ttu-id="b4e86-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b4e86-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="b4e86-423">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-423">no</span></span>             | <span data-ttu-id="b4e86-424">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-424">no</span></span>           |
| <span data-ttu-id="b4e86-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="b4e86-425">msdyn_projectid</span></span>              | <span data-ttu-id="b4e86-426">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-426">yes</span></span>            | <span data-ttu-id="b4e86-427">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-427">no</span></span>           |
| <span data-ttu-id="b4e86-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-428">msdyn_projectidname</span></span>          | <span data-ttu-id="b4e86-429">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-429">no</span></span>             | <span data-ttu-id="b4e86-430">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-430">no</span></span>           |
| <span data-ttu-id="b4e86-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="b4e86-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="b4e86-432">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-432">no</span></span>             | <span data-ttu-id="b4e86-433">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-433">no</span></span>           |
| <span data-ttu-id="b4e86-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="b4e86-435">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-435">no</span></span>             | <span data-ttu-id="b4e86-436">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-436">no</span></span>           |
| <span data-ttu-id="b4e86-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b4e86-437">msdyn_start</span></span>                  | <span data-ttu-id="b4e86-438">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-438">no</span></span>             | <span data-ttu-id="b4e86-439">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-439">no</span></span>           |
| <span data-ttu-id="b4e86-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="b4e86-440">msdyn_taskid</span></span>                 | <span data-ttu-id="b4e86-441">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-441">no</span></span>             | <span data-ttu-id="b4e86-442">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-442">no</span></span>           |
| <span data-ttu-id="b4e86-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-443">msdyn_taskidname</span></span>             | <span data-ttu-id="b4e86-444">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-444">no</span></span>             | <span data-ttu-id="b4e86-445">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-445">no</span></span>           |
| <span data-ttu-id="b4e86-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="b4e86-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="b4e86-447">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-447">no</span></span>             | <span data-ttu-id="b4e86-448">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="b4e86-449">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="b4e86-449">Project team member</span></span>

| <span data-ttu-id="b4e86-450">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="b4e86-450">**Logical name**</span></span>                                 | <span data-ttu-id="b4e86-451">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="b4e86-451">**Can create**</span></span> | <span data-ttu-id="b4e86-452">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b4e86-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="b4e86-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="b4e86-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="b4e86-454">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-454">no</span></span>             | <span data-ttu-id="b4e86-455">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-455">no</span></span>           |
| <span data-ttu-id="b4e86-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="b4e86-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="b4e86-457">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-457">no</span></span>             | <span data-ttu-id="b4e86-458">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-458">no</span></span>           |
| <span data-ttu-id="b4e86-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="b4e86-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="b4e86-460">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-460">no</span></span>             | <span data-ttu-id="b4e86-461">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-461">no</span></span>           |
| <span data-ttu-id="b4e86-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="b4e86-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="b4e86-463">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-463">no</span></span>             | <span data-ttu-id="b4e86-464">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-464">no</span></span>           |
| <span data-ttu-id="b4e86-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b4e86-465">msdyn_effort</span></span>                                     | <span data-ttu-id="b4e86-466">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-466">no</span></span>             | <span data-ttu-id="b4e86-467">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-467">no</span></span>           |
| <span data-ttu-id="b4e86-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b4e86-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="b4e86-469">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-469">no</span></span>             | <span data-ttu-id="b4e86-470">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-470">no</span></span>           |
| <span data-ttu-id="b4e86-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b4e86-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="b4e86-472">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-472">no</span></span>             | <span data-ttu-id="b4e86-473">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-473">no</span></span>           |
| <span data-ttu-id="b4e86-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b4e86-474">msdyn_finish</span></span>                                     | <span data-ttu-id="b4e86-475">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-475">no</span></span>             | <span data-ttu-id="b4e86-476">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-476">no</span></span>           |
| <span data-ttu-id="b4e86-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="b4e86-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="b4e86-478">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-478">no</span></span>             | <span data-ttu-id="b4e86-479">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-479">no</span></span>           |
| <span data-ttu-id="b4e86-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="b4e86-480">msdyn_hours</span></span>                                      | <span data-ttu-id="b4e86-481">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-481">no</span></span>             | <span data-ttu-id="b4e86-482">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-482">no</span></span>           |
| <span data-ttu-id="b4e86-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="b4e86-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="b4e86-484">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-484">no</span></span>             | <span data-ttu-id="b4e86-485">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-485">no</span></span>           |
| <span data-ttu-id="b4e86-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="b4e86-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="b4e86-487">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-487">no</span></span>             | <span data-ttu-id="b4e86-488">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-488">no</span></span>           |
| <span data-ttu-id="b4e86-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="b4e86-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="b4e86-490">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-490">no</span></span>             | <span data-ttu-id="b4e86-491">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-491">no</span></span>           |
| <span data-ttu-id="b4e86-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="b4e86-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="b4e86-493">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-493">no</span></span>             | <span data-ttu-id="b4e86-494">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-494">no</span></span>           |
| <span data-ttu-id="b4e86-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="b4e86-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="b4e86-496">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-496">no</span></span>             | <span data-ttu-id="b4e86-497">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-497">no</span></span>           |
| <span data-ttu-id="b4e86-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="b4e86-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="b4e86-499">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-499">no</span></span>             | <span data-ttu-id="b4e86-500">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-500">no</span></span>           |
| <span data-ttu-id="b4e86-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="b4e86-501">msdyn_start</span></span>                                      | <span data-ttu-id="b4e86-502">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-502">no</span></span>             | <span data-ttu-id="b4e86-503">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="b4e86-504">Project</span><span class="sxs-lookup"><span data-stu-id="b4e86-504">Project</span></span>

| <span data-ttu-id="b4e86-505">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="b4e86-505">**Logical name**</span></span>                       | <span data-ttu-id="b4e86-506">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="b4e86-506">**Can create**</span></span> | <span data-ttu-id="b4e86-507">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="b4e86-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="b4e86-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="b4e86-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="b4e86-509">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-509">no</span></span>             | <span data-ttu-id="b4e86-510">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-510">no</span></span>           |
| <span data-ttu-id="b4e86-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="b4e86-512">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-512">no</span></span>             | <span data-ttu-id="b4e86-513">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-513">no</span></span>           |
| <span data-ttu-id="b4e86-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="b4e86-515">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-515">no</span></span>             | <span data-ttu-id="b4e86-516">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-516">no</span></span>           |
| <span data-ttu-id="b4e86-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="b4e86-518">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-518">no</span></span>             | <span data-ttu-id="b4e86-519">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-519">no</span></span>           |
| <span data-ttu-id="b4e86-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="b4e86-521">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-521">no</span></span>             | <span data-ttu-id="b4e86-522">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-522">no</span></span>           |
| <span data-ttu-id="b4e86-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="b4e86-524">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-524">no</span></span>             | <span data-ttu-id="b4e86-525">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-525">no</span></span>           |
| <span data-ttu-id="b4e86-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="b4e86-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="b4e86-527">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-527">yes</span></span>            | <span data-ttu-id="b4e86-528">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-528">no</span></span>           |
| <span data-ttu-id="b4e86-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="b4e86-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="b4e86-530">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-530">yes</span></span>            | <span data-ttu-id="b4e86-531">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-531">no</span></span>           |
| <span data-ttu-id="b4e86-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="b4e86-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="b4e86-533">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-533">yes</span></span>            | <span data-ttu-id="b4e86-534">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-534">no</span></span>           |
| <span data-ttu-id="b4e86-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="b4e86-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="b4e86-536">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-536">no</span></span>             | <span data-ttu-id="b4e86-537">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-537">no</span></span>           |
| <span data-ttu-id="b4e86-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="b4e86-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="b4e86-539">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-539">no</span></span>             | <span data-ttu-id="b4e86-540">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-540">no</span></span>           |
| <span data-ttu-id="b4e86-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="b4e86-542">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-542">no</span></span>             | <span data-ttu-id="b4e86-543">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-543">no</span></span>           |
| <span data-ttu-id="b4e86-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="b4e86-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="b4e86-545">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-545">no</span></span>             | <span data-ttu-id="b4e86-546">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-546">no</span></span>           |
| <span data-ttu-id="b4e86-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="b4e86-548">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-548">no</span></span>             | <span data-ttu-id="b4e86-549">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-549">no</span></span>           |
| <span data-ttu-id="b4e86-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="b4e86-550">msdyn_duration</span></span>                         | <span data-ttu-id="b4e86-551">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-551">no</span></span>             | <span data-ttu-id="b4e86-552">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-552">no</span></span>           |
| <span data-ttu-id="b4e86-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="b4e86-553">msdyn_effort</span></span>                           | <span data-ttu-id="b4e86-554">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-554">no</span></span>             | <span data-ttu-id="b4e86-555">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-555">no</span></span>           |
| <span data-ttu-id="b4e86-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="b4e86-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="b4e86-557">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-557">no</span></span>             | <span data-ttu-id="b4e86-558">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-558">no</span></span>           |
| <span data-ttu-id="b4e86-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b4e86-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="b4e86-560">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-560">no</span></span>             | <span data-ttu-id="b4e86-561">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-561">no</span></span>           |
| <span data-ttu-id="b4e86-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="b4e86-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="b4e86-563">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-563">no</span></span>             | <span data-ttu-id="b4e86-564">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-564">no</span></span>           |
| <span data-ttu-id="b4e86-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="b4e86-565">msdyn_finish</span></span>                           | <span data-ttu-id="b4e86-566">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-566">yes</span></span>            | <span data-ttu-id="b4e86-567">Ja</span><span class="sxs-lookup"><span data-stu-id="b4e86-567">yes</span></span>          |
| <span data-ttu-id="b4e86-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="b4e86-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="b4e86-569">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-569">no</span></span>             | <span data-ttu-id="b4e86-570">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-570">no</span></span>           |
| <span data-ttu-id="b4e86-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="b4e86-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="b4e86-572">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-572">no</span></span>             | <span data-ttu-id="b4e86-573">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-573">no</span></span>           |
| <span data-ttu-id="b4e86-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="b4e86-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="b4e86-575">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-575">no</span></span>             | <span data-ttu-id="b4e86-576">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-576">no</span></span>           |
| <span data-ttu-id="b4e86-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="b4e86-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="b4e86-578">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-578">no</span></span>             | <span data-ttu-id="b4e86-579">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-579">no</span></span>           |
| <span data-ttu-id="b4e86-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="b4e86-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="b4e86-581">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-581">no</span></span>             | <span data-ttu-id="b4e86-582">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-582">no</span></span>           |
| <span data-ttu-id="b4e86-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="b4e86-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="b4e86-584">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-584">no</span></span>             | <span data-ttu-id="b4e86-585">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-585">no</span></span>           |
| <span data-ttu-id="b4e86-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="b4e86-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="b4e86-587">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-587">no</span></span>             | <span data-ttu-id="b4e86-588">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-588">no</span></span>           |
| <span data-ttu-id="b4e86-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="b4e86-590">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-590">no</span></span>             | <span data-ttu-id="b4e86-591">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-591">no</span></span>           |
| <span data-ttu-id="b4e86-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="b4e86-593">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-593">no</span></span>             | <span data-ttu-id="b4e86-594">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-594">no</span></span>           |
| <span data-ttu-id="b4e86-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="b4e86-596">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-596">no</span></span>             | <span data-ttu-id="b4e86-597">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-597">no</span></span>           |
| <span data-ttu-id="b4e86-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="b4e86-599">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-599">no</span></span>             | <span data-ttu-id="b4e86-600">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-600">no</span></span>           |
| <span data-ttu-id="b4e86-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="b4e86-602">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-602">no</span></span>             | <span data-ttu-id="b4e86-603">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-603">no</span></span>           |
| <span data-ttu-id="b4e86-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="b4e86-604">msdyn_progress</span></span>                         | <span data-ttu-id="b4e86-605">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-605">no</span></span>             | <span data-ttu-id="b4e86-606">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-606">no</span></span>           |
| <span data-ttu-id="b4e86-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="b4e86-608">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-608">no</span></span>             | <span data-ttu-id="b4e86-609">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-609">no</span></span>           |
| <span data-ttu-id="b4e86-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="b4e86-611">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-611">no</span></span>             | <span data-ttu-id="b4e86-612">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-612">no</span></span>           |
| <span data-ttu-id="b4e86-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b4e86-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="b4e86-614">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-614">no</span></span>             | <span data-ttu-id="b4e86-615">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-615">no</span></span>           |
| <span data-ttu-id="b4e86-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="b4e86-617">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-617">no</span></span>             | <span data-ttu-id="b4e86-618">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-618">no</span></span>           |
| <span data-ttu-id="b4e86-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="b4e86-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="b4e86-620">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-620">no</span></span>             | <span data-ttu-id="b4e86-621">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-621">no</span></span>           |
| <span data-ttu-id="b4e86-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="b4e86-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="b4e86-623">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-623">no</span></span>             | <span data-ttu-id="b4e86-624">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-624">no</span></span>           |
| <span data-ttu-id="b4e86-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="b4e86-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="b4e86-626">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-626">no</span></span>             | <span data-ttu-id="b4e86-627">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-627">no</span></span>           |
| <span data-ttu-id="b4e86-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="b4e86-629">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-629">no</span></span>             | <span data-ttu-id="b4e86-630">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-630">no</span></span>           |
| <span data-ttu-id="b4e86-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="b4e86-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="b4e86-632">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-632">no</span></span>             | <span data-ttu-id="b4e86-633">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-633">no</span></span>           |
| <span data-ttu-id="b4e86-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="b4e86-635">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-635">no</span></span>             | <span data-ttu-id="b4e86-636">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-636">no</span></span>           |
| <span data-ttu-id="b4e86-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="b4e86-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="b4e86-638">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-638">no</span></span>             | <span data-ttu-id="b4e86-639">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-639">no</span></span>           |
| <span data-ttu-id="b4e86-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="b4e86-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="b4e86-641">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-641">no</span></span>             | <span data-ttu-id="b4e86-642">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-642">no</span></span>           |
| <span data-ttu-id="b4e86-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="b4e86-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="b4e86-644">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-644">no</span></span>             | <span data-ttu-id="b4e86-645">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-645">no</span></span>           |
| <span data-ttu-id="b4e86-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="b4e86-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="b4e86-647">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-647">no</span></span>             | <span data-ttu-id="b4e86-648">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-648">no</span></span>           |
| <span data-ttu-id="b4e86-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="b4e86-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="b4e86-650">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-650">no</span></span>             | <span data-ttu-id="b4e86-651">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-651">no</span></span>           |
| <span data-ttu-id="b4e86-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="b4e86-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="b4e86-653">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-653">no</span></span>             | <span data-ttu-id="b4e86-654">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-654">no</span></span>           |
| <span data-ttu-id="b4e86-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="b4e86-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="b4e86-656">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-656">no</span></span>             | <span data-ttu-id="b4e86-657">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-657">no</span></span>           |
| <span data-ttu-id="b4e86-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="b4e86-659">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-659">no</span></span>             | <span data-ttu-id="b4e86-660">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-660">no</span></span>           |
| <span data-ttu-id="b4e86-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="b4e86-662">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-662">no</span></span>             | <span data-ttu-id="b4e86-663">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-663">no</span></span>           |
| <span data-ttu-id="b4e86-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="b4e86-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="b4e86-665">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-665">no</span></span>             | <span data-ttu-id="b4e86-666">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-666">no</span></span>           |
| <span data-ttu-id="b4e86-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="b4e86-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="b4e86-668">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-668">no</span></span>             | <span data-ttu-id="b4e86-669">Nein</span><span class="sxs-lookup"><span data-stu-id="b4e86-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="b4e86-670">Einschränkungen und Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="b4e86-670">Limitations and known issues</span></span>
<span data-ttu-id="b4e86-671">Das Folgende ist eine Liste von Einschränkungen und bekannten Problemen:</span><span class="sxs-lookup"><span data-stu-id="b4e86-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="b4e86-672">Zeitplan-APIs können nur von **Benutzern mit Microsoft Project-Lizenz** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e86-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="b4e86-673">Sie können nicht verwendet werden von:</span><span class="sxs-lookup"><span data-stu-id="b4e86-673">They can't be used by:</span></span>
    - <span data-ttu-id="b4e86-674">Anwendungsbenutzer</span><span class="sxs-lookup"><span data-stu-id="b4e86-674">Application users</span></span>
    - <span data-ttu-id="b4e86-675">Systembenutzern</span><span class="sxs-lookup"><span data-stu-id="b4e86-675">System users</span></span>
    - <span data-ttu-id="b4e86-676">Integrationsbenutzern</span><span class="sxs-lookup"><span data-stu-id="b4e86-676">Integration users</span></span>
    - <span data-ttu-id="b4e86-677">Andere Benutzer, die nicht über die erforderliche Lizenz verfügen</span><span class="sxs-lookup"><span data-stu-id="b4e86-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="b4e86-678">Jeder **OperationSet** kann nur maximal 100 Operationen haben.</span><span class="sxs-lookup"><span data-stu-id="b4e86-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="b4e86-679">Jeder Benutzer kann nur maximal 10 offene **OperationSets** haben.</span><span class="sxs-lookup"><span data-stu-id="b4e86-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="b4e86-680">Project Operations unterstützt derzeit maximal 500 Gesamtaufgaben für ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="b4e86-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="b4e86-681">**OperationSet**-Fehlerstatus und -Fehlerprotokolle sind derzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4e86-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="b4e86-682">Grenzwerte und Beschränkungen von Projekten und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b4e86-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="b4e86-683">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="b4e86-683">Error handling</span></span>

   - <span data-ttu-id="b4e86-684">Um die aus den Operations-Sätzen generierten Fehler zu überprüfen, gehen Sie zu **Einstellungen** \> **Integration planen** \> **Operationssätze**.</span><span class="sxs-lookup"><span data-stu-id="b4e86-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="b4e86-685">Um die vom Project Scheduling Service generierten Fehler zu überprüfen, gehen Sie **Einstellungen** \> **Planen Sie die Integration** \> **PSS-Fehlerprotokolle**.</span><span class="sxs-lookup"><span data-stu-id="b4e86-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="b4e86-686">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="b4e86-686">Sample scenario</span></span>

<span data-ttu-id="b4e86-687">In diesem Szenario erstellen Sie ein Projekt, ein Teammitglied, vier Aufgaben und zwei Ressourcenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="b4e86-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="b4e86-688">Als Nächstes aktualisieren Sie eine Aufgabe, aktualisieren das Projekt, löschen eine Aufgabe, löschen eine Ressourcenzuweisung und erstellen eine Aufgabenabhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="b4e86-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="b4e86-689">Zusätzliche Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4e86-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
