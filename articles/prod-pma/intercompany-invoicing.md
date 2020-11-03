---
title: Intercompany-Rechnungsstellung
description: Dieser Artikel enthält Informationen und Beispiele zur Intercompany-Rechnungsstellung für Projekte.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076550"
---
# <a name="intercompany-invoicing"></a>Intercompany-Rechnungsstellung

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen und Beispiele zur Intercompany-Rechnungsstellung für Projekte.

Ihre Organisation verfügt möglicherweise über mehrere Abteilungen, Tochterunternehmen und andere juristische Personen, die Produkte und Dienstleistungen für Projekte untereinander übertragen. Die juristische Person, die die Dienstleistung oder das Produkt erbringt, wird als *kreditgebende juristische Person* bezeichnet, und die juristische Person, die die Dienstleistung oder das Produkt erhält, heißt *kreditnehmende juristische Person*. 

Die folgende Abbildung zeigt ein typisches Szenario, in dem zwei juristische Personen, SI FR (die kreditnehmende juristische Person) und SI USA (die kreditgebende juristische Person), Ressourcen gemeinsam nutzen, um ein Projekt für Kunde A zu liefern. In diesem Szenario wird SI FR mit der Lieferung der Arbeit an Kunde A beauftragt. 

[![Beispiel für Intercompany-Rechnungsstellung](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Ziel ist es, die Kostenkontrolle, die Umsatzrealisierung, die Steuern und den Transferpreis für Intercompany-Projekttransaktionen flexibler und leistungsfähiger zu gestalten. Darüber hinaus stehen folgende Funktionen zur Verfügung:

-   Erstellen Sie Kundenrechnungen für ein Projekt in einer kreditnehmenden juristischen Person, indem Sie Intercompany-Arbeitszeittabellen, Ausgaben und Lieferantenrechnungen in einer kreditgebenden juristischen Person verwenden.
-   Steuerberechnungen und indirekte Kosten unterstützen.
-   Verschieben Sie die Umsatzrealisierung in einer kreditgebenden juristischen Person und wenn eine kreditnehmende juristische Person die Kosten erfassen sollte.
-   Einnahmen aus unfertigen Erzeugnissen (Work in Process, WIP) in der kreditgebenden juristischen Person.
-   Legen Sie Verrechnungspreise fest, die auf verschiedenen Preismodellen basieren können. Hier sehen Sie einige Beispiele:
    -   **Menge** – Der Betrag, den Sie in das Feld **Preisgestaltung** eingeben, umfasst die tatsächlichen Kosten pro Menge oder Einheit.
    -   **Gebührenbetrag** – Der Preis/die Kosten pro Transaktion zuzüglich des Gebührenbetrags, den Sie in das Feld **Preisgestaltung** eingeben.
    -   **Gebührenprozentsatz** – Der Transferpreis ist der Preis/die Kosten pro Transaktion multipliziert mit dem Prozentsatz der Gebühren, den Sie in das Feld **Preisgestaltung** eingeben.
    -   **Prozentsatz des Verkaufspreises** – Der Prozentsatz des Verkaufspreises, der an die kreditgebende juristische Person übertragen wird.
    -   **Betrag unter dem Verkaufspreis** – Der Betrag, den die kreditnehmende juristische Person vor der Übertragung an die kreditgebende juristische Person von den Verkaufspreisen zurückhält.
    -   **Beitragsquote** – Die Zahl, die Sie in das Feld **Preisgestaltung** eingeben, ist das Beitragsverhältnis, das als Prozentsatz des Verkaufspreises ausgedrückt wird.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Beispiel 1: Richten Sie Parameter für die Intercompany-Rechnungsstellung ein
In diesem Beispiel ist USSI eine kreditgebende juristische Person, und ihre Ressourcen melden Zeit bei der kreditnehmenden juristischen Person FRSI, die den Vertrag mit dem Endkunden besitzt. Stunden und Kosten, die USSI-Mitarbeiter melden, können in die von FRSI erstellte Projektrechnung aufgenommen werden. Darüber hinaus gibt es eine dritte Quelle für Transaktionen, die von der kreditgebenden juristischen Person (in diesem Beispiel USSI) stammen können, wenn sie Tochterunternehmen (wie FRSI) gemeinsame Anbieterdienste bereitstellt und diese Kosten dann an Projekte innerhalb dieser Tochterunternehmen weiterleitet. Alle übereinstimmenden Rechnungsbelege und Steuerberechnungen werden von Finance ausgefüllt. 

In diesem Beispiel muss FRSI ein Kunde in der juristischen Person von USSI sein, und USSI muss ein Anbieter in der juristischen Person von FRSI sein. Anschließend können Sie eine Intercompany-Beziehung zwischen den beiden juristischen Personen einrichten. Das folgende Verfahren zeigt, wie Sie die Parameter so einrichten, dass beide juristischen Personen an der Intercompany-Rechnungsstellung teilnehmen können.

1. Richten Sie FRSI als Kunden in der juristischen Person USSI und USSI als Anbieter in der juristischen Person FRSI ein. Es gibt drei Einstiegspunkte für die Schritte, die für diese Aufgabe erforderlich sind.

   | Schritt |                                                       Eingangspunkt                                                        |                                                                                                                                                                                               Beschreibung                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Wählen Sie in USSI <strong>Debitorenkonten</strong> &gt; <strong>Debitoren</strong> &gt; <strong>Alle Debitoren</strong> aus. |                                                                                                                                                                  Erstellen Sie einen neuen Kundendatensatz für FRSI und wählen Sie die Kundengruppe aus.                                                                                                                                                                  |
   |  F   |    Wechseln Sie in FRSI zu <strong>Kreditorenkonten</strong> &gt; <strong>Kreditoren</strong> &gt; <strong>Alle Kreditoren</strong>.     |                                                                                                                                                                    Erstellen Sie einen neuen Kreditorendatensatz für USSI und wählen Sie die Kreditorengruppe aus.                                                                                                                                                                    |
   |  C   |                                  Öffnen Sie in FRSI den Kreditorendatensatz, den Sie gerade erstellt haben.                                  | Wählen Sie im Aktionsbereich auf der Registerkarte <strong>Allgemein</strong> in der Gruppe <strong>Einrichten</strong> die Option <strong>Unternehmen</strong>. Legen Sie auf der <strong>Intercompany</strong>-Seite auf der <strong>Handelsbeziehung</strong>-Registerkarte den <strong>Aktiv</strong>-Schieberegler auf <strong>Ja</strong> fest. Wählen Sie im Feld <strong>Debitorenunternehmen</strong> den Kundendatensatz aus, den Sie in Schritt A erstellt haben. |


2. Klicken Sie auf **Projektmanagement und Buchhaltung** &gt; **Konfiguration** &gt; **Projektmanagement-Buchhaltungsparameter** , und klicken Sie dann auf die **Intercompany** -Registerkarte. Die Art und Weise, wie Sie die Parameter einrichten, hängt davon ab, ob Sie die kreditnehmende juristische Person oder die kreditgebende juristische Person sind.
   -   Wenn Sie die kreditnehmende juristische Person sind, wählen Sie die Beschaffungskategorie aus, die für die automatisch generierten Lieferantenrechnungen verwendet werden soll.
   -   Wenn Sie die kreditgebende juristische Person sind, wählen Sie für jede kreditnehmende Entität eine Standardprojektkategorie für jeden Transaktionstyp aus. Projektkategorien werden für die Steuerkonfiguration verwendet, wenn die Rechnungskategorie in Intercompany-Transaktionen nur in der kreditnehmenden juristischen Person vorhanden ist. Sie können festlegen, dass Einnahmen für Intercompany-Transaktionen anfallen. Diese Rückstellung erfolgt bei Buchung der Transaktionen und wird dann bei Buchung der Intercompany-Rechnung storniert.

3. Klicken Sie auf **Projektmanagement und Buchhaltung** &gt; **Konfiguration** &gt; **Preise** &gt; **Transferkosten**.
4. Wählen Sie eine Währung, einen Transaktionstyp und ein Transferpreismodell aus. Die Währung, die auf der Rechnung verwendet wird, ist die Währung, die im Kundendatensatz für die kreditnehmende juristische Person in der kreditgebenden juristischen Person konfiguriert ist. Die Währung wird verwendet, um Einträge in der Transferpreistabelle abzugleichen.
5. Klicken Sie auf **Finanzbuchhaltung** &gt; **Buchungseinstellungen** &gt; **Intercompany-Verrechnung** , und richten Sie eine Beziehung für USSI und FRSI ein.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Beispiel 2: Erstellen und veröffentlichen Sie eine Intercompany-Arbeitszeittabelle
USSI, die kreditgebende juristische Person, muss die Arbeitszeittabelle für ein Projekt von FRSI, der kreditnehmenden juristischen Person, erstellen und veröffentlichen. Es gibt zwei Einstiegspunkte für die Schritte, die für diese Aufgabe erforderlich sind.

| Schritt | Eingangspunkt                                                                       | Beschreibung                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektmanagement und -buchhaltung** &gt; **Projekte** &gt; **Alle Projekte** | Erstellen einer neuen Zeittabelle. Wählen Sie für die Arbeitszeittabellenposition im Feld **Juristische Person** die juristische Person **FRSI** aus. Wählen Sie im Feld **Projekt-ID** das Projekt in FRSI aus. Geben Sie die Stunden für jeden Wochentag ein. |
| F    | **Arbeitszeitnachweis** -Seite                                                                | Nachdem der Workflow ausgeführt wurde, veröffentlichen Sie die Arbeitszeittabelle und notieren sich die Gutscheinnummer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Beispiel 3: Erstellen und veröffentlichen Sie eine Intercompany-Kreditorenrechnung
USSI, die kreditgebende juristische Person, muss die Intercompany-Kreditorenrechnung für ein Projekt von FRSI, der kreditnehmenden juristischen Person, erstellen und veröffentlichen. Diese Lieferantenrechnung stellt die ausgelagerten Arbeitskräfte und Kosten dar, die von Lieferanten geleistet wurden, die von USSI bezahlt werden. Es gibt zwei Einstiegspunkte für die Schritte, die für diese Aufgabe erforderlich sind.

| Schritt | Eingangspunkt                                                                                      | Beschreibung                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditorenkonten** &gt; **Rechnungen** &gt; **Kreditorenrechnungen öffnen** &gt; **Neue Kreditorenrechnung** | Erstellen Sie eine neue Kreditorenrechnung und geben Sie die Services ein, die im Auftrag des FRSI-Projekts beschafft wurden.                                                                                                                                                                                  |
| F    | Die **Kreditorenrechnung** -Seite                                                                      | Geben Sie im Namen von FRSI Positionen ein, die die ausgelagerten Dienste darstellen. Geben Sie auf dem Inforegister **Positionsdetails** auf der **Projekt** -Registerkarte für die Rechnungsposition im **Projektunternehmen** -Feld **FRSI** ein. Geben Sie das Projekt und die entsprechenden Informationen ein. Buchen Sie dann die Kreditorenrechnung. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Beispiel 4: Erstellen und veröffentlichen Sie eine Intercompany-Rechnung
USSI, die kreditgebende juristische Person, muss die Intercompany-Rechnung erstellen und buchen. Es gibt zwei Einstiegspunkte für die Schritte, die für diese Aufgabe erforderlich sind.

| Schritt | Eingangspunkt                                                                                             | Beschreibung                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektmanagement und Buchhaltung** &gt; **Projektrechnungen** &gt; **Intercompany-Kundenrechnung**  | Klicken Sie auf **Neu** , um die **Intercompany-Rechnung erstellen** -Seite zu öffnen.                                                                                  |
| F    | **Projektmanagement und Buchhaltung** &gt; **Projektrechnungen** &gt; **Intercompany-Kundenrechnungen** | Geben Sie auf der Seite **Intercompany-Rechnung erstellen** die juristische Person ein, geben Sie die Transaktion an, die einbezogen werden soll, und klicken Sie dann auf **Suche**. |
| C    | **Projektmanagement und Buchhaltung** &gt; **Projektrechnungen** &gt; **Intercompany-Kundenrechnungen** | Wählen Sie die zu berechnenden Transaktionen aus, oder klicken Sie auf **Alle auswählen** , um alle Transaktionen in der Liste in Rechnung zu stellen, und klicken Sie dann auf **OK**.                  |
| D    | Die **Intercompany-Rechnung** -Seite                                                                       | Der Intercompany-Kundenrechnungsvorschlag wird angezeigt.                                                                                             |
| E    | Die **Intercompany-Rechnung** -Seite                                                                       | Klicken Sie auf **Buchen**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Beispiel 5: Buchen Sie die Lieferantenrechnung und stellen Sie dem Kunden eine Rechnung
Wenn die kreditgebende juristische Person USSI die Intercompany-Kundenrechnung bucht, wird in der kreditnehmenden juristischen Person FRSI eine übereinstimmende ausstehende Lieferantenrechnung erstellt. Nachdem diese Lieferantenrechnung gebucht wurde, stellt FRSI dem Projektkunden auch die von USSI eingegebenen Stunden in Rechnung. Es gibt drei Einstiegspunkte für die Schritte, die für diese Aufgabe erforderlich sind.

| Schritt | Eingangspunkt                                                                                        | Beschreibung                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Kreditorenkonten** &gt; **Rechnungen** &gt; **Ausstehende Kreditorenrechnungen**                            | Überprüfen Sie die Rechnung, um sicherzustellen, dass die Arbeitszeittabellenwerte enthalten sind, und buchen Sie dann die Lieferantenrechnung.                  |
| F    | **Projektmanagement und Buchhaltung** &gt; **Projektrechnungen** &gt; **Projektrechnungsvorschläge** | Erstellen Sie eine neue Projektrechnung für das Projekt, und überprüfen Sie, ob die gebuchten Stundenvorgänge angezeigt werden.            |
| C    | Die **Projektrechnung** -Seite                                                                       | Wählen Sie die Projektrechnung aus, und klicken Sie dann auf **Details anzeigen** , um die Kosten und den Verkaufsbetrag zu überprüfen. Buchen Sie dann die Rechnung. |


Weitere Informationen finden Sie unter [Konfigurieren Sie die Intercompany-Projektabrechnung](tasks/configure-intercompany-project-invoicing.md).


