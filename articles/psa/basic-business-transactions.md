---
title: Geschäftstransaktionen
description: Dieses Thema enthält Informationen zu Geschäftstransaktionen.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7c1fd7046783b98b7c2e823b2c2eb8bbdfb232fc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583344"
---
# <a name="business-transactions"></a>Geschäftstransaktionen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation ist *Geschäftstransaktion* ein abstraktes Konzept, das von keiner Entität dargestellt wird. Einige häufig verwendete Felder und Prozesse für Entitäten sind jedoch so ausgelegt, dass sie das Konzept von Geschäftstransaktionen verwenden. Die folgenden Entitäten verwenden diese Abstraktion:

- Detailinformationen zur Angebotsposition
- Vertragszeilendetails
- Vorkalkulationszeilen
- Erfassungspositionen
- Ist-Werte

Von diesen Entitäten werden Angebotspositions- und Vertragszeilendetails sowie Vorkalkulationszeilen im Projektlebenszyklus der Vorkalkulationsphase zugeordnet. Die Entitäten „Erfassungspositionen“ und „Ist-Werte“ werden im Projektlebenszyklus der Ausführungsphase zugeordnet.

PSA behandelt Datensätze in diesen fünf Entitäten als Geschäftstransaktionen. Die einzige Unterscheidung besteht darin, dass Datensätze in den Entitäten, die zur Vorkalkulationsphase zugeordnet werden, als Finanzprognosen gelten, wohingegen die Datensätze in den Entitäten, die zur Ausführungsphase zugeordnet werden, als bereits eingetretene Finanztatsachen gelten.

Weitere Informationen finden Sie unter [Vorkalkulationen](estimates.md) und [Ist-Werte](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Einzigartige Konzepte für Geschäftstransaktionen
Die folgenden Konzepte sind für das Konzept der Geschäftstransaktionen einzigartig:

- Transaktionstyp
- Transaktionsklasse
- Transaktionsursprung
- Transaktionsverbindung

### <a name="transaction-type"></a>Transaktionstyp

Der Transaktionstyp gibt den Zeitpunkt und den Kontext der finanziellen Auswirkungen auf ein Projekt an. Es wird durch einen Optionssatz dargestellt, der in PSA die folgenden unterstützten Werte aufweist:
- Kosten
- Projektvertrag
- Nicht fakturierte Umsätze
- Fakturierte Umsätze
- Organisationsübergreifender Umsatz
- Kosten der Ressourcenzuordnungseinheit

### <a name="transaction-class"></a>Transaktionsklasse

Die Transaktionsklasse repräsentiert die verschiedenen Arten von Kosten, die für Projekte angefallen sind. Es wird durch einen Optionssatz dargestellt, der in PSA die folgenden unterstützten Werte aufweist:

- Time
- Expense
- Material
- Gebühr
- Meilenstein
- Steuer

Der Wert **Meilenstein** wird in PSA in der Regel von der Geschäftslogik für die Festpreisfakturierung verwendet.

### <a name="transaction-origin"></a>Transaktionsursprung

Der Buchungsursprung ist eine Entität, die den Ursprung jeder Geschäftsbuchung speichert. Wenn die Projektdurchführung beginnt, führt jede Geschäftsbuchung zu einer anderen Geschäftsbuchung, die wiederum eine weitere erstellt und so weiter. Die Buchungsursprungsentität wurde entwickelt, um Daten über den Ursprung jeder Buchung zu speichern, um die Berichterstellung und Rückverfolgbarkeit zu erleichtern. 

### <a name="transaction-connection"></a>Transaktionsverbindung

Die Transaktionsverbindung ist eine Entität, die die Beziehung zwischen zwei ähnlichen Geschäftstransaktionen speichert, z. B. Kosten und zugehörige Umsatz-Istwerte oder Transaktionsumkehrungen, die durch Fakturierungsaktivitäten wie Rechnungsbestätigung oder Rechnungskorrekturen ausgelöst werden.

Mithilfe von Transaktionsursprung und Transaktionsverbindung können Sie Beziehungen zwischen Geschäftstransaktionen und Aktionen nachverfolgen, die zur Erstellung einer bestimmten Geschäftstransaktion geführt haben.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Beispiel: So funktioniert Transaktionsursprung mit Transaktionsverbindung

Im folgenden Beispiel wird die typische Verarbeitung von Zeiteinträgen im Lebenszyklus eines PSA-Projekts veranschaulicht.

> ![Verarbeitung von Zeiteinträgen in einem Project Service-Lebenszyklus.](media/basic-guide-17.png)
 
1. Die Übermittlung eines Zeiteintrags führt zur Erstellung von zwei Erfassungspositionen: eine für die Kosten und eine für den nicht fakturierten Vertrieb.
2. Die spätere Genehmigung des Zeiteintrags führt zur Erstellung von zwei Ist-Werten: einer für die Kosten und einer für den nicht fakturierten Vertrieb.
3. Wenn der Benutzer eine Projektrechnung erstellt, wird die Rechnungszeilentransaktion unter Verwendung der Daten aus dem nicht fakturiertem vertrieblichen Ist-Wert erstellt. 
4. Wenn die Rechnung bestätigt wird, werden zwei neue Ist-Werte erstellt: eine nicht fakturierte Umsatzumkehrung und ein fakturierter Umsatz-Istwert.

Jedes dieser Ereignisse löst die Erstellung von Datensätzen in den Entitäten „Transaktionsursprung“ und „Transaktionsverbindung“ aus, damit die Beziehungen zwischen diesen Datensätzen, die über Zeiteinträge, Erfassungspositionen, Ist-Werte und Rechnungspositionsdetails erstellt werden, überwacht werden können.

Die folgende Tabelle enthält die Datensätze in der Entität „Transaktionsursprung“ für den vorangehenden Workflow.

| Ereignis                        | Ursprung                   | Ursprungstyp                       | Transaktion                       | Transaktionstyp         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Übermittlung des Zeiteintrags        | GUID des Datensatzes „Zeiteintrag“   | Zeiteintrag                        | GUID des Datensatzes „Erfassungsposition (Kosten)“   | Erfassungsposition             |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Erfassungsposition (Vertrieb)“  | Erfassungsposition                      |                          |
| Genehmigung der Zeit                | GUID des Datensatzes „Erfassungsposition“ | Erfassungsposition                      | GUID des Datensatzes „Nicht fakturierte Umsätze“        | Tatsächlich                   |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Nicht fakturierte Umsätze“        | Tatsächlich                            |                          |
| GUID des Datensatzes „Erfassungsposition“     | Erfassungsposition             | GUID des Datensatzes „Kosten-Istwert“           | Tatsächlich                            |                          |
| GUID des Datensatzes „Zeiteintrag“       | Zeiteintrag               | GUID des Datensatzes „Kosten-Istwert“           | Tatsächlich                            |                          |
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

Die folgende Tabelle enthält die Datensätze in der Entität „Transaktionsverbindung“ für den vorangehenden Workflow.

| Ereignis                          | Transaktion 1                 | Rolle Transaktion 1 | Typ Transaktion 1           | Transaktion 2                | Rolle Transaktion 2 | Typ Transaktion 2 |
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
