---
title: Ressourcenzuweisungen erstellen
description: In diesem Artikel erfahren Sie, wie Sie allgemeine und benannte Ressourcenzuweisungen erstellen.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811992"
---
# <a name="create-resource-assignments"></a>Ressourcenzuweisungen erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Eine Ressourcenzuweisung ist die direkte Zuordnung eines Projektteammitglieds zu einer Blattknotenaufgabe. Dieser Artikel informiert Sie über die verschiedenen Möglichkeiten der Ressourcenzuweisung.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Erstellen eines generischen Teammitglieds über die Aufgabenzuweisung


Wenn Sie ein generisches Teammitglied durch Aufgabenzuweisung erstellen, erstellen Sie einen Platzhalter oder eine generische Ressource. Diese generische Ressource beschreibt die Merkmale der benannten Ressource, die letztendlich an der Aufgabe arbeiten soll. Anschließend generieren Sie eine Anforderung (oder übermittelnd eine Anforderung mithilfe der Anforderung), die zum Suchen und Buchen der genannten Ressource verwendet wird.

1. Wählen Sie im Zeitplanraster für eine Aufgabe das Ressourcen-Symbol in der **Ressourcenzelle** aus.
2. Geben Sie einen Namen als Namen für die Platzhalterressource ein. Zum Beispiel Projektleiter.
3. Wählen Sie **Erstellen** aus und legen Sie im Feld **Schnellerfassung: Projektteammitglied** die Rolle für die allgemeine Ressource fest.
4. Sie der Platzhalterressource bei Bedarf Aufgaben zuweisen, indem Sie die Ressource in der **Ressourcenauswahl** für die Aufgabe auswählen. Die unter **Teammitglieder** aufgelisteten Ressourcen.
5. Wenn Sie die allgemeine Ressource zugewiesen haben, wählen Sie die allgemeine Ressource auf der Registerkarte **Team** aus und wählen Sie dann **Anforderung erstellen**, um eine Ressourcenanforderung für die generische Ressource zu erstellen.
6. Wählen Sie **Buchen** für die allgemeine Ressource und verwenden Sie die Zeitplanübersicht, um eine echte Ressource zu suchen und zu buchen. Sie können die Anfrage für die Erfüllung von einem Ressourcen-Manager auch senden.
7. Wenn die generische Ressource mit einer benannten Ressource vollständig ausgeführt wurde, wird die generische Ressource aus dem Team entfernt. (Die teilweise Erfüllung der Ressourcenanforderungen führt nicht zu einer Ressourcenzuweisung). Die Aufgabenzuweisungen für die generische Ressource werden den benannten Ressource zugewiesen, die die Ressourcenanforderung der generischen Ressource erfüllt hat.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Zuweisen einer benannten Ressource aus der Liste aller buchbaren Ressourcen

Sie können das Suchfeld in der **Ressourcenauswahl** verwenden, um alle aktiven buchbaren Ressourcen zu durchsuchen und einer beliebigen Blattknotenaufgabe zuzuweisen. Auf diese Weise zugewiesene Ressourcen werden dem Team ohne Buchungen hinzugefügt. Dies ist dem Hinzufügen eines Teammitglieds und dem Auswählen von **Keine** als Zuweisungsmethode ähnlich. Die Ressource wird auf den Registerkarten **Team**, **Ressourcenzuweisung** und **Abstimmung** als Ressource mit nur Zuweisungen und einem Buchungsdefizit angezeigt. Buchen Sie sie, wenn Sie die Verfügbarkeit verwenden möchten.

1. Navigieren Sie im Aufgabenraster, der Übersicht oder der Zeitskala zur **Zugewiesen zu**-Zelle.
2. Geben Sie im Suchfeld einen Namen ein. Die Suchergebnisse für den Namen werden in die **Ressourcenauswahl** unter **Weitere Ressourcen** angezeigt.
3. Wählen Sie die Ressource aus, die Sie der Aufgabe zuweisen möchten, oder wählen Sie den Ressourcennamen unter **Andere Teamressourcen**.

## <a name="editing-resource-assignment-contours"></a>Bearbeiten der Konturen der Ressourcenzuweisung

Wenn Ressourcen einem Vorgang im Zeitplan zugewiesen werden, wird ihr Aufwand standardmäßig linear auf jede Ressource verteilt, basierend auf den Arbeitszeiten dieser Ressource und dem Zeitplanmodus des Projekts. Ein Projektmanager kann das Ressourcenzuweisungsraster verwenden, um die Aufwandsschätzungen jeder Ressource zu verfeinern, die einem oder mehreren Vorgängen über die verschiedenen Zeitskalen hinweg zugewiesen ist. Diese Funktion hilft Projektmanagern, genauere Kosten- und Umsatzschätzungen zu erstellen, die von den Ressourcenzuweisungskonturen gesteuert werden, die generiert werden, wenn eine Ressource einem Vorgang zugewiesen wird. Darüber hinaus können Projektmanager den Ressourcenbedarf, der zum Erstellen des Bedarfs erforderlich ist, leichter in einem Ressourcenbedarf widerspiegeln.

### <a name="navigation"></a>Navigation

Um auf das Konturbearbeitungsraster zuzugreifen, wählt der Projektmanager zuerst die Registerkarte **Aufgaben** auf der Projekthauptseite und dann die **Zuweisungen** Tab.

![Registerkarte „Zuweisungen“ auf der Registerkarte „Aufgaben“ der Projekt-Hauptseite.](media/AssignmentGrid.png)

Das Raster unterstützt zwei Gruppierungsmethoden: **Gruppieren nach Ressource** und **Gruppieren nach Aufgabe**. Anders als in der Rasteransicht sind Spalten nicht konfigurierbar. Die einzigen sichtbaren Spalten sind **Zugewiesen zu**, **Aufgabenname**, **Zuweisungsbeginn**, **Zuweisungsende**, und **Zuweisungsaufwand**.

Wenn das Gitter anfänglich gerendert wird, beginnt es bei der frühesten Zuweisungskontur. Wenn Ihr Zeitplan keine Aufgaben enthält, die Aufwand erfordern, ist das Raster leer und es wird nichts gerendert.

![Leeres Zuordnungsraster.](media/emptyassignmentgrid.png)

Wenn Sie Ihre Konturen und verschiedene Zeitskalen anzeigen möchten, stehen auch das schreibgeschützte Ressourcenzuweisungsraster und das Ressourcenabgleichsraster zur Verfügung.

### <a name="resource-calendars"></a>Ressourcenkalender

Die Fähigkeit, eine Kontur für einen bestimmten Tag zu bearbeiten, wird durch die Arbeitstage der Ressource geregelt, wie sie in ihrem Kalender widergespiegelt sind. Wenn eine Zelle für eine bestimmte Ressource deaktiviert ist, hat diese Ressource in diesem Zeitraum keine Arbeitstage.

Die Konturen einer Ressource können sich über die aktuellen Start- und Enddaten der zugewiesenen Aufgabe hinaus erstrecken. Wenn eine Kontur so aktualisiert wird, dass sie nach dem spätesten Enddatum einer Aufgabe oder dem frühesten Startdatum einer Aufgabe liegt, wird das End- oder Startdatum der Aufgabe entsprechend geändert. Wenn jedoch eine Kontur so aktualisiert wird, dass sie vor dem Startdatum einer Aufgabe liegt, die mit einem Vorgänger verknüpft ist, schlägt die Aktualisierung fehl, da die Zuweisung dazu führt, dass die Aufgabe gestartet wird, bevor ihr Vorgänger abgeschlossen ist, und dieses Verhalten ist derzeit nicht der Fall unterstützt.

### <a name="co-authoring"></a>Gemeinsame Dokumenterstellung

Änderungen am Ressourcenzuweisungsraster werden automatisch in allen zugehörigen Ansichten widergespiegelt, einschließlich der Diagramm-, Zeitachsen-, Tafel- und Rasteransichten. Wenn mehrere Benutzer das Projekt gleichzeitig überprüfen, werden alle Änderungen, die ein Benutzer vornimmt, im Raster widergespiegelt. Umgekehrt werden alle Änderungen, die im Ressourcenzuweisungsraster vorgenommen werden, allen anderen Benutzern angezeigt, die das Projekt in derselben Sitzung anzeigen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
