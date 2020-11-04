---
title: Projektvertriebsaufträge für Zeit- und Materialprojekte
description: In diesem Thema wird erläutert, wie projektbasierte Kundenaufträge für Zeit- und Materialprojekte erstellt werden.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
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
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076509"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="7bab6-103">Projektvertriebsaufträge für Zeit- und Materialprojekte</span><span class="sxs-lookup"><span data-stu-id="7bab6-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7bab6-104">In diesem Thema wird beschrieben, wie Sie einen Vertriebsauftrag für ein Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="7bab6-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="7bab6-105">Vertriebsaufträge können nur für Projekte vom Typ **Zeit und Material** erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7bab6-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="7bab6-106">Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag enthält, müssen Sie die Option aktivieren Parameter **Vertriebsaufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="7bab6-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="7bab6-107">Die Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist ab Anwendungsversion 10.0.2 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bab6-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="7bab6-108">Der Parameter zum Aktivieren der Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen wird in der Release-Welle vom April 2020 entfernt. Danach wird die Funktionalität immer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7bab6-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="7bab6-109">Sie können projektbasierte Kundenaufträge auf zwei Arten erstellen:</span><span class="sxs-lookup"><span data-stu-id="7bab6-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="7bab6-110">Gehen Sie zum Projekt selber.</span><span class="sxs-lookup"><span data-stu-id="7bab6-110">Go to the project itself.</span></span> <span data-ttu-id="7bab6-111">Wählen Sie im Aktionsbereich **Verwalten > Artikelaufgabe > Vertriebsauftrag** aus.</span><span class="sxs-lookup"><span data-stu-id="7bab6-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="7bab6-112">Die Projektinformationen beziehen sich standardmäßig auf den Kundenauftrag aus dem Projekt.</span><span class="sxs-lookup"><span data-stu-id="7bab6-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="7bab6-113">Wenn der Projektvertrag mehr als eine Finanzierungsquelle enthält, müssen Sie die Finanzierungsquelle auswählen, um den Kunden für den Kundenauftrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7bab6-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="7bab6-114">Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Kunde automatisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7bab6-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="7bab6-115">Gehen Sie zu Listenseite **Alle Vertriebsaufträge** und erstellen Sie einen neuen Vertriebsauftrag.</span><span class="sxs-lookup"><span data-stu-id="7bab6-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="7bab6-116">Sie müssen das Projekt für den Vertriebsauftrag auswählen.</span><span class="sxs-lookup"><span data-stu-id="7bab6-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="7bab6-117">Nachdem das Projekt ausgewählt wurde, wird der Kunde aus der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen enthält.</span><span class="sxs-lookup"><span data-stu-id="7bab6-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>
