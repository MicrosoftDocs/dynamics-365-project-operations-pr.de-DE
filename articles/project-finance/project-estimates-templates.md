---
title: Synchronisieren Sie Projektschätzungen direkt von Project Service Automation zu Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektstunenschätzungen und Projektausgabenschätzungen direkt von Microsoft Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716488"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="5b083-103">Synchronisieren Sie Projektschätzungen direkt von Project Service Automation zu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b083-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b083-104">Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektstundenschätzungen und Projektausgabenschätzungen direkt von Dynamics 365 Project Service Automation zu Dynamics 365 Finance verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="5b083-105">Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperre sind in Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b083-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="5b083-106">Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b083-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="5b083-107">Datenfluss für Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="5b083-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="5b083-108">Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b083-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="5b083-109">Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projektstundenschätzungen und Projektausgabenschätzungen von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="5b083-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5b083-110">Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="5b083-111">[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="5b083-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="5b083-112">Projektstundenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="5b083-113">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="5b083-113">Template and tasks</span></span>

<span data-ttu-id="5b083-114">Um auf die verfügbarem Vorlagen zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5b083-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5b083-115">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projektstundenschätzungen von Project Service Automation zu Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b083-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="5b083-116">**Name der Vorlage in der Datenintegration:** Projektstundenschätzungen (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="5b083-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="5b083-117">**Name der Aufgabe im Projekt:**</span><span class="sxs-lookup"><span data-stu-id="5b083-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="5b083-118">Transaktionsbeziehungen</span><span class="sxs-lookup"><span data-stu-id="5b083-118">Transaction relationships</span></span>
    - <span data-ttu-id="5b083-119">Ausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="5b083-120">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="5b083-120">Entity set</span></span>

| <span data-ttu-id="5b083-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5b083-121">Project Service Automation</span></span> | <span data-ttu-id="5b083-122">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5b083-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="5b083-123">Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="5b083-123">Project tasks</span></span>              | <span data-ttu-id="5b083-124">Integrationseinheit für Projektstundenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="5b083-125">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="5b083-125">Entity flow</span></span>

<span data-ttu-id="5b083-126">Projektstundenschätzungen werden in Project Service Automation verwaltet und als Projektstundenprognosen mit Finance synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="5b083-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5b083-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-127">Prerequisites</span></span>

<span data-ttu-id="5b083-128">Bevor eine Synchronisierung der Projektstundenschätzungen erfolgen kann, müssen Sie Projekte, Projektaufgaben und Transaktionskategorien für Projektkosten synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b083-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="5b083-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="5b083-129">Power Query</span></span>

<span data-ttu-id="5b083-130">In der Vorlage für Projektstundenschätzungen müssen Sie Microsoft Power Query für Excel verwenden, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="5b083-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="5b083-131">Legen Sie die Standard-ID des Prognosemodells fest, die verwendet wird, wenn die Integration neue Stundenprognosen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b083-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="5b083-132">Filtern Sie alle ressourcenspezifischen Datensätze in der Aufgabe heraus, bei denen die Integration in Stundenvorhersagen fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5b083-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="5b083-133">Filtern Sie alle leeren Transaktionskategoriezeilen heraus.</span><span class="sxs-lookup"><span data-stu-id="5b083-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="5b083-134">Wenn Sie diese Aufgabe nicht ausführen, kann dies zu falschen Stundenvorhersagen führen.</span><span class="sxs-lookup"><span data-stu-id="5b083-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="5b083-135">Legen Sie die Standardmdell-ID fest</span><span class="sxs-lookup"><span data-stu-id="5b083-135">Set the default forecast model ID</span></span>

<span data-ttu-id="5b083-136">Um die Standard-Prognosemodell-ID in der Vorlage zu aktualisieren, klicken Sie auf den Pfeil **Zuordnen** und öffnen das Mapping.</span><span class="sxs-lookup"><span data-stu-id="5b083-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="5b083-137">Dann wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**.</span><span class="sxs-lookup"><span data-stu-id="5b083-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="5b083-138">Wenn Sie die Standardvorlage für Projektstundenschätzungen (PSA zu Fin und Ops) verwenden, wählen Sie die Option **Eingefügter Zustand** aud der Liste **Angewandte Schritte** aus.</span><span class="sxs-lookup"><span data-stu-id="5b083-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="5b083-139">In dem Eintrag **Funktion** ersetzen Sie **O\_Prognose** mit dem Namen der Prognosemodell-ID, die für die Integration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b083-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="5b083-140">Die Standardvorlage enthält eine Prognosemodell-ID aus den Demo-Daten.</span><span class="sxs-lookup"><span data-stu-id="5b083-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="5b083-141">Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="5b083-142">Wählen Sie in Power Query **Bedingte Spalte hinzufügen** aus und geben Sie einen Namen für die neue Spalte ein wie **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="5b083-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="5b083-143">Geben Sie die Bedingung für die Spalte ein. Wenn die Projektaufgabe nicht null ist, dann \<Geben Sie die Prognosemodell-ID ein\>; sonst Null.</span><span class="sxs-lookup"><span data-stu-id="5b083-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="5b083-144">Filtern Sie ressourcenspezifische Datensätze heraus</span><span class="sxs-lookup"><span data-stu-id="5b083-144">Filter out resource-specific records</span></span>

<span data-ttu-id="5b083-145">Die Vorlage Projektstundenschätzungen (PSA zu Fin und Ops) verfügt über einen Standardfilter, mit dem alle ressourcenspezifischen Datensätze entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="5b083-146">Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="5b083-147">Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus, um die Spalte **msdyn\_islinetask** zu filtern, um nur **Fals** Datensätze einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5b083-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="5b083-148">Filtern Sie alle leeren Transaktionskategoriezeilen heraus</span><span class="sxs-lookup"><span data-stu-id="5b083-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="5b083-149">Sie müssen einen Filter hinzufügen, um alle Zeilen mit leeren Transaktionskategorien zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5b083-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="5b083-150">Diese Aufgabe ist erforderlich, unabhängig davon, ob Sie die Standardvorlage verwenden oder eine eigene Vorlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b083-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="5b083-151">Dieser Filter entfernt alle Zusammenfassungszeilen aus Project Service Automation, die dazu führen können, dass die Stundenprognosen in Finance falsch sind.</span><span class="sxs-lookup"><span data-stu-id="5b083-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="5b083-152">Wählen Sie den Link **Erweiterte Abfrage und Filterung** zum Herausfiltern von Nulldatensätzen in der Spalte **msdyn\_Transaktionskategorie\_Wert**.</span><span class="sxs-lookup"><span data-stu-id="5b083-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5b083-153">Vorlagenzuordnung in der Datenintegration</span><span class="sxs-lookup"><span data-stu-id="5b083-153">Template mapping in Data integration</span></span>

<span data-ttu-id="5b083-154">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="5b083-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="5b083-155">Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5b083-156">[![Vorlagenzuordnung](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b083-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="5b083-157">Projektausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="5b083-158">Vorlage und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="5b083-158">Template and tasks</span></span>

<span data-ttu-id="5b083-159">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenschätzungen von Project Service Automation zu Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b083-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="5b083-160">**Name der Vorlage in der Datenintegration:** Projektausgabenschätzungen (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="5b083-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="5b083-161">**Name der Aufgabe im Projekt:**</span><span class="sxs-lookup"><span data-stu-id="5b083-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="5b083-162">Transaktionsbeziehungen</span><span class="sxs-lookup"><span data-stu-id="5b083-162">Transaction relationships</span></span> 
    - <span data-ttu-id="5b083-163">Ausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="5b083-164">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="5b083-164">Entity set</span></span>

| <span data-ttu-id="5b083-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5b083-165">Project Service Automation</span></span> | <span data-ttu-id="5b083-166">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5b083-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="5b083-167">Transaktionsverbindungen</span><span class="sxs-lookup"><span data-stu-id="5b083-167">Transaction Connections</span></span>    | <span data-ttu-id="5b083-168">Integrationsentität für die Projekttransaktion Beziehungen</span><span class="sxs-lookup"><span data-stu-id="5b083-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="5b083-169">Vorkalkulationszeilen</span><span class="sxs-lookup"><span data-stu-id="5b083-169">Estimate Lines</span></span>             | <span data-ttu-id="5b083-170">Integrationseinheit für Projektausgabenschätzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="5b083-171">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="5b083-171">Entity flow</span></span>

<span data-ttu-id="5b083-172">Projektausgabenschätzungen werden in Project Service Automation verwaltet und als Projektausgabenprognosen mit Finance synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="5b083-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5b083-173">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5b083-173">Prerequisites</span></span>

<span data-ttu-id="5b083-174">Bevor eine Synchronisierung der Projektausgabenschätzungen erfolgen kann, müssen Sie Projekte, Projektaufgaben und Transaktionskategorien für Projektkosten synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b083-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="5b083-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="5b083-175">Power Query</span></span>

<span data-ttu-id="5b083-176">In der Vorlage für Projektausgabenschätzungen müssen Sie Microsoft Power Query verwenden, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="5b083-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="5b083-177">Filtern, um nur Ausgabenschätzungszeilendatensätze einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5b083-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="5b083-178">Legen Sie die Standard-ID des Prognosemodells fest, die verwendet wird, wenn die Integration neue Stundenprognosen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b083-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="5b083-179">Transformieren Sie die Abrechnungsarten.</span><span class="sxs-lookup"><span data-stu-id="5b083-179">Transform the billing types.</span></span>
- <span data-ttu-id="5b083-180">Transformieren Sie die Transaktionsarten.</span><span class="sxs-lookup"><span data-stu-id="5b083-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="5b083-181">Filtern, um nur Ausgabenschätzungszeilen einzuschließen</span><span class="sxs-lookup"><span data-stu-id="5b083-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="5b083-182">Die Vorlage Projektkostenschätzungen (PSA zu Fin und Ops) verfügt über einen Standardfilter, der nur Ausgabenzeilen in die Integration einbezieht.</span><span class="sxs-lookup"><span data-stu-id="5b083-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="5b083-183">Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="5b083-184">Wählen Sie die Aufgabe **Transaktionsbeziehungen** und klicken Sie dann auf den Pfeil **Zuordnen**, um das Mapping zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5b083-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="5b083-185">Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**.</span><span class="sxs-lookup"><span data-stu-id="5b083-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="5b083-186">Filtern Sie die Spalte **msdyn\_Transaktionstyp1**, sodass sie nur **msdyn\_Schätzlinie** enthält.</span><span class="sxs-lookup"><span data-stu-id="5b083-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="5b083-187">Legen Sie die Standardmdell-ID fest</span><span class="sxs-lookup"><span data-stu-id="5b083-187">Set the default forecast model ID</span></span>

<span data-ttu-id="5b083-188">Um die Standard-Prognosemodell-ID in der Vorlage zu aktualisieren, wählen Sie die Aufgabe **Ausgabenschhätzung** und klicken auf den Pfeil **Zuordnen** und öffnen das Mapping.</span><span class="sxs-lookup"><span data-stu-id="5b083-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="5b083-189">Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**.</span><span class="sxs-lookup"><span data-stu-id="5b083-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="5b083-190">Wenn Sie die Standardvorlage für Projekt-Ausgabenschätzungen (PSA zu Fin und Ops) verwenden, wählen Sie in Power Query die erste **Eingefügte Bedingung** im Bereich **Angewandte Schritte** aus.</span><span class="sxs-lookup"><span data-stu-id="5b083-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="5b083-191">In dem Eintrag **Funktion** ersetzen Sie **O\_Prognose** mit dem Namen der Prognosemodell-ID, die für die Integration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b083-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="5b083-192">Die Standardvorlage enthält eine Prognosemodell-ID aus den Demo-Daten.</span><span class="sxs-lookup"><span data-stu-id="5b083-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="5b083-193">Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="5b083-194">Wählen Sie in Power Query **Bedingte Spalte hinzufügen** aus und geben Sie einen Namen für die neue Spalte ein wie **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="5b083-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="5b083-195">Geben Sie die Bedingung für die Spalte ein, wenn die Zeile ID nicht null ist, dann \<geben Sie die Prognosemodell-ID ein\>; sonst Null.</span><span class="sxs-lookup"><span data-stu-id="5b083-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="5b083-196">Transformieren Sie die Abrechnungsarten</span><span class="sxs-lookup"><span data-stu-id="5b083-196">Transform the billing types</span></span>

<span data-ttu-id="5b083-197">Die Vorlage für Projektkostenschätzungen (PSA zu Fin und Ops) enthält eine bedingte Spalte, mit der die Abrechnungsarten transformiert werden, die während der Integration von Project Service Automation empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="5b083-198">Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen bedingte Spalte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="5b083-199">Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus und wählen dann **Bedingte Spalte hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5b083-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="5b083-200">Geben Sie einen Namen für die neue Spalte ein, wie **Abrechnungstyp**.</span><span class="sxs-lookup"><span data-stu-id="5b083-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="5b083-201">Geben Sie die folgende Bedingung ein:</span><span class="sxs-lookup"><span data-stu-id="5b083-201">Then enter the following condition:</span></span>

<span data-ttu-id="5b083-202">Wenn **msdyn\_Abrechnungstyp** = 192350000 ist, dann **Nicht belastbar**</span><span class="sxs-lookup"><span data-stu-id="5b083-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="5b083-203">wenn **msdyn\_Abrechnungstyp** = 192350001 ist, dann **belastbar**</span><span class="sxs-lookup"><span data-stu-id="5b083-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="5b083-204">wenn **msdyn\_Abrechnungstyp** = 192350002 ist, dann **kostenlos**</span><span class="sxs-lookup"><span data-stu-id="5b083-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="5b083-205">Sonst **Nicht verfügbar**</span><span class="sxs-lookup"><span data-stu-id="5b083-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="5b083-206">Transformieren Sie die Transaktionsarten</span><span class="sxs-lookup"><span data-stu-id="5b083-206">Transform the transaction types</span></span>

<span data-ttu-id="5b083-207">Die Vorlage für Projektkostenschätzungen (PSA zu Fin und Ops) enthält eine bedingte Spalte, mit der die Transaktionsarten transformiert werden, die während der Integration von Project Service Automation empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="5b083-208">Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen bedingte Spalte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b083-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="5b083-209">Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus und wählen dann **Bedingte Spalte hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5b083-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="5b083-210">Geben Sie einen Namen für die neue Spalte ein, wie **Art der Transaktion**.</span><span class="sxs-lookup"><span data-stu-id="5b083-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="5b083-211">Geben Sie die folgende Bedingung ein:</span><span class="sxs-lookup"><span data-stu-id="5b083-211">Then enter the following condition:</span></span>

<span data-ttu-id="5b083-212">Wenn **msdyn\_Transaktionstypcode** = 192350000 dann **Kosten**</span><span class="sxs-lookup"><span data-stu-id="5b083-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="5b083-213">wenn **msdyn\_Transaktionstypcode** = 192350005 dann **Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="5b083-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="5b083-214">sonst **Null**</span><span class="sxs-lookup"><span data-stu-id="5b083-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5b083-215">Vorlagenzuordnung in der Datenintegration</span><span class="sxs-lookup"><span data-stu-id="5b083-215">Template mapping in Data integration</span></span>

<span data-ttu-id="5b083-216">Die folgende Abbildung zeigt Beispiele für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="5b083-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="5b083-217">Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5b083-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5b083-218">[![Vorlagenzuordnung](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b083-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="5b083-219">[![Vorlagenzuordnung](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b083-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
