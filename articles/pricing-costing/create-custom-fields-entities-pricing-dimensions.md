---
title: Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen benutzerdefinierter Optionssätze oder Entitäten.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000525"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität zur Verwandung als Preisdimension erstellen möchten. Weitere Informationen finden Sie unter [Preisdimensionen – Übersicht](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen. Diese wichtige bewährte Methode bietet in Zukunft Flexibilität, um Änderungen nach Bedarf zu aktualisieren oder zu entfernen. Dies hilft auch bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Nachdem Sie alle erforderlichen Änderungen vorgenommen haben, exportieren Sie diese Lösung als **Verwaltete Lösung** und importieren Sie sie in andere Instanzen, um Ihre Preisgestaltung wiederzuverwenden.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung

Eine Preisdimension kann ein Optionssatz oder eine Entität sein. Beide müssen in der Preisberechnungslösung erstellt werden. In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.

### <a name="entity-based-dimensions"></a>Entitätsbasierte Dimensionen
Führen Sie die folgenden Schritte aus, um entitätsbasierte Dimensionen zu erstellen:

1. Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.
3. Wählen Sie **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen. 
4. Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.

> ![Definition der Entität „Standardtitel”](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Optionssatzbasierte Dimensionen 
Sie können zwei optionssatzbasierte Dimensionen erstellen. 

- Verwenden Sie **Arbeitsort der Ressource**, um den Preis der **Home**-Standortarbeit und **Vor Ort**-Arbeit zu verfolgen. 
- Verwenden sie **Ressourcenarbeitszeit** mit den Werten **Regulär** und **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.

Die folgende Grafik bietet eine Ansicht der **Arbeitsort der Ressource**-Dimension. 

> ![Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource”](media/Option-set-PD-called-Resource-Work-Location.png)

Die folgende Grafik bietet eine Ansicht der **Arbeitsstunden der Ressource**-Dimension. 

> ![Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource”](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie auf  **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus. 
3. Wählen Sie **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und wählen Sie **Speichern**.

## <a name="create-data-for-entity-based-dimensions"></a>Erstellen von Daten für entitätsbasierte Dimensionen

Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen. Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen. Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.

1. Wählen Sie **Erweiterte Suche** aus.
2. Wählen Sie die Entität **Standardtitel** aus und wählen Sie anschließend **Ergebnisse** aus. Alle Zeilen der Entität **Standardtitel** werden angezeigt.
3. Wählen Sie **Neu** und im Feld **Name** geben Sie Systemtechniker ein und wählen dann **Speichern**.
4. Schließen Sie die Seite. 
5. Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.

> ![Beispieldaten für die Entität „Standardtitel“](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]