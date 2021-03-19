---
title: Zeitzonen verwalten
description: Wenn ein Projekt erstellt wird, basiert dessen Zeitzone auf der Zeitzone, die in der angewendeten Arbeitszeitvorlage definiert ist.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279542"
---
# <a name="manage-time-zones"></a>Zeitzonen verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


## <a name="projects"></a>Projekte

Wenn ein Projekt erstellt wird, basiert dessen Zeitzone auf der Zeitzone, die in der angewendeten Arbeitszeitvorlage definiert ist. Im entsprechenden **Projekt** beziehen sich die Daten immer auf die Zeitzone des Benutzers, der auf jeder Registerkarte angemeldet ist, mit Ausnhame der Registerkarte **Aufgabe**. Wenn Sie den Projektstrukturplan anzeigen, werden die Daten immer in der Zeitzone des Projekts angezeigt.

## <a name="tasks"></a>Tasks

Wenn eine Aufgabe erstellt wird, werden Startzeit, Endzeit und Stunden/Tag durch die Arbeitsstunden des Projekts gesteuert. Wenn beispielsweise eine Aufgabe mit einem Projekt erstellt wird, dessen Zeitzone -8 PST ist und Arbeitszeiten von montags bis freitags von 9:00 bis 17:00 Uhr aufweist, berücksichtigt jede Aufgabe, die ohne Abeitsauftrag erstellt wurde, die Startzeit und Endzeit des Projektkalenders.

## <a name="manage-resources-with-time-zones"></a>Ressourcen mit Zeitzonen verwalten

Um genaue und vorhersehbare Ergebnisse bei der Verwendung von **Buchung erweitern** zu erzielen, gibt es zwei wichtige Voraussetzungen, die erfüllt sein müssen:  

- Der Benutzer muss die Zeitzone seines Geräts so konfigurieren, dass sie mit den Zeitzonen überinstimmt, die in den **Personalisierungseinstellungen** des Systems definiert sind.
 
  ![Zeitzoneneinstellungen in Windows 10](media/reconcile-assignments-03.png)

  ![Zeitzoneneinstellungen in den Personalisierungseinstellungen](media/reconcile-assignments-04.png)
 
- Die buchbare Ressource muss mindestens eine Minute Arbeitszeit haben, die sich mit den Konturen überschneidet, die zum Definieren der angeforderten Erweiterung verwendet werden. Nehmen wir als Beispiel die folgenden Ressourcen mit Arbeitszeiten, die zwischen 9:00 und 19:00 Uhr liegen. 

  ![Vergleich der Ressourcenkonturen](media/reconcile-assignments-05.png)

Die folgende Tabelle zeigt:

- Eine Projektkalendervorlage
- Ressource A: Diese Ressource verfügt über denselben Kalender und befindet sich in derselben Zeitzone wie das Projekt. Die Buchung beginnt um 9:00 Uhr.
- Ressource B: Diese Ressource befindet sich in einer anderen Zeitzone als das Projekt und beginnt um 7:00 Uhr in ihrer Zeitzone. Die Buchungen beginnen jedoch um 9:00 Uhr, da dies der früheste Startzeitpunkt der Zuordnungskontur ist.
- Ressourcen C und D: Die Ressourcen befinden sich in unterschiedlichen Zeitzonen, die sich voneinander und vom Projekt unterscheiden, und ihre Buchungen beginnen nicht früher als die jeweils verfügbaren Startzeiten.

|Entität  |Kalender  |
|-|-|
|Projektkalendervorlage   | ![Projektkalender](media/reconcile-assignments-06.png) |
|Ressource A  | ![Kalender Ressource A](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Kalender Ressource B](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Kalender Ressource C](media/reconcile-assignments-08.png) |
|Ressource D  | ![Kalender Ressource D](media/reconcile-assignments-09.png)  |
 
Wenn Sie zur Ansicht **Abstimmung** navigieren, werden die Ressourcenzuweisungen und die damit verbundenen Buchungsverluste angezeigt.

![Abstimmungssicht vor Erweiterung](media/reconcile-assignments-10.png)

Nachdem die Funktion zum Erweitern der Buchung für jede Ressource verwendet wurde, werden die Buchungen für jede Ressource erfolgreich erweitert, da sich die Arbeitszeiten jeder Ressource mit den Konturen des Verlusts überschneiden.

![Abstimmungssicht nach Buchungsverlängerung](media/reconcile-assignments-11.png) 

Beachten Sie, dass ein genauerer Blick auf die Details der Buchungen Unterschiede in der Startzeit der Buchungen zeigt. Die Buchungen beginnen frühestens zur Startzeit der Zuordnungskontur und frühestens zur verfügbaren Startzeit der Ressource.

![Neue Buchungen der Ressourcen in der Zeitplantafel](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]