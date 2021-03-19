---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 20, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 20, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280667"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="df2d2-103">Project Service Automation Update Release 20, V3</span><span class="sxs-lookup"><span data-stu-id="df2d2-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="df2d2-104">Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben.</span><span class="sxs-lookup"><span data-stu-id="df2d2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="df2d2-105">Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.</span><span class="sxs-lookup"><span data-stu-id="df2d2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="df2d2-106">Diese Version ist mit Dynamics 365 9.x kompatibel.</span><span class="sxs-lookup"><span data-stu-id="df2d2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="df2d2-107">Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren.</span><span class="sxs-lookup"><span data-stu-id="df2d2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="df2d2-108">Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="df2d2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="df2d2-109">In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 20 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="df2d2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="df2d2-110">Diese Version hat die Build-Nummer V 3.10.31.37 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df2d2-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="df2d2-111">Update Release 20</span><span class="sxs-lookup"><span data-stu-id="df2d2-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="df2d2-112">Fehlerkorrekturen</span><span class="sxs-lookup"><span data-stu-id="df2d2-112">Bug fixes</span></span>

<span data-ttu-id="df2d2-113">**Projektmanagement**</span><span class="sxs-lookup"><span data-stu-id="df2d2-113">**Project Management**</span></span>

<span data-ttu-id="df2d2-114">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="df2d2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="df2d2-115">Das Importieren von Projektteammitgliedern mit einer Zuordnungsmethode, die mehrere Stunden erfordert, führt zu einer unklaren Fehlermeldung, wenn null Stunden angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="df2d2-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="df2d2-116">Benutzern wird eine falsche Fehlermeldung angezeigt, wenn die maximale Anzahl von Zeichen in das Feld **Beschreibung** für eine Projektaufgabe eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="df2d2-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="df2d2-117">Die Seite **Microsoft Dynamics 365 Project Service Automation-Add-In-Download** leitet zur englischen Download-Seite weiter, wenn die Spracheinstellungen des Benutzers auf Japanisch eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="df2d2-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="df2d2-118">Wenn ein Serverfehler auftritt, bleibt die Synchronisationsbeschriftung auf der Registerkarte **Zeitplan** des Formulars **Projekte** manchmal bestehen.</span><span class="sxs-lookup"><span data-stu-id="df2d2-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="df2d2-119">Redundante Aufgabenaktualisierungen werden an den Server gesendet, wenn eine Aufgabe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="df2d2-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="df2d2-120">**Vertrieb**</span><span class="sxs-lookup"><span data-stu-id="df2d2-120">**Sales**</span></span>

<span data-ttu-id="df2d2-121">Die folgenden Probleme wurden behoben:</span><span class="sxs-lookup"><span data-stu-id="df2d2-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="df2d2-122">Wenn im Formular **Vertrag** auf **Rechnung erstellen** doppelgeklickt wird, werden zwei Rechnungen für einen einzelnen Datensatz mit Istwerten erstellt.</span><span class="sxs-lookup"><span data-stu-id="df2d2-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="df2d2-123">In Internet Explorer 11 können Benutzer keine Ausgabeneinträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="df2d2-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="df2d2-124">Die Rückbuchung von Kosten und die Rückbuchung von nicht fakturierten Umsatz-Istwerten ist nicht verknüpft.</span><span class="sxs-lookup"><span data-stu-id="df2d2-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="df2d2-125">Die Schaltfläche **Tatsächliche Transaktionen aktualisieren** im Formular **Projekt** aktualisiert nicht die Option **Tatsächliche Aufgabenstunden**.</span><span class="sxs-lookup"><span data-stu-id="df2d2-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="df2d2-126">Das Plug-In **PreValidateProjectTeamMemberCreate** kann doppelte allgemeine buchbare Ressourcen erstellen, wenn das Attribut **msdyn_isgenericresourceprojectscoped** auf **False** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="df2d2-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="df2d2-127">**Neu berechnen** löscht die fakturierbaren Kosten für produktbasierte Angebotszeilendetails und Vertragszeilendetails.</span><span class="sxs-lookup"><span data-stu-id="df2d2-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="df2d2-128">In bestimmten Szenarien zeigt das Plug-In **PostEstimateLineUpdate** einen Nullreferenz-Ausnahmefehler an.</span><span class="sxs-lookup"><span data-stu-id="df2d2-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="df2d2-129">Die Zeitphasendauer im **Rentabilitätsanalysediagramm** stimmt nicht mit der Dauer der Kosten im Angebotszeilendetail zum Festpreis des Angebots überein.</span><span class="sxs-lookup"><span data-stu-id="df2d2-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="df2d2-130">Einheiten- und Einheitengruppenwerte sind für Ausgabenkategorien in den Formularen **Vertragszeile Details** und **Detailinformationen zur Angebotsposition** standardmäßig nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="df2d2-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="df2d2-131">**Organisationseinheits-Einstandspreis**-Listen lassen Überschneidungen bei der Datumsgültigkeit zu.</span><span class="sxs-lookup"><span data-stu-id="df2d2-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="df2d2-132">Benutzer dürfen die **Organisationseinheit** nicht ändern, wenn der Auftragstyp nicht arbeitsbasiert ist, weil dies zu einem Nullreferenz-Ausnahmefehler führt.</span><span class="sxs-lookup"><span data-stu-id="df2d2-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="df2d2-133">Beim Versuch, vom Formular **Detailinformationen zur Angebotsposition** zurück zur Registerkarte **Angebot** zu navigieren, wird das Formular aktualisiert und die Registerkarte **Zusammenfassung** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df2d2-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]