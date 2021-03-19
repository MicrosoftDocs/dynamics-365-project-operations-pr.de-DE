---
title: Ressourcenzuweisungen erstellen
description: Dieses Thema enthält Informationen zum Erstellen generischer und benannter Ressourcenzuweisungen.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287102"
---
# <a name="create-resource-assignments"></a>Ressourcenzuweisungen erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Eine Ressourcenzuweisung ist die direkte Zuordnung eines Projektteammitglieds zu einer Blattknotenaufgabe. In diesem Thema finden Sie Informationen zu den unterschiedlichen Methoden für das Zuweisen von Ressourcen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Erstellen eines generischen Teammitglieds über die Aufgabenzuweisung


Wenn Sie ein generisches Teammitglied durch Aufgabenzuweisung erstellen, erstellen Sie einen Platzhalter oder eine generische Ressource. Diese generische Ressource beschreibt die Merkmale der benannten Ressource, die letztendlich an der Aufgabe arbeiten soll. Anschließend generieren Sie eine Anforderung (oder übermittelnd eine Anforderung mithilfe der Anforderung), die zum Suchen und Buchen der genannten Ressource verwendet wird.

1. Wählen Sie im Zeitplanraster für eine Aufgabe das Ressourcen-Symbol in der **Ressourcenzelle** aus.
2. Geben Sie einen Namen als Namen für die Platzhalterressource ein. Zum Beispiel Projektleiter.
3. Wählen Sie **Erstellen** aus und legen Sie im Feld **Schnellerfassung: Projektteammitglied** die Rolle für die allgemeine Ressource fest.
4. Sie der Platzhalterressource bei Bedarf Aufgaben zuweisen, indem Sie die Ressource in der **Ressourcenauswahl** für die Aufgabe auswählen. Die unter **Teammitglieder** aufgelisteten Ressourcen.
5. Wenn Sie die allgemeine Ressource zugewiesen haben, wählen Sie die allgemeine Ressource auf der Registerkarte **Team** aus und wählen Sie dann **Anforderung erstellen**, um eine Ressourcenanforderung für die generische Ressource zu erstellen.
6. Wählen Sie **Buchen** für die allgemeine Ressource und verwenden Sie die Zeitplanübersicht, um eine echte Ressource zu suchen und zu buchen. Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden.
7. Wenn die generische Ressource mit einer benannten Ressource vollständig erfüllt ist (die teilweise Erfüllung der Ressourcenanforderungen führt nicht zu einer Ressourcenzuweisung), wird die generische Ressource aus dem Team entfernt. Die Aufgabenzuweisungen für die allgemeine Ressource werden der benannten Ressource zugewiesen, die die Ressourcenanforderungen der allgemeinen Ressource erfüllt.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Zuweisen einer benannten Ressource aus der Liste aller buchbaren Ressourcen

Sie können das Suchfeld in der **Ressourcenauswahl** verwenden, um alle aktiven buchbaren Ressourcen zu durchsuchen und einer beliebigen Blattknotenaufgabe zuzuweisen. Auf diese Weise zugewiesene Ressourcen werden dem Team ohne Buchungen hinzugefügt. Dies ist dem Hinzufügen eines Teammitglieds und dem Auswählen von **Keine** als Zuweisungsmethode ähnlich. Die Ressource wird auf den Registerkarten **Team**, **Ressourcenzuweisung** und **Abstimmung** als Ressource mit nur Zuweisungen und einem Buchungsdefizit angezeigt. Buchen Sie sie, wenn Sie die Verfügbarkeit verwenden möchten.

1. Navigieren Sie im Aufgabenraster, der Übersicht oder der Zeitskala zur **Zugewiesen zu**-Zelle.
2. Geben Sie im Suchfeld einen Namen ein. Die Suchergebnisse für den Namen werden in die **Ressourcenauswahl** unter **Weitere Ressourcen** angezeigt.
3. Wählen Sie die Ressource aus, die Sie der Aufgabe zuweisen möchten, oder wählen Sie den Ressourcennamen unter **Andere Teamressourcen**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]