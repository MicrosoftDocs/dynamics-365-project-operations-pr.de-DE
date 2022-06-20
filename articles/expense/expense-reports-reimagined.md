---
title: Neu gestaltete Spesenabrechnungen (enthält Video)
description: Dieser Artikel erklärt die überarbeitete und neu gestaltete Eingabe von Spesenabrechnungen.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c74b4b70722af72bc66dba0662813c29d3d1df04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930271"
---
# <a name="expense-reports-reimagined"></a>Neu gestaltete Spesenabrechnungen

Der Eintrag in der Ausgabenabrechnung wurde neu gestaltet, um den Prozess zu vereinfachen und die zum Ausfüllen einer Abrechnung erforderliche Zeit zu verkürzen. Hier sind die Hauptkomponenten der neuen Ausgabenerfahrung:

- Ein neuer Arbeitsbereich für die Ausgabenverwaltung, mit dem Sie auf die Ausgaben Ihrer Stellvertretung zugreifen können.
- Eine neue Erfahrung für den Belegabgleich, um Belege auf Kopfzeilenebene besser anzuzeigen und das Anhängen von Belegen an Ausgabenpositionen zu vereinfachen.
- Ein neues schreibgeschütztes Raster, mit dem Sie viel mehr Kostenzeilen und andere Spalten mit Daten anzeigen können. Sie können jetzt alle aufgelisteten und geteilten Zeilen zusammen mit den übergeordneten Ausgaben anzeigen.
- Ein vereinfachtes Fenster zum Bearbeiten von Ausgaben.
- Überarbeitete Fehler-, Warn- und Richtlinienmeldungen, um den richtigen Kontext und das richtige Verständnis des Problems sowie dessen Behebung bereitzustellen. Wir haben einige der Meldungen entfernt, die angezeigt wurden, bevor Benutzer ihre Aufgaben erledigen und die Probleme beheben konnten.
- Eine neue Seite zum Angeben der erforderlichen Felder, optionalen Felder und der Felder, die nicht enthalten sein sollten. Diese Seite hilft, die Anzahl der Felder zu reduzieren, die festgelegt werden müssen.
- Ein neues Erscheinungsbild für Ausgabenabrechnungen, sodass die Berichte nicht mehr so aussehen, als wären sie für Buchhaltungsmitarbeiter konzipiert.

Um die neue Funktion einzuschalten, verwenden Sie den **Arbeitsbereich Funktionsverwaltung**, um die Funktion **Neu gestaltete Spesenabrechnungen** einzuschalten. Wenn Sie diese Funktion aktivieren, werden die folgenden Aktionen ausgeführt:

- Der bestehende Ausgabenarbeitsbereich wird durch den neuen Arbeitsbereich ersetzt.
- Ein neuer Menüpunkt für die Sichtbarkeit der Kostenfelder wurde hinzugefügt.
- Es werden keine vorhandenen Menüelemente für Ausgabenabrechnungen (die vorhandene Seite) oder Ausgabenabrechnungsfelder entfernt.
- Workflows und Genehmigungen führen Sie weiterhin zur vorhandenen Seite mit den Ausgabenabrechnungen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

## <a name="new-features"></a>Neue Funktionen

| Neue Funktion | Beschreibung |
|---|----|
| Ausgabenfeldsichtbarkeit | Auf einer neuen Einrichtungsseite können Sie festlegen, welche Felder für eine Organisation deaktiviert werden sollen. Sie können auch festlegen, welche Felder erforderlich sein sollen und welche Felder empfohlen werden. |
| Erforderliche Felder | Mit der neuen einfachen Konfiguration können Sie einige Felder erforderlich machen, ohne das Richtlinien-Framework verwenden zu müssen. |
| Optionale Felder | Eine zweite Seite für optionale Felder wird hinzugefügt. Auf diese Weise haben Mitarbeiter nicht das Gefühl, die Felder festlegen zu müssen, aber die Felder sind dennoch leicht zugänglich. |
| Nicht angehängte Belege hinzufügen | Die Möglichkeit, der Ausgabenabrechnung nicht angehängte Belege hinzuzufügen, ist im Arbeitsbereich und in der Ausgabenabrechnung besser sichtbar. |
| Verbessertes Messaging | Es gibt eine bessere Übersicht über Ausgabenabrechnungen mit Warnungen oder Fehlern. |
| Reduzierung der Nachrichten in der Nachrichtenleiste| Die Anzahl der Infolog-Nachrichten wurde verringert, und es wurde versucht, in vielen Fällen zu verhindern, dass doppelte Nachrichten angezeigt werden. |
| Gemeinsame Aktionen wurden zusammengefasst | Die Benutzeroberfläche wurde mit einer neuen Aktionsschaltfläche für die meisten gängigen Aktionen auf Positionsebene und mit einer Ellipsenschaltfläche (...) für Kopfzeilen und andere weniger häufige Aktionen bereinigt. |
| Neuer Arbeitsbereich zur Erhöhung der Sichtbarkeit | Ein neuer Arbeitsbereich vereint Funktionen und Links, mit denen Benutzer in verschiedene Bereiche wechseln können. |
| Vorhandene Ausgaben und Belege während der Ausgabenerstellung hinzufügen | Bei der Erstellung von Spesenabrechnungen können Sie alle Ausgaben hinzufügen oder nicht angehängte Ausgaben auswählen. Nicht angehängte Ausgaben sind Ausgaben, die aus dem Kreditkarten-Feed des Unternehmens importiert wurden, oder Ausgaben, die vom Benutzer manuell erstellt, aber nicht an eine Spesenabrechnung angehängt wurden.|
| Wechselkursrechner | Es wurde ein Wechselkursrechner hinzugefügt, mit dem Sie den Wechselkurs für Transaktionen mit mehreren Währungen aus eigener Tasche berechnen können. |
| Speichern und Hinzufügen neuer Ausgabenpositionen | Die Schaltflächen **Speichern** und **Neu** sind bei der Eingabe neuer Ausgaben verfügbar, mit denen Sie schnell Ausgabenpositionen eingeben können. |
| Bessere Sichtbarkeit in geteilte und aufgeschlüsselte Positionen | Aufgeschlüsselte und geteilte Positionen werden direkt der Liste der Ausgaben hinzugefügt, um die Sichtbarkeit zu erhöhen und um leicht festzustellen, ob Fehler vorliegen. |
| Anzeige von Unterkategorie-Details in Einzelposten-Zeilen | Aufgelistete Positionen einer übergeordneten Ausgabe zeigen die Unterkategoriebezeichnungen in der Ausgabenabrechnung an. Mit der Aufstellung können Sie die granularen Details auf einen Blick überprüfen.|
|Wiederkehrende Ausgaben schnell aufschlüsseln | Der neu gestaltete Spesenarbeitsbereich bietet die Möglichkeit, wiederkehrende Ausgaben schnell aufzuschlüsseln, indem Unterkategorie, Startdatum und Menge hinzugefügt werden. Die Menge bezieht sich auf die Häufigkeit, mit der die Gebühr über einen kontinuierlichen Zeitraum wiederholt wird. |
| Belege während der Auflistung anzeigen | Belege können während der Auflistung angezeigt werden. |
| Barvorschussauswahl | Wählen Sie einen oder mehrere Barvorschüsse aus, um eine einzelne Ausgabentransaktion durchzuführen. |
| Barvorschusssaldo | Überprüfen Sie den Barvorschusssaldo in Echtzeit, wenn Sie einen Speseneintrag für genehmigte und bezahlte Barvorschüsse erstellen. |

Die erste Version konzentriert sich auf Ausgabenabrechnungsszenarien. In jedem Ausgabenabrechnungs- oder Genehmigungsszenario wird weiterhin die vorhandene Ausgabenabrechnung verwendet.


Die folgenden Funktionen werden im Arbeitsbereich für neu gestaltete Spesenabrechnungen nicht unterstützt, sind aber für zukünftige Versionen geplant: 

- Reiseanforderungsintegration
- Speseneintrag pro Tag
- Unterstützung für temporäre Genehmiger
- Möglichkeit zum Anzeigen des Workflow-Verlaufs


[!INCLUDE[footer-include](../includes/footer-banner.md)]
