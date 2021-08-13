---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 16, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 16, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f577cd8407b0f12607c56891eeadb1071f659cff67bd9f086a6b3bbec6376e9d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004400"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation Update Release 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.  Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren einer bevorzugten Lösung](/dynamics365/project-service/upgrade-psa-home-page).
In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 16 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.6.34 und ist im durch ein Selbst-Update im Januar 2020 verfügbar.


## <a name="update-release-16"></a>Update Release 16

### <a name="bug-fixes"></a>Bugfixes

-   Zeit und Ausgaben

    -   Behoben: Benutzer, die versuchen, gelöschte Zeit- und Kosteneinträge zur Genehmigung einzureichen, erhalten jetzt relevante Fehlermeldungen.

-   Projektmanagement

    -   Behoben: Die in Vorlagen für Teammitglieder definierten Ressourceneinheiten werden eingehalten, und die Vorlagen werden auf ein neues Projekt angewendet.

    -   Behoben: Verbesserte Handhabung der Neuzuweisung von Datensatzbesitz.

    -   Behoben: Projekte, die gerade kopiert werden, dürfen erst kopiert werden, wenn alle Kopiervorgänge abgeschlossen sind.

-   Ressourcenverwaltung

    -   Behoben: Durch Buchung verlängern werden kurze Laufzeiten jetzt korrekt gehandhabt, und es werden keine Nullstunden mehr für erweiterte Buchungen erstellt.

    -   Behoben: Die Abstimmungsansicht wird jetzt gerendert, wenn die Projektzeitzone +5:30 GMT beträgt und die Zeit des Benutzers sich davon unterscheidet.

-   Sales

    -   Behoben: Wenn ein einer Vertragszeile zugeordnetes Projekt entfernt und ein neues Projekt zugeordnet wurde, wurden die tatsächlichen Datensätze des neuen Projekts nicht basierend auf den in der Vertragszeile definierten Abrechnungs- und Preisregeln neu bewertet. Dies wurde in dieser Version behoben. Preisgestaltung und tatsächliche Aufzeichnungen des neu zugeordneten Projekts werden rückgängig gemacht und basierend auf den Preis- und Abrechnungsregeln der Vertragszeile korrekt neu erstellt. Die tatsächlichen Aufzeichnungen des nicht zugeordneten Projekts werden ebenfalls neu bewertet und infolgedessen neu erstellt.

    -   Behoben: Eine zusätzliche Validierung wurde zum Feld **Menge** einer Vorkalkulationsposition hinzugefügt, um sicherzustellen, dass Nullwerte nicht beibehalten werden.

    -   Behoben: Wenn Istwerte eines Projekts aktualisiert wurden, wurde dem Hauptformular des Projekts eine Schaltfläche zum Aktualisieren hinzugefügt, damit Benutzer die Istwerte erneut synchronisieren können.

    -   Behoben: Wenn Benutzer ein Upgrade von 2.X auf 3.X durchführen, sind Projekte mit einem NULL-Wert für den Projektnamen zulässig.



[!INCLUDE[footer-include](../includes/footer-banner.md)]