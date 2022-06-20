---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 22, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 22, V3, verfügbar sind.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 733ee6e0d3583f21d0f58f9651920be3e3fd8cb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930639"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation Update Release 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 22, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V 3.10.33.48 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
