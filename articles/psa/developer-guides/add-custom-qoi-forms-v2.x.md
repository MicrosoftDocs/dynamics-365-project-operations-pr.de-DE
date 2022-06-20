---
title: Hinzufügen neuer Formulare der benutzerdefinierten Entität (Project Service Automation 2.x)
description: Dieser Artikel beschreibt, wie Sie angepasste Formulare für Entitäten für Verkaufschancen, Angebote, Aufträge oder Rechnungen in Dynamics 365 Project Service Automation 2.x hinzufügen können.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922727"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Hinzufügen neuer Formulare der benutzerdefinierten Entität (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Feld „Typ“ 

Dynamics 365 Project Service Automation verwendet das Feld **Typ** (**msdyn\_ordertype**) der Entitäten „Verkaufschance“, „Angebot“, „Bestellung“ und „Rechnung“, um **arbeitsbasierte** Versionen dieser Entitäten von **elementbasierten** und **dienstbasierten** Versionen zu unterscheiden. Arbeitsbasierte Versionen dieser Entitäten werden von PSA verwaltet. Viele Geschäftslogiken auf der Kunden- und Serverseite der Lösung hängen vom Feld **Typ** ab. Daher ist es wichtig, dass das Feld beim Erstellen der Entitäten mit einem korrekten Wert initialisiert wird. Ein falscher Wert kann zu falschem Verhalten führen, und einige Geschäftslogiken werden möglicherweise nicht ordnungsgemäß ausgeführt.

## <a name="automatic-form-switching"></a>Automatischer Formularwechsel

Um mögliche Datenverfälschungen und unerwartete Verhaltensweisen zu vermeiden, die durch eine fehlerhafte Initialisierung und Bearbeitung der Verkaufsentitätsdatensätze verursacht werden, enthält PSA jetzt eine Logik für den automatischen Formularwechsel in Standardformularen. Diese Logik führt den Benutzer zum richtigen Formular für die Arbeit mit der arbeitsbasierten Version oder einem anderen Typ der Entitäten Verkaufschance, Angebot, Bestellung oder Rechnung. Wenn ein Benutzer die arbeitsbasierte Version einer Verkaufschancen-, Angebots-, Bestellungs- bzw. Rechnungsentität öffnet, wird zum Formular **Projektinformationen** gewechselt.

Die automatische Formularwechsellogik basiert auf der Zuordnung zwischen dem Wert **formId** und dem Feld **msdyn\_ordertype**. Alle Standardformulare wurden zu dieser Zuordnung hinzugefügt. Benutzerdefinierte Formulare müssen jedoch manuell hinzugefügt werden, um anzugeben, welche Version der Entität verarbeitet werden soll. Dies basiert auf dem Feld **msdyn\_ordertype**. Wenn der Formularwechsel in der Zuordnung fehlt, wechselt die Logik auf der Grundlage des Werts, der im Feld **msdyn\_ordertype** der Entität gespeichert ist, zum Standardformular.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Hinzufügen benutzerdefinierter Formulare und Aktivieren der Formularwechsellogik

Das folgende Beispiel zeigt, wie ein benutzerdefiniertes Formular namens **Meine Projektinformationen** hinzugefügt wird, damit es mit arbeitsbasierten Verkaufschancen funktioniert. Mit demselben Verfahren werden benutzerdefinierte Formulare hinzugefügt, um mit Angeboten, Bestellungen und Rechnungen zu funktionieren.

Gehen Sie folgendermaßen vor, um eine benutzerdefinierte Version des Formulars **Projektinformationen** zu erstellen.

1. Öffnen Sie in der Entität „Verkaufschance“ das Formular **Projektinformationen** und speichern Sie eine Kopie mit dem Namen **Meine Projektinformationen**.
2. Öffnen Sie das neue Formular, und stellen Sie dann in den Eigenschaften sicher, dass die Formularinitialisierungsskripten aus dem Formular **Projektinformationen** vorhanden sind. 

    > [!IMPORTANT]
    > Entfernen Sie die Skripte nicht. Andernfalls werden einige Daten möglicherweise nicht ordnungsgemäß initialisiert.

3. Überprüfen Sie, ob das Feld **Typ** (**msdyn\_ordertype**) im Formular vorhanden ist. 

    > [!IMPORTANT]
    > Entfernen Sie dieses Feld nicht. Andernfalls schlagen die Initialisierungsskripten fehl.

4. Suchen Sie auf dem neuen Formular den Wert **formId**. Sie können diesen Schritt auf zwei Arten ausführen:

    - Exportieren Sie das Formular **Meine Projektinformationen** als Teil einer nicht verwalteten Lösung, und suchen Sie dann den Wert **formId** in der Datei customization.xml der exportierten Lösung.
    - Öffnen Sie das Formular **Meine Projektinformationen** im Formular-Editor, und suchen Sie dann den Globally Unique Identifier (GUID) neben dem Parameter **fromId** in der URL, wie in der folgenden Abbildung gezeigt.

    ![Der Wert „formID“ des neuen Formulars in der URL.](media/how-to-add-custom-forms-in-v2.0.png)

5. Erstellen Sie eine Zuordnung **msdyn\_ordertype** für den Wert **formId**, indem Sie die Webressource msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js bearbeiten. Entfernen Sie den Code aus der Ressource und ersetzen Sie ihn durch den folgenden Code.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Speichern und veröffentlichen Sie dann die Anpassungen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
