---
title: Projektaufwandsverfolgung
description: Dieses Thema enthält Informationen zur Nachverfolgung des Projektaufwands und des Arbeitsfortschritts.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593795"
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
- Der genehmigte Aufwand für einen Sammelvorgang ist die Summe des genehmigten Aufwands für alle untergeordneten Vorgänge plus dem genehmigten Aufwand für den Sammelvorgang.
- Der verbleibende Aufwand für den Sammelvorgang ist die Summe des verbleibenden Aufwands für alle untergeordneten Vorgänge minus dem genehmigten Aufwand für den Sammelvorgang.

## <a name="project-status-summary"></a>Projektstatuszusammenfassung

Nachverfolgungsdaten in den Ansichten **Aufwandsverfolgung** und **Kostenverfolgung** zeigen den Fortschritt und den Kostenverbrauch auf der Ebene des Projektstammknotens, der Zusammenfassungsaufgaben und der Blattknotenaufgaben an. Der Abschnitt **Status** auf der Seite **Projektentität** zeigt eine Zusammenfassung des Status auf Projekteben an.

## <a name="status-summary-fields"></a>Felder der Statuszusammenfassung

Das Feld **Gesamtprojektstatus** kann bearbeitet werden und zeigt den Gesamtstatus für das Projekt an. Es verwendet Farben (z. B. Grün, Gelb und Rot), um ein zunehmendes Risiko anzuzeigen. Im Feld **Kommentare** kann der Projektmanager bestimmte Kommentare zum Status eingeben. Das Feld **Status aktualisiert am** kann nicht bearbeitet und der Wert ist ein Zeitstempel der angibt, wann der Status zuletzt aktualisiert wurde.

Die Felder **Zeitplanleistung** und **Kostenleistung** werden über das Nachverfolgungsdatum festgelegt. Wenn die Zeitplan- und Kostenabweichung für den Stammknoten in der Ansicht **Aufwandsverfolgung** positiv sind, können Sie diese Felder auf **Vorsprung** festlegen. Wenn der Zeitplan und die Kostenabweichung für den Stammknoten negativ sind, können Sie sie als **Behind** festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
