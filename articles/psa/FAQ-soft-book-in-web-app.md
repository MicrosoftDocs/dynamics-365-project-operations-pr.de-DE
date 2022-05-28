---
title: Wie mache ich eine vorläufige Buchung in der App Version 2.x?
description: In diesem Artikel wird beschrieben, wie Projektteammitglieder provisorisch mit Project Service gebucht werden.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 472529c146fbb5e7a4540676c880cabd4ab1a32b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585193"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Wie buche ich Ressourcen vorläufig in der Web (Project Service-App v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sie können vorläufig planen oder eine Ressource für ein Projektteam „unverbindlich buchen“, um zu zeigen, dass Sie eine Ressource dem Projekt zuweisen möchten. Vorläufige Buchungen nutzen die verfügbare Kapazität einer Ressource nicht. Vorläufig gebuchte Teammitglieder können nicht für die Projektaufgaben zugewiesen werden. Nur Ressourcen mit dem Status definitiv gebucht und bestätigte Typen können Aufgaben zugewiesen werden (vorausgesetzt, sie haben genügend definitive Stunden, um den Zuweisungsaufwand auch wirklich abzudecken).

Vorläufig gebuchte Projektteammitglieder werden im Teammitgliedsraster mit ihren vorläufig gebuchten Stunden in der vorläufigen Buchungsspalte angezeigt. Sie werden auch in der Zeitplanübersicht angezeigt. Sie geben wieder keinen Verbrauch der Kapazität an, da vorläufige Buchungen keine Kapazität einer Ressource brauchen.

Es gibt drei Arten, ein Teammitglied im Projekt mit Project Service Version 2.x vorläufig zu buchen.. Sie können mithilfe der Zeitplanübersicht vorläufig buchen und die Funktion Wartungsbuchung nutzen oder eine allgemeine Ressource erstellen. Diese Methoden werden unten beschrieben.

## <a name="soft-book-with-the-schedule-board"></a>Vorläufige Buchungen mit der Zeitplanübersicht

Folgen Sie für vorläufige Buchungen dieser Vorgehensweise: 
1. Zeitplanübersicht öffnen.
2. Wählen Sie die Projektregisterkarte unten auf dem Buchungsanforderungsbereich der Zeitplanübersicht.
3. Suchen Sie das des Projektmanagements, das Sie Weichbuch eine Ressource angezeigt werden soll. Wenn Sie viele Projekte haben, klicken Sie auf der Projektspaltenüberschrift und anschließend auf den Filter, um das Projekt zu suchen.
4. Klicken Sie auf das Projekt und ziehen Sie es auf den Zeitraster der betroffenen Ressource.
5. Dadurch wird der erstellte-Ressourcen-Anmeldungsbereich rechts geöffnet. Passen Sie die Start- und Enddaten an, wählen Sie den Anmeldungs-Status aus, wie vorläufig und legen Sie die Stunden fest. 
6. Klicken Sie auf buchen.
7. Zurück im Projekt, zeigt die Ressource nun ein Team-Mitglied mit den vorläufig gebuchten Stunden in der vorläufigen Buchungsspalte.

Beachten Sie, dass Sie diesen keine Aufgaben im Projektstrukturplan (WBS) zuweisen können, da Ressourcen im zugewiesen Team fest gebucht werden müssen.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Vorläufig buchen mithilfe der vorläufigen Wartungs-Buchungsfunktion

Für vorläufige Buchungen mit der Wartungsbuchung folgen Sie diesem Prozess:
1. Vom Teammitgliedsraster klicken Sie auf die Schaltfläche Neu.
2. Wählen Sie die Projektressource, Rolle, von/zu.
3. Wählen Sie eine Zuordnungsmethode nicht gleich Keine:
- Volle Kapazität
- Kapazität in Prozent
- Nach Stunden gleichmäßig verteilen
- Nach Stunden von vorn nach hinten verteilen
4. Klicken Sie auf „Speichern“. Sie sehen die Ressource für den Teamraster und die Zeiten, die als definitiv angegeben werden.
5. Sie können die Ressourcen der Anmeldungen verwalten, indem Sie auf Buchungen verwalten klicken.
6. Wenn der Zeitplanübersicht geöffnet wird, erweitern Sie die Ressource, um ihre Anmeldungen anzuzeigen. Sie sehen die Buchung als definitiv.
7. Klicken Sie auf die Buchung unter Änderungsstatus und wählen Sie vorläufige Buchung und dann vorläufig. Der Buchungsstatus ist nun vorläufig.
8. Nachdem die Zeitplanübersicht geschlossen wurde, sehen Sie, dass die Stunden für die Ressource von definitiv zu vorläufig gewechselt haben auf dem Teammitgliedsraster.
Beachten Sie auch wenn Sie hartes Buchs eine Ressource für das Team und weisen Sie ihnen Aufgaben in PSP dann auf, wenn Sie für Anmeldungen, um den Status der Weiche dringend, können ihn in ändert sich Zuweisungen von Aufgaben für die Ressource entfernt, z nur dringend empfohlen gebuchte Ressourcen zu den Aufgaben zugewiesen werden kann.

## <a name="soft-book-by-creating-a-generic-resource"></a>Vorläufige Buchungen durch erstellen einer generischen Ressource

Sie können eine vorläufige Buchung erstellen, indem Sie ein Ressourcenteammitglied erstellen, und deZeitplan oder die Ressourcenanforderung erfüllen und den Typ während der Buchung ändern.
Dazu verwenden Sie diesen Verfahren:

1. Auf dem Projekt PSP, weisen Sie die Rollen den Aufgaben zu, für die Sie allgemeine Teammitglieder erstellen möchten.
2. Klicken Sie auf Projektteam generieren.
3. Klicken Sie im Projektteammitgliedsraster auf allgemeine Ressource und klicken Sie auf buchen.
4. Auf der Zeitplanübersicht wählen Sie die Ressource aus, die Sie planen möchten.
5. Auf der Zeitplanübersicht im Ressourcen-Anmeldungsbereich ändern Sie den Buchungsstatus auf vorläufig.
6. Klicken Sie auf buchen oder Buchen und Beenden.

Nachdem Sie die Zeitplanübersicht geschlossen haben, beachten Sie, dass die ausgewählte Ressource, die dem Team gebuchte Stunden mit vorläufig hinzugefügt wird und auch die Stunden zugewiesen werden. Sie sehen auch, dass die allgemeine Ressource für das Team als Indikator bleibt, dass die Aufgaben einem vorläufigen Teammitglied zugewiesen werden.

Wenn Sie bereit sind, vorläufig gebuchte Teammitgliedsressource in ein definitiv gebuchtes Teammitglied zu ändern, sodass Sie sie den Aufgaben zuweisen können, gehen Sie folgendermaßen vor:

1. Wählen Sie die Ressource aus und klicken Sie Buchungen verwalten.
2. Wenn der Zeitplanübersicht geöffnet wird, erweitern Sie die Ressource, um ihre Anmeldungen anzuzeigen. Sie sehen die Buchung als vorläufig markiert.
3. Klicken Sie auf die Buchung unter Änderungsstatus und wählen Sie definitive Buchung und dann definitiv. Der Buchungsstatus ist nun definitiv.
4. Nachdem die Zeitplanübersicht geschlossen wurde, sehen Sie, dass die Stunden für die Ressource von vorläufig auf definitiv im Teammitgliedsraster gewechselt hat. Sie können nun die Ressource den Aufgaben zuweisen (sofern eine Ausrichtung zwischen den definitiven gebuchten Stunden und den Aufwandsstunden der Aufgabe besteht). Beachten Sie, dass Sie den Ressourcenerfüllungsschritten im Element #3 oben folgen, wenn Sie den Status der vorläufig gebuchten, buchbaren Ressource auf definitiv buche. Das allgemeine Teammitglied wird vom Team entfernt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
