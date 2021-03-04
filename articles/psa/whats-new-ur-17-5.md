---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 17.5, Hotfix, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 17.5, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd4142176258820f4718f457ca8610f19f584a32
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143710"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="2952c-103">Project Service Automation Update Release 17.5, V3</span><span class="sxs-lookup"><span data-stu-id="2952c-103">Project Service Automation Update Release 17.5, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2952c-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="2952c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2952c-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="2952c-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="2952c-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2952c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2952c-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2952c-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2952c-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2952c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2952c-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 17.5 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2952c-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="2952c-110">Diese Version hat eine Build-Nummer von V3.10.7.32 und ist durch eine Selbstaktualisierung im März 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2952c-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="2952c-111">Update Release 17.5</span><span class="sxs-lookup"><span data-stu-id="2952c-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2952c-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="2952c-112">Bug fixes</span></span>


<span data-ttu-id="2952c-113">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="2952c-113">**Project Management**</span></span>

- <span data-ttu-id="2952c-114">Behoben: Behobene serverseitige Synchronisationsprobleme, die bei Aufgaben mit langer Dauer auftreten.</span><span class="sxs-lookup"><span data-stu-id="2952c-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="2952c-115">Behoben: Adressierte 24-Stunden-Arbeitsstundenvorlagen fügten Aufgaben ungenau einen zusätzlichen Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="2952c-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="2952c-116">Behoben: Adressierte +13 GMT-Arbeitsstundenvorlagen, die Aufgaben einen Tag im Voraus ungenau verschieben.</span><span class="sxs-lookup"><span data-stu-id="2952c-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

