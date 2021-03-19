---
title: Synchronisieren Sie Projektaufgaben direkt von Project Service Automation zu Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektaufgaben zwischen Microsoft Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288918"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="63f56-103">Synchronisieren Sie Projektaufgaben direkt von Project Service Automation zu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63f56-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="63f56-104">Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektaufgaben zwischen Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63f56-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="63f56-105">Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63f56-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="63f56-106">Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="63f56-107">Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch die Wissensdatenbank 4131710 installieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="63f56-108">Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63f56-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="63f56-109">Datenfluss für Project Service Automation zu Finance</span><span class="sxs-lookup"><span data-stu-id="63f56-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="63f56-110">Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="63f56-111">Die Integrationsvorlage, die mit der Datenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss über Projektkosten-Transaktionskategorien von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="63f56-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="63f56-112">Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="63f56-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="63f56-113">[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="63f56-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="63f56-114">Vorlage und Aufgabe</span><span class="sxs-lookup"><span data-stu-id="63f56-114">Template and task</span></span>

<span data-ttu-id="63f56-115">Um auf die Vorlage zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="63f56-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="63f56-116">Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projektaufgaben zwischen Project Service Automation und Finance zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="63f56-117">**Name der Vorlage in der Datenintegration:** Projektaufgaben (PSA zu Fin und Ops)</span><span class="sxs-lookup"><span data-stu-id="63f56-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="63f56-118">**Name der Aufgabe im Projekt:** Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="63f56-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="63f56-119">Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="63f56-120">Entität festgelegt</span><span class="sxs-lookup"><span data-stu-id="63f56-120">Entity set</span></span>

| <span data-ttu-id="63f56-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="63f56-121">Project Service Automation</span></span> | <span data-ttu-id="63f56-122">Finanzen</span><span class="sxs-lookup"><span data-stu-id="63f56-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="63f56-123">Projektaufgaben</span><span class="sxs-lookup"><span data-stu-id="63f56-123">Project Tasks</span></span>              | <span data-ttu-id="63f56-124">Integrationsentität für Projektaufgabe</span><span class="sxs-lookup"><span data-stu-id="63f56-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="63f56-125">Entitätsfluss</span><span class="sxs-lookup"><span data-stu-id="63f56-125">Entity flow</span></span>

<span data-ttu-id="63f56-126">Projektaufgaben werden in Project Service Automation verwaltet und als Projektaktivitäten mit Finance synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="63f56-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="63f56-127">Voraussetzungen und Mappingeinrichtung</span><span class="sxs-lookup"><span data-stu-id="63f56-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="63f56-128">Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Projektverträge und Projekte synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="63f56-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="63f56-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="63f56-129">Power Query</span></span>

<span data-ttu-id="63f56-130">Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn diese Bedingung erfüllt ist:</span><span class="sxs-lookup"><span data-stu-id="63f56-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="63f56-131">Sie haben ressourcenspezifische Datensätze in einer Projektaufgabe.</span><span class="sxs-lookup"><span data-stu-id="63f56-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="63f56-132">Wenn Sie Power Query verwenden müssen, befolgen Sie diese Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="63f56-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="63f56-133">Die Vorlage Projektaufgaben (PSA zu Fin und Ops) verfügt über einen Standardfilter, der ressourcenspezifische Datensätze von einer Projektaufgabe ausschließt, indem der Filter im **IsLineTask** auf **Falsch** gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="63f56-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="63f56-134">Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="63f56-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="63f56-135">Vorlagenzuordnung in der Datenintegration</span><span class="sxs-lookup"><span data-stu-id="63f56-135">Template mapping in Data integration</span></span>

<span data-ttu-id="63f56-136">Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.</span><span class="sxs-lookup"><span data-stu-id="63f56-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="63f56-137">Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="63f56-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="63f56-138">[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="63f56-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]