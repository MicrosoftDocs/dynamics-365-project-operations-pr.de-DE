---
title: Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176700"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Das Einrichten der Preise für Produktkatalogelemente in Dynamics 365 Project Operations erfolgt genau wie in Dynamics 365 Sales.

Da Produkte in Project Operations nicht vorkalkuliert oder für Projekte verwendet werden können, müssen für Projektangebote und Verträge keine Produktkatalogpreise in Projektpreislisten festgelegt werden.

Produktkatalogpreise sollten im Feld **Produktpreis** eines Angebots, Vertrags oder Kontos eingerichtet sein. Richten Sie für diese Entitäten keine Produktkatalogpreise in den Projektpreislisten ein. Projektpreislisten sind für Project Operations exklusiv. Es gibt eine anwendungsspezifische Geschäftslogik, die die Preislisten von einem Angebot in einen Vertrag kopiert. Das Ergebnis ist eine vertragsspezifische Projektpreisliste. Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird. Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen. Dies bedeutet, dass Produktpreislisten keinen Einfluss auf die Leistung des Angebotsgewinnprozesses haben.
