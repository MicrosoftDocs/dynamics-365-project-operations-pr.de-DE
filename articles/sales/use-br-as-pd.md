---
title: Eine buchbare Ressourcen als Preisdimension verwenden
description: Dieses Thema bietet Informationen über das Verwenden von buchbaren Ressourcen als Preisdimension.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643082"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Eine buchbare Ressourcen als Preisdimension verwenden

 _**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_ 

Dieses Thema bietet Informationen über das Verwenden von buchbaren Ressourcen als Preisdimension. Wenn Ihre Preisstrategie so eingerichtet ist, dass jede buchbare Ressource einen bestimmten Preis oder Kostensatz haben muss, verwenden Sie eine buchbare Ressource als Preisdimension.

## <a name="prerequisites"></a>Anforderungen
Bevor Sie die in diesem Thema beschriebenen Verfahren ausführen, müssen Sie über eine neue Lösung für die Preisdimension für Ihr Unternehmen verfügen. Wenn Sie noch keine erstellt haben, lesen Sie [Benutzerdefinierte Felder und Entitäten erstellen](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Feld „Buchbare Ressource“ zu Formularen und Ansichten hinzufügen
Um das **Buchbare Ressource**-Feld in der Preisdimensionslösung anzuzeigen, müssen Sie das Feld allen Formularen und Ansichten als Entität hinzufügen.

In der folgenden Tabelle sind alle sofort einsatzbereiten Formulare und Ansichten nach Entitäten aufgeführt. Sie müssen das neue Feld auch zusätzlichen Formularen oder Ansichten in Ihren benutzerdefinierten Entitäten hinzufügen.

|   Entity        | Formulare   |Ansichten        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollenpreis| Information | – Preise der aktiven Ressourcenkategorie<br> – Zugeordnete Ansicht: Preis der Ressourcenkategorie |
|  Rollenpreisaufschlag| Information| – Aktive Rollenpreisaufschläge<br>– Zugeordnete Ansicht: Rollenpreisaufschlag |
|  Detailinformationen zur Angebotsposition| – Projektinformationen<br>– Projektschnellerfassung| – Details zu aktiver Angebotsposition<br>– Kombinierte Angebotspositionen<br>– Zugeordnete Ansicht: Angebotsposition |
|  Positionsdetail von Projektvertrag| – Projektinformationen<br>– Projektschnellerfassung| – Kombinierte Vertragszeilendetails<br>– Aktive Vertragszeilendetails<br>– Zugeordnete Vertragspositionsdetail |
|  Projektaufgabe| – Information<br>– Neues Formular| &nbsp; |
|  Projektteammitglied| – Information<br>– Neues Formular| – Aktive Projektteammitglieder<br>– Projektteammitglieder<br>– Zugeordnete Projektteammitglieder |
|  Zeiteintrag| – Information<br>– Zeiteintrag erstellen| – Meine Zeiteinträge nach Datum<br>– Meine Zeiteinträge für diese Woche<br>– Zeiteinträge zur Genehmigung|
|  Erfassungsposition| – Information<br>– Schnellerstellung| – Aktive Erfassungspositionen<br>– Zugeordnete Erfassungsposition |
|  Rechnungsposition| – Information<br>– Schnellerstellung| – Aktive Rechnungspositionen<br>– Fakturierbare Rechnungsbuchungen<br>– Kostenlose Rechnungsbuchungen<br>– Zugeordnete Rechnungsposition <br>– Nicht-fakturierbare Rechnungsbuchungen|
|  Tatsächl.| – Information<br>– Aktive tatsächliche Transaktionen| Zugeordnete Tatsächliche Transaktionen |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Einrichten von buchbaren Ressourcen als Preisdimension
Führen Sie zum Einrichten von buchbaren Ressourcen als Preisdimension die folgenden Schritte durch:

1. Gehen Sie zu **Einstellungen** > **Parameter**. 
2. Auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** stellen Sie sicher, dass das Raster in der Registerkarte die Datensätze in der Entität **Preisdimensionen** anzeigt. 
2. Fügen Sie dieser Liste der Preisdimensionen **Buchbare Ressource** als **msdyn_bookableresource** hinzu. 
3. Wählen Sie unter **Gilt für Kosten** und **Gilt für Vertrieb** einen Wert aus.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus. 
5. Wählen Sie die Kosten- und Vertriebspriorität für die buchbare Ressource aus. In der Regel hat eine buchbare Ressource die höchste Priorität, wenn sie als Preisdimension aufgenommen wird. Setzen Sie die Priorität auf **1** (oder **0** abhängig davon, wie Sie die Priorität zählen), um dieses Verhalten sicherzustellen.

## <a name="set-up-pricing-dimension-field-names"></a>Einrichten von Feldnamen für Preisdimensionen

Wenn sich der Feldname einer Preisdimension in der Tabelle **Rollenpreis** von dem Feldnamen in einer der anderen Entitäten unterscheidet, in denen der Standardpreis verwendet wird, muss der Preisdimensionsdatensatz die verschiedenen Namen kennen.  

Bei einer buchbaren Ressource verfügt die Entität **Projektteammitglieder** über einen geringfügig anderen Feldnamen als die Entität **Rollenpreis**: 

 - **Mitglieder des Projektteams** Entität = **msdyn_bookableresourceid**
 - **Rollenpreis** Entität = **msdyn_bookableresource**

Der Preisdimensionsdatensatz **msydn_bookableresource** muss diesen Unterschied kennen.

1. Doppelklicken Sie auf die Zeile im Raster **Preisdimensionen**, um die Dimensionsseite von **msdyn_bookableresource** zu öffnen.
2. Klicken Sie auf der Dimensionsseite auf der Registerkarte **Verknüpft** auf **Preisdimensions-Feldnamen**.

  ![Registerkarte „Preisdimensions-Feldnamen”](media/PD-fieldname.png)

3. Klicken Sie in der angezeigten Ansicht auf **Neuen Preisdimensions-Feldnamen hinzufügen**.

  ![Neue Preisdimensions-Feldnamen hinzufügen](media/Add-NewPD-fieldname.png)

  Dadurch wird die Seite **Neuer Preisdimensions-Feldnamen** für **msdyn_bookableresource** geöffnet. 

4. Auf der **Neuen Preisdimensions-Feldnamen hinzufügen**-Seite fügen Sie **msdyn_projectteam** zu **Logischer Name der Entität** hinzu.
5. Fügen Sie **msdyn_bookableresourceid** zu **Feldname** hinzu.

 ![Formular „Neuer Preisdimensions-Feldname”](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]