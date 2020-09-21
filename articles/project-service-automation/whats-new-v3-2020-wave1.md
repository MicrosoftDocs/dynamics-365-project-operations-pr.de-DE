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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Neuigkeiten und Änderungen in Project Service Automation, Version 3.x Wave 1 2020
Das Thema zeigt die wichtigsten Überlegungen zum Upgrade bei der Umstellung auf die neueste Version von Project Service Automation (PSA) Version 3.x Wave 1 2020.

## <a name="time-entry"></a>Zeiteintrag
Die Zeiteingabe wurde erweitert, um Funktionen für die Erweiterung der Zeiteingabe in mehr Kundenszenarien bereitzustellen. Dies beinhaltet die Möglichkeit, Eintragstypen hinzuzufügen, die nun ein spezifisches Verhalten basierend auf dem Feldschemanamen **Zeiteingabeeinstellungen** steuern und angezeigt werden als **Zeitquelle**.

### <a name="upgrade-consideration"></a>Üpgradeüberlegung
Um diese Funktionalität zu unterstützen, wurden die Rollen in PSA mit neuen Berechtigungen aktualisiert. Diese Berechtigungen gewähren Lesezugriff auf die neue Entität, **Zeiteingabeeinstellungen**.

Benutzer, die Zeit protokollieren müssen, sollte die Benutzerrolle **Zeiteintrag Benutzer** zusätzlich zu bestehenden Rollen zugewiesen werden. Diese Rolle enthält die neuen Funktionen und stellt sicher, dass die Zeiteingabe weiterhin funktioniert.

### <a name="currently-extended-time-entry-changes"></a>Derzeit erweiterte Zeiteintragsänderungen
Um die Auswirkungen der Zeiteingabe auf die aktuellen Benutzer zu minimieren, ist diese Rollenänderung die einzige Grundvoraussetzung, die für die weitere Nutzung der Zeiteingabe erforderlich ist. Wenn Sie benutzerdefinierte Ansichten oder separate Zeiteingabeerfahrungen erstellt haben, müssen Sie die Option **Zeiteingabeeinstellung** Felder auf den richtigen PSA-Wert festlegen.
