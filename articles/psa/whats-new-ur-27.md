---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 27, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 27, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146662"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 27 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.45.98 und ist im durch ein Selbst-Update im Januar 2021 verfügbar.

## <a name="update-release-27"></a>Update Release 27

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Allgemein**

Die folgenden Probleme wurden behoben:

- Von Plug-Ins in Project Service Automation generierte Protokolle wurden nicht auf automatisches Löschen festgelegt.
- Die automatische Aktualisierung schlägt fehl, da die Project Service Automation-Lösung ein Legacy-Null-NavBarArea- und -Titelelement enthält.

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Der Raster **Zeiteintrag** zeigt falsche Daten für **TimeZone Independent** Datumsverhalten.
- Der Raster **Zeiteintrag** erstellt falsche Zeit für **TimeZone Independent** Datumsverhalten.
- Die Aufgabensuche ist nicht auf das ausgewählte Projekt auf der Seite **Zeiteintrag bearbeiten** beschränkt.
- Die Zeitgenehmigung für Zeiteinträge außerhalb des Projekts ist blockiert, da das System nach einem  Projektgenehmiger sucht.
- Bei korrekten Einträgen in tatsächlichen Transaktionen wird eine falsche Fehlermeldung angezeigt.
- Wenn eine Aufgabe einen Nullwert für die tatsächlichen Kosten enthält und die Projektsummen aktualisiert werden, tritt der folgende Fehler auf: Gegebener Schlüssel nicht im Wörterbuch vorhanden.
- In bestimmten Fällen zeigen die Filter **Gruppiere nach** auf der Registerkarte **Projektschätzung** keine Kostenvoranschläge an.
- **Sommerzeit** Intervall ist für Zeiteinträge nicht korrekt.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Caching-Verbesserungen, die die Leistung beim Laden der Seite **Projekt** verbessern.
- Veraltete Geschäftsregel, die verhindert, dass Projektaufgaben erledigt werden.
- Microsoft Project Add-In-Konturen berücksichtigen den Kalender des Add-Ins nicht, was zu falschen Ressourcenanforderungen führt.
- Durch das Erstellen von Projekten aus Vorlagen werden Zuweisungsdaten falsch festgelegt und die Möglichkeit zum Generieren von Ressourcenanforderungen verhindert.
- Benutzer kann nicht auf die Optionen **Kategorie**, **Beschreibung**, **Status** über die Tastatur zugreifen.
- Die tatsächlichen Verkaufswerte des Projekts enthalten keine Gebühren- und Materialverkaufswerte.
- Aggregation von tatsächlichen Verkäufen und tatsächlichen Kosten erfolgen bei Verwendung unterschiedlicher Wechselkurse fehlerhaft.
- Die Beschreibung in der **Standardarbeitsstundenvorlage** ist irreführend.
- Das Einrücken einer Aufgabe entfernt die **Kategorie** in der Benutzeroberfläche bis zur Aktualisierung nicht.
- Eine fehlende Validierung, um sicherzustellen, dass ein Projekt über sein Enddatum hinaus verschoben wird, ist nicht zulässig.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Eine Nullreferenzausnahme wird in einer Projektangebotszeile generiert, weil **Import aus Projektschätzung** sichtbar ist, wenn kein Projekt ausgewählt wurde.
- Der folgende Fehler Objektreferenz nicht auf eine Instanz eines Objekts festgelegt tritt beim Schließen eines Angebots als **Gewonnen** auf.
- Der Anpassungsstatus muss während der tatsächlichen Stornierung festgelegt werden, während ein Projekt von einer Vertragszeile getrennt wird.
- Wenn Dynamics 365 Field Service und Project Service Automation beide installiert sind, werden die Optionen **Preise sperren** und **Verwenden Sie die aktuelle Preisgestaltung** nicht gleichzeitig auf der Seite **Rechnung** angezeigt.
- Für die japanische Sprache gibt es eine inkonsistente Übersetzung mit anderen kalenderbasierten Seiten.
- **Aktivieren** und **Deaktivieren** wurden von den Entitäten **Preislistenverband** in Project Service Automation entfernt.
