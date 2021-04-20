---
title: Finanzielle Vorkalkulationen für die Ressourcenzeit von Projekten
description: Dieses Thema enthält Informationen darüber, wie finanzielle Schätzungen für die Zeit berechnet werden.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91156c5cf79af8c66c12b84a6d2b17aa7fe09ed1
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701825"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Finanzielle Vorkalkulationen für die Ressourcenzeit von Projekten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Finanzielle Schätzungen für die Zeit werden auf der Grundlage von drei Faktoren berechnet: 

- Der Typ des generischen oder benannten Teammitglieds, das jeder Blattknotenaufgabe im Projektplan zugewiesen ist. 
- Die Art oder Komplexität der Arbeit.
- Die Verteilung des Aufwands für die Zuweisung der Ressource zur Aufgabe. 

Die ersten beiden Faktoren beeinflussen die Stückkosten oder den Rechnungssatz der Zuweisung einer Ressource. Die Stückkosten oder der Rechnungssatz einer Ressourcenzuweisung werden durch die Attribute der zugewiesenen Ressource bestimmt. Diese Attribute umfassen die Organisationseinheit, zu der die Ressource gehört, und die Standardrolle der Ressource. Sie können auch benutzerdefinierte Attribute hinzufügen, die für Ihr Unternehmen für die Ressource relevant sind, z. B. Standardtitel oder Erfahrungsstufe, und diese die Stückkosten oder den Rechnungssatz der Zuordnung beeinflussen lassen.
Zusätzlich zu den Attributen der Ressource können Arbeitsattribute, wie z. B. die Aufgabe, auch den Einheitsrechnungssatz oder den Kostensatz der Zuordnung beeinflussen. Wenn beispielsweise bestimmte Aufgaben komplexer sind, führt die Zuordnung der Ressource zu diesen bestimmten Aufgaben zu höheren Stückkosten oder Rechnungskosten als weniger komplexe Aufgaben.   

Der dritte Faktor gibt die Anzahl der Stunden mit dieser Rate an. In Fällen, in denen eine Aufgabe zwei Preisperioden abdeckt, ist es wahrscheinlich, dass der erste Teil der Ressourcenzuweisung für diese Aufgabe anders berechnet und bewertet wird als der zweite Teil der Aufgabe. Die Aufwandsvorkalkulation für jede Ressourcenzuweisung ist ein komplexer Wert, der mit der täglichen Aufwandsverteilung pro Tag gespeichert wird.

Ausführliche Anweisungen zum Einrichten benutzerdefinierter Arbeits- und Ressourcenattribute als Preis- und Kalkulationsdimensionen finden Sie unter [Preisdimensionen – Übersicht](../pricing-costing/pricing-dimensions-overview.md).

Die finanzielle Schätzung für jede Ressourcenzuweisung wird berechnet als **Rate/Stunde für die Zuordnung multipliziert mit der Anzahl der Stunden**.  Ähnlich wie bei der Aufwandsvorkalkulation ist die finanzielle Schätzung für Kosten und Einnahmen für jede Ressourcenzuweisung ein komplexer Wert, der mit der täglichen Verteilung des Geldbetrags pro Tag gespeichert wird. 

## <a name="summarizing-financial-estimates-for-time"></a>Zusammenfassung der finanziellen Schätzungen für die Zeit
Eine finanzielle Schätzung für die Zeit einer Blattknotenaufgabe ist die Summe der finanziellen Schätzungen für alle Ressourcenzuweisungen für diese Aufgabe.

Eine finanzielle Schätzung für die Zeit in einer Zusammenfassungs- oder übergeordnete Aufgabe ist die Summe der finanziellen Schätzungen aller untergeordneten Aufgaben. Dies sind die geschätzten Arbeitskosten für das Projekt. 

![Ressourcenvorkalkulationen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standardeinstandspreis und Kostenwährung

Der Standardkostenpreis ergibt sich aus den Preislisten, die der Vertragseinheit des Projekts beigefügt sind. Die Kostenwährung des Projekts ist immer die Währung der Vertragseinheit des Projekts. Bei einer Ressourcenzuweisung wird der finanzielle Kostenvoranschlag in der Kostenwährung des Projekts gespeichert. Manchmal unterscheidet sich die Währung, in der der Kostensatz in der Preisliste festgelegt ist, von der Kostenwährung des Projekts. In diesen Fällen konvertiert die Anwendung die Währung, in der der Selbstkostenpreis für die Währung des Projekts festgelegt wurde. Im Raster **Schätzungen** werden alle Kostenvoranschläge angezeigt und in der Kostenwährung des Projekts zusammengefasst. 

## <a name="default-bill-rate-and-sales-currency"></a>Standardrechnungsrate und Verkaufswährung

Der Standardverkaufspreis ergibt sich aus den Projektpreislisten, die dem zugehörigen Projektvertrag beigefügt sind, wenn das Geschäft gewonnen wurde, oder aus dem zugehörigen Projektangebot, wenn sich das Geschäft noch in der Vorverkaufsphase befindet. Die Vertriebswährung des Projekts ist immer die Währung des Projektangebots oder -vertrags. Bei einer Ressourcenzuweisung wird der finanzielle Vertriebsvoranschlag in der Vertriebswährung des Projekts gespeichert. Im Gegensatz zu den Kosten kann der in der Preisliste festgelegte Verkaufspreis niemals von der Verkaufswährung des Projekts abweichen. Es gibt kein Szenario, in dem eine Währungsumrechnung erforderlich ist. Im Raster **Schätzungen** werden alle Vertriebsvoranschläge angezeigt und in der Vertriebswährung des Projekts zusammengefasst. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
