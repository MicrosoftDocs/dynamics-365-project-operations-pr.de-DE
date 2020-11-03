---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 21, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 21, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076475"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="4380d-103">Project Service Automation Update Release 21, V3</span><span class="sxs-lookup"><span data-stu-id="4380d-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="4380d-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="4380d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4380d-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="4380d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4380d-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4380d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4380d-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4380d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4380d-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4380d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4380d-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 21 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4380d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="4380d-110">Diese Version hat die Build-Nummer V 3.10.32.50 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4380d-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="4380d-111">Update Release 21</span><span class="sxs-lookup"><span data-stu-id="4380d-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4380d-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="4380d-112">Bug fixes</span></span>

<span data-ttu-id="4380d-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="4380d-113">**Time and Expense**</span></span>

<span data-ttu-id="4380d-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4380d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4380d-115">Beim Hosting des **Zeiteintragsraster-Steuerelements** in Dashboards nutzt das Raster nicht die gesamte Breite des Dashboardrastercontainers.</span><span class="sxs-lookup"><span data-stu-id="4380d-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="4380d-116">Für bestimmte Zeitzonen zeigt das Rastersteuerelement **Zeiteintrag** keine Datensätze an.</span><span class="sxs-lookup"><span data-stu-id="4380d-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="4380d-117">Zeiteinträge, die nach 21:00 Uhr liegen, werden am falschen Tag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4380d-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="4380d-118">Benutzer können keine Ausgaben übermitteln, wenn die Ausgabenkategorie **Ausgabenbeleg erforderlich** keinen Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="4380d-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="4380d-119">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="4380d-119">**Resource Management**</span></span>

<span data-ttu-id="4380d-120">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4380d-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="4380d-121">Inaktive Buchungen werden in der Ansicht **Abstimmung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4380d-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="4380d-122">Bei der generischen Ressourcenerfüllung fehlte die Prüfung, um sicherzustellen, dass ein gültiger Buchungsstatus vorliegt.</span><span class="sxs-lookup"><span data-stu-id="4380d-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="4380d-123">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="4380d-123">**Project Management**</span></span>

<span data-ttu-id="4380d-124">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4380d-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="4380d-125">Die Formularraster **Projekt** (Ansicht **Ressourcenzuweisung** , **Aufgabe** , **Abstimmung** , **Ausgabenvorkalkulationen** ) bleiben bearbeitbar, selbst wenn ein Projekt nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4380d-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="4380d-126">Doppelte Kunden können nicht mit Kunden zusammengeführt werden, die mit bestätigten Projektverträgen verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="4380d-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="4380d-127">Wenn eine Ressource hinzugefügt wird, die keinen gültigen Kalender hat, gibt das System keine benutzerfreundliche Fehlermeldung zurück.</span><span class="sxs-lookup"><span data-stu-id="4380d-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="4380d-128">Die Schaltfläche **Aufgabe hinzufügen** im Aufgabenraster ist aktiviert, wenn das Projekt mit **Microsoft Project-Add-In** verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4380d-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="4380d-129">Der Aufwand wächst unkontrolliert, wenn eine Aufgabe mit einer Kategorie einer Ressource mit einer Rolle zugewiesen wird, für die ein Einstandspreis definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4380d-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="4380d-130">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="4380d-130">**Sales**</span></span>

<span data-ttu-id="4380d-131">Die folgenden Verbesserungen wurden vorgenommen:</span><span class="sxs-lookup"><span data-stu-id="4380d-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="4380d-132">**Rechnungsintervall** und **Abrechnungsstart** wurden in die Registerkarte **Rechnungszeitplan** verschoben.</span><span class="sxs-lookup"><span data-stu-id="4380d-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="4380d-133">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="4380d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="4380d-134">**Gesamtverkaufspreis** ist null (0) für **Kategorie** , obwohl **Rolle** einen Gesamtverkaufspreis hat, der nicht Null ist.</span><span class="sxs-lookup"><span data-stu-id="4380d-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="4380d-135">Kunden können den Wert des Felds **Rechnungsstatus** nicht in **Bereit zur Rechnungsstellung** ändern, wenn ein anderer angepasster Prozess ein zusätzliches Feld aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4380d-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="4380d-136">Die Schaltfläche **Rechnungspositionen aktualisieren** kann mehrere doppelte Positionen erstellen, wenn sie wiederholt ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="4380d-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="4380d-137">Die Schaltfläche **Preise aktualisieren** funktioniert nicht im Unterraster **Rollenpreise** des Formulars **Schnellansicht**.</span><span class="sxs-lookup"><span data-stu-id="4380d-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="4380d-138">Die Logik **Verkaufspreislisten-Lösung** behandelt Zeitzonen nicht ordnungsgemäß, was zu einer falschen Auswahl von Preislisten führt.</span><span class="sxs-lookup"><span data-stu-id="4380d-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="4380d-139">Die **Gesamten Istkosten** eines Projekts können um einen Bruchteil des Betrags abweichen, nachdem ein einmaliger Eintrag genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="4380d-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="4380d-140">Die Logik **Preislösung** liefert keine benutzerfreundliche Fehlermeldung, wenn **Abgerufener RolePrice** keine Werte in den Feldern **Primäre Einheit** und **Preis in primärer Einheit** hat.</span><span class="sxs-lookup"><span data-stu-id="4380d-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
