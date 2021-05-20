---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 14, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Update Release 14, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 1d0aeb4684ae04d8774a31a51664ceb84307b10d
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949377"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="372a9-103">Project Service Automation Update Release 14, V3</span><span class="sxs-lookup"><span data-stu-id="372a9-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="372a9-104">Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben.</span><span class="sxs-lookup"><span data-stu-id="372a9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="372a9-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="372a9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="372a9-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="372a9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="372a9-107">Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="372a9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="372a9-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="372a9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="372a9-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 14 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="372a9-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="372a9-110">Diese Version hat eine Build-Nummer von V3.10.4.21 und ist nach folgendem Zeitplan verfügbar:</span><span class="sxs-lookup"><span data-stu-id="372a9-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="372a9-111">**Allgemeine Verfügbarkeit (Selbstaktualisierung):** Januar 2020</span><span class="sxs-lookup"><span data-stu-id="372a9-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="372a9-112">**Automatischer Update:** Februar 2020</span><span class="sxs-lookup"><span data-stu-id="372a9-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="372a9-113">Update Release 14</span><span class="sxs-lookup"><span data-stu-id="372a9-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="372a9-114">Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="372a9-114">Enhancements</span></span>

- <span data-ttu-id="372a9-115">Sales</span><span class="sxs-lookup"><span data-stu-id="372a9-115">Sales</span></span>

     - <span data-ttu-id="372a9-116">Benutzerdefinierte Feldwerte von **Angebot Zeilendetails** werden kopiert nach **Projektvertragspositionsdetails**, wenn ein Angebot aktualisiert wird auf **Wie gewonnen geschlossen**.</span><span class="sxs-lookup"><span data-stu-id="372a9-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="372a9-117">Bestätigte Projekte können **Als verloren geschlossen** sein.</span><span class="sxs-lookup"><span data-stu-id="372a9-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="372a9-118">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="372a9-118">Resource Management</span></span>

     - <span data-ttu-id="372a9-119">Beim Erweitern von Buchungen werden Benutzer in einem Bestätigungsdialogfeld aufgefordert, die Buchungsergebnisse zusammenzufassen und einen Link zum Verwalten von Buchungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="372a9-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="372a9-120">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="372a9-120">Bug fixes</span></span>

- <span data-ttu-id="372a9-121">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="372a9-121">Time and Expense</span></span>

     - <span data-ttu-id="372a9-122">Behoben: Verbesserte Benutzererfahrung, wenn der Benutzer keine zu korrigierenden Einträge ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="372a9-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="372a9-123">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="372a9-123">Resource Management</span></span>

     - <span data-ttu-id="372a9-124">Behoben: Das mehrfache Buchen einer Ressource überläuft den Namen der buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="372a9-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="372a9-125">Sales</span><span class="sxs-lookup"><span data-stu-id="372a9-125">Sales</span></span>

     - <span data-ttu-id="372a9-126">Behoben: Der Gesamtverkaufspreis wird erst berechnet, wenn der Benutzer auch einen Selbstkostenpreis für Kostenvoranschläge für ein Projekt eingibt.</span><span class="sxs-lookup"><span data-stu-id="372a9-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="372a9-127">Behoben: Schließen eines Zitats als **Gewonnen** schlägt fehl, wenn der zugehörige Projektvertrag nicht im **Entwurf** Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="372a9-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]