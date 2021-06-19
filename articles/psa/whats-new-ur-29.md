---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 29, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 29, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010470"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="cc9c1-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 29, V3</span><span class="sxs-lookup"><span data-stu-id="cc9c1-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc9c1-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc9c1-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc9c1-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc9c1-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc9c1-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc9c1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc9c1-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 29 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="cc9c1-110">Diese Version hat die Build-Nummer V3.10.47.7 und ist im Allgemeinen über ein Selbstupdate im Februar 2021 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="cc9c1-111">Update Release 29</span><span class="sxs-lookup"><span data-stu-id="cc9c1-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc9c1-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="cc9c1-112">Bug fixes</span></span>

<span data-ttu-id="cc9c1-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="cc9c1-113">**Time and Expense**</span></span>

<span data-ttu-id="cc9c1-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cc9c1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc9c1-115">Benutzer sehen keine Arbeitsstunden, die an arbeitsfreien Tagen im Zeiteintragsraster protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="cc9c1-116">Genehmigte Speseneinträge können im Raster bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="cc9c1-117">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="cc9c1-117">**Project Management**</span></span>

<span data-ttu-id="cc9c1-118">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cc9c1-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc9c1-119">Fehlende Validierungslogik, um sicherzustellen, dass die Aufwandsstunden für die Ressourcenzuweisung nicht negativ sind.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="cc9c1-120">Die benutzerdefinierte Aktion **AssignResourcesForTask** aktualisiert alle Felder anstatt nur geänderter Felder.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="cc9c1-121">Beim Kopieren eines Projekts in einer Umgebung mit Plug-Ins oder Workflows, die im **CreateProject**-Ereignis registriert sind, wird das Attribut **msdyn_bulkgenerationstatus** nicht aktualisiert, wenn **CopyWBSToProject** fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="cc9c1-122">Wenn Sie den Projektkalender erweitern, werden die Arbeitstage nicht in aufsteigender Reihenfolge sortiert, was dazu führt, dass einige Aktualisierungen von Projektaufgaben fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="cc9c1-123">Das Ändern des Projektmanagers für ein vorhandenes Projekt löst die Standardlogik der Organisationseinheit aus.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="cc9c1-124">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="cc9c1-124">**Sales**</span></span>

<span data-ttu-id="cc9c1-125">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cc9c1-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc9c1-126">Die Registerkarte **Vertragsleistung** auf der Seite **Vertrag** schlägt während der Initialisierung stillschweigend fehl, wenn keine Vertragspositionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cc9c1-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>