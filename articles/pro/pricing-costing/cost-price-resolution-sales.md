---
title: Einstandspreise in Schätzungen und tatsächlichen Transaktionen auflösen – Lite
description: Diese Thema enthält Informationen darüber, wie Einstandspreise in Vorkalkulationen und Istwerten aufgelöst werden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764589"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Einstandspreise in Schätzungen und tatsächlichen Transaktionen auflösen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Um die Einstandspreise und die Einstandspreisliste für Vorkalkulationen und Istwerte zu beschließen, verwendet das System die Informationen in den Feldern **Datum**, **Währung** und **Vertragseinheit** des zugehörigen Projekts. Nachdem die Einstandspreisliste beschlossen wurden, schließt die Anwendung den Kostensatz ab.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Vorkalkulationszeilen für Zeit beziehen sich auf die Angebots- und Vertragszeilendetails für Zeit- und Ressourcenzuweisungen in einem Projekt.

Nachdem eine Selbstkostenpreisliste aufgelöst wurde, werden die Felder **Rolle** und **Ressourceneinheit** in der Schätzzeile für Zeit mit den Rollenpreislinien in der Preisliste abgeglichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie die Standardpreisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen. Wenn die Anwendung eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle** und **Ressourceneinheit** findet, dann ist dies der Standardkostensatz. Wenn die Anwendung die Werte **Rolle** und **Ressourceneinheit** nicht zuordnen kann, erhält sie die Rollenpreiszeilen mit einer übereinstimmenden Rolle, aber Nullwerte der **Ressourcenzuordnungseinheit**. Nachdem ein übereinstimmender Rollenpreisdatensatz vorhanden ist, wird der Kostensatz standardmäßig aus diesem Datensatz verwendet. 

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die zuletzt kommenden Dimensionen enthalten.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Vorkalkulationszeilen für Ausgaben beziehen sich auf die Angebots- und Vertragszeilendetails für Ausgaben- und Ausgabenvorkalkulationszeilen in einem Projekt.

Nachdem eine Kostenpreisliste aufgelöst wurde, verwendet das System eine Kombination aus **Kategorie** und **Einheit** Felder in der Kostenschätzungszeile, die mit den Feldern **Kategorie Preis** Zeilen auf der aufgelösten Preisliste übereinstimmen. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt. Wenn das System nicht mit den Werten **Kategorie** und **Einheit** übereinstimmen kann oder wenn es in der Lage ist, eine passende Kategorie Preislinie zu finden, die Preismethode jedoch nicht **Preis pro Einheit** ist, ist der Kostensatz standardmäßig Null (0).
