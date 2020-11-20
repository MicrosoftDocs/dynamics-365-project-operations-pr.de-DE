---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 13, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121622"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="8880b-103">Project Service Automation Update Release 13, V3</span><span class="sxs-lookup"><span data-stu-id="8880b-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="8880b-104">Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben.</span><span class="sxs-lookup"><span data-stu-id="8880b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="8880b-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="8880b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8880b-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8880b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8880b-107">Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8880b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="8880b-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8880b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8880b-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 13 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8880b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="8880b-110">Diese Version hat eine Build-Nummer von V3.10.3.18 und ist nach folgendem Zeitplan verfügbar:</span><span class="sxs-lookup"><span data-stu-id="8880b-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="8880b-111">**Allgemeine Verfügbarkeit (Selbstaktualisierung):** November 2019</span><span class="sxs-lookup"><span data-stu-id="8880b-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="8880b-112">**Automatischer Update:** Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="8880b-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="8880b-113">Update Release 13</span><span class="sxs-lookup"><span data-stu-id="8880b-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="8880b-114">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="8880b-114">Bug fixes</span></span>

- <span data-ttu-id="8880b-115">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8880b-115">Time and Expense</span></span>

     - <span data-ttu-id="8880b-116">Behoben: Suchfunktion auf der **Kostenfreigabe** Seite funktioniert nicht bei Suche nach Spesenzweck.</span><span class="sxs-lookup"><span data-stu-id="8880b-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="8880b-117">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="8880b-117">Resource Management</span></span>

     - <span data-ttu-id="8880b-118">Behoben: Zahlen in der Abstimmung wurden aktualisiert, um die richtige Ausrichtung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="8880b-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="8880b-119">Behoben: Benannte Ressourcen können Aufgaben nicht über die Registerkarte **Zeitplan** zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8880b-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="8880b-120">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="8880b-120">Project Management</span></span>

     - <span data-ttu-id="8880b-121">Behoben: Null-Referenz-Ausnahme beim Zuweisen von Teammitgliedern, wenn dem **Art der Transaktion** Setup-Informationen für **Einheit** und **DefaultGroup** fehlt.</span><span class="sxs-lookup"><span data-stu-id="8880b-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="8880b-122">Sales</span><span class="sxs-lookup"><span data-stu-id="8880b-122">Sales</span></span>

     - <span data-ttu-id="8880b-123">Behoben: Doppelte Transaktionstypdatensätze geben einen Fehler zurück, wenn Rollenpreisdatensätze erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8880b-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="8880b-124">Behoben: Zusätzliche Schaltflächen für **Neue Verkaufschance**, **Angebot**, **Auftragsposition** und **Produkt hinzufügen** werden in Befehlen für Verkaufschancen, Angebote, Bestellprodukte und projektbasierte Zeilenunterraster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8880b-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


