---
title: Nachkalkulation produktbasierter Vertragszeilen – Lite
description: Dieser Artikel enthält Informationen über das Erstellen von
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922911"
---
# <a name="cost-product-based-contract-lines---lite"></a>Nachkalkulation produktbasierter Vertragszeilen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Produktbasierte Vertragszeilen in Dynamics 365 Project Operations umfassen das Feld **Selbstkostenpreis**, in dem der Selbstkostenpreis des Produkts für nachgelagerte Rentabilitätsberechnungen gespeichert wird.

Wenn für ein Katalogprodukt eine produktbasierte Vertragszeile erstellt wird, werden die Kosten für die Zeile standardmäßig aus dem Feld **Standardkosten** im Produktkatalog übernommen. Das Feld **Standardkosten** im Produktkatalog wird in der Basiswährung der Organisation eingerichtet. Wenn die Stückkosten in der Vertragszeile standardmäßig sind, werden sie im Vertrag in die Verkaufswährung umgerechnet.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Einstandspreis bei einer produktbasierten Vertragszeile

Ein Einstandspreis in einer produktbasierten Vertragszeile ermöglicht unterschiedliche Kosten für jeden Kauf einer Einheit. Obwohl dies nicht immer erforderlich ist, gibt es bestimmte Szenarien, in denen die Kosten des Produkts vom Lieferanten für den Kunden abgezogen werden können. Betrachten Sie folgendes Szenario:

Fabrikam Robotics installiert Roboterarme an den Fließbändern der Adatum Corporation. Fabrikam bietet Installationsservices an, die Roboterarme stammen jedoch von Trey Research. Wenn die Installation von Roboterarmen bei Adatum Corporation eine neue vertikale Branche für Trey Research eröffnet, könnten sie einen Sonderrabatt für dieses Geschäft gewähren. In diesem Fall erstellt Fabrikam eine produktbasierte Vertragslinie für Robotic Arms. Für diesen Vertrag werden Kosten pro Einheit eingegeben. Die Kosten unterscheiden sich von den Kosten für Roboterarme von Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]