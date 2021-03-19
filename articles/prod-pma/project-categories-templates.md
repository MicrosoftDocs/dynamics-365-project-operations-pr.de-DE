---
title: Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektkostenkategorien zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289638"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="16168-103">Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16168-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16168-104">Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Ausgaben zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16168-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="16168-105">Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16168-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="16168-106">Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16168-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="16168-107">Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="16168-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="16168-108">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch KB 4131710 installieren.</span><span class="sxs-lookup"><span data-stu-id="16168-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="16168-109">Datenfluss für Project Service Automation and Finance</span><span class="sxs-lookup"><span data-stu-id="16168-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="16168-110">Die Integrationslösung für Project Service Automation und Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="16168-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="16168-111">Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projektkosten-Transaktionskategorien zwischen Finance und Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="16168-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="16168-112">Wenn die Projektausgabenkategorien in Finance beherrscht werden, erfolgt der Integrationsfluss zunächst von Finance zu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="16168-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="16168-113">Die Integrations-IDs der Projektkostenkategorien werden dann durch Synchronisation von Project Service Automation zu Finance aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="16168-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="16168-114">Wenn die Projektausgabenkategorien in Project Service Automation beherrscht werden, erfolgt der Integrationsfluss zunächst von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="16168-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="16168-115">Die Projektkategorien müssen bereits vor der Synchronisierung über Project Service Automation in Finance konfiguriert worden sein.</span><span class="sxs-lookup"><span data-stu-id="16168-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="16168-116">Dann synchronisieren Sie von Finance zurück zu Project Service Automation und synchronisieren Sie dann erneut von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="16168-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="16168-117">Auf diese Weise stellen Sie sicher, dass die Kategorien verknüpft sind und keine Duplikate erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="16168-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="16168-118">In der Regel werden die Projektkostenkategorien in Finance beherrscht.</span><span class="sxs-lookup"><span data-stu-id="16168-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="16168-119">Wenn dies jedoch nicht der Fall ist oder wenn in Project Service Automation bereits Ausgabenkategorien erstellt wurden, müssen Sie zunächst mithilfe der Vorlage Projektausgaben-Transaktionskategorien (PSA zu Fin und Ops) synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="16168-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="16168-120">Synchronisieren Sie anschließend mithilfe der Vorlage für Projektkostentransaktionskategorien (Fin und Ops zu PSA).</span><span class="sxs-lookup"><span data-stu-id="16168-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="16168-121">Anschließend sollten Sie die Synchronisierung von Project Service Automation zu Finance noch einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="16168-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="16168-122">Wenn Sie zuerst über Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance erfüllt sein, bevor die Synchronisierung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="16168-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="16168-123">Die gemeinsam genutzte Kategorie, die der in Project Service Automation eingerichteten Projektkategorie entspricht, muss vorhanden sein und für **Projekt** und **Kosten** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="16168-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="16168-124">Für jede juristische Person im Finance, in die integriert werden muss, müssen die folgenden Projektkategorien vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="16168-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="16168-125">**Projektkategorie** existiert.</span><span class="sxs-lookup"><span data-stu-id="16168-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="16168-126">**Verwendung in Kosten** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="16168-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="16168-127">**Aktiv im Journal** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="16168-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="16168-128">**Art der Transaktion** ist auf **Ausgaben** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16168-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="16168-129">Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="16168-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="16168-130">[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="16168-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="16168-131">Synchronisieren Sie Projektausgabenkategorien von Finance zu Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16168-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="16168-132">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="16168-132">Template and task</span></span>

<span data-ttu-id="16168-133">Um auf die Vorlage zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="16168-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="16168-134">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Finance zu Project Service Automation zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="16168-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="16168-135">**Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (Fin und Ops zu PSA)</span><span class="sxs-lookup"><span data-stu-id="16168-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="16168-136">**Name der Aufgabe im Projekt:** Kategorien mit PSA synchronisieren</span><span class="sxs-lookup"><span data-stu-id="16168-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="16168-137">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="16168-137">Entity set</span></span>

| <span data-ttu-id="16168-138">Finanzen</span><span class="sxs-lookup"><span data-stu-id="16168-138">Finance</span></span>                           | <span data-ttu-id="16168-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16168-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="16168-140">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="16168-140">Integration entity for categories</span></span> | <span data-ttu-id="16168-141">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="16168-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="16168-142">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="16168-142">Entity flow</span></span>

<span data-ttu-id="16168-143">Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="16168-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="16168-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="16168-144">Power Query</span></span>

<span data-ttu-id="16168-145">Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel verwenden, um die Abrechnungsart für die Transaktionskategorie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="16168-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="16168-146">Die Vorlage Projektkosten-Transaktionskategorien (Fin und Ops zu PSA) enthält eine Standardspalte und -zuordnung.</span><span class="sxs-lookup"><span data-stu-id="16168-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="16168-147">Wenn Sie eine eigene Vorlage erstellen, müssen Sie eine bedingte Spalte in Power Query hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="16168-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="16168-148">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="16168-148">Follow these steps.</span></span>

1. <span data-ttu-id="16168-149">Klicken Sie auf den Pfeil, um die Zuordnung der Aufgabe Projektausgabenkategorien in der Vorlage Projektausgaben-Transaktionskategorien (Fin und Ops zu PSA) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="16168-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="16168-150">Klicken Sie auf die Verknüpfung **Erweiterte Abfrage und Filterung**, um Power Query zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="16168-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="16168-151">Wählen Sie **Bedingte Spalte hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="16168-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="16168-152">Geben Sie einen Namen für die neue Spalte ein, wie **Abrechnungstyp**.</span><span class="sxs-lookup"><span data-stu-id="16168-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="16168-153">Geben Sie die folgende Bedingung ein: **Wenn CATEGORYID nicht gleich null ist, dann 19235001, andernfalls null**.</span><span class="sxs-lookup"><span data-stu-id="16168-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="16168-154">Klicken Sie in der Spalte auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="16168-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="16168-155">Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuordnen.</span><span class="sxs-lookup"><span data-stu-id="16168-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="16168-156">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="16168-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="16168-157">Das Mapping zeigt die Feldinformationen an, die von Finance zu Project Service Automation synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="16168-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="16168-158">[![Projektausgabenkategorie zu Project Service Automation-Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="16168-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="16168-159">Synchronisieren Sie Projektausgabenkategorien von Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="16168-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="16168-160">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="16168-160">Template and task</span></span>

<span data-ttu-id="16168-161">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Project Service Automation zu Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="16168-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="16168-162">**Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="16168-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="16168-163">**Name der Aufgabe im Projekt:** Kategorien zu Fin Ops synchronisieren</span><span class="sxs-lookup"><span data-stu-id="16168-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="16168-164">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="16168-164">Entity set</span></span>

| <span data-ttu-id="16168-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16168-165">Project Service Automation</span></span> | <span data-ttu-id="16168-166">Finanzen</span><span class="sxs-lookup"><span data-stu-id="16168-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="16168-167">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="16168-167">Transaction categories</span></span>     | <span data-ttu-id="16168-168">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="16168-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="16168-169">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="16168-169">Entity flow</span></span>

<span data-ttu-id="16168-170">Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="16168-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="16168-171">Die Synchronisation zurück zu Finance aktualisiert die Projektkostenkategorien in Finance mit der Integrations-ID von Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="16168-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="16168-172">Vorlagenzuordnung in der Datenintegration</span><span class="sxs-lookup"><span data-stu-id="16168-172">Template mapping in Data integration</span></span>

<span data-ttu-id="16168-173">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="16168-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="16168-174">Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="16168-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="16168-175">[![Project Service Automation zu Finance-Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="16168-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]