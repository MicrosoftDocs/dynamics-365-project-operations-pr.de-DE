---
title: Die fakturierbaren Komponenten einer Angebotszeile konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten fakturierbarer und nicht fakturierbarer Komponenten in einer projektbasierten Angebotszeile.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076645"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Die fakturierbaren Komponenten einer Angebotszeile konfigurieren

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

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

Eine Projektaufgabe kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein, wodurch das folgende Setup möglich wird:

Wenn eine projektbasierte Angebotszeile **Zeit** und die Aufgabe **T1** enthält, wird die Aufgabe der Angebotszeile als fakturierbar zugeordnet. Wenn es eine zweite Angebotszeile gibt, die **Ausgaben** enthält, können Sie die **T1** -Aufgabe in der Angebotszeile als nicht fakturierbar zuordnen. Das Ergebnis ist, dass die gesamte für die Aufgabe aufgezeichnete Zeit fakturierbar ist und alle für die Aufgabe aufgezeichneten Ausgaben nicht fakturierbar sind.

Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Aufgaben** einer projektbasierten Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Angebotszeilenaufgaben** konfiguriert werden. Alternativ können Sie den Fakturierungstyp für eine Projektaufgabe im Feld **Fakturierungstyp** im Unterraster der Einrichtung der Aufgabenfakturierung eines Projekts aktualisieren, in dem die einer Aufgabe zugeordneten Angebotszeilen angezeigt werden.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren

Eine Rolle kann im Kontext einer bestimmten projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Aufgabe kann auf der Registerkarte **Fakturierbare Rollen** einer Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Fakturierbare Rollen** konfiguriert werden.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren

Eine Transaktionskategorie kann für eine bestimmte Angebotszeile fakturierbar oder nicht fakturierbar sein.

Der Fakturierungstyp einer Transaktion kann auf der Registerkarte **Fakturierbare Kategorien** einer Angebotszeile durch Aktualisieren des Felds **Fakturierungstyp** im Unterraster **Fakturierbare Kategorien** konfiguriert werden.

### <a name="resolve-chargeability"></a>Fakturierbarkeit abschließen
Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn **Zeit** in der Angebotszeile enthalten ist und **Aufgabe** und **Rolle** in der Angebotszeile als fakturierbar konfiguriert sind.

Eine für die Ausgabe erstellte Vorkalkulation oder ein Istwert wird nur dann als fakturierbar angesehen, wenn **Ausgaben** in der Angebotszeile enthalten ist und **Aufgabe** und **Transaktionskategorie** in der Angebotszeile als fakturierbar konfiguriert sind.

| Schließt Zeit ein | Schließt Ausgaben ein | Eingeschlossene Aufgaben | Rolle | Kateg. | Task | Fakturierung |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Gesamtes Projekt | Fakturierbar | Fakturierbar | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Ja | Ja | Nur ausgewählte Aufgaben | Fakturierbar | Fakturierbar | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Ja | Ja | Nur ausgewählte Aufgaben | Nicht fakturierbar | Fakturierbar | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Ja | Ja | Nur ausgewählte Aufgaben | Fakturierbar | Fakturierbar | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</br> Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Ja | Ja | Nur ausgewählte Aufgaben | Nicht fakturierbar | Fakturierbar | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</br> Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Ja | Ja | Nur ausgewählte Aufgaben | Nicht fakturierbar | Nicht fakturierbar | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar</br> Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Nr. | Ja | Gesamtes Projekt | Kann nicht festgelegt werden | Fakturierbar | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Nr. | Ja | Gesamtes Projekt | Kann nicht festgelegt werden | Nicht fakturierbar | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Ja | Nr. | Gesamtes Projekt | Fakturierbar | Kann nicht festgelegt werden | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar</br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar |
| Ja | Nr. | Gesamtes Projekt | Nicht fakturierbar | Kann nicht festgelegt werden | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar |
