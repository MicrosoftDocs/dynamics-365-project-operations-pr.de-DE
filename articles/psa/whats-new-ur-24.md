---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 24, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 24, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000255"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="fafb8-103">Project Service Automation Update Release 24, V3</span><span class="sxs-lookup"><span data-stu-id="fafb8-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fafb8-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="fafb8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fafb8-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="fafb8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fafb8-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fafb8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fafb8-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="fafb8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fafb8-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fafb8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fafb8-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 24 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fafb8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="fafb8-110">Diese Version hat eine Build-Nummer von V 3.10.42.43 und ist durch ein Selbst-Update im Oktober 2020 allgemein verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fafb8-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="fafb8-111">Update Release 24</span><span class="sxs-lookup"><span data-stu-id="fafb8-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fafb8-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="fafb8-112">Bug fixes</span></span>

<span data-ttu-id="fafb8-113">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="fafb8-113">**Sales**</span></span>

<span data-ttu-id="fafb8-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="fafb8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fafb8-115">Problem beim Festlegen der Standardpreisliste der Produkte.</span><span class="sxs-lookup"><span data-stu-id="fafb8-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="fafb8-116">Die Leistung des Angebotsgewinns ist aufgrund der eingebetteten Preisliste und der Kopie der Rollenpreisdatensätze langsam.</span><span class="sxs-lookup"><span data-stu-id="fafb8-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="fafb8-117">**Projektvertrag/Vertriebs-Hub** > **Produktposition/Bestellpositionsmenge** wird automatisch auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="fafb8-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="fafb8-118">Erhöhen Sie die Systemberechtigungen beim Lesen von Preislisten.</span><span class="sxs-lookup"><span data-stu-id="fafb8-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="fafb8-119">Kopieren Sie die Kundenadressfelder **address1_freighttermscode** und **address1_shippingmethodcode** nach Angebot/Auftrag.</span><span class="sxs-lookup"><span data-stu-id="fafb8-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="fafb8-120">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="fafb8-120">**Time and Expense**</span></span>

<span data-ttu-id="fafb8-121">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="fafb8-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="fafb8-122">Das **Zeiterfassungsraster** unterstützt kein **Nur Datum**-Zeitverhalten.</span><span class="sxs-lookup"><span data-stu-id="fafb8-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="fafb8-123">**Zeiteintrag** wird nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="fafb8-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="fafb8-124">Eine manuelle Aktualisierung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fafb8-124">A manual refresh is required.</span></span>
- <span data-ttu-id="fafb8-125">Die Zeiteinträge können nicht aus einer Zuweisung importiert werden, wenn die Zuweisungen einer Ressource unterbrochen sind (0 Stunden).</span><span class="sxs-lookup"><span data-stu-id="fafb8-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="fafb8-126">Stellen Sie beim Erstellen eines Zeiteintrags den Start auf den gleichen Wert ein wie **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="fafb8-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="fafb8-127">Aktivieren Sie die Massenbearbeitung für die Zeiteingabe erneut.</span><span class="sxs-lookup"><span data-stu-id="fafb8-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="fafb8-128">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="fafb8-128">**Resource Management**</span></span>

<span data-ttu-id="fafb8-129">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="fafb8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="fafb8-130">Wenn Sie versuchen, den Status einer Buchung zwischen zwei Tagen ohne Anforderung zu aktualisieren, wird eine null-ref-Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="fafb8-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="fafb8-131">Fehler beim Laden der **Abstimmungsansicht**.</span><span class="sxs-lookup"><span data-stu-id="fafb8-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="fafb8-132">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="fafb8-132">**Project Management**</span></span>

<span data-ttu-id="fafb8-133">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="fafb8-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="fafb8-134">Die automatische Speicherung wird im **Projektplan** beim Wechsel von **Manuell** zu **Automatisch** nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fafb8-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="fafb8-135">Aufwandskosten sollten nicht zur Abweichung auf dem **Projektverfolgungsraster** berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="fafb8-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="fafb8-136">Inkonsistentes Verhalten für **Schätzungs-Tag**-Spalten während des Ladens versus Änderungen vom Typ **Zeitphase**.</span><span class="sxs-lookup"><span data-stu-id="fafb8-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="fafb8-137">Die tatsächlichen Kosten eines Projekts spiegeln möglicherweise nicht die Gesamtsummen von **Tatsächliche Transaktionen** wider.</span><span class="sxs-lookup"><span data-stu-id="fafb8-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="fafb8-138">Das **geschätzte Enddatum** auf der Registerkarte **Zusammenfassung** stimmt nicht mit dem **PSP-Zeitplan** überein.</span><span class="sxs-lookup"><span data-stu-id="fafb8-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="fafb8-139">**Aktuelle Stunden aktualisieren** beim Ausrücken funktioniert nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="fafb8-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="fafb8-140">Ein Projektmanager außerhalb des **Unternehmenseinheit**-Stamms kann kein Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="fafb8-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="fafb8-141">Änderungen an der Aufgabe oder Kategorie unter **Ausgabenschätzungen** werden nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fafb8-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="fafb8-142">**Kopie des Vertrags** kopiert die Rechnungspläne und den Ausführungsstatus.</span><span class="sxs-lookup"><span data-stu-id="fafb8-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="fafb8-143">Die Schaltfläche **Tatsächliche Transaktionen aktualisieren** berechnet Zusammenfassungsaufgaben falsch.</span><span class="sxs-lookup"><span data-stu-id="fafb8-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="fafb8-144">Microsoft Project-Add-In: Behebung eines Nullreferenzfehlers, wenn ein Teammitglied eine leere Ressourceneinheit hat.</span><span class="sxs-lookup"><span data-stu-id="fafb8-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]