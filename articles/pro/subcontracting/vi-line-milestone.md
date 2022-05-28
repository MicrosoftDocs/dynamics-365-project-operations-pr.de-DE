---
title: Kreditorenrechnungspositionen für Meilensteine
description: In diesem Thema wird erläutert, wie Kreditorenrechnungspositionen für Meilensteine in einem Untervertrag erstellt werden.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590621"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Kreditorenrechnungspositionen für Meilensteine

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Eine Kreditorenrechnung in Microsoft Dynamics 365 Project Operations kann Kreditorenrechnungspositionen für Meilensteine haben, die in einer Untervertragsposition definiert sind. Projektmanager können Kreditorenrechnungspositionen für Meilensteine verwenden, um die Kosten von beschafften Dienstleistungen als auf Meilensteinen basierende Kosten zu erfassen, die für Dienstleistungen oder Produkte anfallen, die für das Projekt beschafft werden.

Kreditorenrechnungspositionen für Meilensteine müssen immer auf eine Untervertragsposition verweisen, die eine Festpreis-Fakturierungsmethode hat. Wenn eine Kreditorenrechnungsposition für Meileinsteine auf eine Untervertragsposition verweist, können Projektmanager die zugrunde liegenden Kosten der Zeit, Ausgaben oder Materialien abgleichen und verifizieren, die die Untervertragsposition gegenüber dem Meilenstein verweist, der durch den Kreditor fakturiert wird.

Die folgende Tabelle enthält Informationen zu den Feldern auf Kreditorenrechnungspositionen für Meilensteine.

| Feld | Beschreibung des Dataflows | Funktionsauswirkung |
| --- | --- | --- |
| Name des Dataflows | Der Name der Kreditorenrechnungsposition, um bei der Identifizierung zu helfen. | Dieser Name wird als erste Spalte in allen Nachschlagevorgängen angezeigt, die auf Kreditorenrechnungspositionen basieren. |
| Beschreibung des Dataflows | Eine kurze Beschreibung der Dienste, die vom Kreditor in der Kreditorenrechnungsposition in Rechnung gestellt werden. | Nein |
| Fremdarbeit | Die Fremdarbeit, für die die Dienste ursprünglich bestellt wurden. | Wenn eine Fremdarbeit für die Kreditorenrechnung ausgewählt wird, erben alle Zeilen auf der Kreditorenrechnung diese Auswahl. Eine Kreditorenrechnung darf keine Kreditorenrechnungspositionen haben, die auf verschiedene Fremdarbeiten verweisen. |
| Fremdarbeitsposition | Die Fremdarbeitsposition, für die die Dienste bestellt wurden. Die Liste der auswählbaren Fremdarbeitspositionen ist auf die Positionen der ausgewählten Fremdarbeit beschränkt. | Wenn eine Unterauftragsposition in einer Kreditorenrechnungsposition für Meilensteine ausgewählt wird, sind die Felder **Rolle** und **Transaktionskategorie** und produktbezogene Felder irrelevant und nicht verfügbar. Die Felder **Menge**, **Einheit** und **Einheitsgruppe** sind auch bei Meilenstein-basierten Kreditorenrechnungspositionen nicht relevant. |
| Buchungsdatum | Das Datum, an dem die tatsächlichen Kosten der Kreditorenrechnungsposition im Projekt erfasst werden. | Nein |
| Transaktionsklasse | Wählen Sie **Meilenstein**, um eine Kreditorenrechnung für einen abgeschlossenen Meilenstein zu erfassen, der in einer Unterauftragsposition definiert wurde. | Nein |
| Meilenstein | Wählen Sie den Meilenstein aus, der in der zugehörigen Unterauftragsposition definiert ist, die als **Bereit zur Rechnungsstellung** gekennzeichnet ist. | Meilensteine bei Untervertragspositionen mit dem Status **Bereit für Rechnungsstellung** können auf einer Kreditorenrechnungsposition ausgewählt werden. |
| Project | Der Name des Projekts, für das die in Rechnung gestellten Dienste verwendet wurden. | Dieses Feld ist ein Pflichtfeld und darf nicht leer gelassen werden. |
| Task | Der Name der Aufgabe, für die die in Rechnung gestellten Dienste verwendet wurden. Dieses Feld ist nur verfügbar, wenn ein Projekt ausgewählt ist. Die Auswahl einer Projektaufgabe ist optional. | Wenn dieses Feld leer gelassen wird, kann der Projektmanager die Kreditorenrechnungsposition der Klasse der Transaktionen auf zugehörigen mit Untervertragspositionen abgleichenm die für eine beliebige Aufgabe des Projekts erfasst wird. Wenn die Kreditorenrechnungsposition nicht auf eine Fremdarbeitsposition verweist und dieses Feld leer gelassen wird, werden die Ist-Kosten, die von der Kreditorenrechnungsposition erstellt werden, nicht mit noch nicht fakturierten Verkaufs-Ist-Werten verknüpft. In diesem Fall können bei eingerichteter aufgabenbezogener Abrechnung die Kosten dem Endkunden ggf. nicht in Rechnung gestellt werden. |
| Meilenstein-Betrag | Geben Sie den Wert des Meilensteins ein, der in der zugehörigen Unterauftragsposition definiert ist, die bereit zur Rechnungsstellung ist. | Nein |
| Mehrwertsteuer | Geben Sie den Umsatzsteuerbetrag ein. | Nein |
| Gesamtbetrag | Der Gesamtbetrag der Kreditorenrechnungsposition, einschließlich Steuern. Dieses Feld wird als *Meilensteinbetrag* + *Mehrwertsteuer* berechnet. | Nein |

> [!NOTE]
> Wenn eine Kreditorenrechnungsposition erstellt wird, die auf einen Meilenstein der Unterauftragsposition verweist, wird der Status des Meilensteins der Unterauftragsposition auf **Kreditorenrechnung erstellt** aktualisiert. Wenn diese Kreditorenrechnung dann bestätigt wird, wird der Status des Meilensteins der Unterauftragsposition auf **Kreditorenrechnung bestätigt** aktualisiert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
