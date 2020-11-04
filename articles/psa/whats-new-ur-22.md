---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 22, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 22, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076472"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="8a935-103">Project Service Automation Update Release 22, V3</span><span class="sxs-lookup"><span data-stu-id="8a935-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="8a935-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="8a935-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8a935-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="8a935-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8a935-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="8a935-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8a935-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="8a935-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8a935-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8a935-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8a935-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 22 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a935-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="8a935-110">Diese Version hat die Build-Nummer V 3.10.33.48 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8a935-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="8a935-111">Update Release 22</span><span class="sxs-lookup"><span data-stu-id="8a935-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8a935-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="8a935-112">Bug fixes</span></span>



<span data-ttu-id="8a935-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="8a935-113">**Time and Expense**</span></span>

<span data-ttu-id="8a935-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="8a935-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a935-115">**Zeiteinträge** werden nach dem Import nicht automatisch im Zeiteinträge-Zeitplan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8a935-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="8a935-116">Die Rasterdatumsauswahl für **Zeiteintrag** erkennt die regionalen Einstellungen eines Benutzers nicht.</span><span class="sxs-lookup"><span data-stu-id="8a935-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="8a935-117">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="8a935-117">**Resource Management**</span></span>

<span data-ttu-id="8a935-118">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="8a935-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a935-119">Im manuellen Modus werden Änderungen an den **Ressourcenzuweisung** -Konturen nicht erkannt, wenn **Ressourcenanforderungen** generiert werden.</span><span class="sxs-lookup"><span data-stu-id="8a935-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="8a935-120">**Ressourcenanforderungen** unterstützen keine benutzerdefinierte Anforderungsstatus.</span><span class="sxs-lookup"><span data-stu-id="8a935-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="8a935-121">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="8a935-121">**Project Management**</span></span>

<span data-ttu-id="8a935-122">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="8a935-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a935-123">Durch Doppelklick auf EstimateGridControl werden niederländische Formatzahlen nicht korrekt analyisiert.</span><span class="sxs-lookup"><span data-stu-id="8a935-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="8a935-124">Zugwiesene Stunden werden nicht korrekt aktualisiert, wenn Zuweisungen mithilfe des Microsoft Project-Desktop-Client-Add-In geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8a935-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="8a935-125">Die Raster Projektnachverfolgung und Vorkalkulationen zeigen einen falschen Vertriebswährungscode an, wenn die Vertragswährung sich von der Kundenwährung unterscheidet und die Organisation dazu konfiguriert ist, Währungscodes statt Währungssymbolen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8a935-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="8a935-126">Das Enddatum eines Team-Mitglieds wird um einen Tag verlängert, wenn der Arbeitsstundenzeitplan 24 Stunden pro Tag beträgt.</span><span class="sxs-lookup"><span data-stu-id="8a935-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="8a935-127">Wenn Sie im Projektzeitplan einer Aufgabe eine Transaktionskategorie hinzufügen, wird dadurch nicht das automatische Speichern ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8a935-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="8a935-128">Der folgende Fehler wird angezeigt, wenn ein Teammitglied zur Projektvorlage hinzugefügt wird: „Ressourcenanforderungen können nicht den Projektvorlagen zugeordnet werden“.</span><span class="sxs-lookup"><span data-stu-id="8a935-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="8a935-129">Das Menüleisten-Regelskript „msdyn.Approval.CanApproveOrReject“ zeigt einen Timeout-Fehler an.</span><span class="sxs-lookup"><span data-stu-id="8a935-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="8a935-130">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="8a935-130">**Sales**</span></span>

<span data-ttu-id="8a935-131">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="8a935-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="8a935-132">Eine Prüfungsfehlermeldung wird nicht angezeigt, wenn eine Einstandspreisliste in der Preislisten-Suche für Formular/Entität „Neue Angebotsprojekt-Preisliste“ ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="8a935-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="8a935-133">Wenn Sie das Angebot als gewonnen schließen, navigieren Sie nicht zum erstellten Vertrag, wenn sich ein dem Angebot beigefügter BPF in der Endphase befindet.</span><span class="sxs-lookup"><span data-stu-id="8a935-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="8a935-134">Das Stornieren **Nicht in Rechnung gestellter Verkäufe** wird mit den ursprünglichen Kosten verknüpft, wenn ein Zeiteintrag zurückgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8a935-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="8a935-135">Nach Auswahl der Schaltfläche **Bestätigen** ändert sich der Rechnungsstatus nicht in **Bestätigt** , es sei denn, die Rechnung wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8a935-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>