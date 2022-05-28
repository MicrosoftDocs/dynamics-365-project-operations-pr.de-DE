---
title: Transaktionsverbindungen – Istdaten verschiedener Transaktionstypen verknüpfen
description: In diesem Thema wird erläutert, wie eine Transaktionsverbindung verwendet wird, um Ist-Werte verschiedener Typen zu verknüpfen, um die Rentabilität, den Abrechnungsrückstand und die Berechnung von fakturierten und nicht fakturierten Einnahmen nachzuverfolgen.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580777"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transaktionsverbindungen – Istdaten verschiedener Transaktionstypen verknüpfen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Transaktionsverbindungsdatensätze werden erstellt, um Ist-Werte unterschiedlicher Art zu verknüpfen, wenn sich Zeit, Kosten oder Materialverbrauch in seinem Lebenszyklus von der Angebots- oder Vorverkaufsphase zur Vertragsphase, zu Genehmigungen und/oder Rückrufen, zur Rechnungsstellung und möglicherweise zu Gutschriften oder Korrekturrechnungen bewegen.

Im folgenden Beispiel wird die typische Verarbeitung von Zeiteinträgen im Lebenszyklus eines Project Operations-Projekts veranschaulicht.

> ![Bearbeitung von Zeiteinträgen in Project Operations.](media/basic-guide-17.png)

Die Verarbeitung von Zeiteinträgen im Projektlebenszyklus von Project Operations folgt diesen Schritten: 

1. Die Übermittlung eines Zeiteintrags führt zur Erstellung von zwei Erfassungspositionen: eine für die Kosten und eine für den nicht fakturierten Vertrieb. 
2. Die spätere Genehmigung des Zeiteintrags führt zur Erstellung von zwei Ist-Werten: einer für die Kosten und einer für den nicht fakturierten Vertrieb. Diese 2 Ist-Werte sind über Transaktionsverbindungen verknüpft.
3. Wenn der Benutzer eine Projektrechnung erstellt, wird die Rechnungszeilentransaktion unter Verwendung der Daten aus dem nicht fakturiertem vertrieblichen Ist-Wert erstellt.
4. Wenn die Rechnung bestätigt wird, werden zwei neue Ist-Werte erstellt: eine nicht fakturierte Umsatzumkehrung und ein fakturierter Umsatz-Ist-Wert. Der Storno nicht fakturierter Umsätze und die ursprünglichen nicht fakturierten Verkaufs-Ist-Werte sind über Stornobuchungen verbunden. Die fakturierten Verkäufe und die ursprünglichen nicht fakturierten Verkaufs-Ist-Werte sind ebenfalls verbunden, um die Verknüpfungen zwischen den Einnahmen aus Auftragsrückständen oder unfertigen Arbeiten (WIP) und dem jetzt fakturierten Umsatz aufzuzeigen.   

Jedes Ereignis im Verarbeitungsworkflow löst die Erstellung von Datensätzen in der Tabelle  **Transaktionsverbindung** aus. Dies hilft dabei, eine Ablaufverfolgung des Beziehungen zwischen den Datensätzen zu erstellen, die über Zeiteintrag, Buchungszeile, Ist-Wert und Rechnungszeilendetails erstellt werden.

Die folgende Tabelle enthält die Datensätze in der Entität **Transaktionsverbindung** für den vorangehenden Workflow.

|Ereignis                   |Transaktion 1                 |Rolle Transaktion 1 |Typ Transaktion 1       |Transaktion 2          |Rolle Transaktion 2 |Typ Transaktion 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Übermittlung des Zeiteintrags   |GUID der Erfassungsposition (Vertrieb)     |Nicht fakturierte Umsätze |msdyn_journalline            |GUID der Erfassungsposition (Kosten)     |Kosten            |msdyn_journalline  |
|Genehmigung der Zeit           |GUID des nicht fakturierten Ist-Werts (Umsatz)  |Nicht fakturierte Umsätze |msdyn_actual                 |GUID des Kosten-Istwerts (Kosten)       |Kosten            |msdyn_actual       |
|Rechnungserstellung        |GUID der Rechnungsposition      |Fakturierte Umsätze   |msdyn_invoicelinetransaction |GUID des nicht fakturierten Umsatz-Istwerts   |Nicht fakturierte Umsätze  |msdyn_actual       |
|Rechnungsbestätigung    |GUID des Umkehrens des Ist-Werts         |Umkehren      |msdyn_actual                 |GUID der ursprünglichen nicht fakturierten Umsätze |Original        |msdyn_actual       |
|                        |GUID der Fakturierten Umsätze             |Fakturierte Umsätze   |msdyn_actual                 |GUID des nicht fakturierten Umsatz-Istwerts   |Nicht fakturierte Umsätze  |msdyn_actual       |
|Korrektur des Rechnungsentwurfs |GUID der Rechnungszeilentransaktion|Ersetzen      |msdyn_invoicelinetransaction |GUID der Fakturierten Umsätze            |Original        |msdyn_actual       |
|Bestätigen der Rechnungskorrektur|GUID der Umkehrung der fakturierten Umsätze  |Umkehren      |msdyn_actual                 |GUID der Fakturierten Umsätze            |Original        |msdyn_actual       |
|                        |Neue GUID für nicht fakturierte Umsätze |Ersetzen            |msdyn_actual                 |GUID der Fakturierten Umsätze            |Original        |msdyn_actual       |


Die folgende Abbildung zeigt die Verknüpfungen, die zwischen unterschiedlichen Ist-Typen bei verschiedenen Ereignissen erstellt werden, am Beispiel von Zeiterfassungen in Project Operations.

> ![So werden Ist-Werte unterschiedlicher Typen in Project Operations miteinander verknüpft.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
