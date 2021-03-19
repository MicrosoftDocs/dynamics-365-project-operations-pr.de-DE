---
title: Neues Projekt erstellen
description: Dieses Thema bietet Informationen zum Erstellen eines neuen Projekts.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270722"
---
# <a name="create-a-new-project"></a><span data-ttu-id="90d20-103">Neues Projekt erstellen</span><span class="sxs-lookup"><span data-stu-id="90d20-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d20-104">Führen Sie folgende Schritte aus, um ein neues Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="90d20-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="90d20-105">Auf der Seite **Projektverwaltung** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="90d20-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="90d20-106">**Projekttyp:** Zeit und Material</span><span class="sxs-lookup"><span data-stu-id="90d20-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="90d20-107">**Projektname:** XYZ-Upgrade-Phase 2</span><span class="sxs-lookup"><span data-stu-id="90d20-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="90d20-108">**Projektgruppe** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="90d20-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="90d20-109">**Projektvertrags-ID** 00000002</span><span class="sxs-lookup"><span data-stu-id="90d20-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="90d20-110">Wählen Sie **Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="90d20-111">Eine Ressource einem Projekt zuweisen</span><span class="sxs-lookup"><span data-stu-id="90d20-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="90d20-112">Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, für den Sie zuvor Kompetenzen eingerichtet haben und öffnen Sie den Worker-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="90d20-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="90d20-113">Wählen Sie im Aktionsbereich auf der Registerkarte **Projekt** in der Gruppe **Einrichten** die Option **Projekt zuweisen** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="90d20-114">Auf der Seite **Projektzuweisungen für die Ressourcenvalidierung** auf der Registerkarte **Projekte** im Feld **Fügen Sie das Projekt ausgewählten Projekten hinzu** Filter auf das Projekt **XYZ-Upgrade-Phase 2**.</span><span class="sxs-lookup"><span data-stu-id="90d20-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="90d20-115">In dem Bereich **Verbleibende Projekte** wählen Sie ein Projekt aus und klicken Sie dann auf die Pfeilschaltfläche, um es dem Bereich **Ausgewählte Projekte** hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="90d20-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="90d20-116">Sie können nach Bedarf auch Kategorien für eine Ressource zuweisen.</span><span class="sxs-lookup"><span data-stu-id="90d20-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="90d20-117">Der Kategorietyp ist entweder **Kosten** oder **Umsatz**.</span><span class="sxs-lookup"><span data-stu-id="90d20-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="90d20-118">Der Kategorietyp wird von Ihrer Organisation festgelegt.</span><span class="sxs-lookup"><span data-stu-id="90d20-118">The category type is determined by your organization.</span></span> <span data-ttu-id="90d20-119">Wenn für eine Ressource keine Kategorien zugewiesen sind, sucht Finance die Standardkategorie für Stundenpreise nach Kosten und Einnahmen.</span><span class="sxs-lookup"><span data-stu-id="90d20-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="90d20-120">Richten Sie Projektressourcen- und Rollenmerkmale ein</span><span class="sxs-lookup"><span data-stu-id="90d20-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="90d20-121">Ein Projektmanager kann die Projektresssourcen-Funktion verwenden, um die für das Projekt erforderlichen Rollen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="90d20-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="90d20-122">Rollen können verwendet werden, wenn bestätigte Ressourcen noch unbekannt sind, wenn Ressourcen reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="90d20-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="90d20-123">Rollen können vorübergehend als geplante Ressourcen reserviert werden, sodass Sie die Projektplanungsphase fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="90d20-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="90d20-124">[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="90d20-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="90d20-125">**Szenario:** Contoso wurde beauftragt, ein Zeit- und Materialprojekt mit einer genehmigten Projektcharta abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="90d20-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="90d20-126">Der Junior-Projektmanager schließt den Projektumfang noch ab.</span><span class="sxs-lookup"><span data-stu-id="90d20-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="90d20-127">Der Ressourcenmanager identifiziert derzeit bestimmte Ressourcen, die für die Arbeit an dem neuen Projekt reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="90d20-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="90d20-128">Aufgrund der kritischen Natur des Projekts forderte der Projektsponsor den Senior-Projektmanager als eine der Rollen an.</span><span class="sxs-lookup"><span data-stu-id="90d20-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="90d20-129">Der Ressourcenmanager muss die neue Ressource erwerben und die Rolle im System definieren, falls der Junior-Projektmanager die Ressourceninformationen während der Projektplanung benötigt.</span><span class="sxs-lookup"><span data-stu-id="90d20-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="90d20-130">Die folgenden Schritte zeigen, wie der Ressourcenmanager die Rolle des Senior-Projektmanagers einrichten und ihr Ressourcenmerkmale zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="90d20-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="90d20-131">Später kann die Rolle verwendet werden, um nach verfügbaren Ressourcen zu suchen, die den erforderlichen Ressourcenkompetenzen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="90d20-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="90d20-132">Auf der Seite **Rollen einrichten** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="90d20-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="90d20-133">**Rollen-ID:** Senior Projektmanager</span><span class="sxs-lookup"><span data-stu-id="90d20-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="90d20-134">**Beschreibung:** Senior Projektmanager</span><span class="sxs-lookup"><span data-stu-id="90d20-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="90d20-135">Wählen Sie **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-135">Select **Create**.</span></span>
3. <span data-ttu-id="90d20-136">Wählen Sie die Rolle **Senior Projektmanager** aus und wählen Sie dann **Eigenschaften konfigurieren**.</span><span class="sxs-lookup"><span data-stu-id="90d20-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="90d20-137">In dem Feld **Eigenschaftentyp** wählen Sie **Fertigkeit**.</span><span class="sxs-lookup"><span data-stu-id="90d20-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="90d20-138">In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld die Fertigkeit ein, nach der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="90d20-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="90d20-139">In dem Feld **Eigenschaftentyp** wählen Sie **Zertifikat**.</span><span class="sxs-lookup"><span data-stu-id="90d20-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="90d20-140">In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld den Zertifikatstyp ein, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="90d20-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="90d20-141">Eine Projektressource einem Projekt zuweisen</span><span class="sxs-lookup"><span data-stu-id="90d20-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="90d20-142">Auf der Seite **Alle Projekte** wählen Sie das Projekt **XYZ-Upgrade-Phase 2** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="90d20-143">Auf der Registerkarte **Projektteam und Terminplanung** wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="90d20-144">In dem Feld **Rolle** wählen Sie **Teammitglied**.</span><span class="sxs-lookup"><span data-stu-id="90d20-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="90d20-145">Wählen Sie **Aus Kalender buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="90d20-146">Auf der Seite **Verfügbarkeit von Ressourcen** wählen Sie **Einstellungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="90d20-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="90d20-147">Auf der Seite **Passen Sie die Einstellungen an** geben Sie die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="90d20-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="90d20-148">**Format für die Datumsbereichsansicht:** Tag</span><span class="sxs-lookup"><span data-stu-id="90d20-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="90d20-149">**Verfügbarkeitsbeschreibungen anzeigen:** Ja</span><span class="sxs-lookup"><span data-stu-id="90d20-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="90d20-150">**Restkapazität anzeigen:** Ja</span><span class="sxs-lookup"><span data-stu-id="90d20-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="90d20-151">Wählen Sie eine Ressource in der Liste der buchbaren Ressourcen aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="90d20-152">Wählen Sie **Hartes Buch** und **Volle Kapazität** aus.</span><span class="sxs-lookup"><span data-stu-id="90d20-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="90d20-153">Zuweisen einer Ressource einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="90d20-153">Assign a resource to a default role</span></span>

<span data-ttu-id="90d20-154">Um Projekt- oder Ressourcenmanagern zu helfen, können Sie Drilldown zu den Ressourcen ausführen, die für ein Projekt reserviert werden können.</span><span class="sxs-lookup"><span data-stu-id="90d20-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="90d20-155">Sie können einer vorhandenen Ressource oder einer neu erworbenen Ressource einer Standardrolle zuordnen.</span><span class="sxs-lookup"><span data-stu-id="90d20-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="90d20-156">Als Daniel zum Beispiel eingestellt wurde, verfügte er über die Erfahrung und die Fähigkeiten, um die Rolle des Business Analyst zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="90d20-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="90d20-157">Der Ressourcenmanager hat diese Rolle als Daniels Standardrolle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="90d20-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="90d20-158">Aus diesem Grund hat der Ressourcenmanager Daniel zu einem Pool von Geschäftsanalysten hinzugefügt, die für die Arbeit an Projekten zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="90d20-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="90d20-159">Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die für die Arbeit an Projekten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="90d20-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="90d20-160">Sie können diese Informationen als ein Kriterium verwenden, wenn sie während der Ressourcenerfüllung eine Entscheidungsanalyse mit mehreren Kriterien durchführen.</span><span class="sxs-lookup"><span data-stu-id="90d20-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="90d20-161">Sie können dem Filter auch andere Ressourcenmerkmale hinzufügen, um nach Ressourcen zu suchen, die über bestimmte Fähigkeiten, Ausbildung und Erfahrung für ein bestimmtes Projekt verfügen.</span><span class="sxs-lookup"><span data-stu-id="90d20-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="90d20-162">**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Rolle des Senior-Projektmanagers wurde während der Projektplanungsphase als geplante Ressource reserviert.</span><span class="sxs-lookup"><span data-stu-id="90d20-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="90d20-163">Der Ressourcenmanager hat jetzt eine Ressource erworben, um die Rolle des Senior-Projektmanagers zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="90d20-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="90d20-164">Auf der Seite **Ressourcenliste** wählen Sie **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="90d20-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="90d20-165">Auf der Seite **Rollenressourcen** wählen Sie **Neu** und geben die folgenden Werte ein:</span><span class="sxs-lookup"><span data-stu-id="90d20-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="90d20-166">**Wirksam:** Geben Sie das aktuelle Datum ein.</span><span class="sxs-lookup"><span data-stu-id="90d20-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="90d20-167">**Ablauf:** Geben Sie **Nie** ein.</span><span class="sxs-lookup"><span data-stu-id="90d20-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="90d20-168">**Rolle:** Geben Sie **Senior Project Manager** ein.</span><span class="sxs-lookup"><span data-stu-id="90d20-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="90d20-169">Wählen Sie **Speichern** aus, und schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="90d20-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="90d20-170">Auf der Registerkarte **Kompetenzen** fügen Sie die Fertigkeit **ProjectMgmt** und **PMP** Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="90d20-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]