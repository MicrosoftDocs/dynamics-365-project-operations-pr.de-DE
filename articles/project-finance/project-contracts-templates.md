---
title: Synchronisieren Sie Projektverträge und Projekte direkt von Project Service Automation zu Finance and Operations
description: Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Verträgen und Projekten direkt zwischen Microsoft Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716483"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren Sie Projektverträge und Projekte direkt von Project Service Automation zu Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlagen und zugrunde liegenden Aufgaben, die zum Synchronisieren von Verträgen und Projekten direkt zwischen Dynamics 365 Project Service Automation und Dynamics 365 Finance verwendet werden.

> [!NOTE] 
> Wenn Sie Enterprise Edition 7.3.0 verwenden, müssen Sie die Wissensdatenbank 4074835 installieren.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

> [!NOTE]
> Bevor Sie die Integrationslösung Project Service Automation zu Finance verwenden können, sollten Sie mit der Dynamics 365-Datenintegrationsfunktion vertraut sein.

Die Integrationslösung für Project Service Automation zu Finance verwendet die Datenintegrationsfunktion, um Daten über Instanzen von Project Service Automation und Finance hinweg zu synchronisieren. Die Integrationsvorlage, die mit der Datenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss über Projektverträge, Projekte, Projekt-Vertragszeilen und Projekt-Vertragszeilen-Meilensteine von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie die Daten zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Vorlagen und Aufgaben

Um auf die verfügbarem Vorlagen zuzugreifen, klicken Sie auf das Microsoft Power Apps Admin Center, wählen Sie **Projekte** und wählen Sie dann in der oberen rechten Ecke **Neues Projekt** aus, um öffentliche Vorlagen auszuwählen.

Die folgenden Vorlagen und die zugrunde liegenden Aufgaben werden verwendet, um Projektverträge und Projekte von Project Service Automation und Finance zu synchronisieren.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integration mit Dynamics 365 Project Service Automation v2.x
- **Name der Vorlage in der Datenintegration:** Projekte und Verträge (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:**

    - Projektaufträge PSA mit Fin und Ops
    - Projekte PSA zu Fin und Ops
    - Projektauftragszeilen PSA mit Fin und Ops
    - Projektauftragszeilen-Meilensteine PSA mit Fin und Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integration mit Dynamics 365 Project Service Automation v3.x
In Project Service Automation gibt es eine Schemaänderung, die sich auf die Meilensteinvorlage für die Projektvertragslinie auswirkt. Die v2 Version der Vorlage ist erforderlich, um Project Service Automation v3.x in Dynamics 365 zu integrieren.

- **Name der Vorlage in der Datenintegration:** Projekte und Verträge (PSA 3.x zu Fin und Ops) - v2
- **Name der Aufgabe im Projekt:**

    - Projektaufträge PSA mit Fin und Ops
    - Projekte PSA zu Fin und Ops
    - Projektauftragszeilen PSA mit Fin und Ops
    - Projektauftragszeilen-Meilensteine PSA mit Fin und Ops

Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Konten synchronisieren.

## <a name="entity-set"></a>Entität festgelegt

| Project Service Automation       | Finanzen                                                |
|----------------------------------|--------------------------------------------------------|
| Aufträge                           | Integrationsentität für Projektverträge                |
| Projekte                         | Integrationsentität für Projekt                         |
| Auftragspositionen                      | Integrationsentität für Projektvertragszeile           |
| Meilensteine für Projektvertragszeilen | Integrationsentität für Projektvertragszeile-Meilenstein |

## <a name="entity-flow"></a>Entitätsfluss

Projektverträge werden in Project Service Automation verwaltet und als Projektaktivitäten mit Finance als Projektverträge synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle in Finance für den Projektvertrag festlegen.

Zeit- und Materialprojekt und Projekt mit festen Preisen werden in Project Service Automation verwaltet und sie werden mit Finance als Projekte synchronisiert. Als Teil der Integrationsvorlage können Sie die Integrationsquelle in Finance für das Projekt festlegen.

Projektvertragszeilen werden in Project Service Automation verwaltet und als Projektvertragsabrechnungsregeln mit Finance synchronisiert. Wenn sich die Abrechnungsmethode vom Standardprojekttyp unterscheidet, aktualisiert die Synchronisierung den Projekttyp für das Vertragslinienprojekt und die Projektgruppe.

Projektvertragszeilenmeilensteine werden in Project Service Automation verwaltet und sie werden mit Finance als Projektvertragsabrechnungsregeln-Meilensteine synchronisiert.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation zu Finance Integrationslösung

Das **Projektvertrags-ID** Feld ist verfügbar auf der Seite **Projektverträge**. Dieses Feld wurde zu einem natürlichen und einzigartigen Schlüssel zur Unterstützung der Integration gemacht.

Wenn ein neuer Projektvertrag erstellt wird, wenn ein **Projektvertrags-ID** Wert noch nicht existiert, wird automatisch mithilfe einer Zahlenfolge generiert. Der Wert besteht aus **ORD** gefolgt von einer inkrementellen Zahlenfolge und einem Suffix von sechs Zeichen. Beispiel: **ORD-01022-Z4M9Q0**.

Das **Projektnummern** Feld ist verfügbar auf der Seite **Projekte**. Dieses Feld wurde zu einem natürlichen und einzigartigen Schlüssel zur Unterstützung der Integration gemacht.

Wenn ein neuer Projektvertrag erstellt wird, wenn ein **Projektnummer** Wert noch nicht existiert, wird er automatisch mithilfe einer Zahlenfolge generiert. Der Wert besteht aus **PRJ** gefolgt von einer inkrementellen Zahlenfolge und einem Suffix von sechs Zeichen. Beispiel: **PRJ-01049-CCNID0**.

Wenn die Integrationslösung Project Service Automation zu Finance angewendet wird, legt ein Upgrade-Skript das Feld **Projektvertrags-ID** für bestehende Projektverträge und das Feld **Projektnummer** für bestehende Projekte in Project Service Automation fest.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Mappingeinrichtung

- Bevor die Synchronisierung von Projektaufgaben erfolgen kann, müssen Sie Konten synchronisieren.
- Fügen Sie in Ihrem Verbindungssatz eine Integrationsschlüsselfeldzuordnung für **msdy\_Organisationseinheiten** zu **msdyn\_Name \[Name\]** hinzu. Möglicherweise müssen Sie zuerst ein Projekt zum Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Daten integrieren in Common Data Service für Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Fügen Sie in Ihrem Verbindungssatz eine Integrationsschlüsselfeldzuordnung für **msdyn\_Projekte** zu **msdynce\_projectnumber \[Projektnummer\]**. Möglicherweise müssen Sie zuerst ein Projekt zum Verbindungssatz hinzufügen. Weitere Informationen finden Sie unter [Daten integrieren in Common Data Service für Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** für Projektverträge und Projekte können auf einen anderen Wert aktualisiert oder aus dem Mapping entfernt werden. Der Standardvorlagenwert ist **Project Service Automation**.
- Das **Zahlungsbedingungen**-Mapping muss aktualisiert werden, damit es die gültigen Zahlungsbedingungen in Finance widerspiegelt. Sie können das Mapping auch aus der Projektaufgabe entfernen. Die Standardwertzuordnung enthält Standardwerte für Demodaten. Die folgende Tabelle zeigt die Werte in Project Service Automation.

    | Value | Beschreibung   |
    |-------|---------------|
    | 1     | 30 Tage netto        |
    | 2     | 10 Tage 2%, 30 Tage netto |
    | 3     | 45 Tage netto        |
    | 4     | 60 Tage netto        |

## <a name="power-query"></a>Power Query

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn die folgenden Bedingungen erfüllt sind:

- Sie haben Vertriebsaufträge in Dynamics 365 Sales.
- Sie haben mehrere Organisationseinheiten in Project Service Automation, und diese Organisationseinheiten werden mehreren juristischen Entitäten in Finance zugeordnet.

Wenn Sie Power Query verwenden müssen, folgen Sie diesen Richtlinien:

- Die Vorlage Projekte und Verträge (PSA zu Fin und Ops) verfügt über einen Standardfilter, der nur Vertriebsaufträge des Typs **Arbeitselement (msdyn\_ordertype = 192350001)**. Mit diesem Filter können Sie sicherstellen, dass keine Projektverträge für Vertriebsaufträge in Finance erstellt werden. Wenn Sie eine eigene Vorlage erstellen, müssen Sie diesen Filter hinzufügen.
- Sie müssen einen Filter Power Query erstellen, der nur die Vertragsorganisationen enthält, die mit der juristischen Person des Integrationsverbindungssatzes synchronisiert werden sollen. Beispielsweise sollten Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso US haben, mit der juristischen Person USSI synchronisiert werden, Projektverträge, die Sie mit der Vertragsorganisationseinheit von Contoso Global haben, sollten jedoch mit der juristischen Person USMF synchronisiert werden. Wenn Sie diesen Filter nicht zu Ihrer Aufgabenzuordnung hinzufügen, werden alle Projektverträge unabhängig von der Vertragsorganisationseinheit mit der für den Verbindungssatz definierten juristischen Person synchronisiert.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in der Datenintegration

> [!NOTE] 
> Die Felder **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AdressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, und **AddressZipCode** sind in der Standardzuordnung für Projektverträge nicht enthalten. Sie können die Zuordnungen hinzufügen, wenn diese Daten für Projektverträge synchronisiert werden sollen.
>
> Die Felder **Beschreibung**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, und **ProjektType** sind in der Standardzuordnung für Projekte nicht enthalten. Sie können die Zuordnungen hinzufügen, wenn diese Daten für Projekte synchronisiert werden sollen.

Die folgende Abbildung zeigt Beispiele für die Zuordnung von Vorlagenaufgaben in der Datenintegration. Das Mapping zeigt die Feldinformationen an, die von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Vorlagenzuordnung](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Meilensteinzuordnung für Projektvertragszeilen in der Vorlage Projekte und Verträge (PSA 3.x zu Dynamics) – v2 Vorlage:

[![Vorlagenzuordnung](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
