---
title: Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen benutzerdefinierter Optionssätze oder Entitäten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076562"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Benutzerdefinierte Felder und Entitäten als Preisdimensionen erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität erstellen möchten.

> [!IMPORTANT]
> Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen. Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Erstellen einer benutzerdefinierten Lösung für Preisdimensionen
1. Gehen Sie zu **Einstellungen** > **Lösungen** und wählen **Neu** , um eine neue Lösung zu erstellen. 
2. Geben Sie der Lösung einen Namen, **\<your organization name> Preisdimensionen** , geben die verbleibenden erforderlichen Informationen ein und wählen dann **Speichern**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung

Eine Preisdimension kann ein Optionssatz oder eine Entität sein. Beide müssen in der Preisberechnungslösung erstellt werden. In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.

### <a name="entity-based-dimensions"></a>Entitätsbasierte Dimensionen

1. Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.
3. Wählen Sie **Neu** , um eine neue Entität namens **Standardtitel** zu erstellen. 
4. Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.


### <a name="option-set-based-dimensions"></a>Optionssatzbasierte Dimensionen 
Sie können zwei optionssatzbasierte Dimensionen erstellen. Verwenden Sie **Arbeitsstandort der Ressource** , um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden** , um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.


1. Gehen Sie zu **Einstellungen** > **Lösungen** und doppelklicken Sie auf  **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus. 
3. Wählen Sie **Neu** , um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und wählen Sie **Speichern**.

## <a name="create-data-for-entity-based-dimensions"></a>Erstellen von Daten für entitätsbasierte Dimensionen

Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen. Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen. Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.

1. Wählen Sie **Erweiterte Suche** und wählen Sie die Entität **Standardtitel** und dann **Ergebnisse**. Alle Zeilen der Entität **Standardtitel** werden angezeigt.
2. Wählen Sie **Neu** und im Feld **Name** geben Sie Systemtechniker ein und wählen dann **Speichern**.
3. Schließen Sie das Formular. 
4. Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung
Sie müssen Ihrer Preisberechnungslösung die folgenden Entitäten hinzufügen. Führen Sie die Schritte in diesem Verfahren aus, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.

1. Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.
3. Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:

  - Tatsächlich
  - Buchbare Ressource
  - Vorkalkulationsposition
  - Rechnungsposition
  - Erfassungsposition
  - Projektvertragsposition
  - Projektteammitglied
  - Detailinformationen zur Angebotsposition
  - Rollenpreisaufschlag
  - Rollenpreis 
  - Zeiteintrag 


> [!NOTE]
> Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.

4. Wenn Sie aufgefordert werden, abhängige Entitäten für die oben ausgewählten Entitäten einzuschließen, wählen Sie **Nein**.

