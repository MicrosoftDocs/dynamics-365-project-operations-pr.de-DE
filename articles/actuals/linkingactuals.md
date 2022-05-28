---
title: Transaktionsursprünge – Istewerte mit deren Quelle verknüpfen
description: In diesem Thema wird erläutert, wie das Konzept der Transaktionsursprünge verwendet wird, um Ist-Werte mit ursprünglichen Quelldatensätzen zu verknüpfen, z. B. Zeiteinträgen, Ausgabeneinträgen oder Materialverbrauchsprotokollen.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584825"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Transaktionsursprünge – Istewerte mit deren Quelle verknüpfen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Transaktionsursprungsdatensätze werden erstellt, um Ist-Werte mit ihrer Quelle zu verknüpfen, wie z. B. Zeiteinträge, Ausgabeneinträge, Materialnutzungsprotokolle und Projektrechnungen.

Im folgenden Beispiel wird die typische Verarbeitung von Zeiteinträgen im Lebenszyklus eines Project Operations-Projekts veranschaulicht.

> ![Verarbeiten von Zeiteinträgen in Project Operations.](media/basic-guide-17.png)
 
1. Die Übermittlung eines Zeiteintrags führt zur Erstellung von zwei Erfassungspositionen: eine für die Kosten und eine für den nicht fakturierten Vertrieb.
2. Die spätere Genehmigung des Zeiteintrags führt zur Erstellung von zwei Ist-Werten: einer für die Kosten und einer für den nicht fakturierten Vertrieb.
3. Wenn der Benutzer eine Projektrechnung erstellt, wird die Rechnungszeilentransaktion unter Verwendung der Daten aus dem nicht fakturiertem vertrieblichen Ist-Wert erstellt.
4. Wenn die Rechnung bestätigt wird, werden zwei neue Ist-Werte erstellt: eine nicht fakturierte Umsatzumkehrung und ein fakturierter Umsatz-Istwert.

Jedes Ereignis in diesem Verarbeitungs-Workflow löst die Erstellung von Datensätzen in der Entität „Transaktionsursprung“ aus, damit die Beziehungen zwischen diesen Datensätzen, die über Zeiteinträge, Erfassungspositionen, Ist-Werte und Rechnungspositionsdetails erstellt werden, überwacht werden können.

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
| GUID der Korrekturrechnung      | Rechnung                  | GUID des Neuen nicht fakturierten Umsatz-Istwerts    | Tatsächl.                            |                          |


Die folgende Abbildung zeigt die Verknüpfungen, die zwischen unterschiedlichen Ist-Werten und deren Quellen bei verschiedenen Ereignissen erstellt werden, am Beispiel von Zeiterfassungen in Project Operations.

> ![So werden Ist-Werte in Project Operations mit Quelldatensätzen verknüpft.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
