---
title: Ressourcenkapazität synchronisieren
description: Dieses Thema enthält Informationen zum Synchronisieren der Kapazität einer Ressource über Kalender und Projekte hinweg.
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
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076502"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="1ab8c-103">Ressourcenkapazität synchronisieren</span><span class="sxs-lookup"><span data-stu-id="1ab8c-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ab8c-104">Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass Informationen für den Kalender und den Basiskalender in die Projektressourcenplanung einfließen.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="1ab8c-105">Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen an der Planung der Projektressourcen vor.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="1ab8c-106">Die Prozesse tragen auch zur Verbesserung der Leistung bei, da die Ressourceninformationen des Kalenders im Voraus synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="1ab8c-107">Daher werden Aktualisierungen der Ressourcenzeitplanungsinformationen schneller durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="1ab8c-108">Wir empfehlen, dass Sie die Prozesse als Stapel anstatt einzeln planen.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="1ab8c-109">Andernfalls besteht die Gefahr, dass jemand die Inklusivdaten vergisst, an denen die Informationen zuletzt synchronisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="1ab8c-110">Wenn keine Inklusivdaten verwendet werden, können während der Datumssynchronisierung Lücken auftreten.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendersynchronisation](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="1ab8c-112">Synchronisation der Rollup-Kapazität</span><span class="sxs-lookup"><span data-stu-id="1ab8c-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="1ab8c-113">Der Synchronisierungsprozess dient zum Synchronisieren aller Ressourcenkalenderinformationen.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="1ab8c-114">Diese Informationen enthalten Basiskalenderinformationen zu Änderungen an der Kapazitätstabelle des Ressourcenkalenders des Projekts.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="1ab8c-115">Wenn dem Projekt neue Ressourcen hinzugefügt werden, stellt die Synchronisierung sicher, dass die aktualisierten Kalenderinformationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="1ab8c-116">Diese Synchronisation kann jederzeit durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="1ab8c-117">Es wird empfohlen, dass Sie einen Batch verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-117">We recommend that you use a batch.</span></span> <span data-ttu-id="1ab8c-118">Die Optionen stehen während der Synchronisierung von Kapazitätsreservierungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="1ab8c-119">Wählen Sie **Projektmanagement und Buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisation** &gt; **Synchronisieren Sie Rollups der Ressourcenkapazität**.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="1ab8c-120">Legen Sie die Optionen in der nachfolgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="1ab8c-121">Option</span><span class="sxs-lookup"><span data-stu-id="1ab8c-121">Option</span></span>      | <span data-ttu-id="1ab8c-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ab8c-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="1ab8c-123">Periodencode</span><span class="sxs-lookup"><span data-stu-id="1ab8c-123">Period code</span></span> | <span data-ttu-id="1ab8c-124">Wählen Sie optional den Intervallcode für das Hauptbuchdatum aus, um das Start- und Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="1ab8c-125">Startdatum</span><span class="sxs-lookup"><span data-stu-id="1ab8c-125">Start date</span></span>  | <span data-ttu-id="1ab8c-126">Geben Sie das Startdatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="1ab8c-127">Enddatum</span><span class="sxs-lookup"><span data-stu-id="1ab8c-127">End date</span></span>    | <span data-ttu-id="1ab8c-128">Geben Sie das Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein.</span><span class="sxs-lookup"><span data-stu-id="1ab8c-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="1ab8c-129">[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="1ab8c-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
