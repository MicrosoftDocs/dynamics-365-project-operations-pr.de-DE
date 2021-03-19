---
title: Eine Vorkalkulation in eine projektbasierte Vertragszeile importieren
description: Dieses Thema enthält Informationen zum Importieren von Vorkalkulationen aus einem Projekt in eine Vertragszeile.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d51eb890a4744051ddd7268e1f1f11b15a23b609
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278372"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Eine Vorkalkulation in eine projektbasierte Vertragszeile importieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In Dynamics 365 Project Operations können Sie Schätzungen aus einem Projekt in eine projektbasierte Vertragszeile importieren.

1. Stellen Sie sicher, dass das Feld **Projekt** in der projektbasierten Vertragszeile ausgefüllt ist.
2. Wählen Sie auf der Registerkarte **Vertragszeilendetails** im Unterraster **Aus Projektvorkalkulation importieren** aus. Eine Dialogseite mit Zusammenfassungsoptionen wird geöffnet. Die verfügbaren Zusammenfassungsoptionen lauten **Transaktionsklasse**, **Kategorie**, **Rolle** und **Projektaufgabe**. Basierend auf der Auswahl für die Zusammenfassung wird die Schätzung aus dem Projekt für alle in dieser Vertragszeile enthaltenen Transaktionsklassen kopiert. 
3. Um zu überprüfen, welche Transaktionsklassen enthalten sind, prüfen Sie auf der Registerkarte **Allgemein** der Vertragszeile die Werte in den Feldern **Zeit einschließen**, **Ausgaben einschließen** und **Gebühren einschließen**.

Wenn Sie Vorkalkulationen importieren, verwendet die Anwendung standardmäßig die Preisgestaltung in den Projektpreislisten, die dem Vertrag und der Einrichtung des Fakturierungstyps in der Vertragszeile zugeordnet ist. Wenn eine Rolle oder Kategorie in der Vertragszeile als nicht fakturierbar eingerichtet ist, wird die importierte Vorkalkulationsposition für diese Rolle oder Kategorie als nicht fakturierbar festgelegt und wird nicht zum Vertragswert der Vertragszeile addiert.

Wenn eine Vertragszeile Positionsdetails enthält, werden die Felder **Vertragswert** und **Geschätzte Steuer** in der Vertragszeile zusammengefasst und können nicht bearbeitet werden.

Wenn mehrere Optionen zum Zusammenfassen ausgewählt sind, versucht das System nach allen ausgewählten Optionen zusammenzufassen. Die Zusammenfassungsausgabe führt zu mehr importierten Vertragszeilen als wenn Sie nur eine Zusammenfassungsoption auswählen.

Beispiel: Wenn das Projekt die folgenden Vorkalkulationspositionen für Ausgaben enthält:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |

Wenn der Benutzer die Zusammenfassung nach **Transaktionsklasse** auswählt, werden die folgenden Informationen importiert:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1.10.2020 | 3.34 | 840 | 2800 |

Wenn der Benutzer die Zusammenfassung nach **Transaktionsklasse** und **Kategorie** auswählt, werden die folgenden Informationen importiert:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1.10.2020 | 6 | 200 | 1200 |

Wenn sich der Benutzer dazu entscheidet, eine Zusammenfassung nach **Transaktionsklasse**, **Kategorie** und **Blattknotenaufgabe** durchzuführen, wird Folgendes importiert. Beachten Sie, dass dieses Ergebnis mit dem Ergebnis des Projekts übereinstimmt:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]