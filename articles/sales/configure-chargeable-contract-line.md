---
title: Fakturierbare Komponenten einer projektbasierten Vertragszeile konfigurieren
description: Dieses Thema enthält Informationen zu eingeschlossenen, fakturierbaren und nicht fakturierbaren Komponenten in Vertragszeilen.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2266d8e0fe998e7161ede4cb4eaf7d3c70c54f71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278687"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Fakturierbare Komponenten einer projektbasierten Vertragszeile konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Eine projektbasierte Vertragszeile umfasst das Konzept eingeschlossener, fakturierbarer und nicht fakturierbarer Komponenten.

Eingeschlossene Komponenten unterliegen der Fakturierungsmethode, Kundenaufteilungen, nicht zu überschreitenden Grenzwerten und Einstellungen zur Rechnungshäufigkeit, die in der projektbasierten Vertragszeile definiert sind.

Eine Teilmenge der eingeschlossenen Komponenten kann durch Aktualisierung des Felds **Fakturierungstyp** als fakturierbar markiert werden.

Fakturierbare Komponenten können für die Kategorien Rollen und Transaktionen definiert werden.

Die für Rollen für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Zeit**. Wenn das Feld **Zeit einschließen** in einer Projektvertragszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Rollen** nicht verfügbar.

Die für Transaktionskategorien für eine Projektvertragszeile festgelegte Fakturierbarkeit gilt nur für die Transaktionsklasse **Ausgaben**. Wenn das Feld **Ausgaben einschließen** in einer Projektvertragszeile auf **Nein** festgelegt wurde, ist die Registerkarte **Fakturierbare Kategorien** nicht verfügbar.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren

Eine Rolle kann für eine bestimmte projektbasierte Vertragszeile fakturierbar oder nicht fakturierbar sein.

Aktualisieren Sie auf der Registerkarte **Fakturierbare Rollen** einer projektbasierten Vertragszeile im Unterraster **Fakturierbare Kategorien** im **Fakturierungstyp**-Feld den Fakturierungstyp für eine Rolle.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren

Eine Transaktionskategorie kann für eine bestimmte projektbasierte Vertragszeile fakturierbar oder nicht fakturierbar sein.

Aktualisieren Sie auf der Registerkarte **Fakturierbare Kategorien** einer projektbasierten Vertragszeile im Unterraster **Fakturierbare Kategorien** im **Fakturierungstyp**-Feld den Fakturierungstyp für eine Transaktion.

### <a name="resolve-chargeability"></a>Fakturierbarkeit abschließen

Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn Zeit in der Vertragszeile enthalten und Rolle in der Vertragszeile als fakturierbar konfiguriert ist.

Eine für die Ausgabe erstellte Vorkalkulation oder ein Istwert wird nur dann als fakturierbar angesehen, wenn Ausgaben in der Vertragszeile enthalten sind und die Transaktionskategorie in der Vertragszeile als fakturierbar konfiguriert ist.

| Schließt Zeit ein | Schließt Ausgaben ein | Rolle | Kateg. | Task |
| --- | --- | --- | --- | --- |
| Ja | Ja | Fakturierbar | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Ja | Ja | Nicht fakturierbar | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Ja | Ja | Nicht fakturierbar | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Nr. | Ja | Kann nicht festgelegt werden | Fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Fakturierbar |
| Nr. | Ja | Kann nicht festgelegt werden | Nicht fakturierbar | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht verfügbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht fakturierbar |
| Ja | Nr. | Fakturierbar | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Fakturierbar </br>Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar |
| Ja | Nr. | Nicht fakturierbar | Kann nicht festgelegt werden | Abrechnung zu einem tatsächlichen Zeitpunkt: Nicht fakturierbar </br> Fakturierungstyp bei tatsächlichen Ausgaben: Nicht verfügbar |


[!INCLUDE[footer-include](../includes/footer-banner.md)]