---
title: Schätzungen aus einem Projekt in eine Projektvertragsposition importieren
description: Dieser Artikel enthält Informationen zum Importieren von Kostenvoranschlägen aus einem Projekt in eine Vertragszeile.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824673"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Schätzungen aus einem Projekt in eine Projektvertragsposition importieren

_**Gilt für:** Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung, Project Operations für Ressourcen/nicht vorrätige Szenarien_ _

In Dynamics 365 Project Operations können Sie Schätzungen aus einem Projekt in eine projektbasierte Vertragszeile importieren.

1. Stellen Sie sicher, dass das Feld **Projekt** in der projektbasierten Vertragszeile ausgefüllt ist.
2. Wählen Sie auf der Registerkarte **Vertragszeilendetails** im Unterraster **Aus Projektvorkalkulation importieren** aus. Eine Dialogseite mit Zusammenfassungsoptionen wird geöffnet. Die verfügbaren Zusammenfassungsoptionen lauten **Transaktionsklasse**, **Kategorie**, **Rolle** und **Projektaufgabe**.
3. Basierend auf der Auswahl für die Zusammenfassung wird der Kostenvoranschlag aus dem Projekt für alle in dieser Vertragszeile enthaltenen Transaktionsklassen und -aufgaben kopiert. Um zu überprüfen, welche Transaktionsklassen enthalten sind, prüfen Sie auf der Registerkarte in der projektbasierten Vertragszeile **Allgemein** die Werte in den Feldern **Zeit einschließen**, **Ausgaben einschließen** und **Gebühren einschließen**. 
4. Um zu sehen, welche Aufgaben enthalten sind, wählen Sie die Registerkarte **Fakturierbare Aufgaben** in der Vertragszeile aus. Basierend auf den zugehörigen Aufgaben, bei denen das Feld **Eingeschlossene Transaktionsklassen** auf **Ja** festgelegt ist, werden alle Vorkalkulationen für diese Kombinationen aus Aufgabe und Transaktion in die Vertragszeile importiert.

Wenn Sie Vorkalkulationen importieren, verwendet das System standardmäßig die Preisgestaltung in den Projektpreislisten, die dem Vertrag und der Einrichtung des Fakturierungstyps in der Vertragszeile zugeordnet ist. Wenn eine Aufgabe, Rolle oder Kategorie in der Vertragszeile als nicht fakturierbar eingerichtet ist, wird die importierte Vorkalkulationsposition als nicht fakturierbar festgelegt und wird nicht zum Vertragswert der Vertragszeile addiert.

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
| &nbsp; | &nbsp; | 1.10.2020 | 3.34 | 840 | 2800 |

Wenn der Benutzer die Zusammenfassung nach **Transaktionsklasse** und **Kategorie** auswählt, werden die folgenden Informationen importiert:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1.10.2020 | 6 | 200 | 1200 |

Wenn sich der Benutzer dazu entscheidet, eine Zusammenfassung nach **Transaktionsklasse**, **Kategorie** und **Blattknotenaufgabe** durchzuführen, wird Folgendes importiert. Beachten Sie, dass dieses Ergebnis mit dem Ergebnis des Projekts übereinstimmt:

| Task | Kateg. | Datum | Menge | Einheitenpreis | Betrag |
| --- | --- | --- | --- | --- | --- |
| Aufgabe A | Flugpreis | 1.10.2020 | 4 | 400 | 1600 |
| Aufgabe B | Hotel | 1.10.2020 | 4 | 200 | 800 |
| Aufgabe C | Hotel | 1.11.2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
