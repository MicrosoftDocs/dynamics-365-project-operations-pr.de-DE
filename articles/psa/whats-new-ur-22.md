---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 22, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 22, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150982"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation Update Release 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 22 aufgeführt. Diese Version hat die Build-Nummer V 3.10.33.48 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.

## <a name="update-release-22"></a>Update Release 22

### <a name="bug-fixes"></a>Fehlerkorrekturen



**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- **Zeiteinträge** werden nach dem Import nicht automatisch im Zeiteinträge-Zeitplan hinzugefügt.
- Die Rasterdatumsauswahl für **Zeiteintrag** erkennt die regionalen Einstellungen eines Benutzers nicht.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- Im manuellen Modus werden Änderungen an den **Ressourcenzuweisung**-Konturen nicht erkannt, wenn **Ressourcenanforderungen** generiert werden.
- **Ressourcenanforderungen** unterstützen keine benutzerdefinierte Anforderungsstatus.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Durch Doppelklick auf EstimateGridControl werden niederländische Formatzahlen nicht korrekt analyisiert.
- Zugwiesene Stunden werden nicht korrekt aktualisiert, wenn Zuweisungen mithilfe des Microsoft Project-Desktop-Client-Add-In geändert werden.
- Die Raster Projektnachverfolgung und Vorkalkulationen zeigen einen falschen Vertriebswährungscode an, wenn die Vertragswährung sich von der Kundenwährung unterscheidet und die Organisation dazu konfiguriert ist, Währungscodes statt Währungssymbolen anzuzeigen.
- Das Enddatum eines Team-Mitglieds wird um einen Tag verlängert, wenn der Arbeitsstundenzeitplan 24 Stunden pro Tag beträgt.
- Wenn Sie im Projektzeitplan einer Aufgabe eine Transaktionskategorie hinzufügen, wird dadurch nicht das automatische Speichern ausgelöst.
- Der folgende Fehler wird angezeigt, wenn ein Teammitglied zur Projektvorlage hinzugefügt wird: „Ressourcenanforderungen können nicht den Projektvorlagen zugeordnet werden“. 
- Das Menüleisten-Regelskript „msdyn.Approval.CanApproveOrReject“ zeigt einen Timeout-Fehler an.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Eine Prüfungsfehlermeldung wird nicht angezeigt, wenn eine Einstandspreisliste in der Preislisten-Suche für Formular/Entität „Neue Angebotsprojekt-Preisliste“ ausgewählt ist.
- Wenn Sie das Angebot als gewonnen schließen, navigieren Sie nicht zum erstellten Vertrag, wenn sich ein dem Angebot beigefügter BPF in der Endphase befindet.
- Das Stornieren **Nicht in Rechnung gestellter Verkäufe** wird mit den ursprünglichen Kosten verknüpft, wenn ein Zeiteintrag zurückgerufen wird.
- Nach Auswahl der Schaltfläche **Bestätigen** ändert sich der Rechnungsstatus nicht in **Bestätigt**, es sei denn, die Rechnung wird aktualisiert.
