---
title: Nachkalkulation produktbasierter Vertragszeilen – Lite
description: Dieses Thema enthält Informationen zum Erstellen.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177240"
---
# <a name="cost-product-based-contract-lines---lite"></a>Nachkalkulation produktbasierter Vertragszeilen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_


Produktbasierte Vertragszeilen in Dynamics 365 Project Operations umfassen das Feld **Einstandspreis**, in dem der Einstandspreis des Produkts für nachgelagerte Rentabilitätsberechnungen gespeichert wird.

Wenn eine produktbasierte Vertragszeile für ein Katalogprodukt erstellt wird, werden die Kosten für die produktbasierte Vertragszeile standardmäßig aus dem Feld **Standardkosten** im Produktkatalog berechnet. Das Feld **Standardkosten** im Produktkatalog wird in der Basiswährung der Organisation eingerichtet. Wenn die Stückkosten in der Vertragszeile standardmäßig sind, werden sie im Vertrag in die Verkaufswährung umgerechnet.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Einstandspreis bei einer produktbasierten Vertragszeile

Ein Einstandspreis in einer produktbasierten Vertragszeile ermöglicht unterschiedliche Kosten für jeden Kauf einer Einheit. Obwohl dies nicht immer erforderlich ist, gibt es bestimmte Szenarien, in denen die Kosten des Produkts vom Lieferanten für den Kunden abgezogen werden können. Betrachten Sie folgendes Szenario:

Fabrikam Robotics installiert Roboterarme an den Fließbändern der Adatum Corporation. Fabrikam bietet Installationsservices an, die Roboterarme werden jedoch von Trey Research bezogen. Wenn die Installation von Roboterarmen bei Adatum Corporation eine neue vertikale Branche für Trey Research eröffnet, könnten sie einen Sonderrabatt für dieses Geschäft gewähren. In diesem Fall erstellt Fabrikam eine produktbasierte Vertragszeile für Roboterarme und gibt für diesen Vertrag den Einzelpreis ein, der sich von den Standardkosten für Roboterarme von Trey Research unterscheidet.
