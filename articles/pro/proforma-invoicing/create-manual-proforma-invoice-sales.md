---
title: Proforma-Projektrechnungen
description: Dieses Thema enthält Informationen zu Proforma-Projektrechnungen in Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1b839c3e40ddcfe1f07b0330a78c42851140d4bf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004035"
---
# <a name="proforma-project-pnvoices"></a>Proforma-Projektrechnungen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Proforma-Projektrechnungen sind hilfreich, da sie Projekt-Managern eine zweite Genehmigungsstufe bietet, bevor sie Rechnungen für Kunden erstellen. Die erste Genehmigungsstufe ist abgeschlossen, wenn die von den Projektteammitgliedern eingereichten Zeit-, Ausgaben- und Materialeinträge genehmigt wurden.

Dynamics 365 Project Operations Lite Deployment ist nicht dafür ausgelegt, kundenorientierte Rechnungen zu erstellen. Die folgende Liste zeigt, warum Rechnungen nicht generiert werden können:

- Es sind keine Steuerinformationen enthalten.
- Andere Währungen können nicht in die Rechnungswährung umgerechnet werden.
- Rechnungen zum Drucken können nicht korrekt formatiert werden.

Stattdessen können Sie ein Finanz- oder Buchhaltungssystem verwenden, um Kundenrechnungen zu erstellen, die die Informationen aus generierten Rechnungsvorschlägen verwenden.

## <a name="creating-project-invoices"></a>Erstellen von Projektrechnungen

Projektrechnungen können einzeln oder mithilfe von Massendatensätzen erstellt werden. Sie können manuell erstellt oder so konfiguriert werden, dass sie in automatisierten Abläufen generiert werden.

### <a name="manually-create-project-invoices"></a>Manuelles Erstellen von Projektrechnungen 

Auf der Listenseite **Projektverträge** können Sie Projektrechnungen für jeden Projektvertrag separat erstellen, Sie können jedoch auch Rechnungen für mehrere Projektverträge in einem Massenvorgang erstellen.

   - Um eine Rechnung für einen bestimmten Projektvertrag zu erstellen, öffnen Sie auf der Listenseite **Projektverträge** einen Projektvertrag, und wählen Sie dann **Projektrechnungen erstellen** aus.

   Es wird eine Rechnung für alle Transaktionen des ausgewählten Projektvertrags generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Kosten, Materialien, Meilensteine, produktbasierte Vertragslinien und andere nicht in Rechnung gestellte Verkaufsjournalzeilen, die möglicherweise bestätigt wurden.

Rechnungen in einem Massenvorgang erstellen:

1. Wählen Sie auf der Listenseite **Projektverträge** einen oder mehrere Projektverträge aus, für den bzw. die Sie eine Rechnung erstellen möchten, und wählen Sie dann **Projektrechnungen erstellen** aus.
2. Eine Warnmeldung informiert Sie darüber, dass es zu Verzögerungen kommen kann, bevor Rechnungen erstellt werden. Der Vorgang wird ebenfalls angezeigt. Wählen Sie **OK** aus, um das Nachrichtenfeld zu schließen.

   Es wird eine Rechnung für alle Transaktionen einer Vertragszeile generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Kosten, Materialien, Meilensteine, produktbasierte Vertragslinien und andere nicht in Rechnung gestellte Verkaufsjournalzeilen, die möglicherweise bestätigt wurden.

3. Zeigen Sie die generierten Rechnungen an, indem Sie zu **Vertrieb** \> **Fakturierung** \> **Rechnungen** wechseln. Sie sehen eine Rechnung für jeden Projektvertrag.

### <a name="set-up-automated-creation-of-project-invoices"></a>Einrichten der automatischen Erstellung von Projektrechnungen 

Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf zu konfigurieren.

1. Gehen Sie zu **Einstellungen** \> **Batch-Auftrag**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Vorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss den Wortlaut „Rechnungen erstellen” enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz suchen** werden die folgenden Workflows angezeigt:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld die Option **OK** aus. Auf den Workflow **Ruhezustand** folgt der Workflow **Verarbeiten**.

    Sie können auch **ProcessRunner** in Schritt 5 auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen erstellt. Dieser Workflow durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt die Rechnungen. Zur Bestimmung der Vertragszeilen, für die Rechnungen erstellt werden sollen, überprüft der Workflow die Rechnungsdurchlaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungsdurchlaufdatum aufweisen, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, werden keine Rechnungen erstellt.

Nachdem **ProcessRunner** ausgeführt wurde, ruft es **ProcessRunCaller** auf, gibt die Endzeit an und wird geschlossen. **ProcessRunCaller** startet dann einen Timer, der ab der angegebenen Endzeit 24 Stunden lang läuft. Am Ende des Timers ist **ProcessRunCaller** geschlossen.

Der Batchverarbeitungsauftrag zum Erstellen von Rechnungen ist ein wiederkehrender Auftrag. Wenn diese Stapelverarbeitung mehrmals ausgeführt wird, werden mehrere Instanzen des Jobs erstellt und können Fehler verursachen. Um dieses Problem zu umgehen, sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Gleiches gilt für eine projektbasierte Vertragszeile.      
 
### <a name="edit-a-draft-invoice"></a>Bearbeiten eines Rechnungsentwurfs

Wenn Sie einen Projektrechnungsentwurf erstellen, werden sämtliche nicht fakturierten Verkaufstransaktionen, die bei der Genehmigung der Zeit- und Ausgabeneinträge erstellt wurden, in die Rechnung aufgenommen. Sie können die folgenden Anpassungen vornehmen, solange sich die Rechnung noch im Entwurfsstadium befindet:

- Rechnungspositionsdetails löschen oder bearbeiten.
- Menge und Fakturierungstyp bearbeiten und anpassen.
- Zeit, Ausgaben, Material und Gebühren als Transaktionen direkt der Rechnung hinzufügen. Sie können diese Funktion verwenden, wenn die Rechnungszeile einer Vertragszeile zugeordnet ist, die diese Transaktionsklassen zulässt.

Wählen Sie **Bestätigen** aus, um eine Rechnung zu bestätigen. Diese Aktion ist eine unidirektionale Aktion. Wenn Sie **Bestätigen** auswählen, wird die Rechnung schreibgeschützt und erstellt zudem für jede Rechnungszeile abgerechnete vertriebliche Ist-Werte aus jedem Rechnungspositionsdetail. Wenn das Rechnungspositionsdetail auf einen nicht fakturierten vertrieblichen Ist-Wert verweist, wird der nicht fakturierte vertrieblichen Ist-Wert umgekehrt. Alle Rechnungszeilendetails, die aus einem Zeit-, Kosten- oder Materialverbrauchseintrag erstellt wurden, verweisen auf einen nicht in Rechnung gestellten tatsächlichen Umsatz. Hauptbuch-Integrationssysteme können diese Umkehrung verwenden, um laufende Projektarbeiten (WIP) für Buchhaltungszwecke rückgängig zu machen.

### <a name="correct-a-confirmed-invoice"></a>Korrigieren einer bestätigten Rechnung

Bestätigte Rechnungen können bearbeitet werden. Wenn Sie eine bestätigte Rechnung korrigieren, wird ein neuer Korrekturrechnungsentwurf erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese Korrekturrechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit null ausgewiesen sind.

Wenn Transaktionen vorliegen, die keine Korrektur benötigen, können aus dem Korrekturrechnungsentwurf entfernt werden. Wenn Sie nur eine Teilmenge umkehren oder zurückgeben möchten, können Sie das Feld **Menge** im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile storniert und zwei neue Ist-Werte werden erstellt:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später abgerechnet oder als nicht fakturierbar markiert werden.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
