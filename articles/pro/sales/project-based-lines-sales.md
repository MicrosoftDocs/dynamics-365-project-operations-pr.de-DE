---
title: Projektverkaufschancenzeilen
description: Dieser Artikel enthält Informationen zu projektbasierten Verkaufschancen. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e4f67bd9b7d51559e2942e9005b8f5f9187b1f78
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824954"
---
# <a name="project-opportunity-lines"></a>Projektverkaufschancenzeilen 

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Projektverkaufschancenpositionen sind nur in projektbasierten Verkaufschancen verfügbar. Bei projektbasierten Verkaufschancendatensätze wird der Feldwert **Typ** auf **Arbeitsbasiert** festgelegt.

Projekverkaufschancenpositionen sind die Positionen, die dem Kunden über ein Projekt bereitgestellt werden. Ein Projekt kann jedoch nicht an eine projektbasierte Verkaufschancenposition gebunden werden. Projekte können mit Positionen ab der Phase des **Angebots** verknüpft werden, da die Verkaufschance in der Regel in einer frühen Phase im Lebenszyklus eines Geschäfts auftritt. Die Festlegung, wie viele Projekte verwendet werden, um die Arbeit für den Kunden bereitzustellen, ist eine Entscheidung, die später in der Verkaufsphase getroffen wird. Sie können die Phase der Verkaufschance nutzen, um die einzelnen Bereitstellungskomponenten für den Kunden zu identifizieren. Die Entscheidungen bezüglich der tatsächlichen Anzahl der Projekte, die zur Bereitstellung dieser Komponenten verwendet werden, können verschoben werden, bis weitere Informationen über die Arbeit selbst bekannt sind.

Nachfolgend sind die Felder in einer Projektverkaufschancenposition aufgeführt:

| **Feld** | **Position** | **Beschreibung des Dataflows** | **Downstream-Auswirkungen** |
| --- | --- | --- | --- |
| Produkttyp | Registerkarte „Allgemein“ (ausgeblendet) | Sie können eine der folgenden Optionen auswählen:</br>- Projektbasierter Service (nur vorhanden, wenn Dynamics 365 Project Operations installiert ist)</br>- Produkt (nur verfügbar, wenn Dynamics 365 Project Operations und Dynamics 365 Sales installiert sind) | Der Wert dieses Feldes wird auf **Projektbasierter Service** festgelegt, wenn Sie eine projektbasierte Verkaufschancenposition aus dem projektbasierten Positionsraster in der Verkaufschance erstellen. <br> Wenn Sie diesen Wert ändern oder überschreiben, wird die Projektfunktionalität für Ihre projektbasierten Positionen nicht aktiviert. |
| Verkaufschance | Registerkarte „Allgemein“ | Dieses Feld ist schreibgeschützt und verweist auf den übergeordneten Verkaufschancendatensatz, zu dem diese Position gehört. | Es gibt keine nachgelagerten Auswirkungen über dieses Feld. |
| Name des Dataflows | Registerkarte „Allgemein“ | Dies ist ein bearbeitbares Textfeld, mit dem dieser Position eine kurze Identität zugewiesen werden kann. | Dieser Wert wird in die Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Kundenbudget | Registerkarte „Allgemein“ | Dieses bearbeitbare Währungsfeld kann verwendet werden, um den Betrag zu verfolgen, den der Kunde bereit ist, für diese Position auszugeben. | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. |
| Fakturierungsmethode | Registerkarte „Allgemein“ | Dieses bearbeitbare Feld weist die folgenden Werte auf:</br>- Zeit und Material</br>- Festpreis | Dieser Wert wird in das entsprechende Feld in der Angebotsposition übertragen, wenn Sie aus dieser Verkaufschance ein Angebot erstellen. Nachdem die Angebotsposition erstellt wurde, ist das Feld gesperrt und kann nicht geändert werden. Weisen Sie diesen Feldwert so genau wie möglich zu. Wenn Sie den Wert dieses Felds in der Angebotsposition ändern müssen, löschen Sie die Angebotsposition und erstellen Sie sie neu. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
