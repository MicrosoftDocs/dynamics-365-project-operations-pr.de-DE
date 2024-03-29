---
title: Benutzerdefinierte Felder und Entitäten erstellen
description: Dieser Artikel erklärt, wie Sie Optionssätze und Entitäten in Ihrer eigenen Lösung in der Power Apps-Plattform erstellen können.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926913"
---
# <a name="create-custom-fields-and-entities"></a>Benutzerdefinierte Felder und Entitäten erstellen 

[!include [banner](../includes/psa-now-project-operations.md)]

Führen Sie die folgenden Schritte aus, wenn Sie einen benutzerdefinierten Optionssatz oder eine Entität auf der Power Apps-Plattform erstellen möchten.  
Die Vorgänge in diesem Artikel sollten über die Weboberfläche von Project Service Automation (PSA) ausgeführt werden.

> [!IMPORTANT]
> Wir empfehlen, alle benutzerdefinierten Preisdimensionsänderungen in einer separaten Lösung vorzunehmen. Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Erstellen benutzerdefinierter Felder und Optionssätze in der Preisdimensionslösung

Eine Preisdimension kann ein Optionssatz oder eine Entität sein. Beide müssen in der Preisberechnungslösung erstellt werden. In den Schritten in diesem Verfahren wird erläutert, wie entitätsbasierte bzw. optionssatzbasierte Dimensionen erstellt werden.

### <a name="entity-based-dimensions"></a>Entitätsbasierte Dimensionen

1. Wählen Sie in PSA **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten** aus.
3. Klicken Sie auf **Neu**, um eine neue Entität namens **Standardtitel** zu erstellen. Geben Sie die verbleibenden erforderlichen Informationen ein und klicken Sie anschließend auf **Speichern**.

> ![Definition der Entität „Standardtitel“.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Optionssatzbasierte Dimensionen 
Sie können zwei optionssatzbasierte Dimensionen erstellen. Verwenden Sie **Arbeitsstandort der Ressource**, um den Preis für die Arbeit am **Wohnort** und  **Vor Ort** nachzuverfolgen. Verwenden Sie für **Arbeitszeiten der Ressource** die Werte **Regulär** bzw. **Überstunden**, um einen Aufschlag anzuwenden, wenn die Arbeit abgeschlossen ist.


1. Wählen Sie in PSA **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Optionssätze** aus. 
3. Klicken Sie auf **Neu**, um einen neuen Optionssatz zu erstellen, geben Sie die verbleibenden erforderlichen Informationen ein, und klicken Sie dann auf **Speichern**.

> ![Optionssatzbasierte Preisdimension namens „Arbeitsstandort der Ressource“.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Optionssatzbasierte Preisdimension namens „Arbeitszeiten der Ressource“.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Erstellen von Daten für entitätsbasierte Dimensionen

Sie können Daten für entitätsbasierte Dimensionen manuell oder mithilfe von Microsoft Excel-Import- oder -Service-Aufrufen erstellen. Führen Sie die in diesem Verfahren beschriebenen Schritte aus, um zwei Standardtitel – **- Systemtechniker** und **Leitender Systemtechniker** – aus der entitätsbasierten Dimension **Standardtitel** zu erstellen. Wenn die Datenmenge, die Sie erstellen möchten, gering ist, wie im folgenden Beispiel gezeigt, können Sie ein Standardformular verwenden.

1. Klicken Sie in PSA auf **Erweiterte Suche**. Wählen Sie die Entität **Standardtitel** aus und klicken Sie anschließend auf **Ergebnisse**. Alle Zeilen der Entität **Standardtitel** werden angezeigt.
2. Klicken Sie auf **Neu**. Geben Sie im Feld **Name** „Systemtechniker“ ein und klicken Sie dann auf **Speichern**.
3. Schließen Sie das Formular. 
4. Wiederholen Sie die Schritte 1 - 3, um einen anderen Standardtitel für „Leitender Systemtechniker“ zu erstellen.

> ![Beispieldaten für die Entität „Standardtitel“.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
