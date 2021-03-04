---
title: Neu gestaltete Spesenabrechnungen
description: Dieses Thema enthält Informationen zu der neu gestalteten und neu entworfenen Erfahrung für die Erfassung von Ausgabenabrechnungen.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122792"
---
# <a name="expense-reports-reimagined"></a>Neu gestaltete Spesenabrechnungen

Der Eintrag in der Ausgabenabrechnung wurde neu gestaltet, um den Prozess zu vereinfachen und die zum Ausfüllen einer Abrechnung erforderliche Zeit zu verkürzen. Hier sind die Hauptkomponenten der neuen Ausgabenerfahrung:

- Ein neuer Arbeitsbereich für die Ausgabenverwaltung, mit dem Sie auf die Ausgaben Ihrer Stellvertretung zugreifen können.
- Eine neue Erfahrung für den Belegabgleich, um Belege auf Kopfzeilenebene besser anzuzeigen und das Anhängen von Belegen an Ausgabenpositionen zu vereinfachen.
- Ein neues schreibgeschütztes Raster, mit dem Sie viel mehr Ausgabenpositionen und zusätzliche Datenspalten anzeigen können. Sie können jetzt alle aufgelisteten und geteilten Zeilen zusammen mit den übergeordneten Ausgaben anzeigen.
- Ein vereinfachtes Fenster zum Bearbeiten von Ausgaben.
- Überarbeitete Fehler-, Warn- und Richtlinienmeldungen, um den richtigen Kontext und das richtige Verständnis des Problems sowie dessen Behebung bereitzustellen. Wir haben einige der Meldungen entfernt, die angezeigt wurden, bevor Benutzer ihre Aufgaben erledigen und die Probleme beheben konnten.
- Eine neue Seite zum Angeben der erforderlichen Felder, optionalen Felder und der Felder, die nicht enthalten sein sollten. Diese Seite hilft, die Anzahl der Felder zu reduzieren, die festgelegt werden müssen.
- Ein neues Erscheinungsbild für Ausgabenabrechnungen, sodass die Berichte nicht mehr so aussehen, als wären sie für Buchhaltungsmitarbeiter konzipiert.

Wenn Sie die neue Erfahrung aktivieren möchten, verwenden Sie den **Funktionsverwaltung**-Arbeitsbereich zum Aktivieren der **Neu gestaltete Ausgabenabrechnungen**-Funktion. Wenn Sie diese Funktion aktivieren, werden die folgenden Aktionen ausgeführt:

- Der bestehende Ausgabenarbeitsbereich wird durch den neuen Arbeitsbereich ersetzt.
- Ein neuer Menüpunkt für die Sichtbarkeit der Kostenfelder wurde hinzugefügt.
- Es werden keine vorhandenen Menüelemente für Ausgabenabrechnungen (die vorhandene Seite) oder Ausgabenabrechnungsfelder entfernt.
- Workflows und Genehmigungen führen Sie weiterhin zur vorhandenen Seite mit den Ausgabenabrechnungen.

## <a name="getting-started-video-for-new-users"></a>Video mit den ersten Schritten für neue Benutzer

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Das Video [Ausgabenerfahrung in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (siehe oben) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="new-features"></a>Neue Funktionen

| Neue Funktion | Beschreibung des Dataflows |
|---|----|
| Ausgabenfeldsichtbarkeit | Auf einer neuen Einrichtungsseite können Sie angeben, welche Felder für eine Organisation deaktiviert werden sollen, welche Felder erforderlich sein sollen und welche Felder empfohlen werden. |
| Erforderliche Felder | Mit der neuen einfachen Konfiguration können Sie einige Felder erforderlich machen, ohne das Richtlinien-Framework verwenden zu müssen. |
| Optionale Felder | Eine zweite Seite für optionale Felder wird hinzugefügt. Auf diese Weise haben Mitarbeiter nicht das Gefühl, die Felder festlegen zu müssen, aber die Felder sind dennoch leicht zugänglich. |
| Nicht angehängte Belege hinzufügen | Die Möglichkeit, der Ausgabenabrechnung nicht angehängte Belege hinzuzufügen, ist im Arbeitsbereich und in der Ausgabenabrechnung besser sichtbar. |
| Verbessertes Messaging | Es gibt eine bessere Übersicht über Ausgabenabrechnungen mit Warnungen oder Fehlern. |
| Reduzierung der Nachrichten in der Nachrichtenleiste| Die Anzahl der Infolog-Nachrichten wurde verringert, und es wurde versucht, in vielen Fällen zu verhindern, dass doppelte Nachrichten angezeigt werden. |
| Gemeinsame Aktionen wurden zusammengefasst | Die Benutzeroberfläche wurde mit einer neuen Aktionsschaltfläche für die meisten gängigen Aktionen auf Positionsebene und mit einer Ellipsenschaltfläche (...) für Kopfzeilen und andere weniger häufige Aktionen bereinigt. |
| Neuer Arbeitsbereich zur Erhöhung der Sichtbarkeit | Ein neuer Arbeitsbereich vereint Funktionen und Links, mit denen Benutzer in verschiedene Bereiche wechseln können. |
| Vorhandene Ausgaben und Belege während der Ausgabenerstellung hinzufügen | Wenn Sie Ausgabenabrechnungen erstellen, können Sie alle oder ausgewählte Ausgaben und Belege hinzufügen. |
| Wechselkursrechner | Es wurde ein Wechselkursrechner hinzugefügt, mit dem Sie den Wechselkurs für Transaktionen mit mehreren Währungen aus eigener Tasche berechnen können. |
| Speichern und Hinzufügen neuer Ausgabenpositionen | Die Schaltflächen **Speichern** und **Neu** sind bei der Eingabe neuer Ausgaben verfügbar, mit denen Sie schnell Ausgabenpositionen eingeben können. |
| Bessere Sichtbarkeit in geteilte und aufgeschlüsselte Positionen | Aufgeschlüsselte und geteilte Positionen werden direkt der Liste der Ausgaben hinzugefügt, um die Sichtbarkeit zu erhöhen und um leicht festzustellen, ob Fehler vorliegen. |
| Belege während der Auflistung anzeigen | Belege können während der Auflistung angezeigt werden. |

Die erste Version konzentriert sich auf Ausgabenabrechnungsszenarien. In jedem Ausgabenabrechnungs- oder Genehmigungsszenario wird weiterhin die vorhandene Ausgabenabrechnung verwendet.

Die folgenden Funktionen sind auf der vorhandenen Seite vorhanden, auf der neuen Seite jedoch noch nicht. Diese Funktionen werden in den nächsten Versionen wieder eingeführt:

- Genehmigungen
- Kreditorengenehmigungen und die Möglichkeit, die Buchhaltung zu bearbeiten
- Mehrere Eintragungspunkte
- Reiseanforderungsintegration
- Sichtbarkeit der Datenentität für das Ausgabenfeld
- Eintrag für Tagesausgaben
- Workflow auf Positionsebene
- Unterstützung für temporäre Genehmiger
- Erweiterte Auflistung


[!INCLUDE[footer-include](../includes/footer-banner.md)]