---
title: Projektverträge
description: Dieses Thema enthält Beispiele für die Projektverträge, die Sie für verschiedene Arten von Projekten und Finanzierungsquellen erstellen können, sowie für die Verwaltung von Verträgen und die Rechnungsstellung von Projektkunden.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001025"
---
# <a name="project-contracts"></a>Projektverträge

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Beispiele für die Projektverträge, die Sie für verschiedene Arten von Projekten und Finanzierungsquellen erstellen können, sowie für die Verwaltung von Verträgen und die Rechnungsstellung von Projektkunden.

Die Art des Projekts, das Sie für einen Projektvertrag erstellen, bestimmt die Methode, mit der den Projektkunden Rechnung gestellt wird. Sie können einen Projektvertrag und das zugehörige Projekt ändern, aber Sie können den Projekttyp nicht ändern. 

Mit einem Projektvertrag können Sie ein oder mehrere Projekte gleichzeitig in Rechnung stellen. Projektverträge tragen auch dazu bei, für jedes Teilprojekt einer Projektstruktur ein einheitliches Rechnungsverfahren zu gewährleisten. 

Jedes in Rechnung gestellte Projekt muss einem Projektvertrag zugehörig sein. Die Einstellungen für Projektverträge gelten für alle Projekte und Teilprojekte, die dem Projektvertrag zugeordnet sind. 

In einem Projektvertrag können eine oder mehrere Finanzierungsquellen angegeben werden. Daher können Sie die Abrechnung auf mehrere Geldgeber aufteilen, Finanzierungsgrenzwertes festlegen, damit Finanzierungsquellen nicht mehr als einen bestimmten Betrag in Rechnung stellen, und Finanzierungsregeln für die Erhebung von Ausgaben konfigurieren.

## <a name="funding-for-project-contracts"></a>Finanzierung von Projektverträgen
In einigen Projektverträgen ist festgelegt, dass mehrere Parteien die Verantwortung für die Finanzierung der Projektkosten teilen. Hier sehen Sie einige Beispiele:

-   Ein großer Kunde mit mehreren Abteilungen verlangt, dass die Finanzierung eines Projekts nach Abteilungen aufgeteilt wird.
-   Ihr Unternehmen teilt die Kosten eines Großprojekts mit einer externen Organisation.
-   Ein Straßenprojekt wird von zwei Gemeinden kofinanziert.
-   Ein Brückenprojekt wird durch einen staatlichen Zuschuss und ein privates Unternehmen finanziert.

In Dynamics 365 Finance können Sie die Abrechnung für eine einzelne Transaktion oder ein gesamtes Projekt auf mehrere Kunden, Zuschüsse oder Organisationen aufteilen. 

In Projekten mit mehreren Geldgebern werden alle Parteien, die zur Finanzierung eines fortgeschrittenen Finanzierungsprojekts beitragen, als Finanzierungsquellen bezeichnet. Nachdem ein Kunde, eine Organisation oder ein Zuschuss als Finanzierungsquelle definiert wurde, kann er einer oder mehreren Finanzierungsregeln zugewiesen werden. Die Finanzierungsregeln enthalten die Kriterien, die bestimmen, wie die Gebühren den verschiedenen Finanzierungsquellen für ein Projekt zugeordnet werden. 

Da vorrätige Artikel, wie sie beispielsweise in Bestellanforderungen und Bestellungen enthalten sind, nicht aufgeteilt werden können, kann der Kostenbetrag zum Zeitpunkt der Verteilung nicht auf mehrere Finanzierungsquellen aufgeteilt werden. Daher bleibt der Wert der Finanzierungsquelle 0 (Null), bis das Inventarproblem gebucht wird. Wenn das Inventarproblem gebucht wird, wird der Kostenbetrag gemäß den Kontoverteilungsregeln für das Projekt verteilt.

Hier sind einige Schritte, die Sie unternehmen können, um die Aufteilung auf mehrere Finanzierungsquellen zu vereinfachen:

-   Geben Sie an, dass alle Transaktionen, die für ein Projekt eingegeben werden, dieselbe Verkaufswährung wie der Projektvertrag verwenden.
-   Richten Sie Finanzierungslimits ein, damit einer Finanzierungsquelle nicht mehr als ein bestimmter Betrag für ein Projekt in Rechnung gestellt wird.
-   Konfigurieren Sie Finanzierungsregeln und Finanzierungslimits für jeden Mitarbeiter, Artikel, Kategorie, Kategoriegruppe und Transaktionstyp (oder für alle Transaktionstypen).
-   Wählen Sie optionale Start- und Enddaten aus, um den Zeitraum zu definieren, in dem jede Finanzierungsregel gültig ist.
-   Geben Sie den Prozentsatz an, für den jede Finanzierungsquelle verantwortlich ist.
-   Geben Sie an, welche Finanzierungsquelle für Rundungsdifferenzen verantwortlich ist, die durch Berechnungen der Mittelzuweisung verursacht werden.
-   Richten Sie Regeln ein, die festlegen, wie Projektkosten externen Kunden und internen Organisationen in Rechnung gestellt werden.
-   Erfassen Sie Transaktionen auf einem gehaltenen Finanzierungskonto, bis zusätzliche Mittel verfügbar sind oder bis Sie sich entscheiden, die Kosten intern zu tragen.

Um zu bestimmen, welche Steuergruppe einer Transaktion zugeordnet werden soll, wird das Projekt nach einer Steuergruppenzuordnung durchsucht. Wenn auf Projektebene keine Steuergruppenzuordnung vorgenommen wurde, wird der Projektvertrag durchsucht.

### <a name="example-multiple-funding-sources-simple"></a>Beispiel: Mehrere Finanzierungsquellen (einfach)

Die folgende Tabelle enthält Szenarien zum Verwalten der Mittelzuweisung auf mehrere Finanzierungsquellen. Diese Szenarien basieren auf folgenden Annahmen:

-   Prioritätseinstellungen werden bei der Zuweisung von Mitteln berücksichtigt, bevor andere Kriterien für Finanzierungsregeln angewendet werden.
-   Es wurde kein Datumsbereich angegeben, um den Zeitraum d zu definieren, in dem die Finanzierungsregel gültig ist.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Szenario</strong></td>
<td><strong>Finanzierungsquelle</strong></td>
<td><strong>Zuordnungsprozentsatz</strong></td>
<td><strong>Zuweisungspriorität</strong></td>
</tr>
<tr class="even">
<td>Sie möchten die Kosten einer Finanzierungsquelle zuordnen, bis die Mittel aufgebraucht sind, die Kosten einer zweiten Finanzierungsquelle zuordnen, bis die Mittel aufgebraucht sind, und schließlich die verbleibenden Kosten einer dritten Finanzierungsquelle zuordnen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent einer zweiten Finanzierungsquelle zuordnen. Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten von einer dritten Finanzierungsquelle bezahlen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Sie möchten 75 Prozent der Kosten einer Finanzierungsquelle und 25 Prozent einer zweiten Finanzierungsquelle zuordnen. Wenn eine dieser Finanzierungsquellen erschöpft ist, möchten Sie die verbleibenden Kosten zwischen einer dritten und einer vierte Finanzierungsquelle aufteilen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
<li>Finanzierungsquelle 3</li>
<li>Finanzierungsquelle 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sie möchten die ersten 25 Prozent der Kosten einer Finanzierungsquelle und den Rest einer zweiten Finanzierungsquelle zuordnen.</td>
<td><ul>
<li>Finanzierungsquelle 1</li>
<li>Finanzierungsquelle 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Beispiel: Mehrere Finanzierungsquellen (complex)

Sie haben drei Finanzierungsquellen, die Sie in der folgenden Reihenfolge verwenden möchten:

1.  Verwenden Sie Finanzierungsquelle 2 und Finanzierungsquelle 3 gleichermaßen, bis die Finanzierungsquelle 2 erschöpft ist.
2.  Verwenden Sie weiterhin Finanzierungsquelle 3, bis diese erschöpft ist.
3.  Verwenden Sie die Finanzierungsquelle 1, nachdem die Finanzierungsquelle 3 erschöpft ist.

Um dieses Ziel zu erreichen, müssen Sie Folgendes ausführen:

-   Legen Sie Finanzierungslimits für Finanzierungsquelle 2 und Finanzierungsquelle 3 für ihre jeweiligen Beträge fest.
-   Erstellen Sie die folgenden Finanzierungsregeln:
    -   Regel 1 (Priorität 1): Ordnen Sie 50 Prozent der Transaktionen der Finanzierungsquelle 2 und 50 Prozent der Finanzierungsquelle 3 zu.
    -   Regel 2 (Priorität 2): Ordnen Sie 100 Prozent der Transaktionen der Finanzierungsquelle 3 zu.
    -   Regel 3 (Priorität 3): Ordnen Sie 100 Prozent der Transaktionen der Finanzierungsquelle 1 zu.

Dieses Setup funktioniert, da Transaktionen anhand von Regeln und Grenzwerten überprüft werden, um festzustellen, ob sie für die Transaktion gelten. Wenn für die Transaktion keine spezifischen Regeln oder Beschränkungen gelten, gilt die Regel „Alle Transaktionen“. Die Regel „Alle Transaktionen“ stimmt mit allen Transaktionen überein. 

Wenn eine Regel gefunden wird, die mit einer Transaktion übereinstimmt, wird der Prozentsatz, der in dieser Regel zugewiesen wurde, zuerst angewendet, jedoch erst, nachdem die Übereinstimmungen mit den festgelegten Grenzwerten verglichen wurden. Wenn ein Limit erreicht wurde und die Mittel einer Finanzierungsquelle erschöpft sind, wird die mit dem Finanzierungslimit verbundene Finanzierungsregel nicht berücksichtigt und das Programm prüft, ob die nächste Regel gilt. 

In einigen Fällen kann nur ein Teil einer Transaktion unter einer Regel zugeordnet werden. Dies kann passieren, weil bei der Zuweisung der Transaktion ein Limit erreicht wird. In diesem Fall wird nach dieser Regel nur ein bestimmter Betrag zugewiesen, z. B. 50 Prozent für jede Finanzierungsquelle. Dies ist in Regel 1 der Fall, die weiter oben in diesem Abschnitt beschrieben wird. Der Rest wird gemäß der nächsten Regel in der Sequenz zugewiesen. 

Die Tabelle unten überprüft dieses Szenario genauer.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Details</strong></td>
</tr>
<tr class="even">
<td>Finanzierungsregeln</td>
<td><ul>
<li>Regel 1 (Priorität 1): Alle Transaktionen. Weisen Sie Finanzierungsquelle 2 zu 50 % und Finanzierungsquelle 3 zu 50 % zu.</li>
<li>Regel 2 (Priorität 2): Alle Transaktionen. Weisen Sie die Finanzierungsquelle 3 zu 100 % zu.</li>
<li>Regel 3 (Priorität 2): Alle Transaktionen. Weisen Sie die Finanzierungsquelle 1 zu 100 % zu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finanzierungslimits</td>
<td><ul>
<li>Limit für Finanzierungsquelle 1 = 10.000,00</li>
<li>Limit für Finanzierungsquelle 2 = 500,00</li>
<li>Limit für Finanzierungsquelle 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaktion 1</td>
<td><strong>Transaktionshöhe:</strong> 100,00<strong>Finanzierung:</strong> Die Transaktion wird nur gemäß Regel 1 bezahlt, da die Transaktion nach Anwendung von Regel 1 vollständig bezahlt wird. Die Transaktion wird zu gleichen Teilen zwischen Finanzierungsquelle 2 und Finanzierungsquelle 3 finanziert.
<ul>
<li>Finanzierungsquelle 2: 50,00</li>
<li>Finanzierungsquelle 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaktion 2</td>
<td><strong>Transaktionshöhe:</strong> 5.000,00<strong>Finanzierung:</strong> Die Transaktion wird nach allen drei Regeln bezahlt. <strong>Regel 1</strong>
<ul>
<li>Finanzierungsquelle 2: 450,00</li>
<li>Finanzierungsquelle 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Finanzierungsquelle 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Finanzierungsquelle 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Gesamtmittel, die für jede Finanzierungsquelle verteilt werden</td>
<td><ul>
<li>Finanzierungsquelle 1: 3.850,00</li>
<li>Finanzierungsquelle 2: 500,00</li>
<li>Finanzierungsquelle 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Abrechnungsregeln
Wenn Sie einen Projektvertrag mit einem Kunden aushandeln, legen Sie fest, wie und wann Sie dem Kunden die Arbeit an einem Projekt in Rechnung stellen können. Nachdem Sie den Projektvertrag und das Projekt eingerichtet haben, können Sie Abrechnungsregeln für das Projekt einrichten. Die Abrechnungsregeln basieren auf den im Projektvertrag festgelegten Projektbedingungen. Die Abrechnungsregeln, die Sie erstellen können, hängen von den Bedingungen des Projektvertrags und der Projektart ab, z. B. Zeit und Material oder Festpreis, die Sie der Abrechnungsregel zuordnen. Sie können mehr als eine Abrechnungsregel für einen Projektvertrag erstellen. Sie können auch mehreren Projekten, die demselben Projektvertrag zugeordnet sind und ähnliche Abrechnungsbedingungen haben, eine Abrechnungsregel zuweisen. 

Sie können die folgenden Typen der Abrechnungsregeln einrichten:

-   **Liefereinheit** – Stellen Sie einem Kunden eine Rechnung, wenn Sie eine Liefereinheit fertiggestellt haben. Die Liefereinheiten definieren Sie im Vertrag.
-   **Fortschritt** – Stellen Sie einem Kunden eine Rechnung, wenn Sie einen bestimmten Prozentsatz des Projekts abgeschlossen haben. Sie können eine Abrechnungsregel einrichten, um den Prozentsatz der abgeschlossenen Arbeit automatisch zu berechnen, oder Sie können den Prozentsatz der abgeschlossenen Arbeit und den Rechnungsbetrag für den Kunden manuell berechnen.
-   **Meilenstein** – Rechnungsstellung eines Kunden über den vollen Betrag eines Projektmeilensteins, wenn der Meilenstein erreicht ist.
-   **Gebühr** – Rechnungsstellung eines Kunden für Ihre Dienstleistungen zuzüglich einer Verwaltungsgebühr, die in der Regel einen Prozentsatz der Kosten für Dienstleistungen ausmacht.
-   **Aufwand** – Berechnen Sie einem Kunden den Wert des Aufwands, der für ein Projekt verwendet wird.

Für alle Arten von Abrechnungsregeln können Sie einen Aufbewahrungsprozentsatz angeben, der von den Kundenrechnungen abgezogen wird, bis ein Projekt eine vereinbarte Phase erreicht. Der Prozentsatz der Zahlungsaufbewahrung ist im Projektvertrag festgelegt. Der Betrag wird basierend auf dem Gesamtwert der Zeilen in einer Kundenrechnung berechnet und von diesem abgezogen. 

Für die Abrechnungsregeln **Aufwand** und **Fortschritt** können Sie kostenpflichtige Kategorien zuweisen. Kostenpflichtige Kategorien geben die Transaktionen an, die in Kundenrechnungen enthalten sein sollen. 

Wenn Sie bereit sind, dem Kunden eine Rechnung zu stellen, wird der Rechnungsbetrag für das Projekt basierend auf den Abrechnungsregeln berechnet und ein Projektrechnungsvorschlag generiert. 

In den folgenden Abschnitten finden Sie Beispiele zum Einrichten und Verwalten von Abrechnungsregeln für ein Projekt.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Beispiel: Erstellen Sie eine Abrechnungsregel, die auf der Anzahl der gelieferten Einheiten basiert

Ihre Organisation schließt eine Vereinbarung über die Bereitstellung von insgesamt fünf Schulungssitzungen für die Mitarbeiter eines Kunden zu einem Preis von 10.000 pro Schulungssitzung. Sie stellen dem Kunden nach jeder Schulung eine Rechnung. 

Wenn Sie die Abrechnungsregeln für den Vertrag einrichten, verwenden Sie die folgenden Werte:

-   Die Liefereinheit ist eine Schulungssitzung.
-   Der Stückpreis beträgt 10.000 pro Schulungseinheit.
-   Die Gesamtzahl der Einheiten beträgt fünf Schulungseinheiten.

Wenn Sie eine Schulungssitzung abgeschlossen haben, können Sie für die erste gelieferte Einheit eine Rechnung über 10.000 erstellen und die Rechnung an den Kunden senden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Beispiel: Erstellen Sie eine Abrechnungsregel, die auf einem bestimmten Prozentsatz des Projektabschlusses basiert (manuelle Berechnung)

Ihre Organisation, ein Software-Beratungsunternehmen, schließt mit einem Kunden eine Vereinbarung über die Entwicklung eines Teils eines Produkts, das der Kunde entwickelt. Ihre Organisation verpflichtet sich, den Software-Code über einen Zeitraum von sechs Monaten bereitzustellen. Der Kunde verpflichtet sich, Ihrer Organisation insgesamt 100.000 für die Arbeit zu zahlen. Sie erstellen eine Abrechnungsregel, um dem Kunden eine Rechnung zu stellen, die auf dem im Vertrag angegebenen Prozentsatz der im Projekt abgeschlossenen Arbeiten basiert.

-   Am Ende des ersten Monats treffen Sie sich mit dem Kunden, um den Prozentsatz der abgeschlossenen Arbeiten zu bestimmen. Nachdem Sie und der Kunde das Projekt überprüft haben, entscheiden Sie, dass das Projekt zu 15 Prozent abgeschlossen ist.
-   Sie erstellen eine Rechnung für 15.000 (15 Prozent von 100.000) und senden sie an den Kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Beispiel: Erstellen Sie eine Abrechnungsregel, die auf einem bestimmten Prozentsatz des Projektabschlusses basiert (automatische Berechnung)

Ihre Organisation, eine Softwareentwicklungsfirma, erklärt sich bereit, ein Lohnbuchhaltungspaket für einen Kunden für 30.000 zu entwickeln. Der Kunde verpflichtet sich, Ihre Organisation basierend auf der in Prozent abgeschlossenen Arbeit zu bezahlen. Sie schätzen, dass die Projektkosten 20.000 betragen. Der Projektvertrag legt die Arbeitskategorien fest, die Sie im Abrechnungsprozess verwenden. Sie richten Abrechnungsregeln ein, die automatisch die Rechnungsbeträge für den Prozentsatz der abgeschlossenen Arbeit für jede Kategorie berechnen. Sie richten für jede Kategorie ein Budget ein:

-   **Entwicklung** – Kosten von 15.000 und Einnahmen von 20.000
-   **Entwicklung** – Kosten von 5.000 und Umsatz von 10.000

Wenn Sie zum ersten Mal eine Kundenrechnung erstellen, wird der Rechnungsbetrag automatisch anhand der folgenden Informationen berechnet:

-   Nach einem Monat legt der Projektmitarbeiter eine Arbeitszeittabelle für das Projekt vor. Die Arbeitsstunden betragen 5.000 für die Entwicklung und 1.000 für die Installation. Die Entwicklungsarbeiten sind zu 33 Prozent abgeschlossen (5.000 tatsächliche Kosten/15.000 Budgetkosten) und die Installationsarbeiten zu 20 Prozent abgeschlossen (1.000 tatsächliche Kosten/5.000 Budgetkosten).
-   Der Rechnungsbetrag von 8.667 wird automatisch berechnet (33 Prozent von 20.000 + 20 Prozent von 10.000).
-   Sie erstellen eine Rechnung für 8667 und senden sie an den Kunden.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Beispiel: Erstellen Sie eine Abrechnungsregel, die auf vereinbarten Meilensteinen basiert

Ihre Organisation, eine Unternehmensberatung, erklärt sich bereit, Marktforschungen für ein Verbraucherprodukt durchzuführen, das der Kunde verkaufen möchte. Der Kunde verpflichtet sich, Ihre Dienste ab März für einen Zeitraum von drei Monaten zu nutzen, und verpflichtet sich, Ihrer Organisation 50.000 zu zahlen. Das Projekt hat drei Meilensteine:

-   Meilenstein 1: Verbraucherdaten sammeln – 31. März
-   Meilenstein 2: Verbraucherdaten analysieren – 30. April
-   Meilenstein 3: Vorlage eines Vorschlags zur Produktlebensfähigkeit – 31. Mai

Der Kunde verpflichtet sich, Ihrer Organisation 10.000 für den ersten Meilenstein, 20.000 für den zweiten Meilenstein und 20.000 für den dritten Meilenstein zu zahlen. 

Wenn Sie den Projektvertrag einrichten, erklären Sie sich damit einverstanden, dem Kunden den Meilenstein in Rechnung zu stellen, der abgeschlossen wurde. Das Einrichten der Abrechnungsregeln umfasst die folgenden Schritte:

-   Projektmeilensteine definieren.
-   Definieren Sie den Betrag, der dem Kunden nach Abschluss jedes Meilensteins in Rechnung gestellt werden soll.

Wenn der erste Meilenstein am 31. März abgeschlossen ist, markieren Sie den Meilenstein als abgeschlossen, erstellen eine Rechnung über 10.000 und senden sie an den Kunden. Sie können keine Rechnung für einen Meilenstein erstellen, bis Sie den Meilenstein als abgeschlossen markiert haben.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Beispiel: Erstellen Sie eine Abrechnungsregel, die auf Services zuzüglich einer Verwaltungsgebühr basiert

Ihre Organisation, eine Unternehmensberatung, erklärt sich bereit, Marktforschungen durchzuführen, um die Lebensfähigkeit eines Produkts zu bewerten, das der Kunde, ein Einzelhandelsunternehmen, entwickelt. In den Vertragsbedingungen ist festgelegt, dass Sie die Dienste Ihrer drei wichtigsten Unternehmensberater erbringen, die die Recherchen zeit- und materialbezogen durchführen. Der Kunde verpflichtet sich, 100 pro Stunde zuzüglich einer Verwaltungsgebühr von 10 Prozent für die dem Projekt in Rechnung gestellten Beratungsstunden zu zahlen. 

Erstellen Sie beim Einrichten des Projektvertrags eine Abrechnungsregel, um eine Verwaltungsgebühr von 10 Prozent zu den Beratungsstunden hinzuzufügen, die dem Projekt in Rechnung gestellt werden. 

Wenn Sie eine Rechnung für den Kunden erstellen, wird dem Kunden eine Verwaltungsgebühr von 10 Prozent zuzüglich der Kosten für die Beratungsstunden in Rechnung gestellt. Wenn die drei Berater beispielsweise insgesamt 200 Stunden an dem Projekt gearbeitet haben, wird auf der Grundlage der folgenden Berechnung eine Rechnung über 22.000 erstellt:

-   200 Stunden bei 100 pro Stunde = 20.000
-   10 Prozent Verwaltungsgebühr = 2.000
-   Gesamtbetrag = 22.000

Wenn für einen Kunden Gebühren steuerpflichtig sind und Sie im Projektvertrag eine Umsatzsteuergruppe auswählen, wird die Umsatzsteuergruppe automatisch in eine Abrechnungsregel für Gebühren eingetragen.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Beispiel: Erstellen Sie eine Abrechnungsregel für den Wert von Zeit und Material

Ihre Organisation, eine Softwareberatungsfirma, verpflichtet sich, fünf technische Berater zur Verfügung zu stellen, die für die nächsten sechs Monate an einem Softwareentwicklungsprojekt für einen Kunden arbeiten. Der Kunde verpflichtet sich, 150 pro Beratungsstunde zuzüglich der Kosten für Büromaterial zu zahlen. Ihre Organisation sendet am Ende eines jeden Monats eine Rechnung an den Kunden. 

Wenn Sie den Projektvertrag abschließen, erklären Sie sich damit einverstanden, dem Kunden jeden Monat Zeit und Material für das Projekt in Rechnung zu stellen. Sie erstellen eine Abrechnungsregel, die folgende Informationen enthält:

-   Die Vertragslaufzeit beträgt sechs Monate.
-   Die Beratungszeit wird mit 150 pro Stunde berechnet.
-   Büromaterial wird zu Anschaffungskosten in Rechnung gestellt, und die Gesamtkosten für das Projekt dürfen 10.000 nicht überschreiten.
-   Sie erstellen am Ende jedes Kalendermonats während des Projekts eine Kundenrechnung.

Im ersten Monat werden von den Beratern des Projekts insgesamt 800 Stunden aufgezeichnet. Die Kosten für Büromaterial, das dem Projekt in Rechnung gestellt wird, betragen 2.000. Daher erstellen Sie am Monatsende eine Rechnung über 122.000, die als 800 Stunden bei 150 pro Stunde plus 2.000 für Büromaterial berechnet wird.





[!INCLUDE[footer-include](../includes/footer-banner.md)]