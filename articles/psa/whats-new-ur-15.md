---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 15, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 15, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076481"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation Update Release 15, V3

Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 15 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.5.28 und ist im durch ein Selbst-Update im Januar 2020 verfügbar.

## <a name="update-release-15"></a>Update Release 15 

### <a name="enhancements"></a>Verbesserungen

- Projektmanagement

### <a name="bug-fixes"></a>Bugfixes

- Zeit und Ausgaben

  - Behoben: Fehlerbehandlung beim Laden in der Abstimmungsansicht hinzugefügt.
  - Behoben: Project Resource Hub: Umbenennen von **Menge** , um Mehrdeutigkeit zu reduzieren.
  - Behoben: Passen Sie die Ansicht an **Zeiteintragsspalten kopieren** , um den Typ einzuschließen.
  - Behoben: Das Bearbeiten der Zeiteintragsdauer in der Rasteransicht unter Verwendung von Dezimalzahlen führt bei einigen Zahlen zu einem unbekannten Fehler.

- Projektmanagement

  - Behoben: Das Dropdown-Menü für **In der Verfolgungsansicht verwenden** erweitert sich nun basierend auf der Breite der Optionen.
  - Behoben: Beim Verwalten von Projekten in der Zeitzone +13 können Aufgabenberechnungen zu ungenauen Ergebnissen führen.
  - Behoben: **Endzeit des Teammitglieds** wurde bei Verwendung eines 24-Stunden-Kalenders korrigiert.
  - Behoben: **BPF** im **msdyn_project** Hauptformular wieder aktiviert.
  - Behoben: Zuweisungsberechnung ignoriert einen Tag nicht mehr.
  - Behoben: Ein neues Benachrichtigungsbanner wurde zum Projektformular hinzugefügt, wenn sich die Zeitzone zwischen Benutzer und Projekt unterscheidet.

- Sales

  - Behoben: Die Suche nach Ausgabenschätzungskategorien kann zum Filtern von Duplikaten verwendet werden.
  - Behoben: Code in **PluginDomain.ExecuteInTryCatchBlock (..)** verbirgt nicht länger den Ursprung der Ausnahme.
  - Behoben: Es wird keine Fehlermeldung mehr angezeigt in **Projektsuche** in der **Angebotszeile** , wenn es mehr als 1000 Projekte gibt.
  - Behoben: Raster **Schätzungen** für Arbeitsschätzungen und Ausgabenschätzungen zeigt jetzt das richtige Währungssymbol an.
  - Behoben: Nachdem eine Organisation PSA von Update Release 14 auf Update Release 15 aktualisiert hat, wird die **Zeitplan** Registerkarte nicht mehr als leer auf dem Formular **Projekt** angezeigt.
