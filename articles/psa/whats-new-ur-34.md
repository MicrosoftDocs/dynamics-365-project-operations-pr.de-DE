---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 34, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 34, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 1c8ef43b953ad282a1f5fed6eeeb1e1a991e715100b66938be03b5b5f3da575e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009755"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 34 aufgeführt. Diese Version hat die Build-Nummer V3.10.55.38 und ist allgemein über ein Self-Update im Juli 2021 verfügbar.

## <a name="update-release-34"></a>Update Release 34

### <a name="bug-fixes"></a>Fehlerkorrekturen
Die folgenden Probleme wurden behoben.

**Allgemein**

- Vom Herausgeber gesteuerte Updates aktivieren den neuen modernen Genehmigungsworkflow nicht.
- Die **Zielstatus**- und **Aktionstyp**-Attribute fehlen auf der **Genehmigungssatz**-Hauptseite.

**Zeit und Ausgaben**

- Eine Rückrufanforderung kann mit dem modernen Genehmigungsflow nicht genehmigt werden.
- Das Kopieren von Zeiteinträgen einer Woche funktioniert nicht, wenn Einträge kopiert werden, die sich nicht auf den angemeldeten Benutzer beziehen.

**Projektplanung**

- Die Konturen der Ressourcenzuweisung werden beim Importieren aus dem Microsoft Project-Desktop-Add-In beschädigt.

**Ressourcenverwaltung**

- Wenn Sie ein Projekt aus dem Microsoft Project-Desktopclient-Add-In veröffentlichen, wird das Enddatum vorhandener Anforderungen geändert.
- Die Dezimalgenauigkeit überschreitet zwei Dezimalstellen im Bestätigungsdialog für die Verlängerung der Buchungen.

**Vertrieb**

- Wenn Sie einem Projektvertrag eine produktbasierte Linie mit einem vorhandenen Produkt hinzufügen, wird eine **Schlüssel nicht im Wörterbuch gefunden**-Ausnahme angezeigt.
- Leads können nicht qualifiziert werden, wenn ein Auftragstyp von einem Lead einer Opportunity zugeordnet wird.
