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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124817"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="1cd77-103">Project Service Automation Update Release 14, V3</span><span class="sxs-lookup"><span data-stu-id="1cd77-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="1cd77-104">Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben.</span><span class="sxs-lookup"><span data-stu-id="1cd77-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="1cd77-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="1cd77-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1cd77-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1cd77-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1cd77-107">Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1cd77-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="1cd77-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1cd77-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1cd77-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 14 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cd77-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="1cd77-110">Diese Version hat eine Build-Nummer von V3.10.4.21 und ist nach folgendem Zeitplan verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1cd77-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="1cd77-111">**Allgemeine Verfügbarkeit (Selbstaktualisierung):** Januar 2020</span><span class="sxs-lookup"><span data-stu-id="1cd77-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="1cd77-112">**Automatischer Update:** Februar 2020</span><span class="sxs-lookup"><span data-stu-id="1cd77-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="1cd77-113">Update Release 14</span><span class="sxs-lookup"><span data-stu-id="1cd77-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="1cd77-114">Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="1cd77-114">Enhancements</span></span>

- <span data-ttu-id="1cd77-115">Sales</span><span class="sxs-lookup"><span data-stu-id="1cd77-115">Sales</span></span>

     - <span data-ttu-id="1cd77-116">Benutzerdefinierte Feldwerte von **Angebot Zeilendetails** werden kopiert nach **Projektvertragspositionsdetails**, wenn ein Angebot aktualisiert wird auf **Wie gewonnen geschlossen**.</span><span class="sxs-lookup"><span data-stu-id="1cd77-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="1cd77-117">Bestätigte Projekte können **Als verloren geschlossen** sein.</span><span class="sxs-lookup"><span data-stu-id="1cd77-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="1cd77-118">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="1cd77-118">Resource Management</span></span>

     - <span data-ttu-id="1cd77-119">Beim Erweitern von Buchungen werden Benutzer in einem Bestätigungsdialogfeld aufgefordert, die Buchungsergebnisse zusammenzufassen und einen Link zum Verwalten von Buchungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1cd77-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="1cd77-120">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="1cd77-120">Bug fixes</span></span>

- <span data-ttu-id="1cd77-121">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cd77-121">Time and Expense</span></span>

     - <span data-ttu-id="1cd77-122">Behoben: Verbesserte Benutzererfahrung, wenn der Benutzer keine zu korrigierenden Einträge ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1cd77-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="1cd77-123">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="1cd77-123">Resource Management</span></span>

     - <span data-ttu-id="1cd77-124">Behoben: Das mehrfache Buchen einer Ressource überläuft den Namen der buchbaren Ressource.</span><span class="sxs-lookup"><span data-stu-id="1cd77-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="1cd77-125">Sales</span><span class="sxs-lookup"><span data-stu-id="1cd77-125">Sales</span></span>

     - <span data-ttu-id="1cd77-126">Behoben: Der Gesamtverkaufspreis wird erst berechnet, wenn der Benutzer auch einen Selbstkostenpreis für Kostenvoranschläge für ein Projekt eingibt.</span><span class="sxs-lookup"><span data-stu-id="1cd77-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="1cd77-127">Behoben: Schließen eines Zitats als **Gewonnen** schlägt fehl, wenn der zugehörige Projektvertrag nicht im **Entwurf** Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="1cd77-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

