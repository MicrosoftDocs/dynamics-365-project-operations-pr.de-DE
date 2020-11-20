---
title: Wie weise ich einer Aufgabe in der Web-App eine buchbare Ressource zu?
description: Eine Übersicht über die Möglichkeiten, buchbare Ressourcen zuzuweisen.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: cc1859540ede064c4ab3e2ac128573972912a207
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125177"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Wie weise ich eine Projektressourcenrolle einer Aufgabe in der Internet-App zu (Project Service-App v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Es gibt zwei Möglichkeiten, eine Ressource zu einer Aufgabe in Project Service zuzuweisen. Sie können eine Ressource als Teammitglied planen und dann einer Aufgabe zuweisen. Oder Sie können ein allgemeines Teammitglied durch Rollenzuweisung zu Aufgaben erstellen, ein Team erstellen, und dann die Anforderungen mit einer benannten Ressource abdecken.

Beachten Sie, dass Sie, wenn Sie eine buchbare Ressource einer Aufgabe zuweisen möchten, das buchbare Rssourcenteammitglied ausreichend verfügbare Anmeldungen haben muss. Der Status der Anmeldung muss festgeleger Übernahmetyp und Status festgelegt sein. Falls nicht ausreichend Anmeldungen für die Ressource vorhanden sind, entfernt Project Service die Zuweisung und die folgende Fehlermeldung ‏wird angezeigt:

*Die Ressource kann der Aufgabe nicht zugewiesen werden - folgende Ressourcen verfügen nicht über ausreichend gebuchte Zeiten für das Projekt*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Sie können eine Ressource als Teammitglied planen und dann einer Aufgabe zuweisen.

Mit dieser Methode fügen Sie eine Ressource dem Projektteam hinzu. Anschließend weisen Sie Aufgaben der Ressource im Projektzeitplan zu. So führen Sie diese Aufgabe aus:
1.  Klicken Sie im Teammitgliedsraster und fügen Sie ein neues Teammitglied hinzu, indem Sie **Neu** aktivieren.
2.  Auf dem Teammitglied, das der Bildschirm erstellen, aktivieren Sie den buchbaren Ressourcennamen und legen die Rolle fest.
3.  Wählen Sie die **Von**- und **An**-Daten aus.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot des Hinzufügens eines Teammitglieds](media/FAQ-Resources-to-Tasks2-1.png "Screenshot des Hinzufügens eines Teammitglieds")
 
4.  Dann wählen Sie eine der folgenden Zuordnungsmethoden für die Buchung der Ressource aus:
    - **Volle Kapazität** bucht die Kapazität der vollständige Ressource zum angegebenen Datumsangaben aus und nach.
    - **Kapazität in Prozent** Bucht die Ressource für einen Prozentsatz der Kapazität der Ressource für das angegebene von Datumsangaben und nach.
    - **Nach Stunden gleichmäßig verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden gleichmäßig sie verteilt um die zum angegebenen Datumsangaben aus und nach.
    - **Nach Stunden von vorn nach hinten verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden von vorn nach hinten und verteilt sie zu angegebenen Daten aus und nach.

    Wählen Sie andernfalls **Keine**, da die Ressource dem Team hinzugefügt wird, aber erstellt keine Anmeldungen erstellt, um die Kapazität der Ressource zu absorbieren.
5.  Wählen Sie **Speichern** aus.

    Beachten Sie, dass die Stunden der Anmeldung ausreichend sein, um die Aufwandsstunden und die Datumsbereiche der Aufgaben auch wirklich abzudecken, die Sie diesen Ressource zuweisen. Wenn sie nicht ausgerichtet sind, können Sie die Ressource nicht mehr der Aufgabe zuweisen.

6.  Im Projektstrukturplan (WBS) für die Aufgaben, klicken Sie auf das Dropdown-Menü Ressourcenzellen dann: 

    1. Wählen Sie **Hinzufügen** aus.
    2. Wählen Sie das Dropdown-Listenfeld aus unter **Ressourcen** und wählen Sie das Teammitglied aus, das Sie oben hinzugefügt haben.
    3. Wählen Sie **OK** aus. Das Teammitglied ist nun der Aufgabe zugewiesen.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot des Hinzufügens von Ressourcen mit WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot des Hinzufügens von Ressourcen mit WBS")
 
Klicken Sie im Teammitgliedsraster und Sie finden im Aggregat der Ressource zugewiesene Stunden mit zugeteilten Stunden. Sie ist kleiner oder gleich der gebuchten Stunden für die Ressource. 

> [!div class="mx-imgBorder"] 
> ![Screenshot der zugewiesenen Stunden für eine Ressource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot der zugewiesenen Stunden für eine Ressource")
 
Wenn die Aufgabe, die Sie gerade der Ressource zuweisen möchten nach dem Enddatum der gebuchten Ressourcen beginnt, erscheint die Ressource nicht im Dropdown-Menü.

Beachten Sie, dass Sie eine Ressource zu mehr Stunden als die gebuchten Stunden zuweisen können, wenn die Ressource verbleibende nicht zugewiesene Kapazität hat. In diesem Fall wird die Ressource nur teilweise bei Anmeldungen zugewiesen. Sie können die restlichen nicht zugewiesene Aufgabenstunden anzeigen, indem Sie in der Unstaffed-Stundenspalte den Projektstrukturplan hinzufügen.

Wenn Ressourcen den gebuchten Stunden zugewiesen werden (die gebuchten Stunden entsprechen den zugewiesenen Stunden), wird die folgende Fehlermeldung angezeigt, wenn Sie versuchen, weitere Aufgaben zuzuweisen:

*Die Ressource kann der Aufgabe nicht zugewiesen werden - folgende Ressourcen verfügen nicht über ausreichend gebuchte Zeiten für das Projekt*

Außerdem wird das Standardprojekt Teammitglied verwalten, dem Team hinzugefügt, wenn Sie das Projekt erstellen, ohne die Anmeldungen hinzuzufügen und kann nicht zu einer dieser Aufgaben zugewiesen werden. Sie werden nicht im Ressourcendropdown-Menü für Aufgaben angezeigt.

Wenn Sie diese Ressourcen zuweisen möchten, müssen Sie sie vom Team entfernen und dann mit einer Zuordnungsmethode außer keine erneut hinzufügen. Der Grund, wieso Sie dem Team hinzugefügt werden, wenn das Projekt erstellt wird ist, weil ein Projekt mindestens einen Projektgenehmiger standardmäßig hat.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Erstellen Sie ein allgemeins Teammitglied durch Rollenzuweisung auf Aufgaben

Diese Methode, gewährleistet, dass genügend Anmeldungen für Aufgaben bereitstehen. Erstellen Sie zunächst einen Platzhalter oder eine allgemeine Ressource, die die Eigenschaften der benannten Ressource beschreiben, die Sie letztendlich bearbeiten möchten, indem Sie ein Team erstellen, nachdem Sie Rollen an Aufgaben zugewiesen haben. So führen Sie diese Aufgabe aus:

1. Im Projektstrukturplan wählen Sie eine Aufgabe aus.
2. Wählen Sie das Symbol **Zugewiesene Rolle** in der Ressourcenzelle aus.
3. Wählen Sie das **Rolle** Dropdown-Listenfeld und die Rolle für die allgemeine Ressource aus.
4. Wählen Sie **OK** aus.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot des Hinzufügens von Ressourcen mithilfe von WBS](media/FAQ-Resources-to-Tasks2-4.png "Screenshot des Hinzufügens von Ressourcen mithilfe von WBS")
 
Wenn Sie Rollen zu den Aufgaben einem Benutzer im PSP zuweisen abgeschlossen haben, wählen Sie **Projektteam generieren** aus. Project Service erstellt die Mindestanzahl von Teammitgliedern basierend auf den Rollen, den Beschaffungsorganisationseinheiten und dem Projektkalender, indem Sie die Aufgabenzuordnungen zusammenfassen.

> [!div class="mx-imgBorder"] 
> ![Screenshot der Erstellung eines Projektteams](media/FAQ-Resources-to-Tasks2-5.png "Screenshot der Erstellung eines Projektteams")
 
Klicken Sie im Teammitgliedsraster und suchen Sie die Ressourcen des generischen Ressourcentyps mit den rollen und Positionsnamen. Wenn zwei Ressourcen erforderlich sind, damit eine Rolle abgeschlossen werden kann, erstellt die Teamfunktion zwei Teammitglieder und verwendet Positionsnamen, um Sie zu unterscheiden.

> [!div class="mx-imgBorder"] 
> ![Screenshot des Hinzufügens von zwei allgemeinen Ressourcen](media/FAQ-Resources-to-Tasks2-6.png "Screenshot des Hinzufügens von zwei allgemeinen Ressourcen")
 
Sie können die unterstützende Ressourcenanforderung für das allgemeine Teammitglied öffnen, indem Sie den Link mit Ressourcenanforderungen auswählen.

> [!div class="mx-imgBorder"] 
> ![Screenshot vom Öffnen von unterstützenden Ressourcenanforderung](media/FAQ-Resources-to-Tasks2-7.png "Screenshot vom Öffnen von unterstützenden Ressourcenanforderung")

**Buchen** wählen Sie für die allgemeine Ressource und dann können Sie die Zeitplanübersicht verwenden, um eine echte Ressource zu suchen und zu buchen. Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden, indem Sie **Übermittlungsanfrage** aktivieren.

Wenn die allgemeine Ressource mit einer benannten Ressource erfüllt ist, wird die aufgewendete allgemeine Ressource aus dem Team entfert und die Aufgabenzuordnungen für die allgemeine Ressource werden der benannten Ressource zugewiesen, mit dem generische Ressourcenanforderungen für der Ressource erfüllt wurden.
 

