---
title: Produktbasierte Angebotspositionen
description: Dieses Thema enthält Informationen zu produktbasierten Angebotspositionen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151252"
---
# <a name="product-based-quote-lines"></a>Produktbasierte Angebotspositionen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Sie können produktbasierte Angebotspositionen in Dynamics 365 Project Service Automation erstellen. Bei Angebotspositionen kann es sich um manuell einzutragende Positionen oder Elemente aus dem Produktkatalog handeln.

## <a name="product-catalog"></a>Produktkatalog

Die Produkte im Dynamics 365-Produktkatalog weisen eine Standardeinheit und eine Einheitengruppe auf. Falls verschiedene Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst. Alle Produkte in einer Produktfamilie erben denselben Satz von Attributen.

Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für eine Vielzahl von Software. Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:

- Anzahl der Benutzer 
- Abonnementdauer (in Monaten)

Eine gute Möglichkeit, diese Art von Katalog zu verwalten, besteht darin, eine Produktfamilie mit der Bezeichnung **Abonnement-Software** mit den Attributen **Anzahl der Benutzer** und **Abonnementdauer** zu erstellen. Sie können dann einzelne Produkte, z. B. **Dynamics 365 Sales** oder **Dynamics 365 Field Service**, der Produktfamilie **Abonnement-Software** hinzufügen.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Hinzufügen von Produktkatalogelementen zu einer Angebotsposition

Projektpositions- und Projektvertragsseiten weisen zwei Abschnitte für zwei Arten von Positionen auf: projektbasierte Positionen und produktbasierte Positionen. Bei produktbasierten Positionen wird Dynamics 365 verwendet, um einer Position Elemente aus einem Produktkatalog hinzuzufügen. Die Dropdownliste in der Angebotsposition oder in der Projektvertragsposition enthält alle Produkte und Einheiten in der Produktpreisliste, die dem Angebot oder dem Projektvertrag angefügt ist. Sie können auch Produkte hinzufügen, die nicht Teil der Produktpreisliste des Angebots sind.

Darüber hinaus können Sie Produkte aus anderen Preislisten oder Produkte direkt aus dem Produktkatalog auswählen. Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen. Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.

Wenn eine Angebotsposition auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Angebotsposition überschreiben. Beachten Sie, dass eine Angebotsposition in Dynamics 365 ein Feld mit der Bezeichnung **Preise** aufweist. Zwei Werte sind verfügbar:

- Preise überschreiben  
- Standard verwenden

Wenn Sie dieses Feld auf **Preise überschreiben** festlegen, setzt Dynamics 365 keinen Standardpreis fest. Sie müssen einen Preis für das Produkt in der Angebotsposition eingeben. Wenn Sie dieses Feld auf **Standard verwenden** festlegen, verwendet Dynamics 365 den Standardverkaufspreis und sperrt das Feld, um eine Bearbeitung zu vermeiden.

Nachdem Sie PSA installiert haben, werden die Verkaufspreise in den produktbasierten Positionen in einem Angebot eingegeben. Das Feld **Preise** wird dann auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Angebotspositionen bearbeiten können.

> ![Festlegen der Preisüberschreibung](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Mengenfaktoren für Produkte

PSA verwendet Mengenfaktoren, um den Verkauf von Abonnement-basierten Produkten zu unterstützen. Für Abonnement-basierte Produkte wird die Menge im Angebot oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.

Normalerweise wird der Preis der Abonnement-Software im Katalog als Preis pro Benutzer pro Monat gespeichert. Sie können jedoch auch andere Zeitbeschreibungen verwenden. Während des Vertriebsprozesses wird der Preis in der Angebotsposition in der Regel als Preis pro Benutzer pro Monat angegeben, der vom IT-Vertriebsmitarbeiter verhandelt und diskontiert wurde. Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate. Die Menge, die verwendet wird, um die Menge der Angebotszeile zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.

Um diese Art des Verkaufs zu unterstützen, hat PSA das Konzept der Mengenfaktoren eingeführt. Mengenfaktoren basieren auf den Produktattributen in Dynamics 365. Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, kennzeichnet PSA eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren.

PSA stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden. Wenn einem Produkt, dass für Mengenfaktoren konfiguriert wurde, eine Angebotsposition hinzugefügt wird, ist das Feld **Menge** in der Angebotsposition ein schreibgeschütztes Feld. Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, berechnet PSA die Menge der Angebotsposition.

Beispielsweise kann Dynamics 365 die folgenden Eigenschaften aufweisen: 

- **Anzahl der Benutzer** – Die Anzahl der Benutzer 
- **Anzahl der Monate** – Die Anzahl der Abonnementmonate
- **Produkt-SKU** 

Die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** können durch Bearbeitung der Produktposition als Mengenfaktoren gekennzeichnet werden. 

> ![Kennzeichnen von Anzahl der Benutzer und Anzahl der Monate als Mengenfaktoren](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]