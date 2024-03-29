---
title: Projektvorlagen
description: In diesem Artikel erfahren Sie, wie Sie Projektvorlagen für eine schnelle Einrichtung von Projekten verwenden können.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 03cccf8f0201d82db57e52dc1175fcf9a7812a53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930869"
---
# <a name="project-templates"></a>Projektvorlagen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Eine Projektvorlage ist eine vordefiniertes Framework, mit dessen Hilfe Sie schnell und problemlos ein Projekt starten können. Verwenden Sie eine vordefinierte Vorlage, um mit einem Klick ein neues Projekt zu erstellen. Wie für Projekte auch müssen Sie die Voraussetzungen für Projektvorlagen definieren. Sie müssen für jede Projektvorlage einen Projektkalender definieren. Außerdem müssen in der Organisation Rollen und Preislisten vordefiniert werden, damit für die Komponenten der Vorlage sinnvolle Daten vorhanden sind.

Eine Projektvorlage umfasst drei Komponenten: einen Zeitplan, Projektvorkalkulationen und Projektteammitglieder.

## <a name="schedule"></a>Zeitplan

Ein Zeitplan in einer Projektvorlage enthält denselben Satz von Elementen wie ein Zeitplan in einem Projekt. Sie können eine Aufgabenhierarchie erstellen, Rollen mit Aufgaben verknüpfen, Zeitplanattribute definieren und Abhängigkeiten festlegen. Ein Zeitplan in einer Projektvorlage unterstützt außerdem Aufgabenmodi für jede Aufgabe. Daher unterstützt er das Planungsmodul. Sie müssen dem Projekt einen Projektkalender zuordnen. Wenn Sie einen Arbeitszeitplan erstellen, gibt es keinen Unterschied zwischen einer Projektvorlage und einem Projekt.

## <a name="project-estimates"></a>Projektvorkalkulationen

Projektvorkalkulationen in einer Projektvorlage funktionieren auf dieselbe Weise wie Projektvorkalkulationen in einem Projekt. Allerdings werden die Kosten und Verkaufspreise aus den Standardlisten für Kosten und Verkaufspreise abgerufen, die in den Parametern definiert sind.

## <a name="creating-a-project-from-a-template"></a>Erstellen eines Projekts aus einer Vorlage
 
Es gibt mehrere Möglichkeiten, aus einer Projektvorlage ein Projekt zu erstellen:

- Wenn Sie ein Projekt aus einem Angebot erstellen, können Sie im Dialogfeld **Schnellerfassung: Projekt** eine Projektvorlage auswählen.

> ![Das Dialogfeld „Schnellerfassung: Projekt“.](media/project-11.png)

- Wenn Sie ein Projekt erstellen, indem Sie **Neues Projekt** auswählen, wird die Seite **Projekt** angezeigt, bevor der Datensatz gespeichert wird. Wählen Sie im Feld **Eine Vorlage auswählen** eine der in der Organisation vordefinierten Projektvorlagen aus.
- Verwenden Sie **Projekt aus einer Vorlage erstellen** auf der Seite **Vorlagenentität** aus.

## <a name="copying-components-of-template-to-project"></a>Kopieren von Komponenten einer Vorlage in ein Projekt

Wenn Sie die Komponenten einer Projektvorlage in ein Projekt kopieren, können abhängig von den Einstellungen im Projekt einige Außerkraftsetzungen auftreten.

### <a name="copying-the-schedule"></a>Kopieren des Zeitplans

Wenn Sie den Zeitplan aus einer Projektvorlage kopieren und das Projekt einen anderen Projektkalender als die Vorlage hat, werden die Arbeitsstunden aus dem Kalender des Projekts auf den Aufgabenzeitplan angewendet. Dadurch wird der Zeitplan an den zugrundeliegenden Projektkalender angepasst. Entsprechend übernimmt die erste Aufgabe im Zeitplan das Startdatum des Projekts und der Zeitplan der restlichen Hierarchie wird basierend auf der Dauer und den Abhängigkeiten aktualisiert, die in der Vorlage angegeben sind. 

### <a name="copying-project-estimates"></a>Kopieren der Projektvorkalkulationen 

Wenn Sie Positionen aus der Projektvorkalkulation kopieren, werden die Preislisten aktualisiert. Für die Einstandspreisliste basieren diese Aktualisierungen auf der zuständigen Einheit des Projekts. Für die Verkaufspreisliste basieren sie auf dem Kunden. Für Projekte, die einer Vertriebsentität zugeordnet sind, werden die Einheitskosten und die Verkaufspreise anhand dieser Preislisten bestimmt.

### <a name="copying-a-project-team"></a>Kopieren eines Projektteams

Wenn ein Projektteam aus einer Projektvorlage in ein Projekt kopiert wird, werden die generischen Ressourcen zusammen mit den Kompetenzen und Fähigkeiten kopiert, die in der Vorlage definiert sind. Generische Ressourcenzuweisungen werden wie in der Projektvorlage verwaltet. Benannte Ressourcen werden in Projektvorlagen nicht unterstützt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
