---
title: Planungsleistung für Projektressourcen
description: Dieses Thema enthält Informationen zur Verbesserung der Leistung der Ressourcenplanung für eine große Anzahl von Projekten.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289008"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="d1ec4-103">Planungsleistung für Projektressourcen</span><span class="sxs-lookup"><span data-stu-id="d1ec4-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="d1ec4-104">Leistungsprobleme im Zusammenhang mit der Ressourcenplanung können auftreten, wenn die Anzahl der Projekte in die Tausende geht.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="d1ec4-105">Um die Leistung der Ressourcenplanung zu verbessern, steht eine Funktion zur Verfügung, mit der Benutzer die Zeit reduzieren können, die zum Starten des Ressourcenverfügbarkeitsformulars erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="d1ec4-106">Dies entfernt insbesondere den Rollup-Synchronisierungsprozess für die Ressourcenkapazität und verwendet die Tabelle **ResProjectResource**, um die Ressourcensuche zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="d1ec4-107">Beachten Sie, dass die Tabelle **ResRollup** nicht länger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1ec4-108">Wenn eine Abhängigkeit entweder vom Rollup-Synchronisierungsprozess der Ressourcenkapazität oder von der Tabelle **ResProjectResource** besteht, verwenden Sie diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d1ec4-109">Leistungsverbesserung bei der Ressourcenplanung aktivieren</span><span class="sxs-lookup"><span data-stu-id="d1ec4-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="d1ec4-110">Führen Sie die folgenden Schritte aus, um die Leistungsverbesserung bei der Ressourcenplanung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="d1ec4-111">Navigieren Sie zu **Funktionsverwaltung** > **Alle**, und suchen Sie in der Funktionsliste **Funktion zur Leistungsverbesserung der Ressourcenplanung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d1ec4-112">Wählen Sie **Jetzt aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="d1ec4-113">Wenn Sie die Funktion in der Liste nicht finden können, wählen Sie **Auf Updates prüfen** aus, um die Liste zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="d1ec4-114">Aktualisieren Sie Ihren Browser, und navigieren Sie dann zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Projektressourcen** > **Kapazität der Ressourcenkalender in allen Unternehmen synchronisieren**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="d1ec4-115">Legen Sie **Vorhandene Kapazitätssätze entfernen** auf **Ja** fest, um vorherige Daten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d1ec4-116">Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="d1ec4-117">Wählen Sie im Feld **Periodencode** die Periode aus, in der die Daten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d1ec4-118">Wenn Sie einen Periodencode auswählen, müssen Sie kein Start- und Enddatum definieren.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="d1ec4-119">Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie die entsprechenden Start- und Enddaten zum Generieren von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="d1ec4-120">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d1ec4-121">Dadurch werden allgemeine Daten an die Tabelle **ResCalendarCapacity** für alle Unternehmen in Ihrer Umgebung verteilt, sodass der Batchauftrag nur in einer juristischen Person ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d1ec4-122">Die Daten in diesem Batchauftrag werden benötigt, um die Ressourcenkapazität über den zugehörigen Kalender zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="d1ec4-123">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Projektressourcen** > **Projektressourcen in allen Unternehmen ausfüllen**, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="d1ec4-124">Dies ist das Datenaktualisierungsskript für allgemeine Daten in den Tabellen **ResProjectResource**, **ResCalendarDateTimeRange** und **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="d1ec4-125">Werte für die Felder **PSAPRojSchedRole.RootActivity** werden ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="d1ec4-126">Wenn dies nicht ausgeführt wird, erhalten Sie eine Warnung, wenn Sie versuchen, Ressourcenplanungsvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d1ec4-127">Leistungsverbesserung bei der Ressourcenplanung deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d1ec4-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="d1ec4-128">Navigieren Sie zu **Funktionsverwaltung** > **Alle**, und suchen Sie nach **Funktion zur Leistungsverbesserung der Ressourcenplanung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d1ec4-129">Wählen Sie die Funktion und dann die Schaltfläche **Deaktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="d1ec4-130">Aktualisieren Sie Ihren Browser.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-130">Refresh your browser.</span></span>
4. <span data-ttu-id="d1ec4-131">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Periodisch** > **Kapazitätssynchronisierung** > **Synchronisation der Rollup-Kapazität**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="d1ec4-132">Legen Sie auf der Seite **Synchronisation der Rollup-Kapazität** die Option **Vorhandene Kapazitätssätze entfernen** auf **Ja** fest, um die vorherigen Daten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d1ec4-133">Wenn Sie inkrementelle Daten generieren möchten, legen Sie diese auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="d1ec4-134">Wählen Sie im Feld **Periodencode** die Periode aus, in der die Daten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d1ec4-135">Wenn Sie einen Periodencode auswählen, müssen Sie kein Start- und Enddatum definieren.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="d1ec4-136">Wenn Sie das Feld **Periodencode** leer lassen, wählen Sie die entsprechenden Start- und Enddaten zum Generieren von Daten aus.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="d1ec4-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d1ec4-138">Dadurch werden allgemeine Daten an die Tabelle **ResRollup** für alle Unternehmen in Ihrer Umgebung verteilt, sodass der Batchauftrag nur in einer juristischen Person ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d1ec4-139">Dieser Batchauftrag ist für alle **Ressourcenverfügbarkeits**-Ansichten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="d1ec4-140">Wenn dieser Batchauftrag nicht ausgeführt wird, werden die **ResRollup**-Daten während der Bearbeitung generiert, was einige Zeit dauern kann.</span><span class="sxs-lookup"><span data-stu-id="d1ec4-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]