---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 37, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 37, V3, zur Verfügung stehen.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922497"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 37, V3 neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.58.120 und ist ab November 2021 durch ein Selbst-Update allgemein verfügbar.

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
