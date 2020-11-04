---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 16, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 16, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076483"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="27ffb-103">Project Service Automation Update Release 16, V3</span><span class="sxs-lookup"><span data-stu-id="27ffb-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="27ffb-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="27ffb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="27ffb-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="27ffb-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="27ffb-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="27ffb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="27ffb-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="27ffb-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="27ffb-108">Weitere Informationen: [Installieren, Aktualisieren einer bevorzugten Lösung](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="27ffb-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="27ffb-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 16 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="27ffb-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="27ffb-110">Diese Version hat eine Build-Nummer von V3.10.6.34 und ist im durch ein Selbst-Update im Januar 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27ffb-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="27ffb-111">Update Release 16</span><span class="sxs-lookup"><span data-stu-id="27ffb-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="27ffb-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="27ffb-112">Bug fixes</span></span>

-   <span data-ttu-id="27ffb-113">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27ffb-113">Time and Expense</span></span>

    -   <span data-ttu-id="27ffb-114">Behoben: Benutzer, die versuchen, gelöschte Zeit- und Kosteneinträge zur Genehmigung einzureichen, erhalten jetzt relevante Fehlermeldungen.</span><span class="sxs-lookup"><span data-stu-id="27ffb-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="27ffb-115">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="27ffb-115">Project Management</span></span>

    -   <span data-ttu-id="27ffb-116">Behoben: Die in Vorlagen für Teammitglieder definierten Ressourceneinheiten werden eingehalten, und die Vorlagen werden auf ein neues Projekt angewendet.</span><span class="sxs-lookup"><span data-stu-id="27ffb-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="27ffb-117">Behoben: Verbesserte Handhabung der Neuzuweisung von Datensatzbesitz.</span><span class="sxs-lookup"><span data-stu-id="27ffb-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="27ffb-118">Behoben: Projekte, die gerade kopiert werden, dürfen erst kopiert werden, wenn alle Kopiervorgänge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="27ffb-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="27ffb-119">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="27ffb-119">Resource Management</span></span>

    -   <span data-ttu-id="27ffb-120">Behoben: Durch Buchung verlängern werden kurze Laufzeiten jetzt korrekt gehandhabt, und es werden keine Nullstunden mehr für erweiterte Buchungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="27ffb-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="27ffb-121">Behoben: Die Abstimmungsansicht wird jetzt gerendert, wenn die Projektzeitzone +5:30 GMT beträgt und die Zeit des Benutzers sich davon unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="27ffb-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="27ffb-122">Sales</span><span class="sxs-lookup"><span data-stu-id="27ffb-122">Sales</span></span>

    -   <span data-ttu-id="27ffb-123">Behoben: Wenn ein einer Vertragszeile zugeordnetes Projekt entfernt und ein neues Projekt zugeordnet wurde, wurden die tatsächlichen Datensätze des neuen Projekts nicht basierend auf den in der Vertragszeile definierten Abrechnungs- und Preisregeln neu bewertet.</span><span class="sxs-lookup"><span data-stu-id="27ffb-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="27ffb-124">Dies wurde in dieser Version behoben.</span><span class="sxs-lookup"><span data-stu-id="27ffb-124">This has been fixed in this release.</span></span> <span data-ttu-id="27ffb-125">Preisgestaltung und tatsächliche Aufzeichnungen des neu zugeordneten Projekts werden rückgängig gemacht und basierend auf den Preis- und Abrechnungsregeln der Vertragszeile korrekt neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="27ffb-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="27ffb-126">Die tatsächlichen Aufzeichnungen des nicht zugeordneten Projekts werden ebenfalls neu bewertet und infolgedessen neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="27ffb-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="27ffb-127">Behoben: Eine zusätzliche Validierung wurde zum Feld **Menge** einer Vorkalkulationsposition hinzugefügt, um sicherzustellen, dass Nullwerte nicht beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="27ffb-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="27ffb-128">Behoben: Wenn Istwerte eines Projekts aktualisiert wurden, wurde dem Hauptformular des Projekts eine Schaltfläche zum Aktualisieren hinzugefügt, damit Benutzer die Istwerte erneut synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="27ffb-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="27ffb-129">Behoben: Wenn Benutzer ein Upgrade von 2.X auf 3.X durchführen, sind Projekte mit einem NULL-Wert für den Projektnamen zulässig.</span><span class="sxs-lookup"><span data-stu-id="27ffb-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>
