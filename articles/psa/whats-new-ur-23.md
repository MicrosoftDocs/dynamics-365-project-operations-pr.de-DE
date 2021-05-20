---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 23, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 23, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948958"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="a5e50-103">Project Service Automation Update Release 23, V3</span><span class="sxs-lookup"><span data-stu-id="a5e50-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a5e50-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="a5e50-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a5e50-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="a5e50-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a5e50-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a5e50-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a5e50-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a5e50-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a5e50-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a5e50-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a5e50-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 23 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5e50-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="a5e50-110">Diese Version hat eine Build-Nummer von V 3.10.34.30 und ist durch ein Selbst-Update im August 2020 allgemein verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a5e50-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="a5e50-111">Update Release 23</span><span class="sxs-lookup"><span data-stu-id="a5e50-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a5e50-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="a5e50-112">Bug fixes</span></span>

<span data-ttu-id="a5e50-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="a5e50-113">**Time and Expense**</span></span>

<span data-ttu-id="a5e50-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="a5e50-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="a5e50-115">Edge-Anfrage in **Projektteammitglied löschen** bearbeiten, um eine sinnvolle Ausnahme zu machen.</span><span class="sxs-lookup"><span data-stu-id="a5e50-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="a5e50-116">Der Import von Zuweisungen führt zu einem leeren Bildschirm zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="a5e50-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="a5e50-117">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="a5e50-117">**Resource Management**</span></span>

<span data-ttu-id="a5e50-118">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="a5e50-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a5e50-119">**Ressourcennutzungsraster-Ressourcenkarte** zeigt falsche Daten an, wenn die Zeitskala mehr als fünf Tage beträgt.</span><span class="sxs-lookup"><span data-stu-id="a5e50-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="a5e50-120">Wenn Kunden eine buchbare Ressource erstellen, fügt das Plug-In die Ressource zeitweise nicht automatisch zu einer Microsoft Office 365-Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5e50-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="a5e50-121">Die Ansicht **Abstimmung** zeigt manuelle Konturen in der Ansicht **Woche** oder **Monat** falsch an.</span><span class="sxs-lookup"><span data-stu-id="a5e50-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="a5e50-122">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="a5e50-122">**Project Management**</span></span>

<span data-ttu-id="a5e50-123">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="a5e50-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a5e50-124">Eine übermäßige Anzahl von **RetrieveMultiple für Benutzereinstellungen**-Entitäten verursachen Leistungseinbußen bei Projektgenehmigungen und anderen Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="a5e50-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="a5e50-125">Die **Aufgabenplanung**-Rasterressourcensuche ist auf nur bis zu fünf Teammitglieder aus dem Projektteam beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a5e50-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="a5e50-126">Die **Aufgabenplanung**-Rasterressourcensuche filtert keine inaktiven Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a5e50-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="a5e50-127">Der manuelle Modus funktioniert nicht wie erwartet in der Projektplanungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="a5e50-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="a5e50-128">Das Raster **Aufgabenplanung** zeigt **Inaktive Transaktionskategorien**.</span><span class="sxs-lookup"><span data-stu-id="a5e50-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="a5e50-129">Das Raster **Ressourcenzuweisung** wird falsch gerundet, wenn eine Aufgabe mehrere Zuordnungen hat.</span><span class="sxs-lookup"><span data-stu-id="a5e50-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="a5e50-130">Rundungswerte unterscheiden sich zwischen geplanten Kosten und tatsächlichen Kosten für eine einzelne Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a5e50-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="a5e50-131">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="a5e50-131">**Sales**</span></span>

<span data-ttu-id="a5e50-132">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="a5e50-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="a5e50-133">Durch Doppelklicken auf **Alle Transaktionskategorien abrufen** werden mehrere Zeilen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5e50-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]