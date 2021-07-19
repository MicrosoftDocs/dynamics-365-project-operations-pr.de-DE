---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 33, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334539"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="ae527-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3</span><span class="sxs-lookup"><span data-stu-id="ae527-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ae527-104">Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen.</span><span class="sxs-lookup"><span data-stu-id="ae527-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="ae527-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="ae527-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ae527-106">Es ist kompatibel mit Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ae527-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ae527-107">Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update.</span><span class="sxs-lookup"><span data-stu-id="ae527-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="ae527-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ae527-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ae527-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 33 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae527-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="ae527-110">Diese Version hat die Build-Nummer V3.10.54.98 und ist allgemein über ein Self-Update im Juli 2021 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae527-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="ae527-111">Update Release 33</span><span class="sxs-lookup"><span data-stu-id="ae527-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ae527-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="ae527-112">Bug fixes</span></span>

<span data-ttu-id="ae527-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="ae527-113">**Time and Expense**</span></span>

<span data-ttu-id="ae527-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="ae527-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ae527-115">Zwei gesperrte Felder, **msdyn_description** und **msdyn_externaldescription** sind nach dem Absenden editierbar.</span><span class="sxs-lookup"><span data-stu-id="ae527-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="ae527-116">Es erscheint eine Fehlermeldung, wenn eine Leistung erstellt wird, die nicht mit einem Projekt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ae527-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="ae527-117">Wenn ein Zeiteintrag erstellt wird, wird die Ressourcenrolle standardmäßig auf eine inaktive Rolle gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ae527-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="ae527-118">Erfassungszeilen, die mit einer zurückgerufenen und gelöschten Leistung verbunden sind, werden nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ae527-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="ae527-119">Aktualisieren Sie auf dem **Formular zum schnellen Erstellen von Zeiteinträgen** die Ansicht **Projektaufgabenliste**, um das standardmäßig angezeigte Datum auf das Startdatum der Aufgabe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ae527-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="ae527-120">Wenn Sie einen Zeiteintrag über die Registerkarte **Bezogen** der buchbaren Ressource erstellen, wird der Zeiteintrag fälschlicherweise für den angemeldeten Benutzer erstellt und nicht für die übergeordnete buchbare Ressource.</span><span class="sxs-lookup"><span data-stu-id="ae527-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="ae527-121">Dem Dialogfeld **Gesamtgenehmigung MDD** wurden neue Felder hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ae527-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="ae527-122">**Projektplanung**</span><span class="sxs-lookup"><span data-stu-id="ae527-122">**Project planning**</span></span>

<span data-ttu-id="ae527-123">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="ae527-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="ae527-124">Langsame Leistung bei der Projekterstellung, wenn Projektarbeitsstundenvorlagen mit komplexen Kalendern angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae527-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="ae527-125">Wenn das Startdatum größer als das Enddatum ist, wird in der Projektvorlage zum Kopieren ein Fehler angezeigt, da die Zeitkomponente der einzelnen Felder unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="ae527-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="ae527-126">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="ae527-126">**Resource management**</span></span>

<span data-ttu-id="ae527-127">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="ae527-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="ae527-128">Ein falscher Parameter wird in der Abfrage der Ressourcenauslastung verwendet und die XML führt zu falschen Filterergebnissen im **Ressourcenauslastung** Raster.</span><span class="sxs-lookup"><span data-stu-id="ae527-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="ae527-129">Die Bestätigung **Buchungen verlängern** zeigt ein falsches Enddatum für Buchungen an.</span><span class="sxs-lookup"><span data-stu-id="ae527-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="ae527-130">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="ae527-130">**Sales**</span></span>

<span data-ttu-id="ae527-131">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="ae527-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="ae527-132">Es tritt eine Fehlermeldung auf, wenn eine Kategorie Preis mit fehlenden Werten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ae527-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="ae527-133">Es tritt eine Fehlermeldung auf, wenn ein Meilenstein für eine Vertragszeile ohne eine Auftragszeile erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ae527-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
