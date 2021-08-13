---
title: Eine Lösung für benutzerdefinierte Preisdimensionen erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Lösungen für benutzerdefinierte Preisdimensionen.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992205"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Eine Lösung für benutzerdefinierte Preisdimensionen erstellen

 _**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_ 

>[!IMPORTANT]
>Alle Änderungen der benutzerdefinierten Preisdimension sollten in einer separaten Lösung erfolgen. Diese wichtige bewährte Methode bietet die Flexibilität, Änderungen nach Bedarf zu aktualisieren oder zu entfernen, hilft bei der Wiederverwendung Ihrer Arbeit und erleichtert das Portieren dieser Änderungen auf andere Instanzen. Wenn alle erforderlichen Änderungen vorgenommen wurden, können Sie diese Lösung als **Verwaltete Lösung** exportieren und in andere Instanzen importieren, um sie wiederzuverwenden.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Eine Lösung für benutzerdefinierte Preisdimensionen erstellen

1.  Wählen Sie **Einstellungen** > **Lösungen** und dann **Neu** aus.
2.  Nennen Sie die Lösung *<your organization name>-Preisdimensionen*.
3. Geben Sie die verbleibenden erforderlichen Informationen ein und wählen Sie **Speichern**.

  ![Erstellen einer Lösung für benutzerdefinierte Preisdimensionen.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Hinzufügen aller erforderlichen Entitäten und zugehörigen Komponenten zur Preisdimensionslösung

Fügen Sie Ihrer Preislösung die folgenden Project Service-Entitäten hinzu, um wichtige Schemaänderungen in der Preislösung vorzunehmen. Nachdem Sie dieses Verfahren abgeschlossen haben, erkennen die Entitäten die neuen Preisdimensionen.

1.  Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie anschließend auf **<*Name Ihrer Organisation*> Preisdimensionen**.
2.  Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Vorh. hinzufügen** > **Entitäten** aus.
3.  Wählen Sie im Dialogfeld **Lösungskomponenten** die folgenden Entitäten aus:
 
   - **Tatsächl.**
   - **Buchbare Ressource**
   - **Vorkalkulationsposition**
   - **Projektaufgabe**
   - **Rechnungsposition**
   - **Erfassungsposition**
   - **Projektvertragsposition**
   - **Projektteammitglied**
   - **Detailinformationen zur Angebotsposition**
   - **Rollenpreisaufschlag**
   - **Rollenpreis**
   - **Zeiteintrag**
 
   ![Hinzufügen vorhandener Entitäten zur Lösung für benutzerdefinierte Preisdimensionen.](./media/Existing-entities-to-PD-solution.png)
 
 4. Überprüfen Sie für jede Entität die hinzugefügten Komponenten und die endgültige Liste der Entitätsressourcen für jede Entität. 

   >[!NOTE]
   > Beziehen Sie alle Formulare und Ansichten für jede der ausgewählten Entitäten ein.

  ![Entitäten hinzugefügt.](./media/solution-component-selection.png)


5.  Wenn Sie aufgefordert werden, abhängige Entitäten für die ausgewählten Entitäten einzuschließen, wählen Sie **Nein, erforderliche Komponenten nicht einschließen.**

    ![Einschließlich abhängiger Einheiten.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]