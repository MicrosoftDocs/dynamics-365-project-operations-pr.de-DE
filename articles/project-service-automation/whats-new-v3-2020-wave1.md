---
title: Neuigkeiten und Änderungen in Project Service Automation, Version 3.x wave 1 2020
description: Dieses Thema enthält Informationen über Neuigkeiten und Änderungen in Project Service Automation, Version 3, Wave 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721977"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="d6819-103">Neuigkeiten und Änderungen in Project Service Automation, Version 3.x Wave 1 2020</span><span class="sxs-lookup"><span data-stu-id="d6819-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="d6819-104">Das Thema zeigt die wichtigsten Überlegungen zum Upgrade bei der Umstellung auf die neueste Version von Project Service Automation (PSA) Version 3.x Wave 1 2020.</span><span class="sxs-lookup"><span data-stu-id="d6819-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="d6819-105">Zeiteintrag</span><span class="sxs-lookup"><span data-stu-id="d6819-105">Time entry</span></span>
<span data-ttu-id="d6819-106">Die Zeiteingabe wurde erweitert, um Funktionen für die Erweiterung der Zeiteingabe in mehr Kundenszenarien bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d6819-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="d6819-107">Dies beinhaltet die Möglichkeit, Eintragstypen hinzuzufügen, die nun ein spezifisches Verhalten basierend auf dem Feldschemanamen **Zeiteingabeeinstellungen** steuern und angezeigt werden als **Zeitquelle**.</span><span class="sxs-lookup"><span data-stu-id="d6819-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="d6819-108">Üpgradeüberlegung</span><span class="sxs-lookup"><span data-stu-id="d6819-108">Upgrade consideration</span></span>
<span data-ttu-id="d6819-109">Um diese Funktionalität zu unterstützen, wurden die Rollen in PSA mit neuen Berechtigungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d6819-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="d6819-110">Diese Berechtigungen gewähren Lesezugriff auf die neue Entität, **Zeiteingabeeinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d6819-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="d6819-111">Benutzer, die Zeit protokollieren müssen, sollte die Benutzerrolle **Zeiteintrag Benutzer** zusätzlich zu bestehenden Rollen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d6819-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="d6819-112">Diese Rolle enthält die neuen Funktionen und stellt sicher, dass die Zeiteingabe weiterhin funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d6819-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="d6819-113">Derzeit erweiterte Zeiteintragsänderungen</span><span class="sxs-lookup"><span data-stu-id="d6819-113">Currently extended time entry changes</span></span>
<span data-ttu-id="d6819-114">Um die Auswirkungen der Zeiteingabe auf die aktuellen Benutzer zu minimieren, ist diese Rollenänderung die einzige Grundvoraussetzung, die für die weitere Nutzung der Zeiteingabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d6819-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="d6819-115">Wenn Sie benutzerdefinierte Ansichten oder separate Zeiteingabeerfahrungen erstellt haben, müssen Sie die Option **Zeiteingabeeinstellung** Felder auf den richtigen PSA-Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6819-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
