---
title: Tagesausgaben
description: In diesem Thema finden Sie Informationen dazu, wie Sie mit den Tagesausgaben arbeiten.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596049"
---
# <a name="per-diem-expenses"></a>Tagesausgaben

> [!IMPORTANT] 
> Die in diesem Abschnitt beschriebenen Funktionen stehen der Benutzerzielgruppe im Rahmen einer Vorschauversion zur Verfügung.

Eine Tageszahlung ist eine feste, im Voraus festgelegte Tagespauschale, die ein Unternehmen seinen Mitarbeitern für Unterkunft (Hotels), Mahlzeiten und Nebenkosten zahlt, die diesen Mitarbeitern entstehen, wenn sie zur Arbeit reisen. Diese Zulage zahlt das Unternehmen den Mitarbeitern statt der eigentlichen Reisekosten. Mitarbeiter können ihre **Nebenkosten/Sonstiges**-Tagespauschale zur Deckung von Trinkgeldern, Zimmerservice, Wäsche- oder Reinigungsdiensten für wichtige Geschäftstreffen verwenden. Der Tagessatz kann variieren, je nachdem, ob der Arbeitgeber die kombinierten Kosten für Unterkunft und Verpflegung oder nur die Kosten für Verpflegung und Nebenkosten erstattet.

Die Tagessätze können auf der Jahreszeit, dem Reiseort oder beiden basieren. Wenn Sie eine Tagessatzregel erstellen, können Sie einen Prozentsatz des Tagessatzes angeben, der einbehalten wird, wenn ein Miatarbeiter kostenlose Mahlzeiten oder Dienstleistungen erhält. Sie können auch eine Mindestanzahl von Stunden und eine maximale Anzahl von Stunden definieren, die der Reise eines Mitarbeiters durch den Tagessatz hinzugefügt werden.

Die Tagespauschale errechnet sich aus der gesamten angebotenen Tagespauschale abzüglich des Mahlzeitenabzug (Kosten für kostenlose Mahlzeiten), die dem Mitarnbeiter gewährt wird.

## <a name="configure-per-diems"></a>Tagespauschalen konfigurieren

Um Tagesausgaben zu konfigurieren, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Spesenverwaltung** \> **Einrichtung** \> **Allgemein** \> **Spesenverwaltungsparameter**
2. Auf der Registerkarte **Tagespauschale** im Feld **Berechnung des Mahlzeitenabzugs nach** wählen Sie aus, wie die Tagespauschalen berechnet werden sollen:

    - **Mahlzeitenart pro Reise** – berechnen Sie die Tagesspauschale anhand der eingetragenen Verpflegungsart (Frühstück, Mittag- oder Abendessen) und des für jede Verpflegungsart festgelegten Mahlzeitenabzugs für die Tagespauschale für die Dauer der Reise.
    - **Mahlzeitensart pro Tag** – berechnen Sie die Tagesspauschale anhand der eingetragenen Verpflegungsart und des für jede Verpflegungsart festgelegten Mahlzeitenabzugs für die Tagespauschale.
    - **Anzahl der Mahlzeiten pro Tag** – berechnen Sie die Tagespauschale anhand der Anzahl der pro Tag eingetragenen Mahlzeiten und des Mahlzeitenabzugs für die Anzahl der täglich bereitgestellten Mahlzeiten.

3. Wechseln Sie zu **Spesenmanagement** \> **Einrichtung** \> **Berechnungen und Codes** \> **Tagegeld Standorte**.
4. Fügen Sie Orte hinzu, an denen Tagegelder verwendet werden können.
5. Wählen Sie für jeden Standort, den Sie hinzufügen, auf der **Tagegelder**-Registerkarte den Tagessatz und die Währung aus, die zwischen bestimmten Start- und Enddaten für Unterkunft, Verpflegung und andere Ausgaben gelten. Um die Tagessätze und die Währungen zu konfigurieren, navigieren Sie zu **Spesenverwaltung** \> **Einrichtung** \> **Berechnungen und Codes** \> **Tagessätze**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Tagessätze in der neu gestalteten Spesenschnittstelle

Die Funktion „Tagessatz“ wird im neu gestateten **Spenseverwaltung**-Arbeitsbereich in Microsoft Dynamics 365 Finance-Version 10.0.25 und höher unterstützt.

Zum Aktivieren von Tagessätzen führen die folgenden Schritte aus.

1. Suchen und wählen Sie in dem **Funktionsverwaltung**-Arbeitsbereich die **Neu gestaltete Spesenabrechnungen**-Funktion in der Liste aus, und wählen Sie dann aus **Jetzt aktivieren**.
2. Suchen Sie die **Tagessatz für neu gestaltete Spesenabrechnungen**-Funktion in der Liste und wählen Sie sie aus, und wählen Sie dann **Jetzt aktivieren** aus.

## <a name="how-the-feature-works"></a>Funktionsweise der Funktion

Dieser Abschnitt enthält Beispiele für drei Konfigurationsszenarien. Für jedes Beispiel ist das **Berechnung des Mahlzeitenabzugs nach**-Feld auf einen anderen Wert gesetzt. Bei allen drei Beispielen ist der zu zahlende Gesamtbetrag bis zur Anwendung des Mahlzeitenabzugs gleich. Nach diesem Zeitpunkt unterscheidet sich der zu zahlende Gesamtbetrag für jedes Beispiel.

Führen Sie die folgenden Schritte aus, um die Tagesausgaben zu erstellen, die für alle drei Beispiele verwendet werden.

1. Wechseln Sie zu **Arbeitsbereiche** \> **Spensenverwaltung**
2. Wählen Sie **Neue Spesenabrechnung**, oder wählen Sie eine vorhandenen Spesenabrechnung aus der Liste aus.
3. Neue Ausgaben hinzufügen. Wählen Sie im Feld **Kategorie** die Option **Tagessatz** aus. Wählen Sie den Ort sowie das Start- und Enddatum Ihrer Reise aus. Der Tagessatz für Unterkunft, Verpflegung und Nebenkosten (sonstige Ausgaben) errechnet sich aus dem für den gewählten Standort festgesetzten Zuschuss.

    Sie wählen zum Beispiel **Redmond (USA)** als Standort aus. Die Tagespauschale für diesen Standort beträgt 150 US-Dollar (150 USD) für Unterkunft, 75 USD für Verpflegung und 5 USD für Nebenkosten. Das Startdatum ist der 10. Januar und das Enddatum ist der 14. Januar. Daher beträgt die ausgewählte Dauer fünf Tage, wenn die ausgewählte Konfiguration Kalendertage mit Zeit ist und die ausgewählte Zeit am Start- und Enddatum um 12:00 Uhr beginnt und endet. Hier sind die Berechnungen:

    - Zu zahlender Gesamtbetrag = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Verpflegung und Nebenkostenanteil des Gesamtbetrags = 5 × (75 + 5) = 400 USD

Wenn während der Reise Frühstück, Mittag- und Abendessen bereitgestellt wurden, müssen diese Mahlzeiten als Mahlzeitenabzug berücksichtigt werden.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Beispiel 1: Tagespauschale, bei der der Mahlzeitenabzug auf der Art der Mahlzeit pro Reise basieren

In diesem Beispiel beträgt der Mahlzeitenabzug 30 Prozent für das Frühstück, 30 Prozent für das Mittagessen und 40 Prozent für das Abendessen. Auf der **Spesenverwaltungsparameter**-Seite ist das **Berechnung des Mahlzeitenabzugs nach**-Feld auf **Art der Mahlzeit pro Reise** eingestellt. Hier sind die Berechnungen, wenn dem Mitarbeiter drei Frühstücke, zwei Mittagessen und keine Abendessen angeboten wurden:

- Mahlzeitenabzug = (3 × \[75 × 30 % \]) + (2×\[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Mahlzeiten und Nebenkosten = 400 – 112,50 = 287,50 USD
- Zu zahlender Gesamtbetrag = Gesamtzulage – Mahlzeitenabzug = 1.150 – 112,50 = 1.037,50 USD

![Tagesausgaben bei der der Mahlzeitenabzug auf der Art der Mahlzeit pro Reise basieren.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Beispiel 2: Tagespauschale, bei der der Mahlzeitenabzug für Mahlzeiten auf der Art der Mahlzeit pro Tag basieren

In diesem Beispiel beträgt der Mahlzeitenabzug 30 Prozent für das Frühstück, 30 Prozent für das Mittagessen und 40 Prozent für das Abendessen. Auf der **Spesenverwaltungsparameter**-Seite ist das **Berechnung des Mahlzeitenabzugs nach**-Feld auf **Art der Mahlzeit pro Tag** eingestellt. In diesem Fall deaktivieren Sie im **Verpflegung**-Raster im **Ausgaben bearbeiten**-Dialogfeld die Kontrollkästchen, um anzugeben, welche Mahlzeiten Ihnen während Ihrer Reise bereitgestellt wurden.

Hier sind zum Beispiel die Berechnungen, wenn Frühstück für die ersten drei Tage der Reise bereitgestellt wurde:

- Täglicher Mahlzeitenabzug für jeden der ersten drei Tage = 75 × 30 % = 22,50 USD
- Mahlzeitenabzug insgesamt = 3 × 22,50 = 67,50 USD
- Verpflegung und Nebenkosten für die Tage 1 bis 3 = 75 – 22,50 = 57,50 USD
- Verpflegung und Nebenkosten insgesamt = Summe der Verpflegung und Nebenkosten über fünf Tage = 400 – 67,50 = 332,50 USD
- Zu zahlender Gesamtbetrag = Gesamtbetrag – Mahlzeitenabzug = 1.150 – 67,50 = 1.082,50 USD

![Tagesausgaben bei der der Mahlzeitenabzug auf der Art der Mahlzeit pro Tag basieren.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Beispiel 3: Tagespauschale, bei der der Mahlzeitenabzug für Mahlzeiten auf der Anzahl der Mahlzeit pro Tag basieren

In diesem Beispiel wird der Mahlzeitenabzug basierend auf der Anzahl der Mahlzeiten berechnet, die pro Tag bereitgestellt wurden (d. h. **Berechnung des Mahlzeitenabzugs nach**-Feld auf der **Spesenverwaltungsparameter**-Seite ist auf **Anzahl der Mahlzeiten pro Tag** eingestellt). Deaktivieren Sie im **Verpflegung**-Raster im **Ausgaben bearbeiten**-Dialogfeld die Kontrollkästchen, um anzugeben, welche Mahlzeiten bereitgestellt wurden.
In diesem Fall basiert der Mahlzeitenabzug nur auf der Anzahl der bereitgestellten Mahlzeiten und nicht auf der Art der bereitgestellten Mahlzeit (Frühstück/Mittagessen/Abendessen).

Hier sind die Berechnungen für Tagessätze, wenn das Tagegeld 150 USD für Unterkunft, 75 USD für Mahlzeiten und 5 USD für Nebenkosten beträgt:

- **Zu zahlender Gesamtbetrag** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Eine Mahlzeit:** Mahlzeitenabzug = 20 % = 15 USD
- **Zwei Mahlzeiten:** Mahlzeitenabzug = 50 % = 37,50 USD
- **Drei Mahlzeiten:** Mahlzeitenabzug = 100 % = 75 USD

Hier sind die Berechnungen für die **Verpflegung und Nebenkostenpauschale**, die 5 USD für Nebenkosten enthält:

- Tag 1 – Zwei Mahlzeiten bereitgestellt = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Tag 2 – Zwei Mahlzeiten bereitgestellt = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Tag 3 – Eine bereitgestellte Mahlzeit = (75 – 15) + 5 = 60 + 5 = 65 USD
- Tag 4 – Keine Mahlzeiten bereitgestellt = (75 – 0) + 5 = 75 + 5 = 80 USD
- Tag 5 – Drei Mahlzeiten bereitgestellt = (75 – 75) + 5 = 0 + 5 = 5 USD

- Mahlzeiten und Nebenkosten insgesamt = Mahlzeiten und Nebenkosten für Tag 1+ Tag 2 +Tag 3+Tag 4+ Tag 5 = 235 USD
- Mahlzeitenabzug insgesamt = Mahlzeitenabzug für Tag 1+ Tag 2 +Tag 3+Tag 4+ Tag 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Zu zahlender Gesamtbetrag = Gesamtzulage – Mahlzeitenabzug insgesamt = 1.150 USD – 165 USD = 985 USD

![Tagesausgaben bei der der Mahlzeitenabzug auf der Anzahl der Mahlzeit pro Tag basieren.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Ab Finance-Version 10.0.23 können Sie bei Verwendung der neu gestalteten Spesenschnittstelle keine Tagesspesen mit sich überschneidenden Daten erstellen. Wenn Sie es versuchen, erhalten Sie eine Fehlermeldung.
