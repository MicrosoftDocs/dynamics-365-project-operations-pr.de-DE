---
title: Schlüsselbegriffe in der Fremdarbeit
description: In diesem Thema werden einige Schlüsselkonzepte erläutert, die für die Fremdarbeits-Auftragsvergabe in Microsoft Dynamics 365 Project Operations gelten.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578110"
---
# <a name="key-concepts-in-subcontracting"></a>Schlüsselbegriffe in der Fremdarbeit

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

In diesem Thema werden einige Schlüsselkonzepte erläutert, die Sie kennen sollten, bevor Sie mit der Verwendung der Fremdarbeitsfunktionen in Microsoft Dynamics 365 Project Operations beginnen.

## <a name="contracting-unit-on-the-subcontract"></a>Auftraggeber des Fremdarbeitsvertrags

Die Vertragsschlusseinheit repräsentiert die Abteilung oder Methode, die die Lieferung des möglichen Projekts besitzt. Die Vertragseinheit ist auch die Abteilung, die das Vertragsverhältnis mit dem Lieferanten eingeht.

## <a name="purchase-currency"></a>Einkaufswährung

In Project Operations ist die Einkaufswährung die Währung, in der der Fremdarbeitsauftrag erstellt wird. Es ist auch die Währung, in der die Fremdarbeitskosten für ein Projekt erfasst werden. Die Einkaufswährung kann von der Projektwährung und die Projektwährung wiederum von der Verkaufswährung abweichen.

## <a name="billing-methods-on-subcontract-lines"></a>Abrechnungsmethoden für Fremdarbeitspositionen

Für Projekte gibt es normalerweise Vertragsmodelle mit festen Gebühren und verbrauchsbasierte Modelle. Project Operations unterstützt diese Abrechnungsmethoden im Verkaufs- und Einkaufskontext. Für einen Einkauf funktionieren die Abrechnungsmethoden wie folgt:

- **Zeit und Material** – Wenn eine Fremdarbeitsposition die **Zeit und Material**-Abrechnungsmethode verwendet, wird der Zeitaufwand für das Projekt erfasst, da Fremdarbeitsvertragsarbeiter an diesem Projekt arbeiten und Zeit erfassen. Diese Kostenbuchungen von Fremdarbeitsvertragsarbeitern werden dann mit den Einzelposten auf Kreditorenrechnungen abgeglichen. In diesem Modell können Projektmanager, die Project Operations verwenden, Kreditorenrechnungsposten mit der aufgezeichneten und genehmigten Zeit von Fremdarbeitsvertragsarbeitern abgleichen und überprüfen. Nachdem die Überprüfung abgeschlossen ist, werden vorherige Ist-Kosten, die nach der Genehmigung erfasst wurden, storniert, und neue Ist-Kosten, die auf der Kreditorenrechnung basieren, werden für das Projekt erstellt.
- **Festpreis** – Bei diesem Vertragsmodell mit fester Gebühr basieren die Kreditorenrechnungen auf festen Meilensteinen. Allerdings können auch Fremdarbeitsressourcen Zeit melden. Die Zeit wird dann vom Projektleiter überprüft und freigegeben. Nach der Genehmigung erstellt Project Operations temporäre Ist-Kosten für das Projekt. Nachdem der Kreditor eine Rechnung für einen Meilenstein gesendet hat, kann der Projektmanager zuvor erfasste Ist-Kosten mit dem Meilenstein abgleichen. Wenn die Überprüfung abgeschlossen ist, werden die Ist-Kosten storniert und die meilensteinbasierten Kosten werden erfasst.

## <a name="project-price-lists-on-subcontracts"></a>Projektpreislisten in Fremdarbeitsverträgen

Projektpreislisten werden verwendet, um Einkaufspreise für Zeit, Ausgaben und andere projektbezogene Komponenten festzulegen. Es kann mehrere Preislisten geben, von denen jede einen eigenen datumswirksamen Fremdarbeitsvertrag in Project Operations haben kann. Project Operations unterstützt keine überlappende Datumseffektivität in Projektpreislisten für einen Fremdarbeitsvertrag.

## <a name="transaction-classes-on-subcontracts"></a>Transaktionsklassen auf Fremdarbeitsverträgen

Project Operations unterstützt vier Arten von Transaktionsklassen:

- Zeit
- Ausgaben
- Material
- Gebühr

Einkaufskosten können geschätzt und nur den Transaktionsklassen **Zeit**, **Kosten** und **Material** zugeordnet werden. **Gebühr** ist eine reine Umsatztransaktionsklasse und ist im Inhalt des Einkaufs nicht verfügbar.

## <a name="purchase-pricing-dimensions"></a>Einkaufspreisdimensionen

Mit Preisdimensionen können Sie entscheiden, welche Attribute für die Einrichtung des Einkaufspreises und für die Vorgabe von Zeitbuchungen verwendet werden. In Bezug auf den Einkauf unterstützt Project Operations nur feste Dimensionssätze für die Einrichtung und Vorgabe von Einkaufspreisen. Für die Einkaufspreiseinrichtung und -vorgabe für Fremdarbeitspositionen und Fremdarbeitszeitbuchungen lauten die Attribute **Rolle** und **Buchbare Ressource**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
