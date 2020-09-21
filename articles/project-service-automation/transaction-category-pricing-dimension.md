---
title: Verwenden von Transaktionskategorie als Preisdimension
description: Dieses Thema bietet Informationen über das Verwenden einer Transaktionskategorie als Preisdimension.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722043"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Verwenden von Transaktionskategorie als Preisdimension
Dieses Thema zeigt, wie eine Transaktionskategorie als Preisdimension verwendet wird. Bevor Sie beginnen, falls Sie noch keine Preisdimensionslösung erstellt haben, müssen Sie eine neue erstellen. Wenn Sie bereits eine Preisdimensionslösung haben, dann können Sie Ihre Änderungen in dieser Lösung vornehmen. Wenn Sie keine neue Preisdimensionslösung für Ihre Organisation erstellt haben, führen Sie die Prozeduren im Thema [Erstellen benutzerdefinierter Felder und Entitäten](create-custom-fields-entities.md) durch.

## <a name="add-transaction-category-to-forms-and-views"></a>Transaktionskategorie zu Formularen und Ansichten hinzufügen
Um die Transaktionskategorie in der Benutzeroberfläche in der Preisdimensionslösung sichtbar zu machen, müssen Sie alle Formulare und Ansichten der Schlüsselentitäten durchgehen und diese Felder zu den Formularen und Ansichten dieser Entitäten hinzufügen.
Die folgende Tabelle ist eine umfassende Liste der vorkonfigurierten Formulare und Ansichten, aufgelistete nach Entität, die mit den neuen Feldern aktualisiert werden müssen. Wenn es irgendwelche zusätzlichen Ansichten oder Formulare in Ihren Anpassungen für diese Entitäten gibt, fügen Sie diesen die neuen Felder ebenfalls hinzu.

|  Entität        | Formulare     |Ansichten        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Transaktionskategorie als Preisdimension einrichten

1. In der Weboberfläche wechseln Sie zu **Project Service** > **Einstellungen** > **Parameter**. 
2. Auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** beachten Sie, dass das Raster in der Registerkarte die Datensätze in der Entität **Preisdimensionen** anzeigt.
3. Fügen Sie **Transaktionskategorie** zu dieser Liste hinzu, und legen Sie die Felder **Gilt für Kosten** und **Gilt für Vertrieb** auf **Ja** fest.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus, und wählen Sie anschließend die Priorität für **Transaktionskategorie** in Bezug auf Kosten und Vertrieb fest.
