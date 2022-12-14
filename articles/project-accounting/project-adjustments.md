---
title: Projektanpassungen
description: Dieser Artikel enthält Informationen über Projektanpassungen.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788298"
---
# <a name="project-adjustments"></a>Projektanpassungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung_

## <a name="adjustments-overview"></a>Anpassungen – Übersicht

Sie können Microsoft Dynamics 365 Project Operations so konfigurieren, dass Benutzer Änderungen an gebuchten Transaktionen vornehmen können. Sie können Projekttransaktionen individuell anpassen, oder Sie können mehrere Transaktionen gleichzeitig aus einer Liste alles Projekttransaktionen auswählen. Projektanpassungen werden beispielsweise verwendet, um den abrechenbaren Status massenhaft zu aktualisieren, Kosten nach einer Konfigurationsänderung neu zu berechnen oder Finanzierungsquellen zu aktualisieren.

Benutzer können auf verschiedene Arten auf die Projektanpassungsfunktion zugreifen:

- Durch Verwendung der Seite **Transaktionen anpassen**, auf die über **Projektmanagement und -buchhaltung** \> **Einrichtung** zugegriffen werden kann.
- Durch Verwendung der Schaltfläche **Anpassung** auf der Seite **Gebuchte Projekttransaktionen**, auf die über **Projektmanagement und -buchhaltung** \> **Transaktionen** zugegriffen werden kann.
- Über die Schaltfläche **Anpassung** auf der Seite **Gebuchte Projekttransaktionen** im Kontext eines Projekts. Auf diese Seite kann über **Projektmanagement und -buchhaltung** \> **Alle Projekte** zugegriffen werden.

Um Anpassungen zu ermöglichen, müssen Sie einen oder mehrere Transaktionsstatus von **Projektmanagement und Buchhaltung** \> **Projektmanagement und Buchhaltungsparameter** auf der **Registerkarte Allgemein** unter dem Abschnitt **Anpassung des Transaktionsstatus zulassen**. Beispiele für Transaktionsstatus sind gebuchte Transaktionen, fakturierte Transaktionen oder eliminierte Transaktionen. Jeder Transaktionsstatus, der auf **Nein** gesetzt ist, hat Transaktionen in diesem Status, die im Anpassungsprozess nicht als zur Anpassung auswählbar angezeigt werden.

Eine Konfigurationsoption mit dem Namen **Korrekturbuchung immer erstellen** ist derzeit in Projektverwaltungs- und Buchhaltungsparametern verfügbar. Sie können diese Option deaktivieren, um die ursprüngliche Transaktion zu aktualisieren, anstatt während der Anpassung in einer Teilmenge von Szenarien neue Transaktionen zu erstellen. Es wurde angekündigt, dass dieser Parameter zum 1. März 2023 veraltet sein wird. Nach dem 1. März 2023 verhält sich das System immer so, als wäre die Option aktiviert.

## <a name="adjustments-process-flow"></a>Anpassungsprozessflow

Die folgenden Schritte zeigen den typischen Ablauf für die Verarbeitung von Anpassungen.

1. Öffnen Sie die Seite **Projektanpassungen** .
2. Wählen Sie **Auswählen**, um nach Transaktionen zu suchen, die die erwarteten Kriterien für die Anpassung erfüllen.
3. Wählen Sie in der Liste der Buchungen alle Buchungen oder eine Teilmenge der Buchungen für die Anpassung aus.
4. Wählen Sie **Anpassen** und ändern Sie die Attribute in der Zeile. Wenn die Werte während der Transaktionseingabe manuell angegeben wurden, können Sie alternativ die Eingabe von Standardsystemwerten auswählen.
5. Die Liste der Transaktionen wird zurückgegeben, und in der Spalte **Ausstehende Anpassung** wird ein Häkchen angezeigt, um anzugeben, wo Änderungen vorgenommen wurden. Alle Anpassungen mit ausstehenden Änderungen werden in der unteren Hälfte der Seite angezeigt. Dort können Sie zusätzliche detaillierte Änderungen vornehmen, die über das hinausgehen, was auf der vorherigen Seite gezeigt wurde.
6. Wählen Sie **Buchen** aus, um die Anpassungstransaktionen zu buchen.

Je nach Konfiguration werden typischerweise neue Transaktionen für die Anpassung erstellt.

- Das Feld **Rechnungsstatus** auf der ursprünglichen Transaktion ist auf **Angepasst** eingestellt.
- Eine Stornierungsbuchung wird erstellt, um die ursprüngliche Buchung rückgängig zu machen, und das Feld **Status** wird auf **Angepasst** gesetzt.
- Es wird eine neue Transaktion erstellt, die die Änderungen enthält, die während des Anpassungsprozesses vorgenommen wurden.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Auswählen mehrerer gebuchter Projekttransaktionen gleichzeitig für Anpassungen und Gutschriften

Eine neue Funktion, die in Version 10.0.30 eingeführt wurde, ermöglicht die Auswahl mehrerer Buchungen zur Anpassung gleichzeitig auf der Seite **Gebuchte Projektbuchungen** .

Bevor Sie diese Funktion nutzen können, müssen Sie diese auf Ihrem System aktivieren. Administratoren können mit dem Arbeitsbereich **Funktionsverwaltung** den Status der Funktion überprüfen und ggf. aktivieren. Suchen Sie im Arbeitsbereich **Funktionsverwaltung** nach **Gebuchte Projektbuchungen für Anpassungen und Gutschriften mit Mehrfachauswahl** und wählen Sie sie aus. und wählen Sie dann **Jetzt aktivieren** aus.

Diese Funktion ermöglicht die folgenden wichtigen Funktionen:

- Sie können von der Seite mit den gebuchten Transaktionen innerhalb eines Projekts aus darauf zugreifen, indem Sie die vorhandene Schaltfläche **Anpassung** verwenden.
- Es ermöglicht eine mehrzeilige Auswahlsteuerung auf der Seite **Gebuchte Projekttransaktionen** . Sie können Filter auf die Listenseite anwenden und Ihre Datensätze auswählen, bevor Sie mit den Anpassungen beginnen.
- Sie deaktiviert die Schaltfläche **Anpassung**, wenn eine einzelne Transaktion nicht angepasst werden kann oder wenn Sie eine Kombination aus Gutschriften und Journalen zusammen statt einzeln auswählen.
- Aufgrund der Hinzufügung des Auswahlsteuerelements für mehrere Zeilen ist der Link **Zugesagte Kosten** im Menüband nicht mehr deaktiviert, wenn mehrere Zeilen ausgewählt sind.
- Es fügt die folgende Warnmeldung hinzu: „Sie haben mehr als (ausgewählte Anzahl) Datensätze zur Anpassung ausgewählt. Es kann einige Zeit dauern, mit dieser Aktion fortzufahren. Möchten Sie mit dieser Aktion fortfahren?“

Dieses Feature entfernt auch Schritt 2 aus dem Prozessablauf, der weiter oben in diesem Artikel beschrieben wurde. Daher werden alle Transaktionen, die ausgewählt wurden, bevor die Seite **Transaktionen anpassen** geöffnet wurde, in die Liste der Transaktionen für die Anpassung aufgenommen. Sie müssen nicht die Schaltfläche **Auswählen** verwenden, um danach zu suchen.

> [!NOTE] 
> Auch wenn diese Funktion deaktiviert ist, können Sie immer noch mehrere Datensätze zur Anpassung auswählen. Es bleibt jedoch nur ein Datensatz *ausgewählt*, und das Dialogfeld **Transaktionen auswählen** wird unmittelbar nach Ihrer Auswahl angezeigt offene Anpassungen.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Anpassungstransaktionsstatus, die für Anpassungen aktiviert oder deaktiviert werden können

Die folgenden Status können auf der Registerkarte **Allgemein** der Seite **Projektverwaltungs- und Abrechnungsparameter** aktiviert oder deaktiviert werden:

- Veröffentlicht
- Rechnungsvorschlag
- In Rechnung gestellt
- Geschätzt
- Entfernt
- Anfangssaldomenge (Stunde)

## <a name="adjustment-parameters"></a>Anpassungsparameter

Diese Parameter sind auf der Seite **Projektmanagement und -buchhaltungsparameter** auf der Registerkarte **Allgemein** unter der Gruppe **Anpassung** aufgeführt und ändern das Verhalten, wie Anpassungen verarbeitet werden. 

| Parametername | Beschreibung des Dataflows |
|----------------|-------------
| Anpassungsbuchung immer erstellen | Wenn dieser Parameter aktiviert ist, erstellt der Anpassungsprozess immer eine neue rückgängig gemachte Transaktion und eine neue angepasste Transaktion, wenn es finanzielle oder Berichtsauswirkungen gibt. Wenn der Parameter deaktiviert ist, aktualisiert der Anpassungsprozess die ursprüngliche Transaktion, anstatt eine Stornierung und eine neue Transaktion für ein Szenario wie eine Aktualisierung des Transaktionstexts zu erstellen. |
| Feld automatisch aktualisieren | Wenn dieser Parameter aktiviert ist, berechnet das System den Einstandspreis und den Verkaufspreis neu. |
| Anpassungsdatum als neues Projekt verwenden | Dieser Parameter wird verwendet, um Transaktionen in ein zukünftiges Buchhaltungsperiode zu verschieben, bevor das System diese Funktion unterstützte. Wir empfehlen nicht, dass Sie es verwenden, da es das Geschäftsdatum der Transaktion ändert und in einer zukünftigen Version veraltet sein wird. |
| Geschlossene Aktivitäten zulassen | Normalerweise können keine Transaktionen für abgeschlossene Aktivitäten erstellt werden. Wenn dieser Parameter aktiviert ist, wird dieses Verhalten außer Kraft gesetzt. Daher können Anpassungen für abgeschlossene Aktivitäten erstellt werden. |
