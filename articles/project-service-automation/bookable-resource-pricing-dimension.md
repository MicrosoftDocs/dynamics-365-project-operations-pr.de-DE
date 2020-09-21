---
title: Verwenden buchbarer Ressourcen als Preisdimension
description: Dieses Thema bietet Informationen über das Verwenden von buchbaren Ressourcen als Preisdimension.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721993"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Verwenden buchbarer Ressourcen als Preisdimension
Dieses Thema bietet Informationen über das Verwenden von buchbaren Ressourcen als Preisdimension. Bevor Sie beginnen, falls Sie noch keine Preisdimensionslösung erstellt haben, müssen Sie eine neue erstellen. Wenn Sie bereits eine Preisdimensionslösung haben, dann können Sie Ihre Änderungen in dieser Lösung vornehmen. Wenn Sie keine neue Preisdimensionslösung für Ihre Organisation erstellt haben, führen Sie die Prozeduren im Thema [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities.md) durch.

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
|  Projektteammitglied|• Informationen<br>• Neues Formular|• Aktive Projektteammitglieder<br>• Projektteammitglieder<br>• Zugeordnete Ansicht: Projektteammitglieder|
|  Zeiteintrag|• Informationen<br>• Zeiteintrag erstellen|• Meine Zeiteinträge nach Datum<br>• Meine Zeiteinträge für diese Woche<br>• Zeiteinträge zur Genehmigung|
|  Erfassungsposition|• Informationen<br>• Schnellerfassung|• Aktive Erfassungspositionen<br>• Zugeordnete Ansicht: Erfassungsposition|
|  Rechnungsposition|• Informationen<br>• Schnellerfassung|• Aktive Rechnungspositionsdetails<br>• Fakturierbare Rechnungsbuchungen<br>• Zusätzliche Rechnungsbuchungen<br>• Zugeordnete Ansicht: Rechnungspositionsdetail<br>• Nicht-fakturierbare Rechnungsbuchungen|
|  Tatsächlich|• Informationen<br>• Aktive Ist-Werte|• Zugeordnete Ansicht: Ist-Werte|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Einrichten von buchbaren Ressourcen als Preisdimension

1. In der Weboberfläche wechseln Sie zu **Project Service** > **Einstellungen** > **Parameter**. Beachten Sie auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen**, dass das Raster in der Registerkarte die Datensätze in der Entität „Preisdimensionen” anzeigt. 
2. Fügen Sie dieser Liste der Preisdimensionen **Buchbare Ressource** als **msdyn_bookableresource** hinzu. 
3. Geben Sie den Kontext an, in dem die buchbare Ressource als Preisdimension fungiert, und legen Sie die Werte **Gilt für Kosten** und **Gilt für Vertrieb** fest.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus. 
5. Wählen Sie die Kosten- und Vertriebspriorität für die buchbare Ressource aus. Wenn eine buchbare Ressource als Preisdimension einbezogen wird, hat sie in der Regel die höchste Priorität. Wenn Sie diese also auf **1** (oder **0**, je nachdem, wie Sie die Priorität zählen) festlegen, wird dieses Verhalten sichergestellt.

## <a name="set-up-pricing-dimension-field-names"></a>Einrichten von Feldnamen für Preisdimensionen

Wenn sich der Feldname einer Preisdimension in der Tabelle **Rollenpreis** von dem Feldnamen in einer der anderen Entitäten unterscheidet, in denen der Standardpreis funktionieren muss, muss der Preisdimensionsdatensatz die verschiedenen Namen kennen.    
Bei einer buchbaren Ressource verfügt die Entität **Projektteammitglieder** über einen geringfügig anderen Feldnamen (**msdyn_bookableresourceid**), als die Entität **Rollenpreis** (**msdyn_bookableresource**). Der Preisdimensionsdatensatz **msydn_bookableresource** muss diesen kennen. 
1. Doppelklicken Sie dazu auf die Zeile im Raster **Preisdimensionen**, um die Dimensionsseite von **msdyn_bookableresource** zu öffnen.
2. Klicken Sie auf der Dimensionsseite auf der Registerkarte **Verknüpft** auf **Preisdimensions-Feldnamen**.

 ![Registerkarte „Preisdimensions-Feldnamen”](media/PD-fieldname.png)

4. Klicken Sie in der angezeigten Ansicht auf **Neuen Preisdimensions-Feldnamen hinzufügen**.

 ![Neue Preisdimensions-Feldnamen hinzufügen](media/Add-NewPD-fieldname.png)


Dadurch wird die Seite **Neuer Preisdimensions-Feldnamen** für **msdyn_bookableresource** geöffnet. 

5. Fügen Sie **msdyn_projectteam** dem Feld **Logischer Name der Entität** und **msdyn_bookableresourceid** dem Feld **Feldname** hinzu. Speichern Sie den Datensatz.

 ![Formular „Neuer Preisdimensions-Feldname”](media/PD-fieldname-Added.png)
