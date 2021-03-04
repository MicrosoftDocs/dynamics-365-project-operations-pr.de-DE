---
title: Neuigkeiten und Änderungen in Project Service Automation, Version 3.x wave 1 2020
description: Dieses Thema enthält Informationen über Neuigkeiten und Änderungen in Project Service Automation, Version 3, Wave 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150937"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="05bee-103">Neuigkeiten und Änderungen in Project Service Automation, Version 3.x Wave 1 2020</span><span class="sxs-lookup"><span data-stu-id="05bee-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="05bee-104">Das Thema zeigt die wichtigsten Überlegungen zum Upgrade bei der Umstellung auf die neueste Version von Project Service Automation (PSA) Version 3.x Wave 1 2020.</span><span class="sxs-lookup"><span data-stu-id="05bee-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="05bee-105">Zeiteintrag</span><span class="sxs-lookup"><span data-stu-id="05bee-105">Time entry</span></span>
<span data-ttu-id="05bee-106">Die Zeiteingabe wurde erweitert, um Funktionen für die Erweiterung der Zeiteingabe in mehr Kundenszenarien bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="05bee-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="05bee-107">Dies beinhaltet die Möglichkeit, Eintragstypen hinzuzufügen, die nun ein spezifisches Verhalten basierend auf dem Feldschemanamen **Zeiteingabeeinstellungen** steuern und angezeigt werden als **Zeitquelle**.</span><span class="sxs-lookup"><span data-stu-id="05bee-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="05bee-108">Zur Unterstützung dieser Funktionalität wurde eine neue Lösung mit dem Namen TESA (Time, Expense, Statusing, Approvals) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05bee-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="05bee-109">Üpgradeüberlegung</span><span class="sxs-lookup"><span data-stu-id="05bee-109">Upgrade consideration</span></span>
<span data-ttu-id="05bee-110">Um diese Funktionalität zu unterstützen, wurden die Rollen in PSA mit neuen Berechtigungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="05bee-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="05bee-111">Diese Berechtigungen gewähren Lesezugriff auf die neue Entität, **Zeiteingabeeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="05bee-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="05bee-112">Benutzer, die Zeit protokollieren müssen, sollte die Benutzerrolle **Zeiteintrag Benutzer** zusätzlich zu bestehenden Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="05bee-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="05bee-113">Diese Rolle enthält die neuen Funktionen und stellt sicher, dass die Zeiteingabe weiterhin funktioniert.</span><span class="sxs-lookup"><span data-stu-id="05bee-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="05bee-114">Wenn Sie über benutzerdefinierte App-Module verfügen, die alle Formulare für die Zeiteintragsentität enthalten, müssen Sie das **Formular für Schnellerfassung für TESA-Zeiteintrag** aus dem Modul entfernen.</span><span class="sxs-lookup"><span data-stu-id="05bee-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="05bee-115">Derzeit erweiterte Zeiteintragsänderungen</span><span class="sxs-lookup"><span data-stu-id="05bee-115">Currently extended time entry changes</span></span>
<span data-ttu-id="05bee-116">Um die Auswirkungen der Zeiteingabe auf die aktuellen Benutzer zu minimieren, ist diese Rollenänderung die einzige Grundvoraussetzung, die für die weitere Nutzung der Zeiteingabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="05bee-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="05bee-117">Wenn Sie benutzerdefinierte Ansichten oder separate Zeiteingabeerfahrungen erstellt haben, müssen Sie die Option **Zeiteingabeeinstellung** Felder auf den richtigen PSA-Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="05bee-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
