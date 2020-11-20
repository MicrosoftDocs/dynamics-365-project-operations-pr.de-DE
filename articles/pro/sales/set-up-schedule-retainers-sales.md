---
title: Einen Vorschusszeitplan einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten eines Vorschusszeitplans in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181271"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Einen Vorschusszeitplan einrichten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Vorschusszeitpläne werden auf der **Projektvertrag**-Seite in Dynamics 365 Project Operations eingerichtet.

1. Wählen Sie auf der **Projektvertrag**-Seite auf der **Vorauszahlungen und Vorschüsse**-Registerkarte die Option **Einen Vorschusszeitplan einrichten** aus.
2. Auf der sich öffnenden Dialogseite werden die in der folgenden Tabelle aufgeführten Felder angezeigt. Die Tabelle gibt eine Vorstellung davon, wie sich die eingegebenen Werte auf den zu erstellenden Vorschusszeitplan auswirken oder diesen beeinflussen.

| Feld | Beschreibung des Dataflows | Nachgelagerte Auswirkungen |
| --- | --- | --- |
| Projektvertragskunde | Der Kunde im Vertrag, dem der Vorschuss oder die Vorauszahlung in Rechnung gestellt wird. | Wenn Sie mehrere Kunden im Vertrag haben und jedem von ihnen einen bestimmten Einbehaltungs- oder Vorschussbetrag in Rechnung stellen möchten, erstellen Sie für jeden Kunden manuell eine Rechnung. |
| Beginn des Vorschusszeitplans | Geben Sie das Startdatum des Vorschusszeitplans ein. | Dieses Datum ist möglicherweise nicht das Datum, an dem die erste Vorauszahlung oder Vorschuss erstellt wird. Das Datum, an dem die erste Vorauszahlung oder Vorschuss erstellt wird, wird auch von der Rechnungshäufigkeit beeinflusst. |
| Ende des Vorschusszeitplans | Geben Sie das Enddatum des Vorschusszeitplans ein. | Dieses Datum ist möglicherweise nicht das Datum, an dem die letzte Vorauszahlung oder Vorschuss erstellt wird. Das Datum, an dem die letzte Vorauszahlung oder Vorschuss erstellt wird, wird auch von der Rechnungshäufigkeit beeinflusst. |
| Anzahl der zu erstellenden Vorschüsse | Wenn Sie die Anzahl der zu erstellenden Vorschüsse eingeben, verwendet das System das Startdatum und die Häufigkeit, um die Nummer in diesem Feld zu erstellen. | Wenn dieses Feld manuell aktualisiert wird, ignoriert das System den Wert im Feld **Ende des Vorschusszeitplans** und erstellt stattdessen die spezifische Anzahl von Vorauszahlungen oder Vorschüssen. |
| Rechnungshäufigkeit | Wie oft erstellt die Anwendung Vorauszahlungen und Vorschüsse? | Dieser Wert beeinflusst direkt die Anzahl der Vorauszahlungen und Vorschüsse sowie die erstellten Daten. |
| Gesamtbetrag | Der Gesamtbetrag ist der Betrag, der in die einzelnen Vorschüssen oder Vorauszahlungen aufgeteilt wird, die erstellt werden. | Es gibt keine nachgelagerten Auswirkungen für dieses Feld. |
