---
title: Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren
description: In diesem Artikel erfahren Sie, wie Sie in Project Operations anrechenbare Komponenten zu Vertragszeilen hinzufügen können.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e4118e8e56d45ef75f53d828e267a8a9c1c903a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922957"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_

Eine projektbasierte Vertragszeile hat *eingeschlossene* Komponenten und *fakturierbare* Komponenten.

Eingeschlossene Komponenten sind Komponenten, die Folgendem unterliegen:

  - Fakturierungsmethode und Kundenaufteilung
  - Nicht zu überschreitende Grenzwerte 
  - In der projektbasierten Vertragszeile definierte Einstellungen für die Rechnungshäufigkeit

Eine Teilmenge der eingeschlossenen Komponenten kann mit dem Feld **Fakturierungstyp** als fakturierbar markiert werden. Das Feld **Fakturierungstyp** ist ein Optionssatz, der die folgenden Werte im Kontext einer Vertragszeile zulässt:

  - Fakturierbar
  - Nicht fakturierbar

Fakturierbare Komponenten können für die Kategorien Aufgaben, Rollen und Transaktionen definiert werden.

Die Fakturierbarkeit wird für Aufgaben für eine Projektvertragszeile definiert und gilt für alle in der Zeile enthaltenen Transaktionsklassen. Wenn das Feld **Aufgaben einschließen** in einer Vertragszeile leer ist oder auf **Gesamtes Projekt** festgelegt wurde, ist die Registerkarte **Fakturierbare Aufgaben** nicht verfügbar.

Die für Rollen für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**. Wenn das Feld **Zeit einschließen** in einer Vertragszeile leer ist oder auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.

Die für Transaktionskategorien für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**. Wenn das Feld **Ausgaben einschließen** in einer Vertragszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Eine Projektaufgabe als fakturierbar oder nicht fakturierbar aktualisieren

Eine Projektaufgabe kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird:

Wenn eine projektbasierte Vertragszeile **Zeit** enthält und eine bestimmte Aufgabe, **T1**, dieser Zeile als fakturierbar zugeordnet ist Wenn es eine zweite Vertragszeile gibt, die **Ausgaben** enthält, können Sie die T1-Aufgabe in der Vertragszeile als nicht fakturierbar zuordnen. Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle Ausgaben nicht fakturierbar sind.

Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** der Vertragszeile konfiguriert werden, indem das **Fakturierungstyp**-Feld im Unterraster für Vertragszeilenaufgaben aktualisiert wird. Alternativ können Sie das **Fakturierungstyp**-Feld im Unterraster der Aufgabenabrechnungseinrichtung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Vertragszeilen angezeigt werden.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren

Eine Rolle kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Rolle kann auf der Registerkarte **Fakturierbare Rollen** einer Vertragszeile konfiguriert werden. Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Rollen**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren

Eine Transaktionskategorie kann für eine bestimmte Vertragszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer projektbasierten Vertragszeile konfiguriert werden. Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Kategorien**.

### <a name="resolve-chargeability"></a>Fakturierbarkeit abschließen

Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als steuerpflichtig angesehen, wenn:

   - **Zeit** ist in der Vertragszeile enthalten.
   - **Rolle** ist in der Vertragszeile als fakturierbar konfiguriert.
   - **Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgaben**.
 
 Wenn diese drei Dinge zutreffen, wird die Aufgabe als fakturierbar konfiguriert. 

Eine für den Aufwand erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn:

   - **Aufwand** in der Vertragszeile enthalten ist
   - **Transaktionskategorie** ist in der Vertragszeile als fakturierbar konfiguriert
   - **Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgabe**
  
 Wenn diese drei Dinge zutreffen, wird die **Aufgabe** als fakturierbar konfiguriert. 

Eine für Materialien erstellte Schätzung oder tatsächliche Werte werden nur dann als fakturierbar angesehen, wenn:

   - **Materialien** in der Vertragszeile enthalten ist
   - **Enthaltene Aufgaben** ist in der Vertragszeile eingestellt auf **Ausgewählte Aufgaben**

Wenn diese zwei Dinge zutreffen, wird die **Aufgabe** als fakturierbar konfiguriert. 

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
Kann nicht festgelegt werden </p>
            </td>
            <td width="350" valign="top">
                <p>
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Fakturierbar</strong>
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
Abrechnung zu einem tatsächlichen Zeitpunkt: <strong>Fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Ausgaben: <strong>Fakturierbar</strong>
                </p>
                <p>
Fakturierungstyp bei tatsächlichen Materialien: <strong>Fakturierbar</strong>
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
Kann nicht festgelegt werden </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht festgelegt werden </p>
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
Kann nicht festgelegt werden </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Nicht fakturierbar</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht festgelegt werden </p>
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
Kann nicht festgelegt werden </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht festgelegt werden </p>
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
Kann nicht festgelegt werden </p>
            </td>
            <td width="65" valign="top">
                <p>
Kann nicht festgelegt werden </p>
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
Kann nicht festgelegt werden </p>
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
Kann nicht festgelegt werden </p>
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
