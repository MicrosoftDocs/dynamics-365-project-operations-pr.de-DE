---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 35, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 35, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574027"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 35 aufgeführt. Diese Version hat die Build-Nummer V3.10.56.110 und ist allgemein über ein Self-Update im September 2021 verfügbar.

## <a name="update-release-35"></a>Update Release 35

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Zeit und Ausgaben**

- Die das Projekt genehmigende Person erhält einen Leseberechtigungsfehler, wenn sie Ausgabeneingaben mit einer **Projektgenehmiger**-Rolle genehmigt.
- Die das Projekt genehmigende Person erhält einen Schreibberechtigungsfehler bei **msdyn_projectapproval**, wenn sie einen genehmigten Zeiteintrag mit einer **Projektgenehmiger**-Rolle storniert.
- Wenn Sie **Woche kopieren** in einem Zeiteintrag im Dynamics 365 for Phone – Project Resource Hub-App-Modul auswählen, tritt der folgende Fehler auf: „...\OfficeProductivity_RibbonRules.js.map: HTTP error: Status Code 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE.“
- Die **Wiederholen**-Richtlinie genehmigt automatisch Einträge, die zuvor abgelehnt wurden.
- Das **Zulassungssätze**-Unterraster zeigt nicht anwendbare Menübandaktionen.
- Symbole fehlen für **Projektaufgabe** und **Ressourcenrolle** bei der **Zeiteingabe**-Entität.
- Wenn Sie Ressourcenzuweisungen importieren, haben importierte Zeiteinträge nicht die richtige Dauer für Zuweisungen, die durch Aufgaben im manuellen Modus erstellt wurden.
- **Löschen** fehlt auf der Seite **Erweiterte Suche für Zeiterfassungsdatensätze**.
- **Speichern** fehlt auf der Seite **Informationen zur Zeiteingabe**. Dieses Problem verhindert, dass Änderungen gespeichert werden, wenn die Seite geschlossen wird.

**Projektplanung**

- Die **Ressourcenzuweisung**- und **Ressourcenabgleich**-Raster sortieren gruppierte Attribute nicht alphabetisch.
- Aufgaben können nicht erstellt werden, wenn das Datumsverhalten an **Nur Datum** angepasst ist.

**Ressourcenverwaltung**

- Wenn Dynamics 365 Field Service und Project Service Automation installiert sind, treten Überlagerungsprobleme auf, wenn **Ressourcenanforderungsbezogene Ansicht** einer Hauptseite zugeordnet ist.
- Ein Doppelklick auf **Speichern** in dem **Teammitglied Schnell erstellen**-Dialogfeld verhindert, dass die Ressourcenanforderung erstellt wird.

**Vertrieb**

- Eine Ausnahme wird ausgelöst, wenn Sie eine Aufgabe löschen, die einem Angebot mit dem Status **Gewonnen** zugeordnet ist.
