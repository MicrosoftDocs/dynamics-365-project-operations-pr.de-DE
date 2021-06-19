---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 32, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 32, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129665"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="d9936-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 32, V3</span><span class="sxs-lookup"><span data-stu-id="d9936-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d9936-104">Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen.</span><span class="sxs-lookup"><span data-stu-id="d9936-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d9936-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="d9936-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d9936-106">Es ist kompatibel mit Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d9936-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d9936-107">Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update.</span><span class="sxs-lookup"><span data-stu-id="d9936-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d9936-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d9936-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d9936-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 32 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9936-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="d9936-110">Diese Version hat die Build-Nummer V3.10.53.108 und ist im Juni 2021 durch eine Selbst-Aktualisierung allgemein verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9936-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="d9936-111">Update Release 32</span><span class="sxs-lookup"><span data-stu-id="d9936-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d9936-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="d9936-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="d9936-113">Allgemein</span><span class="sxs-lookup"><span data-stu-id="d9936-113">General</span></span>

- <span data-ttu-id="d9936-114">Wenn eine größere Aktualisierung fehlschlägt, sollten nur die Hauptanwendungseintrittspunkte blockiert werden, um sicherzustellen, dass auf gemeinsam genutzte Entitäten weiterhin zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9936-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="d9936-115">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9936-115">Time and Expense</span></span>

<span data-ttu-id="d9936-116">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="d9936-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9936-117">**TimeEntriesImportFromResourceAssignment** behält die Start- und Endzeiten des Konturabschnitts der Ressourcenzuweisung nicht bei.</span><span class="sxs-lookup"><span data-stu-id="d9936-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="d9936-118">Wenn Sie **Eintrag öffnen** im Raster **Zeiteingabe** auswählen, werden Sie möglicherweise daran gehindert, andere Formulare auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d9936-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="d9936-119">Beim Importieren von Zuweisungen zu Zeiteinträgen kann die Clientcode-Abfrage eine lange URL generieren, die dafür sorgt, dass die Abfrage fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d9936-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="d9936-120">In dem Raster **Zeiteingabe** bleibt der Fokus nicht im Raster, nachdem ein Wert aus einer Zelle gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="d9936-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="d9936-121">Die Schaltfläche **Ablehnen** wurde aus der Ansicht **Verarbeitungsgenehmigungen** für moderne Genehmigungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9936-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="d9936-122">Die Stabilität und Leistung der Zeiterfassungs-Massengenehmigung wird durch Deadlocks und eine nicht ordnungsgemäße Handhabung von Anpassungen im Zusammenhang mit der Entität **Zeiteingabe** beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="d9936-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="d9936-123">Projektplanung</span><span class="sxs-lookup"><span data-stu-id="d9936-123">Project Planning</span></span>

- <span data-ttu-id="d9936-124">Eine Nullverweisausnahme wird generiert, wenn Sie ein Projekt aktualisieren, das einen Nullwert im Feld **Vertragseinheit** hat.</span><span class="sxs-lookup"><span data-stu-id="d9936-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="d9936-125">**Projektsummen aktualisieren** berechnet die verbleibenden Kosten und den verbleibenden Umsatz eines Projekts falsch.</span><span class="sxs-lookup"><span data-stu-id="d9936-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="d9936-126">Redundante Preisberechnungen wirken sich auf die Leistung aus, die sich auf Aktualisierungen von Ressourcenzuweisungskonturen bezieht.</span><span class="sxs-lookup"><span data-stu-id="d9936-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="d9936-127">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="d9936-127">Resource Management</span></span>

<span data-ttu-id="d9936-128">Das folgende Problem wurde behoben:</span><span class="sxs-lookup"><span data-stu-id="d9936-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="d9936-129">Wenn die Kalenderkapazität einer buchbaren Ressource mehr als 1 beträgt, erkennt Project Service Automation die Kapazität fälschlicherweise als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d9936-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="d9936-130">Daher tritt in der Zeitplanansicht eine Endlosschleife auf.</span><span class="sxs-lookup"><span data-stu-id="d9936-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="d9936-131">Vertrieb</span><span class="sxs-lookup"><span data-stu-id="d9936-131">Sales</span></span>

<span data-ttu-id="d9936-132">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="d9936-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9936-133">Wenn eine Journalzeile mit einem benutzerdefinierten Transaktionstyp erstellt wird, tritt die folgende Nullreferenzausnahme auf: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="d9936-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="d9936-134">Rollen und Kategorien, die vor dem Kopieren eines Angebots deaktiviert werden, sollten nicht zu kostenpflichtigen Rollen und Kategorien des neu kopierten Angebots hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d9936-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="d9936-135">Das Dokumentdatum und das Abrechnungsdatum stimmen nicht mit dem Startdatum überein, das in einem Rechnungspostendetail angegeben ist, das direkt auf einem Rechnungsentwurf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d9936-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="d9936-136">Null-Referenz-Ausnahmen werden in Szenarien generiert, die sich auf die Inaktivierung von Rollen und Kategorien vor dem Kopieren eines Angebots beziehen.</span><span class="sxs-lookup"><span data-stu-id="d9936-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="d9936-137">Die Aktion **Preise aktualisieren** auf der Seite **Projekte** aktualisiert keine Ausgabenschätzungen und Materialschätzungen.</span><span class="sxs-lookup"><span data-stu-id="d9936-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
