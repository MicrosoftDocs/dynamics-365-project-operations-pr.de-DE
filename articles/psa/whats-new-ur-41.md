---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 41, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 41, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580915"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 41 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.62.162 und ist durch eine Selbstaktualisierung im März 2022 verfügbar.

## <a name="update-release-41"></a>Update Release 41

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Projektmanagement**
- Wenn Sie versuchen, ein Projekt aus einer Vorlage zu erstellen, die auf einem mit dem Desktop-Add-In erstellten Projekt basiert, wird die folgende Fehlermeldung angezeigt: „Überprüfung des Feldes „Geplante Arbeit“ der Ressourcenzuweisung: Das Enddatum jedes Zeitsegments der Ressourcenzuweisung darf nicht vor dem Startdatum liegen".

**Zeit und Ausgaben**
- Wenn Sie versuchen, einen Zeiteintrag zu löschen, wird die folgende Fehlermeldung angezeigt: „Unerwarteter Fehler im ISV-Code“.

**Vertrieb**
- Wenn Sie eine Rechnung für einen Festpreis-Meilenstein erstellen, werden die Felder **Beschreibung** und **Externe Beschreibung** nicht ausgefüllt. 
