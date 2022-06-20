---
title: Die kostenpflichtigen Komponenten einer Angebotszeile konfigurieren
description: Dieser Artikel enthält Informationen über das Festlegen von berechenbaren und nicht berechenbaren Komponenten in einer projektbasierten Angebotszeile.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930041"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Die kostenpflichtigen Komponenten einer Angebotszeile konfigurieren 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_

Eine projektbasierte Angebotszeile umfasst das Konzept *enthaltener* Komponenten und *fakturierbarer* Komponenten.

Enthaltene Komponenten unterliegen Folgendem:

  - Fakturierungsmethode und Kundenaufteilung
  - Nicht zu überschreitende Grenzwerte 
  - In der projektbasierten Angebotszeile definierte Einstellungen für die Rechnungshäufigkeit

Eine Teilmenge der eingeschlossenen Komponenten kann mit dem Feld **Fakturierungstyp** als fakturierbar markiert werden. Das Feld **Fakturierungstyp** ist ein Optionssatz, der die folgenden Werte im Kontext einer Angebotszeile zulässt:

  - Fakturierbar
  - Nicht fakturierbar

Fakturierbare Komponenten können für die Kategorien Aufgaben, Rollen und Transaktionen definiert werden.

Die Fakturierbarkeit wird für Aufgaben für eine Angebotszeile definiert und gilt für alle in dieser Zeile enthaltenen Transaktionsklassen. Wenn das Feld **Aufgaben einschließen** auf **Gesamtes Projekt** festgelegt wurde oder leer ist, ist die Registerkarte **Fakturierbare Aufgaben** nicht verfügbar.

Die für Rollen für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**. Wenn das Feld **Zeit einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.

Die für Transaktionskategorien für eine Angebotszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**. Wenn das Feld **Ausgaben einschließen** in einer Projektangebotszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Eine Projektaufgabe als fakturierbar oder nicht fakturierbar aktualisieren

Eine Projektaufgabe kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird.

Wenn eine projektbasierte Angebotszeile **Zeit** und die Aufgabe **T1** enthält, wird die Aufgabe der Angebotszeile als fakturierbar zugeordnet. Wenn es eine zweite Angebotszeile gibt, die **Ausgaben** enthält, können Sie die **T1**-Aufgabe in der Angebotszeile als nicht fakturierbar zuordnen. Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle für die Aufgabe aufgezeichneten Ausgaben nicht fakturierbar sind.

Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** einer projektbasierten Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Angebotszeilenaufgaben** aktualisiert wird. Alternativ können Sie den Fakturierungstyp für eine Projektaufgabe im Feld **Fakturierungstyp** im Unterraster der Aufgabenabrechnungseinrichtung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Angebotszeilen angezeigt werden.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren

Eine Rolle kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Rolle kann auf der Registerkarte **Fakturierbare Rollen** einer Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Fakturierbare Rollen** aktualisiert wird.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren

Eine Transaktionskategorie kann für eine bestimmte Angebotszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer Angebotszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster **Fakturierbare Kategorien** aktualisiert wird.

### <a name="resolve-chargeability"></a>Fakturierbarkeit abschließen
Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:

   - **Zeit** ist in der Angebotszeile enthalten.
   - **Rolle** ist in der Angebotszeile als fakturierbar konfiguriert.
   - **Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**. 

Wenn diese drei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert. 

Eine für den Aufwand erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn: 

   - **Ausgaben** ist in der Angebotszeile enthalten.
   - **Transaktionskategorie** ist in der Angebotszeile als fakturierbar konfiguriert.
   - **Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**.

Wenn diese drei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert. 

Eine für die Materialien erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:

   - **Material** ist in der Angebotszeile enthalten.
   - **Enthaltene Aufgaben** ist in der Angebotszeile eingestellt auf **Ausgewählte Aufgaben**.

Wenn diese zwei Dinge zutreffen, wird die **Aufgabe** auch als fakturierbar konfiguriert. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Schließt Zeit ein</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Schließt Ausgaben ein</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Enthält Material</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Eingeschlossene Aufgaben</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rolle</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kateg.</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Aufgabe</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Auswirkungen auf die Fakturierbarkeit</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht Fakturierbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Nur ausgewählte Aufgaben </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht verfügbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ja </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht verfügbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: Fakturierbar </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="70" valign="top">
                <p>
Fakturierbar </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ja </p>
            </td>
            <td width="78" valign="top">
                <p>
Ja </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Keine</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Gesamtes Projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht eingestellt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Nicht fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Nicht verfügbar</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
