---
title: Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite
description: Dieses Thema enthält Informationen zum Einrichten von Kostensätzen und Verkaufsraten für Artikel in einem Produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996030"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Einrichten der Preise für Produktkatalogartikel in Dynamics 365 Project Operations ist dasselbe wie in Dynamics 365 Sales.

In Project Operations können Produkte nicht geschätzt oder für Projekte verwendet werden, sodass die Produktkatalogpreise nicht in den Projektpreislisten für Angebote und Verträge festgelegt werden müssen.

Verwenden Sie das **Produktpreis** Feld eines Angebots, Vertrags oder Kontos zum Einrichten der Produktkatalogpreise. Richten Sie keine Produktkatalogpreise in den Projektpreislisten ein. Projektpreislisten sind für Project Operations exklusiv. Die anwendungsspezifische Geschäftslogik kopiert die Preislisten aus einem Angebot in einen Vertrag. Das Ergebnis ist eine vertragsspezifische Projektpreisliste. Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird. Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen. Da kein Kopieren erforderlich ist, wird die Leistung des Angebotsprozesses nicht beeinträchtigt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]