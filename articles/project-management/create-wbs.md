---
title: Einen Projektstrukturplan erstellen
description: Dieser Artikel erklärt, wie Sie einen Projektstrukturplan (PSP) einschließlich der grundlegenden Steuerelemente in der neuen Planungsoberfläche erstellen.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: a947c0a44464bfad6c3bd74b0cb4fb8128924859
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932065"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Einen Projektstrukturplan (PSP) erstellen

Ein Projektzeitplan teilt mit, welche Arbeit durchgeführt werden muss, welche Ressourcen die Arbeit durchführen und in welchem Zeitrahmen diese Arbeit dann abgeschlossen werden muss. Der Projektzeitplan reflektiert die gesamte Arbeit, die mit dem rechtzeitigen Liefern des Projektes verbunden ist. In Dynamics 365 Project Operations erstellen Sie einen Projektplan durch:

  - Gliedern der Arbeit in verwaltbare Aufgaben.
  - Schätzen der Zeit, die für jede Aufgabe erforderlich ist.
  - Abhängigkeiten der Aufgaben festlegen.
  - Festlegen der Aufgabendauer.
  - Schätzen der generischen Ressourcen, die die Aufgaben ausführen. 

Der Projektzeitplan wird auf der Registerkarte **Zeitplan** der Seite **Projekt** erstellt.

## <a name="tasks"></a>Aufgaben

Der erste Schritt beim Erstellen eines Projektzeitplans ist die Aufteilung der Arbeit in überschaubare Portionen. Der Zeitplan in Project Operations unterstützt die folgenden Funktionen:

- Zusammenfassende oder Behälteraufgaben.
- Blattknotenaufgaben.

### <a name="summary-tasks"></a>Zusammenfassungsaufgaben

Zusammenfassungsaufgaben können andere Zusammenfassungsaufgaben oder Blattknotenaufgaben speichern. Sie haben keinen eigenen Arbeitsaufwand oder Kosten. Stattdessen sind ihr Arbeitsaufwand und die Kosten ein Rollup der Arbeitsaufwands und der Kosten ihrer Containeraufgaben. Das Startdatum der zusammenfassenden Aufgabe ist das Startdatum der Containeraufgaben, und das Enddatum ist das Enddatum der Containeraufgaben. Der Name einer zusammenfassenden Aufgabe kann bearbeitet werden, aber Zeitplanungseigenschaften inklusive Aufwand,Termine und Dauer können nicht bearbeitet werden. Wenn Sie eine zusammenfassende Aufgabe löschen, dann löschen Sie auch all ihre Containeraufgaben.

### <a name="leaf-node-tasks"></a>Blattknotenaufgaben.

Blattknotenaufgaben stellt die Detailarbeit im Projekt dar. Sie haben einen geschätzten Aufwand, geschätzte Ressourcen, geplante Start- und Enddaten und eine Dauer.

## <a name="create-a-task-hierarchy"></a>Aufgabenhierarchie erstellen

### <a name="add-a-task"></a>Eine Aufgabe hinzufügen

Führen Sie zum Hinzufügen einer oder mehrer Aufgaben die folgenden Schritte aus.

1. Gehen Sie zu **Projekte** und wählen Sie den Projektdatensatz aus und öffnen Sie jenen, für den Sie einen Zeitplan erstellen möchten. 
2. Klicken Sie auf die Registerkarte **Aufgaben**. 
3. Wählen Sie **Neue Aufgabe hinzufügen** und geben Sie einen Namen für die Aufgabe ein und drücken Sie die Eingabetaste.
2. Geben Sie einen anderen Aufgabennamen ein und drücken Sie erneut die Eingabetaste, bis Sie eine vollständige Liste der Aufgaben haben.

### <a name="manage-hierarchy-of-a-task"></a>Hierarchie einer Aufgabe verwalten

Wenn eine Aufgabe eingerückt ist, wird es ein untergeordnetes Element der direkt darüberstehenden Aufgabe. Die Zeitplan-ID der Aufgabe wird dann neu berechnet, damit sie auf der Zeitplan-ID seines neuen übergeordneten Elements basiert und dem Gliederungsnummerierungsschema folgt. Die übergeordnete Aufgabe ist jetzt eine zusammenfassende Aufgabe. Daher wird es ein Rollup der untergeordneten Aufgaben. Wenn eine Aufgabe höher gestuft wird, ist sie nicht mehr ein untergeordnetes Element der Aufgabe, die ihr übergeordnetes Element war. Die Zeitplan-ID wird dann neu berechnet, sodass sie die aktualisierte Tiefe und Position der Aufgabe in der Hierarchie widergibt. Der Aufwand, die Kosten und Datumsangaben der vorherigen übergeordneten Aufgabe werden neu berechnet, damit sie diese Aufgabe nicht mit einschließen.

Führen Sie zum Tiefer- oder Höherstufen einer Aufgabendauer folgende Schritte aus.

1. Wählen Sie unter **Zusammenfassungsaufgaben** auf der Seite **Projekt** auf der Registerkarte **Aufgaben** die drei vertikalen Punkte neben dem Aufgabennamen aus und wählen dann **Unteraufgabe**. 
2. Wählen Sie die Aufgabe aus, die tiefer oder höher gestuft werden soll. Um mehr als eine Aufgabe auszuwählen, wählen Sie eine Aufgabe aus, halten STRG gedrückt und wählen die zusätzlichen Aufgaben aus.
2. Sie können auch **Unteraufgabe höher stufen** oder **Unteraufgabe tiefer stufen** auswählen, um die Unteraufgabe von der Zusammenfassungsaufgaben zu verschieben.

### <a name="move-tasks-up-and-down"></a>Aufgabe nach oben und nach unten verschieben

Aufgaben können auf zwei Arten auf eine beliebige Ebene in den Projektstrukturplan verschoben werden:

- Wählen Sie eine weitere Aufgabe aus und ziehen Sie sie an die gewünschte Stelle.
- Wählen Sie eine oder mehrere Aufgaben aus, klicken Sie mit der rechten Maustaste und wählen Sie **Ausschneiden**. Wählen Sie die Zielzelle im Zeitplan aus, klicken Sie mit der rechten Maustaste und wählen Sie **Einfügen**.

## <a name="task-attributes"></a>Aufgabenattribute

Ein Aufgabenname beschreibt die Arbeit, die abgeschlossen werden muss. In Project Operations beschreiben die Attribute, die einer Aufgabe zugeordnet sein, den Zeitplan der Aufgabe und das erforderliche Personal.

## <a name="schedule-attributes"></a>Zeitplanattribute.

Die Attribute **Aufwand**, **Startdatum**, **Enddatum** und **Dauer** definieren den Zeitplan für die Aufgabe.

Die folgende Tabelle zeigt zusätzliche Zeitplanattribute.

| **Endgültiger Anzeigename** | **Endgültige Beschreibung** |
| --- | --- |
| Aufwand abgeschlossen (Stunden) | Gesamtaufwand der Aufgabe in Stunden. |
| Dauer | Zeigt die Dauer für die Aufgabe in Tagen an. |
| Gesamtaufwand | Gesamtarbeitsaufwand für die Aufgabe in Stunden. |
| Fertigstellen | Abschlussdatum und -uhrzeit. |
| % abgeschlossen | Der abgeschlossene Anteil der Aufgabe in Prozent. |
| Projekt-Bucket | Die Aufgabenübersicht kann nach Bucket gruppiert werden, sodass jedes Bucket eine eigene Spalte besitzt. |
| Aufwand verbleibend (Stunden) | Die verbleibende Arbeit für die Aufgabe in Stunden. |
| Anfang | Startdatum und -uhrzeit. |
| Name des Dataflows | Der Name der Projektaufgabe. |
| ID | Die ID der Aufgabe im Projektstrukturplan. |

Als Administrator können Sie benutzerdefinierte Felder in der Aufgabenentität definieren. Die Felder können jedoch nicht im Zeitplanraster angezeigt werden. Fügen Sie diese zum Anzeigen Ihrer benutzerdefinierten Felder der Detailseite **Projektaufgabe** hinzu.

## <a name="staffing-attributes"></a>Personalattributen.

Attribute der Personalbesetzung werden durch das Feld **Ressourcen** im Zeitplan angezeigt. Sie können entweder nach einer bestehenden Ressource suchen oder auf **Erstellen** klicken und im Bereich **Schnellerfassung** ein Projektteammitglied als neue Ressourcen hinzufügen.  Wenn Sie mit der Ressourcenauswahl im Aufgabenraster, in der Übersichtsansicht oder im Gantt nach einer Ressource suchen, gibt die Suche entweder vorhandene Projektteammitglieder oder aktive buchbare Ressourcen zurück.

Die Felder **Rolle**, **Ressourcenzuordnungseinheit** und **Positionsname** werden verwendet, um die Personalanforderungen für die Aufgabe zu beschreiben. Diese Stellenbesetzungsattribute zusammen mit dem Aufgabenplan werden verwendet, um die verfügbare Ressourcen zu finden, um diese Aufgabe auszuführen.

   - **Rolle**: Geben Sie die Art der Ressource an, die für die Aufgabe erforderlich ist.
   - **Ressourcenzuordnungseinheit**: Geben Sie die Einheit an, von der Ressourcen für die Aufgabe zugewiesen werden sollten. Dieses Attribut betrifft die Kosten- und Umsatzschätzung für die Aufgaben, wenn der Kosten- und Berechnungssatz für die Ressource auf Beschaffungseinheiten basieren.
   - **Positionsname**: Geben Sie einen Anzeigenamen für die allgemeine Ressource ein, der als Platzhalter für die Ressource dient, die letztendlich die Arbeit ausführen wird.

Das Feld **Ressourcen** enthält den Positionsnamen der generischen Ressource oder einer benannten Ressource , wenn eine gefunden wird.

Das Feld **Kategorie** enthält die Werte, die eine breitere Art der Arbeit angeben, in denen die Aufgabe kategorisiert werden kann. Dieses Feld betrifft nicht die Zeitplanung oder die Stellenbesetzung. Stattdessen wird das Feld nur für die Berichterstellung verwendet.

## <a name="task-dependencies"></a>Aufgabenabhängigkeiten

Sie können den Zeitplan in Project Operations verwenden, um Vorgängerbeziehungen zwischen Aufgaben zu erstellen. Das Feld **Vorgänger** verwendet einen oder mehrere Werte, um die Aufgaben anzugeben, von denen eine Aufgabe abhängt. Wenn Vorgängerwerte einer Aufgabe zugewiesen werden, kann die Aufgabe erst beginnen, nachdem alle vorherigen Aufgaben abgeschlossen wurden. Aufgrund der Abhängigkeit wird das geplante Startdatum der Aufgabe auf das Datum zurückgesetzt, an dem die Vorgängeraufgaben abgeschlossen wurden.

Der Aufgabenmodus hat keine Auswirkungen auf die Updates, die für das Start- und Enddatum vonVorgängern/abhängigen Aufgaben gemacht werden.

## <a name="accessibility-and-keyboard-shortcuts"></a>Barrierefreiheit und Tastenkombinationen

Auf das Raster **Zeitplan** kann vollständig zugegriffen werden, und es kann mit Bildschirmlesern wie Narrator, JAWS oder NVDA verwendet werden. Sie können durch den Rasterbereich navigieren, indem Sie die Pfeiltasten (wie in Microsoft Excel) verwenden. Sie können die TAB-TASTE verwenden, um über die interaktiven Benutzeroberflächenelemente zu navigieren, und Sie können den ABWÄRTSPFEIL, die EINGABETASTE oder LEERTASTE verwenden, um die Dropdownmenüs auszuwählen und zu öffnen.

## <a name="project-limitations"></a>Projekteinschränkungen 
Beachten Sie die folgenden Einschränkungen, wenn Sie den Projektstrukturplan in Project Operations verwenden. Diese Einschränkungen gelten für Projekte und Aufgaben. Weitere Informationen finden Sie unter [„Project for the web“-Einschränkungen und -Grenzen](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Feld**                                          |  **Grenze**           |
|----------------------------------------------------|----------------------|
| Maximale Gesamtanzahl an Aufgaben für ein Projekt                  | 500                  |
| Maximale Gesamtdauer für ein Projekt               | 3650 Tage (10 Jahre) |
| Maximale Gesamtressourcen für ein Projekt              | 300                  |
| Maximale Gesamtzahl der Links (nur Nachfolger) für ein Projekt | 600                  |
| Maximale Gesamtanzahl benutzerdefinierter Felder für ein Projekt          | 10                   |
| Maximale Checklistenpunkte pro Aufgabe                   | 20                   |

**Aufgabeneinschränkungen**

| **Feld**                               |   **Grenze**           |
|-----------------------------------------|-----------------------|
| Maximale Hierarchieebene                 | 10 Ebenen             |
| Maximale Links (Nachfolger + Vorgänger) | 20                    |
| Maximale Dauer der Blattaufgabe           | 1250 Tage             |
| Maximale Dauer einer Sammelaufgabe      | 3650 Tage (10 Jahre)  |
| Maximale Ressourcen, die einer Aufgabe zugewiesen sind    | 20 Ressourcen          |
| Unterstützter Datumsbereich für eine Aufgabe         | 1.1.2000 bis 31.12.2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
