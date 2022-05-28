---
title: Projektzeitpläne
description: Dieses Thema bietet Informationen zur Vorgehensweise beim Erstellen von Zeitplänen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b7b221c2b0c47ed02c59fb724cf65bc41697d82
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600603"
---
# <a name="project-schedules"></a>Projektzeitpläne 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ein Projektzeitplan teilt mit, welche Arbeit durchgeführt werden muss, welche Ressourcen die Arbeit durchführen und in welchem Zeitrahmen diese Arbeit abgeschlossen werden muss. Der Projektzeitplan reflektiert die gesamte Arbeit, die mit dem rechtzeitigen Liefern des Projektes verbunden ist. In Dynamics 365 Project Service Automation, erstellen Sie einen Projektzeitplan, indem Sie den Arbeitsumfang in überschaubaren Aufgaben einteilen, die für jede Aufgabe erforderliche Zeit schätzen, Aufgabenabhängigkeiten festlegen, Aufgabendauern einstellen und die allgemeine Ressourcen abschätzen, die die Aufgaben ausführen. Der Projektzeitplan wird auf der Registerkarte **Zeitplan** der Projektseite erstellt.
 
## <a name="tasks"></a>Aufgaben

Der erste Schritt beim Erstellen eines Projektzeitplans ist die Aufteilung der Arbeit in überschaubare Portionen. Der Zeitplan in PSA unterstützt die folgenden Funktionen:

- Projektstammknoten.
- Zusammenfassende oder Behälteraufgaben.
- Blattknotenaufgaben.

### <a name="project-root-node"></a>Projektstammknoten.

Der Projektstammknoten ist die Aufgabenzusammenfassung auf oberster Ebene für das Projekt. Alle weiteren Projektaufgaben werden darunter erstellt. Der Name der Stammknotens ist immer auf den Projektnamen eingestellt. Der Aufwand, die Termine und die Dauer des Stammknotens werden, basierend auf den Werten auf der Hierarchie darunter, zusammengefasst. Sie können die Eigenschaften des Stammknotens nicht bearbeiten. Sie können den Stammknoten auch nicht löschen.

### <a name="summary-or-container-tasks"></a>Zusammenfassende oder Behälteraufgaben. 

Zusammenfassende Aufgaben haben Unteraufgaben oder Containeraufgaben darunter. Sie haben keinen eigenen Arbeitsaufwand oder Kosten. Stattdessen sind ihr Arbeitsaufwand und die Kosten ein Rollup der Arbeitsaufwands und der Kosten ihrer Containeraufgaben. Das Startdatum der zusammenfassenden Aufgabe ist das Startdatum der Containeraufgaben, und das Enddatum ist das Enddatum der Containeraufgaben. Der Name einer zusammenfassenden Aufgabe kann bearbeitet werden aber Zeitplanungseigenschaften (Aufwand,Termine und Dauer) können nicht bearbeitet werden. Wenn Sie eine zusammenfassende Aufgabe löschen, dann löschen Sie auch all ihre Containeraufgaben.

### <a name="leaf-node-tasks"></a>Blattknotenaufgaben.

Blattknotenaufgaben stellt die Detailarbeit im Projekt dar. Sie haben einen geschätzten Aufwand, geschätzte Ressourcen, geplante Start- und Enddaten und eine Dauer.
 
## <a name="creating-a-task-hierarchy"></a>Erstellen einer Aufgabenhierarchie

Sie haben die folgenden Optionen zum Erstellen einer Aufgabenhierarchie:

- **Aufgabe hinzufügen** Schaltfläche
- **Aufgabe einrücken** Schaltfläche
- **Aufgabe ausücken** Schaltfläche
- **Nach oben verschieben** und **Nach unten verschieben** Schaltflächen.
- Barrierefreiheit und Tastenkombinationen

### <a name="add-task"></a>Aufgabe hinzufügen

Mit der Schaltfläche **Aufgabe hinzufügen** können Sie eine neue Aufgabe in der Hierarchie erstellen. Wenn Sie keine Position auswählen, wird Ihre Aufgabe am Ende eingefügt. 

Eine Zeitplan-ID ist jeder Aufgabe zugewiesen. Die Zeitplan-ID stellt die Tiefe der Aufgabe und Position in der Hierarchie dar. Sie verwendet Gliederungsnummerierung. Für Aufgaben in der ersten Ebene unter dem Projektstammknoten wird ein Nummerierungsschema von 1, 2, 3 usw. verwendet. Für Aufgaben unter der ersten Ebene wird ein Nummerierungsschema von 1.1, 1.2, 1.3 usw. verwendet.

### <a name="indent-task"></a>Aufgabe einrücken.

Wenn eine Aufgabe eingerückt ist, wird es ein untergeordnetes Element der direkt darüberstehenden Aufgabe. Die Zeitplan-ID der Aufgabe wird dann neu berechnet, damit sie auf der Zeitplan-ID seines neuen übergeordneten Elements basiert und dem Gliederungsnummerierungsschema folgt. Die übergeordnete Aufgabe ist jetzt eine zusammenfassende Aufgabe oder eine Containeraufgabe. Daher wird es ein Rollup der untergeordneten Aufgaben.

### <a name="outdent-task"></a>Aufgabe ausrücken. 

Wenn eine Aufgabe ausgerückt wird, ist sie nicht mehr ein untergeordnetes Element der Aufgabe, die ihr übergeordnetes Element war. Die Zeitplan-ID wird dann neu berechnet, sodass sie die aktualisierte Tiefe und Position der Aufgabe in der Hierarchie widergibt. Der Aufwand, die Kosten und Datumsangaben der vorherigen übergeordneten Aufgabe werden neu berechnet, damit sie diese Aufgabe nicht mit einschließen.

### <a name="move-up-and-move-down"></a>Nach oben und Nach unten verschieben 

Die Schaltflächen **Nach oben** und **Nach unten** ändern die Position einer Aufgabe in ihrer übergeordneten Hierarchie. Änderungen dieser Art betreffen nicht den Aufwand, die Kosten, Datumsangaben oder Dauer der Aufgabe. Nur die Zeitplan-ID der Aufgabe ist betroffen. Die Zeitplan-ID wird neu berechnet, sodass sie die neue Position der Aufgabe in der übergeordneten Liste der untergeordneten Aufgaben widergibt.

### <a name="accessibility-and-keyboard-shortcuts"></a>Barrierefreiheit und Tastenkombinationen

Auf das Raster **Zeitplan** kann vollständig zugegriffen werden, und es kann mit Bildschirmlesern wie Narrator, JAWS oder NVDA verwendet werden. Sie können durch den Rasterbereich navigieren, indem Sie die Pfeiltasten (wie in Microsoft Excel) verwenden. Sie können die TAB-TASTE verwenden, um über die interaktiven Benutzeroberflächenelemente zu navigieren, und Sie können den ABWÄRTSPFEIL, die EINGABETASTE oder LEERTASTE verwenden, um die Dropdownmenüs auszuwählen und aufzurufen. Die Spaltenüberschriften sind auch interaktiv. Sie können Spalten ausblenden und einblenden; verwenden Sie die TAB-TASTE und die PFEILTASTEN, um durch die Spaltenüberschriften zu navigieren, verwenden Sie die interaktiven Schaltflächen auf der Menüleiste. Außerdem können Sie folgende Tastaturkürzel verwenden:

- **Aktualisieren**: ALT+SHIFT+F5
- **Hinzufügen**: ALT+SHIFT+Insert
- **Löschen**: ALT+SHIFT+Delete
- **Verschieben auf/ab**: ALT+SHIFT+Up-/Downpfeile
- **Einrücken/Ausrücken**: ALT_SHIFT+Links-/Rechtspfeile
- **Hierarchien Erweitern/Reduzieren/**: ALT+SHIFT+Plus-/Minustasten

## <a name="task-attributes"></a>Aufgabenattribute

Ein Aufgabenname beschreibt die Arbeit, die abgeschlossen werden muss. In PSA beschreiben die Attribute, die einer Aufgabe zugeordnet sein, den Zeitplan der Aufgabe und das erforderliche Personal.

> ![Aufgabenattribute.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Zeitplanattribute.

Die Attribute **Aufwand**, **Startdatum**, **Enddatum** und **Dauer** definieren den Zeitplan für die Aufgabe.

Weitere Zeitplanattribute enthalten:

- **Aufwandsstunden**: Geben Sie eine geschätzte Anzahl der Stunden ein, die erforderlich sind, um die Aufgabe abzuschließen. 
- **Dauer**: Geben Sie die Anzahl der Arbeitstage an, die erforderlich sind, um die Aufgabe abzuschließen.
- **Zeitplan-ID**: Diese automatisch generierte ID wird verwendet, um Aufgaben in der Hierarchie anzuordnen. Abhängigkeiten zwischen den Aufgaben verwalten die tatsächliche Reihenfolge, in der die Aufgaben bearbeitet werden.
 
### <a name="staffing-attributes"></a>Personalattributen.

Attribute der Personalbesetzung werden durch das Feld **Ressourcen** im Zeitplan angezeigt. Sie können entweder nach einer bestehenden Ressource suchen oder auf **Erstellen** klicken und im Fenster **Schnellerfassung** ein Projektteammitglied als neue Ressourcen hinzufügen.

Die Felder **Rolle**, **Ressourcenzuordnungseinheit** und **Positionsname** werden verwendet, um die Personalanforderungen für die Aufgabe zu beschreiben. Diese Stellenbesetzungsattribute zusammen mit dem Aufgabenplan werden verwendet, um verfügbare Ressourcen zu finden, um diese Aufgabe auszuführen.

**Rolle** – Geben Sie die Art der Ressource an, die für die Aufgabe erforderlich ist.

**Ressourcenzuordnungseinheit** – Geben Sie die Einheit an, von der Ressourcen für die Aufgabe zugewiesen werden sollten. Dieses Attribut betrifft die Kosten- und Umsatzschätzung für die Aufgaben, wenn der Kosten- und Berechnungssatz für die Ressource auf Beschaffungseinheiten basieren.

**Positionsname** – Geben Sie einen Anzeigenamen für die allgemeine Ressource ein, der als Platzhalter für die Ressource dient, die letztendlich die Arbeit ausführen wird.

Das Feld **Ressourcen** enthält den Positionsnamen der generischen Ressource oder einer benannten Ressource , wenn eine gefunden wird.

Das Feld **Kategorie** enthält die Werte, die eine breitere Art der Arbeit angeben, in denen die Aufgabe kategorisiert werden kann. Dieses Feld betrifft nicht die Zeitplanung oder die Stellenbesetzung. Es wird nur für die Berichterstellung verwendet.

### <a name="task-dependencies"></a>Aufgabenabhängigkeiten 

Sie können den Zeitplan in PSA verwenden, um Vorgängerbeziehungen zwischen Aufgaben zu erstellen. Das Feld **Vorgänger** unter **Aufgaben** akzeptiert einen oder mehrere Werte, um die Aufgaben anzugeben, von denen eine Aufgabe abhängt. Wenn Vorgängerwerte einer Aufgabe zugewiesen werden, kann die Aufgabe nur beginnen, nachdem alle vorherigen Aufgaben abgeschlossen wurden. Aufgrund der Abhängigkeit wird das geplante Startdatum der Aufgabe auf das Datum zurückgesetzt, an dem die Vorgängeraufgaben abgeschlossen wurden.

Der Aufgabenmodus hat keine Auswirkungen auf die Updates, die für das Start- und Enddatum vonVorgängern/abhängigen Aufgaben gemacht werden.

## <a name="task-mode"></a>Aufgabenmodus 

Der Aufgabenmodus bestimmt die Zeitplanung von Blattknotenaufgaben. PSA unterstützt zwei Aufgabenmodi für jede Aufgabe: automatischer Zeitplanung und manuelle Zeitplanung.

### <a name="auto-scheduling"></a>Automatische Zeitplanung 
 
Wenn der Aufgabenmodus auf **Automatisch geplant** für eine Aufgabe eingestellt ist, verwendet die Aufgabenzeitplanungsengine die Zeitplanungsregeln für die Aufgabenattribute, um den Zeitplan für die Aufgabe zu bestimmen:

#### <a name="scheduling-rules"></a>Zeitplanungsregeln

Wenn eine Blattknotenaufgabe keine Vorgänger hat, wird ihr Startdatum standardmäßig auf das geplante Startdatum des Projekts gesetzt. Die Dauer einer Blattknotenaufgabe wird immer als die Anzahl der Werktage zwischen seinem Anfangs- und Enddaten berechnet. Wenn eine Aufgabe automatisch terminiert wird, folgt die Zeitplanungsengine diesen Regeln:

- Start- und Enddaten der Aufgabe müssen Werktage entsprechend dem Terminplanungskalender des Projektes sein. 
- Für alle Aufgaben, die Vorgängeraufgaben haben, wird das Startdatum automatisch auf das späteste Enddatum seiner Vorgänger gesetzt.
- Der Aufwand wird berechnet, indem diese Formel verwendet wird: Anzahl der Personen × Dauer × Stunden an einem Standardarbeitstag im Projektkalender.

### <a name="manual-scheduling"></a>Manuelle Terminierung

Wenn die Regeln zur automatischen Zeitplanung Ihre Bedingungen nicht erfüllen, können Sie den Aufgabenmodus der Aufgabe auf **Manuell geplant** setzen. Diese Einstellung stoppt die Zeitplanungsengine an der Berechnung der Werte anderer Zeitplanungsattribute. Wenn Sie unabhängig vom Aufgabenmodus die Vorgänger auf Aufgaben einstellen, beeinflussen Sie immer das Startdatum der abhängigen Aufgabe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
