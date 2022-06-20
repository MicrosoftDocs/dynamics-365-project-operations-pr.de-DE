---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 34, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 34, V3, verfügbar sind.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928661"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 34, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.55.38 und ist allgemein über ein Self-Update im Juli 2021 verfügbar.

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
