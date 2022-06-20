---
title: Übersicht über produktbasierte Vertragszeilen – Lite
description: Dieser Artikel enthält Informationen über produktbasierte Vertragszeilen.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919875"
---
# <a name="product-based-contract-lines-overview---lite"></a>Übersicht über produktbasierte Vertragszeilen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können produktbasierte Vertragspositionen in Dynamics 365 Project Operations erstellen. Bei Vertragszeilen kann es sich um manuell einzutragende Positionen oder Elemente aus dem Produktkatalog handeln.

## <a name="product-catalog"></a>Produktkatalog

Die Produkte im Produktkatalog weisen eine Standardeinheit und eine Einheitengruppe auf. Falls verschiedene Produkte denselben Satz von Attributen enthalten, können Sie eine Produktfamilie erstellen, die auch diese Attribute umfasst. Alle Produkte in einer Produktfamilie erben denselben Satz von Attributen.

Beispielsweise verkauft ein Unternehmen Abonnementlizenzen für unterschiedliche Arten von Software. Die gesamte Abonnement-Software weist die folgenden zwei Attribute auf:

- Anzahl von Benutzern
- Abonnementdauer (in Monaten)

Um diese Art von Katalog zu verwalten, erstellen Sie eine Produktfamilie mit dem Namen **Software-Abonnement**. Fügen Sie der Produktfamilie die Attribute **Anzahl von Benutzern** und **Abonnementdauer** hinzu. Fügen Sie dann der Produktfamilie **Software-Abonnement** einzelne Produkte hinzu.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Einem Vertrag Produktkatalogelemente hinzufügen

Projektverträge weisen Abschnitte für zwei Arten von Positionen auf: projektbasierte Positionen und produktbasierte Positionen. Produktbasierte Zeilen enthalten alle Produkte und Einheiten in der Produktpreisliste des Vertrags. Produkte, die nicht Teil der Produktpreisliste des Vertrags sind, können hinzugefügt werden.

Sie können Produkte aus anderen Preislisten oder direkt aus dem Produktkatalog auswählen. Wenn Sie Produkte direkt aus dem Produktkatalog auswählen, wird die Standardpreisliste dieses Produktes verwendet, um den Verkaufspreis des Produktes zu bestimmen. Wenn eine Standardpreisliste nicht festgelegt ist, wird der Preis auf 0 (null) gesetzt.

Wenn eine Vertragszeile auf einem Produktkatalog basiert, können Sie den Verkaufspreis direkt in der Zeile überschreiben. Eine Vertragszeile besitzt das Feld **Preise** mit den zwei Werten:

- **Preise überschreiben**
- **Standard verwenden**

Wenn Sie das Feld **Preise** auf **Preise überschreiben** festlegen, wurde der Standardpreis nicht festgelegt. Geben Sie einen Preis für das Produkt in die Vertragszeile ein. Wenn Sie das Feld auf **Standard verwenden** festlegen, wird der Standardverkaufspreis verwendet und das Feld kann nicht bearbeitet werden.

Nachdem Sie Project Operations installiert haben, werden die Verkaufspreise in den produktbasierten Positionen in einem Vertrag eingegeben. Das Feld **Preise** ist auf **Preise überschreiben** festgelegt, damit Sie den Standardpreis in den Vertragszeilen bearbeiten können. Dies ist eine Project Operation-spezifische Überschreibung des produktbasierten Zeilenverhaltens in Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]