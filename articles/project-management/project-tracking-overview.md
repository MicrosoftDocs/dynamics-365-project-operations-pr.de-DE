---
title: Projektaufwandsverfolgung
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektaufwands und des Arbeitsfortschritts.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710939"
---
# <a name="project-effort-tracking"></a>Projektaufwandsverfolgung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche. Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen. Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.

## <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht **Aufwandsnachverfolgung** verfolgt den Fortschritt von Aufgaben im Zeitplan, indem die für eine Aufgabe aufgewendeten tatsächlichen Arbeitsstunden mit den geplanten Arbeitsstunden der Aufgabe verglichen werden. Dynamics 365 Project Operations verwendet die folgenden Formeln, um die Metriken zur Nachverfolgung zu berechnen:

- **Fortschritt in Prozent**: Tatsächlicher bisheriger Aufwand ÷ Schätzung bei Fertigstellung (EAC) 
- **Verbleibender Aufwand**: geschätzter Aufwand bei Abschluss – tatsächlicher bisheriger Aufwand 
- **EAC**: Verbleibender Aufwand + Tatsächlicher bisheriger Aufwand 
- **Hochgerechnete Aufwandsabweichung**: Geplanter Aufwand – EAC

Project Operations zeigt eine Hochrechnung der Aufwandsabweichung für die Aufgabe an. Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird und hinter dem Zeitplan zurückliegt. Wenn die EAC kleiner ist als der geplante Aufwand, wird prognostiziert, dass die Aufgabe kürzer als ursprünglich geplant dauern wird und vor dem Zeitplan liegt.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Neuprojektion des Aufwands für Blattknotenaufgaben

Projektmanager überprüfen häufig die ursprünglichen Vorkalkulationen für eine Aufgabe. Erneute Hochrechnungen für ein Projekt spiegeln die Wahrnehmung von Vorkalkulationen durch den Projektmanager angesichts des aktuellen Status eines Projekts wider. Wir empfehlen den Projektmanagern jedoch nicht, die geplanten Aufwandszahlen zu ändern. Dies liegt daran, dass der geplante Projektaufwand die etablierte Quelle der Wahrheit für den Projektplan und die Kostenschätzung darstellt und alle Projektbeteiligten dem zugestimmt haben.

Ein Projektmanager kann den Aufwand für Aufgaben neu projizieren, indem er den Standardwert des **verbleibenden Aufwands** mit einer neuen Schätzung der Aufgabe aktualisiert. Durch diese Aktualisierung werden die Aufwandsschätzung der Aufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Erneute Hochrechnung des Aufwands für Zusammenfassungsaufgaben

Der Aufwand für Zusammenfassungsaufgaben oder Containeraufgaben kann erneut hochgerechnet werden. Projektmanager können den verbleibenden Aufwand für die Zusammenfassungsaufgaben aktualisieren. Das Aktualisieren des verbleibenden Aufwands löst die folgenden Berechnungen in der Anwendung aus:

- Die EAC und der Fortschritt in Prozent werden für die Aufgabe berechnet.
- Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.
- Die neuen BK für jede der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet. 
- Für die betroffenen untergeordneten Aufgaben bis hinunter zu den Blattknoten wird der verbleibende Aufwand und der Fortschritt in Prozent basierend auf dem Wert für die EAC neu berechnet. Hieraus ergibt sich eine neue hochgerechnete Aufwandsabweichung für die Aufgabe. 
- Die EAC wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.


## <a name="project-status-summary"></a>Zusammenfassung des Projektstatus

Die Nachverfolgung von Daten in den Feldern **Aufwandsnachverfolgung** und **Kostennachverfolgung** zeigt den Fortschritt und den Kostenverbrauch für den Stammknoten des Projekts, die Zusammenfassungsaufgaben und die Blattknotenaufgaben an. Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.

## <a name="status-summary-fields"></a>Felder der Statuszusammenfassung

Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an. Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen. Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben. Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten negativ sind, können Sie sie auf **Rückstand** festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
