---
title: Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektkostenkategorien zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.
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
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716499"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="f2fcd-103">Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f2fcd-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f2fcd-104">Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Ausgaben zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="f2fcd-105">Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="f2fcd-106">Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="f2fcd-107">Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f2fcd-108">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch KB 4131710 installieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="f2fcd-109">Datenfluss für Project Service Automation and Finance</span><span class="sxs-lookup"><span data-stu-id="f2fcd-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="f2fcd-110">Die Integrationslösung für Project Service Automation und Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f2fcd-111">Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projektkosten-Transaktionskategorien zwischen Finance und Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="f2fcd-112">Wenn die Projektausgabenkategorien in Finance beherrscht werden, erfolgt der Integrationsfluss zunächst von Finance zu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="f2fcd-113">Die Integrations-IDs der Projektkostenkategorien werden dann durch Synchronisation von Project Service Automation zu Finance aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f2fcd-114">Wenn die Projektausgabenkategorien in Project Service Automation beherrscht werden, erfolgt der Integrationsfluss zunächst von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="f2fcd-115">Die Projektkategorien müssen bereits vor der Synchronisierung über Project Service Automation in Finance konfiguriert worden sein.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="f2fcd-116">Dann synchronisieren Sie von Finance zurück zu Project Service Automation und synchronisieren Sie dann erneut von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="f2fcd-117">Auf diese Weise stellen Sie sicher, dass die Kategorien verknüpft sind und keine Duplikate erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="f2fcd-118">In der Regel werden die Projektkostenkategorien in Finance beherrscht.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="f2fcd-119">Wenn dies jedoch nicht der Fall ist oder wenn in Project Service Automation bereits Ausgabenkategorien erstellt wurden, müssen Sie zunächst mithilfe der Vorlage Projektausgaben-Transaktionskategorien (PSA zu Fin und Ops) synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="f2fcd-120">Synchronisieren Sie anschließend mithilfe der Vorlage für Projektkostentransaktionskategorien (Fin und Ops zu PSA).</span><span class="sxs-lookup"><span data-stu-id="f2fcd-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="f2fcd-121">Anschließend sollten Sie die Synchronisierung von Project Service Automation zu Finance noch einmal ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="f2fcd-122">Wenn Sie zuerst über Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance erfüllt sein, bevor die Synchronisierung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="f2fcd-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="f2fcd-123">Die gemeinsam genutzte Kategorie, die der in Project Service Automation eingerichteten Projektkategorie entspricht, muss vorhanden sein und für **Projekt** und **Kosten** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="f2fcd-124">Für jede juristische Person im Finance, in die integriert werden muss, müssen die folgenden Projektkategorien vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="f2fcd-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="f2fcd-125">**Projektkategorie** existiert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="f2fcd-126">**Verwendung in Kosten** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="f2fcd-127">**Aktiv im Journal** ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="f2fcd-128">**Art der Transaktion** ist auf **Ausgaben** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="f2fcd-129">Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f2fcd-130">[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f2fcd-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="f2fcd-131">Synchronisieren Sie Projektausgabenkategorien von Finance zu Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f2fcd-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="f2fcd-132">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f2fcd-132">Template and task</span></span>

<span data-ttu-id="f2fcd-133">Um auf die Vorlage zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f2fcd-134">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Finance zu Project Service Automation zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="f2fcd-135">**Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (Fin und Ops zu PSA)</span><span class="sxs-lookup"><span data-stu-id="f2fcd-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="f2fcd-136">**Name der Aufgabe im Projekt:** Kategorien mit PSA synchronisieren</span><span class="sxs-lookup"><span data-stu-id="f2fcd-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="f2fcd-137">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="f2fcd-137">Entity set</span></span>

| <span data-ttu-id="f2fcd-138">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f2fcd-138">Finance</span></span>                           | <span data-ttu-id="f2fcd-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f2fcd-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="f2fcd-140">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="f2fcd-140">Integration entity for categories</span></span> | <span data-ttu-id="f2fcd-141">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="f2fcd-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="f2fcd-142">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="f2fcd-142">Entity flow</span></span>

<span data-ttu-id="f2fcd-143">Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f2fcd-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="f2fcd-144">Power Query</span></span>

<span data-ttu-id="f2fcd-145">Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel verwenden, um die Abrechnungsart für die Transaktionskategorie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="f2fcd-146">Die Vorlage Projektkosten-Transaktionskategorien (Fin und Ops zu PSA) enthält eine Standardspalte und -zuordnung.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="f2fcd-147">Wenn Sie eine eigene Vorlage erstellen, müssen Sie eine bedingte Spalte in Power Query hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="f2fcd-148">Führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-148">Follow these steps.</span></span>

1. <span data-ttu-id="f2fcd-149">Klicken Sie auf den Pfeil, um die Zuordnung der Aufgabe Projektausgabenkategorien in der Vorlage Projektausgaben-Transaktionskategorien (Fin und Ops zu PSA) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="f2fcd-150">Klicken Sie auf die Verknüpfung **Erweiterte Abfrage und Filterung**, um Power Query zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="f2fcd-151">Wählen Sie **Bedingte Spalte hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="f2fcd-152">Geben Sie einen Namen für die neue Spalte ein, wie **Abrechnungstyp**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="f2fcd-153">Geben Sie die folgende Bedingung ein: **Wenn CATEGORYID nicht gleich null ist, dann 19235001, andernfalls null**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="f2fcd-154">Klicken Sie in der Spalte auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="f2fcd-155">Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="f2fcd-156">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="f2fcd-157">Das Mapping zeigt die Feldinformationen an, die von Finance zu Project Service Automation synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="f2fcd-158">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f2fcd-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="f2fcd-159">Synchronisieren Sie Projektausgabenkategorien von Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="f2fcd-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="f2fcd-160">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="f2fcd-160">Template and task</span></span>

<span data-ttu-id="f2fcd-161">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Project Service Automation zu Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f2fcd-162">**Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="f2fcd-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f2fcd-163">**Name der Aufgabe im Projekt:** Kategorien zu Fin Ops synchronisieren</span><span class="sxs-lookup"><span data-stu-id="f2fcd-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="f2fcd-164">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="f2fcd-164">Entity set</span></span>

| <span data-ttu-id="f2fcd-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f2fcd-165">Project Service Automation</span></span> | <span data-ttu-id="f2fcd-166">Finanzen</span><span class="sxs-lookup"><span data-stu-id="f2fcd-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="f2fcd-167">Transaktionskategorien</span><span class="sxs-lookup"><span data-stu-id="f2fcd-167">Transaction categories</span></span>     | <span data-ttu-id="f2fcd-168">Integrationsentität für Kategorien</span><span class="sxs-lookup"><span data-stu-id="f2fcd-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="f2fcd-169">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="f2fcd-169">Entity flow</span></span>

<span data-ttu-id="f2fcd-170">Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="f2fcd-171">Die Synchronisation zurück zu Finance aktualisiert die Projektkostenkategorien in Finance mit der Integrations-ID von Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f2fcd-172">Vorlagenzuordnung in der Datenintegration</span><span class="sxs-lookup"><span data-stu-id="f2fcd-172">Template mapping in Data integration</span></span>

<span data-ttu-id="f2fcd-173">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="f2fcd-174">Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2fcd-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f2fcd-175">[![Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f2fcd-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
