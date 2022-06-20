---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 43, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 43, V3, zur Verfügung stehen.
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915317"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 43, V3 neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.74.200 und ist allgemein über ein Selbstupdate im Mail 2022 verfügbar.

## <a name="update-release-43"></a>Update Release 43

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.


**Zeit und Ausgaben**

- Beim Importieren von Zeiteinträgen aus Buchungen oder Ressourcenbelegungen bleibt der Bezug zur zugehörigen buchbaren Ressource nicht erhalten.
- Wenn das Zeiteintragsraster auf Vollbild erweitert ist, funktioniert das Navigieren im Raster mit der Tabulatortaste nicht.
- Beim Absenden eines Zeiteintrags, der von einem anderen Benutzer erstellt wurde, wird das **Eingereicht von**-Feld fälschlicherweise mit dem Benutzer ausgefüllt, der die Arbeitszeittabelle erstellt hat.
