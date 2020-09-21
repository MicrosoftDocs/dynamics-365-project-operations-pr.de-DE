---
title: Wie passe ich den Projektphasegeschäftsprozessfluss an?
description: Eine Übersicht darüber, wie Sie den Projektphasen-Geschäftsprozessfluss anpassen.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721935"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="607f4-103">Wie passe ich den Projektphasegeschäftsprozessfluss an?</span><span class="sxs-lookup"><span data-stu-id="607f4-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="607f4-104">Es gibt eine bekannte Beschränkung bei älteren Versionen der Project Service Anwendung, dass die Namen der Phasen im Projektphasegeschäftsprozessfluss den erwarteten englischen Namen (**Quote**, **Plan**, **Close**) übereinstimmen müssen.</span><span class="sxs-lookup"><span data-stu-id="607f4-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="607f4-105">Andernfalls kann die Geschäftslogik, die von englischen Phasennamen abhängig ist, nicht wie erwartet arbeiten.</span><span class="sxs-lookup"><span data-stu-id="607f4-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="607f4-106">Daher sehen Sie keine bekannten Aktionen wie **Prozess wechseln** oder **Prozess bearbeiten**, die auf dem Projektformular verfügbar sind und das Anpassen vom Geschäftsprozessfluss wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="607f4-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="607f4-107">Diese Beschränkung ist in Version 2.4.5.48 und später behoben worden.</span><span class="sxs-lookup"><span data-stu-id="607f4-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="607f4-108">Dieser Artikel enthält nützliche vorgeschlagene Problemumgehungen von älteren Versionen, wenn Sie den Standardgeschäftsprozessfluss von früheren Versionen anpassen müssen.</span><span class="sxs-lookup"><span data-stu-id="607f4-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="607f4-109">Geschäftslokig erfordert einen genaue Übereinstimmung mit englischen Phasennamen</span><span class="sxs-lookup"><span data-stu-id="607f4-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="607f4-110">Der Projektphasengeschäftsprozessfluss enthält Geschäftslogik, die das folgende Verhalten in der App auslöst:</span><span class="sxs-lookup"><span data-stu-id="607f4-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="607f4-111">Wenn das Projekt in einem Angebot zugeordnet sind, setzt der Codesatz den Geschäftsprozessfluss der Phase auf **Quote**.</span><span class="sxs-lookup"><span data-stu-id="607f4-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="607f4-112">Wenn das Projekt in einem Vertrag zugeordnet sind, setzt der Codesatz den Geschäftsprozessfluss der Phase auf **Plan**.</span><span class="sxs-lookup"><span data-stu-id="607f4-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="607f4-113">Wenn der Geschäftsprozessfluss zur **Close** Phase wechselt, wird der Projektdatensatz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="607f4-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="607f4-114">Wenn das Projekt deaktiviert wird, sind das Projektformular und der Projektstrukturplan (WBS) als schreibgeschützt festgeleg, die Ressourcenanmeldungen freigegeben, und alle zugeordneten Preislisten werden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="607f4-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="607f4-115">Diese Geschäftslogik vertraut auf die englischen Namen für die Projektphasen.</span><span class="sxs-lookup"><span data-stu-id="607f4-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="607f4-116">Diese Abhängigkeit von den englischen Phasennamen ist der Hauptgrund, weshalb Anpassung des Projektphasegeschäftsprozessflusses nicht empfohlen ist und warum Sie die allgemeinen Geschäftsprozessflussaktionen **Prozess wechseln** oder auf der **Prozess bearbeiten** finden.</span><span class="sxs-lookup"><span data-stu-id="607f4-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="607f4-117">Was geschieht, wenn die Phasennamen nicht den englischen Namen entsprechen?</span><span class="sxs-lookup"><span data-stu-id="607f4-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="607f4-118">In der Project Service-App-Version 1.x in der Plattform 8,2, wenn die Phasennamen im Geschäftsprozessfluss nicht mit den englischen Phasennamen übereinstimmen, wird die Geschäftslogik, die die richtige Darstellung für Angebote oder Verträge im Hintergrund ausführt bzw. das Projekt übersprungen, enthält.</span><span class="sxs-lookup"><span data-stu-id="607f4-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="607f4-119">Es werden keine Fehlermeldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="607f4-119">No error messages are displayed.</span></span> <span data-ttu-id="607f4-120">Daher scheint es, dass Sie in der Lage sind, den Projektphasegeschäftsprozessfluss anzupassen.</span><span class="sxs-lookup"><span data-stu-id="607f4-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="607f4-121">Allerdings finden Sie die automatischen Prozesse, die nicht für Angebote, Verträge und Projektabschluß arbeiten.</span><span class="sxs-lookup"><span data-stu-id="607f4-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="607f4-122">In der Project Service-App-Version 2.4.4.30 oder älter in der Plattform 9,0 gibt es eine bedeutende Architekturänderung in den Geschäftsprozessflüssen, die eine Neufassung der Geschäftsprozessflussgeschäftslogik erforderlich machen.</span><span class="sxs-lookup"><span data-stu-id="607f4-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="607f4-123">Daher wenn die Prozessbühnennamen nicht mit den erwarteten englischen Namen übereinstimmen, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="607f4-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="607f4-124">Wenn Sie den Projektphasegeschäftsprozessfluss für die Projektentität anpassen möchten, können Sie neue Phasen für den Standardgeschäftsprozessfluss für die nur Projektentität hinzufügen, und **Quote**, **Plan**und **Close** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="607f4-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="607f4-125">Diese Einschränkung stellt sicher, dass Sie keine Fehler in der Geschäftslogik haben, die nicht Ihren Vorstellungen entspricht und dass die englischen Phasennamen im Geschäftsprozessfluss erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="607f4-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="607f4-126">In Version 2.4.5.48 oder später wurde die Geschäftslogik, die in diesem Artikel beschriebenen ist, vom vom Standardgeschäftsprozessfluss für die Projektentität entfernt.</span><span class="sxs-lookup"><span data-stu-id="607f4-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="607f4-127">Upgraden auf dieser Version oder auf eine höhere macht es möglich, dass Sie den Standardgeschäftsprozessfluss durch gültige Werte aus Ihren Benutzern anzupassen oder ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="607f4-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="607f4-128">Problemumgehung für frühere Versionen:</span><span class="sxs-lookup"><span data-stu-id="607f4-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="607f4-129">Wenn Aktualisieren keine Option ist, können Sie den Projektphasegeschäftsprozessfluss für die Projektentität in einer der beiden folgenden Methoden anpassen:</span><span class="sxs-lookup"><span data-stu-id="607f4-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="607f4-130">Hinzufügen von zusätzlichen Phasen der Standardkonfiguration, unter Beibehaltung der englischen Phasenamen für, **Quote** und **Plan** und **Close**</span><span class="sxs-lookup"><span data-stu-id="607f4-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-131">![Screenshot des Hinzufügens von Phasen der Standard konfiguration](media/FAQ-Customize-BPF-1.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-131">![Screenshot of adding stages to default configuration](media/FAQ-Customize-BPF-1.png)</span></span>
 
2. <span data-ttu-id="607f4-132">Erstellen Sie einen eigenen Geschäftsprozessfluss und erstellen Sie den primären Geschäftsprozessfluss für die Projektentität, mit der Sie alle Phasennamen haben, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="607f4-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="607f4-133">Wenn Sie dieselben Standardprojektphasen **Quote**, **Plan** und **Close** verwenden möchten, müssen Sie einige Schritte anpassen, die die benutzerdefinierten Phasennamen treiben werden.</span><span class="sxs-lookup"><span data-stu-id="607f4-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="607f4-134">Je komplexer die Logik im Schließen des Projektumfangs ist, den Sie immer noch auslösen können durch Deaktivieren des Projektdatensatzes.</span><span class="sxs-lookup"><span data-stu-id="607f4-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-135">![Screebsgit der BPF-Anpassung](media/FAQ-Customize-BPF-2.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-135">![Screenshot of BPF customization](media/FAQ-Customize-BPF-2.png)</span></span>

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="607f4-136">Zusätzliche Überlegungen für Project Service-App-Version 2.4.4.30 oder älter auf und 9,0</span><span class="sxs-lookup"><span data-stu-id="607f4-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="607f4-137">Im Project Service 2.4.4.30 oder älter auf Plattform 9.0 mit einem benutzerdefinierten Geschäftsprozessfluss mit dem Feld **Phasenname** auf der Projektentität, die im Diagramm **Projekt nach Phase** und der Projektlistenansicht verwendet werden, werden die Ansichten nicht aktualisiert, weil es mit de Standard-Projektphasen mit dem Geschäftsprozessfluss verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="607f4-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="607f4-138">Sie können dieses Problem mit folgenden Schritte adressieren:</span><span class="sxs-lookup"><span data-stu-id="607f4-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="607f4-139">Hinzufügen eines benutzerdefinierten Felds, dass die aktuelle Geschäftsprozessflussphase erfasst, die aktualisiert wird, wenn der Benutzer über benutzerdefinierte Geschäftsprozessfluss wechselt.</span><span class="sxs-lookup"><span data-stu-id="607f4-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="607f4-140">Diagramm **Projekt nach Phase** ändern, um mit dem benutzerdefinierten Feld anstelle der Standardkonfiguration zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="607f4-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="607f4-141">Schritte, um den eigenen Geschäftsprozessflusses für die Projektentität zu erstellen</span><span class="sxs-lookup"><span data-stu-id="607f4-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="607f4-142">Um den eigenen Geschäftsprozessflusses für die Projektentität zu erstellen, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="607f4-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="607f4-143">Gehen Sie zu **Einstellungen** > **Prozesscenter**.</span><span class="sxs-lookup"><span data-stu-id="607f4-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="607f4-144">Kopieren Sie nicht den Projektphasegeschäftsprozessfluss, da dies auch die Project Service-Geschäftslogik kopiert.</span><span class="sxs-lookup"><span data-stu-id="607f4-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-145">![Screebsgit der BPF-Anpassung](media/FAQ-Customize-BPF-3.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-145">![Screenshot of BPF customization](media/FAQ-Customize-BPF-3.png)</span></span>

2. <span data-ttu-id="607f4-146">Verwenden Sie den Prozessdesigner, um die Bühnennamen zu erstellen, die angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="607f4-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="607f4-147">Wenn Sie die gleichen Funktionen wie die Standardphasen für **Quote**, **Plan** und **Close** wünschen, müssen Sie das anhand der Phasennamen des benutzerdefinierten Geschäftsprozessflusses erstellen.</span><span class="sxs-lookup"><span data-stu-id="607f4-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-148">![Screenshot des Prozessdesigners wird verwendet, um BPF anzupassen](media/FAQ-Customize-BPF-4.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-148">![Screenshot of Process Designer used to customize BPF](media/FAQ-Customize-BPF-4.png)</span></span> 

3. <span data-ttu-id="607f4-149">Im Prozessdesigner klicken sie auf **Auftragsprozessfluss**, um die benutzerdefinierten Geschäftsprozessflusse des primären Geschäftsprozessflusses für die Projektentität zu machen, indem Sie den Projektphasegeschäftsprozessfluss an den Anfang der Liste verschieben.</span><span class="sxs-lookup"><span data-stu-id="607f4-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-150">![Screenshot der Verwendung des Bestellvorgang-Prozessflusses](media/FAQ-Customize-BPF-5-720.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-150">![Screenshot of using Order Process Flow](media/FAQ-Customize-BPF-5-720.png)</span></span>

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="607f4-151">Folgende Schritte gelten für die Project Service App 2.4.4.30 oder älter in der Plattform 9.0</span><span class="sxs-lookup"><span data-stu-id="607f4-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="607f4-152">Hinzufügen eines neuen benutzerdefinierten Feld der Projektentität, um die benutzerdefinierten Phasen im angepassten Geschäftsprozessfluss aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="607f4-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="607f4-153">Sie müssen die Geschäftslogik (Plug-In/Workflow) hinzufügen, um das Feld zu aktualisieren, wenn die aktuelle Phase im angepassten Geschäftsprozessfluss aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="607f4-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-154">![Screenshot zum Anpassen der Projektentität](media/FAQ-Customize-BPF-6-720.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-154">![Screenshot of customizing Project entity](media/FAQ-Customize-BPF-6-720.png)</span></span>

5. <span data-ttu-id="607f4-155">**Projekt nach Phase** Ändern Sie das Diagramm, um Ihr neues benutzerdefiniertes Feld für Phasen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="607f4-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-156">![Screenshot des Projektumfangs der Anwendung durch Phasendiagramm](media/FAQ-Customize-BPF-7-720.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-156">![Screenshot of using the Project By Stage chart](media/FAQ-Customize-BPF-7-720.png)</span></span>

6. <span data-ttu-id="607f4-157">Ändern Sie alle Ansichten, damit die Projektentität Ihr neues benutzerdefiniertes Feld für Phasen können.</span><span class="sxs-lookup"><span data-stu-id="607f4-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="607f4-158">![Screenshot der Änderung von Ansichten auf der Projektentität](media/FAQ-Customize-BPF-8-720.png)</span><span class="sxs-lookup"><span data-stu-id="607f4-158">![Screenshot of modifying views on the Project entity](media/FAQ-Customize-BPF-8-720.png)</span></span>

