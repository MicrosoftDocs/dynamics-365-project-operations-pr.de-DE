---
title: Benutzerdefinierte Felder und Entitäten erstellen
description: In diesem Thema wird erläutert, wie Optionssätze und Entitäten in Ihrer eigenen Lösung auf der Power Apps Plattform erstellt werden.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722039"
---
# <a name="create-custom-fields-and-entities"></a>Benutzerdefinierte Felder und Entitäten erstellen 

Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität auf der Power Apps-Plattform erstellen möchten.  
Die Verfahren in diesem Thema sollten über die Weboberfläche von Project Service Automation (PSA) ausgeführt werden.

> [!IMPORTANT]
> Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen. Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Erstellen einer benutzerdefinierten Lösung für Preisdimensionen
1. Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und dann auf **Neu**, um eine neue Lösung zu erstellen. 
2. Geben Sie der Lösung einen Namen, **\<Name Ihrer Organisation name > Preisdimensionen**, geben die verbleibenden erforderlichen Informationen ein und klicken anschließend auf **Speichern**.

> ![Erstellen einer benutzerdefinierten Lösung für Preisdimensionen](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung

Eine Preisdimension kann ein Optionssatz oder eine Entität sein. Beide müssen in der Preisberechnungslösung erstellt werden. In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.

### <a name="entity-based-dimensions"></a>Entitätsbasierte Dimensionen

1. Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**.
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.
3. Klicken Sie auf **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen. Geben Sie die verbleibenden erforderlichen Informationen ein und klicken Sie anschließend auf **Speichern**.

> ![Definition der Entität „Standardtitel”](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Optionssatzbasierte Dimensionen 
Sie können zwei optionssatzbasierte Dimensionen erstellen. Verwenden Sie **Arbeitsstandort der Ressource**, um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.


1. Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus. 
3. Klicken Sie auf **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und klicken Sie dann auf **Speichern**.

> ![Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource” ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource” ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Erstellen von Daten für entitätsbasierte Dimensionen

Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen. Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen. Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.

1. Klicken Sie in PSA auf **Erweiterte Suche**. Wählen Sie die Entität **Standardtitel** aus und klicken Sie anschließend auf **Ergebnisse**. Alle Zeilen der Entität **Standardtitel** werden angezeigt.
2. Klicken Sie auf **Neu**. Geben Sie im Feld **Name** „Systemtechniker” ein und klicken Sie dann auf **Speichern**.
3. Schließen Sie das Formular. 
4. Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker” zu erstellen.

> ![Beispieldaten für die Entität „Standardtitel” ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Hinzufügen aller erforderlichen PSA-Entitäten und zugehörigen Komponenten zur Preisdimensionslösung
Sie müssen Ihrer Preisberechnungslösung die folgenden Project Service-Entitäten hinzufügen. Führen Sie die Schritte in diesem Verfahren aus, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.

1. Klicken Sie in PSA auf **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **\<Name Ihrer Organisation > Preisdimensionen**. 
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

> ![Hinzufügen vorhandener Entitäten zur Lösung für Preisdimensionen](media/Existing-entities-to-PD-solution.png)

> ![Lösungskomponenten auswählen](media/Dimension-Components.png)

> [!NOTE]
> Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.

4. Wenn Sie aufgefordert werden, abhängige Entitäten für die oben ausgewählten Entitäten einzuschließen, klicken Sie auf **Nein**.

> ![Schließen Sie nicht alle zugehörigen Komponenten ein.](media/Do-not-include-required.png)


