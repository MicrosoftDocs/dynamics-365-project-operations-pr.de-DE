---
title: Einstandspreise in Projektschätzungen und tatsächlichen Transaktionen auflösen
description: Dieses Thema enthält Informationen zum Auflösen von Kostenpreisen anhand von Projektschätzungen und Istdaten.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997560"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Einstandspreise in Projektschätzungen und tatsächlichen Transaktionen auflösen 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Um die Einstandspreise und die Einstandspreisliste für Vorkalkulationen und Istwerte zu beschließen, verwendet das System die Informationen in den Feldern **Datum**, **Währung** und **Vertragseinheit** des zugehörigen Projekts. Nachdem die Einstandspreisliste beschlossen wurden, schließt die Anwendung den Kostensatz ab.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Vorkalkulationszeilen für Zeit beziehen sich auf die Angebots- und Vertragszeilendetails für Zeit- und Ressourcenzuweisungen in einem Projekt.

Nachdem eine Selbstkostenpreisliste aufgelöst wurde, werden die Felder **Rolle** und **Ressourceneinheit** in der Schätzzeile für Zeit mit den Rollenpreislinien in der Preisliste abgeglichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie die Standardpreisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen. Wenn die Anwendung eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle** und **Ressourceneinheit** findet, dann ist dies der Standardkostensatz. Wenn die Anwendung die Werte **Rolle** und **Ressourceneinheit** nicht zuordnen kann, erhält sie die Rollenpreiszeilen mit einer übereinstimmenden Rolle, aber Nullwerte der **Ressourcenzuordnungseinheit**. Nachdem ein übereinstimmender Rollenpreisdatensatz vorhanden ist, wird der Kostensatz standardmäßig aus diesem Datensatz verwendet. 

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die zuletzt kommenden Dimensionen enthalten.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Vorkalkulationszeilen für Ausgaben beziehen sich auf die Angebots- und Vertragszeilendetails für Ausgaben- und Ausgabenvorkalkulationszeilen in einem Projekt.

Nachdem eine Kostenpreisliste aufgelöst wurde, verwendet das System eine Kombination aus **Kategorie** und **Einheit** Felder in der Kostenvorkalkulationszeile, die mit den Feldern **Kategorie Preis** Zeilen auf der aufgelösten Preisliste übereinstimmen. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt. Wenn das System nicht mit den Werten **Kategorie** und **Einheit** übereinstimmen kann oder wenn es in der Lage ist, eine passende Kategorie Preislinie zu finden, die Preismethode jedoch nicht **Preis pro Einheit** ist, ist der Kostensatz standardmäßig Null (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Auflösen von Verkaufsraten für tatsächliche und geschätzte Zeilen für Material

Schätzlinien für Material beziehen sich auf die Angebots- und Vertragszeilendetails für Materialien und die Materialschätzungslinien für ein Projekt.

Nachdem eine Kostenpreisliste aufgelöst wurde, verwendet das System eine Kombination aus **Produkt**- und **Einheit**-Feldern in der Schätzzeile für eine Materialschätzung, die mit **Preislistenelement**-Zeilen auf der aufgelösten Preisliste übereinstimmt. Wenn das System eine Produktpreiszeile findet, die einen Kostensatz für die **Produkt**- und **Einheit**-Feldkombination hat, wird der Standard-Kostensatz voreingestellt. Wenn das System keine Übereinstimmung für **Produkt**- und **Einheit**-Werte finden kann oder wenn es möglich ist, eine passende Preislisten-Artikelzeile zu finden, die Preismethode jedoch auf Standardkosten oder aktuellen Kosten basiert und keine für das Produkt definiert ist, werden die Stückkosten standardmäßig auf null gesetzt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
