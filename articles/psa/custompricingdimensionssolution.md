---
title: Erstellen von benutzerdefinierten Lösungen für Preisdimensionen
description: Dieser Artikel erklärt, wie Sie eine angepasste Lösung erstellen, wenn Sie angepasste Dimensionen für die Preisgestaltung erstellen.
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
ms.openlocfilehash: 0df6728634b169c8a1a128aba1555d79fee5719f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929029"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Erstellen von benutzerdefinierten Lösungen für Preisdimensionen

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Alle Änderungen der benutzerdefinierten Preisdimension sollten in einer separaten Lösung erfolgen. Diese wichtige bewährte Methode bietet in Zukunft die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf eine andere Instanz. Nachdem Sie die erforderlichen Änderungen vorgenommen haben, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um Ihre Preiskonfiguration wiederzuverwenden.

1. Wählen Sie **Einstellungen** > **Lösungen** und dann **Neu** aus. 
2. Geben Sie der Lösung einen Namen, **\<your organization name> Preisdimensionen**, geben die verbleibenden erforderlichen Informationen ein und wählen dann **Speichern**.

> ![Erstellen einer benutzerdefinierten Lösung für Preisdimensionen.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung
Sie müssen Ihrer Preisberechnungslösung die folgenden Project Service-Entitäten hinzufügen. Schließen Sie die Schritte in diesem Verfahren ab, um einige wichtige Schemaänderungen in der Preisberechnungslösung vorzunehmen, damit die Entitäten die neuen Preisberechnungsdimensionen kennen.

1. Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.
3. Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:

- Tatsächl.
- Buchbare Ressource
- Vorkalkulationsposition
- Projektaufgabe
- Rechnungsposition
- Erfassungsposition
- Projektvertragsposition
- Projektteammitglied
- Detailinformationen zur Angebotsposition
- Rollenpreisaufschlag
- Rollenpreis 
- Zeiteintrag 

> ![Hinzufügen vorhandener Entitäten zur Lösung für Preisdimensionen.](media/Existing-entities-to-PD-solution.png)

> ![Lösungskomponenten auswählen](media/Dimension-Components.png)

> [!NOTE]
> Stellen Sie sicher, dass alle Formulare und Ansichten für jede der ausgewählten Entitäten enthalten sind.

4. Wenn Sie aufgefordert werden, abhängige Entitäten für die ausgewählten Entitäten einzuschließen, wählen Sie **Nein**.

> ![Schließen Sie nicht alle zugehörigen Komponenten ein.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
