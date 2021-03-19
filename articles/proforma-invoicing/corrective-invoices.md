---
title: Korrigierte Rechnungen
description: Dieses Thema enthält Informationen zu korrigierten Rechnungen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287822"
---
# <a name="corrected-invoices"></a>Korrigierte Rechnungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Bestätigte Rechnungen können bearbeitet werden. Wenn Sie eine bestätigte Rechnung bearbeiten, wird eine neue korrigierte Rechnung erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese korrigierte Rechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.

Wenn Transaktionen keine Korrektur benötigen, können sie aus dem Korrekturrechnungsentwurf entfernt werden. Um eine Teilmenge umzukehren oder zurzuückgeben, können Sie das Feld Menge im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile stornier und zwei neue Ist-Werte werden erstellt:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]