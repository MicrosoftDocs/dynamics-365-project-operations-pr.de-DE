---
title: Buchungen und Arbeitsaufträge abstimmen
description: Dieses Thema enthält Informationen zu Ist-Werten.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 264271a5be63cb2e51f175595a48bef5fbff0a42a37795c85dd5b4725deec35e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995130"
---
# <a name="reconcile-bookings-and-assignments"></a>Buchungen und Arbeitsaufträge abstimmen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die Projektbuchungen und Projektaufgabenzuweisungen eines Projektteammitglieds sind lose verbunden. Deshalb kann eine Ressource über Aufgabenzuweisungen verfügen, die keinen Buchungen entsprechen, sowie über Buchungen, die keinen Aufgabenzuweisungen entsprechen. Idealerweise sind Projektbuchungen und -zuweisungen angepasst, sodass die Ressourcen ihre Kapazität für die Aufgabenzuweisungen festgelegt haben. In der Realität ist es jedoch so, dass Buchungen basierend auf der Verfügbarkeit auftreten können und die Aufgabenzeitplanung sich im Laufe des Projekts ändern kann. Aus diesem Grund ermöglicht die lose Verbindung Flexibilität.

Aufgrund der losen Verbindung von Projektbuchungen und -aufgabenzuweisungen ist auf der Projektentität eine Registerkarte **Abstimmung** vorhanden. Mit dieser Registerkarte können Projektmanager die Buchungen von Teammitgliedern und ihre Zuweisungen für ihr Projektteam abgleichen.

Für jedes benannte Teammitglied werden auf der Registerkarte **Abstimmung** Buchungen und Zuweisungen bis hinunter zur einzelnen Aufgabenzuweisung angezeigt. Sie zeigt Stunden in Zellen an, die für Zeitperioden von Monaten bis Tagen stehen können.

Wählen Sie im Feld **Zeitskala** die Option **Monat**, **Woche** oder **Tag** aus. Standardmäßig ist die Option **Woche** ausgewählt. Sie können den Standardwert jedoch ändern, indem Sie die Schaltfläche **Einstellungen** auswählen. Wenn die Registerkarte **Abstimmung** geöffnet ist, zeigt sie das aktuelle Datum an. Über den Kalender können Sie jedoch vor- oder zurückgehen. Wenn das Startdatum eines Projekts in der Zukunft liegt, zeigt die Registerkarte das Datum an, an dem es eröffnet wird. Der Kalender verfügt außerdem über Optionen, mit denen Sie Start- und Enddatum des Projekts verschieben können.

Sie können die Erweiterungssteuerelemente verwenden, um Details zu den Buchungen der einzelnen Ressourcen anzuzeigen. Außerdem können Sie die Zuweisungen jeder Ressource erweitern, bis hinunter zu den einzelnen Aufgaben.

Unten auf der Registerkarte **Abstimmung** werden eine allgemeine Nettosumme für das Projekt und eine Spalte der Gesamtsumme angezeigt. Für jede Ressource nimmt die Registerkarte den Unterschied zwischen den Buchungen eines Teammitglieds für das Projekt und einem Rollup der Aufgabenzuordnungen dieses Teammitglieds. Idealerweise sollte der Unterschied 0 (null) sein. Das bedeutet, dass es keinen Unterschied zwischen den Buchungen der Ressource und ihren Aufgabenzuweisungen geben sollte. Alle Unterschiede werden durch Farben und Schattierungen angezeigt, um zwei Bedingungen anzuzeigen:

- **Verlust der Buchung** – Buchungsverluste treten auf, wenn eine Ressource mehr Zuweisungen als Buchungen hat. Da diese Kapazität nicht reserviert wurde, kann ein Projektmanager diesen Zustand korrigieren, indem er die Ressourcenbuchungen erweitert, um den Verlust auszugleichen.
- **Überzählige Buchungen** – Überzählige Buchungen treten auf, wenn eine Ressource für das Projekt zwar gebucht, aber keinen Aufgaben zugewiesen wurde. Dieser Zustand kann akzeptabel sein, wenn beispielsweise die Ressource vor der Aufgabenzuweisung gebucht wurde. In anderen Fällen wird die Zuweisung der Ressource jedoch eventuell nicht eingeplant. In diesen Fällen sollte es der Projektmanager in Betracht ziehen, die Buchungen der Ressource zu stornieren, sodass die Kapazität für ein anderes Projekt verwendet werden kann.

> [!NOTE]
> Die Legende für diese Bedingungen kann ausgeblendet werden, um mehr Platz für das Raster zu schaffen. In diesem Fall können Sie die Legende einblenden, indem Sie die Schaltfläche **Einstellungen** auswählen.

In manchen Fällen, wenn das Feld **Zeitskala** auf eine höhere Ebene als **Tag** festgelegt ist, kann die Berechnung der Unterschiede 0 (null) ergeben. Beispielsweise kann der Nettounterschied für eine Ressource auf der Ebene **Monat** 0 (null) sein, um anzuzeigen, dass die Anzahl der Buchungen mit der Anzahl der Zuweisungen übereinstimmt. Wenn Sie jedoch die Ebene **Woche** betrachten, sehen Sie, dass es Zuweisungen mit 0 (null) Stunden und Buchungen mit 40 Stunden in der ersten Woche des Monats gibt, aber Zuweisungen von 40 Stunden und Buchungen von 0 (null) Stunden in der zweiten Woche des Monats. Obwohl die insgesamte Anzahl der Buchungen und Zuweisungen für den Monat übereinstimmt, unterscheiden sie sich doch pro Woche.

Wenn Sie höhere Zeitebenen anzeigen, zeigen die Zellen auf der Registerkarte **Abstimmung** einen Indikator an, um Sie darüber zu informieren, dass es Unterschiede auf tieferen Zeitebenen gibt. In der folgenden Abbildung beispielsweise wird in der Zelle für den Oktober 2018 für die Ressource mit dem Namen Karoline Kärchner ein Zellenindikator angezeigt. So können Sie sehen, dass für die Ressource auf tieferen Ebenen die Anzahl der Buchungen nicht mit der Anzahl der Zuweisungen übereinstimmt, obwohl dies bei einer Aggregierung auf der Ebene **Monat** der Fall ist

![Nicht übereinstimmende Buchungen und Zuordnungen auf monatlicher Ebene.](media/reconcile-assignments-01.JPG)

Doppelklicken Sie auf eine Zelle, um die nächstniedrigere Ebene zu vergrößern und den Unterschied anzuzeigen. Wenn Sie beispielsweise auf den Unterschied im Oktober 2018 für Karoline Kärchner doppelklicken, zeigen Sie Detailinformationen für die Ebene **Woche** an. Sie sehen, dass für die Ressource in den ersten zwei Oktoberwochen zwar Buchungen für 16 Stunden, aber keine Zuweisungen vorhanden sind. Für die dritte Oktoberwoche hingegen sind Zuweisungen für 16 Stunden, aber keine Buchungen vorhanden.

![Nicht übereinstimmende Buchungen und Zuordnungen auf wöchentlicher Ebene.](media/reconcile-assignments-02.JPG)

Klicken Sie mit der rechten Maustaste auf eine Zelle, um die nächsthöhere Ebene zu verkleinern. Sie können den Zellenindikator auch deaktivieren, indem Sie die Schaltfläche **Einstellungen** auswählen. 

Sie können auch die Schaltflächen **Zurück** und **Weiter** über dem Raster verwenden, um durch jegliche Unterschiede in Ihrem Projekt zu navigieren. Um diese Schaltflächen verwenden zu können, müssen Sie zuerst eine Ressource auswählen. Wählen Sie **Weiter** aus, um zum nächsten Unterschied zwischen den Buchungen und den Zuweisungen für diese Ressource zu navigieren. Wählen Sie **Zurück** aus, um zum vorherigen Unterschied zu navigieren.

Wenn Sie Aufgabenzuweisungen für eine Ressource ohne Buchungen haben, können Sie den Buchungsverlust und anschließend **Buchung erweitern** auswählen. Anschließend können Sie die Buchung sehen, die erforderlich ist, um den Buchungsverlust auszugleichen. Des Weiteren können Sie die Buchungen der Ressource für das aktuelle Projekt und weitere Projekte anzeigen. Wählen Sie **OK** aus, um die Buchung für Ressource zu erstellen, ohne Rücksicht auf die aktuelle Verfügbarkeit zu nehmen. Der Projektmanager oder der Ressourcenmanager kann dann die Zeitplanübersicht verwenden, um alle Situationen zu verwalten, in denen die Kapazität einer Ressource überbucht wurde, weil ihre Buchungen erweitert wurden.

## <a name="managing-with-time-zones"></a>Verwalten mit Zeitzonen
Um bei der Verwendung von Buchung erweitern genaue und vorhersehbare Ergebnisse zu erzielen, müssen zwei wichtige Voraussetzungen erfüllt sein:  

- Der Benutzer muss die Zeitzone seines Geräts so konfigurieren, dass sie mit der Zeitzone übereinstimmt, die in den Personalisierungseinstellungen Ihres Systems definiert ist.
 
  ![Zeitzoneneinstellungen in Windows 10.](media/reconcile-assignments-03.png)

  ![Zeitzoneneinstellungen in den Personalisierungseinstellungen.](media/reconcile-assignments-04.png)
 
- Die buchbare Ressource muss mindestens eine Minute Arbeitszeit haben, die sich mit den Konturen überschneidet, die zum Definieren der angeforderten Erweiterung verwendet werden. Das folgende Beispiel zeigt beispielsweise Ressourcen zur Überprüfung mit Arbeitszeiten zwischen 9:00 und 19:00 Uhr. 

  ![Vergleich der Ressourcenkonturen.](media/reconcile-assignments-05.png)

Die folgende Tabelle zeigt:

- Eine Projektkalendervorlage.
- Ressource A: Diese Ressource verfügt über denselben Kalender und befindet sich in derselben Zeitzone wie das Projekt. Die Buchung beginnt um 9:00 Uhr.
- Ressourcen B: Diese Ressource befindet sich in einer anderen Zeitzone als das Projekt und beginnt daher um 7:00 Uhr in ihrer Zeitzone. Die Buchungen beginnen jedoch um 9:00 Uhr, da dies der früheste Startzeitpunkt der Zuordnungskontur ist.
- Ressourcen C und D: Die Ressourcen befinden sich auch in unterschiedlichen Zeitzonen, die sich voneinander und vom Projekt unterscheiden, und ihre Buchungen beginnen frühestens zu den jeweils verfügbaren Startzeiten.

|Entity  |Kalender  |
|-|-|
|Projektkalendervorlage   | ![Projektkalender.](media/reconcile-assignments-06.png) |
|Ressource A  | ![Kalender Ressource A.](media/reconcile-assignments-06.png) |
|Ressource B  |  ![Kalender Ressource B.](media/reconcile-assignments-07.png) |
|Ressource C  |  ![Kalender Ressource C.](media/reconcile-assignments-08.png) |
|Ressource D  | ![Kalender Ressource D.](media/reconcile-assignments-09.png)  |
 
Wenn Sie zur Abstimmungssicht navigieren, werden die Ressourcenzuordnungen und die damit verbundenen Buchungsengpässe angezeigt.
 ![Abstimmungssicht vor Erweiterung.](media/reconcile-assignments-10.png)

Nachdem die Funktion Buchung verlängern für jede Ressource ausgeführt wurde, werden Buchungen für jede Ressource erfolgreich verlängert. Dies liegt daran, dass sich die Arbeitsstunden jeder Ressource mit den Konturen des Mangels überschneiden.
 ![Abstimmungssicht nach Buchungsverlängerung.](media/reconcile-assignments-11.png) 

Ein genauerer Blick auf die Details der Buchungen zeigt jedoch Unterschiede in der Startzeit der Buchungen. Die Buchungen beginnen frühestens zum Startzeitpunkt der Zuordnungskontur und frühestens zum verfügbaren Startzeitpunkt der Ressource.
 ![Neue Buchungen der Ressourcen in der Zeitplantafel.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]