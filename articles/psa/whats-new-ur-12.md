---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 12, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: fc92a5dcc111688159f9be5b2839b7c040404a3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119957"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation Update Release 12, V3
Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 12 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.2.34 und ist im durch ein Selbst-Update im Oktober 2019 verfügbar.

## <a name="update-release-12"></a>Update Release 12

### <a name="bug-fixes"></a>Bugfixes

- Zeit und Ausgaben

    - Behoben: Zeiteingabefehlermeldungen wurden mit relevanterem Kontext aktualisiert.
    - Behoben: Zeiteingaberaster und Zeitplan zeigen die vertikale Bildlaufleiste bei Bedarf korrekt an.
    - Behoben: Übermittelte oder genehmigte Zeiteinträge können genehmigt werden.
    - Behoben: Die Meldung zum Abbrechen des Bestätigungsdialogs wurde korrigiert, um den Status der Genehmigung bei Änderung von **Genehmigt** zu **Eingereicht** zu reflektieren.
    - Behoben: **Preis**, **Einheit** und **Menge** Felder sind jetzt im Ausgaben-Datensatz gesperrt, nachdem er genehmigt wurde.

- Projektmanagement

    - Behoben: **Neu** Aktion auf **Teammitglied** Hauptformular wurde entfernt.
    - Behoben: Ressourcenzuweisungen wurden aktualisiert, um ungenaue Rundungsfehler zu berücksichtigen, die zu einer Verschiebung des Enddatums einer Aufgabe führten.
    - Behoben: Im Aufgabenraster werden dem Benutzer relevante serverseitige Fehler angezeigt.
    - Behoben: Der Name des Teammitglieds wird jetzt in der Aufgabenauswahl anstelle des Positionsnamens angezeigt.

- Ressourcenverwaltung

    - Behoben: Ressourcenbedarfsdetails für Projekte, die aus einer Vorlage erstellt wurden, verwenden jetzt den Projektkalender.
    - Behoben: Fertigkeiten und Kompetenzen werden jetzt standardmäßig von den Rollenstammdaten bis zum Ressourcenbedarf, der für diese Rolle erstellt wurde, übernommen.

- Sales

    - Behoben: Objekt-IDs, die im Formular **Hauptvertrag** gefunden wurde, duplizieren.
    - Behoben: Die Logik wurde aktualisiert, um die **Angebotsanalyse** Registerkarte sichtbar zu machen, damit das Metadaten-Setup der Registerkarte angezeigt wird.
    - Behoben: Abrechnungsdatum auf dem aktuellen Datensatz stammt jetzt vom Datum der Zeit-/Ausgabenerfassung und nicht vom Datum der Genehmigung.
