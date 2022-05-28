---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 42, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 42, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589195"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 42 aufgeführt. Diese Version hat die Build-Nummer V3.10.73.61 und ist allgemein über ein Selbstupdate im April 2022 verfügbar.

## <a name="update-release-42"></a>Update Release 42

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Zeit und Ausgaben**

- Wenn ein Arbeitszeitblatt abgelehnt wird, wird der Benutzer, der es abgelehnt hat, fälschlicherweise als **System** identifiziert.
- Beim Importieren von Zeiteinträgen fehlt der **Ressourcenkategorie**-Wert.
- Projektgenehmiger können eingereichte Projekte genehmigen, wenn ihre Berechtigungen nicht ausdrücklich auf **Kann genehmigen** festgelegt sind.

**Vertrieb**

- Wenn Ist-Kosten für Vorgänge auf Nicht-Stammebene protokolliert werden, werden die Ist-Kosten falsch aggregiert.
