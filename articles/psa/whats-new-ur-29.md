---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 29, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 29, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948631"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 29 aufgeführt. Diese Version hat die Build-Nummer V3.10.47.7 und ist im Allgemeinen über ein Selbstupdate im Februar 2021 verfügbar.

## <a name="update-release-29"></a>Update Release 29

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Benutzer sehen keine Arbeitsstunden, die an arbeitsfreien Tagen im Zeiteintragsraster protokolliert wurden.
- Genehmigte Speseneinträge können im Raster bearbeitet werden.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Fehlende Validierungslogik, um sicherzustellen, dass die Aufwandsstunden für die Ressourcenzuweisung nicht negativ sind.
- Die benutzerdefinierte Aktion **AssignResourcesForTask** aktualisiert alle Felder anstatt nur geänderter Felder.
- Beim Kopieren eines Projekts in einer Umgebung mit Plug-Ins oder Workflows, die im **CreateProject**-Ereignis registriert sind, wird das Attribut **msdyn_bulkgenerationstatus** nicht aktualisiert, wenn **CopyWBSToProject** fehlschlägt.
- Wenn Sie den Projektkalender erweitern, werden die Arbeitstage nicht in aufsteigender Reihenfolge sortiert, was dazu führt, dass einige Aktualisierungen von Projektaufgaben fehlschlagen.
- Das Ändern des Projektmanagers für ein vorhandenes Projekt löst die Standardlogik der Organisationseinheit aus.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Die Registerkarte **Vertragsleistung** auf der Seite **Vertrag** schlägt während der Initialisierung stillschweigend fehl, wenn keine Vertragspositionen vorhanden sind.