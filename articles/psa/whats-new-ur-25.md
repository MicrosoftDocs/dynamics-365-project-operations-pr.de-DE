---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 25, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 25, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922543"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 25 neu sind oder geändert wurden. Diese Version hat die Buildnummer V 3.10.43.76 und ist allgemein über ein Self-Update im Oktober 2020 verfügbar.

## <a name="update-release-25"></a>Update Release 25

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Das folgende Problem wurde behoben:

- Zeiterfassungstabelle mit zusätzlichen Daten basierend auf einem zu großen Intervall, das abgerufen wird.

**Ressourcenverwaltung**

Das folgende Problem wurde behoben:

- Paketbereitstellungscode hinzugefügt, um den Universal Resource Scheduling-Patch-Import zu überspringen, wenn bereits ein Patch einer höheren Version vorhanden ist.

**Projektmanagement**

Die folgenden Probleme wurden behoben:

- Korrigierte Rundungs- und Wechselkursdifferenzen führten zu falschen geplanten Kosten im Projektverfolgungsraster.
- Unterstützen Sie die Möglichkeit, zwei oder mehr Reaktionsraster im **Projekt**-Formular anzuzeigen.
- Validierung bereitgestellt, um die Möglichkeit zu adressieren, eine Aufgabe nach dem Enddatum des Kalenders zuzuweisen, was zu einer fehlgeschlagenen Ressourcenzuweisung führt.
- Verbesserte Fehlerbehandlung zur Behebung der Nullreferenz-Ausnahme, die aus folgenden Gründen generiert wurde:

    - **PreValidateProjectTeamMemberCreate**-Plug-In
    - **PreValidateProjectTaskCreate** wenn eine Projektaufgabe ohne zugehöriges Projekt erstellt wird
    - **PreProjectTeamMemberCreate**-Plug-In
    - **PostProjectTeamMemberDelete**-Plug-In
    - **PreValidateProjectTaskDelete**-Plug-In

**Vertrieb**

Die folgenden Probleme wurden behoben:

- Verbesserte Fehlerbehandlung zur Behebung von Nullreferenzausnahmen, die von **Projekt kopieren: Schätzungen HelperResource Management** generiert wurden.
- **Nicht bereit für die Rechnungsstellung** in einem **Rückstandsprotokoll über Zeit- und Materialberechnung** löscht den Abrechnungsstatus nicht.
- Falsch beschriftete **Preise**-Schaltflächen auf den Registerkarten **Rollenpreis** und **Katalogartikel** wurden korrigiert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
