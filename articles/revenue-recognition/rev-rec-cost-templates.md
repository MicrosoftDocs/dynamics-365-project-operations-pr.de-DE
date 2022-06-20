---
title: Kostenvorlagen einrichten
description: Dieser Artikel informiert Sie darüber, wie Sie in Project Operations Kalkulationsvorlagen erstellen und verwenden können.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ffb45d46cf1305fffd5933f4c10b169bf802046d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918403"
---
# <a name="set-up-cost-templates"></a>Kostenvorlagen einrichten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Dieser Artikel informiert Sie darüber, wie Sie in Project Operations Kalkulationsvorlagen erstellen und verwenden können. Eine Kostenvorlage bestimmt:

- Die Projektkategorien für prognostizierte und tatsächliche Transaktionen, die in einen Prozentsatz der Projektabschlussberechnung einbezogen werden sollen. Der prozentuale Gesamtwert wird dann verwendet, um zu berechnen, wie viel Umsatz erfasst wird.
- Gibt an, ob der Fertigstellungsgrad geändert werden kann, wenn er automatisch berechnet wird.
- Ob der Prozentsatz der Fertigstellung anhand von Beträgen oder Einheiten berechnet wird.

## <a name="cost-template-example"></a>Beispiel für eine Kostenvorlage

Sie arbeiten an einem Website-Design-Projekt für einen Kunden, bei dem Sie eine Pauschalgebühr von 10.000 USD erheben. Sie prognostizieren, dass die Fertigstellung des Projekts 100 Stunden (5.000 USD) dauern wird. Sie prognostizieren auch zwei Flugtickets und vier Übernachtungen in einem Hotel für Reisen zum Kunden vor Ort (1.800 USD). Dies führt zu prognostizierten Gesamtkosten von 6.800 USD.

Wenn Sie den Prozess der Umsatzrealisierung zum Festpreis ausführen, um am Monatsende eine Schätzung zu erstellen, stellen Sie fest, dass Sie 35 Stunden an dem Projekt gearbeitet haben. Dies beinhaltet noch keine Flüge oder Hotelkosten. Sie ließen auch einen Assistenten fünf Stunden lang für das Projekt recherchieren, und zwar zu einem Preis von 100 USD, die nicht eingeplant waren.

Wenn Sie den prozentualen Gesamtwert für dieses Projekt berechnen, müssen Sie folgende Optionen auswählen:

- Möchten Sie alle Kosten (Stunden und Ausgaben) oder nur Stunden einbeziehen?
- Möchten Sie alle Stunden oder nur geplante Stunden einbeziehen?
- Möchten Sie den Prozentsatz der Fertigstellung basierend auf den Dollarkosten der geplanten Stunden (5.000 USD) oder nur anhand der Anzahl der Stunden (100) berechnen?

Ihre Antworten auf diese Fragen bestimmen die Optionen, die Sie in der Kostenvorlage festgelegt haben, und die Kategorien, die Sie in den Kostenvorlagenzeilen auswählen.

Die folgende Tabelle zeigt die Ergebnisse verschiedener Methoden zur Berechnung des prozentualen Gesamtwerts für dieses Szenario.

| Fertigstellung basierend auf | Dollarkosten oder Einheiten | Prozent abgeschlossen | Berechnung |
| --- | --- | --- | --- |
| Alle Stunden, keine Ausgaben | Dollarkosten | 37 % 35 x 50 USD + 100 USD = 1.850 USD 1.850 USD/5.000 USD |
| Alle Stunden, keine Ausgaben | Einheiten | 40 % | 40 Stunden/100 Stunden (einschließlich fünf ungeplante Stunden) |
| Geplante Stunden, keine Ausgaben | Dollarkosten oder Einheiten | 35 % | 35/100 Stunden oder 35 x 50 USD/5.000 |
| Alle Stunden und Ausgaben | Dollarkosten | 27,2 % | 1.850 USD/6.800 USD |

Die Entscheidung, welcher Ansatz zum Erstellen einer Kostenvorlage gewählt werden soll, kann von mehreren Überlegungen abhängen:

- Wenn Sie ungeplante Stunden in die Kostenvorlage aufnehmen, besteht die Gefahr, dass Sie zu 100 Prozent fertig sind, bevor das Projekt abgeschlossen ist. Dies liegt daran, dass die tatsächlichen Stunden größer sind als die geplanten Stunden. Wenn Sie eine der ersten beiden in der Tabelle aufgeführten Methoden verwenden, sollten Sie den Plan (prognostizierte Einheiten) ändern, wenn Sie Abweichungen feststellen. In diesem Fall würden Sie Stunden addieren oder subtrahieren, basierend auf Ihrem Wissen darüber, was zum Abschluss des Projekts erforderlich ist. Wenn das Projekt weitere 65 Stunden benötigt, würden Sie dem Plan fünf Stunden für insgesamt 105 Stunden hinzufügen. Wenn Sie wissen, dass Ihr Assistent weitere fünf Stunden recherchieren wird, beträgt die Gesamtsumme 110 Stunden.
- Wenn Sie die dritte in der Tabelle aufgeführte Methode verwenden, aktualisieren Sie die geplanten Stunden nur für Ihre eigene Zeit, um die prozentuale vollständige Berechnung korrekt zu halten. Ihre Rentabilität ändert sich, wenn ungeplante Stunden protokolliert werden, aber Sie bleiben in einem bekannten prozentualen Planungsabschluss.
- Wenn Sie die in der Tabelle aufgeführte vierte Methode verwenden, besteht das Risiko, dass Ausgaben zu unregelmäßigen Zeiten anfallen und sich möglicherweise nicht in Ihrem Fertigstellungsfortschritt widerspiegeln. Wenn die Ausgaben enthalten sind, kann dies dazu führen, dass Ihr Prozentsatz vollständig schwankt, als dies wünschenswert ist. Da Sie beispielsweise noch keinen Flug genommen haben, lag Ihr Prozentsatz für die Fertigstellung bei 27 Prozent anstelle von 35 Prozent oder 37 Prozent, wenn Sie die Berechnung allein auf die Zeit stützen. Wenn Sie eine Reise für zwei Nächte unternommen und Ihre Flug- und Hotelkosten genau vorhergesagt hätten, wäre der Prozentsatz der Fertigstellung 40,4 Prozent gewesen (1850 USD für Arbeit und 900 USD für Ausgaben = 2750 USD/6800 USD = 40,4 Prozent). Wenn also die Kosten für nur eine Flugreise anfallen, ändert sich der Prozentsatz der Fertigstellung von 27 Prozent auf 40 Prozent.

## <a name="create-cost-templates"></a>Kostenvorlagen erstellen
Gehen Sie wie folgt vor, um eine Kostenvorlagen zu erstellen:

1. Um auf Kostenvorlagen zuzugreifen, gehen Sie in der Dynamics 365 Finance-Umgebung zu **Projektmanagement und Buchhaltung** > **Einrichtungen** > **Schätzungen** > **Kostenvorlage**.
2. Wählen Sie **Neu** aus, um eine neue Kostenvorlage zu erstellen. Geben Sie einen Namen und eine Beschreibung ein.
3. Geben Sie die Kostenzeilen-ID für jeden Transaktionstyp an.
4. Wählen Sie eine Standardabschlussmethode aus:

  - **Automatisch**: Der Fertigstellungsgrad wird für ein Projekt automatisch berechnet. Die Ergebniswert kann nicht geändert werden.
  - **Manuell**: Der Fertigstellungsgrad wird für ein Projekt automatisch berechnet. Die Ergebniswert kann geändert werden.

  > [!NOTE]
  > Bei manuellen Berechnungen wird der Fertigstellungsgrad in **Manuelle Berechnung** auf der **Allgemein**-Registerkarte auf der **Schätzung**-Seite beibehalten.

5. Wählen Sie unter **Fertigstellung basierend auf** einen der folgenden Werte:

  - **Betrag**: Der Betrag in Buchungswährung berechnet den Fertigstellungsgrad.
  - **Einheit**: Die Menge berechnet den Fertigstellungsgrad.
  - **Linear**: Das System berechnet den Fertigstellungsgrad anteilig anhand der Start- und Enddaten des Projekts, um die Länge des Projekts zu bestimmen.

6. Wählen Sie **Kostenpositionen** aus, um die Kostenpositionen der Kostenvorlage zu überprüfen. Für jeden Transaktionstyp ist mindestens eine Kostenzeile erforderlich. Sie können jedoch mehrere Kostenzeilen für dieselben Transaktionstypen erstellen und die gewünschten Attribute für diese Zeilen festlegen.
7. Auf der **Kategorien**-Registerkarte wählen Sie die Projektkategorien aus, die in die Kostenvorlagenzeile aufgenommen werden sollen.
8. Auf der **Allgemein**-Registerkarte wählen Sie aus, ob diese Zeile in die Berechnung des Prozentsatzes der Fertigstellung einbezogen werden soll.
9. Wählen Sie die Methode zum Abschluss der Kosten aus, die bei der Berechnung des Fertigstellungsgrads verwendet werden soll.


[!INCLUDE[footer-include](../includes/footer-banner.md)]