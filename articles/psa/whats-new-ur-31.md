---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 31, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 31, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999130"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="4c1b8-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 31, V3</span><span class="sxs-lookup"><span data-stu-id="4c1b8-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4c1b8-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4c1b8-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4c1b8-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4c1b8-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4c1b8-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4c1b8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4c1b8-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 31 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="4c1b8-110">Diese Version hat die Build-Nummer V3.10.52.77 und ist allgemein über ein Selbstupdate im Mail 2021 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="4c1b8-111">Update Release 31</span><span class="sxs-lookup"><span data-stu-id="4c1b8-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4c1b8-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="4c1b8-112">Bug fixes</span></span>

<span data-ttu-id="4c1b8-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="4c1b8-113">**Time and Expense**</span></span>

<span data-ttu-id="4c1b8-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4c1b8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c1b8-115">Befehlsschaltflächen für die Zeiteintragssteuerung auf der Seite **Buchbare Ressource** waren verwirrend.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="4c1b8-116">Eine Nullreferenzausnahme wurde in **Project.SetTrackingFields** bei der Genehmigung eines Zeiteintrags generiert.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="4c1b8-117">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="4c1b8-117">**Resource Management**</span></span>

<span data-ttu-id="4c1b8-118">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4c1b8-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c1b8-119">**Teammitglied erstellen** zeigt die Metadateneinstellung für das Buchungssetup für **Status der festgeschriebenen Standardbuchung** nicht korrekt an.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="4c1b8-120">Fehler beim Beim Upgrade von PSA 1.X auf 3.X bei **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="4c1b8-121">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="4c1b8-121">**Sales**</span></span>

<span data-ttu-id="4c1b8-122">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4c1b8-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c1b8-123">Der tatsächliche Umsatz rechnet die Beträge im Tracking-Raster in die Projektwährung um.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="4c1b8-124">Der Währungsstandard ist unklar, wenn Journalzeilen, Angebotszeilen und Vertragszeilen in Szenarien erstellt werden, in denen die Basiswährung einer Organisation von der Projektwährung abweicht.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="4c1b8-125">Die Abfrage **Ausstehende Korrekturjournalvalidierung** wird nicht nach Projekt gefiltert.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="4c1b8-126">Verbleibende Verkäufe werden für ein Projekt falsch berechnet.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="4c1b8-127">Angebote, die auf einem Kontakt basieren, schlagen fehl, wenn sie ohne eine Preisliste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="4c1b8-128">Bei der Auswahl von **Rechnung bestätigen** wird kein Verarbeitungs-Drehfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="4c1b8-129">Bei der Auswahl von **Rechnung erstellen** wird kein Verarbeitungs-Drehfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="4c1b8-130">Wenn Sie ein Angebot als verloren schließen, werden die Buchungen nicht storniert.</span><span class="sxs-lookup"><span data-stu-id="4c1b8-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







