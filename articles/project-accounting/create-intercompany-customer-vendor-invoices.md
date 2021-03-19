---
title: Intercompany-Debitoren- und -Kreditorenrechnungen erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Intercompany-Debitoren- und -Kreditorenrechnungen.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287462"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Intercompany-Debitoren- und -Kreditorenrechnungen erstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Ein Projektbuchhalter in einer kreditgebenden juristischen Person erstellt eine Intercompany-Kundenrechnung für die Projektkosten, die an die kreditnehmende Person übertragen werden. Nachdem die Intercompany-Kundenrechnung genehmigt und gebucht wurde, sendet die kreditgebende juristische Person die Intercompany-Rechnung an die kreditnehmende juristische Person.

Der Projektbuchhalter der kreditgebenden juristischen Person kann einen Batch-Prozess einrichten, um wiederkehrende Intercompany-Rechnungen zu erstellen. Der Projektbuchhalter gibt die Kriterien an, z. B. bestimmte Projekte, um Intercompany-Rechnungen in einem Stapel zu erstellen.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Erstellen Sie manuell eine Intercompany-Kundenrechnung für Projekttransaktionen 

Verwenden Sie dieses Verfahren, um manuell eine Intercompany-Kundenrechnung für Projekttransaktionen zu erstellen. Suchen Sie nach Stunden, die von Arbeitnehmern für Projekte in den kreditnehmenden juristischen Personen gebucht wurden, und nach Ausgaben, die Ihrer juristischen Person im Auftrag von kreditnehmenden juristischen Personen entstanden sind. Sie können nach Name der juristischen Person, Projektvertragsnummer, Projektnummer, Datumsbereich oder einer beliebigen Kombination dieser Optionen suchen. Wählen Sie in den Suchergebnissen die Transaktionen aus, die einer Intercompany-Rechnung hinzugefügt werden sollen.

1. Gehen Sie in Dynamics 365 Finance zu **Projektmanagement und Buchhaltung** > **Projektrechnungen** > **Intercompany-Debitorenrechnungen**. Auf der **Intercompany-Debitorenrechnungen**-Listenseite wählen Sie im Aktionsbereich **Neu.**
2. Wählen Sie auf der **Intercompany-Debitorenrechnungen erstellen**-Seite im **Juristische Person**-Feld eine kreditnehmende juristische Person aus.
3. Optional: Geben Sie einen bestimmten Projektvertrag und eine bestimmte Projektnummer ein.
4. Grenzen Sie die Suche ein, indem Sie einen Datumsbereich auswählen. Geben Sie bestimmte Daten in die Felder **Anfangsdatum** und **Enddatum** ein. In den Suchergebnissen werden nur Intercompany-Transaktionen angezeigt, die innerhalb dieses Datumsbereichs gebucht wurden.
5. Legen Sie **Erweiterte Projektjournalzeilenparameter** auf **Ja** fest und wählen Sie **Suche** aus.
6. Wählen Sie in den Suchergebnissen die Transaktionen aus, die in den Intercompany-Rechnungsvorschlag aufgenommen werden sollen, und wählen Sie dann **OK**.
7. Auf der **Intercompany-Debitorenrechnungen**-Seite werden die konzerninternen Projekttransaktionen angezeigt, die Sie aus den Suchergebnissen ausgewählt haben. Gehen Sie wie folgt vor, um die Transaktionen zu ändern, bevor Sie die Rechnung an die kreditnehmende juristische Person senden:
  
    1. Öffnen Sie die Seite **Rechnungsvorschlag erstellen**. Wählen Sie zusätzliche Intercompany-Transaktionen für die aktuelle Rechnung aus und wählen Sie dann **Zeile hinzufügen**.
    2. Wählen Sie zum Entfernen einer Zeile die gewünschte Zeile aus, und wählen Sie **Entfernen**.
    3. Zeigen Sie Kommentare, Gründe, finanzielle Dimensionen und andere Informationen zu einer ausgewählten Zeile im Inforegister **Rechnungspositionen** an.
    
8. Wählen Sie zum Buchen einer Intercompany-Debitorenrechnung im Aktionsbereich **Buchen** aus.

> [!NOTE]
> Wenn Ihre Organisation verlangt, dass Intercompany-Rechnungen überprüft werden, bevor sie gebucht werden, kann ein Systemadministrator einen Workflow für Intercompany-Rechnungen einrichten. Wenn für Intercompany-Rechnungen kein Workflow eingerichtet ist, können Sie die Intercompany-Rechnung buchen.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Erstellen Sie einen Stapeljob für Intercompany-Rechnungen

Sie können für alle ausleihenden juristischen Personen mehrere Intercompany-Rechnungen gleichzeitig erstellen. Mithilfe der Suchfunktion können Sie beispielsweise nach allen Transaktionen suchen, die von ausgeliehenen Mitarbeitern gebucht wurden und sich auf Projekte beziehen, die von anderen juristischen Personen verwaltet werden. Anschließend können Sie für jede kreditnehmende juristische Person eine Intercompany-Rechnung für die in den Suchergebnissen angegebenen Transaktionen erstellen.

1. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Preiodisch** > **Projektrechnungen** > **Intercompany-Debitorenrechnungen erstellen**.
2. Wählen Sie auf der **Intercompany-Debitorenrechnungen erstellen**-Seite im **Unternehmen**-Feld eine juristische Person zur Rechnungsstellung aus. Wenn Sie kein Unternehmen auswählen, werden alle Transaktionen, die die Suchkriterien erfüllen, für alle kreditnehmenden juristischen Personen angezeigt.
3. Wählen Sie unter **Eine Rechnung erstellen pro**, ob eine Rechnung für Intercompany-Transaktionen basierend auf einem Projekt oder basierend auf einer ausleihenden juristischen Person erstellt werden soll.
4. Optional: Um ein bestimmtes Projekt und einen bestimmten Projektvertrag auszuwählen, für den Intercompany-Rechnungen erstellt werden solle, klicken Sie auf **Auswählen**. Auf der **Anfrage**-Seite im **Kriterien**-Feld wählen Sie den Projektvertrag, die Projektnummer oder beides aus, und wählen dann **OK**.
5. Auf der **Stapel**-Registerkarte richten Sie einen Stapelprozess ein, um wiederkehrende Intercompany-Rechnungen zu erstellen. Weitere Informationen finden Sie unter [Stapelverarbeitungsauftrag aus einem Formular senden](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Wählen Sie zum Buchen von Intercompany-Rechnungen im Aktionsbereich **Buchen** aus.

> [!NOTE]
> Wenn Ihre Organisation verlangt, dass Intercompany-Rechnungen überprüft werden, bevor sie gebucht werden, kann ein Systemadministrator einen Workflow für Intercompany-Rechnungen einrichten. Wenn für Intercompany-Rechnungen kein Workflow eingerichtet ist, können Sie die Intercompany-Rechnungen buchen.

## <a name="post-the-intercompany-vendor-invoice"></a>Intercompany-Kreditorenrechnung buchen

Ein Projektbuchhalter in der kreditnehmenden juristischen Person kann ausstehende Intercompany-Kreditorenrechnungen überprüfen, wenn die entsprechende Intercompany-Kundenrechnung gebucht wird. In Finance gehen Sie in der kreditnehmenden juristischen Person zu **Kreditorenkonten** > **Rechnungen** > **Ausstehende Kreditorenrechnung**. Die ausstehende Rechnungsnummer stimmt mit der konzerninternen Kundenrechnungsnummer überein. Stellen Sie sicher, dass die Rechnung korrekt ist, und buchen Sie die Rechnung. Durch die Buchung einer konzerninternen Kreditorenrechnung werden ein Projektnebenbuch und eine Hauptbuchtransaktion erstellt, die die Transaktionskosten in der kreditnehmenden juristischen Person widerspiegeln.


[!INCLUDE[footer-include](../includes/footer-banner.md)]