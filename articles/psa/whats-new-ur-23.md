---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 23, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Project Service Automation Updateversion 23, V3, zur Verfügung stehen.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913028"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation Update Release 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 23, neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V 3.10.34.30 und ist durch ein Selbst-Update im August 2020 allgemein verfügbar.

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
