---
title: Leistung von Projektrechnungsvorschlägen
description: Dieses Thema enthält Informationen zu Leistungsverbesserungen bei Projektrechnungsvorschlägen.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920301"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="301bf-103">Leistung von Projektrechnungsvorschlägen</span><span class="sxs-lookup"><span data-stu-id="301bf-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="301bf-104">Wenn Sie einen neuen Rechnungsvorschlag erstellen, können Leistungsprobleme auftreten, wenn die Anzahl der Projekte und Teilprojekte zunimmt.</span><span class="sxs-lookup"><span data-stu-id="301bf-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="301bf-105">Um die Leistung zu verbessern, steht eine Funktion zur Verfügung, die den Zeitaufwand für die Erstellung eines neuen Rechnungsvorschlags für gebuchte Projekttransaktionen verkürzt.</span><span class="sxs-lookup"><span data-stu-id="301bf-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="301bf-106">Leistungsverbesserung von Projektrechnungsvorschlägen aktivieren</span><span class="sxs-lookup"><span data-stu-id="301bf-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="301bf-107">Führen Sie die folgenden Schritte aus, um die Leistungsverbesserungsfunktion für Projektrechnungsvorschläge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="301bf-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="301bf-108">Gehen Sie zu **Funktionsverwaltung** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="301bf-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="301bf-109">Suchen Sie in der Funktionsliste nach **Leistungsverbesserung von Projektrechnungsvorschlägen**.</span><span class="sxs-lookup"><span data-stu-id="301bf-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="301bf-110">Wählen Sie **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="301bf-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="301bf-111">Aktualisieren Sie Ihren Browser und erstellen Sie einen neuen Rechnungsvorschlag.</span><span class="sxs-lookup"><span data-stu-id="301bf-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="301bf-112">Leistungsverbesserung von Projektrechnungsvorschlägen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="301bf-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="301bf-113">Führen Sie die folgenden Schritte aus, um die Leistungsverbesserungsfunktion für Projektrechnungsvorschläge zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="301bf-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="301bf-114">Gehen Sie zu **Funktionsverwaltung** > **Alle**.</span><span class="sxs-lookup"><span data-stu-id="301bf-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="301bf-115">Suchen Sie in der Funktionsliste nach **Leistungsverbesserung von Projektrechnungsvorschlägen**.</span><span class="sxs-lookup"><span data-stu-id="301bf-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="301bf-116">Wählen Sie **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="301bf-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="301bf-117">Aktualisieren Sie Ihren Browser.</span><span class="sxs-lookup"><span data-stu-id="301bf-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="301bf-118">Die Leistung von Rechnungsvorschlägen kann nicht angewendet werden, wenn Abrechnungsregeln aktiviert sind oder Stapelprozesse ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="301bf-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
