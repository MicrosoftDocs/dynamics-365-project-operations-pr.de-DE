---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 37, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 37, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727604"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 37 aufgeführt. Diese Version hat die Build-Nummer V3.10.58.120 und ist ab November 2021 durch ein Selbst-Update allgemein verfügbar.

## <a name="update-release-37"></a>Update Release 37

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Zeit und Ausgaben**
- Benutzer können einen Zeiteintrag nicht löschen, indem sie die Zelle leeren.
- Die **Meine fehlgeschlagenen Genehmigungen**-Ansicht enthält nur Projektgenehmigungen mit dem Status **Gesendet**.

**Projektmanagement**
- Benutzer erhalten beim Öffnen eines Projekts im Microsoft-Desktop-Add-In einen Nullverweis-Ausnahmefehler, wenn der Positionsname des Projektteammitglieds leer ist.
- Es gibt keine **Speichern**-Schaltfläche auf der **Projektaufgabe**-Seite, sodass Benutzer Änderungen an Aufgabendatensätzen nicht speichern können.
- Benutzer können ein Projekt nicht löschen, dessen Aufgabe einem Angebot mit dem Status zugeordnet **Gewonnen** ist.

**Vertrieb**
- Das **Währung**-Feld auf der **Projekt**-Seite wird aktualisiert, sodass es mit der Währung der angewendeten Vorlage übereinstimmt.
- Die Kosten werden für Aufgaben mit mehreren Währungen falsch berechnet.
