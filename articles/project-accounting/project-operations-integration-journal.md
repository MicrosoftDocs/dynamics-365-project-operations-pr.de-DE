---
title: Integrationsjournal in Project Operations
description: Dieser Artikel informiert Sie über die Arbeit mit dem Erfassungsjournal Integration in Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106274"
---
# <a name="integration-journal-in-project-operations"></a>Integrationsjournal in Project Operations

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Zeit-, Kosten- und Materialeinträge erstellen **Tatsächliche** Transaktionen, die die operative Sicht auf Arbeiten darstellen, die für ein Projekt ausgeführt wurden. Dynamics 365 Project Operations bietet Buchhaltern ein Tool, mit dem sie Transaktionen überprüfen und die Buchhaltungsattribute nach Bedarf anpassen können. Nach Abschluss der Prüfung und Anpassungen werden die Transaktionen in das untergeordnete Sachkonto und die Finanzbuchhaltung des Projekts gebucht. Ein Buchhalter kann diese Aktivitäten mit folgender Erfassung durchführen **Project Operations-Integration** (**Dynamics 365 Finance** > **Projektmanagement und -buchhaltung** > **Erfassungen** > **Project Operations-Integrationserfassung**

![Flow des Integrationsjournals.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Datensätze im Project Operations-Integrationsjournal erstellen

Datensätze im Project Operations-Integrationsjournal werden in regelmäßigen Abständen per **Import aus Stagingtabelle** erstellt. Sie können diesen Vorgang ausführen, indem Sie zu **Dynamics 365 Finance** > **Projektmanagement und -buchhaltung** > **Periodisch** > **Project Operations-Integration** > **Aus Stagingtabelle importieren** wechseln. Sie können den Prozess interaktiv ausführen oder den Prozess so konfigurieren, dass er nach Bedarf im Hintergrund ausgeführt wird.

Wenn der periodische Prozess ausgeführt wird, werden alle Aktualisierungen gefunden, die noch nicht zum Project Operations-Integrationsjournal hinzugefügt wurden. Für jede tatsächliche Transaktion wird eine Buchungsblattzeile erstellt.
Das System gruppiert Erfassungspositionen basierend auf dem in der Liste ausgewählten Wert im Feld **Periodeneinheit in der Project Operations-Integrationserfassung** (**Finance** > **Projektmanagement und -buchhaltung** > **Einrichtung** > **Projektmanagement- und Buchhaltungsparameter**, **Project Operations in Dynamics 365 Customer Engagement**-Registerkarte). Mögliche Werte für dieses Feld umfassen:

  - **Tage**: Istwerte werden nach Transaktionsdatum gruppiert. Für jeden Tag wird ein separates Journal erstellt.
  - **Monate**: Istwerte werden nach Kalendermonaten gruppiert. Für jeden Monat wird ein separates Journal erstellt.
  - **Jahre**: Istwerte werden nach Kalenderjahren gruppiert. Für jedes Jahr wird ein separates Journal erstellt.
  - **Alle**: Alle tatsächlichen Transaktionen sind im selben Integrationsjournal enthalten. Wenn das Journal während der Ausführung des periodischen Prozesses nicht verfügbar ist, z. B. wenn das Journal gerade Transaktionen bucht, wird ein neues Journal erstellt.

Journalzeilen werden basierend auf Projekt-Istwerten erstellt. Die folgende Liste enthält einige der bemerkenswertesten Standard- und Transformationsregeln:

  - Jede tatsächliche Projekttransaktion hat eine Zeile im Project Operations-Integrationsjournal. Kosten und nicht abgerechnete Verkaufstransaktionen für Zeit und Materialabrechnungsart werden in separaten Zeilen angezeigt.
  - Das **Datum**-Feld steht für das Datum der Transaktion. Das **Abschlussstichtag**-Feld gibt das Datum an, an dem die Transaktion im Hauptbuch erfasst wird. Wenn das Abschlussstichtag in einer [abgeschlossenen Finanzperiode](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) liegt und der Parameter **Abschlussstichtag automatisch so einstellen, dass die Hauptbuchperiode geöffnet wird** auf der **Finanzen**-Registerkarte der Seite **Projektmanagement- und Buchhaltungsparameter** eingestellt ist, passt das System den Abschlussstichtag der Transaktion an das erste Datum in der nächsten offenen Sachkontoperiode an.
  - Das **Beleg**-Feld zeigt die Belegnummer für jede tatsächliche Transaktion. Die Reihenfolge der Belegnummern ist auf der **Nummernsequenzen**-Registerkarte auf der **Projektmanagement- und Buchhaltungsparameter**-Seite definiert. Jeder Zeile wird eine neue Nummer zugewiesen. Nachdem der Beleg gebucht wurde, können Sie durch Auswahl anzeigen, wie Kosten und nicht in Rechnung gestellte Verkaufstransaktionen zusammenhängen, indem Sie **Zugehörige Belege** auf der **Belegbuchung**-Seite auswählen.
  - Das **Kategorie**-Feld stellt eine Projekttransaktion dar und die Standardeinstellungen basieren auf der Transaktionskategorie für das zugehörige aktuelle Projekt.
    - Wenn **Transaktionskategorie** im Projekt-Istwert eingestellt ist und eine verwandte **Projektkategorie** in einer bestimmten juristischen Person existiert, ist die Kategorie standardmäßig diese Projektkategorie.
    - Wenn im Projekt-Ist-Wert keine **Buchungskategorie** zugeordnet ist, verwendet das System den Wert im Feld **Standardwerte für Projektkategorien** auf der Registerkarte **Project Operations bei Dynamics 365 Customer Engagement** auf der Seite **Projektmanagement und Abrechnungsparameter**.
  - Das Feld **Ressource** repräsentiert die Projektressource für diese Transaktion. Die Ressource wird als Referenz in Projektrechnungsvorschlägen an Kunden verwendet.
  - Der Standardwert im Feld **Wechselkurs** ist **Währungswechselkurs**, der in Dynamics 365 Finance festgelegt ist. Wenn die Wechselkurseinstellung fehlt, fügt der regelmäßige Prozess **Import aus Staging** keinen Datensatz zu einem Journal hinzu, und dem Jobausführungsprotokoll wird eine Fehlermeldung hinzugefügt.
  - Das Feld **Zeileneigenschaft** repräsentiert den Fakturierungstyp in den Projektdaten. Positionseigenschaft und Fakturierungstyp werden auf der Registerkarte **Project Operations bei Dynamics 365 Customer Engagement** auf der Seite **Projektmanagement und Abrechnungsparameter** definiert.

In den Project Operations-Integrationsjournalzeilen können nur die folgenden Abrechnungsattribute aktualisiert werden:

- **Fakturierungs-Mehrwertsteuergruppe** und **Fakturierungs-Artikel-Mehrwertsteuergruppe**.
- **Finanzielle Dimensionen** (mit der Aktion **Beträge verteilen**)

Integrationsjournalpositionen können gelöscht werden. Nicht gebuchte Positionen werden jedoch erneut in das Journal eingefügt, nachdem Sie den periodischen Prozess **Import aus Staging** erneut ausgeführt haben.

### <a name="post-the-project-operations-integration-journal"></a>Project Operations-Integrationsjournal buchen

Wenn Sie das Integrationsjournal buchen, werden ein untergeordnetes Sachkonto und Finanzbuchhaltungsvorgänge erstellt. Diese werden in der nachgelagerten Kundenabrechnung, Umsatzrealisierung und Finanzberichterstattung verwendet.

Das ausgewählte Project Operations-Integrationsjournal kann mit **Buchen** auf der Integrationsjournalseite für Project Operations gebucht werden. Alle Journale können automatisch gebucht werden, indem ein Prozess unter **Periodizität** > **Project Operations-Integration** > **Integrationsjournal für Project Operations buchen** ausgeführt wird.

Die Buchung kann interaktiv oder im Batch erfolgen. Beachten Sie, dass alle Journale mit mehr als 100 Positionen automatisch in einem Batch gebucht werden. Sie können bessere Ergebnisse erzielen, wenn Sie für Journale, in denen viele Positionen in einem Batch gebucht wurden, aktivieren Sie die Funktion **Integrationsjournal für Project Operations mit mehreren Batch-Aufgaben buchen** im Arbeitsbereich **Feature-Verwaltung**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Übertragen Sie alle Positionen mit Buchungsfehlern in ein neues Journal

> [!NOTE]
> Um diese Funktion zu nutzen, aktivieren Sie das Feature **Alle Zeilen mit Buchungsfehlern in ein neues Project Operations-Integrationsjournal übertragen** im Arbeitsbereich **Feature-Verwaltung**.

Während der Buchung in das Integrationsjournals für Project Operations validiert das System jede Position im Journal. Das System bucht alle fehlerfreien Positionen und erstellt ein neues Journal für alle Positionen mit Buchungsfehlern. Um die Journale mit Buchungsfehlerpositionen zu überprüfen, rufen Sie **Projektmanagement und -buchhaltung** > **Journal** > **Project Operations-Integrationsjournal** auf und filtern Sie die Journale mithilfe des Felds **Ursprüngliches Journal**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
