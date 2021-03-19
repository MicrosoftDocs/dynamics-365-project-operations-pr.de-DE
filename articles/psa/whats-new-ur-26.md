---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 26, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 26, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280397"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="6eba8-103">Project Service Automation Update Release 26, V3</span><span class="sxs-lookup"><span data-stu-id="6eba8-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6eba8-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="6eba8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6eba8-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="6eba8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6eba8-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6eba8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6eba8-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="6eba8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6eba8-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6eba8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6eba8-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 26 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6eba8-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="6eba8-110">Diese Version hat die Build-Nummer V3.10.44.59 und ist im Allgemeinen über ein Selbstupdate im Dezember 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6eba8-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="6eba8-111">Update Release 26</span><span class="sxs-lookup"><span data-stu-id="6eba8-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6eba8-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="6eba8-112">Bug fixes</span></span>

<span data-ttu-id="6eba8-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="6eba8-113">**Time and Expense**</span></span>

<span data-ttu-id="6eba8-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="6eba8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6eba8-115">Benutzer können die Aufgabe für einen Zeiteintrag ändern, der genehmigt/übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="6eba8-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="6eba8-116">Fehler „Objektreferenz nicht gesetzt“ beim Speichern der Zeiteingabe.</span><span class="sxs-lookup"><span data-stu-id="6eba8-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="6eba8-117">Der Zeiteintragsimport aus Ressourcenzuweisungen erstellt Zeiteinträge mit den falschen DateTime-Werten.</span><span class="sxs-lookup"><span data-stu-id="6eba8-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="6eba8-118">Wenn Project Service Automation und die Field Service-App installiert sind, wird die **Neu**-Schaltfläche zweimal in der Befehlsleiste für Zeiteinträge in der Field Service-App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6eba8-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="6eba8-119">Zellenaktualisierungen von **Einheit zulassen** und **Einheitengruppe** funktionieren jetzt im Raster **Kostenschätzungen**.</span><span class="sxs-lookup"><span data-stu-id="6eba8-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="6eba8-120">**Zeiteintragsbearbeitung aktualisieren**-Formular enthält **Zeitleiste**.</span><span class="sxs-lookup"><span data-stu-id="6eba8-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="6eba8-121">Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts blockiert das System bei der Suche nach einer Projektgenehmigungsrolle.</span><span class="sxs-lookup"><span data-stu-id="6eba8-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="6eba8-122">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="6eba8-122">**Resource Management**</span></span>

<span data-ttu-id="6eba8-123">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="6eba8-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="6eba8-124">Validierung im **PostProjectCreate**-Plug-In hinzugefügt, um vor dem Erstellen einer primären Anforderung nach einer primären Anforderung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6eba8-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="6eba8-125">**Mitglied des Projektteams**-Formular für Schnellerfassung löst eine Nullreferenzausnahme aus, wenn Felder aus dem Formular entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6eba8-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="6eba8-126">Das Generieren von Anforderungen für 12 Stunden über 1 Jahr schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="6eba8-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="6eba8-127">Verbesserte Nullreferenzausnahme für Fehlermeldungen während der Erstellung der Ressourcenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6eba8-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="6eba8-128">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="6eba8-128">**Project Management**</span></span>

<span data-ttu-id="6eba8-129">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="6eba8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="6eba8-130">Verbesserte Validierung zur Behebung der Nullreferenzausnahme im **PreProjectUpdate** Plug-In.</span><span class="sxs-lookup"><span data-stu-id="6eba8-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="6eba8-131">Vom Microsoft Project-Desktop-Add-In veröffentlichte Projekte löschen nicht zugewiesene Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="6eba8-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="6eba8-132">Neue Validierung hinzugefügt, wenn die Projektreferenz einer Aufgabe aufgrund einer Nullreferenzausnahme im **PreValidateProjectTaskUpdate**-Plug-In ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="6eba8-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="6eba8-133">Das Teammitgliedsraster zeigt keine eindeutigen Zuordnungen im Teammitgliedsdatensatz an.</span><span class="sxs-lookup"><span data-stu-id="6eba8-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="6eba8-134">Neue Validierungs- und Fehlermeldungen aufgrund einer Nullreferenzausnahme im **PreProjectTaskDelete**-Plug-In hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6eba8-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="6eba8-135">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="6eba8-135">**Sales**</span></span>

<span data-ttu-id="6eba8-136">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="6eba8-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="6eba8-137">Bei der Auswahl einer projektbasierten Zeile im Angebot oder Vertrag sollte die **Vorschlag**-Schaltfläche nur sichtbar sein, wenn Sie eine produktbasierte Position auswählen, die einem vorhandenen Produkt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6eba8-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="6eba8-138">**Create_Product**-Berechtigung wurde von **Create_ProjectContract**-Berechtigung abgetrennt.</span><span class="sxs-lookup"><span data-stu-id="6eba8-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="6eba8-139">Das Löschen einer Rechnungsposition führt zu einem Nullreferenzfehler **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="6eba8-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]