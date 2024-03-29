---
title: Kopfzeilendetails für projektbasierte Verträge
description: Dieser Artikel informiert Sie über die Felder und Informationen zu projektbasierten Verträgen in Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5839a812dbb3a61fcf271ae6e80e22bfe61f7e14
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824390"
---
# <a name="header-details-for-project-based-contracts"></a>Kopfzeilendetails für projektbasierte Verträge

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel enthält Informationen über Felder, die für den gesamten Projektvertrag gelten, einschließlich Einstellungen, die sich auf alle Vertragszeilen auswirken. Informationen zum Vertrag, die in allen Zeilenpositionen zusammengefasst sind, um die KPIs des Projektvertrags zu bestimmen, sind ebenfalls enthalten.

In der folgenden Tabelle sind die Felder eines Projektvertrags aufgeführt, die nur in Dynamics 365 Project Operations vorhanden sind oder einige wichtige Änderungen im Verhalten hinsichtlich Vertriebsaufträgen in Dynamics 365 Sales aufweisen.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Art | Registerkarte **Zusammenfassung** (ausgeblendet) | Dies ist ein Optionssatzfeld mit den folgenden Optionen:</br>- **Arbeitsbasiert** (nur bei Installation von Project Operations verfügbar)</br>- **Positionsbasiert** (nur verfügbar, wenn Project Operations und Sales installiert sind)</br>- **Servicewartungsbasiert** (verfügbar, wenn Dynamics 365 Field Service installiert ist) | In Project Operations lautet der Wert dieses Felds standardmäßig **Arbeitsbezogen** und klassifiziert den Vertrag als projektbasierten Vertrag. Ein Vertrag sollte projektbasiert sein, um alle projektspezifischen Erweiterungen und Funktionen zu aktivieren. |
| Zuständiges Unternehmen | Registerkarte **Zusammenfassung** | Die juristische Person, die die Kosten und Einnahmen aus dem Projekt, die mit diesem Projektvertrag verbunden sind, berücksichtigt. Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. | Das zuständige Unternehmen entspricht dem Konzept der juristischen Person im Modul **Projektmanagement und -buchhaltung** von Project Operations. Alle Kosten und Umsätze aus diesem Projekt werden in der Finanzbuchhaltung des zuständigen Unternehmens ausgewiesen. |
| Kunde | Registerkarte **Zusammenfassung** | Ein Verweis auf das Unternehmen des Kunden oder den Firmendatensatz Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. | Die Währung im Projektvertrag basiert auf der Währung des Kunden. Die Währung kann geändert werden, bevor der Vertrag gespeichert wird. |
| Konto-Manager | Registerkarte **Zusammenfassung** | Der Name des Account Managers für dieses Geschäft. Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. | Der Account Manager ist verantwortlich für die Verwaltung der Beziehung zum Kunden bis zum Abschluss dieses Projekts. Basierend auf dem buchbaren Ressourceneintrag, der an den Account Manager gebunden ist, ist die Vertragseinheit im Projektvertrag voreingestellt. |
| Vertragseinheit | Registerkarte **Zusammenfassung** | Die Organisationseinheit, die für die Bereitstellung der mit diesem Vertrag verbundenen Projekte verantwortlich ist. Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. | Die Vertragseinheit ist die Abteilung des Unternehmens, die die Projekte ausführt. Jede Vertragseinheit hat eine Währung, und diese Währung wird verwendet, um geschätzte und tatsächliche Kosten zu melden, die während des Projekts anfallen. |
| Produktpreisliste | Registerkarte **Zusammenfassung** | Dies ist die Preisliste, die verwendet wird, um die Preise in den produktbasierten Vertragszeilen als Standard festzulegen. Die Liste der Dropdownoptionen für dieses Feld enthält eine Liste der Preislisten, bei denen die Preislistenwährung mit der Währung im Vertrag übereinstimmt. Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. Im Projektvertrag wird dieses Feld standardmäßig aus dem Firmendatensatz übernommen, kann jedoch geändert werden. | Für dieses Feld gibt es keine nachgelagerte Relevanz. |
| Währung | Registerkarte **Zusammenfassung** | Die Währung, in der der Wert dieses Geschäfts angegeben wird, und die Währung für die Rechnungsstellung an den Kunden. Bei einem aus einem Angebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld in dem Angebotsdatensatz kopiert. Im Projektvertrag wird dieses Feld standardmäßig aus dem Firmendatensatz übernommen, kann jedoch geändert werden. | Nachdem ein Vertrag gespeichert wurde, kann dieses Feld nicht mehr bearbeitet werden. Dieses Feld wird verwendet, um die Produkt- und Projektpreislisten im Vertrag standardmäßig anzugeben. Die Währung im Vertrag wird verwendet, um die Währung in der Preisliste abzustimmen. |
| Nicht zu überschreitender Grenzwert | Registerkarte **Zusammenfassung** | Dieses Feld zeigt die ausgehandelte Obergrenze für den Endwert an, dem der Kunde für dieses Geschäft zustimmt. | Die Obergrenze wird während der Ausführung bewertet und gilt für alle mit diesem Geschäft verbundenen Positionen und Projekte. |
| Gewünschtes Lieferdatum | Registerkarte **Zusammenfassung** | Bei einem aus einem Projektangebot erstellten Vertrag wird dieses Feld aus dem entsprechenden Feld im Projektangebot kopiert. | Dieses Datum wird als Enddatum für die Erstellung von Rechnungszeitplänen verwendet. |

Die folgenden KPIs sind auf der Registerkarte **Vertragsleistung** eines Projektvertrags verfügbar.

| Feld | Position | Beschreibung des Dataflows |
| --- | --- | --- |
| Vertragswert | Gesamtvertrag | Der Gesamtwert des Projektvertrags |
| Fakturierter Betrag | Gesamtvertrag | Die Summe der Beträge auf allen Rechnungen für diesen Vertrag. |
| Angefallene Kosten | Gesamtvertrag | Die Summe aller tatsächlichen Kosten, die in allen Projekten protokolliert wurden, die dem Vertrag zugeordnet sind. |
| Bruttogewinn | Gesamtvertrag | Rechnungsbetrag – Bis zum Datum angefallene Kosten/Rechnungsbetrag |
| Erwartete Marge | Gesamtvertrag | (Auftragswert – Vorkalkulierte Kosten) / Auftragswert/Vorkalkulierte Kosten = Die Summe aller vorkalkulierten Kosten in allen Projekten, die dem Vertrag zugeordnet sind.|
| Vertragswert | Projektbasierte Positionen | Der Wert der Vertragszeile |
| Fakturierter Betrag | Projektbasierte Positionen | Für Festpreisvertragszeile: Die Summe der Beträge aller in Rechnung gestellten Istwerte für Umsatzmeilensteine für diese Vertragszeile auf verschiedenen für diesen Vertrag erstellten Rechnungen. Für die Vertragszeile „Zeit und Material“: Die Summe der Beträge aller in Rechnung gestellten Umsatz-Istwerte für diese Vertragszeile auf verschiedenen für diesen Vertrag erstellten Rechnungen. |
| Angefallene Kosten | Projektbasierte Positionen | Die Summe aller tatsächlichen Kosten, die in allen Projekten protokolliert wurden, die der Vertragszeile zugeordnet sind. |
| Bruttogewinn | Projektbasierte Positionen | (Rechnungsbetrag – Bis zum Datum angefallene Kosten)/Rechnungsbetrag |
| Erwartete Marge | Projektbasierte Positionen | (Vertragszeilenbetrag in Basiswährung – Vorkalkulierte Kosten für die Vertragszeile in Basiswährung) / Vertragszeilenbetrag in Basiswährung |
| Angefallene Kosten | Detail einer projektbasierten Zeile | Zeit: Die Summe des Betrags der tatsächlichen Werte für Zeitkosten, die für diese Rolle im Projekt protokolliert wurden, die der Vertragszeile zugeordnet ist. Ausgabe: Die Summe des Betrags aller tatsächlichen Ausgabenkosten, die für diese Kategorie im Projekt protokolliert wurden, die der Vertragszeile zugeordnet ist. |
| Protokollierte Menge | Detail einer projektbasierten Zeile | Zeit: Die gesamte Zeitmenge der tatsächlichen Werte für Zeitkosten entspricht einer Rolle im Projekt, die dieser Vertragszeile zugeordnet ist. Ausgaben: Alle Mengen für diese Ausgabenkategorie in den tatsächlichen Ausgabenkosten im Projekt sind dieser Vertragszeile zugeordnet. |
| Fakturierter Betrag | Detail einer projektbasierten Zeile | Bei einer Festpreis-Vertragszeile bleibt dieses Feld auf Detailebene leer und wird nur auf Vertragszeilenebene angezeigt. Bei einer Vertragszeile für Zeit und Material werden Berechnungen auf Detailebene abgeschlossen. Die Details zeigen die Summe des Betrags auf allen in Rechnung gestellten Umsatzzeilen für diese Vertragszeile, die fakturiert werden können. |
| Fakturierte Menge | Detail einer projektbasierten Zeile | Bei einer Festpreis-Vertragszeile bleibt dieses Feld auf Detailebene leer und wird nur auf Vertragszeilenebene angezeigt. Bei einer Vertragszeile für Zeit und Material werden Berechnungen auf Detailebene für Zeit und Ausgaben abgeschlossen. Zeit: Die Summe der Stunden auf allen in Rechnung gestellten Umsatzzeilen für diese Rolle für diese Vertragszeile, die fakturierbar sind. Ausgaben: Alle Mengen für diese Ausgabenkategorie in den tatsächlichen Ausgabenkosten im Projekt sind dieser Vertragszeile zugeordnet. |
| Vertragswert | Produktbasierte Positionen | Der Vertragszeilenwert dieser produktbasierten Vertragszeile. |
| Fakturierter Betrag | Produktbasierte Positionen | Die Summe der Beträge in allen Rechnungspositionen mit dieser produktbasierten Vertragszeile auf verschiedenen Rechnungen, die für diesen Vertrag erstellt wurden. |
| Angefallene Kosten | Produktbasierte Positionen | Die Summe aller tatsächlichen Kosten, die für die produktbasierte Vertragszeile protokolliert wurden. |
| Bruttogewinn | Projektbasierte Positionen | Rechnungsbetrag – Bis zum Datum angefallene Kosten/Rechnungsbetrag |
| Erwartete Marge | Produktbasierte Positionen | (Vertragszeilenwert – Vorkalkulierte Kosten für die Vertragszeile)/Vertragszeilenwert |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
