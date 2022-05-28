---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 43, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 43, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: fcf18a24b3bc354a16a415368063133743e79696
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710007"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 43 aufgeführt. Diese Version hat die Build-Nummer V3.10.74.200 und ist allgemein über ein Selbstupdate im Mail 2022 verfügbar.

## <a name="update-release-43"></a>Update Release 43

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.


**Zeit und Ausgaben**

- Beim Importieren von Zeiteinträgen aus Buchungen oder Ressourcenbelegungen bleibt der Bezug zur zugehörigen buchbaren Ressource nicht erhalten.
- Wenn das Zeiteintragsraster auf Vollbild erweitert ist, funktioniert das Navigieren im Raster mit der Tabulatortaste nicht.
- Beim Absenden eines Zeiteintrags, der von einem anderen Benutzer erstellt wurde, wird das **Eingereicht von**-Feld fälschlicherweise mit dem Benutzer ausgefüllt, der die Arbeitszeittabelle erstellt hat.
