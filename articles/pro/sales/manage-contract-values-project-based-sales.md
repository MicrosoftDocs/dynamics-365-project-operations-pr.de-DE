---
title: Projektbasierte Vertragszeilen – Übersicht
description: Dieses Thema enthält Informationen zur Arbeit mit projektbasierten Vertragszeilen.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 7da8a7f898e6f0bb46d4cf6de65812e3aabb7416a2fdf2f9d9c8bad07e77cd85
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999045"
---
# <a name="project-based-contract-lines-overview"></a>Projektbasierte Vertragszeilen – Übersicht

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektbasierte Vertragszeilen in Dynamics 365 Project Operations dienen dazu, die Kostenvoranschlags- und Abrechnungsvereinbarungen für bestimmte Komponenten der Projektarbeit an einem Auftrag zu speichern. Die Struktur einer projektbasierten Vertragszeile wird für Projektschätzungen und Abrechnungsszenarien um folgende Konzepte erweitert:

- Abrechnungsmethode
- Projekt‑ und Aufgabenzuordnung
- Eingeschlossene Transaktionsklassen
- Nicht zu überschreitender Grenzwert
- Fakturierbarkeitseinrichtung
- Schätzungen unter Verwendung von Vertragszeilendetails
- Vertragszeilenkunden

Die folgende Tabelle enthält die Felder auf der **Allgemein**-Registerkarte mit projektbasierten Vertragszeilen, mit deren Hilfe die Grundlage für eine detaillierte, grundlegende Schätzung und Abrechnungsmodalitäten für projektbasierte Arbeiten geschaffen werden kann.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| **Name** | Name der Vertragszeile. Dies identifiziert die diskrete Komponente des Vertrags, die geschätzt wird. Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Wert der projektbasierten Angebotszeile kopiert. | Der Name, der in die Projektrechnungszeile kopiert wird, die aus dieser Vertragszeile erstellt wird, wenn die Rechnung erstellt wird. |
| **Fakturierungsmethode** | Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert. Dies ist ein Optionssatz, der die beiden wichtigsten Vertragsmodelle darstellt, die von Project Operations unterstützt werden:</br>- **Festpreis**</br>- **Zeit und Materialien** | Basierend auf der Abrechnungsmethode der referenzierten Vertragszeile wird die eigentliche Transaktion verarbeitet. Wenn die Vertragszeile, auf die sich der Istwert bezieht, über eine Zeit- und Materialabrechnungsmethode verfügt, werden Kosten- und nicht abgerechnete Umsatzdatensätze erstellt. Wenn die Vertragszeile, auf die der Istwert verweist, eine Abrechnungsmethode zum Festpreis hat, wird nur ein Istpreis erstellt. |
| **Project** | Verwenden Sie dieses Feld, um das Projekt zu identifizieren, mit dem die Arbeit an diesem Auftrag ausgeführt wird. | Dieser Wert wird in Verbindung mit **Eingeschlossene Aufgaben** und **Eingeschlossene Transaktionsklassen** verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder geschätzten Zeilendatensatz aufzulösen. |
| **Eingeschlossene Aufgaben** | Gibt an, ob diese Vertragszeile alle Projektaufgaben für das ausgewählte Projekt oder nur eine Teilmenge der Aufgaben enthält. Dies ist ein Optionssatz, der über die folgenden möglichen Werte verfügt:</br>- **Alle Projektaufgaben**</br>- **Nur ausgewählte Projektaufgaben**. Ein leerer Wert in diesem Feld entspricht der Auswahl **Alle Projektaufgaben**. | Wenn **Nur ausgewählte Aufgaben** ausgewählt ist, können Sie bestimmte Aufgaben auswählen und dieser Vertragszeile auf der **Einrichtung der Aufgabenabrechnung**-Registerkarte auf der **Projekt**-Seite zuordnen. Der Wert wird in Verbindung mit **Projekt** und **Eingeschlossene Transaktionsklassen** verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Zeit einschließen** | Ein Wert von **Ja**/**Nein** gibt an, ob Zeittransaktionen oder Arbeitskosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden. Ein **Nein**-Wert zeigt an, dass die Zeittransaktionen oder Arbeitskosten in dieser Vertragszeile enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Ausgaben einschließen** | Ein Wert von **Ja**/**Nein** gibt an, ob die Ausgabenkosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden. Ein **Nein**-Wert zeigt an, dass die Ausgabenkosten in dieser Vertragszeile nicht enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Materialien einschließen** | Ein Wert von **Ja**/**Nein** gibt an, ob die Materialkosten für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden. Ein Wert von **Nein** gibt an, dass die Materialkosten nicht in dieser Vertragszeile einbezogen werden. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Gebühr einschließen** | Ein Wert von **Ja**/**Nein** gibt an, ob Gebühren für das ausgewählte Projekt in dieser Vertragszeile einbezogen werden. Ein **Nein**-Wert zeigt an, dass Gebühren in dieser Vertragszeile nicht enthalten sind. Ein **Ja**-Wert gibt an, dass sie enthalten sind | Dieser Wert wird in Verbindung mit dem Projekt verwendet, um die Vertragszeilenreferenz in einem tatsächlichen oder einem geschätzten Zeilendatensatz aufzulösen. |
| **Vertraglicher Betrag** | Bei einer Festpreisvertragszeile ist dieser Betrag der vereinbarte Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird. Bei einer Zeit- und Materialtransaktionenvertragszeile ist dieser Betrag ein geschätzter Wert, der dem Kunden für alle mit dieser Vertragszeile verbundenen Arbeitskomponenten in Rechnung gestellt wird. Bei einem aus einem Angebot erstellten Projektvertrag wird dieser Wert aus einem entsprechenden Feld der Angebotszeile kopiert. Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Betrag in den Vertragszeilendetails zusammengefasst. | Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Beträge in den Zeilendetails geändert werden. In einer Festpreisvertragszeile wird dieser Wert verwendet, um den Betrag vor Steuern für periodische Abrechnungsmeilensteine zu generieren. |
| **Geschätzte Steuer** | Der Benutzer kann dieses Feld bearbeiten, um den geschätzten Steuerbetrag in die Vertragszeile einzugeben. Wenn eine projektbasierte Vertragszeile Zeilendetails enthält, ist dieses Feld für die Bearbeitung gesperrt und wird aus dem Steuerbetrag in den Vertragszeilendetails zusammengefasst. | Wenn die Vertragszeile Zeilendetails enthält, kann dieser Wert durch Ändern der Steuerbeträge in den Zeilendetails geändert werden. In einer Festpreisvertragszeile wird dieser Wert verwendet, um die Steuern für periodische Abrechnungsmeilensteine zu generieren. |
| **Vertraglicher Nettobetrag** | Der vertragliche Nettobetrag. Dieses Feld ist schreibgeschützt und wird berechnet als **Vertraglicher Betrag + Steuer**. | In einer Festpreisvertragszeile wird dieser Wert verwendet, um die periodische Abrechnungsmeilensteine zu generieren. |
| **Nicht zu überschreitender Grenzwert** | Der Benutzer kann dieses Feld bearbeiten und es ist nur in projektbasierten Vertragszeilen verfügbar, für die die Abrechnungsmethode als Zeit und Material festgelegt ist. | Der Benutzer kann dieses Feld bearbeiten. Wenn ein Istwert für Zeit und Material auf diese Vertragszeile für Zeit und Material verweist, wird der Betrag auf dem Istwert anhand der nicht zu überschreitenden Grenze in der Vertragszeile bewertet. Diese Bewertung wird abgeschlossen, nachdem die bereits ausgegebenen und zugesagten Beträge berücksichtigt wurden. |
| **Kundenbudget** | Dieses Feld kann bearbeitet werden und wird aus dem entsprechenden Feld der Angebotszeile kopiert, wenn der Vertrag aus einem Angebot erstellt wurde. | Dieses Feld wird nur zur Information verwendet und hat keine nachgelagerte Bedeutung. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validierungsregeln für die Optionen auf der Registerkarte „Allgemein“ der projektbasierten Vertragszeilen

Regel 1: Wenn das **Enthaltene Aufgaben**-Feld leer oder auf **Alle Projektaufgaben** gesetzt ist, sind alle Aufgaben des Projekts in der Vertragszeile enthalten.

Regel 2: Wenn das **Enthaltene Aufgaben**-Feld leer oder explizit auf **Alle Projektaufgaben** gesetzt ist, können ein Projekt und eine bestimmte Transaktionsklasse nur in einer projektbasierten Vertragszeile eines Vertrags enthalten sein.

Regel 3: Wenn das **Enthaltene Aufgaben**-Feld leer oder explizit auf **Nur ausgewählte Projektaufgaben** gesetzt ist, können ein Projekt und eine bestimmte Transaktionsklasse in mehreren projektbasierten Vertragszeilen eines Vertrags enthalten sein.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Vertrag</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Vertragszeile</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Eingeschlossene Aufgaben</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Zeit einschließen</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Ausgaben einschließen</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Materialien einschließen</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Gültig/Nicht gültig</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Grund</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 Zeit, Kosten und Materialien für das P1-Projekt sind in den Vertragszeilen CL1 und CL2 enthalten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 Zeit, Materialien und Gebühren für das P1-Projekt sind in den Vertragszeilen CL1 und CL2 enthalten.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Zeit, Materialien und Gebühren für das P1-Projekt sind in CL1 enthalten.
                </p>
                <ul>
                    <li>
Die Kosten für das P1-Projekt sind in CL2 enthalten.
                    </li>
                </ul>
                <p>
Keine Überlappung in dem, was in jeder Vertragszeile enthalten ist und daher gültig ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Nr. </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Nicht gültig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Verstoß gegen Regel 2 </p>
                <p>
C1 umfasst Zeit, Materialien, Ausgaben und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.
                </p>
                <p>
CL2 enthält Zeit, Materialien, Ausgaben und Gebühren für das gesamte Projekt P1 und überschneidet sich daher mit dem, was in C1 enthalten ist.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leer </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Gültig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Gemäß Regel 3 </p>
                <p>
C1 umfasst Zeit, Ausgaben, Materialien und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.
                </p>
                <p>
CL2 umfasst Zeit, Ausgaben, Materialien und Gebühren für eine Teilmenge der Aufgaben in Projekt P1.
                </p>
                <p>
Die einzige zusätzliche Validierung betrifft die Teilmenge der Aufgaben in CL1, die sich von der Teilmenge der Aufgaben in CL2 unterscheidet, um sicherzustellen, dass es keine Überlappung gibt. Dies erfolgt durch das System, wenn Aufgaben zugeordnet sind.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
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
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
