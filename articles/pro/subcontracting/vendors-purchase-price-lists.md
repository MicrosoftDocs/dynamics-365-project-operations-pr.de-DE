---
title: Lieferanten- und Einkaufspreislistenverwaltung in Project Operations
description: Dieser Artikel enthält Informationen, die Ihnen helfen, Lieferantendaten und Preislisten für den Kauf von Unteraufträgen zu erstellen und zu pflegen.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261886"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Lieferanten- und Einkaufspreislistenverwaltung in Project Operations


_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

## <a name="vendors-in-project-operations"></a>Lieferanten in Project Operations

In Microsoft Dynamics 365 Project Operations haben Kreditorenkonten den Beziehungstyp **Zulieferer** oder **Lieferant**. Sie können nur einen Kontensatz auswählen, der eine dieser Beziehungsarten als Lieferant für einen Fremdarbeitsauftrag hat.

Sie können einem Lieferantendatensatz eine oder mehrere Einkaufspreislisten zuordnen. Jede Einkaufspreisliste, die einem Lieferantendatensatz zugeordnet ist, sollte jedoch eine eindeutige Datumsgültigkeit aufweisen. Project Operations unterstützt keine überlappende Datumseffektivität in Einkaufspreislisten.

Standardmäßig werden die folgenden Felder und Konzepte in einem Lieferantendatensatz für jede Fremdarbeit verwendet, die für den Lieferanten erstellt wird:

- Zahlungsbedingungen
- Kontakt für Rechnung
- Primärer Kontakt

    > [!NOTE]
    > Standardmäßig wird der Hauptansprechpartner des Lieferanten als Konto-Manager des Zulieferers des Fremdarbeitsvertrags verwendet.

- Währung
- Aktuelle Einkaufspreislisten

## <a name="purchase-price-lists-in-project-operations"></a>Einkaufspreislisten in Project Operations

Eine Preisliste, in der das Feld **Kontext** auf **Einkauf** gesetzt ist, gilt als Einkaufspreisliste. Einkaufspreislisten können so definiert werden, dass sie einen Katalog von Einkaufspreisen für Zeit, Aufwand und Material darstellen. Einkaufspreislisten ähneln Einstands- und Verkaufspreislisten in Project Operations. Die folgenden Konzepte gelten für Einkaufspreislisten in gleicher Weise wie für Einstands- und Verkaufspreislisten:

- **Datumsgültigkeit** – Einkaufspreislisten haben Datumsgültigkeit. Die Datumsgültigkeit wird durch die Felder Startdatum und Enddatum auf jeder Preisliste dargestellt. Die Zeit zwischen dem Startdatum und dem Enddatum ist der Gültigkeitszeitraum für das Datum.
- **Währung** – Die Währung im Preislistenkopf wird als Währung verwendet, in der Einkaufspreise für Arbeit, Aufwandskategorien und Produkte im Katalog ausgedrückt werden.
- **Standardzeiteinheit** – Die Standardzeiteinheit drückt die Arbeitspreise für Einkäufe aus. Das Feld „Zeiteinheit“ in einer Preisliste wird nur verwendet, um einen Standardwert anzugeben. Dieser Wert kann in einzelnen Rollenpreiszeilen geändert werden.

Einkaufspreislisten können als Verknüpfungen, die als Projektpreislisten bekannt sind, an Lieferantendatensätze angehängt werden. Diese Preislisten werden verwendet, um Standardpreise für Lohnbearbeitungspositionen einzugeben. Wenn einem Lieferantendatensatz mehrere Einkaufspreislisten zugeordnet sind, wird standardmäßig die aktuellste Preisliste für Fremdarbeitsunteraufträge verwendet, die für den Lieferanten erstellt werden. Nur Preislisten, bei denen das Feld **Kontext** auf **Einkauf** gesetzt ist, können an Lieferantendatensätze angehängt werden.

### <a name="subcontract-specific-purchase-price-lists"></a>Fremdarbeitsspezifische Einkaufspreislisten

Einkaufspreislisten können als Verknüpfungen, die als Projektpreislisten bekannt sind, an Fremdarbeitsdatensätze angehängt werden. Diese Preislisten werden verwendet, um Standardpreise für Lohnbearbeitungspositionen einzugeben. Wenn einem Fremdarbeitsauftrag mehrere Einkaufspreislisten angehängt sind, muss jede ein eigenes Datumsgültigkeitsdatum haben. Project Operations unterstützt keine Einkaufspreislisten mit überlappender Datumseffektivität. Nur Preislisten, bei denen das Feld **Kontext** auf **Einkauf** gesetzt ist, können an Fremdarbeitsdatensätze angehängt werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
