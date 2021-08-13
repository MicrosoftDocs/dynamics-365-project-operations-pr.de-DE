---
title: Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen
description: In diesem Thema wird erläutert, wie Istdaten mit Originaldatensätzen wie Zeiterfassung, Kostenerfassung oder Materialnutzungsprotokollen verknüpft werden.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991755"
---
# <a name="link-actuals-to-original-records"></a>Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


In Dynamics 365 Project Operations ist eine *Geschäftstransaktion* ein abstraktes Konzept, das von einer Entität dargestellt wird. Einige häufig verwendete Felder und Prozesse für Entitäten sind jedoch so ausgelegt, dass sie das Konzept von Geschäftstransaktionen verwenden. Die folgenden Entitäten verwenden dieses Konzept:

- Detailinformationen zur Angebotsposition
- Vertragszeilendetails
- Vorkalkulationszeilen
- Erfassungspositionen
- Ist-Werte

Von diesen Entitäten werden **Angebotspositions**- und **Vertragszeilendetails** sowie **Vorkalkulationszeilen** im Projektlebenszyklus der Vorkalkulationsphase zugeordnet. Die Entitäten **Erfassungspositionen** und **Ist-Werte** werden im Projektlebenszyklus der Ausführungsphase zugeordnet.

Project Operations erkennt Datensätze in diesen fünf Entitäten als Geschäftstransaktionen. Die einzige Unterscheidung besteht darin, dass Datensätze in den Entitäten, die zur Vorkalkulationsphase zugeordnet werden, als Finanzprognosen gelten, wohingegen die Datensätze in den Entitäten, die zur Ausführungsphase zugeordnet werden, als bereits eingetretene Finanztatsachen gelten.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Einzigartige Konzepte für Geschäftstransaktionen
Die folgenden Konzepte sind für das Konzept der Geschäftstransaktionen einzigartig:

- Transaktionstyp
- Transaktionsklasse
- Transaktionsursprung
- Transaktionsverbindung

### <a name="transaction-type"></a>Transaktionstyp

Der Transaktionstyp gibt den Zeitpunkt und den Kontext der finanziellen Auswirkungen auf ein Projekt an. Dies wird durch einen Optionssatz dargestellt, der in Project Operations die folgenden unterstützten Werte aufweist:

  - Kosten
  - Projektvertrag
  - Nicht fakturierte Umsätze
  - Fakturierte Umsätze
  - Organisationsübergreifender Umsatz
  - Kosten der Ressourcenzuordnungseinheit

### <a name="transaction-class"></a>Transaktionsklasse

Die Transaktionsklasse repräsentiert die verschiedenen Arten von Kosten, die für Projekte angefallen sind. Dies wird durch einen Optionssatz dargestellt, der in Project Operations die folgenden unterstützten Werte aufweist:

  - Zeit
  - Ausgaben
  - Material
  - Gebühr
  - Meilenstein
  - Steuer

Der Wert **Meilenstein** wird in Project Operations in der Regel von der Geschäftslogik für die Festpreisfakturierung verwendet.

### <a name="transaction-origin"></a>Transaktionsursprung

Der **Buchungsursprung** ist eine Entität, die den Ursprung jeder Geschäftsbuchung speichert. Wenn ein Projekt beginnt, führt jede Geschäftstransaktion zu einer anderen Geschäftstransaktion, die wiederum eine weitere erstellt und so weiter. Die Transaktionsursprungsentität dient zum Speichern von Daten über den Ursprung jeder Transaktion, um die Berichterstellung und Rückverfolgbarkeit zu erleichtern. 

### <a name="transaction-connection"></a>Transaktionsverbindung

Die **Transaktionsverbindung** ist eine Entität, die die Beziehung zwischen zwei ähnlichen Geschäftstransaktionen speichert, z. B. Kosten und zugehörige Umsatz-Istwerte oder Transaktionsumkehrungen, die durch Fakturierungsaktivitäten wie Rechnungsbestätigung oder Rechnungskorrekturen ausgelöst werden.

Mithilfe von **Transaktionsursprung** und **Transaktionsverbindung** können Sie Beziehungen zwischen Geschäftstransaktionen und Aktionen nachverfolgen, die zu einer bestimmten Geschäftstransaktion geführt haben.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Beispiel: So funktioniert Transaktionsursprung mit Transaktionsverbindung

Im folgenden Beispiel wird die typische Verarbeitung von Zeiteinträgen im Lebenszyklus eines Project Operations-Projekts veranschaulicht.

> ![Verarbeitung von Zeiteinträgen in einem Project Service-Lebenszyklus.](media/basic-guide-17.png)
 
1. Die Übermittlung eines Zeiteintrags führt zur Erstellung von zwei Erfassungspositionen: eine für die Kosten und eine für den nicht fakturierten Vertrieb.
2. Die spätere Genehmigung des Zeiteintrags führt zur Erstellung von zwei Ist-Werten: einer für die Kosten und einer für den nicht fakturierten Vertrieb.
3. Wenn der Benutzer eine neue Projektrechnung erstellt, wird die Rechnungszeilentransaktion unter Verwendung der Daten aus dem nicht fakturiertem vertrieblichen Ist-Wert erstellt. 
4. Wenn die Rechnung bestätigt wird, werden zwei neue Ist-Werte erstellt: ein nicht fakturierter Umsatzumkehrungs-Istwert und ein fakturierter Umsatz-Istwert.

Jedes dieser Ereignisse erstellt einen Datensatz in den **Transaktionsursprungs**- und **Transaktionsverbindungs**-Entitäten. Mithilfe dieser neuen Datensätze können Sie einen Verlauf von Beziehungen zwischen den Datensätzen erstellen, die über Zeiteintrag, Journalzeile, Istdaten und Rechnungszeilendetails erstellt werden.

Die folgende Tabelle enthält die Datensätze in der Entität **Transaktionsursprung** für den Workflow.

| Veranstaltung                        | Ursprung                   | Ursprungstyp                       | Transaktion                       | Transaktionstyp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Übermittlung des Zeiteintrags        | GUID des Datensatzes „Zeiteintrag“   | Zeiteintrag                        | GUID des Datensatzes „Erfassungsposition (Kosten)“   | Erfassungsposition             |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Erfassungsposition (Vertrieb)“  | Erfassungsposition                      |                          |
| Genehmigung der Zeit                | GUID des Datensatzes „Erfassungsposition“ | Erfassungsposition                      | GUID des Datensatzes „Nicht fakturierte Umsätze“        | Tatsächlich                   |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Nicht fakturierte Umsätze“        | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID des Datensatzes „Kosten-Istwert“           | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Kosten-Istwert“           | Tatsächl.                            |                          |
| Rechnungserstellung             | GUID des Datensatzes „Zeiteintrag“   | Zeiteintrag                        | GUID der Rechnungszeilentransaktion     | Rechnungszeilentransaktion |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID der Rechnungszeilentransaktion     | Rechnungszeilentransaktion          |                          |
| Rechnungsbestätigung         | GUID der Rechnungsposition        | Rechnungsposition                      | GUID des Datensatzes „Fakturierte Umsätze“          | Tatsächlich                   |
| GUID der Rechnung                 | Rechnung                  | GUID des Datensatzes „Fakturierte Umsätze“          | Tatsächlich                            |                          |
| GUID der Rechnungsposition     | Rechnungsposition      | GUID des Datensatzes „Fakturierte Umsätze“          | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Fakturierte Umsätze“          | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID des Datensatzes „Fakturierte Umsätze“          | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID der Nicht fakturierten Umsatzumkehrung      | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID der Nicht fakturierten Umsatzumkehrung      | Tatsächlich                            |                          |
| Korrektur des Rechnungsentwurfs     | GUID der alten ILD (Rechnungsposition)             | Rechnungszeilentransaktion          | GUID der Korrektur der ILD (Rechnungsposition)               | Rechnungszeilentransaktion |
| GUID der alten IL (Rechnungszeile)                  | Rechnungsposition             | GUID der Korrektur der ILD (Rechnungsposition)               | Rechnungszeilentransaktion          |                          |
| GUID der alten Rechnung             | Rechnung                  | GUID der Korrektur der ILD (Rechnungsposition)               | Rechnungszeilentransaktion          |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID der Korrektur der ILD (Rechnungsposition)               | Rechnungszeilentransaktion          |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID der Korrektur der ILD (Rechnungsposition)               | Rechnungszeilentransaktion          |                          |
| Bestätigte Rechnungskorrektur | GUID der alten ILD (Rechnungsposition)             | Rechnungszeilentransaktion          | GUID des umgekehrten, abgerechneten vertrieblichen Ist-Werts | Tatsächlich                   |
| GUID der alten IL (Rechnungszeile)                  | Rechnungsposition             | GUID des umgekehrten, abgerechneten vertrieblichen Ist-Werts | Tatsächlich                            |                          |
| GUID der alten Rechnung             | Rechnung                  | GUID des umgekehrten, abgerechneten vertrieblichen Ist-Werts | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des umgekehrten, abgerechneten vertrieblichen Ist-Werts | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID des umgekehrten, abgerechneten vertrieblichen Ist-Werts | Tatsächlich                            |                          |
| GUID der alten ILD (Rechnungsposition)                 | Rechnungszeilentransaktion | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID der alten IL (Rechnungszeile)                  | Rechnungsposition             | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID der alten Rechnung             | Rechnung                  | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID der Korrektur der ILD (Rechnungsposition)          | Rechnungszeilentransaktion | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID der IL (Rechnungszeilen)-Korrektur           | Rechnungsposition             | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |
| GUID der Korrekturrechnung      | Rechnung                  | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächlich                            |                          |

Die folgende Tabelle enthält die Datensätze in der Entität **Transaktionsverbindung** für den Workflow.

| Veranstaltung                          | Transaktion 1                 | Rolle Transaktion 1 | Typ Transaktion 1           | Transaktion 2                | Rolle Transaktion 2 | Typ Transaktion 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Übermittlung des Zeiteintrags          | GUID der Erfassungsposition (Vertrieb)     | Nicht fakturierte Umsätze     | msdyn_journalline            | GUID der Erfassungsposition (Kosten)     | Kosten               | msdyn_journalline  |
| Genehmigung der Zeit                  | GUID des nicht fakturierten Ist-Werts (Umsatz)  | Nicht fakturierte Umsätze     | msdyn_actual                 | GUID des Kosten-Istwerts (Kosten)       | Kosten               | msdyn_actual       |
| Rechnungserstellung               | GUID der Rechnungsposition      | Fakturierte Umsätze       | msdyn_invoicelinetransaction | GUID des nicht fakturierten Umsatz-Istwerts   | Nicht fakturierte Umsätze     | msdyn_actual       |
| Rechnungsbestätigung           | GUID des Umkehrens des Ist-Werts         | Umkehren          | msdyn_actual                 | GUID der ursprünglichen nicht fakturierten Umsätze | Original           | msdyn_actual       |
| GUID der Fakturierten Umsätze              | Fakturierte Umsätze                  | msdyn_actual       | GUID des nicht fakturierten Umsatz-Istwerts   | Nicht fakturierte Umsätze               | msdyn_actual       |                    |
| Korrektur des Rechnungsentwurfs       | GUID der Rechnungszeilentransaktion | Ersetzen          | msdyn_invoicelinetransaction | GUID der Fakturierten Umsätze            | Original           | msdyn_actual       |
| Bestätigen der Rechnungskorrektur     | GUID der Umkehrung der fakturierten Umsätze    | Umkehren          | msdyn_actual                 | GUID der Fakturierten Umsätze            | Original           | msdyn_actual       |
| GUID des Neuen nicht fakturierten Umsatz-Istwerts | Ersetzen                     | msdyn_actual       | GUID der Fakturierten Umsätze            | Original                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
