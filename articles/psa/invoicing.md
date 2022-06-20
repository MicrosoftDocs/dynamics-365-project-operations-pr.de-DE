---
title: Rechnungsstellung in Project Service Automation
description: Dieser Artikel enthält Informationen über die Rechnungsstellung.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fa036dda6514449b04e1416bde2cd9c21fc558b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926821"
---
# <a name="invoicing-in-project-service-automation"></a>Rechnungsstellung in Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die Rechnungstellung in Dynamics 365 Project Service Automation ist hilfreich, da sie Projekt-Managern eine zweite Genehmigungsstufe bietet, bevor sie Rechnungen für Kunden erstellen. Die erste Genehmigungsstufe ist abgeschlossen, wenn die von den Projektteammitgliedern eingereichten Zeit- und Kosteneinträge genehmigt wurden.

PSA ist aus folgenden Gründen nicht für die Erstellung von Kundenrechnungen konzipiert:

- Es sind keine Steuerinformationen enthalten.
- Es können keine anderen Währungen mit korrekt konfigurierten Wechselkursen in die Rechnungswährung konvertiert werden.
- Rechnungen können nicht korrekt für den Druck formatiert werden.

Stattdessen können Sie ein Finanz- oder Buchhaltungssystem verwenden, um Kundenrechnungen zu erstellen, die die Informationen aus Rechnungsvorschlägen verwenden, die in PSA generiert wurden.

## <a name="creating-project-invoices-in-psa"></a>Erstellen von Projektrechnungen in PSA

Projektrechnungen können einzeln oder mithilfe von Massendatensätzen erstellt werden. Sie können manuell erstellt oder so konfiguriert werden, dass sie in automatisierten Abläufen generiert werden.

### <a name="manually-create-project-invoices-in-psa"></a>Manuelles Erstellen von Projektrechnungen in PSA

Auf der Listenseite **Projektverträge** können Sie Projektrechnungen für jeden Projektvertrag separat erstellen, Sie können jedoch auch Rechnungen für mehrere Projektverträge in einem Massenvorgang erstellen.

Befolgen Sie diesen Schritt, um eine Rechnung für einen bestimmten Projektvertrag zu erstellen.

- Öffnen Sie auf der Listenseite **Projektverträge** einen Projektvertrag und wählen Sie dann **Rechnung erstellen** aus.

    ![Erstellen von Projektrechnungen für einen bestimmten Projektvertrag.](media/CreateProjectInvoicesOneByOne.png)

    Für alle Transaktionen des ausgewählten Projektvertrags mit dem Status **Bereit für die Rechnungsstellung** wird eine Rechnung erstellt. Diese Transaktionen umfassen Zeit, Spesen, Meilensteine und produktbasierte Vertragszeilen.

Führen Sie die folgenden Schritte aus, um Rechnungen in großen Mengen zu erstellen.

1. Wählen Sie über die Listenseite **Projektverträge** einen oder mehrere Projektverträge aus, für die Sie eine Rechnung erstellen müssen, und klicken Sie dann auf **Projektrechnungen erstellen**.

    ![Erstellen von Projektrechnungen mithilfe von Massendatensätzen.](media/CreateProjectInvoicesBulk.png)

    Eine Warnmeldung informiert Sie darüber, dass es zu Verzögerungen kommen kann, bevor Rechnungen erstellt werden. Der Vorgang wird ebenfalls angezeigt.

2. Wählen Sie **OK** aus, um das Nachrichtenfeld zu schließen.

    Für alle Transaktionen auf einer Vertragszeile mit dem Status **Bereit für die Rechnungsstellung** wird eine Rechnung erstellt. Diese Transaktionen umfassen Zeit, Ausgaben und Meilensteine sowie produktbasierte Vertragszeilen.

3. Um die generierten Rechnungen anzuzeigen, wechseln Sie zu **Vertrieb** \> **Fakturierung** \> **Rechnungen**. Sie sehen eine Rechnung für jeden Projektvertrag.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Einrichten der automatischen Erstellung von Projektrechnungen in PSA

Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf in PSA zu konfigurieren.

1. Wechseln Sie zu **Project Service** \> **Einstellungen** \> **Batchaufträge**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **PSA Rechnungen erstellen**. Der Name des Batchauftrags muss den Wortlaut „Rechnungen erstellen“ enthalten.
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
> Die Stapelrechnungsstellung in Project Service Automation wird nur für Projektvertragspositionen ausgeführt, die über Rechnungszeitpläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Informationen zum Festlegen der Häufigkeit der Rechnungsstellung im Rahmen eines Projekts, das auf einer Angebotszeile basiert, finden Sie in dem Artikel [Angebote und Angebotszeilen](basic-quote-lines.md#invoice-schedule). Gleiches gilt für eine projektbasierte Vertragszeile.      
 
### <a name="edit-a-draft-psa-invoice"></a>Bearbeiten eines PSA-Rechnungsentwurfs

Wenn Sie einen Projektrechnungsentwurf erstellen, werden sämtliche nicht fakturierten Verkaufstransaktionen, die bei der Genehmigung der Zeit- und Ausgabeneinträge erstellt wurden, in die Rechnung aufgenommen. Sie können die folgenden Anpassungen vornehmen, solange sich die Rechnung noch im Entwurfsstadium befindet:

- Rechnungspositionsdetails löschen oder bearbeiten.
- Menge und Fakturierungstyp bearbeiten und anpassen.
- Zeit, Ausgaben und Gebühren als Transaktionen direkt der Rechnung hinzufügen. Sie können diese Funktion verwenden, wenn die Rechnungszeile einer Vertragszeile zugeordnet ist, die diese Transaktionsklassen zulässt.

Wählen Sie **Bestätigen** aus, um eine Rechnung zu bestätigen. Die Aktion „Bestätigen“ ist eine unidirektionale Aktion. Wenn Sie **Bestätigen** auswählen, generiert das System eine schreibgeschützte Rechnung und erstellt zudem für jede Rechnungszeile abgerechnete vertriebliche Ist-Werte aus jedem Rechnungspositionsdetail. Wenn das Rechnungspositionsdetail auf einen nicht fakturierten vertrieblichen Ist-Wert verweist, kehrt das System auch den nicht fakturierten vertrieblichen Ist-Wert um. (Sämtliche Rechnungspositionsdetails, die aus einem Zeit- oder Ausgabeneintrag erstellt wurden, verweisen auf einen nicht fakturierten vertrieblichen Ist-Wert.) Allgemeine Hauptbuchintegrationssysteme können sich diese Umkehrung zunutze machen, um laufende Projektarbeit (WIP, Work In Progress) für Buchhaltungszwecke umzukehren.

### <a name="correct-a-confirmed-psa-invoice"></a>Korrigieren einer bestätigten PSA-Rechnung

Bestätigte PSA-Rechnungen können bearbeitet (korrigiert) werden. Wenn Sie eine bestätigte Rechnung korrigieren, wird ein neuer Korrekturrechnungsentwurf erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese Korrekturrechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.

Transaktionen, die keine Korrektur benötigen, können aus dem Korrekturrechnungsentwurf entfernt werden. Wenn Sie nur eine Teilmenge umkehren oder zurückgeben möchten, können Sie das Feld **Menge** im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete vertriebliche Ist-Wert acht Stunden war, und das korrigierte Rechnungspostendetail eine reduzierte Menge von sechs Stunden aufweist, kehrt PSA die ursprüngliche abgerechnete Vertriebszeile um und erstellt zwei neue Ist-Werte:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
