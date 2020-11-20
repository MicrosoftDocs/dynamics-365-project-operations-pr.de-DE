---
title: Zuweisen einer Ressource zu einer Aufgabe
description: In diesem Thema finden Sie Informationen zum Zuweisen von Ressourcen zu Aufgaben.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125132"
---
# <a name="assign-a-resource-to-a-task"></a>Zuweisen einer Ressource zu einer Aufgabe

Es gibt drei Möglichkeiten, eine Ressource zu einer Aufgabe in Microsoft Dynamics 365 Project Service Automation zuzuweisen.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Sie können eine Ressource als Teammitglied buchen und dann einer Aufgabe zuweisen.

Mit dieser Methode fügen Sie eine Ressource dem Projektteam hinzu. Anschließend weisen Sie Aufgaben der Ressource im Projektzeitplan zu.

1. Fügen Sie auf der Registerkarte **Teammitglied** ein neues Teammitglied hinzu, indem Sie **Neu** auswählen. 

2. Der Bereich **Schnellerfassung: Teammitglied** wird geöffnet. Hier können Sie den Namen der buchbaren Ressource auswählen und eine Rolle festlegen. 

    Wählen Sie eine der folgenden Zuordnungsmethoden für die Buchung der Ressource aus:

    - **Volle Kapazität** bucht die Kapazität der vollständige Ressource zum angegebenen Datumsangaben aus und nach.
    - **Kapazität in Prozent** Bucht die Ressource für einen Prozentsatz der Kapazität der Ressource für das angegebene von Datumsangaben und nach.
    - **Nach Stunden gleichmäßig verteilen** Bucht die Ressource für eine bestimmte Anzahl und Stunden und verteilt diese gleichmäßig pro Tag zwischen dem angegebenen Start- und Enddatum.
    - **Nach Stunden von vorn nach hinten verteilen** Bucht die Ressource für eine festgelegte Anzahl und Stunden von vorn nach hinten und verteilt sie zu angegebenen Daten aus und nach.
    - Wählen Sie andernfalls **Keine**, da die Ressource dem Team hinzugefügt wird, aber keine Anmeldungen erstellt, um die Kapazität der Ressource zu absorbieren.

3. Wählen Sie im **Zeitplanraster** einer Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle und wählen Sie anschließend unter **Teammitglieder** das Teammitglied aus, das Sie soeben hinzugefügt haben. 

> [!NOTE]
> Auf den Registerkarten **Teammitglied** und **Abstimmung** weist die Ressource die gebuchten und zugewiesenen Stunden auf. Die Stunden sollten gleich sein, dies ist jedoch nicht erforderlich, da Buchungen und Zuweisungen nicht fest miteinander gekoppelt sind. Auf der Registerkarte **Abstimmung** werden Details angezeigt, wenn sich diese unterscheiden, z. B. wenn Sie einer Ressource mehr Stunden zuweisen, als Sie gebucht haben. Bei Bedarf können Sie die Informationen korrigieren, indem Sie die Buchungen der Ressource erweitern oder die Zuweisung ändern.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Erstellen eines generischen Teammitglieds über die Aufgabenzuweisung

Wenn Sie ein generisches Teammitglied durch Aufgabenzuweisung erstellen, erstellen Sie einen Platzhalter oder eine generische Ressource, die die Merkmale der benannten Ressource beschreibt, die letztendlich die Aufgaben durchführen soll. Anschließend generieren Sie eine Anforderung (oder übermittelnd eine Anforderung mithilfe der Anforderung), die zum Suchen und Buchen der genannten Ressource verwendet wird.

1. Wählen Sie im **Zeitplanraster** für eine Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle aus.

2. Geben Sie einen Namen als Namen für die Platzhalterressource ein. Zum Beispiel Projektleiter.

3. Wählen Sie **Erstellen** aus und legen Sie im Feld **Schnellerfassung: Projektteammitglied** die Rolle für die allgemeine Ressource fest.

4. Sie können dieser Platzhalterressource weitere Aufgaben zuweisen, indem Sie die Ressource in der **Ressourcenauswahl** für die Aufgabe auswählen. Sie sind unter **Teammitglieder** aufgelistet.

5. Wenn Sie die allgemeine Ressource zugewiesen haben, wählen Sie sie auf der Registerkarte **Team** aus und wählen Sie dann **Anforderung erstellen**, um eine Ressourcenanforderung für die generische Ressource zu erstellen.

6. Wählen Sie **Buchen** für die allgemeine Ressource. Mithilfe der Zeitplanübersicht können Sie echte Ressourcen suchen und buchen. Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden.

7. Wenn die allgemeine Ressource mit einer benannten Ressource erfüllt ist, wird die aufgewendete allgemeine Ressource aus dem Team entfert und die Aufgabenzuordnungen für die allgemeine Ressource werden der benannten Ressource zugewiesen, mit dem generische Ressourcenanforderungen für der Ressource erfüllt wurden.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Zuweisen einer benannten Ressource aus der Liste aller buchbaren Ressourcen

Sie können das Suchfeld in der **Ressourcenauswahl** verwenden, um alle buchbaren Ressourcen zu durchsuchen und einer Aufgabe zuzuweisen.

Auf diese Weise zugewiesene Ressourcen werden dem Team ohne Buchungen hinzugefügt. Dies ist dem Hinzufügen eines Teammitglieds und dem Auswählen von „Keine” als Zuweisungsmethode ähnlich. Die Ressource wird auf den Registerkarten **Team** und **Abstimmung** als Ressource mit nur Zuweisungen und einem Buchungsdefizit angezeigt. Buchen Sie sie, wenn Sie die Verfügbarkeit verwenden möchten.

1. Wählen Sie im **Zeitplanraster** für eine Aufgabe das **Ressourcen**-Symbol in der Ressourcenzelle aus.

2. Starten Sie mit dem Eingeben des Namens. Die Suchergebnisse für den Namen werden in die **Ressourcenauswahl** unter **Weitere Ressourcen** angezeigt.

3. Wählen Sie die Ressource aus, die Sie der Aufgabe zuweisen möchten.

