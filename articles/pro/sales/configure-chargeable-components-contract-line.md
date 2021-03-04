---
title: Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren – Lite
description: Dieses Thema enthält Informationen zum Hinzufügen fakturierbarer Komponenten zu Vertragszeilen in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513878"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Kostenpflichtige Komponenten einer projektbasierten Vertragszeile konfigurieren – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

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

Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn **Zeit** in der Vertragszeile enthalten ist und **Aufgabe** und **Rolle** in der Vertragszeile als fakturierbar konfiguriert sind.

Eine für die Ausgabe erstellte Vorkalkulation oder ein Istwert wird nur dann als fakturierbar angesehen, wenn **Ausgaben** in der Vertragszeile enthalten ist und die Kategorien **Aufgabe** und **Transaktion** in der Vertragszeile als fakturierbar konfiguriert sind.


| Schließt Zeit ein | Schließt Ausgaben ein | Schließt Aufgaben ein | Rolle           | Kateg.       | Task                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Gesamtes Projekt | Fakturierbar     | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Fakturierbar**           |
| Ja           | Ja              | Ausgewählte Aufgaben | Fakturierbar     | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Fakturierbar**           |
| Ja           | Ja              | Ausgewählte Aufgaben | Nicht fakturierbar | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Fakturierbar**       |
| Ja           | Ja              | Ausgewählte Aufgaben | Fakturierbar     | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht fakturierbar** |
| Ja           | Ja              | Ausgewählte Aufgaben | Nicht fakturierbar | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht fakturierbar** |
| Ja           | Ja              | Ausgewählte Aufgaben | Nicht fakturierbar | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht fakturierbar** |
| Nr.            | Ja              | Gesamtes Projekt | Kann nicht festgelegt werden   | Fakturierbar     | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht verfügbar**</br>Fakturierungstyp bei tatsächlichen Ausgaben: **Fakturierbar**          |
| Nr.            | Ja              | Gesamtes Projekt | Kann nicht festgelegt werden   | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht verfügbar**</br> Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht fakturierbar**     |
| Ja           | Nr.               | Gesamtes Projekt | Fakturierbar     | Kann nicht festgelegt werden   | Abrechnung zu einem tatsächlichen Zeitpunkt: **Fakturierbar** </br> Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht verfügbar**        |
| Ja           | Nr.               | Gesamtes Projekt | Nicht fakturierbar | Kann nicht festgelegt werden   | Abrechnung zu einem tatsächlichen Zeitpunkt: **Nicht fakturierbar** </br>Fakturierungstyp bei tatsächlichen Ausgaben: **Nicht verfügbar**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]