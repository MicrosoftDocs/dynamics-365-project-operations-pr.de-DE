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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122387"
---
# <a name="corrected-invoices"></a>Korrigierte Rechnungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Bestätigte Rechnungen können bearbeitet werden. Wenn Sie eine bestätigte Rechnung bearbeiten, wird eine neue korrigierte Rechnung erstellt. Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese korrigierte Rechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.

Wenn Transaktionen keine Korrektur benötigen, können sie aus dem Korrekturrechnungsentwurf entfernt werden. Um eine Teilmenge umzukehren oder zurzuückgeben, können Sie das Feld Menge im Positionsdetail bearbeiten. Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge. Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.

Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt. Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt. Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile stornier und zwei neue Ist-Werte werden erstellt:

- Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.
- Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden. Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.
