---
title: Mehrere Kunden in einem Projektangebot verwalten
description: Dieses Thema enthält Informationen zur Bearbeitung von Angeboten, an denen mehrere Kunden beteiligt sind, die das Projekt finanzieren.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 62bd8e3539102229c79126397cf60287747b187d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011415"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Mehrere Kunden in einem Projektangebot verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektangebote unterstützen das Szenario, in dem mehrere Kunden an dem Angebot beteiligt sind, die das Geschäft finanzieren. Die Registerkarte **Zusammenfassung** des Angebots enthält das **Potenzieller Kunde**-Feld, das den Hauptkunden des Geschäfts identifiziert. Andere Kunden für das Geschäft können auf der **Kunden**-Registerkarte des Projektangebots eingerichtet werden.

Alle Angebotskunden auf der **Kunden**-Registerkarte des Projektangebots werden auf beliebigen **neuen** projektbasierten Angebotspositionen, die für das Angebot erstellt wurden, standardmäßig als Angebotspositionskunden angegeben. Vorhandene projektbasierte Angebotspositionen erben keine neuen Angebotskundendatensätze, die nach ihnen erstellt wurden.

Angebotskunden und Angebotspositionskunden können jederzeit hinzugefügt, aktualisiert oder gelöscht werden, bevor das Angebot gewonnen wird. Ein gültiger Kunde auf dem Angebot muss als Kunde im zuständigen Unternehmen oder der juristischen Person auf der **Kunden**-Seite eingerichtet sein. Juristische Personen sind im Modul **Projektmanagement und -buchhaltung** von Dynamics 365 Project Operations festgelegt und als Unternehmen in den Modulen **Projektvertrieb und Lieferung** von Project Operations verfügbar.

## <a name="concept-of-a-primary-customer"></a>Konzept eines Hauptkunden

Der Kunde, der auf der **Zusammenfassung**-Registerkarte des Projektangebots, als der potenzielle Kunde aufgeführt wird, ist der Hauptkunde des Angebots. Wenn Sie versuchen, den Hauptkunden aus der Kundenliste im Angebot zu löschen, wird die Fehlermeldung angezeigt, dass ein Hauptkundendatensatz in einem Angebot nicht gelöscht werden kann.

Der Hauptkunde sollte nicht aus der Kundenliste im Angebot aktualisiert werden. Sie können den Hauptkunden jedoch beeinflussen, indem Sie den potenziellen Kunden auf der **Zusammenfassung**-Registerkarte des Angebots ändern. Wenn dieses Feld auf der **Angebotszusammenfassung** aktualisiert wird, wird der neu ausgewählte potenzielle Kunde als neuer Angebotskunde mit dem festgelegten **Primär**-Flag hinzugefügt. Der alte potenzielle Kunde bleibt weiterhin Kunde im Angebot.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Erstellen, Aktualisieren oder Löschen eines Angebotskundendatensatzes

Ein Angebotskunde kann in der **Angebotskunden**-Registerkarte auf der **Angebot**-Seite erstellt, aktualisiert oder gelöscht werden. Die in der folgenden Tabelle aufgeführten Felder befinden sich im Angebotskundendatensatz eines Projektangebots.

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Konto | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Führt alle aktiven Konten auf. Dieses Feld wird gesperrt, nachdem der Datensatz erstellt wurde. Wenn Sie ihn aktualisieren möchten, löschen Sie den Datensatz und erstellen Sie ihn neu. Wenn Sie Ist-Daten aufgezeichnet haben oder wenn der Angebotskundendatensatz ein Hauptkunde ist, können Sie den Datensatz löschen. | Angebotspositionskunden werden als Angebotspositionskunden kopiert, wenn eine Angebotsposition erstellt wird. Angebotskunden werden auch zu den Kunden der Projektvertrags kopiert, wenn ein Angebot gewonnen wird. |
| Prozentsatz der Abrechnungsteilung | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Stellen Sie den Prozentsatz jeder nicht in Rechnung gestellten Verkaufstransaktion dar, die diesem Angebotskunden zugeordnet wird. | Wird zu erstellten neuen Angebotspositionen und zu Projektvertragskunden kopiert. |
| Kontaktname für Rechnungsadresse | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Dies ist ein Textfeld und sollte verwendet werden, um die Rechnungskontaktperson für diesen Kunden zu identifizieren. Diese werden standardmäßig aus dem zugehörigen Kontodatensatz übernommen | Wird zu Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird, und anschließend in das Feld „Vertragsname für Rechnungsadresse“ auf der Rechnung kopiert, die für diesen Kunden erstellt wurde. |
| Name für Rechnungsadresse | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Dieses Textfeld sollte verwendet werden, um die Rechnungskontaktperson für diesen Kunden zu identifizieren. | Wird zum Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird, und anschließend in das Feld **Vertragsname für Rechnungsadresse** auf der Rechnung kopiert, die für diesen Kunden erstellt wurde. |
| Zahlungsbedingungen | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Dies ist ein Optionssatz mit Werten, die standardmäßig aus dem zugehörigen Kontodatensatz stammen. | Wird zum Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird, und anschließend in das Feld **Vertragsname für Rechnungsadresse** auf der Rechnung kopiert, die für diesen Kunden erstellt wurde. |
| Wird gerundet | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Gibt an, ob dieser Kunde ein Standardrundungskunde für dieses Geschäft ist. | Wird an die Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird. |
| Zuständiges Unternehmen | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Die juristische Person, mit der dieser Kunde innerhalb der **Projektmanagement und -buchhaltung**-Modul eingerichtet ist. Dieses Feld ist schreibgeschützt und auf das zuständige Unternehmen des Angebots selbst festgelegt. Die Liste der Kunden, die in das **Konto**-Feld aufgenommen werden sollen, ist bereits auf die Liste des zuständigen Unternehmens im **Projektmanagement und -buchhaltung**-Modul von Project Operations gefiltert. | Das zuständige Unternehmen entspricht dem Konzept der juristischen Person im **Projektmanagement und -buchhaltung**-Modul von Project Operations. Alle Kosten und Einnahmen aus diesem Projekt werden im Hauptbuch des zuständigen Unternehmens ausgewiesen. |
| Nicht zu überschreitender Grenzwert | Bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte und die Formulare **Haupt** und **Schnellerfassung** für einen Angebotspositionskunden. | Gibt an, ob es ein ausgehandeltes Limit oder eine Obergrenze für den Gesamtbetrag gibt, der diesem Kunden für dieses Engagement in Rechnung gestellt wird. | Wird an die Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird. |

## <a name="editing-billing-split-percentages"></a>Bearbeiten von Aufteilungsprozentsätzen

Sie können die Prozentsätze für die Aufteilung der Abrechnung mithilfe der Inline-Rasterbearbeitung bearbeiten. Wenn die Prozentsätze für die Aufteilung der Abrechnung nicht 100 % betragen, tritt ein Fehler auf. Aktualisieren Sie die Seite, nachdem Sie die Prozentsätze für die Aufteilung der Abrechnung aktualisiert haben, um den Fehler zu beheben.

Sie können auch **Gleichmäßig verteilen** im Angebotskunden-Unterraster auswählen. Diese Aktion weist allen Angebotskunden Abrechnungssplits zu. Wenn es einen Rundungsfaktor gibt, wird dieser dem Rundungskunden hinzugefügt. Einer der Angebotskunden wird immer als Rundungskunde gekennzeichnet. Dies bedeutet, dass der Angebotskundendatensatz das **Rundung**-Flag auf **Ja** festgelegt hat. In der Regel ist dies der Hauptkunde des Angebots, dies kann jedoch geändert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]