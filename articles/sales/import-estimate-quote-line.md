---
title: Schätzungen für ein Projekt in eine projektbasierte Angebotsposition importieren
description: Dieses Thema enthält Informationen zum Importieren von Schätzungen aus einem Projekt in eine Angebotsposition.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908139"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Schätzungen für ein Projekt in eine projektbasierte Angebotsposition importieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Wenn ein Projekt in der Vorverkaufsphase erstellt wird, können Sie den Finanzvoranschlag aus dem Projekt in die projektbasierte Angebotsposition importieren.

1. Stellen Sie sicher, dass die projektbasierte Angebotsposition die Projektinformationen im **Projekt**-Feld enthält.
2. Wählen Sie auf der **Detailinformationen zur Angebotsposition**-Registerkarte **Import aus Projektschätzung**.
3. Die Dialogseite wird geöffnet, wählen Sie eine der folgenden Aggregationsoptionen aus.

  - **Transaktionsklasse**
  - **Kategorie**
  - **Rolle** 
  - **Projektaufgabe**

Basierend auf Ihrer Auswahl wird die Schätzung aus dem Projekt für alle in dieser Angebotsposition enthaltenen Transaktionsklassen kopiert. Um zu überprüfen, welche Transaktionsklassen enthalten sind, wählen Sie die Registerkarte **Allgemeines** in der projektbasierten Angebotsposition aus und überprüfen Sie die Werte für **Zeit einschließen**, **Ausgaben einschließen** und **Gebühren einschließen**.

Wenn Sie Schätzungen importieren, verwendet das System standardmäßig die Preisgestaltung basierend auf den dem Angebot beigefügten Projektpreislisten und der in der projektbasierten Angebotsposition festgelegten Abrechnungsart. Wenn eine Rolle oder Kategorie in der projektbasierten Angebotsposition als nicht kostenpflichtig eingerichtet ist, wird die importierte Schätzungsposition als nicht kostenpflichtig festgelegt und addiert sich nicht zum angegebenen Wert der Angebotsposition.

Wenn eine Angebotsposition Positionsdetails enthält, werden die Felder **Angebotswert** und **Geschätzte Steuer** in der Angebotsposition zusammengefasst und können nicht bearbeitet werden.

Wenn mehrere Aggregationsoptionen ausgewählt sind, versucht die Aggregation nach allen ausgewählten Optionen zusammenzufassen. Dies bedeutet, dass die Ausgabe importierter Angebotspositionen höher ist, als wenn Sie nur eine Aggregationsoption ausgewählt haben.

Beispiel: Wenn das Projekt die folgenden Schätzzeilen für Ausgaben enthält.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |

Wenn der Benutzer die Aggregation nach Transaktionsklasse auswählt, werden die folgenden Informationen importiert.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| | | 1.10.2020 | 3.34 | 840 | 2800 |

Wenn der Benutzer die Aggregation nach Transaktionsklasse und Kategorie auswählt, werden die folgenden Informationen importiert.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| | Hotel | 1.10.2020 | 6 | 200 | 1200 |

Wenn der Benutzer die Aggregation nach Transaktionsklasse, Kategorie und Blattknotenaufgabe auswählt, werden die folgenden Informationen importiert. Beachten Sie, dass dieses Ergebnis mit dem Ergebnis des Projekts übereinstimmt.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |