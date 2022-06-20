---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Project Service Automation Updateversion 28, V3, zur Verfügung stehen.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930593"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 28 neu sind oder geändert wurden. Diese Version hat die Buildnummer V3.10.46.32 und ist allgemein über ein Self-Update im Januar 2021 verfügbar.

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
