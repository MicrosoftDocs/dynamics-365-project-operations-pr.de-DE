---
title: Standardpreislisten
description: Dieses Thema bietet Informationen zu Standard-Verkaufs- und Einstandspreislisten in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd29a3fc9c873d46dd66a05ad100c7515177d6cd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130937"
---
# <a name="default-price-lists"></a>Standardpreislisten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

## <a name="sales-price-lists"></a>Verkaufspreislisten

Jedes Projektangebot und jeder Vertrag in Dynamics 365 Project Operations enthält eine Standardverkaufspreisliste. 

### <a name="price-list-default-on-project-quotes"></a>Standardpreislisten in Projektangeboten
Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für ein Projektangebot standardmäßig verwendet werden soll:

1. Das System überprüft die Preislisten, die den Projektpreislisten des Kontos beigefügt sind. 
2. Wenn dem Firmendatensatz Projektpreislisten beigefügt sind, überprüft das System die Verkaufspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektangebots übereinstimmen.
3. Als Nächstes überprüft das System die Datumseffektivität der Preislisten, die dem Datumsbereich des Projektangebots entsprechen. Speziell das Datum, an dem das Angebot erstellt wurde.
4. Wenn es mehrere Preislisten gibt, die für das Datum des Projektangebots gültig sind, werden alle Preislisten standardmäßig im Projektangebot verwendet.
5. Wenn für das Datum des Projektangebots keine Preislisten gültig sind, enthält das Projektangebot keine Standardprojektpreisliste. Im Projektangebot wird eine Warnmeldung angezeigt. In der Meldung heißt es, dass Istwerte und Vorkalkulationen im Projekt nicht bewertet werden, da keine Projektpreislisten angefügt sind.

### <a name="price-list-default-on-project-contracts"></a>Standardpreislisten in Projektverträgen 
Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für einen Projektvertrag standardmäßig verwendet werden soll:

1. Wenn der Vertrag aus einem Angebot erstellt wird, werden die Projektpreislisten auf dem Angebot separat kopiert und dem Projektvertrag beigefügt.
2. Wenn der Vertrag von Grund auf neu erstellt wird, überprüft das System die Preislisten, die den Projektpreislisten des Kontos beigefügt sind. Wenn dem Firmendatensatz keine Projektpreislisten beigefügt sind, überprüft das System die Verkaufspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektvertrags übereinstimmen.
4. Als Nächstes überprüft das System die Datumseffektivität der Preislisten, die dem Datumsbereich des Projektvertrags entsprechen. Speziell das Datum, an dem der Vertrag erstellt wurde.
5. Wenn es mehrere Preislisten gibt, die für das Datum des Vertrags gültig sind, werden alle Preislisten standardmäßig im Vertrag verwendet.
6. Wenn für das Datum des Vertrags keine Preislisten gültig sind, enthält der Vertrag keine Standardprojektpreislisten. Im Projektvertrag wird eine Warnmeldung angezeigt. In der Meldung heißt es, dass Istwerte und Vorkalkulationen im Projekt nicht bewertet werden, da keine Projektpreislisten angefügt sind.

## <a name="cost-price-lists"></a>Einstandspreislisten

Einstandspreislisten sind standardmäßig keine Entität in Project Operations. Die Ermittlung der Einstandspreise für die Projektkosten erfolgt immer im entsprechenden Moment. Das System führt den folgenden Vorgang aus, um zu bestimmen, welche Preisliste für Projektkosten verwendet werden soll:

1. Das System prüft zunächst die Preislisten, die der Vertragsorganisationseinheit des Projekts beigefügt sind.
2. Das System prüft dann die Datumseffektivität der Preislisten, die mit dem Datum der eingehenden Zeile der Vorkalkulation oder der tatsächlichen Transaktionen übereinstimmen. In dieser Situation bezieht sich *Vorkalkulationsposition* auf alle drei Vorkalkulationen in Project Operations:

    - Projektvorkalkulationsposition
    - Detailinformationen zur Angebotsposition
    - Vertragszeilendetail
  
3. Wenn mehrere Preislisten vorhanden sind, die für das Datum der eingehenden Vorkalkulation oder der tatsächlichen Transaktionen gültig sind, wird die zuletzt erstellte Preisliste ausgewählt.
4. Wenn der Vertragsorganisationseinheit des Projekts keine Projektpreislisten beigefügt sind, überprüft das System die Einstandspreislisten, die den Projektparametern zugeordnet sind und mit der Währung des Projektangebots übereinstimmen.
5. Das System prüft als Nächstes die Datumseffektivität der Preislisten, die mit dem Datum der Zeile der eingehenden Vorkalkulation oder der tatsächlichen Transaktionen übereinstimmen. 
6. Wenn mehrere Preislisten vorhanden sind, die für das Datum der eingehenden Vorkalkulation oder der tatsächlichen Transaktionen gültig sind, wird die zuletzt erstellte Preisliste ausgewählt.
7. Wenn den Projektparametern keine Einstandspreislisten zugeordnet sind, die der Währung und dem Datum des Inkrafttretens entsprechen, setzt das System den Kostensatz in der Zeile der eingehenden Vorkalkulation oder der tatsächlichen Transaktionen auf Null (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]