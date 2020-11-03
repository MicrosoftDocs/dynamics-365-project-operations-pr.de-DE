---
title: Planen Sie ein Projekt mit einem Projektstrukturplan
description: Planen Sie ein Projekt mit einem Projektstrukturplan (Project Service)
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076706"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planen Sie ein Projekt mit einem Projektstrukturplan (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ein Projektzeitplan teilt mit, welche Arbeit durchgeführt werden muss, welche Ressourcen die Arbeit durchführen und in welchem Zeitrahmen diese Arbeit abgeschlossen werden muss. Der Projektzeitplan reflektiert die ganze Arbeit, die mit dem rechtzeitigen Liefern des Projektes verbunden ist. Einer der ersten Schritte in der Anfangsphase des Projektes ist, einen Projektzeitplan zu finden. Um einen Projektzeitplan zu erstellen, müssen Sie einen Projektstrukturplan erstellen.  
  
 Erstellen Sie eine Projektstruktur mit einem Projektstrukturplan, der Ihnen bei Folgendem hilft:  
  
- Gliedern der Arbeit in verwaltbare Aufgaben  
  
- Schätzen der Zeit, die erforderlich ist, um eine Aufgabe abzuschließen  
  
- Festlegen von Aufgabenabhängigkeiten und Aufgabendauer  
  
- Bestimmen der Rollen, die erforderlich sind, um jede Aufgabe abzuschließen  
  
  Der Projektzeitplan im Projektstrukturplan hat ein vertrautes Aussehen und Gefühl, einschließlich einem interaktiven Gantt-Diagramms.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Erstellen eines Projektstrukturplans für ein Projekt  
 Erstellen Sie einen Projektstrukturplan, um die Reihenfolge von Aufgaben in einem Projekt darzustellen. Der Projektstrukturplan umfasst Aufgaben, Anforderungen für jede Aufgabe und Umsdatz- und Kosteninformationen. In Ihrem Projektstrukturplan können Sie Folgendes hinzufügen:  
  
-   Die Reihenfolge von Aufgaben in einer Hierarchie  
  
-   Andere Aufgaben, sofern vorhanden, die abgeschlossen werden müssen, bevor eine Aufgabe begonnen werden kann  
  
-   Das Anfangsdatum, Enddatum und Dauer einer Aufgabe  
  
-   Die Anzahl von Stunden, die für eine Aufgabe erforderlich sind  
  
-   Alle erforderlichen Arbeitskraftfähigkeiten und -ausbildung  
  
-   Die Arbeitskräfte, die einer Aufgabe zugewiesen werden  
  
-   Geschätzter Umsatz und Kosten  
  
## <a name="task-types"></a>Aufgabentypen  
Sie benutzen die folgenden Aufgabentypen, wenn Ihr Projektstrukturplan erstellt wird:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projektstammknoten**. | Die auf höchster Ebene zusammengefasste Aufgabe für das Projekt. Alle weiteren Projektaufgaben werden darunter erstellt. Der Name der Stammaufgabe ist der Projektname. Der Aufwand, die Daten und die Dauer des Stammknotens basieren auf den Werten auf der Hierarchie darunter. Sie können Stammknoteneigenschaften nicht bearbeiten oder den Stammnoten löschen. | 
| **Zusammenfassende oder Behälteraufgaben**. | Eine zusammenfassende Aufgabe ist eine Aufgabe, die Teilaufgaben umfasst. Eine zusammenfassende Aufgabe hat keinen eigenen Arbeitsaufwand oder keine eigenen Kosten. Der Arbeitsaufwand und die Kosten sind ein Rollup der Teilaufgaben. Sie können den Namen einer zusammenfassenden Aufgabe ändern, aber Sie können den Aufwand, die Daten oder die Dauer nicht ändern, weil die automatisch berechnet werden. Das Löschen einer zusammenfassenden Aufgabe löscht die Aufgabe und alle Teilaufgaben.|  
| **Blattknotenaufgaben**. | Eine Blattknotenaufgabe stellt die Detailarbeit im Projekt dar. Sie hat einen geschätzten Aufwand, eine geplante Anzahl von Ressourcen, geplante Start- und Enddaten und eine Dauer.|

  
## <a name="task-hierarchy"></a>Aufgabenhierarchie  
 Sie haben die folgenden Optionen, wenn Sie eine Aufgabenhierarchie erstellen:  
  
- **Aufgabe hinzufügen**.   Sie können eine Aufgabe an einer Position hinzufügen, die Sie in der Aufgabenhierarchie auswählen. Wenn Sie keine Position auswählen, erscheint Ihre neue Aufgabe am Ende.  
  
- **Aufgabe herunterstufen**.   Stufen Sie eine Aufgabe herunter, um eine untergeordnete Aufgabe von der darüber daraus zu machen.  
  
- **Aufgabe heraufstufen**.   Stufen Sie eine Aufgabe herauf, damit Sie keine Teilaufgabe der ursprünglichen übergeordneten Aufgabe mehr ist.  
  
- **Nach oben oder unten verschieben**.   Verschieben Sie Aufgaben in der Hierarchie seiner übergeordneten Aufgaben hoch- und herunter. Das hoch und herunter Verschieben einer Aufgabe hat keinen Effekt auf Aufwand, Kosten, Daten oder Dauer.  
  
## <a name="task-attributes"></a>Aufgabenattribute  
 Ein Aufgabenname beschreibt die Arbeit, die abgeschlossen werden muss. Sie verwenden verschiedene Aufgabenattribute, um den Zeitplan und die Personalanforderungen für die Aufgabe zu beschreiben.  
  
### <a name="schedule-attributes"></a>Zeitplanattribute.

 - Weisen Sie **Aufwandsstunden** , **Anzahl der Ressourcen** , **Startdatum** , **Enddatum** und **Dauer** Werte zu, um den Zeitplan für die Aufgabe zu bestimmen. 
 - **Audwand** ist eine Schätzung der Stunden, die für den Abschluss der Aufgabe erforderlich sind.
 - **Anzahl der Ressourcen** ist eine Schätzung, die der Projektleiter für die Aufgabe angibt, um den bestmöglichen Zeitplan zu erhalten. 
 - **Dauer** (in Tagen) zeigt die Anzahl von Arbeitstagen an, die für den Abschluss der Aufgabe erforderlich sind.  
  
### <a name="staffing-attributes"></a>Personalattributen.

 - **Rollen** , **Organisationseinheit der Ressource** , **Anzahl der Ressourcen** und **Ressourcen** beschreiben die Personalanforderungen für die Aufgabe. 
 - **Rolle** beschreibt die Art der Ressource, die benötigt wird, um die Aufgabe durchzuführen. 
 - **Organisationseinheit der Ressource** zeigt die Organisationseinheit an, aus der Ressourcen für diese Aufgabe mit Personal besetzt werden sollten. Dies wirkt sich auch auf die Kosten und die Umsatzschätzung der Aufgabe aus, da es von Bedeutung ist, wenn der Verkaufspreis pro Einheit für die Ressource bestimmt wird. 
 - **Ressourcen** enthält eine generische Ressource oder eine benannte Ressource, wenn eine gefunden wird.  
  
## <a name="task-dependencies"></a>Aufgabenabhängigkeiten  
 Sie können Beziehungen zwischen einer oder mehreren vorherigen Aktivitäten im Projektstrukturplan erstellen. Sie können eine oder mehrere Werte für das Feld für vorherige Aktivitäten bei Aufgaben einstellen, um die Aufgaben anzuzeigen, von denen sie abhängig ist. Wenn Sie einer Aufgabe einen Wert für vorherige Aufgaben zuweisen, kann die Aufgabe nur beginnen, wenn alle vorherigen Aktivitäten abgeschlossen wurden. Die Einstellung dieser Abhängigkeit von einer Aufgabe ergibt die Neuberechnung des geplanten Anfangsdatums der Aufgabe als das späteste Ende von aller vorherigen Aktivitäten. Auswirkungen durch vorherige Aktivitäten auf einen Zeitplan werden nicht durch den Aufgabenmodus begrenzt, der für die Aufgabe definiert wird.  
  
## <a name="task-mode"></a>Aufgabenmodus  
 Der Aufgabenmodus ist einer der wichtigen Faktoren bei der Bestimmung des Zeitplans für Blattknotenaufgaben. Es gibt zwei Aufgabenmodi für jede Aufgabe: automatischer Zeitplanmodus und manueller Zeitplanmodus.  
  
-   **Automatische Planung**   Wenn Sie den Aufgabenmodus auf "Automatisch geplant" einstellen, verwendet die Aufgabenplanungsengine die Zeitplanregeln für die folgenden Aufgabenattribute, um den Zeitplan für die Aufgabe zu bestimmen:  
  
    -   Vorherige Aktivitäten  
  
    -   Aufwand  
  
    -   Anzahl der Ressourcen  
  
    -   Start- und Enddatum  
  
-   **Meine Buchungsregeln**   Das Startdatum der Blattknotenaufgabe ohne vorherige Aktivitäten ist standardmäßig das geplante Anfangsdatum des Projektes. Die Dauer einer Blattknotenaufgabe wird immer als die Anzahl der Werktage zwischen seinem Anfangs- und Enddaten berechnet. Wenn eine Aufgabe automatisch geplant wird, folgt die Planungsengine den Regeln unten:  
  
    -   Start- und Enddaten einer Aufgabe müssen immer Werktage entsprechend dem Planungskalender des Projektes sein  
  
    -   Das Startdatum einer Aufgabe mit vorherigen Aktivitäten entspricht standardmäßig dem spätesten Enddatum seiner vorherigen Aktivitäten  
  
    -   Aufwand = Anzahl der Menschen * Dauer * Stunden an einem Standardwerktag des Projektkalenders  
  
-   **Planmanager**   In einigen Fällen sollten Sie von diesen Regeln abweichen. In diesen Fällen können Sie den Aufgabenmodus auf manuelle Planung einstellen. Das hindert die Planungsengine an der Berechnung der Werte für andere Planungsattribute. Das Einstellen von vorherigen Aktivitäten für Aufgaben wirkt sich immer auf das Startdatum der abhängigen Aufgabe aus.  
  
## <a name="create-a-work-breakdown-structure"></a>Erstellen eines Projektstrukturplans  
  
1.  Wechseln Sie zu **Project Service > Projekte**.  
  
2.  Klicken Sie auf das gewünschte Projekt.  
  
3.  Wählen Sie auf der Leiste oben auf dem Bildschirm den Abwärtspfeil neben dem Projektnamen, und klicken Sie dann auf "Projektstrukturplan".  
  
4.  Um eine Aufgabe hinzuzufügen, klicken Sie auf **Aufgabe hinzufügen**. Füllen Sie die Felder für die Aufgabe aus, und klicken Sie dann auf **Speichern**.  
  
5.  Fügen Sie weiter Aufgaben hinzu, bis Ihr Projektstrukturplan vollständig ist. Bei der Erstellung Ihres Projektstrukturplans können Sie Folgendes tun, um Ihre Aufgaben zu organisieren:  
  
    -   Wählen Sie eine Aufgabe aus, und klicken Sie auf **Herunterstufen** , um sie unter eine andere Aufgabe zu verschieben oder klicken Sie auf "Höherstufen" , um sie eine ebene heraus zu bewegen.  
  
    -   Wählen Sie eine Aufgabe aus, und klicken Sie auf **Nach oben** oder **Nach unten** , um sie in der Liste auf oder ab zu bewegen.  
  
    -   Klicken Sie auf **Gantt ausblenden** , um das Gantt-Diagramm zu verbergen, und klicken Sie auf **Gantt anzeigen** , um es wieder anzuzeigen.  
  
    -   Wählen Sie einen anderen Zeitabschnitt für das Gantt-Diagramm auf der **Zeitskala** aus.  
  
6.  Um die Rollen hinzuzufügen, die Sie in Ihrem Projektstrukturplan für Ihre Projektteammitglieder angegeben haben, klicken Sie auf **Projektteam generieren**.  
  
7.  Wenn Sie fertig mit den Änderungen sind, klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms.  
  
### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)
