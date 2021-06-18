---
title: Projektbasierte Verkaufschancenpositionen – Lite
description: Dieses Thema bietet Informationen zur Arbeit mit projektbasierten Verkaufschancenpositionen. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 90b1b078d51c2842f6406c4455188a4433820a77
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994405"
---
# <a name="project-based-opportunity-lines---lite"></a>Projektbasierte Verkaufschancenpositionen – Lite

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektbasierte Verkaufschancenpositionen sind nur in projektbasierten Verkaufschancen verfügbar. Bei projektbasierten Verkaufschancendatensätze wird der Feldwert **Typ** auf **Arbeitsbasiert** festgelegt.

Projektbasierte Verkaufschancenpositionen sind die Positionen, die dem Kunden über ein Projekt bereitgestellt werden. Ein Projekt kann jedoch nicht an eine projektbasierte Verkaufschancenposition gebunden werden. Projekte können mit Positionen ab der Phase des **Angebots** verknüpft werden, da die Verkaufschance in der Regel in einer frühen Phase im Lebenszyklus eines Geschäfts auftritt. Die Festlegung, wie viele Projekte verwendet werden, um die Arbeit für den Kunden bereitzustellen, ist eine Entscheidung, die später in der Verkaufsphase getroffen wird. Sie können die Phase der Verkaufschance nutzen, um die einzelnen Bereitstellungskomponenten für den Kunden zu identifizieren. Die Entscheidungen bezüglich der tatsächlichen Anzahl der Projekte, die zur Bereitstellung dieser Komponenten verwendet werden, können verschoben werden, bis weitere Informationen über die Arbeit selbst bekannt sind.

Nachfolgend sind die Felder in einer projektbasierten Verkaufschancenposition aufgeführt:

| **Feld** | **Ort** | **Beschreibung** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Produkttyp | Registerkarte „Allgemein“ (ausgeblendet) | Sie können eine der folgenden Optionen auswählen:</br>- Projektbasierter Service (nur vorhanden, wenn Dynamics 365 Project Operations installiert ist)</br>- Produkt (nur verfügbar, wenn Dynamics 365 Project Operations und Dynamics 365 Sales installiert sind) | Der Wert dieses Feldes wird auf **Projektbasierter Service** festgelegt, wenn Sie eine projektbasierte Verkaufschancenposition aus dem projektbasierten Positionsraster in der Verkaufschance erstellen. <br> Wenn Sie diesen Wert ändern oder überschreiben, wird die Projektfunktionalität für Ihre projektbasierten Positionen nicht aktiviert. |
| Verkaufschance | Registerkarte „Allgemein“ | Dieses Feld ist schreibgeschützt und verweist auf den übergeordneten Verkaufschancendatensatz, zu dem diese Position gehört. | Es gibt keine nachgelagerten Auswirkungen über dieses Feld. |
| Name des Dataflows | Registerkarte „Allgemein“ | Dies ist ein bearbeitbares Textfeld, mit dem dieser Position eine kurze Identität zugewiesen werden kann. | Dieser Wert wird in die Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Kundenbudget | Registerkarte „Allgemein“ | Dieses bearbeitbare Währungsfeld kann verwendet werden, um den Betrag zu verfolgen, den der Kunde bereit ist, für diese Position auszugeben. | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Fakturierungsmethode | Registerkarte „Allgemein“ | Dieses bearbeitbare Feld weist die folgenden Werte auf:</br>- Zeit und Material</br>- Festpreis | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. Nachdem die Angebotsposition erstellt wurde, ist das Feld gesperrt und kann nicht geändert werden. Weisen Sie diesen Feldwert so genau wie möglich zu. Wenn Sie den Wert dieses Felds in der Angebotsposition ändern müssen, löschen Sie die Angebotsposition und erstellen Sie sie neu. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]