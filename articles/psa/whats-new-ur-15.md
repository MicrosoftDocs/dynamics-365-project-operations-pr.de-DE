---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 15, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 15, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076481"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="cdd90-103">Project Service Automation Update Release 15, V3</span><span class="sxs-lookup"><span data-stu-id="cdd90-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="cdd90-104">Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben.</span><span class="sxs-lookup"><span data-stu-id="cdd90-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="cdd90-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="cdd90-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cdd90-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cdd90-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cdd90-107">Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cdd90-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="cdd90-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cdd90-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cdd90-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 15 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdd90-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="cdd90-110">Diese Version hat eine Build-Nummer von V3.10.5.28 und ist im durch ein Selbst-Update im Januar 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cdd90-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="cdd90-111">Update Release 15</span><span class="sxs-lookup"><span data-stu-id="cdd90-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="cdd90-112">Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="cdd90-112">Enhancements</span></span>

- <span data-ttu-id="cdd90-113">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="cdd90-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cdd90-114">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="cdd90-114">Bug fixes</span></span>

- <span data-ttu-id="cdd90-115">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdd90-115">Time and Expense</span></span>

  - <span data-ttu-id="cdd90-116">Behoben: Fehlerbehandlung beim Laden in der Abstimmungsansicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cdd90-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="cdd90-117">Behoben: Project Resource Hub: Umbenennen von **Menge** , um Mehrdeutigkeit zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="cdd90-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="cdd90-118">Behoben: Passen Sie die Ansicht an **Zeiteintragsspalten kopieren** , um den Typ einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cdd90-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="cdd90-119">Behoben: Das Bearbeiten der Zeiteintragsdauer in der Rasteransicht unter Verwendung von Dezimalzahlen führt bei einigen Zahlen zu einem unbekannten Fehler.</span><span class="sxs-lookup"><span data-stu-id="cdd90-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="cdd90-120">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="cdd90-120">Project Management</span></span>

  - <span data-ttu-id="cdd90-121">Behoben: Das Dropdown-Menü für **In der Verfolgungsansicht verwenden** erweitert sich nun basierend auf der Breite der Optionen.</span><span class="sxs-lookup"><span data-stu-id="cdd90-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="cdd90-122">Behoben: Beim Verwalten von Projekten in der Zeitzone +13 können Aufgabenberechnungen zu ungenauen Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="cdd90-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="cdd90-123">Behoben: **Endzeit des Teammitglieds** wurde bei Verwendung eines 24-Stunden-Kalenders korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cdd90-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="cdd90-124">Behoben: **BPF** im **msdyn_project** Hauptformular wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cdd90-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="cdd90-125">Behoben: Zuweisungsberechnung ignoriert einen Tag nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="cdd90-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="cdd90-126">Behoben: Ein neues Benachrichtigungsbanner wurde zum Projektformular hinzugefügt, wenn sich die Zeitzone zwischen Benutzer und Projekt unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="cdd90-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="cdd90-127">Sales</span><span class="sxs-lookup"><span data-stu-id="cdd90-127">Sales</span></span>

  - <span data-ttu-id="cdd90-128">Behoben: Die Suche nach Ausgabenschätzungskategorien kann zum Filtern von Duplikaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdd90-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="cdd90-129">Behoben: Code in **PluginDomain.ExecuteInTryCatchBlock (..)** verbirgt nicht länger den Ursprung der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="cdd90-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="cdd90-130">Behoben: Es wird keine Fehlermeldung mehr angezeigt in **Projektsuche** in der **Angebotszeile** , wenn es mehr als 1000 Projekte gibt.</span><span class="sxs-lookup"><span data-stu-id="cdd90-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="cdd90-131">Behoben: Raster **Schätzungen** für Arbeitsschätzungen und Ausgabenschätzungen zeigt jetzt das richtige Währungssymbol an.</span><span class="sxs-lookup"><span data-stu-id="cdd90-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="cdd90-132">Behoben: Nachdem eine Organisation PSA von Update Release 14 auf Update Release 15 aktualisiert hat, wird die **Zeitplan** Registerkarte nicht mehr als leer auf dem Formular **Projekt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cdd90-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
