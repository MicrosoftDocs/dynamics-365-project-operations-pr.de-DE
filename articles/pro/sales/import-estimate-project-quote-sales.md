---
title: Vorkalkulationen aus einem Projekt in eine Projektangebotsposition importieren
description: In diesem Artikel erfahren Sie, wie Sie Kostenvoranschläge aus einem Projekt in eine Projektangebotszeile importieren können.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824485"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Vorkalkulationen aus einem Projekt in eine Projektangebotsposition importieren 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung Project Operations für Ressourcen/nicht vorrätige Szenarien_

Wenn ein Projekt in der Vorverkaufsphase erstellt wird, können Sie den Finanzvoranschlag aus dem Projekt in die projektbasierte Angebotsposition importieren.

1. Stellen Sie sicher, dass die projektbasierte Angebotsposition die Projektinformationen im **Projekt**-Feld enthält.
2. Wählen Sie auf der **Detailinformationen zur Angebotsposition**-Registerkarte **Import aus Projektvorkalkulation**.
3. Die Dialogseite wird geöffnet, wählen Sie eine der folgenden Aggregationsoptionen aus.

  - **Transaktionsklasse**
  - **Kategorie**
  - **Rolle** 
  - **Projektaufgabe**

Basierend auf Ihrer Auswahl wird die Schätzung aus dem Projekt für alle in dieser Angebotsposition enthaltenen Transaktionsklassen kopiert. Um zu überprüfen, welche Transaktionsklassen enthalten sind, wählen Sie die Option **Allgemein** in der projektbasierten Angebotszeile auf die Registerkarte, und überprüfen Sie die Werte für **Zeit einschließen**, **Ausgaben einschließen**, **Materialien einschließen** und **Gebühren einschließen**.  Um zu prüfen, welche Aufgaben enthalten sind, wählen Sie die Registerkarte **Fakturierbare Aufgaben** in der Angebotsposition aus.

Basierend auf den zugehörigen Aufgaben und enthaltenen Transaktionsklassen, werden die Vorkalkulationen für diese Kombinationen aus Aufgabe und Transaktionsklasse in die Angebotsposition importiert.

Wenn Sie Schätzungen importieren, verwendet das System standardmäßig die Preisgestaltung basierend auf den dem Angebot beigefügten Projektpreislisten und der in der projektbasierten Angebotsposition festgelegten Abrechnungsart. Wenn eine Aufgabe, Rolle oder Kategorie in der projektbasierten Angebotsposition als nicht fakturierbar eingerichtet ist, wird die importierte Vorkalkulationsposition als nicht fakturierbar festgelegt und wird nicht zum Angebotswert der Angebotsposition addiert.

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
|||1.10.2020 | 3.34 | 840 | 2800 |

Wenn der Benutzer die Aggregation nach Transaktionsklasse und Kategorie auswählt, werden die folgenden Informationen importiert.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| | Hotel | 1.10.2020 | 6 | 200 | 1200 |

Wenn der Benutzer die Zusammenfassung nach Transaktionsklasse, Kategorie und Blattknotenaufgabe auswählt, werden die folgenden Informationen importiert. Beachten Sie, dass dieses Ergebnis mit dem Ergebnis des Projekts übereinstimmt.

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
