---
title: Neuigkeiten und Änderungen in Project Service Automation, Version 3.x wave 1 2020
description: Dieses Thema enthält Informationen über Neuigkeiten und Änderungen in Project Service Automation, Version 3, Wave 1 2020.
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
ms.openlocfilehash: a88b777c54ce54935d5483f616f3a24724ee192d40fbfd5d514f990e958dd5ea
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002105"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Neuigkeiten und Änderungen in Project Service Automation, Version 3.x Wave 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Das Thema zeigt die wichtigsten Überlegungen zum Upgrade bei der Umstellung auf die neueste Version von Project Service Automation (PSA) Version 3.x Wave 1 2020.

## <a name="time-entry"></a>Zeiteintrag
Die Zeiteingabe wurde erweitert, um Funktionen für die Erweiterung der Zeiteingabe in mehr Kundenszenarien bereitzustellen. Dies beinhaltet die Möglichkeit, Eintragstypen hinzuzufügen, die nun ein spezifisches Verhalten basierend auf dem Feldschemanamen **Zeiteingabeeinstellungen** steuern und angezeigt werden als **Zeitquelle**. Zur Unterstützung dieser Funktionalität wurde eine neue Lösung mit dem Namen TESA (Time, Expense, Statusing, Approvals) hinzugefügt.

### <a name="upgrade-consideration"></a>Üpgradeüberlegung
Um diese Funktionalität zu unterstützen, wurden die Rollen in PSA mit neuen Berechtigungen aktualisiert. Diese Berechtigungen gewähren Lesezugriff auf die neue Entität, **Zeiteingabeeinstellungen**.

Benutzer, die Zeit protokollieren müssen, sollte die Benutzerrolle **Zeiteintrag Benutzer** zusätzlich zu bestehenden Rollen zugewiesen werden. Diese Rolle enthält die neuen Funktionen und stellt sicher, dass die Zeiteingabe weiterhin funktioniert.

Wenn Sie über benutzerdefinierte App-Module verfügen, die alle Formulare für die Zeiteintragsentität enthalten, müssen Sie das **Formular für Schnellerfassung für TESA-Zeiteintrag** aus dem Modul entfernen.

### <a name="currently-extended-time-entry-changes"></a>Derzeit erweiterte Zeiteintragsänderungen
Um die Auswirkungen der Zeiteingabe auf die aktuellen Benutzer zu minimieren, ist diese Rollenänderung die einzige Grundvoraussetzung, die für die weitere Nutzung der Zeiteingabe erforderlich ist. Wenn Sie benutzerdefinierte Ansichten oder separate Zeiteingabeerfahrungen erstellt haben, müssen Sie die Option **Zeiteingabeeinstellung** Felder auf den richtigen PSA-Wert festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]