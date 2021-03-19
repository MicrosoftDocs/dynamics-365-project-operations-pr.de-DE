---
title: Übersicht Project Service Automation
description: Dieses Thema bietet Informationen über die Dynamics 365 Project Service Automation zu Dynamics 365 Finance Integrationslösung.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d2eace497f4291022da0775cca7cda7d600df7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271082"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="57b19-103">Übersicht Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="57b19-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="57b19-104">Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Dynamics 365 Finance und Dynamics 365 Project Service Automation über Common Data Service zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="57b19-105">Die Integrationsvorlage, die mit der Datenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss über Projektverträge, Projekte, Projekt-Vertragszeilen und Projekt-Vertragszeilen-Meilensteine, Projektaufgaben Ausgabetransaktionskategorien, Stundenschätzungen und Ausgabenschätzungen von Project Service Automation zu Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="57b19-106">Wenn Sie Version 7.3.0 verwenden, müssen Sie die Wissensdatenbank 4074835 installieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="57b19-107">Sie können dann Festpreisprojekte integrieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="57b19-108">Wenn Sie Version 7.3.0 verwenden und Gebührentransaktionen von Project Service Automation zu übertragen, müssen Sie die Wissensdatenbank 4345320 installieren, um diese Gebühren in die Projektrechnung aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="57b19-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="57b19-109">Wenn Sie Version 8.0 verwenden, können Sie Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren verwenden.</span><span class="sxs-lookup"><span data-stu-id="57b19-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="57b19-110">Wenn Sie Version 8.0.1 oder höher verwenden, können Sie die Istdaten synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="57b19-111">Bevor Sie Project Service Automation Finance integrieren können, müssen Sie die Integrationsparameter von Project Service Automation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="57b19-112">Weitere Informationen finden Sie unter [Integrationsparameter für Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="57b19-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="57b19-113">Diese Integrationslösung ermöglicht die direkte Synchronisation in den folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="57b19-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="57b19-114">Verwalten Sie Projektverträge in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-115">Erstellen Sie Projekte in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-116">Verwalten Sie Projektvertragszeilen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-117">Verwalten Sie Projektvertragszeilen-Meilensteine in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-118">Verwalten Sie Projektaufträge in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-119">Verwalten Sie Ausgabentransaktionskategorien in Finance und synchronisieren Sie sie direkt von Finance zu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="57b19-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="57b19-120">Erstellen Sie Projektstundenschätzungen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-121">Erstellen Sie Projektausgabenschätzungen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.</span><span class="sxs-lookup"><span data-stu-id="57b19-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="57b19-122">Erstellen Sie Projektzeit, Ausgaben und tatsächliche Gebühren in Project Service Automation und erstellen Sie Projekttransaktionen im Project Service Automation-Integrationsjournal, damit sie in Finance gebucht werden können.</span><span class="sxs-lookup"><span data-stu-id="57b19-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="57b19-123">Datensynchronisierung</span><span class="sxs-lookup"><span data-stu-id="57b19-123">Data synchronization</span></span>

<span data-ttu-id="57b19-124">Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance als Teil der Integration synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="57b19-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="57b19-125">Derzeit sind nicht alle Vorlagen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57b19-125">Not all templates are currently available.</span></span> <span data-ttu-id="57b19-126">Vorlagen werden veröffentlicht, sobald sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="57b19-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="57b19-127">[![Project Service Automation Integration mit Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="57b19-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="57b19-128">Systemanforderungen für Finanzen</span><span class="sxs-lookup"><span data-stu-id="57b19-128">System requirements for Finance</span></span>

<span data-ttu-id="57b19-129">Um die Integrationslösung Project Service Automation zu Finance verwenden zu können, müssen Sie Enterprise Edition 7.3 mit Platform Update 12 oder höher installieren.</span><span class="sxs-lookup"><span data-stu-id="57b19-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="57b19-130">Systemanforderungen für Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="57b19-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="57b19-131">Um die Integrationslösung Project Service Automation zu Finance verwenden zu können, müssen Sie die folgenden Komponenten installieren:</span><span class="sxs-lookup"><span data-stu-id="57b19-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="57b19-132">Dynamics 365 Project Service Automation Version 9.0.0.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="57b19-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="57b19-133">Aussicht auf Bargeldlösung für Dynamics 365 Sales, Version 1.14.0.0 (v14) oder höher</span><span class="sxs-lookup"><span data-stu-id="57b19-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="57b19-134">Project Service Automation zu Finance-Lösung für Dynamics 365 Project Service Automation Version 1.0.0.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="57b19-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="57b19-135">Installieren Sie Project Service Automation zu Finance Integrationslösung in Ihre Project Service Automation-Instanz</span><span class="sxs-lookup"><span data-stu-id="57b19-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="57b19-136">Laden Sie die Integrationslösung Project Service Automation zu Finance vom [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) herunter und befolgen Sie die Anweisungen, die der Lösung beiliegen.</span><span class="sxs-lookup"><span data-stu-id="57b19-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]