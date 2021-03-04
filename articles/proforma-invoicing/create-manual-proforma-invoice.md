---
title: Manuelle Proforma-Rechnung erstellen
description: Diese Thema enthält Informationen zum Erstellen einer Proforma-Rechnung.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d3c84664f1b0701db17f0c05654e0c99bb6c640
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128057"
---
# <a name="create-a-manual-proforma-invoice"></a>Manuelle Proforma-Rechnung erstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Die Rechnungstellung bietet Projekt-Managern eine zweite Genehmigungsstufe, bevor sie Rechnungen für Kunden erstellen. Die erste Genehmigungsstufe ist abgeschlossen, wenn die von den Projektteammitgliedern eingereichten Zeit- und Kosteneinträge genehmigt wurden.

Dynamics 365 Project Operations ist aus folgenden Gründen nicht für die Erstellung von Kundenrechnungen konzipiert:

- Es sind keine Steuerinformationen enthalten.
- Es können keine anderen Währungen mit korrekt konfigurierten Wechselkursen in die Rechnungswährung konvertiert werden.
- Rechnungen können nicht korrekt für den Druck formatiert werden.

Stattdessen können Sie ein Finanz- oder Buchhaltungssystem verwenden, um Kundenrechnungen zu erstellen, die die Informationen aus generierten Rechnungsvorschlägen verwenden.

## <a name="creating-project-invoices"></a>Erstellen von Projektrechnungen

Projektrechnungen können einzeln oder mithilfe von Massendatensätzen erstellt werden. Sie können manuell erstellt oder so konfiguriert werden, dass sie in automatisierten Abläufen generiert werden.

### <a name="manually-create-project-invoices"></a>Manuelles Erstellen von Projektrechnungen 

Auf der Listenseite **Projektverträge** können Sie Projektrechnungen für jeden Projektvertrag separat erstellen, Sie können jedoch auch Rechnungen für mehrere Projektverträge in einem Massenvorgang erstellen.

Führen Sie diesen Schritt aus, um eine Rechnung für einen bestimmten Projektvertrag zu erstellen.

- Öffnen Sie auf der Listenseite **Projektverträge** einen Projektvertrag und wählen Sie dann **Rechnung erstellen** aus.

    Es wird eine Rechnung für alle Transaktionen des ausgewählten Projektvertrags generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Ausgaben und Meilensteine sowie produktbasierte Vertragszeilen.

Befolgen Sie diese Schritte, um Rechnungen in einem Massenvorgang zu erstellen.

1. Wählen Sie auf der Listenseite **Projektverträge** einen oder mehrere Projektverträge aus, für den bzw. die Sie eine Rechnung erstellen müssen, und wählen Sie dann **Projektrechnungen erstellen** aus.

    Eine Warnmeldung weist Sie darauf hin, dass es zu Verzögerungen kommen kann, bevor Rechnungen erstellt werden. Der Prozess wird auch angezeigt.

2. Wählen Sie **OK** aus, um das Meldungsfeld zu schließen.

    Es wird eine Rechnung für alle Transaktionen einer Vertragszeile generiert, die den Status **Bereit für die Rechnungsstellung** aufweisen. Diese Transaktionen umfassen Zeit, Ausgaben und Meilensteine sowie produktbasierte Vertragszeilen.

3. Um die generierten Rechnungen anzuzeigen, wechseln Sie zu **Vertrieb** \> **Fakturierung** \> **Rechnungen**. Sie sehen eine Rechnung für jeden Projektvertrag.

### <a name="set-up-automated-creation-of-project-invoices"></a>Einrichten der automatischen Erstellung von Projektrechnungen 

Führen Sie die folgenden Schritte aus, um einen automatisierten Rechnungslauf zu konfigurieren.

1. Gehen Sie zu **Einstellungen** \> **Batch-Auftrag**.
2. Erstellen Sie einen Batchauftrag und nennen Sie ihn **Vorgang zum Erstellen von Rechnungen**. Der Name des Batchauftrags muss den Wortlaut „Rechnungen erstellen” enthalten.
3. Wählen Sie im Feld **Auftragstyp** **Keiner** aus. Standardmäßig sind die Optionen **Frequenz täglich** und **Ist aktiv** auf **Ja** festgelegt.
4. Wählen Sie **Workflow ausführen** aus. Im Dialogfeld **Datensatz nachschlagen** finden Sie drei Workflows:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Wählen Sie **ProcessRunCaller** und dann **Hinzufügen** aus.
6. Wählen Sie im nächsten Dialogfeld **OK** aus. Einem **Sleep**-Workflow folgt ein **Process** -Workflow.

    In Schritt 5 können Sie auch **ProcessRunner** auswählen. Wenn Sie dann **OK** auswählen, folgt auf einen **Process**-Workflow ein **Sleep**-Workflow.

Die Workflows **ProcessRunCaller** und **ProcessRunner** erstellen Rechnungen. **ProcessRunCaller** ruft **ProcessRunner** auf. **ProcessRunner** ist der Workflow, der die Rechnungen tatsächlich erstellt. Es durchläuft alle Vertragszeilen, für die Rechnungen erstellt werden sollen, und erstellt Rechnungen für diese Zeilen. Zur Bestimmung der Vertragszeilen, für die Rechnungen erstellt werden sollen, überprüft der Job die Rechnungsdurchlaufdaten für die Vertragszeilen. Wenn Vertragszeilen, die zu einem Vertrag gehören, dasselbe Rechnungsdurchlaufdatum aufweisen, werden die Transaktionen zu einer Rechnung mit zwei Rechnungszeilen zusammengefasst. Wenn keine Transaktionen zum Erstellen von Rechnungen vorhanden sind, überspringt der Job die Rechnungserstellung.

Nachdem **ProcessRunner** ausgeführt wurde, ruft es **ProcessRunCaller** auf, gibt die Endzeit an und wird geschlossen. **ProcessRunCaller** startet dann einen Zeitgeber, der ab der angegebenen Endzeit 24 Stunden lang ausgeführt wird. Am Ende des Zeitgebers wird **ProcessRunCaller** geschlossen.

Beim Stapelverarbeitungsjob zum Erstellen von Rechnungen handelt es sich um einen wiederkehrenden Job. Wenn diese Stapelverarbeitung mehrmals ausgeführt wird, werden mehrere Instanzen des Jobs erstellt und verursachen Fehler. Deshalb sollten Sie die Stapelverarbeitung nur einmal starten und nur dann neu starten, wenn sie nicht mehr ausgeführt wird.

> [!NOTE]
> Die Stapelabrechnung wird nur für Projektvertragszeilen ausgeführt, die durch Rechnungspläne konfiguriert sind. Für eine Vertragszeile mit einer Festpreis-Abrechnungsmethode müssen Meilensteine konfiguriert sein. Für eine Projektvertragsposition mit einer Zeit- und Materialabrechnungsmethode muss ein datumsbasierter Rechnungszeitplan erstellt werden. Gleiches gilt für eine projektbasierte Vertragszeile.      
 
### <a name="edit-a-draft-invoice"></a>Bearbeiten eines Rechnungsentwurfs

Wenn Sie einen Projektrechnungsentwurf erstellen, werden sämtliche nicht fakturierten Verkaufstransaktionen, die bei der Genehmigung der Zeit- und Ausgabeneinträge erstellt wurden, in die Rechnung aufgenommen. Sie können die folgenden Anpassungen vornehmen, solange sich die Rechnung noch im Entwurfsstadium befindet:

- Rechnungspositionsdetails löschen oder bearbeiten.
- Menge und Fakturierungstyp bearbeiten und anpassen.
- Zeit, Ausgaben und Gebühren als Transaktionen direkt der Rechnung hinzufügen. Sie können diese Funktion verwenden, wenn die Rechnungszeile einer Vertragszeile zugeordnet ist, die diese Transaktionsklassen zulässt.

Wählen Sie **Bestätigen** aus, um eine Rechnung zu bestätigen. Die Aktion „Bestätigen” ist eine unidirektionale Aktion. Wenn Sie **Bestätigen** auswählen, generiert das System eine schreibgeschützte Rechnung und erstellt zudem für jede Rechnungszeile abgerechnete vertriebliche Ist-Werte aus jedem Rechnungspositionsdetail. Wenn das Rechnungspositionsdetail auf einen nicht fakturierten vertrieblichen Ist-Wert verweist, kehrt das System auch den nicht fakturierten vertrieblichen Ist-Wert um. (Sämtliche Rechnungspositionsdetails, die aus einem Zeit- oder Ausgabeneintrag erstellt wurden, verweisen auf einen nicht fakturierten vertrieblichen Ist-Wert.) Allgemeine Hauptbuchintegrationssysteme können sich diese Umkehrung zunutze machen, um laufende Projektarbeit (WIP, Work In Progress) für Buchhaltungszwecke umzukehren.

### <a name="correct-a-confirmed-invoice"></a>Korrigieren einer bestätigten Rechnung

Bestätigte Rechnungen können bearbeitet (korrigiert) werden. Wenn Sie eine bestätigte Rechnung korrigieren, wird ein neuer Korrekturrechnungsentwurf erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese Korrekturrechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.

Transaktionen, die keine Korrektur benötigen, können aus dem Korrekturrechnungsentwurf entfernt werden. Wenn Sie nur eine Teilmenge umkehren oder zurückgeben möchten, können Sie das Feld **Menge** im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile storniert und zwei neue Ist-Werte werden erstellt:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]