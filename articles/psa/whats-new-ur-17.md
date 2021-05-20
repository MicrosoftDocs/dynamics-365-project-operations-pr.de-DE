---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 17, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 17, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949228"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="5d077-103">Project Service Automation Update Release 17, V3</span><span class="sxs-lookup"><span data-stu-id="5d077-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5d077-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="5d077-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5d077-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="5d077-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="5d077-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5d077-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5d077-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5d077-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5d077-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5d077-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5d077-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 17 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d077-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="5d077-110">Diese Version hat eine Build-Nummer von V3.10.6.34 und ist durch eine Selbstaktualisierung im März 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d077-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="5d077-111">Update Release 17</span><span class="sxs-lookup"><span data-stu-id="5d077-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5d077-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="5d077-112">Bug fixes</span></span>

<span data-ttu-id="5d077-113">**Allgemein**</span><span class="sxs-lookup"><span data-stu-id="5d077-113">**General**</span></span>

- <span data-ttu-id="5d077-114">Behoben: Aktualisieren Sie Project Service Automation, um Team Member-Lizenzen durchzusetzen (Project Resource Hub enthält die Metadaten für den Team Member Service-Plan 3.x).</span><span class="sxs-lookup"><span data-stu-id="5d077-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="5d077-115">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="5d077-115">**Time and Expense**</span></span>

- <span data-ttu-id="5d077-116">Behoben: Es ist nicht möglich, eine Kostenvorkalkulation von einem Preis ungleich Null auf Null (0) zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5d077-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="5d077-117">Die Änderung wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5d077-117">The change is ignored.</span></span>

<span data-ttu-id="5d077-118">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="5d077-118">**Project Management**</span></span>

- <span data-ttu-id="5d077-119">Behoben: Eine Prüfung auf Nullwerte wurde zum Positionsnamen eines Teammitglieds hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5d077-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="5d077-120">Behoben: Das Feld **msdyn_userresourceid** in der Entität **msdyn_resourceassignment** ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="5d077-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="5d077-121">Behoben: Das Upgrade von 2.x auf 3.x behandelt jetzt leere Aufwandskonturen bei Aufgabenzuweisungen.</span><span class="sxs-lookup"><span data-stu-id="5d077-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="5d077-122">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="5d077-122">**Sales**</span></span>

- <span data-ttu-id="5d077-123">Behoben: **Invoice.PreValidateInvoiceUpdate** behandelt jetzt das Szenario der ordnungsgemäßen Neuzuweisung von Datensatzbesitzern.</span><span class="sxs-lookup"><span data-stu-id="5d077-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="5d077-124">Behoben: Wenn die Transaktionsklasse **Zeit** ist, kann **UnitGroup** nicht für alle Entitäten bearbeitet werden, einschließlich, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** und **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="5d077-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="5d077-125">Jedoch ist das Feld **Einheit** nur für **JournalLine** und **InvoiceLineDetails** nicht bearbeitbar.</span><span class="sxs-lookup"><span data-stu-id="5d077-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]