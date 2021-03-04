---
title: Mehrere Kunden in Projektverträgen verwalten – Lite
description: Dieses Thema enthält Informationen zum Verwalten von mehreren Kunden für Projektverträge.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b248dabdbd5239b140da7c99d3f38609facfe75e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181316"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Mehrere Kunden in Projektverträgen verwalten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektverträge in Dynamics 365 Project Operations unterstützen das Szenario, in dem eine vertragliche Vereinbarung mehrere Kunden umfasst, die einen Deal finanzieren. Die **Zusammenfassung**-Registerkarte auf der **Projektvertrag**-Seite enthält das **Kunde**-Feld. Dieses Feld identifiziert den Hauptkunden des Geschäfts. Andere Kunden für das Geschäft können auf der **Kunden**-Registerkarte der **Projektvertrag**-Seite eingerichtet werden.

Alle Vertragskunden, die im Projektvertrag aufgeführt sind, werden standardmäßig als Vertragszeilenkunden in allen neuen projektbasierten Vertragszeilen aufgeführt, die für den Projektvertrag erstellt wurden. Bestehende projektbasierte Vertragszeilen erben keine neuen Vertragskunden, wenn neue Datensätze erstellt werden.

Produktbasierte Vertragszeilen werden automatisch dem Hauptkunden zugeordnet.

Vertragskunden und Vertragskunden können jederzeit hinzugefügt, aktualisiert oder gelöscht werden, bevor der Vertrag gewonnen wird.

## <a name="primary-customer"></a>Primärer Kunde

Der Kunde auf der **Zusammenfassung**-Registerkarte des Projektvertrags, da der potenzielle Kunde der Hauptkunde des Vertrags ist. Wenn Sie versuchen, den Hauptkunden aus der Kundenliste des Vertrags zu löschen, wird eine Fehlermeldung angezeigt, dass ein Hauptkundendatensatz eines Vertrags nicht gelöscht werden kann.

Der Hauptkunde kann nicht aus der Liste der Vertragskunden aktualisiert werden. Ändern Sie stattdessen den potenziellen Kunden auf der **Zusammenfassung**-Registerkarte des Vertrags. Wenn dieses Feld auf der **Vertragszusammenfassung**-Seite aktualisiert wird, wird der neue Kunde als neuer Vertragskunde mit dem gesetzten **Primär**-Flag hinzugefügt. Der vorherige Hauptkunde bleibt weiterhin ein Kunde im Vertrag.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Erstellen, aktualisieren oder löschen Sie einen Vertragskundendatensatz

Ein Vertragskunde kann über die **Kunden**-Registerkarte auf der **Projektvertrag**-Seite erstellt, aktualisiert oder gelöscht werden. Die Felder in der folgenden Tabelle befinden sich im Vertragskundendatensatz eines Projektvertrags und sollten bei der Arbeit mit dem Vertrag berücksichtigt werden.

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Firma** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Führt alle aktiven Konten auf. Dieses Feld wird gesperrt, nachdem der Datensatz erstellt wurde. Um das Konto zu aktualisieren, löschen Sie den Datensatz und erstellen Sie ihn neu. Wenn Sie Istdaten aufgezeichnet haben oder wenn der Vertragskundendatensatz ein Hauptkunde ist, können Sie den Datensatz nicht löschen. | Vertragskunden werden beim Erstellen einer Vertragszeile als Vertragszeilenkunden kopiert. |
| **Abrechnungsteilungsprozentsatz** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Stellt den Prozentsatz jeder nicht in Rechnung gestellten Verkaufstransaktion dar, der diesem Vertragskunden zugeordnet wird. | Übertragen auf neue Vertragszeilen und auf Projektvertragszeilenkunden in neuen Projektvertragszeilen. |
| **Kontaktname für Rechnungsadresse** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Dieses Textfeld sollte verwendet werden, um die Rechnungskontaktperson für diesen Kunden zu identifizieren. Dieses Feld wird standardmäßig aus dem zugehörigen Kontodatensatz verwendet. | Dies wird in das Feld **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| **Name für Rechnungsadresse** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Dieses Textfeld sollte verwendet werden, um die Rechnungskontaktperson für diesen Kunden zu identifizieren. Dieses Feld wird standardmäßig aus dem zugehörigen Kontodatensatz verwendet. | Dies wird in das Feld **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| **Zahlungsbedingungen** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Die Werte werden standardmäßig aus dem zugehörigen Kontodatensatz verwendet. | Dies wird in das Feld **Rech. an Vertragsnamen** auf der Rechnung kopiert, die für diesen Kunden generiert wird. |
| **Wird gerundet** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Gibt an, ob dieser Kunde ein Standardrundungskunde für dieses Geschäft ist. Es kann nur einen Rundungskunden in einem Projektvertrag geben. | Wenn Kosten und nicht abgerechnete Umsatzaufteilungen nach Menge zu einer Rundungsdifferenz führen, wird diese Differenz auf die tatsächliche Differenz angewendet, die diesem Kunden zugeordnet ist. |
| **Nicht zu überschreitender Grenzwert** | Das Raster kann auf der **Vertragskunden**-Registerkarte und den Formularen **Hauptbereich** und **Schnellerfassung** für einen Vertragskunden bearbeitet werden. | Gibt an, ob es ein ausgehandeltes Limit oder eine Obergrenze für den Gesamtbetrag gibt, der dem Kunden für dieses Engagement in Rechnung gestellt wird. | Der **Nicht zu überschreitende Grenzwert**, der auf Vertragskundenebene eingerichtet wurde, erhält eine Bewertung für **Nicht in Rechnung gestellte vertriebliche Ist-Werte**, die auf diesen Vertragskunden verweisen. |

## <a name="edit-billing-split-percentages"></a>Aufteilungsprozentsätze bearbeiten

Fakturierungs-Aufteilungsprozentsätze können mithilfe der Inline-Rasterbearbeitungserfahrung bearbeitet werden. Wenn die Prozentsätze für die Aufteilung der Abrechnung nicht 100 Prozent betragen, wird eine Fehlermeldung angezeigt. Aktualisieren Sie die Seite, nachdem Sie die Prozentsätze für die Aufteilung der Abrechnung bearbeitet haben, um den Fehler zu beheben.

Sie können auch **Gleichmäßig verteilen** auf dem **Vertragskunden**-Unterraster auswählen, um Zuordnungen von Abrechnungssplits auf alle Vertragskunden gleichmäßig zu verteilen. Wenn es einen Rundungsfaktor gibt, wird dieser dem Rundungskunden hinzugefügt. Einer der Vertragskunden ist immer als **Rundungs**-Kunde gekennzeichnet, was bedeutet, dass für den Vertragskundendatensatz das Rundungsflag **Ja** gesetzt ist. In der Regel ist dies der Hauptkunde des Vertrags, er kann jedoch auch geändert werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]