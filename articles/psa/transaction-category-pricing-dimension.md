---
title: Verwenden von Transaktionskategorie als Preisdimension
description: Dieser Artikel enthält Informationen über die Verwendung einer Transaktionskategorie als Preisdimension.
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
ms.openlocfilehash: 1a1c2dc17c2092e5364d90e7efc1f13aee80703e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915735"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Verwenden von Transaktionskategorie als Preisdimension

[!include [banner](../includes/psa-now-project-operations.md)]

Dieser Artikel zeigt Ihnen, wie Sie eine Transaktionskategorie als Dimension für die Preisgestaltung verwenden können. Bevor Sie beginnen, falls Sie noch keine Preisdimensionslösung erstellt haben, müssen Sie eine neue erstellen. Wenn Sie bereits eine Preisdimensionslösung haben, dann können Sie Ihre Änderungen in dieser Lösung vornehmen. Wenn Sie noch keine neue Lösung für Preisdimensionen in Ihrem Unternehmen erstellt haben, führen Sie die Verfahren im Artikel [Angepasste Felder und Entitäten erstellen](create-custom-fields-entities.md) aus.

## <a name="add-transaction-category-to-forms-and-views"></a>Transaktionskategorie zu Formularen und Ansichten hinzufügen
Um die Transaktionskategorie in der Benutzeroberfläche in der Preisdimensionslösung sichtbar zu machen, müssen Sie alle Formulare und Ansichten der Schlüsselentitäten durchgehen und diese Felder zu den Formularen und Ansichten dieser Entitäten hinzufügen.
Die folgende Tabelle ist eine umfassende Liste der vorkonfigurierten Formulare und Ansichten, aufgelistete nach Entität, die mit den neuen Feldern aktualisiert werden müssen. Wenn es irgendwelche zusätzlichen Ansichten oder Formulare in Ihren Anpassungen für diese Entitäten gibt, fügen Sie diesen die neuen Felder ebenfalls hinzu.

|  Entität        | Formulare     |Ansichten        |
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

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Transaktionskategorie als Preisdimension einrichten

1. In der Weboberfläche wechseln Sie zu **Project Service** > **Einstellungen** > **Parameter**. 
2. Auf der Seite **Parameter** in der Registerkarte **Betragsbasierte Preisdimensionen** beachten Sie, dass das Raster in der Registerkarte die Datensätze in der Entität **Preisdimensionen** anzeigt.
3. Fügen Sie **Transaktionskategorie** zu dieser Liste hinzu, und legen Sie die Felder **Gilt für Kosten** und **Gilt für Vertrieb** auf **Ja** fest.
4. Wählen Sie im Feld **Dimensionstyp** die Option **Betragsbasiert** aus, und wählen Sie anschließend die Priorität für **Transaktionskategorie** in Bezug auf Kosten und Vertrieb fest.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
