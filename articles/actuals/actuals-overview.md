---
title: Tatsächliche Transaktionen
description: Dieses Thema enthält Informationen zum Arbeiten mit Istwerten in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368610"
---
# <a name="actuals"></a>Tatsächliche Transaktionen 

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Die tatsächlichen Werte repräsentieren den überprüften und genehmigten finanziellen und geplanten Fortschritt eines Projekts. Sie werden als Ergebnis der Genehmigung von Zeit-, Kosten-, Materialverbrauchseinträgen sowie Journaleinträgen und Rechnungen erstellt.

## <a name="journal-lines-and-time-submission"></a>Erfassungspositionen und Zeiteinreichung

Weitere Informationen zum Zeiteintrag finden Sie unter [Zeiteintragsübersicht](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Zeit und Materialien

Wenn ein übermittelter Zeiteintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.

### <a name="fixed-price"></a>Festpreis

Wenn ein eingereichter Zeiteintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Erfassungsposition für Kosten.

### <a name="default-pricing"></a>Standardpreise

Die Logik zur Erstellung von Standardpreisen befindet sich in der Journalposition. Die Feldwerte des Zeiteintrags werden in die Erfassungsposition kopiert. Diese Werte enthalten das Transaktionsdatum, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste.

Die Felder, die sich auf die Standardpreise wie etwa **Rolle** und **Ressourceneinheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen. Sie können dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen. Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**. Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen. Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Erfassungspositionen und Einreichung der Grundkosten

Weitere Informationen zum Ausgabeneintrag finden Sie unter [Ausgabeneintragsübersicht](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Zeit und Materialien

Wenn ein übermittelter Grundkosteneintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Erfassungspositionen, eine für Kosten und eine für nicht abgerechnete Verkäufe.

### <a name="fixed-price"></a>Festpreis

Wenn ein übertragener Basisausgabeneintrag mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Journalzeile für Kosten.

### <a name="default-pricing"></a>Standardpreise

Die Logik zur Eingabe von Standardpreisen für Ausgaben basiert auf der Ausgabenkategorie. Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet. Die Felder, die sich auf die Standardpreise wie etwa **Transaktionskategorie** und **Einheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen. Dies funktioniert jedoch nur, wenn die Preismethode in der Preisliste **Preis pro Einheit** lautet. Wenn die Preismethode **Zum Einstandswert** oder **Aufschlag auf Kosten** lautet, wird der bei der Erstellung der Spesenbuchung eingegebene Preis für die Kosten verwendet und der Preis in der Verkaufsjournalzeile wird anhand der Preismethode berechnet. 

Sie können der Spesenbuchung ein benutzerdefiniertes Feld hinzufügen. Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**. Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen. Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Übermittlung von Journalzeilen und Materialverwendungsprotokollen

Weitere Informationen zur Kostenerfassung finden Sie unter [Materialverbrauchsprotokoll](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Zeit und Materialien

Wenn ein übermittelter Materialverwendungsprotokolleintrag mit einem Projekt verknüpft ist, das einer Zeit- und Materialvertragszeile zugeordnet ist, erstellt das System zwei Journalzeilen, eine für Kosten und eine für nicht abgerechnete Verkäufe.

### <a name="fixed-price"></a>Festpreis

Wenn ein übertragenes Materialverbrauchsprotokoll mit einem Projekt verknüpft wird, das einer Festpreisvertragszeile zugeordnet ist, erstellt das System eine Journalzeile für Kosten.

### <a name="default-pricing"></a>Standardpreise

Die Logik zur Eingabe von Standardpreisen für Material basiert auf der Produkt- und Einheitenkombination. Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet. Die Felder, die sich auf die Standardpreise wie etwa **Produkt-ID** und **Einheit** auswirken, werden verwendet, um den entsprechenden Preis in die Erfassungsposition festzulegen. Dies funktioniert jedoch nur für Katalogprodukte. Bei manuell einzutragenden Produkten wird der Preis, der bei der Erstellung des Materialverbrauchsprotokolleintrags eingegeben wurde, für Kosten und Verkaufspreis in den Journalzeilen verwendet. 

Sie können dem **Materialverbrauchsprotokoll** ein benutzerdefiniertes Feld hinzufügen. Wenn Sie möchten, dass der Feldwert an Istwerte weitergegeben wird, erstellen Sie das Feld in den Tabellen **Istwerte** und **Journalzeile**. Verwenden Sie benutzerdefinierten Code, um den ausgewählten Feldwert mithilfe von Transaktionsursprüngen von Zeiteinträgen zu Istwerten über die Journalzeile zu übertragen. Weitere Informationen zu Transaktionsursprüngen und -verbindungen finden Sie unter [Tatsächliche Transaktionen mit ursprünglichen Datensätzen verknüpfen](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Eintragserfassungen zur Erfassung von Kosten verwenden

Sie können mithilfe von Erfassungenn die Kosten bzw. den Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen. Erfassungen können für die folgenden Zwecke verwendet werden:

- Importieren Sie Transaktions-Istwerte aus einem anderen System nach Microsoft Dynamics 365 Project Operations.
- Zeichnen Sie die Kosten auf, die in einem anderen System aufgetreten sind. Diese Kosten können Beschaffungs- oder Fremdarbeitskosten umfassen.

> [!IMPORTANT]
> Die Anwendung überprüft weder den Erfassungspositionstyp noch den zugehörigen Preis, der in der Erfassungsposition eingegeben wird. Daher sollte nur ein Benutzer, der sich der Auswirkungen der tatsächlichen Buchhaltung auf das Projekt voll bewusst ist, Eintragserfassungen verwenden, um tatsächliche Daten zu erstellen. Aufgrund der Auswirkungen dieses Erfassungstyps sollten Sie sorgfältig auswählen, wer Zugriff zum Erstellen von Eintragserfassungen hat.

## <a name="record-actuals-based-on-project-events"></a>Ist-Werte basierend auf Projektereignissen erfassen

Project Operations erfasst die Finanztransaktionen, die während eines Projekts stattfinden. Diese Transaktionen werden als Ist-Werte aufgezeichnet. Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts

<table>
<thead>
<tr>
<th rowspan="3">Ereignis</th>
<th colspan="4">Abrechenbares oder verkauftes Projekt</th>
<th rowspan="3">Projekt in der Vorverkaufsphase</th>
<th rowspan="3">Internes Projekt</th>
</tr>
<tr>
<th colspan="2">Zeit und Materialien</th>
<th colspan="2">Festpreis</th>
</tr>
<tr>
<th>Ist-Werte</th>
<th>Transaktionswährung</th>
<th>Festpreis</th>
<th>Transaktionswährung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ein Zeiteintrag wird erstellt.</td>
<td colspan="6">Keine Aktivität in der Entität „Ist-Werte”</td>
</tr>
<tr>
<td>Ein Zeiteintrag wird übermittelt.</td>
<td colspan="6">Keine Aktivität in der Entität „Ist-Werte”</td>
</tr>
<tr>
<td rowspan="2">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</td>
<td>Kosten-Istwert</td>
<td>Währung der Vertragseinheit</td>
<td rowspan="2">Kosten-Istwert</td>
<td rowspan="2">Währung der Vertragseinheit
<td rowspan="2">Kosten-Istwert</td>
<td rowspan="2">Kosten-Istwert</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Fakturierbar</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="3">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</td>
<td>Kosten-Istwert</td>
<td>Währung der Vertragseinheit</td>
<td rowspan="3">Kosten-Istwert</td>
<td rowspan="3">Währung der Vertragseinheit</td>
<td rowspan="3">Kosten-Istwert</td>
<td rowspan="3">Kosten-Istwert</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="2">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</td>
<td>Nicht fakturierte Umsatzumkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="2">Abgerechnete Umsätze für Meilenstein</td>
<td rowspan="2">Währung des Projektvertrags</td>
<td rowspan="2">Nicht verfügbar</td>
<td rowspan="2">Nicht verfügbar</td>
</tr>
<tr>
<td>Fakturierte Umsätze</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="3">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</td>
<td>Nicht fakturierte Umsatzumkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
</tr>
<tr>
<td>Abgerechneter Umsatz – Fakturierbar für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="2">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</td>
<td>Abgerechneter Umsatz – Umkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="5">
<ul>
<li>Abgerechnete Umsatzumkehrung für Meilenstein</li>
<li>Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></li>
</ul>
</td>
<td rowspan="5">Währung des Projektvertrags</td>
<td rowspan="5">Nicht verfügbar</td>
<td rowspan="5">Nicht verfügbar</td>
</tr>
<tr>
<td>Fakturierte Umsätze</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="3">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</td>
<td>Abgerechneter Umsatz – Umkehrung</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Abgerechneter Umsatz für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Nicht fakturierte Umsätze – Fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet

<table>
<thead>
<tr>
<th rowspan="3">Ereignis</th>
<th colspan="4">Abrechenbares oder verkauftes Projekt</th>
<th rowspan="3">Projekt in der Vorverkaufsphase</th>
<th rowspan="3">Internes Projekt</th>
</tr>
<tr>
<th colspan="2">Zeit und Materialien</th>
<th colspan="2">Festpreis</th>
</tr>
<tr>
<th>Ist-Werte</th>
<th>Transaktionswährung</th>
<th>Festpreis</th>
<th>Transaktionswährung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ein Zeiteintrag wird erstellt.</td>
<td colspan="6">Keine Aktivität in der Entität „Ist-Werte”</td>
</tr>
<tr>
<td>Ein Zeiteintrag wird übermittelt.</td>
<td colspan="6">Keine Aktivität in der Entität „Ist-Werte”</td>
</tr>
<tr>
<td rowspan="4">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung weder geändert noch erhöht werden.</td>
<td>Kosten-Istwert</td>
<td>Währung der Vertragseinheit</td>
<td rowspan="4">Kosten-Istwert</td>
<td rowspan="4">Währung der Vertragseinheit</td>
<td rowspan="4">Kosten-Istwert</td>
<td rowspan="4">Kosten-Istwert</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Fakturierbar</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Kosten der Ressourcenzuordnungseinheit</td>
<td>Währung der Ressourcenzuordnungseinheit</td>
</tr>
<tr>
<td>Organisationsübergreifender Umsatz</td>
<td>Währung der Vertragseinheit</td>
</tr>
<tr>
<td rowspan="5">Die Zeit wird genehmigt, wobei die abrechenbaren Stunden während der Genehmigung verringert werden.</td>
<td>Kosten-Istwert</td>
<td>Währung der Vertragseinheit</td>
<td rowspan="5">Kosten-Istwert</td>
<td rowspan="5">Währung der Vertragseinheit</td>
<td rowspan="5">Kosten-Istwert</td>
<td rowspan="5">Kosten-Istwert</td>
</tr>
<tr>
<td>Kosten der Ressourcenzuordnungseinheit</td>
<td>Währung der Ressourcenzuordnungseinheit</td>
</tr>
<tr>
<td>Organisationsübergreifender Umsatz</td>
<td>Währung der Vertragseinheit</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Fakturierbar für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Nicht fakturierter Umsatz-Istwert – Nicht fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="2">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden weder geändert noch erhöht werden.</td>
<td>Nicht fakturierte Umsatzumkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="2">Abgerechnete Umsätze für Meilenstein</td>
<td rowspan="2">Währung des Projektvertrags</td>
<td rowspan="2">Nicht verfügbar</td>
<td rowspan="2">Nicht verfügbar</td>
</tr>
<tr>
<td>Fakturierte Umsätze</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="3">Eine Rechnung wird bestätigt, wobei die abrechenbaren Stunden verringert werden.</td>
<td>Nicht fakturierte Umsatzumkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
<td rowspan="3">Nicht verfügbar</td>
</tr>
<tr>
<td>Abgerechneter Umsatz – Fakturierbar für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Abgerechneter Umsatz – Nicht fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="2">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu erhöhen.</td>
<td>Abgerechneter Umsatz – Umkehrung</td>
<td>Währung des Projektvertrags</td>
<td rowspan="5">
<ul>
<li>Abgerechnete Umsatzumkehrung für Meilenstein</li>
<li>Änderung des Meilensteinstatus von <strong>In Rechnung gestellt</strong> in <strong>Bereit für die Rechnungsstellung</strong></li>
</ul>
</td>
<td rowspan="5">Währung des Projektvertrags</td>
<td rowspan="5">Nicht verfügbar</td>
<td rowspan="5">Nicht verfügbar</td>
</tr>
<tr>
<td>Fakturierte Umsätze</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td rowspan="3">Eine Rechnung wird korrigiert, um die fakturierbare Menge zu verringern.</td>
<td>Abgerechneter Umsatz – Umkehrung</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Abgerechneter Umsatz für die neue Menge</td>
<td>Währung des Projektvertrags</td>
</tr>
<tr>
<td>Nicht fakturierte Umsätze – Fakturierbar für die Differenz</td>
<td>Währung des Projektvertrags</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
