---
title: Vorkalkulationen für ein Projekt in eine Projektangebotsposition importieren
description: Dieser Artikel informiert Sie darüber, wie Sie Kostenvoranschläge aus einem Projekt in eine Angebotszeile importieren.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915045"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Vorkalkulationen für ein Projekt in eine Projektangebotsposition importieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Wenn ein Projekt in der Vorverkaufsphase erstellt wird, können Sie den Finanzvoranschlag aus dem Projekt in die projektbasierte Angebotsposition importieren.

1. Stellen Sie sicher, dass die projektbasierte Angebotsposition die Projektinformationen im **Projekt**-Feld enthält.
2. Wählen Sie auf der **Detailinformationen zur Angebotsposition**-Registerkarte **Import aus Projektvorkalkulation**.
3. Die Dialogseite wird geöffnet, wählen Sie eine der folgenden Optionen zur Zusammenfassung aus:

  - **Transaktionsklasse**
  - **Kategorie**
  - **Rolle** 
  - **Projektaufgabe**

Basierend auf Ihrer Auswahl wird die Schätzung aus dem Projekt für alle in dieser Angebotsposition enthaltenen Transaktionsklassen kopiert. Um zu überprüfen, welche Transaktionsklassen enthalten sind, wählen Sie die Registerkarte **Allgemeines** in der projektbasierten Angebotsposition aus und überprüfen Sie die Werte für **Zeit einschließen**, **Ausgaben einschließen** und **Gebühren einschließen**.

Wenn Sie Vorkalkulationen importieren, verwendet das System standardmäßig die Preisgestaltung basierend auf den dem Angebot beigefügten Projektpreislisten und den in der projektbasierten Angebotsposition festgelegten Fakturierungstyp. Wenn eine Rolle oder Kategorie in der projektbasierten Angebotsposition als nicht kostenpflichtig eingerichtet ist, wird die importierte Schätzungsposition als nicht kostenpflichtig festgelegt und addiert sich nicht zum angegebenen Wert der Angebotsposition.

Wenn eine Angebotsposition Positionsdetails enthält, werden die Felder **Angebotswert** und **Geschätzte Steuer** in der Angebotsposition zusammengefasst und können nicht bearbeitet werden.

Wenn mehrere Optionen zum Zusammenfassen ausgewählt sind, versucht das System nach allen ausgewählten Optionen zusammenzufassen. Das Ergebnis ist, dass die Ausgabe importierter Angebotspositionen höher ist, als wenn Sie nur eine Zusammenfassungsoption ausgewählt haben.

Beispiel: Wenn das Projekt die folgenden Vorkalkulationspositionen für Ausgaben enthält.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
