---
title: Projektbasierte Angebotspositionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung projektbasierter Angebotspositionen für die Projektarbeit.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994855"
---
# <a name="project-based-quote-lines-overview"></a>Projektbasierte Angebotspositionen – Übersicht 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_

Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen. Die Struktur einer projektbasierten Angebotsposition wird für Projektvorkalkulationen um folgende Konzepte erweitert:

- Fakturierungsmethode
- Projekt- und Aufgabenzuordnung
- Eingeschlossene Transaktionsklassen
- Nicht zu überschreitender Grenzwert
- Fakturierbarkeitseinrichtung
- Schätzung unter Verwendung von Angebotspositionsdetails
- Angebotszeilenkunden

Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile. Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Name des Dataflows | Der Name der Angebotszeile, mit dessen Hilfe Sie die diskrete Komponente des Angebots identifizieren können, die geschätzt wird. | Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Fakturierungsmethode | Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert. Dieses Feld enthält die beiden Haupt-Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</br>- Festpreis</br>- Zeit und Materialien| Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Project | Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird. Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails. Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird.|
| Eingeschlossene Aufgaben | Gibt an, ob diese Angebotsposition für alle oder einige der Projektaufgaben für das ausgewählte Projekt verwendet wird. Dieses Feld weist die möglichen Werte auf:</br>- Alle Projektaufgaben</br>- Nur ausgewählte Projektaufgaben</br>Ein leerer Wert in diesem Feld entspricht der Option **Alle Projektaufgaben**. | Wenn **Nur ausgewählte Projektaufgaben** auf der Projektseite ausgewählt wurde, können Sie auf der **Einrichtung der Aufgabenfakturierung**-Registerkarte bestimmte Aufgaben auswählen, um sie dieser Angebotszeile zuzuordnen. Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Zeit einschließen | Ein Wert von **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden. Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Ausgaben einschließen | Ein Wert von **Ja**/**Nein** gibt an, ob die Ausgabenkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden. Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Material einschließen | Ein Wert von **Ja**/**Nein** gibt an, ob die Materialkosten für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden. Ein Wert von **Nein** gibt an, dass die Materialkosten nicht in die Schätzung in dieser Angebotszeile einbezogen werden. Ein Wert von **Ja** gibt an, dass die Materialkosten in die Schätzung in dieser Angebotszeile einbezogen werden. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Gebühr einschließen | Ein Wert von **Ja**/**Nein** gibt an, ob die Gebühren für das ausgewählte Projekt in die Schätzung in dieser Angebotszeile einbezogen werden. Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Angebotsbetrag | Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotszeile prognostizierten Arbeiten angeboten wird. Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert. Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Geschätzte Steuer | Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann. Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Nettoangebotsbetrag | Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt. Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Nicht zu überschreitender Grenzwert | Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Kundenbudget | Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde. | Dieser Wert wird in die Projektvertragszeile kopiert, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen

**Regel 1**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, ist ein Projekt in der Angebotsposition einbezogen.

**Regel 2**: Wenn das Feld **Eingeschlossene Aufgaben** leer oder auf **Alle Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.

**Regel 3**: Wenn das Feld **Eingeschlossene Aufgaben** auf **Nur ausgewählte Projektaufgaben** festgelegt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Angebotspositionen eines Angebots enthalten sein.

**Regel 4**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.

**Regel 5**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Verkaufschance</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Angebot</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Angebotsposition</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Eingeschlossene Aufgaben</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Zeit einschließen</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Ausgaben einschließen</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Material einschließen</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Einschließen</strong>
                </p>
                <p>
                    <strong>Gebühr</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Gültig/Nicht gültig</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Grund</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 Zeit, Kosten und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 Zeit, Material und Gebühren für das P1-Projekt sind in den Angebotspositionen QL1 und QL2 enthalten </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Zeit, Material und Gebühren für das P1-Projekt sind in QL1 enthalten <br>
Die Kosten für das P1-Projekt sind in QL2 enthalten <br>
Keine Überlappung in dem, was in jeder Angebotszeile enthalten ist und daher gültig ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="41" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 </p>
                <p>
Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1 </p>
                <p>
QL2 enthält Zeit, Ausgaben und Gebühren für das gesamte Projekt P1 und überschneidet sich daher mit dem, was in Q1 enthalten ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Gemäß Regel 3, </p>
                <p>
Q1 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.
                </p>
                <p>
QL2 umfasst Zeit, Material, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.
                </p>
                <p>
Die einzige zusätzliche Validierung betrifft die Teilmenge der Aufgaben in QL1, die sich von der Teilmenge der Aufgaben in QL2 unterscheidet, um sicherzustellen, dass es keine Überlappung gibt. Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle Projektaufgaben oder leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Gemäß Regel 5 sind Q1 und Q2 zwei Anführungszeichen für dieselbe Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle Projektaufgaben oder leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle Projektaufgaben oder leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Gemäß Regel 4 sind Q1 und Q2 zwei Anführungszeichen für verschiedene Verkaufschance, sodass beide für dieselben Komponenten eines Projekts schätzen können.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle Projektaufgaben oder leer </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
