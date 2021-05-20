---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 18, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 18, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: bd6038b3594e8507c4a441b00ddc2eb240f796dc
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949183"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="5aa7b-103">Project Service Automation Update Release 18, V3</span><span class="sxs-lookup"><span data-stu-id="5aa7b-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5aa7b-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5aa7b-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5aa7b-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5aa7b-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5aa7b-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5aa7b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5aa7b-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 18 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="5aa7b-110">Diese Version hat die Build-Nummer V3.10.8.12 und ist allgemein über ein Selbstupdate im April 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="5aa7b-111">Update Release 18</span><span class="sxs-lookup"><span data-stu-id="5aa7b-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5aa7b-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="5aa7b-112">Bug fixes</span></span>

<span data-ttu-id="5aa7b-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-113">**Time and Expense**</span></span>

- <span data-ttu-id="5aa7b-114">Behoben: Die Flows **Zurückrufen**, **Anfordern**, und **Genehmigung abbrechen** lösen Ausnahmen mit unklaren Fehlermeldungen aus.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="5aa7b-115">Behoben: Wenn **Genehmigung abbrechen** für eine Ausgabe fehlschlägt, wird kein relevanter Ausnahmefehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="5aa7b-116">Behoben: Das Zeiteintragsraster behandelt arbeitsfreie Tage in Australien nach der Sommerzeitumstellung im Oktober falsch.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="5aa7b-117">Behoben: Eine falsche Standardlogik verhindert die Übermittlung von Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="5aa7b-118">Behoben: Wenn die Zeiteintragsgenehmigung fehlschlägt, bleibt die Genehmigung im Status **Ausstehend**.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="5aa7b-119">Behoben: SQL-Fehler bei Massengenehmigungen (Deadlock/Timeout).</span><span class="sxs-lookup"><span data-stu-id="5aa7b-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="5aa7b-120">Behoben: Erhebliche Leistungsprobleme in der Benutzererfahrung, die durch die Aktualisierung der Teammitglieder beim Genehmigen von Zeiteinträgen verursacht wurden.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="5aa7b-121">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-121">**Project Management**</span></span>

- <span data-ttu-id="5aa7b-122">Behoben: Die Zeitzonenbenachrichtigung wurde von der Ansicht **Abstimmung** zum Hauptformular **Projekt** verschoben.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="5aa7b-123">Behoben: Die Kalendervorlage ist beim Öffnen eines neuen Projektformulars nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="5aa7b-124">Behoben: Bei chrombasierten Browsern können Benutzer vorherige Aufgaben zum Löschen nicht einfach auswählen.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="5aa7b-125">Behoben: Durch das Erstellen oder Kopieren von **Projekt aus leerer Vorlage** werden nicht verknüpfte Arbeitsaufträge abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="5aa7b-126">Behoben: In bestimmten Grenzfällen werden beim Erstellen eines neuen Arbeitsauftrags aus dem Aufgabenraster doppelte Datensätze erstellt.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="5aa7b-127">Behoben: Im manuellen Modus können Benutzer die Startdaten der Aufgabe nicht so aktualisieren, dass sie nach dem aktuell gespeicherten Datum liegen.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="5aa7b-128">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-128">**Resource Management**</span></span>

- <span data-ttu-id="5aa7b-129">Behoben: Die Zwischensummenzeile der Ansicht **Abstimmung** berechnet die Buchungsabweichung nach dem Erweitern von Buchungen falsch.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="5aa7b-130">Behoben: In der Ansicht **Abstimmung** werden Ressourcenzuweisungen falsch angezeigt, wenn die buchbare Ressource einen Kalender hat, der nicht mit dem Projektkalender übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="5aa7b-131">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="5aa7b-131">**Sales**</span></span>

- <span data-ttu-id="5aa7b-132">Behoben: Wenn Zeiteinträge erneut genehmigt werden (**Genehmigen > Abbrechen >** Erneut genehmigen), wird ein Duplikat des nicht kostenpflichtigen Ist-Werts erstellt.</span><span class="sxs-lookup"><span data-stu-id="5aa7b-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]