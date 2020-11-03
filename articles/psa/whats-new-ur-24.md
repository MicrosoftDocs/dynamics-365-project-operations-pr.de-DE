---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 24, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 24, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076476"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="cd3a3-103">Project Service Automation Update Release 24, V3</span><span class="sxs-lookup"><span data-stu-id="cd3a3-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="cd3a3-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cd3a3-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd3a3-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd3a3-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cd3a3-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cd3a3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd3a3-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 24 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="cd3a3-110">Diese Version hat eine Build-Nummer von V 3.10.42.43 und ist durch ein Selbst-Update im Oktober 2020 allgemein verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="cd3a3-111">Update Release 24</span><span class="sxs-lookup"><span data-stu-id="cd3a3-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cd3a3-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="cd3a3-112">Bug fixes</span></span>

<span data-ttu-id="cd3a3-113">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="cd3a3-113">**Sales**</span></span>

<span data-ttu-id="cd3a3-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cd3a3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd3a3-115">Problem beim Festlegen der Standardpreisliste der Produkte.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="cd3a3-116">Die Leistung des Angebotsgewinns ist aufgrund der eingebetteten Preisliste und der Kopie der Rollenpreisdatensätze langsam.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="cd3a3-117">**Projektvertrag/Vertriebs-Hub** > **Produktposition/Bestellpositionsmenge** wird automatisch auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="cd3a3-118">Erhöhen Sie die Systemberechtigungen beim Lesen von Preislisten.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="cd3a3-119">Kopieren Sie die Kundenadressfelder **address1_freighttermscode** und **address1_shippingmethodcode** nach Angebot/Auftrag.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="cd3a3-120">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="cd3a3-120">**Time and Expense**</span></span>

<span data-ttu-id="cd3a3-121">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cd3a3-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd3a3-122">Das **Zeiterfassungsraster** unterstützt kein **Nur Datum** -Zeitverhalten.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="cd3a3-123">**Zeiteintrag** wird nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="cd3a3-124">Eine manuelle Aktualisierung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-124">A manual refresh is required.</span></span>
- <span data-ttu-id="cd3a3-125">Die Zeiteinträge können nicht aus einer Zuweisung importiert werden, wenn die Zuweisungen einer Ressource unterbrochen sind (0 Stunden).</span><span class="sxs-lookup"><span data-stu-id="cd3a3-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="cd3a3-126">Stellen Sie beim Erstellen eines Zeiteintrags den Start auf den gleichen Wert ein wie **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="cd3a3-127">Aktivieren Sie die Massenbearbeitung für die Zeiteingabe erneut.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="cd3a3-128">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="cd3a3-128">**Resource Management**</span></span>

<span data-ttu-id="cd3a3-129">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cd3a3-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd3a3-130">Wenn Sie versuchen, den Status einer Buchung zwischen zwei Tagen ohne Anforderung zu aktualisieren, wird eine null-ref-Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="cd3a3-131">Fehler beim Laden der **Abstimmungsansicht**.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="cd3a3-132">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="cd3a3-132">**Project Management**</span></span>

<span data-ttu-id="cd3a3-133">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="cd3a3-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd3a3-134">Die automatische Speicherung wird im **Projektplan** beim Wechsel von **Manuell** zu **Automatisch** nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-134">In the **Project Schedule** , when changing from **Manual** to **Auto** , auto save is not completing.</span></span>
- <span data-ttu-id="cd3a3-135">Aufwandskosten sollten nicht zur Abweichung auf dem **Projektverfolgungsraster** berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="cd3a3-136">Inkonsistentes Verhalten für **Schätzungs-Tag** -Spalten während des Ladens versus Änderungen vom Typ **Zeitphase**.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="cd3a3-137">Die tatsächlichen Kosten eines Projekts spiegeln möglicherweise nicht die Gesamtsummen von **Tatsächliche Transaktionen** wider.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="cd3a3-138">Das **geschätzte Enddatum** auf der Registerkarte **Zusammenfassung** stimmt nicht mit dem **PSP-Zeitplan** überein.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="cd3a3-139">**Aktuelle Stunden aktualisieren** beim Ausrücken funktioniert nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="cd3a3-140">Ein Projektmanager außerhalb des **Unternehmenseinheit** -Stamms kann kein Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="cd3a3-141">Änderungen an der Aufgabe oder Kategorie unter **Ausgabenschätzungen** werden nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="cd3a3-142">**Kopie des Vertrags** kopiert die Rechnungspläne und den Ausführungsstatus.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="cd3a3-143">Die Schaltfläche **Tatsächliche Transaktionen aktualisieren** berechnet Zusammenfassungsaufgaben falsch.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="cd3a3-144">Microsoft Project-Add-In: Behebung eines Nullreferenzfehlers, wenn ein Teammitglied eine leere Ressourceneinheit hat.</span><span class="sxs-lookup"><span data-stu-id="cd3a3-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

