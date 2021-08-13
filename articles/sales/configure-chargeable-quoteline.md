---
title: Die kostenpflichtigen Komponenten einer projektbasierten Angebotsposition konfigurieren
description: Dieses Thema enthält Informationen zu enthaltenen, kostenpflichtigen und nicht kostenpflichtigen Komponenten in projektbasierten Angebotszeilen.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003995"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Die kostenpflichtigen Komponenten einer projektbasierten Angebotsposition konfigurieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Eine projektbasierte Angebotszeile kann Komponenten und kostenpflichtige Komponenten enthalten.

Enthaltene Komponenten unterliegen der Abrechnungsmethode, Kundensplits, nicht zu überschreitenden Grenzwerten und Rechnungshäufigkeitseinstellungen, die in der projektbasierten Angebotszeile definiert sind.
Eine Teilmenge der enthaltenen Komponenten kann mithilfe von **Abrechnungsart** als kostenpflichtig markiert werden. Sie können eine der folgenden Optionen im **Abrechnungsart**-Feld im Kontext einer Anführungszeichenzeile auswählen:

   - Fakturierbar
   - Nicht fakturierbar

Fakturierbare Komponenten können für die Kategorien Rollen und Transaktionen definiert werden.

Die für Rollen für eine Projektangebotszeile definierte Aufladbarkeit gilt nur für die **Zeit**-Transaktionsklasse. Wenn eine Projektangebotszeile **Zeit einschließen** = **Nein** festgelegt hat, ist die **Fakturierbare Rollen**-Registerkarte nicht verfügbar.

Die für Transaktionskategorien für eine Projektangebotszeile definierte Aufladbarkeit gilt nur für die **Ausgaben**-Transaktionsklasse. Wenn eine Projektangebotszeile **Ausgaben einschließen** = **Nein** festgelegt hat, ist die **Fakturierbare Kategorien**-Registerkarte nicht verfügbar.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Eine Rolle als fakturierbar oder nicht fakturierbar aktualisieren
Eine Rolle kann in einer projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein. Die Abrechnungsart für eine Rolle kann auf der **Fakturierbare Rollen**-Registerkarte einer projektbasierten Angebotszeile konfiguriert werden. Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Rollen**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Eine Transaktionskategorie als fakturierbar oder nicht fakturierbar aktualisieren
Eine Transaktionskategorie kann in einer projektbasierten Angebotszeile fakturierbar oder nicht fakturierbar sein. Die Abrechnungsart für eine Transaktionskategorie kann auf der **Fakturierbare Kategorien**-Registerkarte einer projektbasierten Angebotszeile konfiguriert werden. Aktualisieren Sie dazu das **Fakturierungstyp**-Feld auf dem Unterraster **Fakturierbare Kategorien**. 

## <a name="resolve-chargeability"></a>Fakturierbarkeit abschließen

Eine für die Zeit erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn die Zeit in der Angebotszeile enthalten ist und die Rolle als fakturierbar konfiguriert ist.
Eine für die Ausgaben erstellte Schätzung oder tatsächliche Schätzung wird nur dann als fakturierbar angesehen, wenn die Ausgaben in der Angebotszeile enthalten sind und die Transaktionskategorie auf der Angebotszeile als fakturierbar konfiguriert ist. Die folgende Tabelle zeigt, wie die Aufladbarkeit standardmäßig für jeden tatsächlichen Wert festgelegt ist. Die Standardeinstellungen basieren auf den enthaltenen Komponenten und der Abrechnungsart, die in der Angebotszeile eingerichtet ist.

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