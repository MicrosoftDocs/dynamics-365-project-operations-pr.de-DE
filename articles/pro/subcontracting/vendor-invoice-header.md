---
title: Kopfzeilendetails für Kreditorenrechnungen
description: Dieser Artikel erläutert die Funktionen, die in der Kopfzeile der Lieferantenrechnung in Microsoft Dynamics 365 Project Operations zur Verfügung stehen.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929857"
---
# <a name="header-details-for-vendor-invoices"></a>Kopfzeilendetails für Kreditorenrechnungen

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel erläutert die Funktionen, die in der Kopfzeile der Lieferantenrechnung in Microsoft Dynamics 365 Project Operations zur Verfügung stehen.

Wenn Projektmanager Projekte planen und ausführen, können sie Fremdarbeiter beschäftigen und Produkte und Dienstleistungen von Anbietern kaufen. Während der Ausführung eines Projekts entstehen Kosten für Dienstleistungen, Materialien und Ausgabenkategorien, die im Rahmen von Fremdarbeit mit Lieferanten beschafft werden. Kreditoren stellen diese Kosten Projekten in Rechnung, indem sie Kreditorenrechnungen erstellen.

Die folgende Tabelle enthält Informationen zu den Feldern in den Kopfzeilen von Kreditorenrechnungspositionen in Project Operations.

| Feld | Beschreibung des Dataflows | Funktionsauswirkung |
| --- | --- | --- |
| Name des Dataflows | Der Name der Kreditorenrechnung. | In allen Dropdown-Listen für Kreditorenrechnungen wird der Name der Kreditorenrechnung in der ersten Spalte aufgeführt, um Ihnen die Identifizierung der Kreditorenrechnung zu erleichtern. Wenn eine Kreditorenrechnung aus einer Fremdarbeit erstellt wird, wird standardmäßig das **Name**-Feld der Kreditorenrechnung auf einen Wert gesetzt, der sich aus dem Namen der Fremdarbeit und dem aktuellen Datum zusammensetzt. |
| Beschreibung des Dataflows | Eine kurze Beschreibung der Dienste und Produkte, die in der Kreditorenrechnung in Rechnung gestellt werden. | Nein |
| Hersteller | Der Name des Unternehmens, das die Produkte und Dienstleistungen in Rechnung stellt. Dieses Unternehmen sollte ein Firmendatensatz mit dem Beziehungstyp **Kreditor** oder **Lieferant** sein. | <p>Basierend auf dem ausgewählten Lieferanten werden automatisch Vorschlagswerte in die folgenden Felder eingegeben:</p><ul><li>Währungen</li><li>Preislisten</li><li>Zahlungsbedingungen</li><li>Zahlungsadresse</li></ul> |
| Fremdarbeit | Ein Verweis auf die Fremdarbeit für die Kreditorenrechnung. | <p>Basierend auf die ausgewählten Fremdarbeit werden automatisch Vorschlagswerte in die folgenden Felder eingegeben:</p><ul><li>Währungen</li><li>Preislisten</li><li>Zahlungsbedingungen</li><li>Zahlungsadresse</li></ul><p>Die auf der Kreditorenrechnungskopfzeile ausgewählte Fremdarbeit wird standardmäßig in den Kreditorenrechnungspositionen eingegeben und kann dort nicht geändert werden.</p> |
| Rechnungsdatum | Das Datum für die tatsächlichen Kosten, die erstellt werden, wenn die Kreditorenrechnung bestätigt wird. | Das Rechnungsdatum wird zudem verwendet, um die richtige Einkaufspreisliste entweder aus den Preislisten, die dem zugehörigen Lieferanten beigefügt sind, oder aus den Projektparametern auszuwählen. |
| Statusgrund | Der Status der Kreditorenrechnung | <p>Der Status bestimmt, wo sich die Kreditorenrechnung im Geschäftsprozess befindet und ob er bearbeitet werden kann. Dies sind einige der verfügbaren Werte:</p><ul><li>**Entwurf**: Die Kreditorenrechnung kann bearbeitet werden.</li><li>**Bestätigt** – Die Kreditorenrechnung wurde geprüft und bestätigt. Kreditorenrechnungen mit diesem Status können nicht bearbeitet oder gelöscht werden.</li><li>**In Bearbeitung** – Die Kreditorenrechnung wird überprüft. Kreditorenrechnungen mit diesem Status können bearbeitet aber nicht gelöscht werden.</li><li>**Storniert** – Die Kreditorenrechnung wurde storniert. Kreditorenrechnungen mit diesem Status können nicht bearbeitet oder gelöscht werden.</li></ul> |
| Währungen | Die Währung, in der der Kreditor die Produkte und Dienstleistungen auf der Kreditorenrechnung fakturiert. | Auf einer Kreditorenrechnung, die auf eine Fremdarbeit verweist, wird die Währung der Fremdarbeit standardmäßig als Währung der Kreditorenrechnung eingegeben. Bei einer Kreditorenrechnung, die keine Fremdarbeit referenziert, wird der Standardwert aus dem Kreditorenkontodatensatz eingegeben und kann geändert werden. Nachdem eine Kreditorenrechnung gespeichert wurde, kann die Währung nicht mehr bearbeitet werden. |
| Vertragsschlusseinheit | Die Abteilung des Unternehmens, die für den Erhalt der Dienstleistungen und/oder Produkte vom Kreditor verantwortlich ist. | Nein |
| Zahlungsbedingungen | Die Zahlungsbedingungen für Kreditorenrechnungen, die ausgestellt werden. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Zahlungsbedingungen aus einer Fremdarbeit werden in alle Kreditorenrechnungen kopiert, die sich auf die Fremdarbeit beziehen. Zahlungsbedingungen können aktualisiert werden, wenn die Kreditorenrechnung den Status **Entwurf** hat. |
| Zahlungsadresse | Die Adresse des Verkäufers, an den die Zahlungen gesendet werden müssen. Der Standardwert wird automatisch aus dem Kreditorenkonto eingegeben. | Die Zahlungsadresse aus einer Fremdarbeit wird als Zahlungsadresse in alle Kreditorenrechnungen übernommen, die für diese Fremdarbeit erstellt werden. Die Zahlungsadresse kann aktualisiert werden, wenn die Kreditorenrechnung den Status **Entwurf** hat. |
| Zwischensumme | Wenn die Kreditorenrechnung keine Zeilen hat, geben Sie die Rechnungszwischensumme vor Steuern ein. Wenn die Kreditorenrechnung Zeilen enthält, ist dieses Feld schreibgeschützt. In diesem Fall ist der angezeigte Betrag der Zwischensummenbetrag aus allen Zeilen der Kreditorenrechnung. | Nein |
| Steuern gesamt | Wenn die Kreditorenrechnung keine Zeilen hat, geben Sie die Summe der Steuern der Fremdarbeit ein. Wenn die Kreditorenrechnung Zeilen enthält, ist dieses Feld schreibgeschützt. In diesem Fall ist der angezeigte Betrag die Summe des Steuerbetrags aus allen Zeilen der Kreditorenrechnung. | Nein |
| Gesamtbetrag | Dieses berechnete Feld zeigt den Gesamtbetrag der Kreditorenrechnung nach Berücksichtigung der Steuern an. | Nein |

> [!NOTE]
> Die folgenden Felder auf einer Kreditorenrechnung können nicht geändert werden, nachdem die Kreditorenrechnung gespeichert wurde: **Kreditor**, **Fremdarbeit**, **Währung**, **Vertragseinheit** und **Zahlungsbedingungen**. Wenn Änderungen an diesen Feldern auf einer Kreditorenrechnung erforderlich sind, müssen Sie die Kreditorenrechnung löschen und eine neue Kreditorenrechnung erstellen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
