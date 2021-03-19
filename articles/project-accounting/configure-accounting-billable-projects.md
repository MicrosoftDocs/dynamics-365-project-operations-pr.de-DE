---
title: Buchhaltung für fakturierbare Projekte konfigurieren
description: Dieses Thema enthält Informationen zu den Buchhaltungsoptionen für abrechnungsfähige Projekte.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4398ef44d4211a2921270bebe38fc92f18503854
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287642"
---
# <a name="configure-accounting-for-billable-projects"></a>Buchhaltung für fakturierbare Projekte konfigurieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt verschiedene Abrechnungsoptionen für abrechnungsfähige Projekte, einschließlich Zeit-, Material- und Festpreistransaktionen.

- **Zeit- und Materialtransaktionen**: Diese Transaktionen werden im Verlauf der Arbeiten basierend auf dem Verbrauch von Stunden, Ausgaben, Artikeln oder Gebühren für das Projekt in Rechnung gestellt. Diese Transaktionskosten können mit den Einnahmen aus jeder Transaktion abgeglichen werden, und das Projekt wird im Verlauf der Arbeiten in Rechnung gestellt. Projekteinnahmen können auch zum Zeitpunkt der Transaktion abgegrenzt werden. Während der Rechnungsstellung werden Umsatzerlöse erfasst und gegebenenfalls aufgelaufene Umsatzerlöse aufgelöst.
- **Festpreistransaktionen**: Diese Transaktionen werden nach einem Abrechnungsplan in Rechnung gestellt, der auf dem Projektvertrag basiert. Umsatz aus Festpreistransaktionen können bei Rechnungsstellung entsprechend der **Vertrag abgeschlossen**- oder **Abgeschlossener Anteil**-Methoden erfasst oder entsprechend berechnet und periodisch gebucht werden.

Ein Projekt gilt als abrechnungsfähig, wenn es einer oder mehreren Vertragszeilen zugeordnet sind. Eine Projektvertragszeilen definiert für sich selbst, welche Abrechnungsmethode und Transaktionstypen zulässig sind.

Beispielsweise hat Fabrikam Robotics einen Projektvertrag mit der Adatum Corporation zur Geräteoptimierung gewonnen. Adatum zahlt einen festen Betrag von 10.000 USD zur Deckung der angefallenen Projektkosten. Dies ist eine Festpreis-Abrechnungsmethode. Projektzeit und Gebühren werden pro Nutzung in Rechnung gestellt. Dies ist eine Fakturierungsmethode für Zeit- und Materialtransaktionen. Alle Arbeiten werden unter einem einzigen Projekt namens Adatum Equipment Optimization verfolgt.

Ein Mitglied des Projektteams legt acht Stunden Arbeit für das Adatum-Projekt zur Geräteoptimierung vor. Wenn der Projektmanager diese Zeit genehmigt, verwendet das System die Zeit- und Materialabrechnungsmethode, um tatsächliche Transaktionen, eine Rechnung und ein Konto zu erstellen. Diese Transaktion wird nicht in die Berechnung der Festpreisumsatzschätzung einbezogen.

Ein anderes Mitglied des Projektteams reicht Reisekosten für 2.000,00 USD für das Adatum-Projekt zur Geräteoptimierung ein. Wenn der Projektmanager diese Einreichung genehmigt, verwendet das System Festpreisabrechnungsmethode, um tatsächliche Transaktionen und ein Konto für diese Projektausgaben zu erstellen. Dem Kunden wird aufgrund dieser Transaktion nichts in Rechnung gestellt. Stattdessen werden sie mithilfe separat konfigurierter Abrechnungsmeilensteine fakturiert. Diese Ausgabentransaktion zusammen mit den Ausgabenschätzungen werden in die Berechnung der Festpreisumsatzschätzung einbezogen.

Die Rechnungslegungsgrundsätze für Projekttransaktionen sind in den Projektkosten- und Ertragsprofilen definiert. Für jede Projekttransaktion ermittelt das System das entsprechende Projektkosten- und Ertragsprofil anhand der konfigurierten Projektkosten- und Ertragsprofilregeln.

## <a name="define-project-cost-and-revenue-profiles"></a>Definieren der Projektkosten- und Umsatzprofile 

Projektkosten und Umsatzprofile bestimmen die Buchhaltungsregeln für Projekttransaktionen. Diese Profile werden in Projektmanagement und Buchhaltung konfiguriert. 

Führen Sie die folgenden Schritte aus, um ein neues Projektkosten- und Umsatzprofil zu erstellen. 

1. Wechseln Sie zu **Projektmanagement und Buchhaltung** > **Einrichtung** > **Buchung** > **Projektkosten- und Umsatzprofile**. 
2. Wählen Sie **Neu**, um ein neues Projektkosten- und Umsatzprofil zu erstellen.
3. In dem **Name**-Feld geben Sie den Namen und eine kurze Beschreibung des Profils ein.
4. In dem **Abrechnungsmethode**-Feld wählen Sie **Zeit und Material** oder **Festpreis** aus.
5. Erweitern Sie das Inforegister **Ledger**. Die Felder auf dieser Registerkarte definieren die Rechnungslegungsgrundsätze, die verwendet werden, wenn Projekttransaktionen mithilfe des Project Operations-Integrationsjournals protokolliert und dann über den Projektrechnungsvorschlag in Rechnung gestellt werden.
6. Wählen Sie die entsprechenden Informationen in die folgenden Feldern im Inforegister **Ledger** aus.

    - **Kosten buchen – Stunde**:

       - *Kein Ledger*: Die Kosten für Zeittransaktionen werden nicht in das Ledger gebucht, wenn die Project Operations-Integration-Erfassung gebucht wird. Der Buchhalter kann jedoch zu einem späteren Zeitpunkt Kosten über die Funktion „Kosten buchen“ buchen.
       - **Saldo**: Die Kosten für Zeittransaktionen werden dem Ledger-Kontotyp *WIP – Kostenwert* belastet dem *Lohn- und Gehaltsabrechnungskonto* in der Ledger-Buchungs-Einrichtung gutgeschrieben. Der Buchhalter verwendet die Funktion „Kosten buchen“, um diese Kosten regelmäßig von einem Saldokonto auf ein Gewinn- und Verlustkonto zu verschieben.
       - **Gewinn- und Verlust**: Beim Buchen des Project Operations-Integrationsjournals werden die Zeittransaktionskosten dem Ledger-Kontotyp *Kosten* belastet und dem *Lohn- und Gehaltsabrechnungskonto* das, auf der **Kosten**-Registerkarte auf der **Einrichtung der Hauptbuchbuchung**-Seite (**Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Buchung** \> **Einrichtung der Hauptbuchbuchung**) definiert ist, gutgeschrieben. Dies ist die häufigste Einrichtung für Zeit- und Materialtransaktionen.
        - *Niemals Ledger* : Die Kosten für Zeittransaktionen werden niemals in das Ledger gebucht.

    - **Kosten buchen – Ausgaben**:

         - **Saldo** : Beim Buchen des Project Operations-Integrationsjournals werden die Ausgabentransaktionskosten dem Ledger-Kontotyp *WIP – Kostenwert* belastet, wie auf der **Kosten**-Registerkarte auf der **Einrichtung der Ledger-Buchung**-Seite definiert, und dem Offset-Konto in der Journalzeile gutgeschrieben. Standard-Offset-Konten für Ausgaben sind in **Projektmanagement und Buchhaltung** > **Einrichtung** \> **Buchung** \> **Standard-Offset-Konto für Ausgaben** definiert. Der Buchhalter verwendet die Funktion **Kosten buchen**, um diese Kosten regelmäßig aus dem Saldokonto auf ein Gewinn- und Verlustkonto zu verschieben.
        - **Gewinn und Verlust** : Beim Buchen des Project Operations-Integrationsjournals werden die Ausgabentransaktionskosten dem Ledger-Kontotyp *Kosten* belastet, wie auf der **Kosten**-Registerkarte auf der **Einrichtung der Ledger-Buchung**-Seite definiert, und dem Offset-Konto in der Journalzeile gutgeschrieben. Standard-Offset-Konten für Ausgaben sind in **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Buchung** \> **Standard-Offset-Konto für Ausgaben** definiert.
       
    - **Auf-Konto-Rechnungsstellung**:

        - **Saldo**: Beim Buchen des Projektrechnungsvorschlags wird dem Ledger-Kontotyp *WIP abgerechnet – auf Rechnung* eine Kontotransaktion (ein Abrechnungsmeilenstein) gutgeschrieben, wie auf der **Umsatz**-Registerkarte auf der **Einrichtung der Ledger-Buchbuchung**-Seite definiert, und dem Kundensaldokonto belastet.
         - **Gewinn und Verlust**: Beim Buchen des Projektrechnungsvorschlags wird dem Ledger-Kontotyp *Abgerechneter Umsatz – auf Rechnung* eine Kontotransaktion (ein Abrechnungsmeilenstein) gutgeschrieben, wie auf der **Umsatz**-Registerkarte auf der **Einrichtung der Ledger-Buchbuchung**-Seite definiert, und dem Kundensaldokonto belastet. Debitorenausgleichskonten werden in **Debitorenkonten** \> **Einrichtung** \> **Debitorenbuchungsprofile** definiert.

   Wenn Sie die Buchungsprofile für Zeit- und Materialabrechnungsmethoden definieren, haben Sie die Möglichkeit, Einnahmen pro Transaktionstyp (Stunde, Aufwand und Gebühr) zu erzielen. Wenn die **Einnahmen erzielen**-Option auf **Ja** festgelegt ist, werden nicht abgerechnete Verkaufstransaktionen in der Project Operations Integration-Erfassung im Ledger erfasst. Der Verkaufswert wird dem **WIP – Verkaufswertkonto** belastet und dem **Aufgelaufene Einnahmen – Verkaufswert**-Konto gutgeschrieben, das auf dem **Einrichtung der Ledger-Buchbuchung**-Seite auf der **Umsatz**-Registerkarte eingerichtet wurde. 
  
  > [!NOTE]
  > Die Option **Einnahmen erzielen** ist nur verfügbar, wenn der jeweilige Transaktionstyp **Kosten** auf die Gewinn- und Verlustrechnung gebucht wird.
    
7. Erweitern Sie das Inforegister **Schätzung**. Die Felder auf dieser Registerkarte definieren die Berechnungseinstellungen für Schätzungen der Festpreisumsätze. Die Felder auf dieser Registerkarte gelten nur für Projektkosten- und Ertragsprofile mit einer Abrechnungsmethode von **Festpreis**.
8. Wählen Sie die entsprechenden Informationen in die folgenden Feldern im Inforegister **Schätzung** aus.

    - **Prinzip für Projektabschlusskalkulationen**:

        - **Abgeschlossener Vertrag**: Kostenabgleich und Umsatzrealisierung erfolgen erst am Ende des Projekts. Die Kosten werden bis zum Abschluss des Projekts als WIP in der Bilanz ausgewiesen.
        - **Abgeschlossener Anteil**: Der aufgelaufene Umsatz wird berechnet und in jedem Zeitraum auf der Grundlage des Projektabschlussprozentsatzes im Hauptbuch gebucht. Es stehen mehrere Methoden zur Berechnung der prozentualen Fertigstellung zur Verfügung. Diese Methoden können je nach Konfiguration automatisch oder manuell erfolgen.
        - **Kein WIP** : Dieses Einrichtung wird für Festpreisprojekte mit kurzer Zeitspanne verwendet, bei denen die Rechnung und die Kosten im selben Zeitraum anfallen. In diesem Fall wird der **Rechnungsstellung auf Rechnung**-Feldwert im Inforegister **Ledger** automatisch auf **Gewinn- und Verlust** festgelegt, um sicherzustellen, dass der Umsatz bei der Rechnungsstellung erfasst wird. Der Umsatzschätzungsprozess wird für dieses Projektkosten- und Umsatzprofil nicht verwendet.

    - **Abgleichungsprinzip**: In diesem Feld wird festgelegt, wie der berechnete Verkaufswert (aufgelaufene Einnahmen) in das Ledger gebucht wird.

        - Mit dem **Verkaufswert**-Prinzip berechnet das System den Verkaufswert, indem Kosten und Einnahmen abgeglichen und dann als Einzelbetrag gebucht werden.
        - Mit dem **Produktion und Gewinn**-Prinzip teilt das System den Verkaufswert in realisierte Kosten und berechneten Gewinn auf. Diese werden separat gebucht.

    - **Kostenvorlagen**: Ermöglichen die Gruppierung von Projekttransaktionen basierend auf Transaktionstyp und Projektkategorie und definieren Berechnungsregeln für die prozentuale Fertigstellung für diese Gruppen.
    - **Periodencodes**: Definieren Sie die Häufigkeit, mit der Umsatzschätzungen für ein bestimmtes Projektkosten- und Umsatzprofil berechnet werden.
    - **Kategorien für die Schätzung** : Wird für die Buchung des Verkaufswerts (aufgelaufener Umsatz) in Projekttransaktionen verwendet. Konfigurieren Sie zunächst die dedizierte Projektkategorie für einen **Gebühr**-Transaktionstyp und legen Sie dann das Flag **Schätzen** für diese Projektkategorie fest. Wählen Sie als Nächstes abhängig vom ausgewählten Abgleichungsprinzip diese Projektkategorie im **Vertrieb**-Wert oder dem **Profit**-Feld im Projektkosten- und Ertragsprofil fest.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Beispielkonfigurationen für Projektkosten- und Umsatzprofile

Zeit und Materialien - kein WIP

![Kosten- und Umsatzprofil: Zeit und Material – kein WIP](media/time-material-no-wip.png)

Zeit und Material – WIP (Umsatz)

![Kosten- und Umsatzprofil: Zeit und Material – WIP](media/time-material-with-wip.png)

Festpreis – Kein WIP

![Kosten- und Umsatzprofil: Festpreis – kein WIP](media/fixed-price-no-wip.png)

Festpreis – abgeschlossener Vertrag

![Kosten- und Umsatzprofil: Festpreis – abgeschlossener Vertrg](media/fixed-price-completed-contract.png)

Festpreis – prozentuale Fertigstellung

![Kosten- und Umsatzprofil: Festpreis – prozentuale Fertigstellung](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Buchführungsereignissbeispiele für Beispielprojektkosten- und Umsatzprofile.

| Buchhaltungsereignis                  | Zeit und Materialien – Kein WIP                       | Zeit und Materialien – WIP                                                                                           | Festpreis – Kein WIP                                            | Festpreis – abgeschlossener Vertrag                                                                            | Festpreis – prozentuale Fertigstellung                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Journalisierung von Zeittransaktionen    | Belastung – Kosten <br>Gutschrift – Lohnzuweisung          | Belastung – Kosten <br>Gutschrift – Lohnzuweisung <br>Belastung – WIP Verkaufswert <br>Gutschrift – aufgelaufener Umsatz aus Verkaufswert                | Belastung – Kosten <br>Gutschrift – Lohnzuweisung                         | Belastung – Kosten <br>Gutschrift – Lohnzuweisung                                                                    | Belastung – Kosten <br>Gutschrift – Lohnzuweisung                       |
| Journalisierung von Ausgabentransaktionen | Belastung – Kosten <br>Gutschrift – Gegenkonto für Ausgaben | Belastung – Kosten <br>Gutschrift – Gegenkonto für Ausgaben <br>Belastung – WIP-Verkaufswert <br>Gutschrift – aufgelaufener Umsatz aus Verkaufswert      | Belastung – Kosten <br>Gutschrift – Gegenkonto für Ausgaben                 | Belastung – Kosten<br> Gutschrift – Gegenkonto für Ausgaben                                                            | Belastung – Kosten <br>Gutschrift – Gegenkonto für Ausgaben               |
| Rechnungsstellung Kunde                | Belastung – Kundenguthaben <br>Gutschrift - Rechnungsumsatz | Belastung – Kundenguthaben <br>Gutschrift – Rechnungsumsatz <br>Gutschrift – WIP-Verkaufswert Belastung – Aufgelaufener Umsatz Verkaufswert | Belastung – Kundenguthaben <br>Gutschrift – Rechnungsumsatz – auf Rechnung | Belastung – Kundenguthaben <br>Gutschrift – WIP – Rechnungsstellung auf Rechnung                                                  | Belastung – Kundenguthaben <br>Gutschrift – WIP – Rechnungsstellung auf Rechnung    |
| Geschätzter Buchungsumsatz             | Nicht verfügbar                                   | Nicht verfügbar                                                                                                    | Nicht zutreffend                                                  | Belastung – WIP-Kostenwert <br>Guthaben – Kosten                                                                         | Belastung – WIP – Verkaufswert <br>Gutschrift – aufgelaufener Umsatz aus Verkaufswert |
| Entfernen                         | Nicht verfügbar                                   | Nicht verfügbar                                                                                                    | Nicht zutreffend                                                  | Gutschrift – WIP-Kostenwert <br>Belastung – Kosten <br>Gutschrift – aufgelaufener Umsatz aus Verkaufswert <br>Belastung – WIP Rechnungsstellung auf Rechnung | Belastung – WIP – Rechnungsstellung auf Rechnung <br>Belastung – WIP-Verkaufswert     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projektkosten- und Umsatzprofilregeln konfigurieren

Die Regeln für Projektkosten- und Umsatzprofile bestimmen das Projektkosten- und Ertragsprofil, das bei der Verarbeitung abrechnungsfähiger Projekttransaktionen verwendet werden muss. Definieren Sie die Regeln unter **Projektmanagement und Buchhaltung** \> **Einrichtung** \> **Buchung** \> **Regeln für das Projektkosten- und Ertragsprofil**.

Regeln können durch Projektvertrag, Projektgruppe oder durch ein bestimmtes Projekt definiert werden. Das System wählt immer zuerst die Regel mit der höchsten Granularität aus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]