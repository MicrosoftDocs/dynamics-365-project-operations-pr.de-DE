---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 28, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010515"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die Funktionen und Korrekturen aufgeführt, die für Project Service Automation V3, Update Release 28, neu hinzugefügt oder geändert wurden. Diese Version hat die Build-Nummer V3.10.46.32 und ist im Januar 2021 über ein Selbstupdate verfügbar.

## <a name="update-release-28"></a>Update Release 28

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Benutzer können **Massen-Bearbeitung** verwenden, um Zeiteinträge zu aktualisieren, die genehmigt und übermittelt wurden.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- In Fällen, in denen die Aufgaben-GUID als Zahl interpretiert wird, können Aufgaben nicht zum Bearbeiten mit **Aufgabe bearbeiten** im Band auf der Seite **Projektstrukturplan** geöffnet werden.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Eine Nullreferenzausnahme wird generiert, wenn das **GetEstimatesForProject** Plug-In aufgerufen wird.
- **Als für Rechnung bereit markieren** im Meilensteinraster werden nur die teilweise aktualisierten Attribute mit Ausnahme des Attributs **InvoiceStatus** aktualisiert.



[!INCLUDE[footer-include](../includes/footer-banner.md)]