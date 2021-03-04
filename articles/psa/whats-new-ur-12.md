---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 12, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143827"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="d66f3-103">Project Service Automation Update Release 12, V3</span><span class="sxs-lookup"><span data-stu-id="d66f3-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d66f3-104">Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben.</span><span class="sxs-lookup"><span data-stu-id="d66f3-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="d66f3-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="d66f3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d66f3-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d66f3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d66f3-107">Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d66f3-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="d66f3-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d66f3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d66f3-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 12 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d66f3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="d66f3-110">Diese Version hat eine Build-Nummer von V3.10.2.34 und ist im durch ein Selbst-Update im Oktober 2019 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d66f3-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="d66f3-111">Update Release 12</span><span class="sxs-lookup"><span data-stu-id="d66f3-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d66f3-112">Bugfixes</span><span class="sxs-lookup"><span data-stu-id="d66f3-112">Bug fixes</span></span>

- <span data-ttu-id="d66f3-113">Zeit und Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d66f3-113">Time and Expense</span></span>

    - <span data-ttu-id="d66f3-114">Behoben: Zeiteingabefehlermeldungen wurden mit relevanterem Kontext aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d66f3-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="d66f3-115">Behoben: Zeiteingaberaster und Zeitplan zeigen die vertikale Bildlaufleiste bei Bedarf korrekt an.</span><span class="sxs-lookup"><span data-stu-id="d66f3-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="d66f3-116">Behoben: Übermittelte oder genehmigte Zeiteinträge können genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="d66f3-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="d66f3-117">Behoben: Die Meldung zum Abbrechen des Bestätigungsdialogs wurde korrigiert, um den Status der Genehmigung bei Änderung von **Genehmigt** zu **Eingereicht** zu reflektieren.</span><span class="sxs-lookup"><span data-stu-id="d66f3-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="d66f3-118">Behoben: **Preis**, **Einheit** und **Menge** Felder sind jetzt im Ausgaben-Datensatz gesperrt, nachdem er genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="d66f3-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="d66f3-119">Projektmanagement</span><span class="sxs-lookup"><span data-stu-id="d66f3-119">Project Management</span></span>

    - <span data-ttu-id="d66f3-120">Behoben: **Neu** Aktion auf **Teammitglied** Hauptformular wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="d66f3-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="d66f3-121">Behoben: Ressourcenzuweisungen wurden aktualisiert, um ungenaue Rundungsfehler zu berücksichtigen, die zu einer Verschiebung des Enddatums einer Aufgabe führten.</span><span class="sxs-lookup"><span data-stu-id="d66f3-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="d66f3-122">Behoben: Im Aufgabenraster werden dem Benutzer relevante serverseitige Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d66f3-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="d66f3-123">Behoben: Der Name des Teammitglieds wird jetzt in der Aufgabenauswahl anstelle des Positionsnamens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d66f3-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="d66f3-124">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="d66f3-124">Resource Management</span></span>

    - <span data-ttu-id="d66f3-125">Behoben: Ressourcenbedarfsdetails für Projekte, die aus einer Vorlage erstellt wurden, verwenden jetzt den Projektkalender.</span><span class="sxs-lookup"><span data-stu-id="d66f3-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="d66f3-126">Behoben: Fertigkeiten und Kompetenzen werden jetzt standardmäßig von den Rollenstammdaten bis zum Ressourcenbedarf, der für diese Rolle erstellt wurde, übernommen.</span><span class="sxs-lookup"><span data-stu-id="d66f3-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="d66f3-127">Sales</span><span class="sxs-lookup"><span data-stu-id="d66f3-127">Sales</span></span>

    - <span data-ttu-id="d66f3-128">Behoben: Objekt-IDs, die im Formular **Hauptvertrag** gefunden wurde, duplizieren.</span><span class="sxs-lookup"><span data-stu-id="d66f3-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="d66f3-129">Behoben: Die Logik wurde aktualisiert, um die **Angebotsanalyse** Registerkarte sichtbar zu machen, damit das Metadaten-Setup der Registerkarte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d66f3-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="d66f3-130">Behoben: Abrechnungsdatum auf dem aktuellen Datensatz stammt jetzt vom Datum der Zeit-/Ausgabenerfassung und nicht vom Datum der Genehmigung.</span><span class="sxs-lookup"><span data-stu-id="d66f3-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
