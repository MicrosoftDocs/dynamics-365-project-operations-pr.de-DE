---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 20, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 20, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147112"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation Update Release 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 20 aufgeführt. Diese Version hat die Build-Nummer V 3.10.31.37 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.

## <a name="update-release-20"></a>Update Release 20

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Das Importieren von Projektteammitgliedern mit einer Zuordnungsmethode, die mehrere Stunden erfordert, führt zu einer unklaren Fehlermeldung, wenn null Stunden angegeben sind.
- Benutzern wird eine falsche Fehlermeldung angezeigt, wenn die maximale Anzahl von Zeichen in das Feld **Beschreibung** für eine Projektaufgabe eingegeben wurde.
- Von der **Downloadseite für das Microsoft Dynamics 365 Project Service Automation-Add-In** wird zur englischen Downloadseite weitergeleitet, wenn Japanisch in den Spracheinstellungen des Benutzers festgelegt ist.
- Wenn ein Serverfehler auftritt, bleibt die Synchronisationsbeschriftung auf der Registerkarte **Zeitplan** des Formulars **Projekte** manchmal bestehen.
- Redundante Aufgabenaktualisierungen werden an den Server gesendet, wenn eine Aufgabe geändert wird.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Wenn im Formular **Vertrag** auf **Rechnung erstellen** doppelgeklickt wird, werden zwei Rechnungen für einen einzelnen Datensatz mit Istwerten erstellt.
- In Internet Explorer 11 können Benutzer keine Ausgabeneinträge erstellen.
- Die Rückbuchung von Kosten und die Rückbuchung von nicht fakturierten Umsatz-Istwerten ist nicht verknüpft.
- Die Schaltfläche **Tatsächliche Transaktionen aktualisieren** im Formular **Projekt** aktualisiert nicht die Option **Tatsächliche Aufgabenstunden**.
- Das Plug-In **PreValidateProjectTeamMemberCreate** kann doppelte allgemeine buchbare Ressourcen erstellen, wenn das Attribut **msdyn_isgenericresourceprojectscoped** auf **False** gesetzt ist.
- **Neu berechnen** löscht die fakturierbaren Kosten für produktbasierte Angebotszeilendetails und Vertragszeilendetails.
- In bestimmten Szenarien zeigt das Plug-In **PostEstimateLineUpdate** einen Nullreferenz-Ausnahmefehler an.
- Die Zeitphasendauer im **Rentabilitätsanalysediagramm** stimmt nicht mit der Dauer der Kosten im Angebotszeilendetail zum Festpreis des Angebots überein.
- Einheiten- und Einheitengruppenwerte sind für Ausgabenkategorien in den Formularen **Vertragszeile Details** und **Detailinformationen zur Angebotsposition** standardmäßig nicht korrekt.
- **Organisationseinheits-Einstandspreis**-Listen lassen Überschneidungen bei der Datumsgültigkeit zu.
- Benutzer dürfen die **Organisationseinheit** nicht ändern, wenn der Auftragstyp nicht arbeitsbasiert ist, weil dies zu einem Nullreferenz-Ausnahmefehler führt.
- Beim Versuch, vom Formular **Detailinformationen zur Angebotsposition** zurück zur Registerkarte **Angebot** zu navigieren, wird das Formular aktualisiert und die Registerkarte **Zusammenfassung** angezeigt.
