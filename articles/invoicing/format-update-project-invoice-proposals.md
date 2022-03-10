---
title: Projektrechnungsvorschläge verwalten
description: Dieses Thema bietet Details zur Verarbeitung von kundenspezifischen Rechnungen für Project Operations für ressourcen /nicht vorrätige Szenarien.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989910"
---
# <a name="manage-project-invoice-proposals"></a>Projektrechnungsvorschläge verwalten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Projektrechnungsvorschläge können von Ihrer Rechnungsabteilung bearbeitet werden, wenn die folgenden zwei Bedingungen erfüllt sind:

  - Der Projektmanager bestätigt die Proforma-Rechnung in Microsoft Dataverse.
  - Alle in der Proforma-Rechnung enthaltenen nicht in Rechnung gestellten Zeit- und Materialverkaufstransaktionen werden mithilfe dem Dynamics 365 Journal **Integration von Project Operations** gebucht.

Führen Sie die folgenden Schritte aus, um einen Projektrechnungsvorschlag in Dynamics 365 Finance abzuschließen.

1. Überprüfen Sie die Rechnungsinformationen für Zeit- und Materialtransaktionen und buchen Sie das Journal **Project Operations**.
2. Überprüfen Sie die Rechnungsinformationen für Meilensteine für die Festpreisabrechnung.
3. Rechnungsvorschläge formatieren und überprüfen.
4. Projektrechnungen buchen und drucken.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Verwalten Sie Rechnungsinformationen im Journal Project Operations Integration

Projekt-Istwerte, die in Dataverse erstellt wurden, werden vom Projektbuchhalter geprüft und in Finance gebucht. Weitere Informationen zur Arbeit mit dem Integrationsjournal finden Sie unter [Integrationsjournal in Project Operations](../project-accounting/project-operations-integration-journal.md).

Istwerte und nicht abgerechnete Umsatzzahlen werden dem Integrationsjournal als separate Zeilen hinzugefügt:

  - Der Stückkostenpreis und der Kostenbetrag auf dem tatsächlichen Standardwert aus der Projektkosten-Transaktion in Dataverse.
  - Der Verkaufspreis und der Verkaufsbetrag für die nicht in Rechnung gestellte Verkaufstransaktion werden standardmäßig aus der tatsächlichen nicht in Rechnung gestellten Verkaufstransaktion des Projekts in Dataverse übernommen.

### <a name="billing-sales-tax"></a>Abrechnung der Umsatzsteuer

Die Umsatzsteuerberechnung für die Abrechnung erfolgt durch die Feldkombination **Abrechnung Umsatzsteuergruppe** und **Abrechnungsposten Umsatzsteuergruppe** auf einem nicht abgerechneten Verkaufsrekord auf der Journalzeile **Project Operations Integration**. Das System verwendet diese Feldwerte standardmäßig basierend auf den Einstellungen auf der Registerkarte **Finanzen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**.

- **Umsatzsteuergruppenmethode** bestimmt die Standardlogik der Abrechnungsumsatzsteuergruppe:
  
  - **Projekt**: Standardmäßig wird immer die Abrechnungsumsatzsteuergruppe aus dem Projekt verwendet. Sie können die Standardabrechnungsumsatzsteuergruppe für ein Projekt überprüfen oder ändern, indem Sie **Standardabrechnung anzeigen** auf der Seite **Alle Projekte** auswählen.
  - **Projektvertrag**: Standardmäßig wird immer die Abrechnungsumsatzsteuergruppe aus dem Vertrag verwendet. Sie können die Standardabrechnungsumsatzsteuergruppe für einen Projektvertrag überprüfen oder ändern, indem Sie **Standardabrechnung anzeigen** auf der Seite **Projekteverträge** auswählen.
  - **Kunde**: Standardmäßig wird immer die Abrechnungsumsatzsteuergruppe vom Kunden verwendet.
  - **Suche**: Sucht in allen oben genannten Objekten und wählt den ersten verfügbaren Wert aus. Die Suche beginnt mit der Entität **Projekt**, gefolgt von der Entiät **Projektvertrag** und schließlich die Entität **Kunde**.

- **Umsatzsteuergruppenmethode für Rechnungspositionen** bestimmt die Standardlogik der Abrechnungsumsatzsteuergruppe für Rechnungspositionen:
  
  - Für Zeit-, Kosten- und Gebührentransaktionsarten wird die Umsatzsteuergruppe für Rechnungspositionen immer standardmäßig von der Entität **Projektkategorie** abgeleitet.
  - Für Materialtransaktionsarten wird die Umsatzsteuergruppe der Rechnungsposition basierend auf dem Standardwert der Einstellung **Artikelumsatzsteuer-Gruppenmethode** in **Projektmanagement- und Buchhaltungsparameter** verwendet. Die Artikelnummer ist standardmäßig die Artikelumsatzsteuergruppe aus der Entität **Freigegebenes Produkt**. Die Kategorie ist standardmäßig die Artikelumsatzsteuergruppe aus der Entität **Projektkategorie**.

### <a name="financial-dimensions"></a>Finanzielle Dimensionen

Die finanziellen Dimensionen für nicht in Rechnung gestellte Verkaufsunterlagen im Journal **Integration von Project Operations** stammt standardmäßig aus der Entität **Projekt**. Finanzielle Dimensionen können durch Auswahl von **Beträge verteilen** überprüft und angepasst werden. Wenn Sie die finanziellen Dimensionen des nicht in Rechnung gestellten Verkaufsdatensatzes ändern müssen, nachdem das Integrationsjournal gebucht wurde, aber bevor die Proforma-Rechnung bestätigt wurde, gehen Sie zu **Alle Projekte** > **Verwalten** > **Gebuchte Transaktionen** und wählen Sie die Transaktion aus und wählen Sie dann **Prozess** > **Buchhaltung anpassen**.

### <a name="exchange-rates"></a>Wechselkurse

Nicht in Rechnung gestellte Transaktionswährung in Dataverse wird als Transaktionswährung in Finance verwendet und zu den in Finance definierten Wechselkursen in die Buchhaltungswährung des Unternehmens umgerechnet.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Verwalten Sie die finanziellen Eigenschaften von Abrechnungsmeilensteinen 

Projektvertragszeilen nach der Festpreisabrechnungsmethode werden über [Festpreismeilensteine](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line) in Rechnung gestellt. Der Projektbuchhalter kann die Abrechnungsmeilensteine im Finanzbereich unter **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Verwalten** > **Transaktionen auf Rechnung** überprüfen.

### <a name="billing-sales-tax"></a>Abrechnung der Umsatzsteuer

Die Werte **Umsatzsteuergruppe** und **Artikel Umsatzsteuergruppe** stammen standardmäßig aus den Einstellungen, wenn ein neuer Abrechnungsmeilenstein in Dataverse erstellt wird. Das System verwendet die Werte für diese Felder standardmäßig basierend auf den Einstellungen auf der Registerkarte **Finanzen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**.

- **Umsatzsteuergruppenmethode** bestimmt die Standardlogik der **Abrechnungsumsatzsteuergruppe**:

    - **Projekt**: Standardmäßig wird immer die Abrechnungsumsatzsteuergruppe aus dem Projekt verwendet. Sie können die Standardabrechnungsumsatzsteuergruppe für ein Projekt überprüfen oder ändern, indem Sie **Standardabrechnung anzeigen** auf der Seite **Alle Projekte** auswählen.
    - **Projektvertrag**: Wird standardmäßig immer die Abrechnungsumsatzsteuergruppe aus dem Vertrag verwendet. Sie können die Standardabrechnungsumsatzsteuergruppe für einen Projektvertrag überprüfen oder ändern, indem Sie **Standardabrechnung anzeigen** auf der Seite **Projekteverträge** auswählen.
    - **Kunde**: Wird standardmäßig immer die Abrechnungsumsatzsteuergruppe vom Kunden verwendet.
    - **Suche**: Wird in allen oben genannten Entitäten in dieser Liste suchen und wählt den ersten verfügbaren Wert aus. Die Suche beginnt mit der Entität **Projekt**, gefolgt von der Entiät **Projektvertrag** und dann von der Entität **Kunde**.

- **Festpreis Meilenstein Artikel Umsatzsteuergruppe** wird als Standardwert im Feld **Artikel Umsatzsteuergruppe** für den Abrechnungsmeilenstein verwendet. Der Buchhalter kann diesen Wert auf der Seite **Transaktionen auf Rechnung** überprüfen und ändern. Das System verwendet den Wert aus der On-Account-Transaktion beim Erstellen einer Projektrechnungsvorschlagszeile.
 

### <a name="financial-dimensions"></a>Finanzielle Dimensionen

Die finanziellen Standarddimensionen für den Meilenstein der Festpreisabrechnung werden in den Projektvertragszeilen festgelegt. Gehen Sie zu **Projektverträge** > **Standardabrechnung anzeigen** und wählen Sie auf der Registerkarte **Vertragszeilen** dann **Preisvertragszeilen** aus. Legen Sie dann die finanziellen Dimensionswerte fest, die Sie als Standard verwenden möchten.

Der Projektbuchhalter kann die Umsatzsteuer- und Finanzdimensionsinformationen zu Rechnungsmeilensteinen bearbeiten, bis der Projektrechnungsvorschlag erstellt wird.


## <a name="create-project-invoice-proposals"></a>Projektrechnungsvorschläge erstellen

Projektrechnungsvorschläge können im Modul **Projektmanagement und Buchhaltung** eingesehen werden, indem Sie zu **Projektrechnungen** > **Projektrechnungsvorschläge** gehen.

Die Kopfzeile des Projektrechnungsvorschlags wird in Finance erstellt, wenn die Proforma-Rechnung in Dataverse bestätigt wird. Zur einfacheren Abstimmung setzt das System die Projektrechnungsvorschlagsnummer in Finance auf die selbe Nummer wie die Proforma-Rechnungs-ID in Dataverse. Da Proforma-Rechnungen nicht unbedingt in derselben Reihenfolge bestätigt werden, in der sie erstellt wurden, muss die Reihenfolge der Projektrechnungsvorschlagsnummern in Finance die Änderungen an niedrigeren und höheren Nummern berücksichtigen. Konfigurieren Sie Nummernfolgen mit den folgenden Schritten:

1. Rufen Sie in Finance **Organisationsverwaltung** > **Nummernkreise** > **Nummernkreise** auf.
2. In dem Filter **Bereich** wählen Sie **Projekte**.
3. In dem Filter **Referenz** wählen Sie **Rechnungsvorschlag**.
4. Verwenden Sie die das Feld **Unternehmen** zum Filtern jeder juristischen Person mit aktivierter Project Operations Dataverse Integration.
5. Öffnen Sie **Details zur Nummernfolge** und legen Sie auf der Registerkarte **Allgemein** fest:

    - **Benutzeränderungen zulassen: Auf eine niedrigere Zahl** = **Ja**
    - **Benutzeränderungen zulassen: Auf eine höhere Zahl** = **Ja**

Projektrechnungsvorschlagszeilen werden vom System mithilfe des periodischen Prozesses hinzugefügt **Import aus Staging-Tabelle** (**Projektmanagement und Buchhaltung** > **Periodisch** > **Project Operations Integration** > **Import aus Staging-Tabelle**). Dieser Prozess kann entweder manuell oder in regelmäßigen Abständen ausgeführt werden. Das System fügt dem Rechnungsvorschlagsdokument erst dann Zeilen hinzu, wenn alle Zeilen zur Rechnungsstellung bereit sind. Zeit- und Materialtransaktionen können nur in Rechnung gestellt werden, wenn sie mithilfe der Erfassung **Project Operations Integration** gebucht werden.

## <a name="format-and-print-invoice-proposals"></a>Projektrechnungsvorschläge formatieren und drucken

Der Projektbuchhalter kann einen Ausdruck der Projektrechnung mithilfe der Seite **Rechnungsvorschlag formatieren** anpassen und Verwaltungsfunktionen drucken.

### <a name="format-invoice-proposals"></a>Projektrechnungsvorschläge formatieren

Die Seite **Rechnungsvorschläge formatieren** ermöglicht es, benutzerdefinierte Gruppierungstransaktionen in der Kundenprojektrechnung anzuzeigen.

1. Auf der Seite **Projektrechnungsvorschlag** wählen Sie **Drucken** > **Rechnungsvorschlag formatieren**.
2. Wählen Sie **Neu**, um eine neue Gruppierung für den Ausdruck der Projektrechnung zu erstellen.
3. In dem Feld **Detail/Zusammenfassung** wählen Sie die Optionen für diese Gruppierung aus:

    - Wählen Sie **Detail**, um die Transaktionsdetails der Kundenrechnung auszudrucken.
    - Wählen Sie **Zusammenfassung**, um die Transaktionszusammenfassung der Kundenrechnung auszudrucken.

> [!NOTE]
> Die Auswahl im Feld **Detail/Zusammenfassung** auf der Seite **Rechnungsvorschlag formatieren** überschreibt das in der Option ausgewählte Feld **Rechnungsformat** auf der Seite **Rechnungsvorschläge** zum Drucken einer detaillierten Rechnung oder einer zusammengefassten Rechnung.

- Wählen Sie die Transaktionszeilen aus, die in diesem Abschnitt auf der Registerkarte **Verfügbare Transaktionen** enthalten sein soll und wählen Sie **Transaktionen einschließen**, um sie in die Registerkarte **Ausgewählte Transaktionen** zu verschieben.
- Wählen Sie **Nach oben bewegen** und **nach unten bewegen**, um die Reihenfolge der Abschnitte zu ändern.
- Wählen Sie **Druckvorschau** zur Vorschau der formatierten Rechnung.

### <a name="print-management"></a>Druckverwaltung

Die Druckverwaltung verwendet verschiedene Berichtsdateien, um bestimmte Ziele zu drucken und den Fußzeilentext für die Rechnung anzupassen. Die Druckverwaltung kann auf Modulebene eingerichtet werden. Diese Einstellungen können jedoch für einen bestimmten Kunden-, Vertrags- oder Rechnungsvorschlag überschrieben werden. Um auf diese Funktion zuzugreifen, klicken Sie auf die Seite **Projektrechnungsvorschlag** und wählen **Drucken** > **Druckverwaltung**.

Das Einrichten der Druckverwaltung wird als Baumansicht angezeigt, in der auf jeder Knotenebene die verfügbaren Dokumente zum Anpassen angezeigt werden. Sie können benutzerdefinierte Ausdrucke auf Modul-, Kunden-, Vertrags- oder Rechnungsvorschlagsdokumentebene zuweisen. Erweitern Sie zum Ändern des Originaldokumentausdrucks den gewünschten Knoten und wählen Sie **Originalartikel**. In dem Feld **Berichtsformat** wählen Sie das Berichtsformat aus, das zum Drucken verwendet werden soll. Sie können benutzerdefinierte Berichtsformate verwenden, indem Sie [das Gechäftsdokumenten-Framework](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management) verwenden.

## <a name="post-invoice-proposals"></a>Projektrechnungsvorschläge buchen

Nachdem die Rechnung überprüft und bearbeitet wurde und die Rechnungsvorschlagszeilen zufriedenstellend sind, überprüfen Sie die Rechnungssummen und die Umsatzsteuer. In der Gruppe **Einzelheiten** wählen Sie **Summen** und dann **Buchen**, um die Rechnung zu buchen.

Deaktivieren Sie das Kontrollkästchen, um die Rechnung vor dem **Buchen** anzuzeigen. **Pro forma** wird auf die Rechnung gedruckt, um anzuzeigen, dass es sich um eine Musterrechnung handelt. Um die Rechnung zu drucken, wählen Sie das Kontrollkästchen **Rechnung drucken** aus.

Zusätzlich zur Seite **Rechnungsvorschlag** können Rechnungsvorschläge auch durch Ausführen des periodischen Auftrags **Rechnungsvorschläge buchen** gebucht werden. Um diesen Auftrag zu finden, gehen Sie zu **Projektverwaltung und Buchhaltung** > **Periodisch** > **Projektrechnungen** > **Rechnungsvorschläge buchen**.

Diese Seite zeigt alle Rechnungsvorschläge, die zur Buchung bereit sind. Sie können die Buchung von Rechnungsvorschlägen durch Auswahl von **Batch** planen. Stellen Sie die **Batchverarbeitungsparameter** auf **Ja** und legen Sie die Batchverarbeitung auf **Serie** fest.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
