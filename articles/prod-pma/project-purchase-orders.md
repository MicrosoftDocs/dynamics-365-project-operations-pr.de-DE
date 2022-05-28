---
title: Bestellungen für ein Projekt
description: Dieser Artikel beschreibt die verschiedenen Methoden, mit denen Sie Bestellungen für ein Projekt erstellen können. Die Methode, die Sie verwenden, hängt vom Zweck der Bestellung ab und wann die bestellen Artikel verbraucht werden und wann Artikel für ein Projekt belastet werden.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49ca1f9af715dcb1beb7932f7c484abc7b183dcd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684993"
---
# <a name="purchase-orders-for-a-project"></a>Bestellungen für ein Projekt

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die verschiedenen Methoden, mit denen Sie Bestellungen für ein Projekt erstellen können. Die Methode, die Sie verwenden, hängt vom Zweck der Bestellung ab und wann die bestellen Artikel verbraucht werden und wann Artikel für ein Projekt belastet werden.

### <a name="methods-for-creating-a-purchase-order"></a>Methoden zum Anlegen einer Bestellung

Mit einer der folgenden Methoden können Sie eine Bestellung in Projektmanagement und Buchhaltung anlegen. Der Zweck der Bestellung bestimmt, wann die Bestellung verbraucht wird und wann die Artikel für ein Projekt belastet werden.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Zweck</th>
<th>Verbrauch von Gegenständen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Eine Bestellung auf Grundlage eines Projekts direkt anlegen.</td>
<td>Verwenden Sie diese Methode, um Artikel von einem externen Lieferanten zum Verbrauch in einem Projekt zu kaufen. Sie können die Bestellung in zwei Arten erstellen:
<ul>
<li>Vom Projekt selber. In diesem Fall ist das Projekt bereits für die Bestellung definiert.</li>
<li>Durch Navigieren zur Projektbestellung. Sie müssen sowohl den Kreditor als auch das Projekt auswählen, für das Sie die Bestellung erstellen möchten.</li>
</ul></td>
<td>Artikel werden verbraucht, wenn die Lieferantenrechnung aktualisiert wird.</td>
</tr>
<tr class="even">
<td>Eine Bestellung auf Grundlage eines Auftrags anlegen</td>
<td>Verwenden Sie diese Methode, um Artikel zu kaufen, wenn Sie einen Kundenauftrag aus einem Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn der Kundenauftrag dem Kunden in Rechnung gestellt wird.</td>
</tr>
<tr class="odd">
<td>Erstellen Sie eine Bestellung aus einer Artikelanforderung.</td>
<td>Verwenden Sie diese Methode, um Artikel zu kaufen, wenn Sie eine Artikelanforderung aus einem Projekt erstellen.</td>
<td>Artikel werden verbraucht, wenn der Lieferschein der Artikelanforderung aktualisiert wird.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Wenn Sie die Lieferantenrechnung oder den Packzettel aktualisieren, werden Sie aufgefordert, den Packzettel für die Artikelanforderung zu aktualisieren.

Weitere Informationen finden Sie unter [Erhalten Sie Artikel auf Bestellung aus Artikelanforderung](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]