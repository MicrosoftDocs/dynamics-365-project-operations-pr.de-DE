---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 27, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 27, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 8879229b50ef113d6d6cb8622b707f0c12182a57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280307"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a><span data-ttu-id="2cd1b-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 27, V3</span><span class="sxs-lookup"><span data-stu-id="2cd1b-103">What's new or changed in Project Service Automation Update Release 27, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2cd1b-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2cd1b-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2cd1b-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2cd1b-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2cd1b-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2cd1b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2cd1b-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 27 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 27.</span></span> <span data-ttu-id="2cd1b-110">Diese Version hat eine Build-Nummer von V3.10.45.98 und ist im durch ein Selbst-Update im Januar 2021 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-27"></a><span data-ttu-id="2cd1b-111">Update Release 27</span><span class="sxs-lookup"><span data-stu-id="2cd1b-111">Update Release 27</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2cd1b-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="2cd1b-112">Bug fixes</span></span>

<span data-ttu-id="2cd1b-113">**Allgemein**</span><span class="sxs-lookup"><span data-stu-id="2cd1b-113">**General**</span></span>

<span data-ttu-id="2cd1b-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2cd1b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2cd1b-115">Von Plug-Ins in Project Service Automation generierte Protokolle wurden nicht auf automatisches Löschen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-115">Logs generated by plug-ins in Project Service Automation haven't been set to auto-delete.</span></span>
- <span data-ttu-id="2cd1b-116">Die automatische Aktualisierung schlägt fehl, da die Project Service Automation-Lösung ein Legacy-Null-NavBarArea- und -Titelelement enthält.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-116">Auto-upgrade fails because the Project Service Automation solution contains a legacy null NavBarArea and title element.</span></span>

<span data-ttu-id="2cd1b-117">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="2cd1b-117">**Time and Expense**</span></span>

<span data-ttu-id="2cd1b-118">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2cd1b-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="2cd1b-119">Der Raster **Zeiteintrag** zeigt falsche Daten für **TimeZone Independent** Datumsverhalten.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-119">The **Time Entry** grid displays incorrect data for **TimeZone Independent** date behavior.</span></span>
- <span data-ttu-id="2cd1b-120">Der Raster **Zeiteintrag** erstellt falsche Zeit für **TimeZone Independent** Datumsverhalten.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-120">The **Time Entry** grid creates incorrect time for **TimeZone Independent** date behavior.</span></span>
- <span data-ttu-id="2cd1b-121">Die Aufgabensuche ist nicht auf das ausgewählte Projekt auf der Seite **Zeiteintrag bearbeiten** beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-121">Task lookup isn't limited to the selected project on the **Edit Time Entry** page.</span></span>
- <span data-ttu-id="2cd1b-122">Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts ist blockiert, da das System nach einem  Projektgenehmiger sucht.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-122">Time approval for non-project time entries is blocked because the system is looking for a project approver.</span></span>
- <span data-ttu-id="2cd1b-123">Bei korrekten Einträgen in tatsächlichen Transaktionen wird eine falsche Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-123">Correct entries on Actuals displays an incorrect error message.</span></span>
- <span data-ttu-id="2cd1b-124">Wenn eine Aufgabe einen Nullwert für die tatsächlichen Kosten enthält und die Projektsummen aktualisiert werden, tritt der folgende Fehler auf: Gegebener Schlüssel nicht im Wörterbuch vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-124">When a task contains a null value for actual cost and the project totals are refreshed, the following error occurs, "Given key not present in dictionary".</span></span>
- <span data-ttu-id="2cd1b-125">In bestimmten Fällen zeigen die Filter **Gruppiere nach** auf der Registerkarte **Projektschätzung** keine Kostenvoranschläge an.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-125">In specific instances, **Group By** filters on the **Project Estimate** tab does not display expense estimates.</span></span>
- <span data-ttu-id="2cd1b-126">**Sommerzeit** Intervall ist für Zeiteinträge nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-126">**Daylight Saving Time** interval isn't correct for time entries.</span></span>

<span data-ttu-id="2cd1b-127">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="2cd1b-127">**Project Management**</span></span>

<span data-ttu-id="2cd1b-128">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2cd1b-128">The following issues have been fixed:</span></span>

- <span data-ttu-id="2cd1b-129">Caching-Verbesserungen, die die Leistung beim Laden der Seite **Projekt** verbessern.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-129">Caching improvements, which enhances performance related to loading the **Project** page.</span></span>
- <span data-ttu-id="2cd1b-130">Veraltete Geschäftsregel, die verhindert, dass Projektaufgaben erledigt werden.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-130">Obsolete business rule preventing project tasks from being completed.</span></span>
- <span data-ttu-id="2cd1b-131">Microsoft Project Add-In-Konturen berücksichtigen den Kalender des Add-Ins nicht, was zu falschen Ressourcenanforderungen führt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-131">Microsoft Project Add-in contours aren't respecting the add-in’s calendar resulting in incorrect resource requirements.</span></span>
- <span data-ttu-id="2cd1b-132">Durch das Erstellen von Projekten aus Vorlagen werden Zuweisungsdaten falsch festgelegt und die Möglichkeit zum Generieren von Ressourcenanforderungen verhindert.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-132">Creating projects from templates incorrectly sets assignment dates and prevents the ability to generate resource requirements.</span></span>
- <span data-ttu-id="2cd1b-133">Benutzer kann nicht auf die Optionen **Kategorie**, **Beschreibung**, **Status** über die Tastatur zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-133">User can't access **Category**, **Description**, **Status** options using the keyboard.</span></span>
- <span data-ttu-id="2cd1b-134">Die tatsächlichen Verkaufswerte des Projekts enthalten keine Gebühren- und Materialverkaufswerte.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-134">Actual sales values of the project aren't including fee and materials sales values.</span></span>
- <span data-ttu-id="2cd1b-135">Aggregation von tatsächlichen Verkäufen und tatsächlichen Kosten erfolgen bei Verwendung unterschiedlicher Wechselkurse fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-135">Aggregation of actual sales and actual cost happens incorrectly with different exchange rates.</span></span>
- <span data-ttu-id="2cd1b-136">Die Beschreibung in der **Standardarbeitsstundenvorlage** ist irreführend.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-136">The description in the **Default Work Hour Template** is misleading.</span></span>
- <span data-ttu-id="2cd1b-137">Das Einrücken einer Aufgabe entfernt die **Kategorie** in der Benutzeroberfläche bis zur Aktualisierung nicht.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-137">Indenting a task doesn't remove **Category** in the user interface until it is refreshed.</span></span>
- <span data-ttu-id="2cd1b-138">Eine fehlende Validierung, um sicherzustellen, dass ein Projekt über sein Enddatum hinaus verschoben wird, ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-138">Missing validation to ensure moving a project beyond its end date isn't permitted.</span></span>

<span data-ttu-id="2cd1b-139">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="2cd1b-139">**Sales**</span></span>

<span data-ttu-id="2cd1b-140">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2cd1b-140">The following issues have been fixed:</span></span>

- <span data-ttu-id="2cd1b-141">Eine Nullreferenzausnahme wird in einer Projektangebotszeile generiert, weil **Import aus Projektschätzung** sichtbar ist, wenn kein Projekt ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-141">A null reference exception is generated on a project quote line because **Import from Project Estimation** is visible when a project hasn't been selected.</span></span>
- <span data-ttu-id="2cd1b-142">Der folgende Fehler Objektreferenz nicht auf eine Instanz eines Objekts festgelegt tritt beim Schließen eines Angebots als **Gewonnen** auf.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-142">The following error, "Object reference not set to an instance of an object" occurs when closing a quote as **Won**.</span></span>
- <span data-ttu-id="2cd1b-143">Der Anpassungsstatus muss während der tatsächlichen Stornierung festgelegt werden, während ein Projekt von einer Vertragszeile getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-143">Adjustment status isn't set during an actual reversal while unlinking a project from a contract line.</span></span>
- <span data-ttu-id="2cd1b-144">Wenn Dynamics 365 Field Service und Project Service Automation beide installiert sind, werden die Optionen **Preise sperren** und **Verwenden Sie die aktuelle Preisgestaltung** nicht gleichzeitig auf der Seite **Rechnung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-144">When Dynamics 365 Field Service and Project Service Automation are both installed, the **Lock pricing** and **Use Current Pricing** options are not displayed at a same time on the **Invoice** page.</span></span>
- <span data-ttu-id="2cd1b-145">Für die japanische Sprache gibt es eine inkonsistente Übersetzung mit anderen kalenderbasierten Seiten.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-145">For the Japanese language, there is inconsistent translation with other calendar-based pages.</span></span>
- <span data-ttu-id="2cd1b-146">**Aktivieren** und **Deaktivieren** wurden von den Entitäten **Preislistenverband** in Project Service Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="2cd1b-146">**Activate** and **Deactivate** have been removed from **Price List Association** entities in Project Service Automation.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]