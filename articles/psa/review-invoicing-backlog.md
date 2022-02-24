---
title: Rechnungsstellungsrückstand für Projekte und Projektverträge überprüfen
description: Dieses Thema enthält Informationen zur Überprüfung von Zeit-, Ausgaben- und Produktrückständen sowie dazu, wie man sie als bereit für die Rechnungsstellung markiert.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150487"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Rechnungsstellungsrückstand für Projekte und Projektverträge überprüfen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Wenn eine Transaktion bereit zur Erstellung und Verarbeitung einer Rechnung ist, sollte die Transaktion als **Bereit für die Rechnungsstellung** markiert werden. Dieses Thema beschreibt die Transaktionstypen, die erstellt werden können.

## <a name="review-the-time-and-material-billing-backlog"></a>Abrechnungsrückstand für Zeit und Material überprüfen

Wenn ein Zeit- oder Ausgabeneintrag übermittelt und für ein Projekt genehmigt wird, erstellt PSA einen Projekt-Istwert. Wenn die Kombination aus Projekt und Transaktionsklasse für ein Zeit- und Materialprojekt auf eine Vertragszeile abgebildet wird, werden zwei Istwerte erstellt, wenn der Eintrag genehmigt wird:

- Kosten-Istwert 
- Nicht fakturierter Umsatz-Istwert

Nicht fakturierte Umsatz-Istwerte stehen für den Abrechnungsrückstand und ihr Fakturierungsstatus muss auf **Bereit für die Rechnungsstellung** festgelegt werden. Wenn eine Projektrechnung erstellt wird, werden mit **Bereit für die Rechnungsstellung** markierte, nicht fakturierte Umsatz-Istwerte als Rechnungspositionsdetails in die Rechnung kopiert.

Um den Abrechnungsrückstand für Zeit und Materialien zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Abrechnungsrückstand für Zeit und Material überprüfen**. Wählen Sie alle nicht fakturierten Umsatz-Istwerte aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus. Der Fakturierungsstatus dieser Istwerte wird in **Bereit für die Rechnungsstellung** geändert.

![Abrechnungsrückstand für Zeit- und Material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Abrechnungsrückstand für das Produkt überprüfen

Wenn ein Projektvertrag über produktbasierte Vertragszeilen verfügt, werden diese Zeilen in PSA für die Rechnungsstellung berücksichtigt, wann immer eine Rechnung für den Projektvertrag erstellt wird. Jedes Produkt mit Vertragszeilen, die als **Bereit für die Rechnungsstellung** markiert sind, wird als Projektrechnungszeile in die Projektrechnung kopiert.

Um den Abrechnungsrückstand für Produkte zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Abrechnungsrückstand für Produkte**. Wählen Sie alle produktbasierten Vertragszeilen aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus. Der Fakturierungsstatus dieser Zeilen wird in **Bereit für die Rechnungsstellung** geändert.

![Abrechnungsrückstand für Produkte](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Abrechnungsmeilensteine für Festpreisverträge überprüfen

Jede Projektvertragszeile mit einer Festpreis-Fakturierungsmethode muss Vertragsmeilensteine definieren. Diese Vertragsmeilensteine können nur dann in Rechnung gestellt werden, wenn sie als **Bereit für die Rechnungsstellung** markiert sind. 

Um Abrechnungsmeilensteine zu überprüfen, navigieren Sie zu **Vertrieb** \> **Abrechnung** \> **Festpreismeilensteine**. Wählen Sie die Meilensteine aus, die abgerechnet werden können, und wählen Sie dann **Bereit für die Rechnungsstellung** aus. Der Fakturierungsstatus dieser Meilensteine wird in **Bereit für die Rechnungsstellung** geändert.

![Festpreismeilensteine](media/FPBacklog.png)
