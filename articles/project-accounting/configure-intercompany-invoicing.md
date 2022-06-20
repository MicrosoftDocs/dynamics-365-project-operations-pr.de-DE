---
title: Intercompany-Rechnungsstellung konfigurieren
description: Dieser Artikel enthält Informationen und Beispiele zur Konfiguration der Intercompany Rechnungen für Projekte.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929359"
---
# <a name="configure-intercompany-invoicing"></a>Intercompany-Rechnungsstellung konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Führen Sie die folgenden Schritte aus, um die Intercompany-Rechnungsstellung für Projekte in Dynamics 365 Project Operations einzurichten. Intercompany-Transaktionen sind Zeit- und Kostentransaktionen aus einem Projektvertrag, die zu einem Unternehmen oder einer Organisationseinheit gehören, während die Ressourcen im Projektvertrag Teil eines anderen Unternehmens oder einer anderen Organisationseinheit sind.

## <a name="example-configure-intercompany-invoicing"></a>Beispiel: Intercompany-Rechnungsstellung konfigurieren

Im folgenden Beispiel ist Contoso Robotics USA (USPM) die kreditnehmende juristische Person und Contoso Robotics UK (GBPM) die kreditgebende juristische Person. 

1. **Konfigurieren Sie die Intercompany-Buchhaltung zwischen juristischen Personen**. Jedes Paar juristischer Personen, die Kredite aufnehmen oder geben, muss auf der Hauptbuchseite [Intercompany-Buchhaltung](/dynamics365/finance/general-ledger/intercompany-accounting-setup) konfiguriert werden.
    
    1. Gehen Sie in Dynamics 365 Finance zu **Hauptbuch** > **Buchungseinrichtung** > **Intercompany-Buchhaltung**. Erstellen Sie einen Datensatz mit den folgenden Informationen:

        - **Ausgangsunternehmen** = **GBPM**
        - **Zielunternehmen** = **USPM**

2. **Konfigurieren Sie die Handelsbeziehung zwischen juristischen Personen**. Der Debitorendatensatz, der die kreditnehmende juristische Person darstellt, muss in der kreditgebenden juristischen Person erstellt werden. Der Kreditorendatensatz, der die kreditgebende juristische Person darstellt, muss in der kreditnehmenden juristischen Person erstellt werden.

     1. Wählen Sie in Finance die juristische Person **GBPM** aus.
     2. Wechseln Sie zu **Debitorenkonten** > **Debitor** > **Alle Debitoren**. Erstellen Sie einen neuen Datensatz für die juristische Person **USPM**.
     3. Erweitern Sie **Name**, filtern Sie die Datensätze nach **Typ** und wählen Sie **Juristische Personen**. 
     4. Suchen Sie den Debitorendatensatz für **Contoso Robotics USA (USPM)** und wählen Sie ihn aus.
     5. Wählen Sie **Übereinstimmung verwenden** aus. 
     6. Wählen Sie die Kundengruppe **50 – Konzerninterne Kunden** und speichern Sie dann den Datensatz.
     7. Wählen Sie die juristische Person **USPM** aus.
     8. Wechseln Sie zu **Kreditorenkonten** > **Kreditoren** > **Alle Kreditoren**. Erstellen Sie einen neuen Datensatz für die juristische Person **GBPM**.
     9. Erweitern Sie **Name**, filtern Sie die Datensätze nach **Typ** und wählen Sie **Juristische Personen**. 
     10. Suchen Sie den Debitorendatensatz für **Contoso Robotics UK (GBPM)** und wählen Sie ihn aus.
     11. Wählen Sie **Übereinstimmung verwenden**, wählen Sie die Kreditorengruppe aus und speichern Sie den Datensatz.
     12. Wählen Sie im Kreditorendatensatz **Allgemein** > **Einrichten** > **Intercompany** aus.
     13. Auf der **Handelsbeziehung**-Registerkarte legen Sie **Aktiv** auf **Ja** fest.
     14. Setzen Sie das Feld **Kundenfirma** auf **GBPM** und wählen Sie in **Mein Kontodatensatz** den Kundendatensatz aus, den Sie zuvor in der Prozedur erstellt haben.

3. **Konfigurieren Sie Intercompany-Einstellungen in den Projektmanagement- und Buchhaltungsparametern**. 

    1. Wählen Sie die juristische Person **USPM** aus und gehen Sie zu **Projektmanagement und Buchhaltung** > **Einrichtung** > **Projektmanagement- und Buchhaltungsparameter**.
    2. Auf der **Intercompany**-Registerkarte wählen Sie die Beschaffungskategorie aus, die den automatisch generierten Kreditorenrechnungen entspricht.
    3. Wählen Sie unter **Standardkategorie** **Intercompany-Ressourcen**.
    4. Wählen Sie die juristische Person **GBPM** aus und gehen Sie zu **Projektmanagement und Buchhaltung** > **Einrichtung** > **Projektmanagement- und Buchhaltungsparameter**.
    5. Auf der **Intercompany**-Registerkarte wählen Sie eine Standardprojektkategorie für jeden Transaktionstyp aus. Projektkategorien werden für die Steuerkonfiguration verwendet, wenn die Rechnungskategorie in Intercompany-Transaktionen nur in der kreditnehmenden juristischen Person vorhanden ist. Sie können festlegen, dass Einnahmen für Intercompany-Transaktionen anfallen. Die Abgrenzung erfolgt, wenn die Transaktionen über das Project Operations-Integrationsjournal in der kreditgebenden juristischen Person gebucht werden. Das Journal wird storniert, wenn die Intercompany-Rechnung gebucht wird.
    6. Wählen Sie in der Gruppe **Beim Ausleihen von Ressourcen** **...** > **Neu** aus. 
    7. Wählen Sie im Raster die folgenden Informationen aus:

          - **Kreditnehmende juristische Person** = **USPM**
          - **Einnahmen erzielen** = **Ja**
          - **Standardkategorie der Arbeitszeittabelle** = **Standard – Stunde**
          - **Standardkostenkategorie** = **Standard – Aufwand**

4. **Legen Sie im Ledger-Buchungssetup Intercompany-Kosten- und Ertragskonten fest**. Das Intercompany-Ertragskonto wird gutgeschrieben, wenn die Intercompany-Kundenrechnung in der kreditgebenden juristischen Person gebucht wird. Das Intercompany-Kostenkonto wird belastet, wenn die passende ausstehende Kreditorenrechnung in der kreditnehmenden juristischen Person gebucht wird. Diese Konten werden in entsprechenden juristischen Personen eingerichtet. 
      
     1. Wählen Sie in Finance die kreditnehmende juristische Person **USPM** aus. 
     2. Wechseln Sie zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Buchung** > **Sachkontobuchungseinstellungen**. 
     3. Wählen Sie auf der **Kostenkonten**-Registerkarte in **Sachkontenart** **Intercompany-Kosten** aus. Erstellen Sie einen neuen Datensatz mit den folgenden Informationen:
      
        - **Kreditgebende juristische Person** = **GBPM**
        - **Hauptkonto** = Wählen Sie das Hauptkonto für die konzerninternen Kosten aus. Diese Einrichtung ist erforderlich. Das Setup wird für konzerninterne Flows im Finanzwesen verwendet, nicht jedoch für projektbezogene konzerninterne Flows. Diese Auswahl hat keine nachgelagerten Auswirkungen. 
        
     4. Wählen Sie die kreditgebende juristische Person **GBPM** aus. 
     5. Wechseln Sie zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Buchung** > **Sachkontobuchungseinstellungen**. 
     6. Wählen Sie auf der **Umsatzerlöskonten**-Registerkarte in **Sachkontenart** **Intercompany-Einnahmen** aus. Erstellen Sie einen neuen Datensatz mit den folgenden Informationen:

        - **Kreditnehmende juristische Person** = **USPM**
        - **Hauptkonto** = Wählen Sie das Hauptkonto für die konzerninternen Umsätze .aus Diese Einrichtung ist erforderlich. Das Setup wird für konzerninterne Flows im Finanzwesen verwendet, nicht jedoch für projektbezogene konzerninterne Flows. Diese Auswahl hat keine nachgelagerten Auswirkungen. 

5. **Richten Sie Verrechnungspreise für Arbeitskräfte ein**. Die Intercompany-Verrechnungspreisgestaltung wird in Project Operations auf Dataverse konfiguriert. Konfigurieren Sie [Arbeitskostensätze](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) und [Lohnkosten](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) für die Intercompany-Rechnungsstellung. Verrechnungspreise werden für Intercompany-Aufwandsbuchungen nicht unterstützt. Der organisationsübergreifende Einheitspreis wird immer auf den gleichen Wert wie der Ressourcenstückkostenpreis festgelegt.

      Die Kosten für Entwicklerressourcen in Contoso Robotics UK betragen 88 GBP pro Stunde. Contoso Robotics UK berechnet Contoso Robotics USA 120 USD für jede Stunde, in der diese Ressource an US-Projekten gearbeitet hat. Contoso Robotics USA wird dem Kunden Adventure Works 200 USD die von der Entwicklerressource Contoso Robotics UK geleistete Arbeit in Rechnung stellen.

      1. In Project Operations auf Dataverse gehen Sie zu **Verkauf** > **Preisliste**. Erstellen Sie eine neue Kostenpreisliste mit dem Namen **Kosten für Contoso Robotics UK.** 
      2. Erstellen Sie in der Kostenpreisliste einen Datensatz mit den folgenden Informationen:
         - **Rolle** = **Entwickler**
         - **Kosten** = **88 GBP**
      3. Gehen Sie zu **Einstellungen** > **Organisationseinheiten** und fügen Sie diese Kostenpreisliste der **Contoso Robotics UK**-Organisationseinheit hinzu.
      4. Gehen Sie zu **Vertrieb** > **Preisliste**. Erstellen Sie eine neue Kostenpreisliste mit dem Namen **Kosten für Contoso Robotics USA.** 
      5. Erstellen Sie in der Kostenpreisliste einen Datensatz mit den folgenden Informationen:
          - **Rolle** = **Entwickler**
          - **Ressourcenzuordnungsunternehmen** = **Contoso Robotics UK**
          - **Kosten** = **120 USD**
      6. Gehen Sie zu **Einstellungen** > **Organisationseinheiten** und fügen Sie die Kostenpreisliste **Kosten für Contoso Robotics USA** der **Contoso Robotics USA**-Organisationseinheit hinzu.
      7. Gehen Sie zu **Vertrieb** > **Preisliste**. Erstellen Sie eine Verkaufspreisliste mit dem Namen **Rechnungssätze für Adventure Works**. 
      8. Erstellen Sie in der Verkaufspreisliste einen Datensatz mit den folgenden Informationen:
          - **Rolle** = **Entwickler**
          - **Ressourcenzuordnungsunternehmen** = **Contoso Robotics UK**
          - **Fakturierungsrate** = **200 USD**
      9. Gehen Sie zu **Vertrieb** > **Projektverträge** und hängen Sie die **Rechnungssätze für Adventure Works**-Preisliste an die Adventure Works-Projektpreisliste des Projektvertrags an.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
