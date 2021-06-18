---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 31, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 31, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945534"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 31 aufgeführt. Diese Version hat die Build-Nummer V3.10.52.77 und ist allgemein über ein Selbstupdate im Mail 2021 verfügbar.

## <a name="update-release-31"></a>Update Release 31

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Befehlsschaltflächen für die Zeiteintragssteuerung auf der Seite **Buchbare Ressource** waren verwirrend.
- Eine Nullreferenzausnahme wurde in **Project.SetTrackingFields** bei der Genehmigung eines Zeiteintrags generiert.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- **Teammitglied erstellen** zeigt die Metadateneinstellung für das Buchungssetup für **Status der festgeschriebenen Standardbuchung** nicht korrekt an.
- Fehler beim Beim Upgrade von PSA 1.X auf 3.X bei **UpgradeResourceRequirements**.


**Vertrieb**

Die folgenden Probleme wurden behoben:

- Der tatsächliche Umsatz rechnet die Beträge im Tracking-Raster in die Projektwährung um.
- Der Währungsstandard ist unklar, wenn Journalzeilen, Angebotszeilen und Vertragszeilen in Szenarien erstellt werden, in denen die Basiswährung einer Organisation von der Projektwährung abweicht.
- Die Abfrage **Ausstehende Korrekturjournalvalidierung** wird nicht nach Projekt gefiltert.
- Verbleibende Verkäufe werden für ein Projekt falsch berechnet.
- Angebote, die auf einem Kontakt basieren, schlagen fehl, wenn sie ohne eine Preisliste erstellt werden.
- Bei der Auswahl von **Rechnung bestätigen** wird kein Verarbeitungs-Drehfeld angezeigt.
- Bei der Auswahl von **Rechnung erstellen** wird kein Verarbeitungs-Drehfeld angezeigt.
- Wenn Sie ein Angebot als verloren schließen, werden die Buchungen nicht storniert.






