---
title: Projektvertriebs-Nachverfolgung
description: In diesem Artikel erfahren Sie, wie Project Operations den Fortschritt bei den Arbeitsumsätzen in einem Projekt verfolgt.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911273"
---
# <a name="project-sales-tracking"></a>Projektvertriebs-Nachverfolgung

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations verfolgt Arbeitsvorkalkulationen und Umsatz mit der niedrigsten erforderlichen Granularität für den Projektplan. Die Schätzung des Arbeitsumsatzes basiert auf dem geplanten Aufwand und den generischen oder benannten Ressourcen, die jeder Blattknotenaufgabe im Projektplan zugewiesen sind. Wenn das Projekt beginnt und die Mitarbeiter beginnen, Zeit für verschiedene Projektaufgaben zu melden, werden die tatsächlichen Arbeitsumsätze zusammengefasst, wodurch eine Berechnung der Projektionen gestartet wird.

## <a name="labor-revenue-tracking-view"></a>Arbeitsumsatzverfolgungsansicht

Auf der **Projekte**-Seite auf der **Verfolgung**-Registerkarte können Sie **Verfolgung** > **Kosten** auswählen, um die **Kostenverfolgung**-Ansicht zu öffnen. Oder Sie können **Verwenden** > **Fakturierungsrate** auswählen, die **Umsatzverfolgung**-Ansicht zu öffnen, die den Fortschritt der Arbeitseinnahmen für jede Aufgabe im Projektplan zeigt. In dieser Ansicht werden auch die tatsächlichen Arbeitsumsätze, die für eine Aufgabe aufgewendet wurden, mit den geplanten Arbeitsumsätzen der Aufgabe verglichen. Project Operations verwendet die folgenden Formeln zur Berechnung der Arbeitsumsatzmetriken:

- **Geplanter Umsatz**: Geschätzte Umsatzwerte aller Ressourcenzuweisungen für jede Blattknotenaufgabe
- **Tatsächlicher Umsatz**: Summe aller tatsächlichen nicht fakturierten Verkaufstransaktionen für die in der Aufgabe aufgezeichnete Zeit
- **Abrechenbarer Umsatz %**: Tatsächlicher Umsatz ÷ Vorkalkulierter Umsatz bei Abschluss
- **Verbleibende Umsatz**: Vorkalkulierter Umsatz bei Abschluss – Tatsächlicher Umsatz
- **Vorkalkulierter Umsatz bei Abschluss**: Verbleibender Umsatz + Tatsächlicher Umsatz
- **Abweichung des Umsatzes**: Geplanter Umsatz – Vorkalkulierter Umsatz bei Abschluss


> [!NOTE]
> Project Operations zeigt nur die Arbeitsumsätze auf der **Projekt**-Seite auf der Registerkarte **Verfolgung**. Während Materialien und Ausgaben geschätzt und für den Verbrauch nachverfolgt werden können, sind diese Umsätze nicht in den auf der Registerkarte **Verfolgung** angegebenen Umsätzen enthalten. Diese Registerkarte dient nur zur Neuprojektion von Arbeitsumsätzen durch Neuprojektion des Aufwands.  
> Alle angezeigten Umsatzbeträge werden in die Kostenwährung des Projekts umgerechnet. Die Kostenwährung des Projekts ist die Währung der Vertragseinheit des Projekts. Bei Festpreisprojekten sind die Umsatzzahlen in der **Arbeitsumsatzverfolgungsansicht**-Ansicht nicht relevant, da nicht in Rechnung gestellte Verkaufszahlen nicht mit der Genehmigung der Zeit erfasst werden.
> Die geschätzten Verkaufswerte für die Zeit, die auf der **Schätzen**-Registerkarte des Projekts angezeigt werden, addiert sich möglicherweise nicht zum geplanten Ertragswert auf der **Verfolgung**-Registerkarte. Die Ursache für diese Diskrepanz sind zwei mögliche Gründe:
><ol>
   ><li> Die <b>Schätzungen</b>-Registerkarte zeigt den geschätzten Umsatz in der Verkaufswährung an, während die Registerkarte <b>Verfolgung</b> die geplanten Einnahmen zeigt, die in die Kostenwährung umgerechnet wurden. </li>
   ><li> Wenn geschätzte Verkäufe in die Vertragswährung umgerechnet werden, wie auf der <b>Schätzungen</b>-Registerkarte bei der Projektwährung, umfasst die Konvertierung Schritte, die zu einem gewissen Genauigkeitsverlust führen können: </li>
><ol>
><li> Der geschätzte Verkaufsbetrag in der Vertragswährung wird zunächst in die Basiswährung umgerechnet (Umrechnung 1).</li>
><li> Der geschätzte Verkaufsbetrag in der Basiswährung wird in die Projektkostenwährung umgerechnet (Umrechnung 2). </li>
></ol>
></ol>
> In beiden Schritten wird die Währungsgenauigkeit angewendet, was zu einer Abweichung der geplanten Einnahmen in der Projektwährung von den geplanten Verkäufen in der Vertragswährung führt.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Neuprojektion von Umsätzen für Blattknotenaufgaben

Die Arbeitsumsätze für eine Blattknotenaufgabe können nicht direkt auf die **Verfolgung**-Registerkarte auf der **Projektseite** projiziert werden. Sie können jedoch die **Aufwandsnachverfolgung**-Ansicht verwenden, um den verbleibenden Aufwand für eine Aufgabe neu zu projizieren. Dies führt zu einer Neuberechnung der verbleibenden Umsätze für die Aufgabe. Im Folgenden finden Sie eine Beschreibung zur Funktionsweise:

1. Ein Projektmanager kann den Aufwand für Aufgaben neu projizieren, indem er den Standardwert im **Verbleibender Aufwand**-Feld mit einer neuen Schätzung des verbleibenden Aufwands für die Aufgabe aktualisiert. Durch die Neuprojektion werden die Aufwandsvorkalkulation der Aufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC (geschätzt bis zum Abschluss) und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.
2. Basierend auf dem neuen Wert für den verbleibenden Aufwand für die Aufgabe berechnet das System die verbleibenden Umsätze für die **Umsatznachverfolgung**-Ansicht. Um die verbleibenden Umsätze basierend auf dem verbleibenden Aufwand zu berechnen, berechnet das System zunächst die durchschnittlichen Umsätze einer Stunde Aufwand für die Zusammenfassungsaufgabe als geplante Umsätze oder geplanten Aufwand. Die geplanten Umsätze sind die Summe der Umsätze aller Ressourcenzuweisungen für die Aufgabe. Die durchschnittlichen Umsätze pro Stunde werden verwendet, um die verbleibenden Umsätze für den neu projizierten verbleibenden Aufwand für die Aufgabe zu berechnen.
3. Die geschätzten Umsätze und der prozentuale Umsatzverbrauch für die Blattknotenaufgabe werden neu berechnet.
4. Der Wert der berechneten Umsätze bei Abschluss wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Neuprojektion von Umsätzen für Zusammenfassungsaufgaben

Sie können die Arbeitsumsätze für Zusammenfassungsaufgaben oder Containeraufgaben neu projizieren. Sie können die Arbeitsumsätze direkt in einer Zusammenfassungsprojektaufgabe auf der **Verfolgung**-Registerkarte auf der **Projektseite** projizieren. Ähnlich wie bei Blattknotenaufgaben können Projektions- und Containeraufgaben mit der Ansicht **Aufwandsverfolgung** neu projiziert werden. In dieser Ansicht können Sie den verbleibenden Aufwand für eine Zusammenfassungsaufgabe neu projizieren, wodurch die verbleibenden Umsätze für die Zusammenfassungsaufgabe neu berechnet werden. Im Folgenden finden Sie eine Beschreibung zur Funktionsweise:

1. Ein Projektmanager kann den Aufwand für Aufgaben neu projizieren, indem er den Standardwert im **Verbleibender Aufwand**-Feld mit einer neuen Schätzung des **Verbleibenden Aufwands** für die Aufgabe aktualisiert. Durch die Neuprojektion werden die Aufwandsvorkalkulation der Aufgabe bei Abschluss (EAC), der Fortschrittsprozentsatz und die projizierte Aufwandsabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine neue Hochrechnung der Aufwandsabweichung.
2. Basierend auf dem neuen Wert im Feld **Verbleibender Aufwand** für die Aufgabe berechnet das System die verbleibenden Umsätze für die **Umsatznachverfolgung**-Ansicht. Um die verbleibenden Umsätze basierend auf dem verbleibenden Aufwand zu berechnen, berechnet das System zunächst die durchschnittlichen Umsätze einer Stunde Aufwand für die Zusammenfassungsaufgabe als geplante Umsätze oder geplanten Aufwand. Die geplanten Umsätze sind die Summe der Umsätze aller Ressourcenzuweisungen für die Aufgabe. Diese durchschnittlichen Umsätze pro Stunde werden berechnet, um die verbleibenden Umsätze für den neu projizierten verbleibenden Aufwand für die Aufgabe zu berechnen.
3. Die geschätzten Umsätze und der prozentuale Umsatzverbrauch für die Zusammenfassungsaufgabe werden neu berechnet.
4. Der neue Wert für den geschätzten Umsatz bei Abschluss wird für die Aufgabe im selben Verhältnis auf die Aufgabe aufgeteilt wie die ursprünglich geplanten Umsätze.
5. Der neue geschätze Umsatz bei Abschluss der einzelnen Aufgaben bis hinunter zu den Blattknotenaufgaben wird berechnet. Basierend auf diesem Wert werden für die betroffenen untergeordneten Aufgaben bis zu den Blattknoten die verbleibenden Umsätze und der prozentuale Umsatzverbrauch basierend auf den Umsätzen zum vollständigen Wert neu berechnet. Hieraus ergibt sich eine neue hochgerechnete Umsatzabweichung für die Aufgabe. 
6. Der Wert der berechneten Umsätze bei Abschluss wird für alle Zusammenfassungsaufgaben bis zum Stammknoten neu berechnet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

