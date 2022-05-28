---
title: Projektangebotspositionen – Übersicht
description: Dieses Thema enthält Informationen zum Verwenden von Projektangebotspositionen für die Projektarbeit.
author: rumant
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 07ee2e6a7823b25eacb1c7ad6180f8af571348bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587033"
---
# <a name="project-quote-lines-overview"></a>Projektangebotspositionen – Übersicht

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Projektbasierte Angebotspositionen sollen helfen, die Projektarbeit für ein Projekt abzuschätzen. Die Struktur einer projektbasierten Angebotsposition wird für Projektvorkalkulationen um folgende Konzepte erweitert:

- Fakturierungsmethode
- Projektzuordnung
- Eingeschlossene Transaktionsklassen
- Nicht zu überschreitender Grenzwert
- Fakturierbarkeitseinrichtung
- Schätzung unter Verwendung von Angebotspositionsdetails
- Angebotszeilenkunden

Die folgende Tabelle enthält Informationen zu den Feldern auf der Registerkarte **Allgemein** der projektbasierten Angebotszeile. Diese Felder bilden die Grundlage für eine detaillierte, grundlegende Schätzung der Projektarbeit.

| **Feld** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- |
| Name des Dataflows | Der Name der Angebotsposition, mit dessen Hilfe Sie die einzelne Komponente des Angebots identifizieren können, die geschätzt wird. | Kopiert in die Projektvertragszeile, die aus dieser Angebotszeile erstellt wird, wenn das Angebot gewonnen wird. |
| Fakturierungsmethode | Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem entsprechenden Feld in der Verkaufschancenposition kopiert. Dieses Feld enthält die beiden Haupt-Vertragsmodelle, die von Dynamics 365 Project Operations unterstützt werden:</br>- Festpreis</br>- Zeit und Materialien| Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Project | Verwenden Sie dieses optionale Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird. Wenn ein Projekt einer Angebotsposition zugeordnet ist, hilft es beim Einrichten kostenpflichtiger Aufgaben und beim Einfügen einer projektbasierten Schätzung in die Angebotsposition als Angebotspositionsdetails. Wenn ein Projekt keiner projektbasierten Angebotsposition zugeordnet ist, sollte die Schätzung manuell erstellt werden, indem jedes Detail der Angebotsposition erstellt wird. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Zeit einschließen | Die Kennzeichnung **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in die Schätzung in dieser Angebotsposition einbezogen werden. Der Wert **Nein** gibt an, dass die Zeittransaktionen oder Arbeitskosten nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Zeittransaktionen oder Arbeitskosten in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Ausgaben einschließen | Die Kennzeichnung **Ja**/**Nein** gibt an, ob Ausgaben für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden. Der Wert **Nein** gibt an, dass die Ausgaben nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Ausgaben in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Gebühr einschließen | Die Kennzeichnung **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in der Schätzung in dieser Angebotsposition einbezogen werden. Der Wert **Nein** gibt an, dass die Gebühren nicht in der Schätzung in dieser Angebotsposition einbezogen sind. Der Wert **Ja** gibt an, dass die Gebühren in der Schätzung in dieser Angebotsposition einbezogen sind. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Angebotsbetrag | Dies ist der Betrag, der dem Kunden für alle in dieser projektbasierten Angebotsposition prognostizierten Arbeiten angeboten wird. Bei einem aus einer Verkaufschance erstellten Angebot wird dieser Wert aus dem Feld **Kundenbudget** in der Verkaufschancenposition kopiert. Wenn die projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Angebotspositionsdetails zusammengefasst. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Geschätzte Steuer | Dies ist ein bearbeitbares Feld, in dem der Benutzer den geschätzten Steuerbetrag in die Angebotsposition einfügen kann. Wenn eine projektbasierte Angebotsposition Positionsdetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Angebotspositionsdetails zusammengefasst. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Nettoangebotsbetrag | Dieses Feld ist der Angebotspositionsbetrag nach Steuern und schreibgeschützt. Der Betrag in diesem Feld wird als *Nettoangebotsbetrag* berechnet. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Nicht zu überschreitender Grenzwert | Dieses Feld kann bearbeitet werden und ist nur in projektbasierten Angebotspositionen mit der verfügbaren Abrechnungsmethode **Zeit und Material** verfügbar. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |
| Kundenbudget | Dieses Feld ist beabeitbar und wird aus dem entsprechenden Feld in der Verkaufschancenposition kopiert, wenn das Angebot aus einer Verkaufschance erstellt wurde. | Dieser Feldwert wird in die Projektvertragszeile kopiert, die aus dieser Angebotsposition erstellt wird, wenn das Angebot gewonnen wird. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Validierungsregeln für Felder auf der Registerkarte „Allgemein“ von projektbasierten Angebotszeilen

**Regel 1**: Eine bestimmte Transaktionsklasse für das ausgewählte Projekt kann nur in einer projektbasierten Angebotsposition eines Angebots enthalten sein.

**Regel 2**: Wenn eine Verkaufschance mehrere Angebote enthält, können Angebotspositionen aus verschiedenen Angeboten vorhanden sein, die alle auf dasselbe Projekt verweisen und dieselbe Transaktionsklasse enthalten.

**Regel 3**: Wenn die Angebote nicht zu derselben Verkaufschance gehören, können sie nicht dasselbe Projekt und dieselbe Transaktionsklasse enthalten.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Verkaufschance</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Angebot</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Angebotsposition</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zeit einbeziehen</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Ausgabe einbeziehen</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Einschließen</strong>
                </p>
                <p>
                    <strong>Gebühr</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Gültig/Nicht gültig</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Grund</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 1 Zeit, Kosten und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 1 Zeit und Gebühren für das P1-Projekt sind in beiden Angebotszeilen QL1 und QL2 enthalten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Zeit und Gebühren für das P1-Projekt sind in QL1 enthalten.
Die Kosten für das P1-Projekt sind in QL2 enthalten.
Es gibt keine Überlappung in dem, was in jeder Angebotsposition enthalten ist, sodass es gültig ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Nr. </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 1 oben </p>
                <p>
Q1 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1.
                </p>
                <p>
QL2 enthält Zeit, Kosten und Gebühren für das gesamte Projekt P1 und überschneidet sich mit dem, was in Q1 enthalten ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Basierend auf Regel 2 sind Q1 und Q2 zwei Angebote für dieselbe Verkaufschance, sodass beide dieselben Komponenten eines Projekts schätzen können.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 in Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Basierend auf Regel 3 sind Q1 und Q2 zwei Angebote für unterschiedliche Verkaufschancen, sodass sie nicht dieselben Komponenten desselben Projekts schätzen können.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="54" valign="top">
                <p>
Nicht gültig </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
