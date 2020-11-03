---
title: Beschließen von Einstandspreisen für Vorkalkulationen und Istwerten
description: In diesem Thema wird erläutert, wie Einstandspreise für Vorkalkulationen und Istwerte beschlossen werden.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d3422ef2eacc1e0617e60d41b7ddbcefe44d5b90
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076386"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Beschließen von Einstandspreisen für Vorkalkulationen und Istwerten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Um die Einstandspreise und die Einstandspreisliste für Vorkalkulationen und Istwerte zu beschließen, verwendet das System die Informationen in den Feldern **Datum** , **Währung** und **Vertragseinheit** des zugehörigen Projekts. Nachdem die Einstandspreisliste beschlossen wurden, schließt die Anwendung den Kostensatz ab.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Vorkalkulationszeilen für Zeit beziehen sich auf die Angebots- und Vertragszeilendetails für Zeit- und Ressourcenzuweisungen in einem Projekt.

Nachdem eine Einstandspreisliste beschlossen wurde, verwendet das System die Felder **Rolle** , **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit, um diese mit den Rollenpreislisten in der Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie sofort einsatzbereite Preisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle** , **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen. Wenn die Anwendung eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle** , **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** besitzt, dann ist dies der Standardkostensatz. Wenn die Anwendung die Werte **Rolle** , **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** nicht zuordnen kann, erhält sie die Rollenpreiszeilen mit einer übereinstimmenden Rolle, aber Nullwerte der **Ressourcenzuordnungseinheit**. Nachdem ein übereinstimmender Rollenpreisdatensatz vorhanden ist, wird der Kostensatz standardmäßig aus diesem Datensatz verwendet. 

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle** , **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die zuletzt kommenden Dimensionen enthalten.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Vorkalkulationszeilen für Ausgaben beziehen sich auf die Angebots- und Vertragszeilendetails für Ausgaben- und Ausgabenvorkalkulationszeilen in einem Projekt.

Nachdem eine Einstandspreisliste beschlossen wurde, verwendet das System eine Kombination der Felder **Kategorie** und **Einheit** in der Vorkalkulationszeile für eine Ausgabe, um Zeilen mit **Kategoriepreis** in der beschlossenen Preisliste abzugleichen. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt. Wenn das System die Werte **Kategorie** und **Einheit** nicht abgleichen kann oder es eine übereinstimmende Kategoriepreiszeile findet, die Preisberechnungsmethode jedoch nicht **Einzelpreis** lautet, ist der Kostensatz standardmäßig auf Null (0) festgelegt.
