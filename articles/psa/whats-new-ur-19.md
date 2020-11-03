---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 19, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 19, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076477"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="77582-103">Project Service Automation Update Release 19, V3</span><span class="sxs-lookup"><span data-stu-id="77582-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="77582-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="77582-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="77582-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="77582-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="77582-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="77582-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="77582-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="77582-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="77582-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="77582-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="77582-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 19 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="77582-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="77582-110">Diese Version hat die Build-Nummer V3.10.30.41 und ist allgemein über ein Selbstupdate im Mail 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77582-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="77582-111">Update Release 19</span><span class="sxs-lookup"><span data-stu-id="77582-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="77582-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="77582-112">Bug fixes</span></span>

<span data-ttu-id="77582-113">**Zeit und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="77582-113">**Time and Expense**</span></span>

<span data-ttu-id="77582-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="77582-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="77582-115">Fehler, die aus Zeiteintragsimporten stammen, werden nicht korrekt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77582-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="77582-116">Das Zeiteintragsraster unterstützt das Verhalten des Felds **Nur Datum** nicht.</span><span class="sxs-lookup"><span data-stu-id="77582-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="77582-117">Projektressourcen können keine Ausgaben mit einem Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="77582-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="77582-118">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="77582-118">**Project Management**</span></span>

<span data-ttu-id="77582-119">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="77582-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="77582-120">Um zwei Ebenen untergeordnete Aufgabe verursacht eine falsche Aufwandsschätzung während der Abschlussberechnung (BK).</span><span class="sxs-lookup"><span data-stu-id="77582-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="77582-121">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="77582-121">**Sales**</span></span>

<span data-ttu-id="77582-122">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="77582-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="77582-123">Die Aktion **Neu berechnen** funktioniert nicht mit Details zu Ausgabenvertragszeilen oder Angebotszeilen.</span><span class="sxs-lookup"><span data-stu-id="77582-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="77582-124">**Preise aktualisieren** fehlt für Ausgabenschätzungen.</span><span class="sxs-lookup"><span data-stu-id="77582-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="77582-125">Kunden können keine benutzerdefinierten Vertragsstatusgründe auf der Seite **Projektvertrag** auswählen.</span><span class="sxs-lookup"><span data-stu-id="77582-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="77582-126">Kunden können beim Erstellen einer benutzerdefinierten Preisliste aus einem Angebot eine Leistungsverschlechterung feststellen.</span><span class="sxs-lookup"><span data-stu-id="77582-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="77582-127">Kunden erleben Inkonsistenzen bei Standardeinstellungen für **Einheit** auf den Seiten **Detailinformationen zur Angebotsposition** und **Vertragszeile Details**.</span><span class="sxs-lookup"><span data-stu-id="77582-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="77582-128">Wenn nicht fakturierbare Transaktionskategorieartikel einer fakturierbaren Vertragszeile hinzugefügt werden, wird der Fakturierungstyp **Nicht fakturierbar** der Transaktionskategorie nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="77582-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="77582-129">Kunden können die neu hinzugefügten Rollen und Kategorien nicht für zuvor erstellte Verträge verwenden.</span><span class="sxs-lookup"><span data-stu-id="77582-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="77582-130">Kunden erleben Leistungsverschlechterungen. Unnötige Abrufe in PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="77582-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="77582-131">Rollen, die in der Liste **Ressourcenkategorien** als nicht fakturierbar festgelegt sind, sollten der Registerkarte **Fakturierbare Rollen** als **Nicht fakturierbar** in der Vertragszeile für ein Projekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="77582-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="77582-132">Kunden können beim Erstellen eines Projekts eine Leistungsminderung feststellen, weil **GetBookableResourceIdFromUser** alle Spalten buchbarer Ressourcen und nicht nur die primäre ID abruft.</span><span class="sxs-lookup"><span data-stu-id="77582-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="77582-133">Der Entität **TransactionType** fehlt das Plug-In zur Updatevorüberprüfung, das verhindert, dass Benutzer **Einheiten** und **Einheitengruppen** eingeben, die für Transaktionstypen nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="77582-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="77582-134">Der Schritt **Entfernen** funktioniert nicht beim Zeiteintragsimport.</span><span class="sxs-lookup"><span data-stu-id="77582-134">The **Remove** step does not work for time entry import.</span></span>
