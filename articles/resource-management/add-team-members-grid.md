---
title: Teammitglieder aus dem Teammitgliedsraster hinzufügen
description: In diesem Thema finden Sie Informationen dazu, wie Sie Teammitglied-Ressourcen verwalten.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cacf3913c3893dd09509cd02361c4a21bed59825
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280082"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Teammitglieder aus dem Teammitgliedsraster hinzufügen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations enthält ein Ressource Manager-Dashboard, das eine visuelle Übersicht zur Ressourcennachfrage und -nutzung in der Organisation bereitstellt. Sie können die Diagramme im Dashboard verwenden, um die folgenden Informationen visuell darzustellen:

- **Ressourcennachfrage**: Das Diagramm **Aktive Ressourcenanfragen** zeigt Ressourcen an, die übermittelt wurden. Die Ressourcen werden entweder nach Rolle oder Projekt zusammengefasst.
- **Nicht gesendeter Ressourcenbedarf**: Das Diagramm **Nicht zugewiesener Ressourcenbedarf** zeigt alle Ressourcenanforderungen an, die nicht gesendet wurden. Mit diesem Diagramm können Ressourcen-Manager die Nachfrage anzeigen, die nicht fest ist und durch eine Ressourcenanforderung gesendet werden kann.
- **Fakturierbare Nutzung für die letzte Woche**: Das Diagramm – **Nutzung nach Rolle** zeigt den Prozentsatz der tatsächlich abrechenbaren Nutzung der Organisation nach Rolle im Vergleich zum Ziel an.

    > [!NOTE]
    > Um das Diagramm **Nutzung nach Rolle** verfügbar zu machen, erstellen Sie einen Auftrag, in dem der **UpdateRoleUtilizations**-Workflow ausgeführt wird. Dieser wiederholende Auftrag wird alle sieben Tage ausgeführt, um die fakturierbare Nutzung der sieben vorherigen Tage zu berechnen. Als Ergebnisse werden nach Rolle zusammengefasst.

## <a name="manage-project-team-members"></a>Projektteammitglieder verwalten

Projektmanager können das Ressourcen-Manager-Dashboard verwenden, um Ressourcen in Projekten zu verwalten. Beispielsweise können sie ein Teammitglied direkt einem Projekt hinzufügen oder ein Teammitglied buchen, um die Ressourcenanforderungen zu erfüllen, die von einer allgemeine Ressource aufgezeichnet wurden.

### <a name="add-a-team-member-directly-to-a-project"></a>Direktes Hinzufügen eines Teammitglieds zu einem Projekt

Um ein Teammitglied direkt einem Projekt hinzuzufügen, wählen Sie im Formular **Projekte**, auf der Registerkarte **Team** **Neu** aus. Das Dialogfeld **Quick Create:Projektteammitglied** wird angezeigt. In diesem Dialogfeld können Sie die folgenden Aufgaben ausführen:

- **Eine benannte Ressource buchen**: Wählen Sie im Feld **Buchbare Ressource** den Namen der Ressource aus. Wählen Sie die Rolle aus, legen Sie den Zeitraum fest und wählen Sie eine Zuordnungsmethode aus. Die die ausgewählte benannte Ressource wird zum Projekt hinzufügt, indem Sie die ausgewählte Zuordnungsmethode und den Ressourcenkalender verwenden.
- **Eine allgemeine Ressource hinzufügen**: Lassen Sie das Feld **Buchbare Ressource** leer, und wählen Sie die Rolle aus, legen Sie den Zeitraum fest und wählen Sie die bevorzugte Zuordnungsmethode aus. Eine generische Ressource wird dem Team als Platzhalter hinzugefügt. Der Platzhalter enthält das Nachfragemuster, mit dem benannte Ressourcen im Team gebucht werden. Die Anforderung wird gemäß dem Projektkalender gemacht.
- **Eine benannte Ressource zum Team hinzufügen, ohne Ressourcenkapazität zu nutzen**: Wählen Sie im Feld **Buchbare Ressource** eine Ressource aus. Wählen Sie den Zeitraum und dann **Keine** als Zuordnungsmethode aus. Die Ressource wird dem Team hinzugefügt, aber die Kapazität der Ressource wird von einer Buchung genutzt.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Buchen Sie ein Teammitglied, um Ressourcenanforderungen für eine allgemeine Ressource zu erfüllen

In Project Operations können Sie eine allgemeine Ressource für ein Projektteam buchen. Sie können auch die Rolle, die erforderliche Kapazität und die Verteilung dieser Kapazität angeben. Für die Ressourcenanforderung können Sie Attribute angeben, die der generischen Ressource zugeordnet sind. Diese Attribute enthalten erforderliche Qualifikationen, die bevorzugte Organisationseinheit und bevorzugte Ressourcen.

Führen Sie die folgenden Schritte aus, um die Fähigkeiten einer allgemeinen Ressource für einen Entwickler anzugeben.

1. Wählen Sie im Formular **Projekte** auf der Registerkarte **Team** **Neu** aus, um eine generische Ressource zu buchen.
2. Wählen Sie in der Ansicht **Alle Teammitglieder** in der Spalte **Ressourcenanforderung** den Link aus, um die Fähigkeiten für die allgemeine Ressource hinzufügen.
3. Im Formular **Ressourcenanforderung** im Raster **Qualifikationen** wählen Sie die Auslassungspunkte (**...**) und dann **Neues Anforderungsmerkmal hinzufügen** aus, um die erforderlichen Fähigkeiten für den Entwickler hinzuzufügen.
4. Wählen Sie im Dialogformular **Schnellerfassung: Anforderungsmerkmale**, das angezeigt wird, im Feld **Merkmal** die erforderliche Fähigkeit aus.
5. Wählen Sie im Feld **Bewertungswert** die Leistungsfähigkeitsebene für diese Fähigkeit aus. 
6. Legen Sie im Feld **Ressourcenanforderung** die Anforderungen von Organisationseinheiten oder sogar benannten Ressourcen auf Quellressourcen fest. Wenn Sie fertig sind, wählen Sie **Speichern** aus.
7. Wählen Sie im Formular **Ressourcenanforderung** die Option **Buchen** aus, um die Ressourcenanforderung zu erfüllen. Sie können die allgemeine Ressource auch im Raster **Alle Teammitglieder** auswählen und dann **Buchen** auswählen.

    > [!NOTE]
    > In diesem Beispiel gibt es 40 erforderliche Stunden aber keine tatsächlich aufgezeichnete Stunden, da keine allgemeinen Ressourcen über Buchungen verfügen. Darüber hinaus gibt keine zugewiesenen Stunden, da die allgemeine Ressource direkt dem Team hinzugefügt wurde, statt die Aufgabenzuweisung zum Hinzufügen zu verwenden.

    Im Formular **Planungs-Assistent** können Sie die verfügbaren Ressourcen nach Anforderungen filtern, die für Ressourcenanforderungen angegeben wurden. Ressourcen werden nach den Sortierungsparametern sortiert, die auf der Zeitplan-Karte angegeben wurden.

   Einige der am häufigsten verwendeten Filter sind:

    - **Merkmale zusammen mit einer Bewertung**: Filtern Sie nach Fähigkeiten, Zertifizierungen und anderen Ressourcenqualitäten neben den Bewertungen der Leistungsfähigkeit.
    - **Rollen**: Filtern Sie nach Standardrollen, die buchbaren Ressourcen zugewiesen sind.
    - **Organisationseinheiten**: Filtern Sie buchbare Ressourcen nach Organisationseinheiten, denen sie zugewiesen sind.

8. Wenn Sie mit den Ergebnissen der Suche nach der ursprünglichen Anforderung nicht zufrieden sind, können Sie die Filterkriterien ändern. Erweitern Sie den Bereich auf der linken Seite **Filteransicht**, und wählen Sie dann **Suchen** aus, um nach weiteren Ressourcen zu suchen. Wählen Sie zum Ändern der Ergebnissortierung **Sortieren** aus.
9. Wählen Sie die Ressourcen nach Bedarf aus, der in der Anforderung angegebenen ist, wie oben im Raster angezeigt. Sie können die Auswahl der Zellen im Raster löschen und die Ressourcenkapazität offen lassen. Es kann nur eine Ressource als gebucht gleichzeitig ausgewählt werden.
10. Wählen Sie **Buchen** aus, um die ausgewählten Ressource zu buchen und die Zeitplan-Karte offen zu lassen, sodass Sie weitere Ressourcen auswählen können. Alternativ wählen Sie die Option **Buchen und beenden**, um die ausgewählte Ressource zu buchen und die Zeitplan-Karte zu schließen.
11. Wechseln Sie zur Ansicht **Alle Teammitglieder** zurück. Beachten Sie im Raster, dass die allgemeine Ressource durch die benannte Ressource ersetzt wurde, und 40 Stunden werden als für die Ressource gebucht angezeigt.

    > [!NOTE]
    > Es werden keine zugeteilten Stunden angezeigt, da diese direkt im Team aufgezeichnet wurden. Sie wurden nicht mit der Aufgabenzuordnung aufgezeichnet.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Weisen Sie allgemeine Ressourcen zu den Aufgaben zu und erstellen Sie Ressourcenanforderungen

In Project Operations können Sie Aufgaben erstellen und anschließend zu allgemeinen Ressourcen zuweisen. Der Ressourcenbedarf kann dann durch Platzhalter dargestellt werden, während Sie Ihren Zeitplan und die wirtschaftlichen Zahlen schätzen. Sie können für allgemeine Ressourcenanforderungen Ressourcen generieren und erfüllen.

1. Wählen Sie im Formular **Projekte** auf der Registerkarte **Zeitplan** **Hinzufügen** aus, um eine Aufgabe zu erstellen.
2. Wählen Sie im Feld **Ressourcen** das Symbol **Ressourcenauswahl** aus. Die Ressourcenauswahl wird mit vorhandenen Teammitgliedern für das Projekt angezeigt.
3. Geben Sie den Namen der neuen generischen Ressource ein, und wählen Sie dann **Erstellen** aus.
4. Wählen Sie im Dialogfeld **Schnellerfassung: Projektteammitglied** im Feld **Rolle** die Rolle für die allgemeine Ressource aus. 
5. Wählen Sie im Feld **Ressourcenzuordnungseinheit** die Organisationseinheit für die allgemeine Zustand Ressource aus. Wählen Sie dann **Speichern** aus. Das allgemeine Teammitglied ist nun der Aufgabe zugewiesen.

   Auf der Registerkarte **Team** finden Sie neue das allgemeine Teammitglied. Beachten Sie, dass nur Stunden zugewiesen sind. Diese Stunden umfassen die Summe aller Aufgaben, die dem generischen Teammitglied zugewiesen werden. Das allgemeine Teammitglied hat keine erforderlichen Stunden oder eine Ressourcenanforderung.

6. Sie können das allgemeine Teammitglied jetzt anderen Aufgaben zuweisen, indem Sie die Ressourcenauswahl verwenden.

   Wenn Sie fertig mit der Zuweisung der allgemeinen Ressource zu Aufgaben fertig sind, können Sie eine Ressourcenanforderungen für die allgemeine Ressource erstellen.

7. Wählen Sie auf der Registerkarte **Team** die allgemeine Ressource aus, und wählen Sie dann **Anforderung generieren** aus. Wenn die Anforderung generiert wurde, besitzt das allgemeine Teammitglied erforderliche Stunden und einen Link für die Ressourcenanforderung.

  Wenn Sie eine benannte Ressource gebucht haben, wird die allgemeine Ressource aus dem Team entfernt und durch die benannte Ressource ersetzt. Auf der Registerkarte **Zeitplan** werden die allgemeinen Ressourcen-Zuweisungen entfernt und durch benannte Ressourcen ersetzt.

  > [!NOTE]
  > Dieses Verhalten tritt auf, wenn eine Ressource vollständig für die generische Ressourcenanforderung aufgezeichnet wird. Wenn eine Ressource eine generische Ressourcenanforderung entweder teilweise ersetzt oder mehrere benannte Ressourcen die generische Ressourcenanforderung ersetzen, verbleibt die allgemeine Ressourcen der Aufgabe zugewiesen.

Project Operations weist die beiden Ressourcen nicht der Aufgabe zu, da dieses Verhalten einen weniger vorhersagbaren Zeitplan erzeugen würde. In diesem Beispiel ist es einfacher, die Stunden gleichmäßig zwischen zwei Ressourcen aufzuteilen. In komplexeren Szenarien mit mehreren Aufgaben und mehrere Ressourcen, muss PSA Annahmen machen, wie die Buchungen zugeordnet werden sollen, die für mehrere Ressourcen für mehrere Aufgaben empfangen werden.

Daher ist in den Szenarien der Projektmanager für die Analyse und Zuweisung der Buchungen verantwortlich. Um die Buchungen zuzuordnen, weist der Projektmanager die Aufgaben von den generischen Ressourcen zu den benannten Ressourcen zu und verwendet anschließend die Ansicht **Abstimmung**, um sicherzustellen, dass die Zuordnung mit den Buchungen funktioniert.

### <a name="edit-a-resource-requirement"></a>Ressourcenanforderung bearbeiten

Wenn eine Ressourcenanforderung erstellt wurde, kann ein Projektmanager oder ein Ressourcenmanager die Details bearbeiten, um Suchkriterien zu verfeinern, wenn die Zeitplan-Karte verwendet wird. Um die Ressourcenanforderungen zu bearbeiten, führen Sie die folgenden Schritte aus.

1. Wählen Sie im Formular **Projekte** auf der Registerkarte **Team** den Link zu einer Anforderung für eine generische Ressource aus.
2. Geben Sie im angezeigten Formular **Ressourcenbedarf** die erforderlichen Feldinformationen ein

   Im Formular **Ressourcenbedarf** kann der Projektmanager oder der Ressourcenmanager auch Qualifikationen, Rollen, Ressourceneinstellungen und die bevorzugte Organisationseinheit definieren.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Aktualisieren der Ressourcenbuchungen, wenn sie in einem Projekt gebucht sind

Wenn Sie eine generische oder benannte Ressource einem Projektteam hinzugefügt haben, können Sie die Buchungen der Ressource ändern.

1. Wählen Sie im Formular **Projekte** auf der Registerkarte **Team** Neu ein Teammitglied aus und dann **Buchungen verwalten**.
 
   Die Zeitplanübersicht wird mit den Projektteammitgliedsbuchungen angezeigt. Erweitern Sie den Datensatz des Teammitglieds, um die Stunden anzuzeigen, die für das Projekt und andere Projekte aufgezeichnet wurden, die die Kapazität des Teammitglieds nutzen.

2. Wählen und ziehen Sie die Buchung, um sie zu erweitern oder zu verkürzen. Ein Dialogfeld **Ressourcenbuchung erstellen** wird angezeigt, in dem Sie die Buchung ändern können.
3. Klicken Sie mit der rechten Maustaste auf Buchung. Sie können das Verknüpfungsmenü verwenden, um die folgenden Aktionen auszuführen:

    - Buchungsstatus ändern
    - Buchung bearbeiten
    - Eine Ressource im Projektteam ersetzen

### <a name="change-the-booking-status"></a>Buchungsstatus ändern

Sie können den Status jeder Standard- oder benutzerdefinierten Buchung ändern.

Die folgenden Status sind in Project Operations enthalten:

- **Storniert**: Bricht die Buchung einer Ressource ab und gibt die Kapazität der Ressource frei.
- **Verbindliche Buchungen**: Verbraucht die Kapazität einer Ressource. Normalerweise hat eine Buchung diesen Status, wenn Sie **Buchungen verwalten** im Raster **Alle Teammitglieder** im Formular **Projekte** öffnen.
- **Unverbindlich buchen**: Fügt eine Ressource einem Team hinzu, verbraucht jedoch keine Kapazität der Ressource. Dieser Status wird angegeben, dass die Ressource für potenzielle Arbeit reserviert wurde, aber noch über Kapazität verfügt, wenn sie für andere Aufträge erforderlich ist. In der Ansicht der allgemeinen Ressourcenverfügbarkeit haben unverbindliche Buchungen einen anderen Status als verbindliche Buchungen.
- **Vorgeschlagen**: Stelle den Vorschlag eines Ressourcen-Managers oder Projekt-Managers für eine Ressource dar. Vorschläge verbrauchen keine Kapazität einer Ressource, und die Ressource ist nicht dem Projektteam hinzugefügt. Um die Ressource verbindlich im Team zu buchen, muss der Projektmanager den Vorschlag akzeptieren.

### <a name="submit-resource-requests"></a>Ressourcenanfragen übermitteln

Ressourcenanforderungen werden genutzt, um die Nachfrage oder Ressourcenanforderung zu transportieren, die vom Ressourcenmanager erfüllt werden. Für eine generische Ressource, die bereits im Team ist, können Sie eine Ressourcenanforderung direkt senden. Eine Ressourcenanforderung kann auf zwei Arten erfüllt werden:

- Der Ressourcenmanager erfüllt die Anforderung direkt. In diesem Fall wird die allgemeine Ressource durch eine verbindliche Buchung ersetzt, die eine benannte Ressource hat.
- Der Ressourcenmanager schlägt dem Projektmanager eine Ressource vor und der Projektmanager genehmigt die Ressource oder lehnt sie ab.

#### <a name="direct-fulfillment-of-resource-requests"></a>Direkte Erfüllung von Ressourcenanforderungen

Wenn eine Ressourcenanforderung erstellt wird, kann ein Projektmanager eine Ressourcenanforderung für eine allgemeine Ressource übermitteln, indem er die Ressource und dann **Übermittlungsanfrage** auswählt. Kommentare zur Ressource können dem Ressourcenmanager bereitgestellt werden, der die Anforderung erfüllt. Nachdem die Anforderung gesendet wurde, wird das Feld **Status** für das Teammitglied in **Gesendet** geändert. Wenn der Ressourcenmanager die Anforderung erfüllt, wird das allgemeine Teammitglied durch die benannte Ressource im Raster **Alle Teammitglieder** ersetzt.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Verwenden Sie einen Ressourcenvorschlag für eine Ressourcenanforderung

Anstatt eine Ressource direkt für eine Ressourcenanforderung zu buchen, kann ein Ressourcenmanager dem Projektmanager eine Ressource vorschlagen. Ein Ressourcenmanager kann diese Option verwenden, wenn keine genaue Übereinstimmung für die Anforderung verfügbar ist. Wenn ein Ressourcenmanager eine Ressource vorschlägt, sieht der Projektmanager, dass das Feld **Status** für das allgemeine Teammitglied in **Prüfung erforderlich** geändert wird.

Sie können die vorgeschlagene Ressource zusammen mit einer Visualisierung der Auswirkungen der Buchung des Angebots anzeigen. 

1. Klicken Sie zweimal auf das Teammitglied mit dem Status **Muss überprüft werden**. 
2. Wählen Sie die Registerkarte **Vorgeschlagene Ressourcen** aus.
3. Wählen Sie **Alle Vorschläge akzeptieren** aus, um alle vorgeschlagenen Ressourcen zu akzeptieren, oder **Alle Vorschläge ablehnen**, um sie abzulehnen. Wenn Sie die vorgeschlagenen Ressourcen annehmen, werden diese im Projekt als verbindliche Teammitglieder gebucht und ersetzen die allgemeinen Ressourcen.

> [!NOTE]
> Sie müssen alle vorgeschlagenen Ressourcen entweder akzeptieren oder ablehnen. Sie können sie nicht teilweise akzeptieren oder ablehnen.

### <a name="substitute-a-resource-on-the-project-team"></a>Eine Ressource im Projektteam ersetzen

Gelegentlich muss ein Projektmanager ein gebuchtes Teammitglied in einem Projekt ersetzen.

1. Wählen Sie im Formular **Projekte** auf der Registerkarte **Team** die Ressource aus, die ersetzt werden muss, und wählen Sie dann **Buchungen verwalten**.
2. Erweitern Sie die Ressource, um die Projekte anzuzeigen, die ihr zugewiesen wurden.
3. Klicken Sie mit der rechten Maustaste auf das Projekt und wählen Sie dann **Ersatzressource** aus.
4. Wenn Sie wissen, durch welche Ressource die aktuelle Ressource ersetzt werden soll, wählen Sie den Namen aus oder geben ihn ein und wählen dann **Neu zuweisen** aus.

Oder. wenn Sie nach einer Ressource suchen müssen, führen Sie die folgenden Schritte aus.

1. Wählen Sie **Ersatz suchen** aus.

   Der Zeitplan-Assistent gibt eine Liste aller verfügbaren Ersätzen zurück. Im Zeitplan-Assistenten können Sie die verfügbaren Ressourcen weiter filtern, um einen passenden Ersatz zu suchen.

2. Um die Ressource zu ersetzen, wählen Sie die gewünschte Ressource und dann **Ersatz** aus.   

   Die Buchungen und Zuweisungen werden durch die neue Ressource ersetzt.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Abgleichen der Teammitgliedsbuchungen und -zuweisungen

Teammitglieder werden für Buchungen und Zuweisungen lose verbunden. Das bedeutet, Ressourcen können Zuweisungen haben, jedoch keine Buchungen, oder sie können Buchungen, jedoch keine Zuweisungen haben. Idealerweise sollten Buchungen und Zuweisungen angepasst werden, sodass die Ressourcen ihre Kapazität für die Aufgabenzuordnungen festgelegt haben. Unter Umständen basieren die Buchungen auf der Verfügbarkeit, und die Aufgabenzeitplanung wird im Laufe des Projekts geändert. Daher bietet die lose Verbindung von Buchungen und Zuweisungen Flexibilität.

Project Operations hat eine Registerkarte **Abstimmung**, die es dem Projektmanager ermöglicht, die Buchungen und Zuweisungen der Teammitglieder für die Projektteams abzustimmen.

Auf der Registerkarte **Abstimmung** werden Buchungen und Zuweisungen bis zu Ebene der einzelnen Aufgabenzuordnungen für jedes Teammitglied angezeigt. Sie zeigt Stunden in Zellen an, was für Zeitperioden von Monaten bis Tagen stehen kann.

Auf der Registerkarte wird auch die allgemeine Nettosumme für das Projekt zusammen mit einer der Spalte der Gesamtsumme angezeigt.

Für jede Ressource berechnet die Registerkarte den Unterschied zwischen den Buchungen des Teammitglieds und einem Rollup der Aufgabenzuordnungen des Teammitglieds. Idealerweise sollte der Unterschied 0 (null) sein. Das bedeutet, dass es keinen Unterschied zwischen Buchungen und Zuweisungen geben sollte. Die Unterschiede werden farbig und schattiert angezeigt, um auf zwei Bedingungen hinzuweisen:

- **Verlust der Buchung**: Tritt auf, wenn eine Ressource mehr Zuweisungen als Buchungen hat. Da diese Kapazität nicht reserviert wurde, kann ein Projektmanager diesen Zustand korrigieren, indem er die Ressourcenbuchungen erweitert, um das Defizit abzudecken.
- **Überzählige Buchungen**: Treten auf, wenn eine Ressource für das Projekt zwar gebucht, aber keinen Aufgaben zugewiesen wurde. Diese Bedingung kann in den Fällen akzeptabel sein, in denen die Ressource vor der Aufgabenzuordnung für das Projekt gebucht wurde. In anderen Fällen wird die Ressource jedoch nicht eingeplant, um Aufgaben zugewiesen zu werden. In diesen Fällen sollte es der Projektmanager in Betracht ziehen, die Buchungen der Ressource zu stornieren, sodass die Kapazität für ein anderes Projekt verwendet werden kann.

Wenn Sie die Zeit in einigen Fällen auf einer höheren als der Tagsebene (z. B. auf Monatsebene) anzeigen, sehen Sie einen Nettounterschied von null für eine Ressource. Mit anderen Worten, Buchungen = Aufgaben. Wenn Sie die Zeit jedoch auf Wochenebene anzeigen, sehen Sie, dass es Zuweisungen mit null Stunden und Buchungen mit 40 Stunden in der ersten Woche gibt, aber Zuweisungen von 40 Stunden und Buchungen von null Stunden in der zweiten Woche. Die Buchungen und Zuweisungen werden insgesamt abgestimmt, sie unterscheiden sich jedoch von einer Woche zur nächsten.

Wenn Sie Zeit auf höheren Ebenen anzeigen, haben die Zellen auf der Registerkarte **Abstimmung** einen Indikator, um Sie darüber zu informieren, dass es Unterschiede auf tieferen Ebenen gibt. Doppelklicken Sie zweimal in einer Zelle, um die Ansicht zu vergrößern, um die Unterschiede anzuzeigen. Sie können dann mit der rechten Maustaste klicken, um die Ansicht wieder zu verkleinern. Sie können eine Ressource und dann das **Nächster Unterschied**-Steuerelement auf der Rastersymbolleiste auswählen, um zu den folgenden Unterschieden zwischen Buchungen und Zuweisungen für die Ressource wechseln. Wählen Sie **Vorheriger Unterschied** aus, um zurückkehren. Sie können den Unterschiedindikator und das Navigationsverhalten unter **Einstellungen** deaktivieren.

Wenn Sie Aufgabenzuordnungen für eine Ressource, jedoch keine Buchungen haben, wählen Sie im Formular **Projekte**, auf der Registerkarte **Abstimmung** den Buchungsverlust aus, und wählen Sie dann **Buchung erweitern** aus. Das Dialogfeld **Buchung erweitern** wird mit der Buchung angezeigt, die benötigt wird, um einen Ressourcenmangel zu beheben. Das Dialogfeld enthält außerdem die vorhandenen Buchungen der Ressource in allen Projekten oder anderen planbaren Entitäten. Wenn Sie **OK** auswählen, um die Buchung für die Ressource zu erstellen, entsteht ungeachtet der Verfügbarkeit der Ressource möglicherweise eine Überbuchung.

Der Projektmanager oder der Ressourcenmanager kann dann die Zeitplanübersicht verwenden, um alle Situationen zu verwalten, in denen eine Ressource über die Kapazität überbucht wird.


[!INCLUDE[footer-include](../includes/footer-banner.md)]