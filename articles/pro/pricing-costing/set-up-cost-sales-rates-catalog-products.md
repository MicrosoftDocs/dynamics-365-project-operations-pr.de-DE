---
title: Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite
description: In diesem Artikel erfahren Sie, wie Sie die Kalkulation und die Verkaufssätze für Elemente in einem Produktkatalog festlegen.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917391"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Einrichten der Preise für Produktkatalogartikel in Dynamics 365 Project Operations ist dasselbe wie in Dynamics 365 Sales.

In Project Operations können Produkte nicht geschätzt oder für Projekte verwendet werden, sodass die Produktkatalogpreise nicht in den Projektpreislisten für Angebote und Verträge festgelegt werden müssen.

Verwenden Sie das **Produktpreis** Feld eines Angebots, Vertrags oder Kontos zum Einrichten der Produktkatalogpreise. Richten Sie keine Produktkatalogpreise in den Projektpreislisten ein. Projektpreislisten sind für Project Operations exklusiv. Die anwendungsspezifische Geschäftslogik kopiert die Preislisten aus einem Angebot in einen Vertrag. Das Ergebnis ist eine vertragsspezifische Projektpreisliste. Der Kopiervorgang kann den Angebotsgewinn verzögern, wenn die Projektpreisliste im Angebot zu groß wird. Produktpreislisten werden nicht kopiert, um benutzerdefinierte Preislisten für Verträge zu erstellen. Da kein Kopieren erforderlich ist, wird die Leistung des Angebotsprozesses nicht beeinträchtigt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]