---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 18, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 18, V3 aufgeführt.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006645"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation Update Release 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 18 aufgeführt. Diese Version hat die Build-Nummer V3.10.8.12 und ist allgemein über ein Selbstupdate im April 2020 verfügbar.

## <a name="update-release-18"></a>Update Release 18

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

- Behoben: Die Flows **Zurückrufen**, **Anfordern**, und **Genehmigung abbrechen** lösen Ausnahmen mit unklaren Fehlermeldungen aus.
- Behoben: Wenn **Genehmigung abbrechen** für eine Ausgabe fehlschlägt, wird kein relevanter Ausnahmefehler ausgelöst.
- Behoben: Das Zeiteintragsraster behandelt arbeitsfreie Tage in Australien nach der Sommerzeitumstellung im Oktober falsch.
- Behoben: Eine falsche Standardlogik verhindert die Übermittlung von Ausgaben.
- Behoben: Wenn die Zeiteintragsgenehmigung fehlschlägt, bleibt die Genehmigung im Status **Ausstehend**.
- Behoben: SQL-Fehler bei Massengenehmigungen (Deadlock/Timeout).
- Behoben: Erhebliche Leistungsprobleme in der Benutzererfahrung, die durch die Aktualisierung der Teammitglieder beim Genehmigen von Zeiteinträgen verursacht wurden.

**Projektmanagement**

- Behoben: Die Zeitzonenbenachrichtigung wurde von der Ansicht **Abstimmung** zum Hauptformular **Projekt** verschoben.
- Behoben: Die Kalendervorlage ist beim Öffnen eines neuen Projektformulars nicht korrekt.
- Behoben: Bei chrombasierten Browsern können Benutzer vorherige Aufgaben zum Löschen nicht einfach auswählen.
- Behoben: Durch das Erstellen oder Kopieren von **Projekt aus leerer Vorlage** werden nicht verknüpfte Arbeitsaufträge abgerufen.
- Behoben: In bestimmten Grenzfällen werden beim Erstellen eines neuen Arbeitsauftrags aus dem Aufgabenraster doppelte Datensätze erstellt.
- Behoben: Im manuellen Modus können Benutzer die Startdaten der Aufgabe nicht so aktualisieren, dass sie nach dem aktuell gespeicherten Datum liegen.

**Ressourcenverwaltung**

- Behoben: Die Zwischensummenzeile der Ansicht **Abstimmung** berechnet die Buchungsabweichung nach dem Erweitern von Buchungen falsch.
- Behoben: In der Ansicht **Abstimmung** werden Ressourcenzuweisungen falsch angezeigt, wenn die buchbare Ressource einen Kalender hat, der nicht mit dem Projektkalender übereinstimmt.

**Vertrieb**

- Behoben: Wenn Zeiteinträge erneut genehmigt werden (**Genehmigen > Abbrechen >** Erneut genehmigen), wird ein Duplikat des nicht kostenpflichtigen Ist-Werts erstellt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]