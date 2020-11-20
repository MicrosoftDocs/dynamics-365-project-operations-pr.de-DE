---
title: Berechnete Kosten bei Abschluss aktualisieren
description: Dieses Thema enthält Informationen zum Aktualisieren der Projektion des Aufwands für ein Projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127202"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="e57de-103">Berechnete Kosten bei Abschluss aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e57de-103">Update estimate at completion</span></span>

<span data-ttu-id="e57de-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="e57de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e57de-105">Es ist üblich, das ein Projektmanager die ursprünglichen Vorkalkulationen für eine Aufgabe erneut überprüft.</span><span class="sxs-lookup"><span data-stu-id="e57de-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e57de-106">Erneute Hochrechnungen für ein Projekt spiegeln die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider.</span><span class="sxs-lookup"><span data-stu-id="e57de-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e57de-107">Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern, da die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.</span><span class="sxs-lookup"><span data-stu-id="e57de-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e57de-108">Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für Aufgaben durchführen kann:</span><span class="sxs-lookup"><span data-stu-id="e57de-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e57de-109">Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="e57de-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e57de-110">Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="e57de-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e57de-111">Jeder dieser Ansätze führt zu einer Neuberechnung der ETC, der Schätzung von EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="e57de-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e57de-112">Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden auch neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.</span><span class="sxs-lookup"><span data-stu-id="e57de-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
