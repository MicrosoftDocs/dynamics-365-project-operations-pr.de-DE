---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643262"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="f234e-102">Project Service Automation Update Release 26, V3</span><span class="sxs-lookup"><span data-stu-id="f234e-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="f234e-103">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="f234e-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f234e-104">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="f234e-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f234e-105">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f234e-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f234e-106">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f234e-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f234e-107">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f234e-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f234e-108">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 26 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f234e-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="f234e-109">Diese Version hat die Build-Nummer V3.10.44.59 und ist im Allgemeinen über ein Selbstupdate im Dezember 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f234e-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="f234e-110">Update Release 26</span><span class="sxs-lookup"><span data-stu-id="f234e-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="f234e-111">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="f234e-111">Bug fixes</span></span>

<span data-ttu-id="f234e-112">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="f234e-112">**Time and Expense**</span></span>

<span data-ttu-id="f234e-113">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="f234e-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f234e-114">Benutzer können die Aufgabe für einen Zeiteintrag ändern, der genehmigt/übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f234e-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="f234e-115">Fehler „Objektreferenz nicht gesetzt“ beim Speichern der Zeiteingabe.</span><span class="sxs-lookup"><span data-stu-id="f234e-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="f234e-116">Der Zeiteintragsimport aus Ressourcenzuweisungen erstellt Zeiteinträge mit den falschen DateTime-Werten.</span><span class="sxs-lookup"><span data-stu-id="f234e-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="f234e-117">Wenn Project Service Automation und die Field Service-App installiert sind, wird die **Neu**-Schaltfläche zweimal in der Befehlsleiste für Zeiteinträge in der Field Service-App angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f234e-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="f234e-118">Zellenaktualisierungen von **Einheit zulassen** und **Einheitengruppe** funktionieren jetzt im Raster **Kostenschätzungen**.</span><span class="sxs-lookup"><span data-stu-id="f234e-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="f234e-119">**Zeiteintragsbearbeitung aktualisieren**-Formular enthält **Zeitleiste**.</span><span class="sxs-lookup"><span data-stu-id="f234e-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="f234e-120">Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts blockiert das System bei der Suche nach einer Projektgenehmigungsrolle.</span><span class="sxs-lookup"><span data-stu-id="f234e-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="f234e-121">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="f234e-121">**Resource Management**</span></span>

<span data-ttu-id="f234e-122">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="f234e-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f234e-123">Validierung im **PostProjectCreate**-Plug-In hinzugefügt, um vor dem Erstellen einer primären Anforderung nach einer primären Anforderung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f234e-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="f234e-124">**Mitglied des Projektteams**-Formular für Schnellerfassung löst eine Nullreferenzausnahme aus, wenn Felder aus dem Formular entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f234e-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="f234e-125">Das Generieren von Anforderungen für 12 Stunden über 1 Jahr schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="f234e-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="f234e-126">Verbesserte Nullreferenzausnahme für Fehlermeldungen während der Erstellung der Ressourcenanforderungen.</span><span class="sxs-lookup"><span data-stu-id="f234e-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="f234e-127">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="f234e-127">**Project Management**</span></span>

<span data-ttu-id="f234e-128">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="f234e-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f234e-129">Verbesserte Validierung zur Behebung der Nullreferenzausnahme im **PreProjectUpdate** Plug-In.</span><span class="sxs-lookup"><span data-stu-id="f234e-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="f234e-130">Vom Microsoft Project-Desktop-Add-In veröffentlichte Projekte löschen nicht zugewiesene Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="f234e-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="f234e-131">Neue Validierung hinzugefügt, wenn die Projektreferenz einer Aufgabe aufgrund einer Nullreferenzausnahme im **PreValidateProjectTaskUpdate**-Plug-In ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="f234e-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="f234e-132">Das Teammitgliedsraster zeigt keine eindeutigen Zuordnungen im Teammitgliedsdatensatz an.</span><span class="sxs-lookup"><span data-stu-id="f234e-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="f234e-133">Neue Validierungs- und Fehlermeldungen aufgrund einer Nullreferenzausnahme im **PreProjectTaskDelete**-Plug-In hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f234e-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="f234e-134">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="f234e-134">**Sales**</span></span>

<span data-ttu-id="f234e-135">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="f234e-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="f234e-136">Bei der Auswahl einer projektbasierten Zeile im Angebot oder Vertrag sollte die **Vorschlag**-Schaltfläche nur sichtbar sein, wenn Sie eine produktbasierte Position auswählen, die einem vorhandenen Produkt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f234e-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="f234e-137">**Create_Product**-Berechtigung wurde von **Create_ProjectContract**-Berechtigung abgetrennt.</span><span class="sxs-lookup"><span data-stu-id="f234e-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="f234e-138">Das Löschen einer Rechnungsposition führt zu einem Nullreferenzfehler **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="f234e-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
