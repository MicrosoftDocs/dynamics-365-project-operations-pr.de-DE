---
title: Ressourcenschätzungen
description: Dieses Thema enthält Informationen zum Berechnen der Ressourcenschätzungen in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286517"
---
# <a name="resource-estimates"></a>Ressourcenschätzungen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ressourcenschätzungen basieren auf zeitlich abgestuftem Aufwand, der in der Projektstrukturplan zusammen mit den geltenden Preisdimensionen definiert ist. In der Regel lautet die Berechnung **Rate/Stunde für jede Rolle x Stunden.** Der zeitlich abgestufte Aufwand für jede Ressource wird im Ressourcenzuweisungsdatensatz gespeichert. Die Preisgestaltung wird in einer vordefinierten Preisliste gespeichert. Die Umrechnung der Einheiten erfolgt auf der Grundlage der geltenden Preisliste.

![Ressourcenschätzungen](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Standardeinstandspreis und Kostenwährung

Die Einstandspreise werden standardmäßig von der Organisationseinheit übernommen.

## <a name="default-bill-rate-and-sales-currency"></a>Standardrechnungsrate und Verkaufswährung

Verkaufspreise werden einmal pro Geschäft angewendet. Die Hierarchie für die Standardeinstellung der Verkaufspreisliste lautet wie folgt:

1. Organisation
2. Kunde
3. Angebot/Vertrag


[!INCLUDE[footer-include](../includes/footer-banner.md)]