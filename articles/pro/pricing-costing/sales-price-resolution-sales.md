---
title: Vertriebspreise für Projektschätzungen und tatsächliche Transaktionen bestimmen
description: Dieser Artikel informiert Sie darüber, wie Vertriebspreise für Projektschätzungen und -Istwerte bestimmt werden.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410117"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Vertriebspreise für Projektschätzungen und tatsächliche Transaktionen bestimmen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Um den Verkaufspreise für Schätzungen und Istwerte in Microsoft Dynamics 365 Project Operations zu bestimmen, verwendet das System zunächst das Datum und die Währung des verknüpften Projektangebots oder -vertrags, um die Vertriebspreisliste aufzulösen. Im eigentlichen Kontext verwendet das System das Feld **Transaktionsdatum**, um zu bestimmen, welche Preisliste anwendbar ist. Nachdem der Verkaufspreis bestimmt wurde, bestimmt das System den Verkaufs- oder Fakturierungssatz auf.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Verkaufsraten in Istwert- und Vorkalkulationszeilen für Zeit bestimmen

Geschätzer Kontext für **Zeit** bezieht sich auf:

- Angebotszeilendetails für **Zeit**.
- Vertragsszeilendetails für **Zeit**.
- Ressourcenzuweisung für ein Projekt.

Tatsächlicher Kontext für **Zeit** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Zeit**.
- Journalzeilen, die erstellt werden, wenn ein Zeiteintrag übermittelt wird.
- Rechnungszeilendetails für **Zeit**. 

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Fakturierungssatz als Standard festzulegen.

1. Das System stimmt die Felder **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit ab, um diese mit den Rollenpreisen in der aufgelösten Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie sofort einsatzbereite Preisdimensionen für Fakturierungssätze verwenden. Wenn Sie die Preise basierend auf anderen Feldern anstatt zusätzlich zu **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren, ist das dann die Kombination von Feldern, die verwendet wird, um eine übereinstimmende Rollenpreiszeile abzurufen.
1. Wenn das System eine Rollenpreiszeile findet, die eine Fakturierungsrate für die Feldkombination **Rolle** und **Ressourcenzuordnungseinheit** aufweist, wird der Fakturierungssatz als Standardwert verwendet.
1. Wenn das System die Feldwerte **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** nicht zuordnen kann, ruft es die Rollenpreiszeilen mit übereinstimmenden Werten für das Feld **Rolle** aber Nullwerte für das Feld Ressourceneinheit ab. Nachdem das System einen passenden Rollenpreisdatensatz gefunden hat, wird der Fakturierungssatz aus diesem Datensatz standardmäßig als Fakturierungssatz festgelegt. Diese Übereinstimmung setzt eine sofort einsatzbereite Konfiguration für die relative Priorität der **Rolle** im Vergleich zur **Ressourcenzuordnungseinheit** als Verkaufspreisdimension voraus.

> [!NOTE]
> Wenn Sie eine andere Priorisierung der Felder **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die jedem Preisdimensionswert in der Reihenfolge ihrer Priorität entsprechen. Zeilen mit Nullwerten für diese Dimensionen kommen zuletzt.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Bestimmen der Verkaufsraten in Istwert- und Vorkalkulationszeilen für Ausgaben

Geschätzer Kontext für **Ausgaben** bezieht sich auf:

- Angebotszeilendetails für **Ausgaben**.
- Vertragszeilendetails für **Ausgaben**.
- Ausgabenschätzungszeile in einem Projekt.

Tatächlicher für **Ausgaben** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Ausgabe**.
- Journalzeilen, die erstellt werden, wenn ein Ausgabeneintrag übermittelt wird.
- Rechnungszeilendetails für **Ausgaben**. 

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Einheitsvertriebskostenpreis als Standard einzugeben.

1. Das System stimmt die Feldkombination **Kategorie** und **Einheit** in der Vorkalkulationszeile für **Ausgaben**, um diese mit den Kategoriepreiszeilen in der aufgelösten Preisliste abzugleichen.
1. Wenn das System eine Kategoriepreiszeile findet, die eine Verkaufsrate für die Feldkombination **Kategorie** und **Einheit** hat, dann wird die Verkaufsrate standardmäßig festgelegt.
1. Wenn das System eine übereinstimmende Kategoriepreiszeile findet, könnte die Preismethode verwendet werden, um den Verkaufspreis als Standard festzulegen. Die folgende Tabelle zeigt das Standardverhalten für Ausgabenpreisen in Project Operations an.

    | Context | Preisberechnungsmethode | Standardpreis |
    | --- | --- | --- |
    | Vorkalkulation | Einzelpreis | Basierend auf der Kategoriepreiszeile. |
    |        | Zum Einstandswert | 0.00 |
    |        | Aufschlag auf Kosten | 0.00 |
    | Tatsächl. | Einzelpreis | Basierend auf der Kategoriepreiszeile. |
    |        | Zum Einstandswert | Basierend auf den damit verbundenen tatsächlichen Kosten. |
    |        | Aufschlag auf Kosten | Einen Aufschlag wird gemäß der Preiszeile der Kategorie auf den Stückkostensatz der zugehörigen tatsächlichen Kosten angewendet. |

1. Wenn das System die Feldwerte **Kategorie** und **Einheit** nicht abgleichen kann, ist die Verkaufsrate standardmäßig **0** (Null).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Bestimmen von Verkaufsraten für tatsächliche und geschätzte Zeilen für Material

Geschätzer Kontext für **Material** bezieht sich auf:

- Angebotszeilendetails für **Material**.
- Vertragszeilendetails für **Material**.
- Materailschätzungszeile in einem Projekt.

Tatächlicherkontext für **Material** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Material**.
- Journalzeilen, die erstellt werden, wenn ein Materialnutzungsprotokoll übermittelt wird.
- Rechnungszeilendetails für **Material**. 

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Einheitsvertriebskostenpreis als Standard einzugeben.

1. Das System verwendet die Felder **Produkt** und **Einheit** in der Schätzzeile für **Material**, das mit den Preislisten-Artikelzeilen in der aufgelösten Preisliste übereinstimmt.
1. Wenn das System eine Preislisten-Artikelzeile findet, die eine Verkaufsrate für die **Produkt**- und **Einheit**-Feldkombination hat und die Preismethode **Währungsbetrag** ist, wird der in der Preislistenzeile angegebene Verkaufspreis verwendet. 
1. Wenn die **Produkt** und **Einheit** Feldwerte nicht übereinstimmen oder wenn die Preismethode etwas anderes ist als **Währungsbetrag**, wird die Verkaufsrate standardmäßig auf **0** (Null) festgelegt. Dieses Verhalten tritt auf, weil Project Operations nur die **Währungsbetrag** Preisfindungsmethode für Materialien untestützt, die in einem Projekt verwendet werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
