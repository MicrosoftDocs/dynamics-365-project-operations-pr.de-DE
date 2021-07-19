---
title: Projektaufwandsverfolgung
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektaufwands und des Arbeitsfortschritts.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 6fe381470326fc4000a9ed096b91fde56c045c38
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369195"
---
# <a name="project-effort-tracking"></a>Projektaufwandsverfolgung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die Anforderungen zur Nachverfolgung des Fortschritts anhand eines Zeitplans variiert je nach Branche. Manche Branchen führen eine Nachverfolgung auf granularer Ebene durch, während andere Branchen eine sehr viel detailliertere Nachverfolgung durchführen. Dieses Thema behandelt, wie eine Planung zu erfolgen hat, um den Anforderungen Ihrer Organisation zu entsprechen.

## <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht **Aufwandsnachverfolgung** verfolgt den Fortschritt von Aufgaben im Zeitplan, indem die für eine Aufgabe aufgewendeten tatsächlichen Arbeitsstunden mit den geplanten Arbeitsstunden der Aufgabe verglichen werden. Dynamics 365 Project Operations verwendet die folgenden Formeln, um die Metriken zur Nachverfolgung zu berechnen:

- **Fortschritt in Prozent**: Tatsächlicher bisheriger Aufwand ÷ Schätzung bei Fertigstellung (EAC) 
- **Verbleibender Aufwand**: geschätzter Aufwand bei Abschluss – tatsächlicher bisheriger Aufwand 
- **EAC**: Verbleibender Aufwand + Tatsächlicher bisheriger Aufwand 
- **Projizierte Aufwandsabweichung**: Geplanter Aufwand – EAC

Project Operations zeigt eine Projektion der Aufwandsabweichung für die Aufgabe. Wenn die EAC den geplanten Aufwand übersteigt, nimmt die Aufgabe voraussichtlich mehr Zeit in Anspruch als ursprünglich geplant und ihre Erfüllung liegt hinter dem Zeitplan zurück. Wenn die EAC kleiner ist als der geplante Aufwand, wird prognostiziert, dass die Aufgabe kürzer als ursprünglich geplant dauern wird und vor dem Zeitplan liegt.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Neuprojektion des Aufwands für Blattknotenaufgaben

Projektmanager überprüfen häufig die ursprünglichen Vorkalkulationen für eine Aufgabe. Projektneuprojektionen sind die Wahrnehmung von Schätzungen durch den Projektmanager anhand des aktuellen Status eines Projekts. Wir empfehlen den Projektmanagern jedoch nicht, die geplanten Aufwandszahlen zu ändern. Dies liegt daran, dass der geplante Projektaufwand die etablierte Quelle der Wahrheit für den Projektplan und die Kostenschätzung darstellt und alle Projektbeteiligten dem zugestimmt haben.

Ein Projektmanager kann den Aufwand für Aufgaben neu projizieren, indem er den Standardwert des **verbleibenden Aufwands** mit einer neuen Schätzung der Aufgabe aktualisiert. Durch diese Aktualisierung werden die Aufwandsschätzung der Aufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Der EAC‑, ETC‑ und Fortschrittsprozentsatz für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet und erzeugen eine neue Projektion der Aufwandsabweichung.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Projektion des Aufwands für Zusammenfassungsaufgaben

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

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn der Zeitplan und die Kostenabweichung für den Stammknoten negativ sind, können Sie sie als **Behind** festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
