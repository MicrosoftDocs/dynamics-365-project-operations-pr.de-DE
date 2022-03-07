---
title: Projektkostennachverfolgung
description: Dieses Thema enthält Informationen darüber, wie Project Operations den Fortschritt anhand der Arbeitskosten und der Ausgaben für ein Projekt verfolgt.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d37df64db1808722b7851c952c20be731aa2d670fe066c02ef90386712487407
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987795"
---
# <a name="labor-cost-tracking-on-projects"></a>Nachverfolgung der Arbeitskosten bei Projekten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verfolgt Arbeitsvorkalkulationen und Ausgaben mit der niedrigsten erforderlichen Granularität für den Projektplan. Die finanzielle Schätzung der Arbeitskosten basiert auf dem geplanten Aufwand und den generischen oder benannten Ressourcen, die jeder Blattknotenaufgabe im Projektplan zugewiesen sind. Wenn das Projekt beginnt und die Mitarbeiter beginnen, Zeit für verschiedene Projektaufgaben zu melden, werden die tatsächlichen Arbeitsausgaben zusammengefasst, wodurch eine Berechnung der Projektionen gestartet wird.

## <a name="labor-cost-tracking-view"></a>Arbeitskostenverfolgungsansicht

Sie können auf der **Projekte**-Seite auf der **Verfolgung**-Registerkarte **Verfolgung** > **Kosten** auswählen, um die **Kostenverfolgung**-Ansicht zu öffnen und den Fortschritt der Arbeitsausgaben für jede Aufgabe im Projektplan anzuzeigen. In dieser Ansicht werden auch die tatsächlichen Arbeitskosten, die für eine Aufgabe aufgewendet wurden, mit den geplanten Arbeitskosten der Aufgabe verglichen. Project Operations verwendet die folgenden Formeln zur Berechnung der Arbeitskostenmetriken:

- **Geplante Kosten**: Geschätzte Kosten aller Ressourcenzuweisungen für jede Blattknotenaufgabe
- **Tatsächliche Kosten**: Summe aller tatsächlichen Kosten für die in der Aufgabe aufgezeichnete Zeit
- **Kostenverbrauchsprozentsatz**: Tatsächliche Kosten ÷ Berechnete Kosten bei Abschluss
- **Verbleibende Kosten**: Berechnete Kosten bei Abschluss – Tatsächliche Kosten
- **Kosten bei Abschluss**: Verbleibende Kosten + Tatsächliche Kosten
- **Kostenabweichung**: Geplante Kosten bei Abschluss – Berechnete Kosten bei Abschluss

Jede Aufgabe zeigt eine Projektion der Kostenabweichung für die Aufgabe. Wenn der Kostenvoranschlag vollständig höher ist als die geplanten Kosten, wird die Aufgabe voraussichtlich über das Budget hinausgehen. Wenn die berechneten Kosten bei Abschluss geringer sind als die geplanten Kosten, wird die Aufgabe voraussichtlich mit geringerem Budget ausgeführt.

>[!NOTE]
> Project Operations zeigt nur die Arbeitskosten auf der **Projekt**-Seite auf der Registerkarte **Verfolgung**. Während Materialien und Ausgaben geschätzt und für den Verbrauch nachverfolgt werden können, sind diese Kosten nicht in den auf der Registerkarte **Verfolgung** angegebenen Kosten enthalten. Diese Registerkarte dient nur zur Neuprojektion von Arbeitskosten durch Neuprojektion des Aufwands.
Alle angezeigten Kostenbeträge werden aus der zur Ermittlung des Kostensatzes verwendeten Selbstkostenpreiswährung des Projekts in die Kostenwährung des Projekts umgerechnet. Die Kostenwährung des Projekts ist die Währung der Vertragseinheit des Projekts. Die geschätzten Kostenwerte für die Zeit, die auf der **Schätzungen**-Registerkarte auf der **Projekt**-Seite angezeigt werden, summiert sich möglicherweise nicht zu den geplanten Kosten auf der **Verfolgung**-Registerkarte. Der Grund für diese Diskrepanz liegt in den Unterschieden in der Zusammenfassung der geschätzten Kosten im **Schätzungen**-Raster und wie die geplanten Kosten im **Verfolgung**-Raster berechnet werden. 
>
> - Die Registerkarte **Schätzungen** berechnet die geschätzten Kosten unter Verwendung derselben Währung wie der Kostensatz in der Preisliste. Anschließend werden die geschätzten Kosten in der Preislistenwährung in die geschätzten Kosten in der Kostenwährung des Projekts umgerechnet. Die geschätzten Kosten in der Projektwährung werden auf 2 Dezimalstellen gerundet angezeigt. Zu keinem Zeitpunkt während dieser Umrechnung wird Währungsgenauigkeit angewendet. 
> - Auf der **Verfolgung**-Registerkarte folgt die geplante Kostenberechnung einer geringfügig anderen Berechnungsreihenfolge, bei der die Währungsgenauigkeit in zwei Schritten angewendet wird: 
   ><ol>
   ><li>Der geschätzte Kostenbetrag in der Preislistenwährung wird in die Basiswährung umgerechnet (Umrechnung 1).</li>
   ><li>Der geschätzte Kostenbetrag in der Basiswährung wird in die Projektkostenwährung umgerechnet (Umrechnung 2). </li>
   ></ol>
   >In beiden Schritten wird die Währungsgenauigkeit angewendet, um die geplanten Kosten zu ermitteln (auf der **Verfolgung**-Registerkarte), die geringfügig von den geschätzten Kosten abweicht (auf der **Zeitphasenansicht** in der **Schätzungen**-Registerkarte). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Neuprojektion von Kosten für Blattknotenaufgaben

Die Arbeitskosten für eine Blattknotenaufgabe können nicht direkt auf die **Verfolgung**-Registerkarte auf der **Projektseite** projiziert werden. Sie können jedoch die **Aufwandsnachverfolgung**-Ansicht verwenden, um den verbleibenden Aufwand für eine Aufgabe neu zu projizieren. Dies führt zu einer Neuberechnung der verbleibenden Kosten für die Aufgabe. Im Folgenden finden Sie eine Beschreibung zur Funktionsweise:

1. Ein Projektmanager kann den Aufwand für Aufgaben neu projizieren, indem er den Standardwert im **Verbleibender Aufwand**-Feld mit einer neuen Schätzung des verbleibenden Aufwands für die Aufgabe aktualisiert. Durch die Neuprojektion werden die Aufwandsvorkalkulation der Aufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC (geschätzt bis zum Abschluss) und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.
2. Basierend auf dem neuen Wert für den verbleibenden Aufwand für die Aufgabe berechnet das System die verbleibenden Kosten für die **Kostennachverfolgung**-Ansicht. Um die verbleibenden Kosten basierend auf dem verbleibenden Aufwand zu berechnen, berechnet das System zunächst die durchschnittlichen Kosten einer Stunde Aufwand für die Aufgabe als geplante Kosten oder geplanten Aufwand. Die geplanten Kosten sind die Summe der Kosten aller Ressourcenzuweisungen für die Aufgabe. Die durchschnittlichen Kosten pro Stunde werden verwendet, um die verbleibenden Kosten für den neu projizierten verbleibenden Aufwand für die Aufgabe zu berechnen.
3. Die Gesamtkosten und der prozentuale Kostenverbrauch für die Blattknotenaufgabe werden neu berechnet.
4. Der Wert der berechneten Kosten bei Abschluss wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.

## <a name="reprojecting-costs-on-summary-tasks"></a>Neuprojektion von Kosten für Zusammenfassungsaufgaben

Sie können die Arbeitskosten für Zusammenfassungsaufgaben oder Containeraufgaben neu projizieren. Sie können die Arbeitskosten direkt in einer Zusammenfassungsprojektaufgabe auf der **Verfolgung**-Registerkarte auf der **Projektseite** projizieren. Ähnlich wie bei Blattknotenaufgaben können Projektions- und Containeraufgaben mit der Ansicht **Aufwandsverfolgung** neu projiziert werden. In dieser Ansicht können Sie den verbleibenden Aufwand für eine Zusammenfassungsaufgabe neu projizieren, wodurch die verbleibenden Kosten für die Zusammenfassungsaufgabe neu berechnet werden. Im Folgenden finden Sie eine Beschreibung zur Funktionsweise:

1. Ein Projektmanager kann den Aufwand für Zusammenfassungsaufgaben neu projizieren, indem er den Standardwert des verbleibenden Aufwands mit einer neuen Schätzung der Aufgabe aktualisiert. Durch diese Aktualisierung werden die Aufwandsvorkalkulation der Zusammenfassungsaufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.
2. Basierend auf dem neuen Wert für den verbleibenden Aufwand für die Zusammenfassungsaufgabe berechnet das System die verbleibenden Kosten für die **Kostennachverfolgung**-Ansicht. Um die verbleibenden Kosten basierend auf dem verbleibenden Aufwand zu berechnen, berechnet das System zunächst die durchschnittlichen Kosten einer Stunde Aufwand für die Zusammenfassungsaufgabe als geplante Kosten oder geplanten Aufwand. Die durchschnittlichen Kosten pro Stunde werden verwendet, um die verbleibenden Aufwand für den neu projizierten verbleibenden Aufwand für die Zusammenfassungsaufgabe zu berechnen.
3. Die Gesamtkosten und der prozentuale Kostenverbrauch für die Zusammenfassungsaufgabe werden neu berechnet.
4. Die neue Vorkalkulation der Kosten bei Abschluss wird für die Aufgabe im selben Verhältnis auf die Aufgabe aufgeteilt wie die ursprünglich geplanten Kosten.
5. Die neuen Kosten bei Abschluss der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben werden berechnet. Basierend auf diesem Wert werden für die betroffenen untergeordneten Aufgaben bis zu den Blattknoten die verbleibenden Kosten und der prozentuale Kostenverbrauch basierend auf den Kosten zum vollständigen Wert neu berechnet. Dieser Wert ergibt eine neue hochgerechnete Kostenabweichung für die Aufgabe. 


Das **Kostenleistung**-Feld kann über die Nachverfolgungsdaten eingestellt werden. Wenn die Kostenabweichung für den Stammknoten in der **Kostenverfolgung**-Ansicht negativ ist, können Sie dieses Feld auf **Unter Budget** festlegen. Wenn die Kostenabweichung für den Stammknoten positiv ist, können Sie den Wert auf **Über Budget** festlegen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
