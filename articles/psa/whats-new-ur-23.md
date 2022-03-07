---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 23, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 23, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996615"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation Update Release 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 23 aufgeführt. Diese Version hat eine Build-Nummer von V 3.10.34.30 und ist durch ein Selbst-Update im August 2020 allgemein verfügbar.

## <a name="update-release-23"></a>Update Release 23

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:
- Edge-Anfrage in **Projektteammitglied löschen** bearbeiten, um eine sinnvolle Ausnahme zu machen.
- Der Import von Zuweisungen führt zu einem leeren Bildschirm zum Entfernen.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- **Ressourcennutzungsraster-Ressourcenkarte** zeigt falsche Daten an, wenn die Zeitskala mehr als fünf Tage beträgt.
- Wenn Kunden eine buchbare Ressource erstellen, fügt das Plug-In die Ressource zeitweise nicht automatisch zu einer Microsoft Office 365-Gruppe hinzu.
- Die Ansicht **Abstimmung** zeigt manuelle Konturen in der Ansicht **Woche** oder **Monat** falsch an.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Eine übermäßige Anzahl von **RetrieveMultiple für Benutzereinstellungen**-Entitäten verursachen Leistungseinbußen bei Projektgenehmigungen und anderen Vorgängen.
- Die **Aufgabenplanung**-Rasterressourcensuche ist auf nur bis zu fünf Teammitglieder aus dem Projektteam beschränkt. 
- Die **Aufgabenplanung**-Rasterressourcensuche filtert keine inaktiven Ressourcen.
- Der manuelle Modus funktioniert nicht wie erwartet in der Projektplanungsstruktur.
- Das Raster **Aufgabenplanung** zeigt **Inaktive Transaktionskategorien**.
- Das Raster **Ressourcenzuweisung** wird falsch gerundet, wenn eine Aufgabe mehrere Zuordnungen hat.
- Rundungswerte unterscheiden sich zwischen geplanten Kosten und tatsächlichen Kosten für eine einzelne Aufgabe.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Durch Doppelklicken auf **Alle Transaktionskategorien abrufen** werden mehrere Zeilen erstellt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]