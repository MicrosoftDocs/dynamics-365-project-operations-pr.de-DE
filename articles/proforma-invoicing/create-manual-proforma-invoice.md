---
title: Proforma-Rechnungen
description: Dieses Thema enthält Informationen zu Proforma-Rechnungen in Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2050a313fe530065341410d60801b13eb958cb32ae24eb4a0a71ab7ea5061881
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995625"
---
# <a name="proforma-invoices"></a>Proforma-Rechnungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Proforma-Rechnungen sind hilfreich, da sie Projekt-Managern eine zweite Genehmigungsstufe bietet, bevor sie Rechnungen für Kunden erstellen. Die erste Genehmigungsstufe ist abgeschlossen, wenn die von den Projektteammitgliedern eingereichten Zeit-, Ausgaben- und Materialeinträge genehmigt wurden. Bestätigte Proforma-Rechnungen sind im Projektbuchhaltungsmodul von Project Operations verfügbar. Projektbuchhalter können zusätzliche Aktualisierungen wie Umsatzsteuer, Buchhaltung und Rechnungslayout durchführen.


## <a name="creating-project-invoices"></a>Erstellen von Projektrechnungen

Projektrechnungen können einzeln oder mithilfe von Massendatensätzen erstellt werden. Sie können sie manuell erstellen oder so konfigurieren, dass sie in automatisierten Ausführungen generiert werden.

### <a name="manually-create-project-invoices"></a>Projektrechnungen manuell erstellen 

Auf der Listenseite **Projektverträge** können Sie Projektrechnungen für jeden Projektvertrag separat erstellen, Sie können jedoch auch Rechnungen für mehrere Projektverträge in einem Massenvorgang erstellen.

Befolgen Sie diesen Schritt, um eine Rechnung für einen bestimmten Projektvertrag zu erstellen.

- Öffnen Sie auf der Listenseite **Projektverträge** einen Projektvertrag, und klicken Sie dann auf **Rechnung erstellen**.

    Es wird eine Rechnung für alle Transaktionen des ausgewählten Projektvertrags generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Ausgaben, Materialien, Meilensteine und andere nicht abgerechnete Verkaufsjournalzeilen.

Befolgen Sie diese Schritte, um Rechnungen in einem Massenvorgang zu erstellen.

1. Wählen Sie auf der Listenseite **Projektverträge** einen oder mehrere Projektverträge aus, für den bzw. die Sie eine Rechnung erstellen müssen, und wählen Sie dann **Projektrechnungen erstellen** aus.

    Eine Warnmeldung informiert Sie darüber, dass es zu Verzögerungen kommen kann, bevor Rechnungen erstellt werden. Der Vorgang wird ebenfalls angezeigt.

2. Wählen Sie **OK** aus, um das Nachrichtenfeld zu schließen.

    Es wird eine Rechnung für alle Transaktionen einer Vertragszeile generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Ausgaben, Materialien, Meilensteine und andere nicht abgerechnete Verkaufsjournalzeilen.

3. Um die generierten Rechnungen anzuzeigen, wechseln Sie zu **Vertrieb** \> **Fakturierung** \> **Rechnungen**. Sie sehen eine Rechnung für jeden Projektvertrag.

### <a name="set-up-automated-creation-of-project-invoices"></a>Einrichten der automatischen Erstellung von Projektrechnungen 

Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf zu konfigurieren.

1. Gehen Sie zu **Einstellungen** \> **Batch-Auftrag**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Vorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss den Wortlaut „Rechnungen erstellen“ enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz suchen** werden drei Workflows angezeigt:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld die Option **OK** aus. Auf den Workflow **Ruhezustand** folgt der Workflow **Verarbeiten**.

    Sie können auch **ProcessRunner** in Schritt 5 auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt. Es durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen. Um die Vertragszeilen zu bestimmen, für die Rechnungen erstellt werden müssen, überprüft der Auftrag die Rechnungslaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungslaufdatum haben, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Auftrag die Rechnungserstellung.

Nach dem **ProcessRunner** durchgeführt wurde, wird **ProcessRunCaller** aufgerufen, liefert die Endzeit und ist geschlossen. **ProcessRunCaller** startet dann einen Timer, der ab der angegebenen Endzeit 24 Stunden lang läuft. Am Ende des Timers ist **ProcessRunCaller** geschlossen.

Der Batchverarbeitungsauftrag zum Erstellen von Rechnungen ist ein wiederkehrender Auftrag. Wenn dieser Batchauftrag mehrmals ausgeführt wird, werden mehrere Instanzen des Auftrags erstellt und verursachen Fehler. Deshalb sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Gleiches gilt für eine projektbasierte Vertragszeile.      
 
### <a name="edit-a-draft-invoice"></a>Bearbeiten eines Rechnungsentwurfs

Wenn Sie einen Projektrechnungsentwurf erstellen, werden sämtliche nicht fakturierten Verkaufstransaktionen, die bei der Genehmigung der Zeit-, Ausgaben- und Materialverbrauchseinträge erstellt wurden, in die Rechnung aufgenommen. Sie können die folgenden Anpassungen vornehmen, solange sich die Rechnung noch im Entwurfsstadium befindet:

- Rechnungspositionsdetails löschen oder bearbeiten.
- Menge und Fakturierungstyp bearbeiten und anpassen.

Wählen Sie **Bestätigen** aus, um eine Rechnung zu bestätigen. Die Aktion „Bestätigen“ ist eine unidirektionale Aktion. Wenn Sie **Bestätigen** auswählen, generiert das System eine schreibgeschützte Rechnung und erstellt zudem für jede Rechnungszeile abgerechnete vertriebliche Ist-Werte aus jedem Rechnungspositionsdetail. Wenn das Rechnungspositionsdetail auf einen nicht fakturierten vertrieblichen Ist-Wert verweist, kehrt das System auch den nicht fakturierten vertrieblichen Ist-Wert um. (Sämtliche Rechnungspositionsdetails, die aus einem Zeit- oder Ausgabeneintrag erstellt wurden, verweisen auf einen nicht fakturierten vertrieblichen Ist-Wert.) Allgemeine Hauptbuchintegrationssysteme können sich diese Umkehrung zunutze machen, um laufende Projektarbeit (WIP, Work In Progress) für Buchhaltungszwecke umzukehren.

### <a name="correct-a-confirmed-invoice"></a>Korrigieren einer bestätigten Rechnung

Bestätigte Rechnungen können bearbeitet (korrigiert) werden. Wenn Sie eine bestätigte Rechnung korrigieren, wird ein neuer Korrekturrechnungsentwurf erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese Korrekturrechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.

Transaktionen, die keine Korrektur benötigen, können aus dem Korrekturrechnungsentwurf entfernt werden. Wenn Sie nur eine Teilmenge umkehren oder zurückgeben möchten, können Sie das Feld **Menge** im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile storniert und zwei neue Ist-Werte werden erstellt:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
