---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 25, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 25, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 3aa10e1d4b23fbe6c2743d71497bdef840776008
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948870"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="867ad-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 25, V3</span><span class="sxs-lookup"><span data-stu-id="867ad-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="867ad-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="867ad-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="867ad-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="867ad-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="867ad-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="867ad-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="867ad-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="867ad-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="867ad-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="867ad-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="867ad-109">In diesem Thema sind die Funktionen und Korrekturen aufgeführt, die für Project Service Automation V3, Update Release 25, neu hinzugefügt oder geändert wurden. Diese Version hat die Build-Nummer V 3.10.43.76 und ist im Oktober 2020 über ein Selbstupdate verfügbar.</span><span class="sxs-lookup"><span data-stu-id="867ad-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="867ad-110">Update Release 25</span><span class="sxs-lookup"><span data-stu-id="867ad-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="867ad-111">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="867ad-111">Bug fixes</span></span>

<span data-ttu-id="867ad-112">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="867ad-112">**Time and Expense**</span></span>

<span data-ttu-id="867ad-113">Das folgende Problem wurde behoben:</span><span class="sxs-lookup"><span data-stu-id="867ad-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="867ad-114">Zeiterfassungstabelle mit zusätzlichen Daten basierend auf einem zu großen Intervall, das abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="867ad-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="867ad-115">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="867ad-115">**Resource Management**</span></span>

<span data-ttu-id="867ad-116">Das folgende Problem wurde behoben:</span><span class="sxs-lookup"><span data-stu-id="867ad-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="867ad-117">Paketbereitstellungscode hinzugefügt, um den Universal Resource Scheduling-Patch-Import zu überspringen, wenn bereits ein Patch einer höheren Version vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="867ad-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="867ad-118">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="867ad-118">**Project Management**</span></span>

<span data-ttu-id="867ad-119">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="867ad-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="867ad-120">Korrigierte Rundungs- und Wechselkursdifferenzen führten zu falschen geplanten Kosten im Projektverfolgungsraster.</span><span class="sxs-lookup"><span data-stu-id="867ad-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="867ad-121">Unterstützen Sie die Möglichkeit, zwei oder mehr Reaktionsraster im **Projekt**-Formular anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="867ad-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="867ad-122">Validierung bereitgestellt, um die Möglichkeit zu adressieren, eine Aufgabe nach dem Enddatum des Kalenders zuzuweisen, was zu einer fehlgeschlagenen Ressourcenzuweisung führt.</span><span class="sxs-lookup"><span data-stu-id="867ad-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="867ad-123">Verbesserte Fehlerbehandlung zur Behebung der Nullreferenz-Ausnahme, die aus folgenden Gründen generiert wurde:</span><span class="sxs-lookup"><span data-stu-id="867ad-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="867ad-124">**PreValidateProjectTeamMemberCreate**-Plug-In</span><span class="sxs-lookup"><span data-stu-id="867ad-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="867ad-125">**PreValidateProjectTaskCreate** wenn eine Projektaufgabe ohne zugehöriges Projekt erstellt wird</span><span class="sxs-lookup"><span data-stu-id="867ad-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="867ad-126">**PreProjectTeamMemberCreate**-Plug-In</span><span class="sxs-lookup"><span data-stu-id="867ad-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="867ad-127">**PostProjectTeamMemberDelete**-Plug-In</span><span class="sxs-lookup"><span data-stu-id="867ad-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="867ad-128">**PreValidateProjectTaskDelete**-Plug-In</span><span class="sxs-lookup"><span data-stu-id="867ad-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="867ad-129">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="867ad-129">**Sales**</span></span>

<span data-ttu-id="867ad-130">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="867ad-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="867ad-131">Verbesserte Fehlerbehandlung zur Behebung von Nullreferenzausnahmen, die von **Projekt kopieren: Schätzungen HelperResource Management** generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="867ad-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="867ad-132">**Nicht bereit für die Rechnungsstellung** in einem **Rückstandsprotokoll über Zeit- und Materialberechnung** löscht den Abrechnungsstatus nicht.</span><span class="sxs-lookup"><span data-stu-id="867ad-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="867ad-133">Falsch beschriftete **Preise**-Schaltflächen auf den Registerkarten **Rollenpreis** und **Katalogartikel** wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="867ad-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]