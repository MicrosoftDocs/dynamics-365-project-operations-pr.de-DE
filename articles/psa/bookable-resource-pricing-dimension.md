---
title: Verwenden buchbarer Ressourcen als Preisdimension
description: Dieser Artikel enthält Informationen über die Verwendung einer buchbaren Ressource als Dimension für die Preisgestaltung.
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
ms.openlocfilehash: becb64bb137079422a765dd7cd61369297e1ffb1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916103"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Verwenden buchbarer Ressourcen als Preisdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Dieser Artikel enthält Informationen über die Verwendung einer buchbaren Ressource als Dimension für die Preisgestaltung. Bevor Sie beginnen, falls Sie noch keine Preisdimensionslösung erstellt haben, müssen Sie eine neue erstellen. Wenn Sie bereits eine Preisdimensionslösung haben, dann können Sie Ihre Änderungen in dieser Lösung vornehmen. Wenn Sie noch keine neue Lösung für Preisdimensionen in Ihrem Unternehmen erstellt haben, führen Sie die Verfahren im Artikel [Angepasste Felder und Entitäten erstellen](create-custom-fields-entities.md) aus.

## <a name="add-bookable-resource-to-forms-and-views"></a>Hinzufügen von buchbaren Ressourcen zu Formularen und Ansichten
Um die Felder in der Benutzeroberfläche in der Preisdimensionslösung sichtbar zu machen, müssen Sie alle Formulare und Ansichten der wichtigsten Project Service-Entitäten durchgehen und diese Felder zu den Formularen und Ansichten dieser Entitäten hinzufügen.
Die folgende Tabelle enthält eine umfassende Liste der vorkonfigurierten Formulare und Ansichten nach Entität, die aktualisiert werden müssen. Wenn es irgendwelche zusätzlichen Ansichten oder Formulare in Ihren Anpassungen für diese Entitäten gibt, fügen Sie diesen die neuen Felder ebenfalls hinzu.
Öffnen Sie den Lösungs-Explorer der Preisdimensionslösung und klicken Sie dann auf **Alle Anpassungen veröffentlichen**.


|   Entität        | Formulare   |Ansichten        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollenpreis|• Informationen |• Preise der aktiven Ressourcenkategorie<br> • Zugeordnete Ansicht: Preis der Ressourcenkategorie|
|  Rollenpreisaufschlag|• Informationen|• Aktiver Rollenpreisaufschlag<br>• Zugeordnete Ansicht: Rollenpreisaufschlag|
|  Detailinformationen zur Angebotsposition|• Projektinformationen<br>• Projektschnellerfassung|• Details zu aktiver Angebotsposition<br>• Kombinierte Angebotspositionsdetails<br>• Zugeordnete Ansicht: Angebotspositionsdetail|
|  Positionsdetail von Projektvertrag|• Projektinformationen<br>• Projektschnellerfassung|• Kombinierte Vertragspositionsdetails<br>• Aktive Vertragspositionsdetails<br>• Zugeordnete Ansicht: Vertragspositionsdetail|
|  Projektaufgabe|• Informationen<br>• Neues Formular||
|  Projektteammitglied|• Informationen<br>• Neues Formular|• Aktive Projektteammitglieder<br>• Projektteammitglieder<br>• Zugeordnete Ansicht: Projektteammitglieder|
|  Zeiteintrag|• Informationen<br>• Zeiteintrag erstellen|• Meine Zeiteinträge nach Datum<br>• Meine Zeiteinträge für diese Woche<br>• Zeiteinträge zur Genehmigung|
|  Erfassungsposition|• Informationen<br>• Schnellerfassung|• Aktive Erfassungspositionen<br>• Zugeordnete Ansicht: Erfassungsposition|
|  Rechnungsposition|• Informationen<br>• Schnellerfassung|• Aktive Rechnungspositionsdetails<br>• Fakturierbare Rechnungsbuchungen<br>• Zusätzliche Rechnungsbuchungen<br>• Zugeordnete Ansicht: Rechnungspositionsdetail<br>• Nicht-fakturierbare Rechnungsbuchungen|
|  Tatsächlich|• Informationen<br>• Aktive Ist-Werte|• Zugeordnete Ansicht: Ist-Werte|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Einrichten von buchbaren Ressourcen als Preisdimension

1. In der Weboberfläche wechseln Sie zu **Project Service** > **Einstellungen** > **Parameter**. Beachten Sie auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen**, dass das Raster in der Registerkarte die Datensätze in der Entität „Preisdimensionen“ anzeigt. 
2. Fügen Sie dieser Liste der Preisdimensionen **Buchbare Ressource** als **msdyn_bookableresource** hinzu. 
3. Geben Sie den Kontext an, in dem die buchbare Ressource als Preisdimension fungiert, und legen Sie die Werte **Gilt für Kosten** und **Gilt für Vertrieb** fest.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus. 
5. Wählen Sie die Kosten- und Vertriebspriorität für die buchbare Ressource aus. Wenn eine buchbare Ressource als Preisdimension einbezogen wird, hat sie in der Regel die höchste Priorität. Wenn Sie diese also auf **1** (oder **0**, je nachdem, wie Sie die Priorität zählen) festlegen, wird dieses Verhalten sichergestellt.

## <a name="set-up-pricing-dimension-field-names"></a>Einrichten von Feldnamen für Preisdimensionen

Wenn sich der Feldname einer Preisdimension in der Tabelle **Rollenpreis** von dem Feldnamen in einer der anderen Entitäten unterscheidet, in denen der Standardpreis funktionieren muss, muss der Preisdimensionsdatensatz die verschiedenen Namen kennen.    
Bei einer buchbaren Ressource verfügt die Entität **Projektteammitglieder** über einen geringfügig anderen Feldnamen (**msdyn_bookableresourceid**), als die Entität **Rollenpreis** (**msdyn_bookableresource**). Der Preisdimensionsdatensatz **msydn_bookableresource** muss diesen kennen. 
1. Doppelklicken Sie dazu auf die Zeile im Raster **Preisdimensionen**, um die Dimensionsseite von **msdyn_bookableresource** zu öffnen.
2. Klicken Sie auf der Dimensionsseite auf der Registerkarte **Verknüpft** auf **Preisdimensions-Feldnamen**.

 ![Registerkarte „Preisdimensions-Feldnamen“.](media/PD-fieldname.png)

4. Klicken Sie in der angezeigten Ansicht auf **Neuen Preisdimensions-Feldnamen hinzufügen**.

 ![Neue Preisdimensions-Feldnamen hinzufügen.](media/Add-NewPD-fieldname.png)


Dadurch wird die Seite **Neuer Preisdimensions-Feldnamen** für **msdyn_bookableresource** geöffnet. 

5. Fügen Sie **msdyn_projectteam** dem Feld **Logischer Name der Entität** und **msdyn_bookableresourceid** dem Feld **Feldname** hinzu. Speichern Sie den Datensatz.

 ![Formular „Neuer Preisdimensions-Feldname“.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
