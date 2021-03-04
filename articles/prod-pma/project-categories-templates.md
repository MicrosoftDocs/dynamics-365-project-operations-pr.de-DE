---
title: Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projektkostenkategorien zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076663"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronisieren Sie Projektkostenkategorien zwischen Finance and Operations und Project Service Automation

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Ausgaben zwischen Microsoft Dynamics 365 Finance und Dynamics 365 Project Service Automation verwendet werden.

> [!NOTE]
> - Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperren sind in Version 8.0 verfügbar.
> - Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch KB 4131710 installieren.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Datenfluss für Project Service Automation and Finance

Die Integrationslösung für Project Service Automation und Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren. Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projektkosten-Transaktionskategorien zwischen Finance und Project Service Automation.

Wenn die Projektausgabenkategorien in Finance beherrscht werden, erfolgt der Integrationsfluss zunächst von Finance zu Project Service Automation. Die Integrations-IDs der Projektkostenkategorien werden dann durch Synchronisation von Project Service Automation zu Finance aktualisiert.

Wenn die Projektausgabenkategorien in Project Service Automation beherrscht werden, erfolgt der Integrationsfluss zunächst von Project Service Automation zu Finance. Die Projektkategorien müssen bereits vor der Synchronisierung über Project Service Automation in Finance konfiguriert worden sein. Dann synchronisieren Sie von Finance zurück zu Project Service Automation und synchronisieren Sie dann erneut von Project Service Automation zu Finance. Auf diese Weise stellen Sie sicher, dass die Kategorien verknüpft sind und keine Duplikate erstellt werden.

> [!NOTE]
> In der Regel werden die Projektkostenkategorien in Finance beherrscht. Wenn dies jedoch nicht der Fall ist oder wenn in Project Service Automation bereits Ausgabenkategorien erstellt wurden, müssen Sie zunächst mithilfe der Vorlage Projektausgaben-Transaktionskategorien (PSA zu Fin und Ops) synchronisieren. Synchronisieren Sie anschließend mithilfe der Vorlage für Projektkostentransaktionskategorien (Fin und Ops zu PSA). Anschließend sollten Sie die Synchronisierung von Project Service Automation zu Finance noch einmal ausführen.
>
> Wenn Sie zuerst über Project Service Automation synchronisieren, müssen die folgenden Anforderungen in Finance erfüllt sein, bevor die Synchronisierung ausgeführt wird:
>
> - Die gemeinsam genutzte Kategorie, die der in Project Service Automation eingerichteten Projektkategorie entspricht, muss vorhanden sein und für **Projekt** und **Kosten** aktiviert sein.
> - Für jede juristische Person im Finance, in die integriert werden muss, müssen die folgenden Projektkategorien vorhanden sein:
>
>     - **Projektkategorie** existiert. 
>     - **Verwendung in Kosten** ist aktiviert.
>     - **Aktiv im Journal** ist aktiviert.
>     - **Art der Transaktion** ist auf **Ausgaben** festgelegt.

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronisieren Sie Projektausgabenkategorien von Finance zu Project Service Automation

### <a name="template-and-task"></a>Vorlage und Aufgabe

Um auf die Vorlage zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Finance zu Project Service Automation zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (Fin und Ops zu PSA)
- **Name der Aufgabe im Projekt:** Kategorien mit PSA synchronisieren

### <a name="entity-set"></a>Entität festgelegt

| Finanzen                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsentität für Kategorien | Transaktionskategorien     |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert.

### <a name="power-query"></a>Power Query

Wenn Sie mit Project Service Automation synchronisieren, müssen Sie Microsoft Power Query für Excel verwenden, um die Abrechnungsart für die Transaktionskategorie festzulegen. Die Vorlage Projektkosten-Transaktionskategorien (Fin und Ops zu PSA) enthält eine Standardspalte und -zuordnung. Wenn Sie eine eigene Vorlage erstellen, müssen Sie eine bedingte Spalte in Power Query hinzufügen. Führen Sie die folgenden Schritte aus.

1. Klicken Sie auf den Pfeil, um die Zuordnung der Aufgabe Projektausgabenkategorien in der Vorlage Projektausgaben-Transaktionskategorien (Fin und Ops zu PSA) zu öffnen.
2. Klicken Sie auf die Verknüpfung **Erweiterte Abfrage und Filterung** , um Power Query zu öffnen.
2. Wählen Sie **Bedingte Spalte hinzufügen**.
3. Geben Sie einen Namen für die neue Spalte ein, wie **Abrechnungstyp**.
4. Geben Sie die folgende Bedingung ein: **Wenn CATEGORYID nicht gleich null ist, dann 19235001, andernfalls null**.
5. Klicken Sie in der Spalte auf **OK**.
6. Stellen Sie sicher, dass Sie diese neue Spalte auf der Zuordnungsseite zuordnen.

Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Finance zu Project Service Automation synchronisiert werden.

[![Projektausgabenkategorie zu Project Service Automation-Vorlagenzuordnung](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronisieren Sie Projektausgabenkategorien von Project Service Automation zu Finance

### <a name="template-and-task"></a>Vorlage und Aufgabe

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenkategorien von Project Service Automation zu Finance zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektausgabentransaktionskategorien (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:** Kategorien zu Fin Ops synchronisieren

### <a name="entity-set"></a>Entität festgelegt

| Project Service Automation | Finanzen                           |
|----------------------------|-----------------------------------|
| Transaktionskategorien     | Integrationsentität für Kategorien |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgabenkategorien werden in Finance verwaltet und als Transaktionskategorien in Project Service Automation synchronisiert. Die Synchronisation zurück zu Finance aktualisiert die Projektkostenkategorien in Finance mit der Integrations-ID von Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration.

> [!NOTE]
> Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Project Service Automation zu Finance-Vorlagenzuordnung](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]