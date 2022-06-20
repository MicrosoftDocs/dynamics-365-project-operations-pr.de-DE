---
title: Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations
description: Dieser Artikel beschreibt die Vorlage und die zugrundeliegende Aufgabe, die verwendet werden, um Projektaufgaben direkt von Microsoft Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931145"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt die Vorlage und die zugrundeliegende Aufgabe, die verwendet werden, um Projektaufgaben direkt von Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.

> [!NOTE]
> - Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch die Wissensdatenbank 4131710 installieren.
> - Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren. Die Integrationsvorlage, die mit der Datenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss über Projektkosten-Transaktionskategorien von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Vorlage und Aufgabe

Um auf die Vorlage zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projektaufgaben zwischen Project Service Automation und Finance zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektaufgaben (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:** Projektaufgaben

Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Projektverträge und Projekte synchronisieren.

## <a name="entity-set"></a>Entität festgelegt

| Project Service Automation | Finanzen                             |
|----------------------------|-------------------------------------|
| Projektaufgaben              | Integrationsentität für Projektaufgabe |

## <a name="entity-flow"></a>Entitätsfluss

Projektaufgaben werden in Project Service Automation verwaltet und als Projektaktivitäten mit Finance synchronisiert.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Mappingeinrichtung

Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Projektverträge und Projekte synchronisieren.

## <a name="power-query"></a>Power Query

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn diese Bedingung erfüllt ist:

- Sie haben ressourcenspezifische Datensätze in einer Projektaufgabe.

Wenn Sie Power Query verwenden möchten, folgen Sie dieser Richtlinie:

- Die Vorlage Projektaufgaben (PSA zu Fin und Ops) verfügt über einen Standardfilter, der ressourcenspezifische Datensätze von einer Projektaufgabe ausschließt, indem der Filter im **IsLineTask** auf **Falsch** gesetzt wird. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]