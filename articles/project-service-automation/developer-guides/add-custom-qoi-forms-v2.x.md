---
title: Hinzufügen neuer Formulare der benutzerdefinierten Entität (Project Service Automation 2.x)
description: In diesem Thema finden Sie Informationen zum Hinzufügen von Formularen der benutzerdefinierten Entität für Verkaufschancen, Angebote, Aufträge bzw. Rechnungen in Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721881"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="32544-103">Hinzufügen neuer Formulare der benutzerdefinierten Entität (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="32544-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="32544-104">Feld „Typ”</span><span class="sxs-lookup"><span data-stu-id="32544-104">Type field</span></span> 

<span data-ttu-id="32544-105">Dynamics 365 Project Service Automation verwendet das Feld **Typ** (**msdyn\_ordertype**) der Entitäten „Verkaufschance”, „Angebot”, „Bestellung” und „Rechnung”, um **arbeitsbasierte** Versionen dieser Entitäten von **elementbasierten** und **dienstbasierten** Versionen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="32544-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="32544-106">Arbeitsbasierte Versionen dieser Entitäten werden von PSA verwaltet.</span><span class="sxs-lookup"><span data-stu-id="32544-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="32544-107">Viele Geschäftslogiken auf der Kunden- und Serverseite der Lösung hängen vom Feld **Typ** ab.</span><span class="sxs-lookup"><span data-stu-id="32544-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="32544-108">Daher ist es wichtig, dass das Feld beim Erstellen der Entitäten mit einem korrekten Wert initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="32544-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="32544-109">Ein falscher Wert kann zu falschem Verhalten führen, und einige Geschäftslogiken werden möglicherweise nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32544-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="32544-110">Automatischer Formularwechsel</span><span class="sxs-lookup"><span data-stu-id="32544-110">Automatic form switching</span></span>

<span data-ttu-id="32544-111">Um mögliche Datenverfälschungen und unerwartete Verhaltensweisen zu vermeiden, die durch eine fehlerhafte Initialisierung und Bearbeitung der Verkaufsentitätsdatensätze verursacht werden, enthält PSA jetzt eine Logik für den automatischen Formularwechsel in Standardformularen.</span><span class="sxs-lookup"><span data-stu-id="32544-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="32544-112">Diese Logik führt den Benutzer zum richtigen Formular für die Arbeit mit der arbeitsbasierten Version oder einem anderen Typ der Entitäten Verkaufschance, Angebot, Bestellung oder Rechnung.</span><span class="sxs-lookup"><span data-stu-id="32544-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="32544-113">Wenn ein Benutzer die arbeitsbasierte Version einer Verkaufschancen-, Angebots-, Bestellungs- bzw. Rechnungsentität öffnet, wird zum Formular **Projektinformationen** gewechselt.</span><span class="sxs-lookup"><span data-stu-id="32544-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="32544-114">Die automatische Formularwechsellogik basiert auf der Zuordnung zwischen dem Wert **formId** und dem Feld **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="32544-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="32544-115">Alle Standardformulare wurden zu dieser Zuordnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="32544-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="32544-116">Benutzerdefinierte Formulare müssen jedoch manuell hinzugefügt werden, um anzugeben, welche Version der Entität verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32544-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="32544-117">Dies basiert auf dem Feld **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="32544-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="32544-118">Wenn der Formularwechsel in der Zuordnung fehlt, wechselt die Logik auf der Grundlage des Werts, der im Feld **msdyn\_ordertype** der Entität gespeichert ist, zum Standardformular.</span><span class="sxs-lookup"><span data-stu-id="32544-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="32544-119">Hinzufügen benutzerdefinierter Formulare und Aktivieren der Formularwechsellogik</span><span class="sxs-lookup"><span data-stu-id="32544-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="32544-120">Das folgende Beispiel zeigt, wie ein benutzerdefiniertes Formular namens **Meine Projektinformationen** hinzugefügt wird, damit es mit arbeitsbasierten Verkaufschancen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="32544-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="32544-121">Mit demselben Verfahren werden benutzerdefinierte Formulare hinzugefügt, um mit Angeboten, Bestellungen und Rechnungen zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="32544-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="32544-122">Gehen Sie folgendermaßen vor, um eine benutzerdefinierte Version des Formulars **Projektinformationen** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="32544-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="32544-123">Öffnen Sie in der Entität „Verkaufschance” das Formular **Projektinformationen** und speichern Sie eine Kopie mit dem Namen **Meine Projektinformationen**.</span><span class="sxs-lookup"><span data-stu-id="32544-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="32544-124">Öffnen Sie das neue Formular, und stellen Sie dann in den Eigenschaften sicher, dass die Formularinitialisierungsskripten aus dem Formular **Projektinformationen** vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="32544-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="32544-125">Entfernen Sie die Skripte nicht.</span><span class="sxs-lookup"><span data-stu-id="32544-125">Don't remove the scripts.</span></span> <span data-ttu-id="32544-126">Andernfalls werden einige Daten möglicherweise nicht ordnungsgemäß initialisiert.</span><span class="sxs-lookup"><span data-stu-id="32544-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="32544-127">Überprüfen Sie, ob das Feld **Typ** (**msdyn\_ordertype**) im Formular vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="32544-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="32544-128">Entfernen Sie dieses Feld nicht.</span><span class="sxs-lookup"><span data-stu-id="32544-128">Don't remove this field.</span></span> <span data-ttu-id="32544-129">Andernfalls schlagen die Initialisierungsskripten fehl.</span><span class="sxs-lookup"><span data-stu-id="32544-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="32544-130">Suchen Sie auf dem neuen Formular den Wert **formId**.</span><span class="sxs-lookup"><span data-stu-id="32544-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="32544-131">Sie können diesen Schritt auf zwei Arten ausführen:</span><span class="sxs-lookup"><span data-stu-id="32544-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="32544-132">Exportieren Sie das Formular **Meine Projektinformationen** als Teil einer nicht verwalteten Lösung, und suchen Sie dann den Wert **formId** in der Datei customization.xml der exportierten Lösung.</span><span class="sxs-lookup"><span data-stu-id="32544-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="32544-133">Öffnen Sie das Formular **Meine Projektinformationen** im Formular-Editor, und suchen Sie dann den Globally Unique Identifier (GUID) neben dem Parameter **fromId** in der URL, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="32544-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Der Wert „formID” des neuen Formulars in der URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="32544-135">Erstellen Sie eine Zuordnung **msdyn\_ordertype** für den Wert **formId**, indem Sie die Webressource msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="32544-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="32544-136">Entfernen Sie den Code aus der Ressource und ersetzen Sie ihn durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="32544-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="32544-137">Speichern und veröffentlichen Sie dann die Anpassungen.</span><span class="sxs-lookup"><span data-stu-id="32544-137">Save and then publish the customizations.</span></span>
