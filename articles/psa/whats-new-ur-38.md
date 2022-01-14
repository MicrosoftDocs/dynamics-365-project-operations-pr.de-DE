---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 38, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 38, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901487"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 38 aufgeführt. Diese Version hat die Build-Nummer V3.10.59.117 und ist im Allgemeinen über ein Selbstupdate im Dezember 2021 verfügbar.

## <a name="update-release-38"></a>Update Release 38

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Zeit und Ausgaben**

- Eine Ausnahme tritt auf, wenn die Länge der Genehmigungssatzprotokolle 100.000 Datensätze überschreitet.
- Benutzer können nicht auf das Raster **Zeiteingabe** von der Hauptseite **Zeiteingabe** zugreifen.
- Das Dialogfeld **Zeiteintrag importieren** zeigt keinen Text an, wenn keine Elemente für den Import geeignet sind.
- Benutzer können Genehmigungssätze erstellen, in denen das Feld **Zielstatus** auf **Unbekannt** gesetzt ist.

**Projektmanagement**

- Konturen werden in Ressourcenzuweisungen für UTC(+09:30) und UTC(+10:00) nicht korrekt angezeigt, wenn die Sommerzeit beginnt.
- Das Feld **Zusätzliche Spalte** für Projektstrukturpläne ist in einigen Gebietsschemas ausgeblendet.
- Die Datumsauswahl für das Kalendersteuerelement im **Projektaufgabe**-Raster ist für Chinesisch nicht richtig lokalisiert.

**Vertrieb**

- Die Werte **Vertragserfüllung** und **Tatsächliche Projektkosten** stimmen nicht überein, wenn buchbare Ressourcen mit unterschiedlichen Vertragseinheiten und Währungen Zeiteinträge übermitteln.
- Ein benutzerdefinierter Workflow zum automatischen Bestätigen von Rechnungen schlägt fehl, wenn die Rechnungen als verwaltete Lösung importiert werden. Die folgende Nachricht wird angezeigt: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException Nachricht: Ungültiger Rechnungsstatus.“
- Wenn **Stamm** als Zusammenfassungsoption ausgewählt ist und das Projekt Schätzungen aus einer Mischung von Transaktionsklassen enthält (z. B. eine Kombination aus Zeit, Ausgaben und Materialschätzung), fasst das System transaktionsklassenübergreifend als einzelne Gebührenposition zusammen.
- In Szenarien, in denen eine Aufwandsposition hinzugefügt wird, bevor eine Vertragsposition mit einem Projekt verknüpft wird, wird der richtige Preis nicht als Standardwert im Feld **Preis aktualisieren** eingegeben.
- Negative Verkaufsbeträge sind nicht zulässig bei **Projekt**‑ und **Aufgabe**-Entitäten.
