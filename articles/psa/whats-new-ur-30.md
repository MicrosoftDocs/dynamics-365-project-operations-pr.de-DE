---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 30, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 30, V3 aufgeführt.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852853"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 30 aufgeführt. Diese Version hat die Build-Nummer V3.10.51.61 und ist allgemein über ein Selbstupdate im April 2021 verfügbar.

## <a name="update-release-30"></a>Update Release 30

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Ein Fehler tritt auf, wenn Sie einen Zeiteintrag auf der Seite **Schnellerstellung** erstellen und speichern, wenn das Feld **Rolle** entfernt wird.
- Der Zeiteingabefilter wendet den falschen Filteroperator an.
- Kopierte Arbeitszeittabellen werden bei der Auswahl von **Woche kopieren** auf die Zeiteintragssteuerung nicht automatisch angezeigt.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:

- Wenn Sie eine Buchung verlängern, ist der der harten Buchung zugewiesene Buchungsstatus falsch. Bei der Verlängerung einer Buchung wird der Buchungsstatus berücksichtigt, der als **Zugesagt** in den Metadaten des Buchungs-Setups definiert ist.
- Wenn kein gültiger Buchungsstatus angegeben ist, ist die Fehlermeldung nicht korrekt lokalisiert.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Projekte können nicht in einer Währung erstellt werden und enthalten verwandte Aufgaben in einer anderen Währung.

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Wenn eine Preisliste kopiert wird, werden die Preise nicht aktualisiert.
- Das Schließen eines Angebots als gewonnen schlägt fehl, wenn das Kostendetail einen Ursprungswert hat.
- In der **Projektaufgabe**-Entität wurde **Geschätzte Kosten** umbenannt in **Geplante Kosten (Basis)**.
- Eine Nullreferenzausnahme wird generiert, wenn Rechnungen erstellt oder gelöscht werden.