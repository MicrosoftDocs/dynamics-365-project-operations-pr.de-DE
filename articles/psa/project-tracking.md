---
title: Projektfortschritt und Kostenverbrauch
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektfortschritts und des Kostenverbrauchs.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0b69cee49e028b98bbb32e4a7e7aedf5479527dc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148012"
---
# <a name="project-progress-and-cost-consumption"></a>Projektfortschritt und Kostenverbrauch

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche. Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen. Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.

## <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht **Aufwandsnachverfolgung** nachverfolgt den Fortschritt von Aufgaben im Zeitplan. Sie vergleicht die tatsächlichen Aufwandsstunden für eine Aufgabe mit den geplanten Aufwandsstunden der Aufgabe. Project Service Automation verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

Anfänglich bei der Aufgabenerstellung: Die geplanten Kosten werden auf die geschätzten Kosten bei Abschluss gesetzt. Sobald die tatsächlichen Transaktionen für die Aufgabe aufgezeichnet wurden, wird in der Verfolgungsansicht für Aufwand Folgendes berechnet

- Fortschritt in Prozent = Tatsächlicher bisheriger Aufwand ÷ Schätzung bei Fertigstellung (EAC) 
- Schätzung bis Abschluss (EAC) = Schätzung bei Fertigstellung (EAC) – Tatsächlicher bisheriger Aufwand 
- EAC = Verbleibender Aufwand + Tatsächlicher bisheriger Aufwand 
- Hochgerechnete Aufwandsabweichung = geplanter Aufwand – EAC

Project Service Automation zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an. Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird. Daher liegt die Aufgabe im Zeitplan zurück. Wenn die EAC kürzer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe schneller als ursprünglich geplant abgeschlossen wird. Daher ist die Aufgabe im Zeitplan voraus.

## <a name="reprojecting-effort"></a>Erneute Hochrechnung des Aufwands

Es ist üblich, das ein Projektmanager die ursprünglichen Vorkalkulationen für eine Aufgabe erneut überprüft. Erneute Hochrechnungen für ein Projekt spiegeln die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider. Wir empfehlen Projektmanagern jedoch nicht, die Baselinezahlen zu ändern, da die Projektbaseline die sichere Informationsquelle für den Zeitplan und die Kostenvorkalkulation des Projekt darstellt, der alle am Projekt Beteiligten zugestimmt haben.

Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für Aufgaben durchführen kann:

- Er kann die standardmäßige ETC mit einer neuen Vorkalkulation des tatsächlichen verbleibenden Aufwands für die Aufgabe außer Kraft setzen. 
- Er kann den standardmäßigen Fortschritt in Prozent mit einer neuen Vorkalkulation des tatsächlichen Fortschritts für die Aufgabe außer Kraft setzen.

Jeder dieser Ansätze führt zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für eine Aufgabe. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben

Der Aufwand für Zusammenfassungsaufgaben oder Containeraufgaben kann erneut hochgerechnet werden. Unabhängig davon, ob der Benutzer eine erneute Hochrechnung für die Zusammenfassungsaufgaben anhand des verbleibenden Aufwands oder des Fortschritts in Prozent durchführt, müssen folgende Berechnungen durchgeführt werden:

- Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.
- Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.
- Die neuen BK für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet. 
- Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten werden die ETC und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet. Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe. 
- Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.

### <a name="cost-tracking-view"></a>Die Ansicht „Kostennachverfolgung“ 

Die Ansicht **Kostennachverfolgung** vergleicht die tatsächlichen Kosten für eine Aufgabe mit den geplanten Kosten. 

> [!NOTE]
> Diese Ansicht enthält ausschließlich Arbeitskosten und keine Kosten aus den Ausgabenschätzungen. 

Project Service Automation verwendet die folgenden Formeln, um die Metrik zur Nachverfolgung zu berechnen:

Wenn eine Aufgabe erstellt wird, entsprechen die geplanten Kosten den geschätzten Gesamtkosten. Nachdem die tatsächlichen Transaktionen für die Aufgabe aufgezeichnet wurden, wird in der **Verfolgungsansicht** für Kosten Folgendes berechnet:

 - Verbrauchte Kosten in Prozent = Tatsächliche bisherige Kosten ÷ Geschätzte Kosten bei Abschluss für die Aufgabe
 - Kosten bis Abschluss (CTC) = Geschätzte Kosten bei Abschluss – Tatsächliche bisherige Kosten
 - Geschätzte Kosten bei Abschluss = CTC + Tatsächliche bisherige Kosten
 - Hochgerechnete Kostenabweichung = Geplante Kosten – Geschätzte Kosten bei Abschluss

Eine Hochrechnung der Kostenabweichung für die Aufgabe wird angezeigt. Wenn die geschätzten Kosten bei Abschluss größer als die geplanten Kosten sind, wird prognostiziert, dass die Aufgabe mehr als ursprünglich geplant kosten wird. Daher tendiert sie zu einer Überschreitung des Budgets. Wenn die geschätzten Kosten bei Abschluss niedriger als die geplanten Kosten sind, wird prognostiziert, dass die Aufgabe weniger als ursprünglich geplant kosten wird und zu einer Unterschreitung des Budgets tendiert.

## <a name="project-managers-reprojection-of-cost"></a>Erneute Kostenhochrechnung des Projektmanagers

Wenn für den Aufwand eine erneute Hochrechnung durchgeführt wird, werden die CTC, die geschätzten Kosten bei Abschluss, die verbrauchten Kosten in Prozent und die hochgerechnete Kostenabweichung in der Ansicht **Kostennachverfolgung** neu berechnet.

## <a name="project-status-summary"></a>Zusammenfassung des Projektstatus

Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an. Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.

## <a name="status-summary-fields"></a>Felder der Statuszusammenfassung

Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an. Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen. Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben. Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]