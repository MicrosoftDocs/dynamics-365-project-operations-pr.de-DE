---
title: Mehrere Kunden in projektbasierten Vertragszeilen verwalten
description: Dieser Artikel enthält Informationen über die Arbeit mit Vertragszeilen und Verträgen, die mehrere Kunden enthalten.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e0652d4b9cdb0489d4f191ef0f3b251e39262f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914861"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Mehrere Kunden in projektbasierten Vertragszeilen verwalten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Projektbasierte Vertragszeilen können eine Liste der Kunden enthalten, die für die Zahlung verantwortlich sind. Diese Liste der Kunden in der projektbasierten Vertragszeilen kann mit der Liste der Kunden in der Vertragszeile identisch sein, dies ist jedoch nicht erforderlich. Wenn ein Projektangebot gewonnen und ein Projektvertrag erstellt wird, wird die Kundenliste in der Angebotszeile in die entsprechende Vertragszeile kopiert. Kunden auf dem Angebot werden in den Vertrag kopiert.

Wenn der Projektvertrag in Rechnung gestellt wird, hat die Kundenliste in der projektbasierten Vertragszeile Vorrang vor der Kundenliste im Vertrag. Die Kundenliste im Projektvertrag wird nur verwendet, um neue Vertragszeilen als Standard festzulegen.

Alle Vertragskunden, die auf der **Kunden**-Registerkarte im Projektvertrag aufgeführt sind, werden standardmäßig als Vertragszeilenkunden in allen neuen Vertragszeilen aufgeführt, die für den Projektvertrag erstellt wurden. Bestehende Vertragszeilen erben nicht die nach ihnen erstellten neuen Vertragskundenaufzeichnungen.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Erstellen, aktualisieren oder löschen Sie einen Vertragszeilen-Kundendatensatz

Sie können einen Vertragszeilenkunden auf der Registerkarte **Vertragszeilenkunden** auf der Seite **Projektbasierte Vertragszeile** erstellen, aktualisieren oder löschen. Wenn ein neuer Kunde zur projektbasierten Vertragszeile hinzugefügt wird, wird er auch als Vertragskunde mit einem Standardabrechnungssplit von null Prozent zum Gesamtvertrag hinzugefügt. Der Prozentsatz der Abrechnungsaufteilung auf den Gesamtvertrag wird in neue Vertragszeilen und in den eventuellen Projektvertrag kopiert. Bei der Rechnungsstellung aus dem Vertrag wird jedoch der Prozentsatz der Abrechnungsaufteilung auf Vertragszeilenebene verwendet und nicht der Prozentsatz der Abrechnungsaufteilung auf Gesamtvertragsebene. 

Unten sind die Felder im Vertragszeilen-Kundendatensatz einer projektbasierten Vertragszeile, die Sie bei der Arbeit berücksichtigen sollten:

| Feld | Position | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- | --- |
| Konto | Bearbeitbares Raster auf der **Vertragszeilenkunden**-Registerkarte und den Formularen Hauptbereich und Schnellerfassung für einen Vertragszeilenkunden. | Alle aktiven Firmen. Dieses Feld wird gesperrt, nachdem der Datensatz erstellt wurde. Um das Feld zu aktualisieren, löschen Sie den Datensatz und erstellen Sie einen neuen. Wenn Sie Aktualisierungen aufgezeichnet haben, können Sie die Aufzeichnung nicht löschen. Sie können jedoch den Prozentsatz der Abrechnungsaufteilung für dieses Konto als null markieren. Wenn der Datensatz als null markiert ist, sind alle zukünftigen Kosten- und Ertragsdaten, die diesem Kunden zugeordnet oder aufgeteilt werden, betroffen. | Wenn Sie ein Konto aus der Hauptliste der Konten auswählen, um sie hinzuzufügen und zu speichern, wird der Vertragszeilenkunde auch als Vertragskunde hinzugefügt. Vertragszeilenkunden werden verwendet, wenn Rechnungen erstellt werden. |
| Prozentsatz der Abrechnungsteilung | Bearbeitbares Raster auf der **Vertragszeilenkunden**-Registerkarte und den Formularen Hauptbereich und Schnellerfassung für einen Vertragszeilenkunden. | Dieses Feld stellt den Prozentsatz jeder nicht in Rechnung gestellten Verkaufstransaktion dar, der diesem Vertragszeilenkunden zugeordnet wird. | Vertragszeilenkunden und Abrechnungsaufteilungsprozentsätze werden verwendet, wenn nach der Genehmigung Istwerte erstellt werden und wenn die Rechnung erstellt wird. |
| Nicht zu überschreitender Grenzwert | Bearbeitbares Raster auf der **Vertragszeilenkunden**-Registerkarte und den Formularen Hauptbereich und Schnellerfassung für einen Vertragszeilenkunden. | Gibt an, ob es ein ausgehandeltes Limit oder eine Obergrenze für den Gesamtbetrag gibt, der dem Kunden für diese Vertragszeile in Rechnung gestellt wird. | Das nicht zu überschreitende Limit für den Kunden der Vertragszeile wird verwendet, wenn Istwerte erstellt und die Rechnungen erstellt werden. |
| Zuständiges Unternehmen | Bearbeitbares Raster auf der **Angebotszeilenkunden**-Registerkarte und den Formularen Hauptbereich und Schnellerfassung für einen Angebotszeilenkunden. | Die juristische Person, in der dieser Kunde ansässig ist. Dieses Feld ist schreibgeschützt und auf die Eigentümerfirma des Angebots festgelegt. Die Liste der Kunden, die ins Feld **Konto** aufgenommen werden sollen, ist bereits in die Liste dieser Eigentümerfirma gefiltert. | Das Konzept einer Eigentümergesellschaft entspricht dem Konzept einer juristischen Person. Alle Kosten und Einnahmen aus diesem Projekt werden im Hauptbuch der Eigentümergesellschaft ausgewiesen. |
| Wird gerundet | Bearbeitbares Raster auf der **Vertragszeilenkunden**-Registerkarte und den Formularen Hauptbereich und Schnellerfassung für einen Vertragszeilenkunden. | Dieses Feld gibt an, ob dieser Kunde ein Standardrundungskunde für diese projektbasierte Vertragszeile ist. | Wenn Sie einen Istwert gemäß dem Prozentsatz der Abrechnungsaufteilung generieren, kann es zu Rundungsunterschieden kommen. Diesem Kunden werden in diesem Fall die Rundungsunterschiede zugeordnet. |

## <a name="edit-billing-split-percentages"></a>Aufteilungsprozentsätze bearbeiten

Fakturierungs-Aufteilungsprozentsätze können im Raster bearbeitet werden. Wenn die Prozentsätze für die Aufteilung der Abrechnung nicht 100 Prozent betragen, wird eine Fehlermeldung angezeigt. Aktualisieren Sie die Seite, nachdem Sie die Prozentsätze für die Aufteilung der Abrechnung bearbeitet haben, um den Fehler zu entfernen.

Sie können auch **Gleichmäßig verteilen** im Vertragszeilenkunden-Unterraster auswählen. Durch diese Aktion werden allen Vertragszeilenkunden gleichmäßig Abrechnungssplits zugewiesen. Wenn es einen Rundungsfaktor gibt, wird dieser dem Rundungskunden hinzugefügt. Ein Vertragszeilenkunde wird immer als **Rundungs**-Kunde gekennzeichnet, bei dem das **Rundungs**-Flag auf **Ja** gesetzt ist.


[!INCLUDE[footer-include](../includes/footer-banner.md)]