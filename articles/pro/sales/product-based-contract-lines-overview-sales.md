---
title: Übersicht über produktbasierte Vertragszeilen
description: Dieses Thema enthält Informationen zu produktbasierten Vertragszeilen.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076451"
---
# <a name="product-based-contract-lines-overview"></a>Übersicht über produktbasierte Vertragszeilen

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Sie können produktbasierte Vertragszeilen in Dynamics 365 Project Operations erstellen. Bei Vertragszeilen kann es sich um manuell einzutragende Positionen oder Elemente aus dem Produktkatalog handeln.

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
