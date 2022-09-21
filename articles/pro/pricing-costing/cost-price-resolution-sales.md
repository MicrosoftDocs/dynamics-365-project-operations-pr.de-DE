---
title: Kostenraten für Projektschätzungen und tatsächliche Transaktionen bestimmen
description: Dieser Artikel informiert Sie darüber, wie Kalkulationen für Projektschätzungen und Istwerte bestimmt werden.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475230"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Kostenraten für Projektschätzungen und tatsächliche Transaktionen bestimmen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Um den Kostensatz für Schätzungen und Istwerte in Microsoft Dynamics 365 Project Operations zu bestimmen, verwendet das System zunächst das Datum und die Währung des verknüpften Projektangebots oder -vertrags, um die Einstandspreisliste aufzulösen. Im eigentlichen Kontext verwendet das System das Feld **Transaktionsdatum**, um zu bestimmen, welche Preisliste anwendbar ist. Der Wert **Transaktionsdatum** der eingehenden oder tatsächlichen Schätzung wird mit dem Wert **Effektiver Start (zeitzonenunabhängig)** und dem Wert **Effektives Ende (zeitzonenunabhängig)** auf der Preisliste verglichen. Nachdem die Einstandspreisliste besstimmt wurde, bestimmt das System  den Kostensatz. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Bestimmen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Geschätzer Kontext für **Zeit** bezieht sich auf:

- Angebotszeilendetails für **Zeit**.
- Vertragsszeilendetails für **Zeit**.
- Ressourcenzuweisung für ein Projekt.

Tatsächlicher Kontext für **Zeit** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Zeit**.
- Journalzeilen, die erstellt werden, wenn ein Zeiteintrag übermittelt wird.

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Kostenssatz als Standard festzulegen.

1. Das System stimmt die Felder **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit ab, um diese mit den Rollenpreisen in der aufgelösten Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie die Standardpreisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen.
1. Wenn das System eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle** und **Ressourcenzuordnungseinheit** und Ressourcenzuordnungseinheit besitzt, dann ist dies der Standardkostensatz.
1. Wenn das System die Feldwerte **Rolle** und **Ressourcenzuordnungseinheit** nicht zuordnen kann, ruft es die Rollenpreiszeilen mit übereinstimmenden Werten für das Feld **Rolle** aber Nullwerte für das Feld **Ressourceneinheit** ab. Nachdem das System einen passenden Rollenpreisdatensatz gefunden hat, wird der Kostensatz aus diesem Datensatz standardmäßig als Fakturierungssatz festgelegt.

> [!NOTE]
> Wenn Sie eine andere Priorisierung der Felder **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die jedem Preisdimensionswert in der Reihenfolge ihrer Priorität entsprechen. Zeilen mit Nullwerten für diese Dimensionen kommen zuletzt.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Bestimmen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Geschätzer Kontext für **Ausgaben** bezieht sich auf:

- Angebotszeilendetails für **Ausgaben**.
- Vertragszeilendetails für **Ausgaben**.
- Ausgabenschätzungen für ein Projekt.

Tatächlicher für **Ausgaben** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Ausgabe**.
- Journalzeilen, die erstellt werden, wenn ein Ausgabeneintrag übermittelt wird.

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Kostenssatz als Standard festzulegen.

1. Das System stimmt die Felder **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit ab, um diese mit den Kategorienpreisen in der aufgelösten Preisliste abzugleichen.
1. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt.
1. Wenn das System die Feldwerte **Kategorie** und **Einheit** nicht abgleichen kann, ist der Preis standardmäßig **0** (Null).
1. Im Schätzungskontext, wenn das System keine übereinstimmende Kategoriepreiszeile finden kann, aber die Preisberechnungsmethode nicht **Preis pro Einheit** ist wird der Kostensatz auf **0** standardmäßig auf Null festgelegt.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Bestimmen von Kostensätzen für tatsächliche und geschätzte Zeilen für Material

Geschätzer Kontext für **Material** bezieht sich auf:

- Angebotszeilendetails für **Material**.
- Vertragszeilendetails für **Material**.
- Materialschätzungen für ein Projekt.

Tatächlicherkontext für **Material** bezieht sich auf:

- Erfassungs- und Korrekturjournalzeilen für **Material**.
- Journalzeilen, die erstellt werden, wenn ein Materialnutzungsprotokoll übermittelt wird.

Nachdem eine Preisliste für Verkäufe bestimmt wurde, führt das System die folgenden Schritte aus, um den Kostenssatz als Standard festzulegen.

1. Das System verwendet die Kombination von Feldern **Produkt** und **Einheit** im Schätzungs- oder Istkontekxt **Material** in Preislistenelementzeilen auf der Preisliste.
1. Wenn das System eine Preislistenelementzeile hat, die einen Kostensatz für die Kombination **Produkt** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt.
1. Wenn das System keine Übereinstimmung für die Werte **Produkt** und **Einheit** hat, ist die Kosteneinheit standardmäßig auf **0** (Null) festgelegt.
1. Im Schätzungs- oder Istkontext, wenn das System kein übereinstimmendes Preislistenelement finden kann, aber die Preisberechnungsmethode nicht **Währungsbetrag** ist, werden die Einheitskosten standardmäßig auf **0** Null festgelegt. Dieses Verhalten tritt auf, weil Project Operations nur die **Währungsbetrag** Preisfindungsmethode für Materialien untestützt, die in einem Projekt verwendet werden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
