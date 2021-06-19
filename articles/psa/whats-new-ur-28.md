---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 28, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="163f3-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3</span><span class="sxs-lookup"><span data-stu-id="163f3-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="163f3-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="163f3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="163f3-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="163f3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="163f3-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="163f3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="163f3-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="163f3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="163f3-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="163f3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="163f3-109">In diesem Thema sind die Funktionen und Korrekturen aufgeführt, die für Project Service Automation V3, Update Release 28, neu hinzugefügt oder geändert wurden. Diese Version hat die Build-Nummer V3.10.46.32 und ist im Januar 2021 über ein Selbstupdate verfügbar.</span><span class="sxs-lookup"><span data-stu-id="163f3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="163f3-110">Update Release 28</span><span class="sxs-lookup"><span data-stu-id="163f3-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="163f3-111">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="163f3-111">Bug fixes</span></span>

<span data-ttu-id="163f3-112">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="163f3-112">**Time and Expense**</span></span>

<span data-ttu-id="163f3-113">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="163f3-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="163f3-114">Benutzer können **Massen-Bearbeitung** verwenden, um Zeiteinträge zu aktualisieren, die genehmigt und übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="163f3-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="163f3-115">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="163f3-115">**Project Management**</span></span>

<span data-ttu-id="163f3-116">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="163f3-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="163f3-117">In Fällen, in denen die Aufgaben-GUID als Zahl interpretiert wird, können Aufgaben nicht zum Bearbeiten mit **Aufgabe bearbeiten** im Band auf der Seite **Projektstrukturplan** geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="163f3-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="163f3-118">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="163f3-118">**Sales**</span></span>

<span data-ttu-id="163f3-119">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="163f3-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="163f3-120">Eine Nullreferenzausnahme wird generiert, wenn das **GetEstimatesForProject** Plug-In aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="163f3-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="163f3-121">**Als für Rechnung bereit markieren** im Meilensteinraster werden nur die teilweise aktualisierten Attribute mit Ausnahme des Attributs **InvoiceStatus** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="163f3-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]