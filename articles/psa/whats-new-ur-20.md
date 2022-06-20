---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 20, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Project Service Automation Updateversion 20, V3 verfügbar sind.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913061"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation Update Release 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 20, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V 3.10.31.37 und ist allgemein über ein Selbstupdate im Juni 2020 verfügbar.

## <a name="update-release-20"></a>Update Release 20

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Das Importieren von Projektteammitgliedern mit einer Zuordnungsmethode, die mehrere Stunden erfordert, führt zu einer unklaren Fehlermeldung, wenn null Stunden angegeben sind.
- Benutzern wird eine falsche Fehlermeldung angezeigt, wenn die maximale Anzahl von Zeichen in das Feld **Beschreibung** für eine Projektaufgabe eingegeben wurde.
- Die Seite **Microsoft Dynamics 365 Project Service Automation-Add-In-Download** leitet zur englischen Download-Seite weiter, wenn die Spracheinstellungen des Benutzers auf Japanisch eingestellt sind.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
