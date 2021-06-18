---
title: Produktbasierte Angebotspositionen – Lite
description: Dieses Thema enthält Informationen zur Arbeit mit produktbasierten Angebotszeilen.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994450"
---
# <a name="product-based-quote-lines-overview---lite"></a>Produktbasierte Angebotspositionen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können produktbasierte Angebotspositionen in Dynamics 365 Project Operations erstellen. Bei Angebotspositionen kann es sich um manuell hinzugefügte Positionen oder Elemente aus dem Produktkatalog handeln.

## <a name="product-catalog"></a>Produktkatalog

Jedes Produkt im Produktkatalog weist eine Standardeinheit und eine Einheitengruppe auf. Falls mehrere Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst. 

Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für unterschiedliche Arten von Software. Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:

- Anzahl von Benutzern
- Eine Abonnementdauer in Monaten

Um diese Art von Katalog zu verwalten, erstellen sie eine Produktfamilie mit der Bezeichnung **Abonnement-Software** und fügen die Anzahl der Benutzer und die Abonnementdauer als Attribute hinzu. Im nächsten Schritt können Sie der **Abonnement-Software**-Produktfamilie einzelne Produkte hinzufügen.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Hinzufügen von Produktkatalogelementen zu einer Angebotsposition

Die Seiten **Projektangebot** und **Projektvertrag** weisen Abschnitte für projektbasierte Positionen und produktbasierte Positionen auf. Für produktbasierte Positionen enthält die Dropdownliste in der Angebotsposition oder in der Projektvertragsposition alle Produkte und Einheiten in der Produktpreisliste. Sie können auch Produkte hinzufügen, die nicht Teil der Produktpreisliste sind.

Darüber hinaus können Sie Produkte aus anderen Preislisten oder Produkte direkt aus dem Produktkatalog auswählen. Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen. Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.

Wenn eine Angebotsposition auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Angebotsposition überschreiben. Eine Angebotszeile im **Preisgestaltung**-Feld mit zwei verfügbaren Werten:

- **Preise überschreiben**
- **Standard verwenden**

Wenn Sie **Preise überschreiben** auswählen, ist der Standardpreis nicht festgelegt. Sie müssen stattdessen einen Preis für das Produkt in der Angebotsposition eingeben. Wenn Sie **Standard verwenden** auswählen, wird der Standardverkaufspreis verwendet und das Feld für die Bearbeitung gesperrt.

Es werden die Standardverkaufspreise in den produktbasierten Positionen in einem Angebot eingegeben. Das Feld **Preise** wird dann auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Angebotspositionen bearbeiten können. Dies ist eine Project Operations-spezifische Überschreibung des produktbasierten Zeilenverhaltens in Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]