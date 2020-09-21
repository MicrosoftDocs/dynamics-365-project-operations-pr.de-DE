---
title: Projektfortschritt und Kostenverbrauch
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektfortschritts und des Kostenverbrauchs.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722034"
---
# <a name="project-progress-and-cost-consumption"></a>Projektfortschritt und Kostenverbrauch

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche. Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen. Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.

## <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht **Aufwandsnachverfolgung** nachverfolgt den Fortschritt von Aufgaben im Zeitplan. Sie vergleicht die tatsächlichen Aufwandsstunden für eine Aufgabe mit den geplanten Aufwandsstunden für diese Aufgabe. PSA verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

- Fortschritt in % = tatsächlicher bisheriger Aufwand ÷ geplanter Aufwand für die Aufgabe 
- Schätzung bis Abschluss (ETC) = geplanter Aufwand – tatsächlicher bisheriger Aufwand 
- Schätzung bei Abschluss (EAC) = verbleibender Aufwand + tatsächlicher bisheriger Aufwand 
- Hochgerechnete Aufwandsabweichung = geplanter Aufwand – EAC

PSA zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an. Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird. Daher liegt die Aufgabe im Zeitplan zurück. Wenn die EAC kürzer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe schneller als ursprünglich geplant abgeschlossen wird. Daher ist die Aufgabe im Zeitplan voraus.

## <a name="re-projecting-effort"></a>Erneute Hochrechnung des Aufwands

Es ist üblich, das ein Projektmanager die ursprünglichen Vorkalkulationen für eine Aufgabe erneut überprüft. Die erneute Hochrechnung für ein Projekt spiegelt die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider. Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern, da die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.

Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für eine Aufgabe durchführen kann:

- Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen. 
- Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.

Jeder dieser Ansätze führt zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben

Der Aufwand für Zusammenfassungsaufgaben oder Behälteraufgaben kann erneut hochgerechnet werden. Unabhängig davon, ob der Benutzer eine erneute Hochrechnung für die Zusammenfassungsaufgaben anhand des verbleibenden Aufwands oder des Fortschritts in Prozent durchführt, müssen folgende Berechnungen durchgeführt werden:

- Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.
- Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.
- Die neue EAC für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet. 
- Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten werden die ETC und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet. Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe. 
- Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.

### <a name="cost-tracking-view"></a>Die Ansicht „Kostennachverfolgung“ 

Die Ansicht **Kostennachverfolgung** vergleicht die tatsächlichen Kosten für eine Aufgabe mit den geplanten Kosten dieser Aufgabe. 

> [!NOTE]
> Diese Ansicht enthält ausschließlich Arbeitskosten und keine Kosten aus den Ausgabenschätzungen. 

PSA verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

- Verbrauchte Kosten in Prozent = tatsächliche bisherige Kosten ÷ geplante Kosten für die Aufgabe
- Kosten bis Abschluss (CTC) = geplante Kosten – tatsächliche bisherige Kosten
- EAC = CTC + tatsächliche bisherige Kosten
- Hochgerechnete Kostenabweichung = geplante Kosten – EAC

Eine Hochrechnung der Kostenabweichung für die Aufgabe wird angezeigt. Wenn die EAC größer als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe mehr als ursprünglich geplant kosten wird. Daher tendiert sie zu einer Überschreitung des Budgets. Wenn die EAC niedriger als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe weniger als ursprünglich geplant kosten wird. Daher tendiert sie zu einer Unterschreitung des Budgets.

## <a name="project-managers-re-projection-of-cost"></a>Erneute Kostenhochrechnung des Projektmanagers

Wenn für den Aufwand eine erneute Hochrechnung durchgeführt wird, werden die CTC, die EAC, die verbrauchten Kosten in Prozent und die hochgerechnete Kostenabweichung in der Ansicht **Kostennachverfolgung** neu berechnet.

## <a name="project-status-summary"></a>Zusammenfassung des Projektstatus

Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an. Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.

## <a name="status-summary-fields"></a>Felder der Statuszusammenfassung

Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an. Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen. Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben. Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.
