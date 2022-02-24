---
title: Integrationsjournal in Project Operations
description: Dieses Thema enthält Informationen zur Arbeit mit dem Integrationsjournal in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948329"
---
# <a name="integration-journal-in-project-operations"></a>Integrationsjournal in Project Operations

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Zeit- und Kosteneinträge erstellen **Tatsächliche** Transaktionen, die die operative Sicht auf Arbeiten darstellen, die für ein Projekt ausgeführt wurden. Dynamics 365 Project Operations bietet Buchhaltern ein Tool, mit dem sie Transaktionen überprüfen und die Buchhaltungsattribute nach Bedarf anpassen können. Nach Abschluss der Prüfung und Anpassungen werden die Transaktionen in das untergeordnete Sachkonto und die Finanzbuchhaltung des Projekts gebucht. Ein Buchhalter kann diese Aktivitäten mit dem ausführen **Project Operations-Integrationsjournal** (**Dynamics 365 Finance** > **Projektmanagement und Buchhaltung** > **Journale** > **Project Operations-Integrationsjournal**) ausführen.

![Flow des Integrationsjournals](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Datensätze im Project Operations-Integrationsjournal erstellen

Datensätze im Project Operations-Integrationsjournal werden in regelmäßigen Abständen per **Import aus Stagingtabelle** erstellt. Sie können diesen Vorgang ausführen, indem Sie auf **Dynamics 365 Finance** > **Projektmanagement und Buchhaltung** > **Periodisch** > **Project Operations-Integration** > **Import aus Stagingtabelle** gehen. Sie können den Prozess interaktiv ausführen oder den Prozess so konfigurieren, dass er nach Bedarf im Hintergrund ausgeführt wird.

Wenn der periodische Prozess ausgeführt wird, werden alle Aktualisierungen gefunden, die noch nicht zum Project Operations-Integrationsjournal hinzugefügt wurden. Für jede tatsächliche Transaktion wird eine Buchungsblattzeile erstellt.
Das System gruppiert Journalzeilen basierend auf dem im **Periodeneinheit im Project Operations Integration-Journal** ausgewählten Wert (**Finance** > **Projektmanagement und Buchhaltung** > **Einrichtung** > **Projektmanagement- und Buchhaltungsparameter**, **Project Operations in Dynamics 365 Customer Engagement**-Registerkarte) in separate Journale. Mögliche Werte für dieses Feld sind:

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
    - Wenn **Transaktionskategorie** nicht im aktuellen Projekt festgelegt ist, verwendet das System den Wert im **Standardeinstellungen für Projektkategorien**-Feld auf der **Project Operations in Dynamics 365 Customer Engagement**-Registerkarte auf der **Projektmanagement- und Buchhaltungsparameter**-Seite.
  - Das Feld **Ressource** repräsentiert die Projektressource für diese Transaktion. Die Ressource wird als Referenz in Projektrechnungsvorschlägen an Kunden verwendet.
  - Das Feld **Wechselkurs** nutzt die Standardeinstellungen aus dem **Wechselkurs** in Dynamics 365 Finance. Wenn die Wechselkurseinstellung fehlt, fügt der regelmäßige Prozess **Import aus Staging** keinen Datensatz zu einem Journal hinzu, und dem Jobausführungsprotokoll wird eine Fehlermeldung hinzugefügt.
  - Das Feld **Zeileneigenschaft** repräsentiert den Fakturierungstyp in den Projektdaten. Die Zuordnung von Zeileneigenschaft und Fakturierungstyp ist auf der **Project Operations in Dynamics 365 Customer Engagement**-Registerkarte auf der **Projektmanagement- und Buchhaltungsparameter**-Seite definiert.

In den Project Operations-Integrationsjournalzeilen können nur die folgenden Abrechnungsattribute aktualisiert werden:

- **Fakturierungs-Mehrwertsteuergruppe** und **Fakturierungs-Artikel-Mehrwertsteuergruppe**.
- **Finanzielle Dimensionen** (mit der Aktion **Beträge verteilen**)

Integrationsjournalzeilen können gelöscht werden. Nicht gebuchte Zeilen werden jedoch erneut in das Journal eingefügt, nachdem Sie den periodischen Prozess **Import aus Staging** erneut ausgeführt haben.

Wenn Sie das Integrationsjournal buchen, werden ein untergeordnetes Sachkonto und Finanzbuchhaltungsvorgänge erstellt. Diese werden in der nachgelagerten Kundenabrechnung, Umsatzrealisierung und Finanzberichterstattung verwendet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]