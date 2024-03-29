---
title: Synchronisieren von Projektvorkalkulationen direkt aus Project Service Automation für Finanz- und Betriebs-Apps
description: Dieser Artikel beschreibt die Vorlagen und zugrundeliegenden Aufgaben, die verwendet werden, um Projektstundenschätzungen und Projektkostenschätzungen direkt von Microsoft Dynamics 365 Project Service Automation zu Dynamics 365 Finance zu synchronisieren.
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
ms.openlocfilehash: 2a71a2a7ca0c9179ddd5667364d8b5c9e413b917
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029804"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektvorkalkulationen direkt aus Project Service Automation für Finanz- und Betriebs-Apps

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt die Vorlagen und zugrundeliegenden Aufgaben, die verwendet werden, um Projektstunden- und Projektkostenvoranschläge direkt von Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.

> [!NOTE]
> - Projektaufgabenintegration, Kostentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Funktionssperre sind in Version 8.0 verfügbar.
> - Die tatsächliche Integration ist in Version 8.0.1 oder höher verfügbar.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren. Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projektstundenschätzungen und Projektausgabenschätzungen von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projektstundenschätzungen

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Um auf die verfügbarem Vorlagen zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projektstundenschätzungen von Project Service Automation zu Finance zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektstundenschätzungen (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:**

    - Transaktionsbeziehungen
    - Ausgabenschätzungen

### <a name="entity-set"></a>Entität festgelegt

| Project Service Automation | Finanzen                                       |
|----------------------------|-----------------------------------------------|
| Projektaufgaben              | Integrationseinheit für Projektstundenschätzungen |

### <a name="entity-flow"></a>Entitätsfluss

Projektstundenschätzungen werden in Project Service Automation verwaltet und als Projektstundenprognosen mit Finance synchronisiert.

### <a name="prerequisites"></a>Voraussetzungen

Bevor eine Synchronisierung der Projektstundenschätzungen erfolgen kann, müssen Sie Projekte, Projektaufgaben und Transaktionskategorien für Projektkosten synchronisieren.

### <a name="power-query"></a>Power Query

In der Vorlage für Projektstundenvorkalkulationen müssen Sie Microsoft Power Query für Excel verwenden, um diese Aufgaben abzuschließen:

- Legen Sie die Standard-ID des Prognosemodells fest, die verwendet wird, wenn die Integration neue Stundenprognosen erstellt.
- Filtern Sie alle ressourcenspezifischen Datensätze in der Aufgabe heraus, bei denen die Integration in Stundenvorhersagen fehlschlägt.
- Filtern Sie alle leeren Transaktionskategoriezeilen heraus. Wenn Sie diese Aufgabe nicht ausführen, kann dies zu falschen Stundenvorhersagen führen.

#### <a name="set-the-default-forecast-model-id"></a>Legen Sie die Standardmdell-ID fest

Um die Standard-Prognosemodell-ID in der Vorlage zu aktualisieren, klicken Sie auf den Pfeil **Zuordnen** und öffnen das Mapping. Dann wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**.

- Wenn Sie die Standardvorlage für Projektstundenschätzungen (PSA zu Fin und Ops) verwenden, wählen Sie die Option **Eingefügter Zustand** aud der Liste **Angewandte Schritte** aus. In dem Eintrag **Funktion** ersetzen Sie **O\_Prognose** mit dem Namen der Prognosemodell-ID, die für die Integration verwendet werden soll. Die Standardvorlage enthält eine Prognosemodell-ID aus den Demo-Daten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie in Power Query die Option **Bedingte Spalte hinzufügen** aus, und geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **ModelID**. Geben Sie die Bedingung für die Spalte ein, wobei, wenn Projektaufgabe nicht null ist, dann \<enter the forecast model ID\>; andernfalls null

#### <a name="filter-out-resource-specific-records"></a>Filtern Sie ressourcenspezifische Datensätze heraus

Die Vorlage Projektstundenschätzungen (PSA zu Fin und Ops) verfügt über einen Standardfilter, mit dem alle ressourcenspezifischen Datensätze entfernt werden. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus, um die Spalte **msdyn\_islinetask** zu filtern, um nur **Fals** Datensätze einzuschließen.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtern Sie alle leeren Transaktionskategoriezeilen heraus

Sie müssen einen Filter hinzufügen, um alle Zeilen mit leeren Transaktionskategorien zu entfernen. Diese Aufgabe ist erforderlich, unabhängig davon, ob Sie die Standardvorlage verwenden oder eine eigene Vorlage erstellen. Dieser Filter entfernt alle Zusammenfassungszeilen aus Project Service Automation, die dazu führen können, dass die Stundenprognosen in Finance falsch sind. Wählen Sie den Link **Erweiterte Abfrage und Filterung** zum Herausfiltern von Nulldatensätzen in der Spalte **msdyn\_Transaktionskategorie\_Wert**.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt ein Beispiel für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Zuordnung von Vorlagenaufgaben in der Datenintegration.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projektausgabenschätzungen

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekausgabenschätzungen von Project Service Automation zu Finance zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projektausgabenschätzungen (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:**

    - Transaktionsbeziehungen 
    - Ausgabenschätzungen

### <a name="entity-set"></a>Entität festgelegt

| Project Service Automation | Finanzen                                                  |
|----------------------------|----------------------------------------------------------|
| Transaktionsverbindungen    | Integrationsentität für die Projekttransaktion Beziehungen |
| Vorkalkulationszeilen             | Integrationseinheit für Projektausgabenschätzungen         |

### <a name="entity-flow"></a>Entitätsfluss

Projektausgabenschätzungen werden in Project Service Automation verwaltet und als Projektausgabenprognosen mit Finance synchronisiert.

### <a name="prerequisites"></a>Voraussetzungen

Bevor eine Synchronisierung der Projektausgabenschätzungen erfolgen kann, müssen Sie Projekte, Projektaufgaben und Transaktionskategorien für Projektkosten synchronisieren.

### <a name="power-query"></a>Power Query

In der Vorlage für Projektausgabenvorkalkulationen müssen Sie Power Query verwenden, um die folgenden Aufgaben abzuschließen:

- Filtern, um nur Ausgabenschätzungszeilendatensätze einzuschließen.
- Legen Sie die Standard-ID des Prognosemodells fest, die verwendet wird, wenn die Integration neue Stundenprognosen erstellt.
- Transformieren Sie die Abrechnungsarten.
- Transformieren Sie die Transaktionsarten.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtern, um nur Ausgabenschätzungszeilen einzuschließen

Die Vorlage Projektkostenschätzungen (PSA zu Fin und Ops) verfügt über einen Standardfilter, der nur Ausgabenzeilen in die Integration einbezieht. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen. Wählen Sie die Aufgabe **Transaktionsbeziehungen** und klicken Sie dann auf den Pfeil **Zuordnen**, um das Mapping zu öffnen. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**. Filtern Sie die Spalte **msdyn\_Transaktionstyp1**, sodass sie nur **msdyn\_Schätzlinie** enthält.

#### <a name="set-the-default-forecast-model-id"></a>Legen Sie die Standardmdell-ID fest

Um die Standard-Prognosemodell-ID in der Vorlage zu aktualisieren, wählen Sie die Aufgabe **Ausgabenschhätzung** und klicken auf den Pfeil **Zuordnen** und öffnen das Mapping. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung**.

- Wenn Sie die Vorlage der standardmäßigen Projektausgaben-Ist-Werte (PSA zu Fin and Ops) verwenden, wählen Sie in Power Query die erste **Eingefügte Bedingung** aus dem Abschnitt **Angewendete Schritte** aus. In dem Eintrag **Funktion** ersetzen Sie **O\_Prognose** mit dem Namen der Prognosemodell-ID, die für die Integration verwendet werden soll. Die Standardvorlage enthält eine Prognosemodell-ID aus den Demo-Daten.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie diese Spalte hinzufügen. Wählen Sie in Power Query die Option **Bedingte Spalte hinzufügen** aus, und geben Sie einen Namen für die neue Spalte ein, wie beispielsweise **ModelID**. Geben Sie die Bedingung für die Spalte ein, wobei, wenn Vorkakulationspositions-ID nicht null ist, dann \<enter the forecast model ID\>; andernfalls null.

#### <a name="transform-the-billing-types"></a>Transformieren Sie die Abrechnungsarten

Die Vorlage für Projektkostenschätzungen (PSA zu Fin und Ops) enthält eine bedingte Spalte, mit der die Abrechnungsarten transformiert werden, die während der Integration von Project Service Automation empfangen werden. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen bedingte Spalte hinzufügen. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus und wählen dann **Bedingte Spalte hinzufügen**. Geben Sie einen Namen für die neue Spalte ein, wie **Abrechnungstyp**. Geben Sie die folgende Bedingung ein:

Wenn **msdyn\_Abrechnungstyp** = 192350000 ist, dann **Nicht belastbar**  
wenn **msdyn\_Abrechnungstyp** = 192350001 ist, dann **belastbar**  
wenn **msdyn\_Abrechnungstyp** = 192350002 ist, dann **kostenlos**  
Sonst **Nicht verfügbar**

#### <a name="transform-the-transaction-types"></a>Transformieren Sie die Transaktionsarten

Die Vorlage für Projektkostenschätzungen (PSA zu Fin und Ops) enthält eine bedingte Spalte, mit der die Transaktionsarten transformiert werden, die während der Integration von Project Service Automation empfangen werden. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen bedingte Spalte hinzufügen. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** aus und wählen dann **Bedingte Spalte hinzufügen**. Geben Sie einen Namen für die neue Spalte ein, wie **Art der Transaktion**. Geben Sie die folgende Bedingung ein:

Wenn **msdyn\_Transaktionstypcode** = 192350000 dann **Kosten**  
wenn **msdyn\_Transaktionstypcode** = 192350005 dann **Vertrieb**  
sonst **Null**

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt Beispiele für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung von Kostenvoranschlagstransaktionen.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Vorlagenzuordnung von Ausgabenvorkalkulationen.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]