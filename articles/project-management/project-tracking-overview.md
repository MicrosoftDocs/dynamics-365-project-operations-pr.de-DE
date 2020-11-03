---
title: Projektverfolgung – Übersicht
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektfortschritts und des Kostenverbrauchs.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076375"
---
# <a name="project-tracking-overview"></a>Projektverfolgung – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche. Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen. Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.

## <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht **Aufwandsnachverfolgung** verfolgt den Fortschritt von Aufgaben im Zeitplan, indem die für eine Aufgabe aufgewendeten tatsächlichen Arbeitsstunden mit den geplanten Arbeitsstunden der Aufgabe verglichen werden. Dynamics 365 Project Operations verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

- **Fortschritt in Prozent** : Tatsächlicher bisheriger Aufwand ÷ Schätzung bei Fertigstellung (EAC) 
- **Schätzung bis Abschluss (ETC)** : Geplanter Aufwand – tatsächlicher bisheriger Aufwand 
- **EAC** : Verbleibender Aufwand + Tatsächlicher bisheriger Aufwand 
- **Hochgerechnete Aufwandsabweichung** : Geplanter Aufwand – EAC

Project Operations zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an. Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird und hinter dem Zeitplan zurückliegt. Wenn die EAC kleiner ist als der geplante Aufwand, wird prognostiziert, dass die Aufgabe kürzer als ursprünglich geplant dauern wird und vor dem Zeitplan liegt.

## <a name="reprojecting-effort"></a>Erneute Hochrechnung des Aufwands

Projektmanager überprüfen häufig die ursprünglichen Vorkalkulationen für eine Aufgabe. Erneute Hochrechnungen für ein Projekt spiegeln die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider. Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern. Dies hängt damit zusammen, dass die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.

Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für Aufgaben durchführen kann:

- Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen. 
- Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.

Jeder Ansatz führt zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben

Der Aufwand für Zusammenfassungsaufgaben oder Containeraufgaben kann erneut hochgerechnet werden. Unabhängig davon, ob der Benutzer eine erneute Hochrechnung für die Zusammenfassungsaufgaben anhand des verbleibenden Aufwands oder des Fortschritts in Prozent durchführt, müssen folgende Berechnungen durchgeführt werden:

- Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.
- Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.
- Die neuen BK für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet. 
- Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten werden die ETC und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet. Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe. 
- Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.

### <a name="cost-tracking-view"></a>Die Ansicht „Kostennachverfolgung“ 

Die Ansicht **Kostennachverfolgung** vergleicht die tatsächlichen Kosten für eine Aufgabe mit den geplanten Kosten dieser Aufgabe. 

> [!NOTE]
> Diese Ansicht enthält ausschließlich Arbeitskosten und keine Kosten aus den Ausgabenschätzungen. Project Operations verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

- **Verbrauchte Kosten in Prozent** : Tatsächliche bisherige Kosten ÷ Geschätzte Kosten bei Abschluss
- **Kosten bis Abschluss (CTC)** : Geplante Kosten – Tatsächliche bisherige Kosten
- **EAC** : Verbleibende Kosten + Istkosten, die bis heute bezahlt wurden
- **Hochgerechnete Kostenabweichung** : Geplante Kosten – EAC

Eine Hochrechnung der Kostenabweichung für die Aufgabe wird angezeigt. Wenn die EAC größer als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe mehr als ursprünglich geplant kosten wird. Daher tendiert sie zu einer Überschreitung des Budgets. Wenn die EAC niedriger als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe weniger als ursprünglich geplant kosten wird. Daher tendiert sie zu einer Unterschreitung des Budgets.

## <a name="project-managers-reprojection-of-cost"></a>Erneute Kostenhochrechnung des Projektmanagers

Wenn für den Aufwand eine erneute Hochrechnung durchgeführt wird, werden die CTC, die BK, die verbrauchten Kosten in Prozent und die hochgerechnete Kostenabweichung in der Ansicht **Kostennachverfolgung** neu berechnet.

## <a name="project-status-summary"></a>Zusammenfassung des Projektstatus

Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an. Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.

## <a name="status-summary-fields"></a>Felder der Statuszusammenfassung

Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an. Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen. Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben. Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.
