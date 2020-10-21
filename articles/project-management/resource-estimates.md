---
title: Ressourcenschätzungen
description: Dieses Thema enthält Informationen zum Berechnen der Ressourcenschätzungen in Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928566"
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
