---
title: Einstandspreise in Schätzungen und tatsächlichen Transaktionen auflösen – Lite
description: Diese Thema enthält Informationen darüber, wie Einstandspreise in Vorkalkulationen und Istwerten aufgelöst werden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176790"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Einstandspreise in Schätzungen und tatsächlichen Transaktionen auflösen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Um die Einstandspreise und die Einstandspreisliste für Vorkalkulationen und Istwerte zu beschließen, verwendet das System die Informationen in den Feldern **Datum**, **Währung** und **Vertragseinheit** des zugehörigen Projekts. Nachdem die Einstandspreisliste beschlossen wurden, schließt die Anwendung den Kostensatz ab.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Vorkalkulationszeilen für Zeit beziehen sich auf die Angebots- und Vertragszeilendetails für Zeit- und Ressourcenzuweisungen in einem Projekt.

Nachdem eine Einstandspreisliste aufgelöst wurde, verwendet das System die Felder **Rolle** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit, um diese mit Rollenpreiszeilen in der Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie sofort einsatzbereite Preisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen. Wenn die Anwendung eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle** und **Ressourceneinheit** findet, dann ist dies der Standardkostensatz. Wenn die Anwendung die Werte **Rolle** und **Ressourceneinheit** nicht zuordnen kann, erhält sie die Rollenpreiszeilen mit einer übereinstimmenden Rolle, aber Nullwerte der **Ressourcenzuordnungseinheit**. Nachdem ein übereinstimmender Rollenpreisdatensatz vorhanden ist, wird der Kostensatz standardmäßig aus diesem Datensatz verwendet. 

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die zuletzt kommenden Dimensionen enthalten.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Vorkalkulationszeilen für Ausgaben beziehen sich auf die Angebots- und Vertragszeilendetails für Ausgaben- und Ausgabenvorkalkulationszeilen in einem Projekt.

Nachdem eine Einstandspreisliste beschlossen wurde, verwendet das System eine Kombination der Felder **Kategorie** und **Einheit** in der Vorkalkulationszeile für eine Ausgabe, um Zeilen mit **Kategoriepreis** in der beschlossenen Preisliste abzugleichen. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt. Wenn das System die Werte **Kategorie** und **Einheit** nicht abgleichen kann oder es eine übereinstimmende Kategoriepreiszeile findet, die Preisberechnungsmethode jedoch nicht **Einzelpreis** lautet, ist der Kostensatz standardmäßig auf Null (0) festgelegt.
