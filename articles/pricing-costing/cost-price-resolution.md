---
title: Beschließen von Einstandspreisen für Vorkalkulationen und Istwerten
description: Dieser Artikel informiert Sie darüber, wie Kalkulationen für Schätzungen und Istwerte aufgelöst werden.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af17712f0aef4fe3e6e758edd976cc377e90631d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919967"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Beschließen von Einstandspreisen für Vorkalkulationen und Istwerten

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Um die Einstandspreise und die Einstandspreisliste für Vorkalkulationen und Istwerte zu beschließen, verwendet das System die Informationen in den Feldern **Datum**, **Währung** und **Vertragseinheit** des zugehörigen Projekts. Nachdem die Einstandspreisliste beschlossen wurden, schließt die Anwendung den Kostensatz ab.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Zeit

Vorkalkulationszeilen für Zeit beziehen sich auf die Angebots- und Vertragszeilendetails für Zeit- und Ressourcenzuweisungen in einem Projekt.

Nachdem eine Einstandspreisliste beschlossen wurde, verwendet das System die Felder **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** in der Vorkalkulationszeile für Zeit, um diese mit den Rollenpreislisten in der Preisliste abzugleichen. Bei dieser Übereinstimmung wird davon ausgegangen, dass Sie sofort einsatzbereite Preisdimensionen für die Arbeitskosten verwenden. Wenn Sie das System so konfiguriert haben, dass es mit Feldern anstelle von **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** übereinstimmt, wird eine andere Kombination verwendet, um eine übereinstimmende Rollenpreiszeile abzurufen. Wenn die Anwendung eine Rollenpreiszeile findet, die einen Kostensatz für die Kombination **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** besitzt, dann ist dies der Standardkostensatz. Wenn die Anwendung nicht genau mit der Kombination der Werte **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** übereinstimmt, werden Rollenpreiszeilen mit einem übereinstimmenden Rollenwert abgerufen, für die jedoch Nullwerte für **Ressourcenzuordnungseinheit** und **Ressourcenzuordnungsunternehmen** festgelegt sind. Nachdem ein übereinstimmender Rollenpreisdatensatz mit übereinstimmendem Rollenpreiswert gefunden wurde, wird der Kostensatz standardmäßig aus diesem Datensatz verwendet. 

> [!NOTE]
> Wenn Sie eine andere Priorisierung von **Rolle**, **Ressourcenzuordnungsunternehmen** und **Ressourcenzuordnungseinheit** konfigurieren oder Sie andere Dimensionen mit einer höheren Priorität haben, ändert sich dieses Verhalten entsprechend. Das System ruft Rollenpreisdatensätze mit Werten ab, die mit jedem der Preisdimensionswerte in der Reihenfolge ihrer Priorität übereinstimmen, wobei Zeilen Nullwerte für die Dimensionen enthalten, die in der Prioritätsreihenfolge an letzter Stelle stehen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Beschließen von Kostensätzen in Istwert- und Vorkalkulationszeilen für Ausgaben

Vorkalkulationszeilen für Ausgaben beziehen sich auf die Angebots- und Vertragszeilendetails für Ausgaben- und Ausgabenvorkalkulationszeilen in einem Projekt.

Nachdem eine Einstandspreisliste beschlossen wurde, verwendet das System eine Kombination der Felder **Kategorie** und **Einheit** in der Vorkalkulationszeile für eine Ausgabe, um Zeilen mit **Kategoriepreis** in der beschlossenen Preisliste abzugleichen. Wenn das System eine Kategoriepreiszeile findet, die einen Kostensatz für die Kombination **Kategorie** und **Einheit** hat, ist der Kostensatz standardmäßig festgelegt. Wenn das System die Werte **Kategorie** und **Einheit** nicht abgleichen kann oder es eine übereinstimmende Kategoriepreiszeile findet, die Preisberechnungsmethode jedoch nicht **Einzelpreis** lautet, ist der Kostensatz standardmäßig auf Null (0) festgelegt.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Auflösen von Verkaufsraten für tatsächliche und geschätzte Zeilen für Material

Schätzlinien für Material beziehen sich auf die Angebots- und Vertragszeilendetails für Materialien und die Materialschätzungslinien für ein Projekt.

Nachdem eine Kostenpreisliste aufgelöst wurde, verwendet das System eine Kombination aus **Produkt**- und **Einheit**-Feldern in der Schätzzeile für eine Materialschätzung, die mit **Preislistenelement**-Zeilen auf der aufgelösten Preisliste übereinstimmt. Wenn das System eine Produktpreiszeile findet, die einen Kostensatz für die **Produkt**- und **Einheit**-Feldkombination hat, wird der Standard-Kostensatz voreingestellt. Wenn das System keine Übereinstimmung für **Produkt**- und **Einheit**-Werte findet, sind die Stückkosten standardmäßig null. Diese Standardeinstellung tritt auch auf, wenn eine übereinstimmende Preislisten-Artikelzeile vorhanden ist, die Preismethode jedoch auf Standardkosten oder aktuellen Kosten basiert, die nicht im Produkt definiert sind.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
