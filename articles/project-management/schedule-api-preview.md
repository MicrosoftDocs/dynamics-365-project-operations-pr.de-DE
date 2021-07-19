---
title: Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung
description: Dieses Thema enthält Informationen und Beispiele für die Verwendung von Projektzeitplan-APIs.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293226"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="5e4b2-103">Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="5e4b2-104">_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="5e4b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5e4b2-105">Einige oder alle der in diesem Thema genannten Funktionen stehen im Rahmen einer Vorschauversion zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="5e4b2-106">Inhalt und Funktionalität können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="5e4b2-107">Planungsentitäten</span><span class="sxs-lookup"><span data-stu-id="5e4b2-107">Scheduling entities</span></span>

<span data-ttu-id="5e4b2-108">Projektzeitplan-APIs bieten die Möglichkeit, Vorgänge zum Erstellen, Aktualisieren und Löschen mit **Terminplan-Entitäten** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="5e4b2-109">Diese Entitäten werden über das Planungsmodul in Project für das Web verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="5e4b2-110">Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten** wurden in früheren Version von Dynamics 365 Project Operations eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="5e4b2-111">Die folgende Tabelle enthält eine vollständige Liste der Projektzeitplan-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="5e4b2-112">Entitätsname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-112">Entity name</span></span>  | <span data-ttu-id="5e4b2-113">Logischer Entitätsname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="5e4b2-114">Project</span><span class="sxs-lookup"><span data-stu-id="5e4b2-114">Project</span></span> | <span data-ttu-id="5e4b2-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5e4b2-115">msdyn_project</span></span> |
| <span data-ttu-id="5e4b2-116">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="5e4b2-116">Project Task</span></span>  | <span data-ttu-id="5e4b2-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="5e4b2-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="5e4b2-118">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="5e4b2-118">Project Task Dependency</span></span>  | <span data-ttu-id="5e4b2-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="5e4b2-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="5e4b2-120">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-120">Resource Assignment</span></span> | <span data-ttu-id="5e4b2-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="5e4b2-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="5e4b2-122">Projekt-Bucket</span><span class="sxs-lookup"><span data-stu-id="5e4b2-122">Project Bucket</span></span>  | <span data-ttu-id="5e4b2-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="5e4b2-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="5e4b2-124">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="5e4b2-124">Project Team Member</span></span> | <span data-ttu-id="5e4b2-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="5e4b2-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="5e4b2-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="5e4b2-126">OperationSet</span></span>

<span data-ttu-id="5e4b2-127">OperationSet ist ein Arbeitseinheitsmuster, das verwendet werden kann, wenn innerhalb einer Transaktion mehrere zeitplanbezogene Anforderungen verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="5e4b2-128">Projektzeitplan-APIs</span><span class="sxs-lookup"><span data-stu-id="5e4b2-128">Project schedule APIs</span></span>

<span data-ttu-id="5e4b2-129">Im Folgenden finden Sie eine Liste der aktuellen Projektzeitplan-APIs.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="5e4b2-130">**msdyn_CreateProjectV1**: Mit dieser API kann ein Projekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="5e4b2-131">Der Projekt- und Standardprojekt-Bucket wird sofort erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="5e4b2-132">**msdyn_CreateTeamMemberV1**: Mit dieser API kann ein Projektteammitglied erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="5e4b2-133">Der Teammitgliedsdatensatz wird sofort erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="5e4b2-134">**msdyn_CreateOperationSetV1**: Mit dieser API können mehrere Anforderungen geplant werden, die innerhalb einer Transaktion ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="5e4b2-135">**msdyn_PSSCreateV1**: Mit dieser API kann eine Entität erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="5e4b2-136">Die Entität kann eine der Projektplanungs-Entitäten sein, die den Vorgang des Erstellens unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="5e4b2-137">**msdyn_PSSUpdateV1**: Mit dieser API kann eine Entität aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="5e4b2-138">Die Entität kann eine beliebige Projektplanungs-Entität sein, die den Vorgang „Aktualisieren“ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="5e4b2-139">**msdyn_PSSDeleteV1**: Mit dieser API kann eine Entität gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="5e4b2-140">Die Entität kann eine beliebige Projektplanungs-Entität sein, die den Vorgang „Löschen“ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="5e4b2-141">**msdyn_ExecuteOperationSetV1**: Diese API wird verwendet, um alle Operationen innerhalb des angegebenen Operationssatzes auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="5e4b2-142">Verwenden von Projektzeitplan-APIs mit OperationSet</span><span class="sxs-lookup"><span data-stu-id="5e4b2-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="5e4b2-143">Weil Aufzeichnungen sowohl mit **CreateProjectV1** als auch **CreateTeamMemberV1** sofort erstellt werden, können diese APIs nicht direkt im **OperationSet** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="5e4b2-144">Sie können jedoch die API verwenden, um die erforderlichen Datensätze zu erstellen, ein **OperationSet** zu erstellen und dann diese vorab erstellten Datensätze im **OperationSet** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="5e4b2-145">Unterstützte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5e4b2-145">Supported operations</span></span>

| <span data-ttu-id="5e4b2-146">Planungsentität</span><span class="sxs-lookup"><span data-stu-id="5e4b2-146">Scheduling entity</span></span> | <span data-ttu-id="5e4b2-147">Erstellen</span><span class="sxs-lookup"><span data-stu-id="5e4b2-147">Create</span></span> | <span data-ttu-id="5e4b2-148">Update</span><span class="sxs-lookup"><span data-stu-id="5e4b2-148">Update</span></span> | <span data-ttu-id="5e4b2-149">Entf</span><span class="sxs-lookup"><span data-stu-id="5e4b2-149">Delete</span></span> | <span data-ttu-id="5e4b2-150">Wichtige Überlegungen</span><span class="sxs-lookup"><span data-stu-id="5e4b2-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="5e4b2-151">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="5e4b2-151">Project task</span></span> | <span data-ttu-id="5e4b2-152">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-152">Yes</span></span> | <span data-ttu-id="5e4b2-153">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-153">Yes</span></span> | <span data-ttu-id="5e4b2-154">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-154">Yes</span></span> | <span data-ttu-id="5e4b2-155">Kein Wert</span><span class="sxs-lookup"><span data-stu-id="5e4b2-155">None</span></span> |
| <span data-ttu-id="5e4b2-156">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="5e4b2-156">Project task dependency</span></span> | <span data-ttu-id="5e4b2-157">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-157">Yes</span></span> | <span data-ttu-id="5e4b2-158">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-158">Yes</span></span> | | <span data-ttu-id="5e4b2-159">Abhängigkeitsdatensätze für Projektaufgaben werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="5e4b2-160">Stattdessen kann ein alter Datensatz gelöscht und ein neuer Datensatz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5e4b2-161">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-161">Resource assignment</span></span> | <span data-ttu-id="5e4b2-162">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-162">Yes</span></span> | <span data-ttu-id="5e4b2-163">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-163">Yes</span></span> | | <span data-ttu-id="5e4b2-164">Vorgänge mit den folgenden Feldern werden nicht unterstützt: **BookableResourceID**, **Aufwand**, **EffortCompleted**, **EffortRemaining** und **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="5e4b2-165">Ressourcenzuweisungsdatensätze werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="5e4b2-166">Stattdessen kann der alte Datensatz gelöscht und ein neuer Datensatz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="5e4b2-167">Projekt-Bucket</span><span class="sxs-lookup"><span data-stu-id="5e4b2-167">Project bucket</span></span> | <span data-ttu-id="5e4b2-168">N/V</span><span class="sxs-lookup"><span data-stu-id="5e4b2-168">N/A</span></span> | <span data-ttu-id="5e4b2-169">N/V</span><span class="sxs-lookup"><span data-stu-id="5e4b2-169">N/A</span></span> | <span data-ttu-id="5e4b2-170">N/V</span><span class="sxs-lookup"><span data-stu-id="5e4b2-170">N/A</span></span> | <span data-ttu-id="5e4b2-171">Der Standard-Bucket wird mit der **CreateProjectV1**-API erstellt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="5e4b2-172">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="5e4b2-172">Project team member</span></span> | <span data-ttu-id="5e4b2-173">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-173">Yes</span></span> | <span data-ttu-id="5e4b2-174">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-174">Yes</span></span> | <span data-ttu-id="5e4b2-175">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-175">Yes</span></span> | <span data-ttu-id="5e4b2-176">Verwenden Sie für den Erstellungsvorgang die **CreateTeamMemberV1**-API.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="5e4b2-177">Project</span><span class="sxs-lookup"><span data-stu-id="5e4b2-177">Project</span></span> | <span data-ttu-id="5e4b2-178">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-178">Yes</span></span> | <span data-ttu-id="5e4b2-179">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-179">Yes</span></span> | <span data-ttu-id="5e4b2-180">N/V</span><span class="sxs-lookup"><span data-stu-id="5e4b2-180">N/A</span></span> | <span data-ttu-id="5e4b2-181">Vorgänge mit den folgenden Feldern werden nicht unterstützt: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Aufwand**, **EffortCompleted**, **EffortRemaining**, **Fortschritt**, **Fertigstellen**, **TaskEarliestStart** und **Dauer**.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="5e4b2-182">Diese APIs können mit Entitätsobjekten aufgerufen werden, die benutzerdefinierte Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="5e4b2-183">Diese ID-Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-183">The ID property is optional.</span></span> <span data-ttu-id="5e4b2-184">Wenn sie bereitgestellt wird, versucht das System, sie zu verwenden, und löst eine Ausnahme aus, wenn sie nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="5e4b2-185">Wenn sie nicht bereitgestellt wird, generiert das System sie.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="5e4b2-186">Eingeschränkte Felder</span><span class="sxs-lookup"><span data-stu-id="5e4b2-186">Restricted fields</span></span>

<span data-ttu-id="5e4b2-187">In den folgenden Tabellen werden die Felder definiert, für die **Erstellen** und **Bearbeiten** eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="5e4b2-188">Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="5e4b2-188">Project task</span></span>

| <span data-ttu-id="5e4b2-189">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-189">**Logical name**</span></span>                       | <span data-ttu-id="5e4b2-190">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-190">**Can create**</span></span> | <span data-ttu-id="5e4b2-191">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="5e4b2-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="5e4b2-193">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-193">no</span></span>             | <span data-ttu-id="5e4b2-194">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-194">no</span></span>               |
| <span data-ttu-id="5e4b2-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="5e4b2-196">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-196">no</span></span>             | <span data-ttu-id="5e4b2-197">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-197">no</span></span>               |
| <span data-ttu-id="5e4b2-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="5e4b2-198">msdyn_actualend</span></span>                        | <span data-ttu-id="5e4b2-199">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-199">no</span></span>             | <span data-ttu-id="5e4b2-200">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-200">no</span></span>               |
| <span data-ttu-id="5e4b2-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="5e4b2-202">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-202">no</span></span>             | <span data-ttu-id="5e4b2-203">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-203">no</span></span>               |
| <span data-ttu-id="5e4b2-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5e4b2-205">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-205">no</span></span>             | <span data-ttu-id="5e4b2-206">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-206">no</span></span>               |
| <span data-ttu-id="5e4b2-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="5e4b2-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="5e4b2-208">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-208">no</span></span>             | <span data-ttu-id="5e4b2-209">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-209">no</span></span>               |
| <span data-ttu-id="5e4b2-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="5e4b2-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="5e4b2-211">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-211">no</span></span>             | <span data-ttu-id="5e4b2-212">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-212">no</span></span>               |
| <span data-ttu-id="5e4b2-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="5e4b2-214">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-214">no</span></span>             | <span data-ttu-id="5e4b2-215">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-215">no</span></span>               |
| <span data-ttu-id="5e4b2-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5e4b2-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="5e4b2-217">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-217">no</span></span>             | <span data-ttu-id="5e4b2-218">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-218">no</span></span>               |
| <span data-ttu-id="5e4b2-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e4b2-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5e4b2-220">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-220">no</span></span>             | <span data-ttu-id="5e4b2-221">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-221">no</span></span>               |
| <span data-ttu-id="5e4b2-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e4b2-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="5e4b2-223">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-223">no</span></span>             | <span data-ttu-id="5e4b2-224">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-224">no</span></span>               |
| <span data-ttu-id="5e4b2-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="5e4b2-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="5e4b2-226">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-226">no</span></span>             | <span data-ttu-id="5e4b2-227">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-227">no</span></span>               |
| <span data-ttu-id="5e4b2-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="5e4b2-229">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-229">no</span></span>             | <span data-ttu-id="5e4b2-230">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-230">no</span></span>               |
| <span data-ttu-id="5e4b2-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="5e4b2-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="5e4b2-232">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-232">no</span></span>             | <span data-ttu-id="5e4b2-233">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-233">no</span></span>               |
| <span data-ttu-id="5e4b2-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="5e4b2-235">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-235">no</span></span>             | <span data-ttu-id="5e4b2-236">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-236">no</span></span>               |
| <span data-ttu-id="5e4b2-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="5e4b2-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="5e4b2-238">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-238">no</span></span>             | <span data-ttu-id="5e4b2-239">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-239">no</span></span>               |
| <span data-ttu-id="5e4b2-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="5e4b2-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="5e4b2-241">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-241">no</span></span>             | <span data-ttu-id="5e4b2-242">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-242">no</span></span>               |
| <span data-ttu-id="5e4b2-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="5e4b2-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="5e4b2-244">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-244">no</span></span>             | <span data-ttu-id="5e4b2-245">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-245">no</span></span>               |
| <span data-ttu-id="5e4b2-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="5e4b2-247">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-247">no</span></span>             | <span data-ttu-id="5e4b2-248">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-248">no</span></span>               |
| <span data-ttu-id="5e4b2-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="5e4b2-250">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-250">no</span></span>             | <span data-ttu-id="5e4b2-251">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-251">no</span></span>               |
| <span data-ttu-id="5e4b2-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="5e4b2-253">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-253">no</span></span>             | <span data-ttu-id="5e4b2-254">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-254">no</span></span>               |
| <span data-ttu-id="5e4b2-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="5e4b2-256">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-256">no</span></span>             | <span data-ttu-id="5e4b2-257">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-257">no</span></span>               |
| <span data-ttu-id="5e4b2-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5e4b2-259">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-259">no</span></span>             | <span data-ttu-id="5e4b2-260">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-260">no</span></span>               |
| <span data-ttu-id="5e4b2-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5e4b2-262">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-262">no</span></span>             | <span data-ttu-id="5e4b2-263">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-263">no</span></span>               |
| <span data-ttu-id="5e4b2-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="5e4b2-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="5e4b2-265">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-265">no</span></span>             | <span data-ttu-id="5e4b2-266">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-266">no</span></span>               |
| <span data-ttu-id="5e4b2-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5e4b2-267">msdyn_progress</span></span>                         | <span data-ttu-id="5e4b2-268">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-268">no</span></span>             | <span data-ttu-id="5e4b2-269">nein (ja für P4W)</span><span class="sxs-lookup"><span data-stu-id="5e4b2-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="5e4b2-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5e4b2-271">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-271">no</span></span>             | <span data-ttu-id="5e4b2-272">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-272">no</span></span>               |
| <span data-ttu-id="5e4b2-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5e4b2-274">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-274">no</span></span>             | <span data-ttu-id="5e4b2-275">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-275">no</span></span>               |
| <span data-ttu-id="5e4b2-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5e4b2-277">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-277">no</span></span>             | <span data-ttu-id="5e4b2-278">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-278">no</span></span>               |
| <span data-ttu-id="5e4b2-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5e4b2-280">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-280">no</span></span>             | <span data-ttu-id="5e4b2-281">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-281">no</span></span>               |
| <span data-ttu-id="5e4b2-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="5e4b2-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="5e4b2-283">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-283">no</span></span>             | <span data-ttu-id="5e4b2-284">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-284">no</span></span>               |
| <span data-ttu-id="5e4b2-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="5e4b2-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="5e4b2-286">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-286">no</span></span>             | <span data-ttu-id="5e4b2-287">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-287">no</span></span>               |
| <span data-ttu-id="5e4b2-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="5e4b2-289">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-289">no</span></span>             | <span data-ttu-id="5e4b2-290">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-290">no</span></span>               |
| <span data-ttu-id="5e4b2-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="5e4b2-292">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-292">no</span></span>             | <span data-ttu-id="5e4b2-293">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-293">no</span></span>               |
| <span data-ttu-id="5e4b2-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="5e4b2-295">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-295">no</span></span>             | <span data-ttu-id="5e4b2-296">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-296">no</span></span>               |
| <span data-ttu-id="5e4b2-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="5e4b2-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="5e4b2-298">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-298">no</span></span>             | <span data-ttu-id="5e4b2-299">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-299">no</span></span>               |
| <span data-ttu-id="5e4b2-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e4b2-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="5e4b2-301">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-301">no</span></span>             | <span data-ttu-id="5e4b2-302">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-302">no</span></span>               |
| <span data-ttu-id="5e4b2-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="5e4b2-304">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-304">no</span></span>             | <span data-ttu-id="5e4b2-305">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-305">no</span></span>               |
| <span data-ttu-id="5e4b2-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5e4b2-307">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-307">no</span></span>             | <span data-ttu-id="5e4b2-308">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-308">no</span></span>               |
| <span data-ttu-id="5e4b2-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5e4b2-310">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-310">no</span></span>             | <span data-ttu-id="5e4b2-311">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-311">no</span></span>               |
| <span data-ttu-id="5e4b2-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="5e4b2-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="5e4b2-313">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-313">no</span></span>             | <span data-ttu-id="5e4b2-314">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-314">no</span></span>               |
| <span data-ttu-id="5e4b2-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="5e4b2-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="5e4b2-316">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-316">no</span></span>             | <span data-ttu-id="5e4b2-317">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-317">no</span></span>               |
| <span data-ttu-id="5e4b2-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="5e4b2-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="5e4b2-319">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-319">no</span></span>             | <span data-ttu-id="5e4b2-320">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-320">no</span></span>               |
| <span data-ttu-id="5e4b2-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5e4b2-322">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-322">no</span></span>             | <span data-ttu-id="5e4b2-323">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-323">no</span></span>               |
| <span data-ttu-id="5e4b2-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="5e4b2-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="5e4b2-325">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-325">no</span></span>             | <span data-ttu-id="5e4b2-326">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-326">no</span></span>               |
| <span data-ttu-id="5e4b2-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="5e4b2-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="5e4b2-328">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-328">no</span></span>             | <span data-ttu-id="5e4b2-329">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-329">no</span></span>               |
| <span data-ttu-id="5e4b2-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="5e4b2-330">msdyn_summary</span></span>                          | <span data-ttu-id="5e4b2-331">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-331">no</span></span>             | <span data-ttu-id="5e4b2-332">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-332">no</span></span>               |
| <span data-ttu-id="5e4b2-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="5e4b2-334">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-334">no</span></span>             | <span data-ttu-id="5e4b2-335">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-335">no</span></span>               |
| <span data-ttu-id="5e4b2-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="5e4b2-337">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-337">no</span></span>             | <span data-ttu-id="5e4b2-338">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="5e4b2-339">Abhängigkeit der Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="5e4b2-339">Project task dependency</span></span>

| <span data-ttu-id="5e4b2-340">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-340">**Logical name**</span></span>              | <span data-ttu-id="5e4b2-341">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-341">**Can create**</span></span> | <span data-ttu-id="5e4b2-342">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="5e4b2-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="5e4b2-343">msdyn_linktype</span></span>                | <span data-ttu-id="5e4b2-344">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-344">no</span></span>             | <span data-ttu-id="5e4b2-345">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-345">no</span></span>           |
| <span data-ttu-id="5e4b2-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="5e4b2-346">msdyn_linktypename</span></span>            | <span data-ttu-id="5e4b2-347">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-347">no</span></span>             | <span data-ttu-id="5e4b2-348">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-348">no</span></span>           |
| <span data-ttu-id="5e4b2-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="5e4b2-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="5e4b2-350">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-350">yes</span></span>            | <span data-ttu-id="5e4b2-351">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-351">no</span></span>           |
| <span data-ttu-id="5e4b2-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="5e4b2-353">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-353">yes</span></span>            | <span data-ttu-id="5e4b2-354">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-354">no</span></span>           |
| <span data-ttu-id="5e4b2-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="5e4b2-355">msdyn_project</span></span>                 | <span data-ttu-id="5e4b2-356">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-356">yes</span></span>            | <span data-ttu-id="5e4b2-357">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-357">no</span></span>           |
| <span data-ttu-id="5e4b2-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-358">msdyn_projectname</span></span>             | <span data-ttu-id="5e4b2-359">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-359">yes</span></span>            | <span data-ttu-id="5e4b2-360">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-360">no</span></span>           |
| <span data-ttu-id="5e4b2-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="5e4b2-362">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-362">yes</span></span>            | <span data-ttu-id="5e4b2-363">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-363">no</span></span>           |
| <span data-ttu-id="5e4b2-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="5e4b2-364">msdyn_successortask</span></span>           | <span data-ttu-id="5e4b2-365">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-365">yes</span></span>            | <span data-ttu-id="5e4b2-366">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-366">no</span></span>           |
| <span data-ttu-id="5e4b2-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="5e4b2-368">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-368">yes</span></span>            | <span data-ttu-id="5e4b2-369">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="5e4b2-370">Ressourcenzuweisung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-370">Resource assignment</span></span>

| <span data-ttu-id="5e4b2-371">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-371">**Logical name**</span></span>             | <span data-ttu-id="5e4b2-372">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-372">**Can create**</span></span> | <span data-ttu-id="5e4b2-373">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="5e4b2-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="5e4b2-375">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-375">yes</span></span>            | <span data-ttu-id="5e4b2-376">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-376">no</span></span>           |
| <span data-ttu-id="5e4b2-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="5e4b2-378">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-378">yes</span></span>            | <span data-ttu-id="5e4b2-379">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-379">no</span></span>           |
| <span data-ttu-id="5e4b2-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="5e4b2-381">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-381">no</span></span>             | <span data-ttu-id="5e4b2-382">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-382">no</span></span>           |
| <span data-ttu-id="5e4b2-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="5e4b2-384">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-384">no</span></span>             | <span data-ttu-id="5e4b2-385">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-385">no</span></span>           |
| <span data-ttu-id="5e4b2-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="5e4b2-386">msdyn_committype</span></span>             | <span data-ttu-id="5e4b2-387">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-387">no</span></span>             | <span data-ttu-id="5e4b2-388">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-388">no</span></span>           |
| <span data-ttu-id="5e4b2-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="5e4b2-389">msdyn_committypename</span></span>         | <span data-ttu-id="5e4b2-390">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-390">no</span></span>             | <span data-ttu-id="5e4b2-391">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-391">no</span></span>           |
| <span data-ttu-id="5e4b2-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e4b2-392">msdyn_effort</span></span>                 | <span data-ttu-id="5e4b2-393">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-393">no</span></span>             | <span data-ttu-id="5e4b2-394">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-394">no</span></span>           |
| <span data-ttu-id="5e4b2-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e4b2-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="5e4b2-396">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-396">no</span></span>             | <span data-ttu-id="5e4b2-397">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-397">no</span></span>           |
| <span data-ttu-id="5e4b2-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e4b2-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="5e4b2-399">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-399">no</span></span>             | <span data-ttu-id="5e4b2-400">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-400">no</span></span>           |
| <span data-ttu-id="5e4b2-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e4b2-401">msdyn_finish</span></span>                 | <span data-ttu-id="5e4b2-402">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-402">no</span></span>             | <span data-ttu-id="5e4b2-403">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-403">no</span></span>           |
| <span data-ttu-id="5e4b2-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="5e4b2-405">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-405">no</span></span>             | <span data-ttu-id="5e4b2-406">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-406">no</span></span>           |
| <span data-ttu-id="5e4b2-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="5e4b2-408">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-408">no</span></span>             | <span data-ttu-id="5e4b2-409">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-409">no</span></span>           |
| <span data-ttu-id="5e4b2-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="5e4b2-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="5e4b2-411">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-411">no</span></span>             | <span data-ttu-id="5e4b2-412">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-412">no</span></span>           |
| <span data-ttu-id="5e4b2-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="5e4b2-414">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-414">no</span></span>             | <span data-ttu-id="5e4b2-415">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-415">no</span></span>           |
| <span data-ttu-id="5e4b2-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="5e4b2-417">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-417">no</span></span>             | <span data-ttu-id="5e4b2-418">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-418">no</span></span>           |
| <span data-ttu-id="5e4b2-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="5e4b2-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="5e4b2-420">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-420">no</span></span>             | <span data-ttu-id="5e4b2-421">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-421">no</span></span>           |
| <span data-ttu-id="5e4b2-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="5e4b2-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="5e4b2-423">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-423">no</span></span>             | <span data-ttu-id="5e4b2-424">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-424">no</span></span>           |
| <span data-ttu-id="5e4b2-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-425">msdyn_projectid</span></span>              | <span data-ttu-id="5e4b2-426">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-426">yes</span></span>            | <span data-ttu-id="5e4b2-427">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-427">no</span></span>           |
| <span data-ttu-id="5e4b2-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-428">msdyn_projectidname</span></span>          | <span data-ttu-id="5e4b2-429">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-429">no</span></span>             | <span data-ttu-id="5e4b2-430">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-430">no</span></span>           |
| <span data-ttu-id="5e4b2-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="5e4b2-432">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-432">no</span></span>             | <span data-ttu-id="5e4b2-433">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-433">no</span></span>           |
| <span data-ttu-id="5e4b2-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="5e4b2-435">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-435">no</span></span>             | <span data-ttu-id="5e4b2-436">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-436">no</span></span>           |
| <span data-ttu-id="5e4b2-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5e4b2-437">msdyn_start</span></span>                  | <span data-ttu-id="5e4b2-438">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-438">no</span></span>             | <span data-ttu-id="5e4b2-439">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-439">no</span></span>           |
| <span data-ttu-id="5e4b2-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-440">msdyn_taskid</span></span>                 | <span data-ttu-id="5e4b2-441">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-441">no</span></span>             | <span data-ttu-id="5e4b2-442">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-442">no</span></span>           |
| <span data-ttu-id="5e4b2-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-443">msdyn_taskidname</span></span>             | <span data-ttu-id="5e4b2-444">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-444">no</span></span>             | <span data-ttu-id="5e4b2-445">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-445">no</span></span>           |
| <span data-ttu-id="5e4b2-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="5e4b2-447">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-447">no</span></span>             | <span data-ttu-id="5e4b2-448">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="5e4b2-449">Projektteammitglied</span><span class="sxs-lookup"><span data-stu-id="5e4b2-449">Project team member</span></span>

| <span data-ttu-id="5e4b2-450">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-450">**Logical name**</span></span>                                 | <span data-ttu-id="5e4b2-451">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-451">**Can create**</span></span> | <span data-ttu-id="5e4b2-452">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="5e4b2-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="5e4b2-454">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-454">no</span></span>             | <span data-ttu-id="5e4b2-455">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-455">no</span></span>           |
| <span data-ttu-id="5e4b2-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="5e4b2-457">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-457">no</span></span>             | <span data-ttu-id="5e4b2-458">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-458">no</span></span>           |
| <span data-ttu-id="5e4b2-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="5e4b2-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="5e4b2-460">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-460">no</span></span>             | <span data-ttu-id="5e4b2-461">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-461">no</span></span>           |
| <span data-ttu-id="5e4b2-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="5e4b2-463">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-463">no</span></span>             | <span data-ttu-id="5e4b2-464">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-464">no</span></span>           |
| <span data-ttu-id="5e4b2-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e4b2-465">msdyn_effort</span></span>                                     | <span data-ttu-id="5e4b2-466">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-466">no</span></span>             | <span data-ttu-id="5e4b2-467">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-467">no</span></span>           |
| <span data-ttu-id="5e4b2-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e4b2-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="5e4b2-469">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-469">no</span></span>             | <span data-ttu-id="5e4b2-470">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-470">no</span></span>           |
| <span data-ttu-id="5e4b2-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e4b2-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="5e4b2-472">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-472">no</span></span>             | <span data-ttu-id="5e4b2-473">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-473">no</span></span>           |
| <span data-ttu-id="5e4b2-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e4b2-474">msdyn_finish</span></span>                                     | <span data-ttu-id="5e4b2-475">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-475">no</span></span>             | <span data-ttu-id="5e4b2-476">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-476">no</span></span>           |
| <span data-ttu-id="5e4b2-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="5e4b2-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="5e4b2-478">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-478">no</span></span>             | <span data-ttu-id="5e4b2-479">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-479">no</span></span>           |
| <span data-ttu-id="5e4b2-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="5e4b2-480">msdyn_hours</span></span>                                      | <span data-ttu-id="5e4b2-481">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-481">no</span></span>             | <span data-ttu-id="5e4b2-482">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-482">no</span></span>           |
| <span data-ttu-id="5e4b2-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="5e4b2-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="5e4b2-484">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-484">no</span></span>             | <span data-ttu-id="5e4b2-485">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-485">no</span></span>           |
| <span data-ttu-id="5e4b2-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="5e4b2-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="5e4b2-487">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-487">no</span></span>             | <span data-ttu-id="5e4b2-488">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-488">no</span></span>           |
| <span data-ttu-id="5e4b2-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="5e4b2-490">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-490">no</span></span>             | <span data-ttu-id="5e4b2-491">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-491">no</span></span>           |
| <span data-ttu-id="5e4b2-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="5e4b2-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="5e4b2-493">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-493">no</span></span>             | <span data-ttu-id="5e4b2-494">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-494">no</span></span>           |
| <span data-ttu-id="5e4b2-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="5e4b2-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="5e4b2-496">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-496">no</span></span>             | <span data-ttu-id="5e4b2-497">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-497">no</span></span>           |
| <span data-ttu-id="5e4b2-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="5e4b2-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="5e4b2-499">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-499">no</span></span>             | <span data-ttu-id="5e4b2-500">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-500">no</span></span>           |
| <span data-ttu-id="5e4b2-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="5e4b2-501">msdyn_start</span></span>                                      | <span data-ttu-id="5e4b2-502">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-502">no</span></span>             | <span data-ttu-id="5e4b2-503">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="5e4b2-504">Project</span><span class="sxs-lookup"><span data-stu-id="5e4b2-504">Project</span></span>

| <span data-ttu-id="5e4b2-505">**Logischer Name**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-505">**Logical name**</span></span>                       | <span data-ttu-id="5e4b2-506">**Kann erstellen**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-506">**Can create**</span></span> | <span data-ttu-id="5e4b2-507">**Kann bearbeiten**:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="5e4b2-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="5e4b2-509">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-509">no</span></span>             | <span data-ttu-id="5e4b2-510">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-510">no</span></span>           |
| <span data-ttu-id="5e4b2-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="5e4b2-512">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-512">no</span></span>             | <span data-ttu-id="5e4b2-513">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-513">no</span></span>           |
| <span data-ttu-id="5e4b2-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="5e4b2-515">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-515">no</span></span>             | <span data-ttu-id="5e4b2-516">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-516">no</span></span>           |
| <span data-ttu-id="5e4b2-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="5e4b2-518">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-518">no</span></span>             | <span data-ttu-id="5e4b2-519">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-519">no</span></span>           |
| <span data-ttu-id="5e4b2-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="5e4b2-521">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-521">no</span></span>             | <span data-ttu-id="5e4b2-522">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-522">no</span></span>           |
| <span data-ttu-id="5e4b2-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="5e4b2-524">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-524">no</span></span>             | <span data-ttu-id="5e4b2-525">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-525">no</span></span>           |
| <span data-ttu-id="5e4b2-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="5e4b2-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="5e4b2-527">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-527">yes</span></span>            | <span data-ttu-id="5e4b2-528">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-528">no</span></span>           |
| <span data-ttu-id="5e4b2-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="5e4b2-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="5e4b2-530">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-530">yes</span></span>            | <span data-ttu-id="5e4b2-531">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-531">no</span></span>           |
| <span data-ttu-id="5e4b2-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="5e4b2-533">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-533">yes</span></span>            | <span data-ttu-id="5e4b2-534">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-534">no</span></span>           |
| <span data-ttu-id="5e4b2-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="5e4b2-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="5e4b2-536">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-536">no</span></span>             | <span data-ttu-id="5e4b2-537">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-537">no</span></span>           |
| <span data-ttu-id="5e4b2-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="5e4b2-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="5e4b2-539">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-539">no</span></span>             | <span data-ttu-id="5e4b2-540">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-540">no</span></span>           |
| <span data-ttu-id="5e4b2-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="5e4b2-542">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-542">no</span></span>             | <span data-ttu-id="5e4b2-543">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-543">no</span></span>           |
| <span data-ttu-id="5e4b2-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="5e4b2-545">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-545">no</span></span>             | <span data-ttu-id="5e4b2-546">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-546">no</span></span>           |
| <span data-ttu-id="5e4b2-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="5e4b2-548">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-548">no</span></span>             | <span data-ttu-id="5e4b2-549">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-549">no</span></span>           |
| <span data-ttu-id="5e4b2-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="5e4b2-550">msdyn_duration</span></span>                         | <span data-ttu-id="5e4b2-551">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-551">no</span></span>             | <span data-ttu-id="5e4b2-552">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-552">no</span></span>           |
| <span data-ttu-id="5e4b2-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="5e4b2-553">msdyn_effort</span></span>                           | <span data-ttu-id="5e4b2-554">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-554">no</span></span>             | <span data-ttu-id="5e4b2-555">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-555">no</span></span>           |
| <span data-ttu-id="5e4b2-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="5e4b2-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="5e4b2-557">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-557">no</span></span>             | <span data-ttu-id="5e4b2-558">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-558">no</span></span>           |
| <span data-ttu-id="5e4b2-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5e4b2-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="5e4b2-560">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-560">no</span></span>             | <span data-ttu-id="5e4b2-561">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-561">no</span></span>           |
| <span data-ttu-id="5e4b2-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="5e4b2-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="5e4b2-563">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-563">no</span></span>             | <span data-ttu-id="5e4b2-564">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-564">no</span></span>           |
| <span data-ttu-id="5e4b2-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="5e4b2-565">msdyn_finish</span></span>                           | <span data-ttu-id="5e4b2-566">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-566">yes</span></span>            | <span data-ttu-id="5e4b2-567">Ja</span><span class="sxs-lookup"><span data-stu-id="5e4b2-567">yes</span></span>          |
| <span data-ttu-id="5e4b2-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="5e4b2-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="5e4b2-569">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-569">no</span></span>             | <span data-ttu-id="5e4b2-570">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-570">no</span></span>           |
| <span data-ttu-id="5e4b2-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="5e4b2-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="5e4b2-572">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-572">no</span></span>             | <span data-ttu-id="5e4b2-573">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-573">no</span></span>           |
| <span data-ttu-id="5e4b2-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="5e4b2-575">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-575">no</span></span>             | <span data-ttu-id="5e4b2-576">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-576">no</span></span>           |
| <span data-ttu-id="5e4b2-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="5e4b2-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="5e4b2-578">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-578">no</span></span>             | <span data-ttu-id="5e4b2-579">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-579">no</span></span>           |
| <span data-ttu-id="5e4b2-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="5e4b2-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="5e4b2-581">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-581">no</span></span>             | <span data-ttu-id="5e4b2-582">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-582">no</span></span>           |
| <span data-ttu-id="5e4b2-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="5e4b2-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="5e4b2-584">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-584">no</span></span>             | <span data-ttu-id="5e4b2-585">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-585">no</span></span>           |
| <span data-ttu-id="5e4b2-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="5e4b2-587">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-587">no</span></span>             | <span data-ttu-id="5e4b2-588">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-588">no</span></span>           |
| <span data-ttu-id="5e4b2-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="5e4b2-590">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-590">no</span></span>             | <span data-ttu-id="5e4b2-591">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-591">no</span></span>           |
| <span data-ttu-id="5e4b2-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="5e4b2-593">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-593">no</span></span>             | <span data-ttu-id="5e4b2-594">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-594">no</span></span>           |
| <span data-ttu-id="5e4b2-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="5e4b2-596">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-596">no</span></span>             | <span data-ttu-id="5e4b2-597">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-597">no</span></span>           |
| <span data-ttu-id="5e4b2-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="5e4b2-599">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-599">no</span></span>             | <span data-ttu-id="5e4b2-600">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-600">no</span></span>           |
| <span data-ttu-id="5e4b2-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="5e4b2-602">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-602">no</span></span>             | <span data-ttu-id="5e4b2-603">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-603">no</span></span>           |
| <span data-ttu-id="5e4b2-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="5e4b2-604">msdyn_progress</span></span>                         | <span data-ttu-id="5e4b2-605">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-605">no</span></span>             | <span data-ttu-id="5e4b2-606">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-606">no</span></span>           |
| <span data-ttu-id="5e4b2-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="5e4b2-608">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-608">no</span></span>             | <span data-ttu-id="5e4b2-609">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-609">no</span></span>           |
| <span data-ttu-id="5e4b2-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="5e4b2-611">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-611">no</span></span>             | <span data-ttu-id="5e4b2-612">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-612">no</span></span>           |
| <span data-ttu-id="5e4b2-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="5e4b2-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="5e4b2-614">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-614">no</span></span>             | <span data-ttu-id="5e4b2-615">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-615">no</span></span>           |
| <span data-ttu-id="5e4b2-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="5e4b2-617">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-617">no</span></span>             | <span data-ttu-id="5e4b2-618">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-618">no</span></span>           |
| <span data-ttu-id="5e4b2-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="5e4b2-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="5e4b2-620">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-620">no</span></span>             | <span data-ttu-id="5e4b2-621">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-621">no</span></span>           |
| <span data-ttu-id="5e4b2-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="5e4b2-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="5e4b2-623">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-623">no</span></span>             | <span data-ttu-id="5e4b2-624">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-624">no</span></span>           |
| <span data-ttu-id="5e4b2-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="5e4b2-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="5e4b2-626">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-626">no</span></span>             | <span data-ttu-id="5e4b2-627">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-627">no</span></span>           |
| <span data-ttu-id="5e4b2-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="5e4b2-629">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-629">no</span></span>             | <span data-ttu-id="5e4b2-630">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-630">no</span></span>           |
| <span data-ttu-id="5e4b2-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="5e4b2-632">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-632">no</span></span>             | <span data-ttu-id="5e4b2-633">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-633">no</span></span>           |
| <span data-ttu-id="5e4b2-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="5e4b2-635">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-635">no</span></span>             | <span data-ttu-id="5e4b2-636">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-636">no</span></span>           |
| <span data-ttu-id="5e4b2-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="5e4b2-638">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-638">no</span></span>             | <span data-ttu-id="5e4b2-639">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-639">no</span></span>           |
| <span data-ttu-id="5e4b2-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="5e4b2-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="5e4b2-641">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-641">no</span></span>             | <span data-ttu-id="5e4b2-642">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-642">no</span></span>           |
| <span data-ttu-id="5e4b2-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="5e4b2-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="5e4b2-644">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-644">no</span></span>             | <span data-ttu-id="5e4b2-645">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-645">no</span></span>           |
| <span data-ttu-id="5e4b2-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="5e4b2-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="5e4b2-647">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-647">no</span></span>             | <span data-ttu-id="5e4b2-648">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-648">no</span></span>           |
| <span data-ttu-id="5e4b2-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="5e4b2-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="5e4b2-650">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-650">no</span></span>             | <span data-ttu-id="5e4b2-651">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-651">no</span></span>           |
| <span data-ttu-id="5e4b2-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="5e4b2-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="5e4b2-653">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-653">no</span></span>             | <span data-ttu-id="5e4b2-654">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-654">no</span></span>           |
| <span data-ttu-id="5e4b2-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="5e4b2-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="5e4b2-656">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-656">no</span></span>             | <span data-ttu-id="5e4b2-657">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-657">no</span></span>           |
| <span data-ttu-id="5e4b2-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="5e4b2-659">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-659">no</span></span>             | <span data-ttu-id="5e4b2-660">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-660">no</span></span>           |
| <span data-ttu-id="5e4b2-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="5e4b2-662">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-662">no</span></span>             | <span data-ttu-id="5e4b2-663">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-663">no</span></span>           |
| <span data-ttu-id="5e4b2-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="5e4b2-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="5e4b2-665">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-665">no</span></span>             | <span data-ttu-id="5e4b2-666">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-666">no</span></span>           |
| <span data-ttu-id="5e4b2-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="5e4b2-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="5e4b2-668">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-668">no</span></span>             | <span data-ttu-id="5e4b2-669">Nein</span><span class="sxs-lookup"><span data-stu-id="5e4b2-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="5e4b2-670">Einschränkungen und Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="5e4b2-670">Limitations and known issues</span></span>
<span data-ttu-id="5e4b2-671">Das Folgende ist eine Liste von Einschränkungen und bekannten Problemen:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="5e4b2-672">Project Schedule APIs können nur von **Benutzern mit Microsoft Project-Lizenz verwendet werden.**</span><span class="sxs-lookup"><span data-stu-id="5e4b2-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="5e4b2-673">Sie können nicht verwendet werden von:</span><span class="sxs-lookup"><span data-stu-id="5e4b2-673">They can't be used by:</span></span>
    - <span data-ttu-id="5e4b2-674">Anwendungsbenutzer</span><span class="sxs-lookup"><span data-stu-id="5e4b2-674">Application users</span></span>
    - <span data-ttu-id="5e4b2-675">Systembenutzern</span><span class="sxs-lookup"><span data-stu-id="5e4b2-675">System users</span></span>
    - <span data-ttu-id="5e4b2-676">Integrationsbenutzern</span><span class="sxs-lookup"><span data-stu-id="5e4b2-676">Integration users</span></span>
    - <span data-ttu-id="5e4b2-677">Andere Benutzer, die nicht über die erforderliche Lizenz verfügen</span><span class="sxs-lookup"><span data-stu-id="5e4b2-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="5e4b2-678">Jeder **OperationSet** kann nur maximal 100 Operationen haben.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="5e4b2-679">Jeder Benutzer kann nur maximal 10 offene **OperationSets** haben.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="5e4b2-680">Project Operations unterstützt derzeit maximal 500 Gesamtaufgaben für ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="5e4b2-681">**OperationSet**-Fehlerstatus und -Fehlerprotokolle sind derzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="5e4b2-682">Grenzwerte und Beschränkungen von Projekten und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="5e4b2-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="5e4b2-683">Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="5e4b2-683">Error handling</span></span>

   - <span data-ttu-id="5e4b2-684">Um die aus den Operations-Sätzen generierten Fehler zu überprüfen, gehen Sie zu **Einstellungen** \> **Integration planen** \> **Operationssätze**.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="5e4b2-685">Um vom Project Schedule Service generierte Fehler zu überprüfen, gehen Sie auf **Einstellungen** \> **Planungsintegration** \> **PSS Fehlerprotokolle**.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="5e4b2-686">Beispielszenario</span><span class="sxs-lookup"><span data-stu-id="5e4b2-686">Sample scenario</span></span>

<span data-ttu-id="5e4b2-687">In diesem Szenario erstellen Sie ein Projekt, ein Teammitglied, vier Aufgaben und zwei Ressourcenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="5e4b2-688">Als Nächstes aktualisieren Sie eine Aufgabe, aktualisieren das Projekt, löschen eine Aufgabe, löschen eine Ressourcenzuweisung und erstellen eine Aufgabenabhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="5e4b2-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="5e4b2-689">Zusätzliche Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e4b2-689">Additional samples</span></span>

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
