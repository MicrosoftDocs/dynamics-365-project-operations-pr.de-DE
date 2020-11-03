---
title: Kostensätze und Verkaufsraten für Katalogprodukte einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076591"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Kostensätze und Verkaufsraten für Katalogprodukte einrichten

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Das Einrichten der Preise für Produktkatalogelemente in Dynamics 365 Project Operations erfolgt genau wie in Dynamics 365 Sales.

Da Produkte in Project Operations nicht vorkalkuliert oder für Projekte verwendet werden können, müssen für Projektangebote und Verträge keine Produktkatalogpreise in Projektpreislisten festgelegt werden.

Produktkatalogpreise sollten im Feld **Produktpreis** eines Angebots, Vertrags oder Kontos eingerichtet sein. Richten Sie für diese Entitäten keine Produktkatalogpreise in den Projektpreislisten ein. Projektpreislisten sind für Project Operations exklusiv. Es gibt eine anwendungsspezifische Geschäftslogik, die die Preislisten von einem Angebot in einen Vertrag kopiert. Das Ergebnis ist eine vertragsspezifische Projektpreisliste. Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird. Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen. Dies bedeutet, dass Produktpreislisten keinen Einfluss auf die Leistung des Angebotsgewinnprozesses haben.
