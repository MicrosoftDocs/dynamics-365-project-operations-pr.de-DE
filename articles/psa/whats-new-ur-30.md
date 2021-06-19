---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 30, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 30, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010425"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="2c71c-103">Neuigkeiten und Änderungen in Project Service Automation, Update Release 30, V3</span><span class="sxs-lookup"><span data-stu-id="2c71c-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2c71c-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="2c71c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2c71c-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="2c71c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2c71c-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2c71c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2c71c-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2c71c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2c71c-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="2c71c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="2c71c-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 30 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c71c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="2c71c-110">Diese Version hat die Build-Nummer V3.10.51.61 und ist allgemein über ein Selbstupdate im April 2021 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c71c-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="2c71c-111">Update Release 30</span><span class="sxs-lookup"><span data-stu-id="2c71c-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2c71c-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="2c71c-112">Bug fixes</span></span>

<span data-ttu-id="2c71c-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="2c71c-113">**Time and Expense**</span></span>

<span data-ttu-id="2c71c-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2c71c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c71c-115">Ein Fehler tritt auf, wenn Sie einen Zeiteintrag auf der Seite **Schnellerstellung** erstellen und speichern, wenn das Feld **Rolle** entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2c71c-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="2c71c-116">Der Zeiteingabefilter wendet den falschen Filteroperator an.</span><span class="sxs-lookup"><span data-stu-id="2c71c-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="2c71c-117">Kopierte Arbeitszeittabellen werden bei der Auswahl von **Woche kopieren** auf die Zeiteintragssteuerung nicht automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c71c-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="2c71c-118">**Ressourcenverwaltung**</span><span class="sxs-lookup"><span data-stu-id="2c71c-118">**Resource Management**</span></span>

<span data-ttu-id="2c71c-119">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2c71c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c71c-120">Wenn Sie eine Buchung verlängern, ist der der harten Buchung zugewiesene Buchungsstatus falsch.</span><span class="sxs-lookup"><span data-stu-id="2c71c-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="2c71c-121">Bei der Verlängerung einer Buchung wird der Buchungsstatus berücksichtigt, der als **Zugesagt** in den Metadaten des Buchungs-Setups definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c71c-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="2c71c-122">Wenn kein gültiger Buchungsstatus angegeben ist, ist die Fehlermeldung nicht korrekt lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="2c71c-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="2c71c-123">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="2c71c-123">**Project Management**</span></span>

<span data-ttu-id="2c71c-124">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2c71c-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c71c-125">Projekte können nicht in einer Währung erstellt werden und enthalten verwandte Aufgaben in einer anderen Währung.</span><span class="sxs-lookup"><span data-stu-id="2c71c-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="2c71c-126">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="2c71c-126">**Sales**</span></span>

<span data-ttu-id="2c71c-127">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="2c71c-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c71c-128">Wenn eine Preisliste kopiert wird, werden die Preise nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2c71c-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="2c71c-129">Das Schließen eines Angebots als gewonnen schlägt fehl, wenn das Kostendetail einen Ursprungswert hat.</span><span class="sxs-lookup"><span data-stu-id="2c71c-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="2c71c-130">In der **Projektaufgabe**-Entität wurde **Geschätzte Kosten** umbenannt in **Geplante Kosten (Basis)**.</span><span class="sxs-lookup"><span data-stu-id="2c71c-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="2c71c-131">Eine Nullreferenzausnahme wird generiert, wenn Rechnungen erstellt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="2c71c-131">A null reference exception is generated when invoices are created or deleted.</span></span>
