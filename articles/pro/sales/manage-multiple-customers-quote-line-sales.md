---
title: Mehrere Kunden in projektbasierten Angebotspositionen verwalten – Lite
description: Dieses Thema beschreibt, wie mehrere Kunden in projektbasierten Angebotspositionen verwaltet werden.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2e45e0a83f904a65a29c1e39b59adac47a77c58
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994990"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Mehrere Kunden in projektbasierten Angebotspositionen verwalten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektbasierte Angebotspositionen unterstützen Szenarien, in denen jede Angebotsposition eine Liste von Kunden enthält, die dafür bezahlen. Diese Liste der Kunden in der projektbasierten Angebotsposition kann mit der Liste der Kunden in der Angebotsposition identisch sein. Sie können die Kundenliste auch anders ändern. Wenn ein Projektangebot gewonnen wurde, wird die Kundenliste in der projektbasierten Angebotsposition in die entsprechende projektbasierte Vertragszeile kopiert, um den endgültigen Projektkontakt zu erstellen. Kunden im projektbasierten Angebot werden in den Projektvertrag kopiert.

Wenn Sie den letztendlichen Projektvertrag in Rechnung stellen, hat die Kundenliste in der projektbasierten Vertragszeile Vorrang vor der Liste im Projektvertrag. Die Kundenliste im Projektvertrag wird nur verwendet, um neue Projektvertragszeileen als Standard festzulegen.

Alle Angebotskunden auf der **Kunden**-Registerkarte des Projektangebots werden auf beliebigen neuen projektbasierten Angebotspositionen, die für das Projektangebot erstellt wurden, standardmäßig als Angebotspositionskunden angegeben. Vorhandene projektbasierte Angebotspositionen erben keine neuen Angebotskundendatensätze, die nach ihnen erstellt wurden.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Erstellen, Aktualisieren oder Löschen eines Angebotspositionskundendatensatzes

Sie können einen Angebotspositionskunden auf der **Angebotspositionskunden**-Registerkarte auf der **Projektbasierte Angebotsposition**-Seite erstellen, aktualisieren oder löschen. Wenn Sie der projektbasierten Angebotsposition einen neuen Kunden hinzufügen, wird der Kunde auch als Angebotskunde zum Gesamtangebot hinzugefügt, wobei der Standardprozentsatz für die Aufteilung der Abrechnung auf das Gesamtangebot 0 % beträgt. Der Prozentsatz der Abrechnungsaufteilung auf das Gesamtangebot wird in neue Angebotspositionen und in den eventuellen Projektvertrag kopiert. Wenn Sie jedoch aus dem Vertrag abrechnen, wird der Abrechnungssplit-Prozentsatz auf Angebotspositionsebene verwendet, nicht der Abrechnungssplit-Prozentsatz auf Gesamtvertragsebene. 

Die folgenden Tabelle zeigt die Felder im Angebotspositionskundendatensatz einer projektbasierten Angebotsposition.

| Feld | Position | Beschreibung und Anleitung | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| **Firma** | Ein bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte, das Hauptformular und die Schnellerstellungsformulare für einen Angebotspositionnkunden. | Führt alle aktiven Konten auf. Dieses Feld wird gesperrt, nachdem der Datensatz erstellt wurde. Wenn Sie das Feld aktualisieren müssen, löschen Sie den Datensatz und erstellen Sie ihn neu. Wenn Sie Aktualisierungen aufgezeichnet haben, können Sie die Aufzeichnung nicht löschen. | Wenn Sie ein Konto aus der Hauptliste der hinzuzufügenden Konten auswählen, wird der Angebotspositionskunde beim Speichern auch als Angebotskunde hinzugefügt. Wenn ein Angebot gewonnen wird, werden Angebotspositionskunden zu den Kunden der Projektvertragszeile kopiert. |
| **Prozentsatz der Abrechnungsteilung** | Ein bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte, das Hauptformular und die Schnellerstellungsformulare für einen Angebotspositionnkunden. | Stellt den Prozentsatz jeder nicht in Rechnung gestellten Verkaufstransaktion dar, die diesem Angebotspositionskunden zugeordnet wird. | Zu Projektvertragszeilenkunden kopiert. |
| **Nicht zu überschreitender Grenzwert** | Ein bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte, das Hauptformular und die Schnellerstellungsformulare für einen Angebotspositionnkunden. | Gibt an, ob es ein ausgehandeltes Limit oder eine Obergrenze für den Gesamtbetrag gibt, der diesem Kunden für diese angebotene Position in Rechnung gestellt wird. | Wird an die Projektvertragszeilenkunden kopiert, wenn ein Angebot gewonnen wird. |
| **Wird gerundet** | Ein bearbeitbares Raster auf der **Angebotspositionnkunden**-Registerkarte, das Hauptformular und die Schnellerstellungsformulare für einen Angebotspositionnkunden. | Gibt an, ob dieser Kunde ein Standardrundungskunde für diese projektbasierte Angebotsposition ist. | Wird an die Projektvertragskunden kopiert, wenn ein Angebot gewonnen wird. |

## <a name="edit-billing-split-percentages"></a>Aufteilungsprozentsätze bearbeiten

Sie können Abrechnungsaufteilungsprozentsätze inline bearbeiten. Wenn die Prozentsätze für die Aufteilung der Abrechnung nicht 100 % betragen, tritt ein Fehler auf. Aktualisieren Sie die Angebotspositionnseite, nachdem Sie die Prozentsätze für die Aufteilung der Abrechnung bearbeitet haben, um den Fehler zu beheben.

Verwenden Sie die Aktion „Gleichmäßig verteilen“ im Unterraster „Angebotspositionskunde“, um allen Angebotspositionskunden Abrechnungsaufteilungen zuzuweisen. Wenn es einen Rundungsfaktor gibt, wird dieser dem Rundungskunden hinzugefügt. Einer der Kunden der Angebotsposition wird immer als Rundungskunde gekennzeichnet. Dies bedeutet, dass für den Kundendatensatz der Angebotsposition das Rundungsflag auf **Ja** festgelegt ist. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]