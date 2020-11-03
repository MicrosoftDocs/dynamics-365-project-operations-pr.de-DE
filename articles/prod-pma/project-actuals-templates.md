---
title: Synchronisieren Sie die Projektdaten direkt von Project Service Automation in das Projektintegrationsjournal, um sie in Finance and Operations zu veröffentlichen
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projekt-Istwerten zwischen Microsoft Dynamics 365 Project Service Automation und Finance and Operations verwendet werden.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076656"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronisieren Sie die Projektdaten direkt von Project Service Automation in das Projektintegrationsjournal, um sie in Finance and Operations zu veröffentlichen

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Projekt-Istwerten zwischen Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.

Die Vorlage synchronisiert Transaktionen von Project Service Automation in eine Staging-Tabelle in Finance. Nach Abschluss der Synchronisierung **müssen** Sie die Daten aus der Staging-Tabelle in das Integrationsjournal importieren.

> [!NOTE]
> - Die Integration der Projekt-Istwerte ist ab Version 8.0.1 verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden, können Sie nach der Installation der Wissensdatenank 4132657 und 4132660 die Vorlagen verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, Stundenschätzungen, Kostenschätzungen und Istdaten zu integrieren und die Funktionssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, empfehlen wir, dass Sie auch KB 4131710 installieren.
> - Wenn Sie Version 7.3.0 verwenden und Gebührentransaktionen von Project Service Automation zu übertragen, müssen Sie die Wissensdatenbank 4345320 installieren, um diese Gebühren in die Projektrechnung aufzunehmen.
> - Wenn Sie in Project Service Automation Umsatzsteuerbeträge für Zeit- oder Aufwandsbuchungen eingeben, müssen Sie Project Service Automation Update 7 installieren. Andernfalls werden die Steuerwerte nicht mit den zugehörigen Zeit- oder Kosten-Istwerten verknüpft und nicht mit Finance synchronisiert. Weitere Informationen erhalten Sie vom Support.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren. Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Datenfluss über Projekt-Istwerte von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekt-Istwerte aus Project Service Automation

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Um auf die verfügbarem Vorlagen zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um Projekt-Istwerte zwischen Project Service Automation und Finance zu synchronisieren.

- **Name der Vorlage in der Datenintegration:** Projekt-Istwerte (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:**

    - Tatsächliche Transaktionen
    - TransactionConnections

### <a name="entity-set"></a>Entität festgelegt

| Project Service Automation | Finanzen                                   |
|----------------------------|----------------------------------------------------------|
| Tatsächliche Transaktionen                    | Integrationsentität für Projekt-Istwerte                   |
| Transaktionsverbindungen    | Integrationsentität für die Projekttransaktion Beziehungen |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Istwerte werden in Project Service Automation verwaltet und mit dem Projektintegrationsjournal von Finance synchronisiert. Die Buchhaltung wird basierend auf den Standardfinanzdimensionen und der Buchungseinrichtung angewendet.

### <a name="prerequisites"></a>Voraussetzungen

Bevor eine Synchronisierung der Istwerte erfolgen kann, müssen Sie die Integrationsparameter von Project Service Automation konfigurieren und Projekte, Projektaufgaben und Projektkosten-Transaktionskategorien synchronisieren.

### <a name="power-query"></a>Power Query

In der Vorlage für Projekt-Istwerte müssen Sie Microsoft Power Query für Excel verwenden, um die folgenden Aufgaben auszuführen:

- Transformieren Sie den Transaktionstyp in Project Service Automation in den richtigen Transaktionstyp in Finance. Diese Transformation ist bereits in der Vorlage für Projekt-Istwerte (PSA zu Fin und Ops) definiert.
- Transformieren Sie den Fakturierungstyp in Project Service Automation in den richtigen Fakturierungstyp in Finance. Diese Transformation ist bereits in der Vorlage für Projekt-Istwerte (PSA zu Fin und Ops) definiert. Die Abrechnungsart wird dann basierend auf der Konfiguration auf der **Integrationsparameter für Project Service Automation** -Seite zur Positionseigenschaft zugeordnet.
- Filtern Sie nach bestimmten Ressourcenorganisationseinheiten, die mit dieser Vorlage synchronisiert werden müssen.
- Wenn Intercompany-Zeit- oder Intercompany-Aufwandsdaten mit Finance synchronisiert werden, müssen Sie die Vertragsorganisationseinheit in die richtige juristische Person in Finance umwandeln. In der Vorlage für Projekt-Istwerte (PSA zu Fin und Ops) wird eine bedingte Spalte basierend auf Demodaten definiert. Sie müssen die zuletzt eingefügte bedingte Spalte auf die richtigen juristischen Personen aktualisieren. Andernfalls kann entweder ein Integrationsfehler auftreten, oder es können falsche tatsächliche Transaktionen in Finance importiert werden.
- Wenn die tatsächlichen oder Intercompany-Ausgaben nicht mit Finance synchronisiert werden, müssen Sie die zuletzt eingefügte bedingte Spalte aus Ihrer Vorlage löschen. Andernfalls kann entweder ein Integrationsfehler auftreten, oder es können falsche tatsächliche Transaktionen in Finance importiert werden.

#### <a name="contract-organizational-unit"></a>Vertragsorganisationseinheit
Um die eingefügte bedingte Spalte in der Vorlage zu aktualisieren, klicken Sie auf den Pfeil **Zuordnen** und öffnen die Zuordnung. Wählen Sie die Verknüpfung **Erweiterte Abfrage und Filterung** , um Power Query zu öffnen.

- Wenn Sie die Standardvorlage für Projekt-Istwerte (PSA zu Fin und Ops) verwenden, wählen Sie in Power Query die letzte Option **Eingefügter Zustand** aus dem Abschnitt **Angewandte Schritte**. In dem Eintrag **Funktion** ersetzen Sie **USSI** mit dem Namen der juristischen Person, die für die Integration verwendet werden soll. Fügen Sie dem **Funktion** -Eintrag nach Bedarf Bedingungen hinzu, und aktualisieren Sie die **else** -Bedingung von **USMF** auf die richtige juristische Person.
- Wenn Sie eine neue Vorlage erstellen, müssen Sie die Spalte hinzufügen, um die Intercompany-Zeit und -Kosten zu unterstützen. Wählen Sie **Bedingte Spalte hinzufügen** aus, und geben Sie einen Namen für die neue Spalte ein wie **LegalEntity**. Geben Sie eine Bedingung für die Spalte ein, wobei, wenn **msdyn\_contractorganizationalunitid.msdyn\_name** \<organizational unit\> entspricht, dann \<enter the legal entity\>; sonst null

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt ein Beispiel der Zuordnungen von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung – Istwerte](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Vorlagenzuordnung – Transaktionsverbindungen](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Import aus Staging-Tabelle nach Integration aus Project Service Automation

Der Import aus periodischen Staging-Tabellenprozessen muss nach der Synchronisierung der Istwerte von Project Service Automation zu Finance ausgeführt werden. Dieser Prozess importiert die Projekttransaktionen aus der Staging-Tabelle in das Integrationsjournal von Project Service Automation, in dem die Buchhaltung angewendet wird und die importierten Transaktionen gebucht werden können. Wir empfehlen, diesen Prozess im Batch-Modus auszuführen. Es kann optional so eingerichtet werden, dass es als wiederkehrender Stapel ausgeführt wird.

## <a name="update-actuals-from-finance"></a>Aktualisieren Sie die Istwerte aus Finance

### <a name="template-and-tasks"></a>Vorlage und Aufgaben

Die folgende Vorlage und die zugrunde liegenden Aufgaben werden verwendet, um die Belegnummer und die Umsatzsteuer für gebuchte Projekttransaktionen von Finance zu Project Service Automation zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Aktualisierung der Projekt-Istwerte (Fin Ops zu PSA)
- **Name der Aufgabe im Projekt:**

    - Tatsächliche Transaktionen 
    - TransactionConnections

### <a name="entity-set"></a>Entität festgelegt

| Finanzen                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integrationsentität für Projekt-Istwerte                   | Tatsächliche Transaktionen                    |
| Integrationsentität für die Projekttransaktion Beziehungen | Transaktionsverbindungen    |

### <a name="entity-flow"></a>Entitätsfluss

Projekt-Istwerte werden in Project Service Automation verwaltet und mit dem Projektintegrationsjournal von Finance synchronisiert. Nachdem die Istwerte in Finance gebucht wurden, werden sie in Project Service Automation mit der Belegnummer aus Finance aktualisiert. Wenn in Finance Umsatzsteuern hinzugefügt wurden, werden in Project Service Automation neue Steuerwerte erstellt.

### <a name="power-query"></a>Power Query

In der Vorlage zur Aktualisierung von Projekt-Istwerten müssen Sie Power Query verwenden, um die folgenden Aufgaben auszuführen:

- Transformieren Sie den Transaktionstyp in Finance in den richtigen Transaktionstyp in Project Service Automation. Diese Transformation ist bereits in der Vorlage zur Aktualisierung von Projekt-Istwerten (Fin Ops zu PSA) definiert.
- Transformieren Sie den Fakturierungstyp in Finance in den richtigen Fakturierungstyp in Project Service Automation. Diese Transformation ist bereits in der Vorlage zur Aktualisierung von Projekt-Istwerten (Fin Ops zu PSA) definiert.

### <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

Die folgende Abbildung zeigt Beispiele für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Finance zu Project Service Automation synchronisiert werden.

[![Vorlagenzuordnung – Istwerte-Aktualisierung](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Vorlagenzuordnung – Transaktionsaktualisierung](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
