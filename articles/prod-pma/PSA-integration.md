---
title: Übersicht Project Service Automation
description: Dieses Thema bietet Informationen über die Dynamics 365 Project Service Automation zu Dynamics 365 Finance Integrationslösung.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076665"
---
# <a name="project-service-automation-overview"></a>Übersicht Project Service Automation

[!include[banner](../includes/banner.md)]

Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Dynamics 365 Finance und Dynamics 365 Project Service Automation über Common Data Service zu synchronisieren. Die Integrationsvorlage, die mit der Datenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss über Projektverträge, Projekte, Projekt-Vertragszeilen und Projekt-Vertragszeilen-Meilensteine, Projektaufgaben Ausgabetransaktionskategorien, Stundenschätzungen und Ausgabenschätzungen von Project Service Automation zu Finance.

> [!NOTE]
> - Wenn Sie Version 7.3.0 verwenden, müssen Sie die Wissensdatenbank 4074835 installieren. Sie können dann Festpreisprojekte integrieren.
> - Wenn Sie Version 7.3.0 verwenden und Gebührentransaktionen von Project Service Automation zu übertragen, müssen Sie die Wissensdatenbank 4345320 installieren, um diese Gebühren in die Projektrechnung aufzunehmen.
> - Wenn Sie Version 8.0 verwenden, können Sie Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren verwenden.
> - Wenn Sie Version 8.0.1 oder höher verwenden, können Sie die Istdaten synchronisieren.

Bevor Sie Project Service Automation Finance integrieren können, müssen Sie die Integrationsparameter von Project Service Automation konfigurieren. Weitere Informationen finden Sie unter [Integrationsparameter für Project Service Automation](PSA-parameters.md).

Diese Integrationslösung ermöglicht die direkte Synchronisation in den folgenden Szenarien:

- Verwalten Sie Projektverträge in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Erstellen Sie Projekte in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Verwalten Sie Projektvertragszeilen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Verwalten Sie Projektvertragszeilen-Meilensteine in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Verwalten Sie Projektaufträge in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Verwalten Sie Ausgabentransaktionskategorien in Finance und synchronisieren Sie sie direkt von Finance zu Project Service Automation.
- Erstellen Sie Projektstundenschätzungen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Erstellen Sie Projektausgabenschätzungen in Project Service Automation und synchronisieren Sie sie direkt von Project Service Automation mit Finance.
- Erstellen Sie Projektzeit, Ausgaben und tatsächliche Gebühren in Project Service Automation und erstellen Sie Projekttransaktionen im Project Service Automation-Integrationsjournal, damit sie in Finance gebucht werden können.

## <a name="data-synchronization"></a>Datensynchronisierung

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance als Teil der Integration synchronisiert werden.

> [!NOTE]
> Derzeit sind nicht alle Vorlagen verfügbar. Vorlagen werden veröffentlicht, sobald sie fertig sind.

[![Project Service Automation Integration mit Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemanforderungen für Finanzen

Um die Integrationslösung Project Service Automation zu Finance verwenden zu können, müssen Sie Enterprise Edition 7.3 mit Platform Update 12 oder höher installieren.

## <a name="system-requirements-for-project-service-automation"></a>Systemanforderungen für Project Service Automation

Um die Integrationslösung Project Service Automation zu Finance verwenden zu können, müssen Sie die folgenden Komponenten installieren:

- Dynamics 365 Project Service Automation Version 9.0.0.0 oder höher
- Aussicht auf Bargeldlösung für Dynamics 365 Sales, Version 1.14.0.0 (v14) oder höher
- Project Service Automation zu Finance-Lösung für Dynamics 365 Project Service Automation Version 1.0.0.0 oder höher

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installieren Sie Project Service Automation zu Finance Integrationslösung in Ihre Project Service Automation-Instanz

Laden Sie die Integrationslösung Project Service Automation zu Finance vom [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) herunter und befolgen Sie die Anweisungen, die der Lösung beiliegen.
