---
title: Tatsächliche Transaktionen – Übersicht
description: Dieses Thema enthält Informationen zu Projekt-Istwerten.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146122"
---
# <a name="actuals-overview"></a>Tatsächliche Transaktionen – Übersicht

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ist-Werte sind der Arbeitsaufwand, der für ein Projekt erbracht wurde. Projekt-Istwerte können zu ihren Quelldokumenten zurückverfolgt werden. Diese Quelldokumente umfassen Zeit-, Ausgaben- und Journaleinträge und auch Rechnungen.

![So werden Projekt-Istwerte zu den Quelldokumenten zurückverfolgt](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Übermitteln eines Zeiteintrags

Wenn in PSA ein Zeiteintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt. Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb. Wenn ein Zeiteintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt. 

Die Logik zur Eingabe von Standardpreisen befindet sich in der Journalposition. Alle Feldwerte eines Zeiteintrags werden in die Erfassungsposition kopiert. Diese Felder enthalten das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie das Währungsergebnis in der entsprechenden Preisliste. 

In den Feldern, die sich auf die Standardpreise wie etwa **Rolle** und **Organisationseinheit** auswirken, wird standardmäßig ein entsprechender Preis in die Erfassungsposition eingegeben. Wenn Sie dem Zeiteintrag ein benutzerdefiniertes Feld hinzufügen und möchten, dass der Feldwert an „Ist-Werte” weitergegeben wird, erstellen Sie das Feld in der Entität „Ist-Werte” und kopieren Sie das Feld mithilfe von Feldzuordnungen vom Zeiteintrag zum Ist-Wert.

## <a name="submitting-an-expense-entry"></a>Übermitteln eines Ausgabeneintrags

Wenn in PSA ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Zeit- und Materialvertragszeile zugeordnet ist, werden zwei Journaleinträge erstellt. Eine Zeile ist für Kosten und die andere Zeile ist für den nicht fakturierten Vertrieb. Wenn ein Ausgabeneintrag für ein Projekt übermittelt wird, das einer Festpreisvertragszeile zugeordnet ist, wird nur für Kosten ein Journaleintrag erstellt.

Die Logik zur Eingabe von Standardpreisen basiert auf der Ausgabenkategorie, die auf der Seite **Ausgabeneintrag** ausgewählt wurde. Das Datum der Transaktion, die Vertragszeile, der das Projekt zugeordnet ist, sowie die Währung werden alle zum Bestimmen der entsprechenden Preisliste verwendet. Für den Preis selbst wird der vom Benutzer eingegebene Betrag jedoch standardmäßig direkt in den entsprechenden Ausgabenerfassungspositionen für Kosten und Umsatz festgelegt.

In der aktuellen Version von PSA ist der kategoriebasierte Eintrag von Standardpreisen pro Einheit bei Ausgabeneinträgen nicht verfügbar.

## <a name="using-entry-journals-to-record-costs"></a>Verwenden von Eintragserfassungen zum Erfassen von Kosten

In PSA können Sie mithilfe von Eintragserfassungen Kosten bzw. Umsatz in den Transaktionsklassen Material, Gebühr, Zeit, Ausgabe oder Steuer erfassen. Ein Journal enthält eine Kopfzeile, Zeilen und eine Aktion **Bestätigen**. Hier finden Sie einige Szenarien, in denen Sie möglicherweise ein Journal verwenden:

- Bei einem Projekt müssen Sie die tatsächlichen Materialkosten und -umsätze erfassen.
- Sie müssen Transaktions-Istwerte aus einem anderen System in PSA importieren.
- Sie müssen Kosten erfassen, die in einem anderen System angefallen sind, z. B. Beschaffungskosten oder Kosten für Unteraufträge.

> [!IMPORTANT]
> Istwerte sollten nur mithilfe von Eintragsjournalen erstellt werden, wenn dem Benutzer die buchhalterische Auswirkung der Istwerte auf das Projekt voll bewusst ist. Dies liegt daran, dass die Anwendung den Erfassungsposition oder den zugehörigen Preis, der in der Erfassungsposition eingegeben wird, nicht überprüft. Seien Sie aufgrund der Auswirkungen dieses Erfassungstyps entsprechend vorsichtig dabei, wer Zugriff auf die Erstellung von Eintragserfassungen erhält.     


## <a name="recording-actuals-based-on-project-events"></a>Erfassen von Ist-Werten basierend auf Projektereignissen

PSA erfasst die Finanztransaktionen, die während eines Projekts stattfinden. Diese Transaktionen werden als **Ist-Werte** aufgezeichnet. Die folgenden Tabellen enthalten die verschiedenen Arten von Ist-Werten, die abhängig davon erstellt werden, ob es sich beim Projekt um ein Zeit-und Material- oder ein Festpreisprojekt handelt, es sich in der Vorverkaufsphase befindet oder ein internes Projekt ist.

**Die Ressource gehört zu derselben Organisationseinheit wie die Vertragseinheit des Projekts**

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

**Die Ressource gehört zu einer Organisationseinheit, die sich von der Vertragseinheit des Projekts unterscheidet**

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
