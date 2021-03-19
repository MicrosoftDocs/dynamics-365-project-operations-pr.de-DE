---
title: Projektressourcen einrichten
description: Dieses Thema enthält Informationen zum Einrichten oder Anfordern von Projektressourcen.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288738"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="872e8-103">Projektressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="872e8-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="872e8-104">Sie müssen einen Kalender einrichten und ihn einem Mitarbeiter oder einem Mitarbeiter zuordnen.</span><span class="sxs-lookup"><span data-stu-id="872e8-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="872e8-105">Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen zu planen, die für das Projekt reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="872e8-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="872e8-106">Während der Kalendereinrichtung können Projektmanager im Rahmen der Ressourcenoptimierung eine Ressourcenebene erstellen.</span><span class="sxs-lookup"><span data-stu-id="872e8-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="872e8-107">Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="872e8-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="872e8-108">Sie können einen Kalender auf der Seite **Kalender** einrichten.</span><span class="sxs-lookup"><span data-stu-id="872e8-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="872e8-109">Wenn Sie einen Mitarbeiter als Projektressource einrichten, können Sie aus Mitarbeitern auswählen, die in dem Unternehmen arbeiten, für das Sie Ressourcen einrichten.</span><span class="sxs-lookup"><span data-stu-id="872e8-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="872e8-110">Alternativ können Sie Arbeiter aus anderen Unternehmen für Ihre Organisation auswählen.</span><span class="sxs-lookup"><span data-stu-id="872e8-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="872e8-111">Diese Mitarbeiter werden als konzerninterne Ressourcen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="872e8-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="872e8-112">In den folgenden Verfahren wird erläutert, wie Sie einen Worker als Projektressource in Ihrem Unternehmen einrichten und eine konzerninterne Projektressource einrichten.</span><span class="sxs-lookup"><span data-stu-id="872e8-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="872e8-113">Richten Sie einen Worker als Projektressource ein</span><span class="sxs-lookup"><span data-stu-id="872e8-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="872e8-114">Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, den Sie als Projektressource hinzufügen, und öffnen Sie den Worker-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="872e8-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="872e8-115">Wählen Sie im Aktionsbereich **Projekt** &gt; **Einrichtung** &gt; **Projekt einrichten**.</span><span class="sxs-lookup"><span data-stu-id="872e8-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="872e8-116">Wählen Sie einen Kalender aus, und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="872e8-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="872e8-117">Sie können auch Standardprojekte für eine Ressource als eine Art Vorzuweisung angeben.</span><span class="sxs-lookup"><span data-stu-id="872e8-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="872e8-118">Vorabzuweisungen können verwendet werden, wenn der Ressourcenmanager oder Projektmanager im Voraus weiß, an welchen Projekten die Ressource arbeiten wird.</span><span class="sxs-lookup"><span data-stu-id="872e8-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="872e8-119">Vorabzuweisungen können auch auf Anfrage eines Projektsponsors oder Kunden erfolgen.</span><span class="sxs-lookup"><span data-stu-id="872e8-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="872e8-120">Um ein Projekt vorab zuzuweisen, klicken Sie auf die Seite **Projekte zuweisen** auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** und wählen Sie das entsprechende Projekt.</span><span class="sxs-lookup"><span data-stu-id="872e8-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="872e8-121">Richten Sie eine Intercompany-Ressource ein</span><span class="sxs-lookup"><span data-stu-id="872e8-121">Set up an intercompany resource</span></span>

<span data-ttu-id="872e8-122">Wenn Sie einen Mitarbeiter als konzerninterne Ressource einrichten, müssen Sie die Einrichtung sowohl im Kreditunternehmen als auch im Kreditunternehmen abschließen.</span><span class="sxs-lookup"><span data-stu-id="872e8-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="872e8-123">In der Kreditgesellschaft</span><span class="sxs-lookup"><span data-stu-id="872e8-123">In the lending company</span></span>

1. <span data-ttu-id="872e8-124">Vergewissern Sie sich unter Finanzen, dass das Kreditunternehmen ausgewählt ist, und führen Sie dann den Vorgang im vorherigen Abschnitt Einrichten eines Arbeitnehmers als Projektressource aus.</span><span class="sxs-lookup"><span data-stu-id="872e8-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="872e8-125">Klicken Sie auf der Seite **Intercompany-Buchhaltung** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="872e8-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="872e8-126">In dem Feld **ID der juristischen Person** wählen Sie das kreditgebende Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="872e8-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="872e8-127">Füllen Sie die verbleibenden Felder aus, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="872e8-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="872e8-128">Wählen Sie auf der Seite **Übertragungspreis** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="872e8-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="872e8-129">In dem Feld **Kreditgebende juristische Person** wählen Sie das entsprechende Unternehmen aus.</span><span class="sxs-lookup"><span data-stu-id="872e8-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="872e8-130">Um dem Kreditnehmer nur die Ressource zu verleihen, die Sie am Anfang dieses Abschnitts erstellt haben, wählen Sie im Feld **Ressource** den Namen der Ressource aus, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="872e8-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="872e8-131">Um alle Ressourcen des kreditgebenden Unternehmens dem Kreditunternehmen zur Verfügung zu stellen, lassen Sie das Feld **Ressource** leer.</span><span class="sxs-lookup"><span data-stu-id="872e8-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="872e8-132">Auf der Seite **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Intercompany** legen Sie Option **Aktivieren Sie die unternehmensübergreifende Ressourcenplanung und Arbeitszeittabellen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="872e8-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="872e8-133">Im Kreditunternehmen</span><span class="sxs-lookup"><span data-stu-id="872e8-133">In the borrowing company</span></span>

- <span data-ttu-id="872e8-134">Auf der Seite **Ressourcenliste** geben Sie im Suchfilter auf der Seite den Namen der Ressource ein, die Sie für das kreditgebende Unternehmen erstellt haben, um zu überprüfen, ob der Name in der Ressourcenliste des kreditgebenden Unternehmens enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="872e8-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="872e8-135">Projektressourcen anfordern</span><span class="sxs-lookup"><span data-stu-id="872e8-135">Request project resources</span></span>
<span data-ttu-id="872e8-136">Mit der Funktionalität für die Planung von Projektressourcen können Ressourcenmanager nur besetzte Ressourcen auf Aufträge oder Projekte verteilen.</span><span class="sxs-lookup"><span data-stu-id="872e8-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="872e8-137">Um diese Funktionalität zu aktivieren, führen Sie die folgenden Aufgaben aus oder überprüfen Sie, ob sie abgeschlossen wurden:</span><span class="sxs-lookup"><span data-stu-id="872e8-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="872e8-138">Nummernserien einrichten.</span><span class="sxs-lookup"><span data-stu-id="872e8-138">Set up number sequences.</span></span>
- <span data-ttu-id="872e8-139">Projektmanagement- und Buchhaltungsworkflows einrichten.</span><span class="sxs-lookup"><span data-stu-id="872e8-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="872e8-140">Aktivieren Sie Workflows für Ressourcenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="872e8-140">Enable resource request workflows.</span></span>

<span data-ttu-id="872e8-141">Nachdem die vorhergehenden Aufgaben abgeschlossen wurden, können Sie die folgenden Aufgaben nach Bedarf ausführen:</span><span class="sxs-lookup"><span data-stu-id="872e8-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="872e8-142">Erstellen Sie eine Ressourcenanforderung aus einer mit Personal gebuchten Ressource.</span><span class="sxs-lookup"><span data-stu-id="872e8-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="872e8-143">Ressourcenanforderungen überwachen.</span><span class="sxs-lookup"><span data-stu-id="872e8-143">Monitor resource requests.</span></span>
- <span data-ttu-id="872e8-144">Erfüllen von Ressourcenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="872e8-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="872e8-145">Fordern Sie eine besetzte Ressource von einem PSP an.</span><span class="sxs-lookup"><span data-stu-id="872e8-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="872e8-146">Buchen Sie Ressourcen für ein Projekt, ohne eine Personalressource anzufordern.</span><span class="sxs-lookup"><span data-stu-id="872e8-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]