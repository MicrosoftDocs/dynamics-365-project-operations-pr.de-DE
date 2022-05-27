---
title: Verkaufspreise für Vorkalkulationen und Istwerte auflösen
description: Diese Thema enthält Informationen darüber, wie Verkaufsraten für Vorkalkulationen und Istwerte aufgelöst werden.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 697d5e330fec1874e8cb59fb86dd688637860346
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578247"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Verkaufspreise für Vorkalkulationen und Istwerte auflösen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Wenn Verkaufspreise für Schätzungen und Istwerte in Dynamics 365 Project Operations aufgelöst werden, verwendet das System zunächst das Datum und die Währung des verknüpften Projektangebots oder -vertrags, um die Vertriebspreisliste aufzulösen. Nachdem die Verkaufspreisliste aufgelöst wurde, löst das System den Verkaufs- oder Fakturierungssatz auf.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Verkaufsraten in Istwert- und Vorkalkulationszeilen für Zeit auflösen

In Project Operations werden Vorkalkulationszeilen für die Zeit verwendet, um die Angebots- und Vertragszeilendetails für die Zeit und die Ressourcenzuweisungen für das Projekt anzugeben.

Nachdem eine Preisliste für Verkäufe aufgelöst wurde, führt das System die folgenden Schritte aus, um den Fakturierungssatz als Standard festzulegen.

1. Das System verwendet die Felder **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit, um diese mit den Rollenpreisen in der aufgelösten Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass sofort einsatzbereite Preisdimensionen für Fakturierungssätze verwendet werden. Wenn Sie die Preise basierend auf anderen Feldern anstatt zusätzlich zu **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** zu konfigurieren, ist das die Kombination, die verwendet wird, um eine übereinstimmende Rollenpreiszeile abzurufen.
2. Wenn das System eine Rollenpreiszeile findet, die eine Fakturierungsrate für die Feldkombination **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** aufweist, ist dieser Fakturierungssatz der Standardwert.
3. Wenn das System die Feldwerte **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** nicht zuordnen kann, erhält es die Rollenpreiszeilen mit einer übereinstimmenden Rolle, aber Nullwerte der **Ressourcenzuordnungseinheit**. Nachdem das System einen passenden Rollenpreisdatensatz gefunden hat, wird der Fakturierungssatz aus diesem Datensatz standardmäßig festgelegt. Diese Übereinstimmung setzt eine sofort einsatzbereite Konfiguration für die relative Priorität der **Rolle** im Vergleich zur **Ressourcenzuordnungseinheit** als Verkaufspreisdimension voraus.

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** konfiguriert haben, oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit übereinstimmenden Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die zuletzt kommenden Dimensionen enthalten.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Verkaufsraten in Istwert- und Vorkalkulationszeilen für Ausgaben auflösen

In Project Operations werden Vorkalkulationszeilen für Ausgaben verwendet, um die Angebots- und Vertragszeilendetails für Ausgaben und die Ausgabenvorkalkulationszeilen im Projekt anzugeben.

Nachdem eine Preisliste für Verkäufe aufgelöst wurde, führt das System die folgenden Schritte aus, um den Einheitsvertriebskostenpreis als Standard festzulegen.

1. Das System verwendet die Feldkombination **Kategorie** und **Einheit** in der Vorkalkulationszeile für Ausgaben, um diese mit den Kategoriepreiszeilen in der aufgelösten Preisliste abzugleichen.
2. Wenn das System eine Kategoriepreiszeile findet, die eine Verkaufsrate für die Feldkombination **Kategorie** und **Einheit** hat, dann ist die Verkaufsrate standardmäßig festgelegt.
3. Wenn das System eine übereinstimmende Kategoriepreiszeile findet, kann die Preismethode verwendet werden, um den Verkaufspreis als Standard festzulegen. Die folgende Tabelle zeigt das Standardverhalten von Ausgabenpreisen in Project Operations.

    | Kontext | Preisberechnungsmethode | Standardpreis |
    | --- | --- | --- |
    | Schätzung | Einzelpreis | Basierend auf der Kategoriepreiszeile |
    | &nbsp; | Zum Einstandswert | 0.00 |
    | &nbsp; | Aufschlag auf Kosten | 0.00 |
    | Tatsächl. | Einzelpreis | Basierend auf der Kategoriepreiszeile |
    | &nbsp; | Zum Einstandswert | Basierend auf den damit verbundenen tatsächlichen Kosten |
    | &nbsp; | Aufschlag auf Kosten | Durch Anwenden eines Aufschlags gemäß der Preiszeile der Kategorie auf den Stückkostensatz der zugehörigen tatsächlichen Kosten |

4. Wenn das System die Feldwerte **Kategorie** und **Einheit** nicht abgleichen kann, ist die Verkaufsrate standardmäßig null (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Lösen Sie die Verkaufsraten für tatsächliche und geschätzte Zeilen für Material auf

In Project Operations werden Schätzlinien für Material verwendet, um Angebots- und Vertragszeilendetails für Materialien und die Materialschätzungslinien für ein Projekt zu bezeichnen.

Nachdem eine Preisliste für Verkäufe aufgelöst wurde, führt das System die folgenden Schritte aus, um den Einheitsvertriebskostenpreis als Standard festzulegen.

1. Das System verwendet die **Produkt**- und **Einheit**-Feldkombination in der Schätzzeile für Material, das mit den Preislisten-Artikelzeilen in der aufgelösten Preisliste übereinstimmt.
2. Wenn das System eine Preislisten-Artikelzeile findet, die eine Verkaufsrate für die **Produkt**- und **Einheit**-Feldkombination hat und die Preismethode ist **Währungsbetrag**, wird der in der Preislistenzeile angegebene Verkaufspreis verwendet.
3. Wenn keine Übereinstimmung für **Produkt**- und **Einheit**-Werte gefunden wird, ist die Verkaufsrate standardmäßig null.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
