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
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Wie passe ich den Projektphasegeschäftsprozessfluss an?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Es gibt eine bekannte Beschränkung bei älteren Versionen der Project Service Anwendung, dass die Namen der Phasen im Projektphasegeschäftsprozessfluss den erwarteten englischen Namen (**Quote**, **Plan**, **Close**) übereinstimmen müssen. Andernfalls kann die Geschäftslogik, die von englischen Phasennamen abhängig ist, nicht wie erwartet arbeiten. Daher sehen Sie keine bekannten Aktionen wie **Prozess wechseln** oder **Prozess bearbeiten**, die auf dem Projektformular verfügbar sind und das Anpassen vom Geschäftsprozessfluss wird nicht empfohlen. 

Diese Beschränkung ist in Version 2.4.5.48 und später behoben worden. Dieser Artikel enthält nützliche vorgeschlagene Problemumgehungen von älteren Versionen, wenn Sie den Standardgeschäftsprozessfluss von früheren Versionen anpassen müssen.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Geschäftslokig erfordert einen genaue Übereinstimmung mit englischen Phasennamen

Der Projektphasengeschäftsprozessfluss enthält Geschäftslogik, die das folgende Verhalten in der App auslöst:
- Wenn das Projekt in einem Angebot zugeordnet sind, setzt der Codesatz den Geschäftsprozessfluss der Phase auf **Quote**.
- Wenn das Projekt in einem Vertrag zugeordnet sind, setzt der Codesatz den Geschäftsprozessfluss der Phase auf **Plan**.
- Wenn der Geschäftsprozessfluss zur **Close** Phase wechselt, wird der Projektdatensatz deaktiviert. Wenn das Projekt deaktiviert wird, sind das Projektformular und der Projektstrukturplan (WBS) als schreibgeschützt festgeleg, die Ressourcenanmeldungen freigegeben, und alle zugeordneten Preislisten werden deaktiviert.

Diese Geschäftslogik vertraut auf die englischen Namen für die Projektphasen. Diese Abhängigkeit von den englischen Phasennamen ist der Hauptgrund, weshalb Anpassung des Projektphasegeschäftsprozessflusses nicht empfohlen ist und warum Sie die allgemeinen Geschäftsprozessflussaktionen **Prozess wechseln** oder auf der **Prozess bearbeiten** finden.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Was geschieht, wenn die Phasennamen nicht den englischen Namen entsprechen?

In der Project Service-App-Version 1.x in der Plattform 8,2, wenn die Phasennamen im Geschäftsprozessfluss nicht mit den englischen Phasennamen übereinstimmen, wird die Geschäftslogik, die die richtige Darstellung für Angebote oder Verträge im Hintergrund ausführt bzw. das Projekt übersprungen, enthält. Es werden keine Fehlermeldungen angezeigt. Daher scheint es, dass Sie in der Lage sind, den Projektphasegeschäftsprozessfluss anzupassen. Allerdings finden Sie die automatischen Prozesse, die nicht für Angebote, Verträge und Projektabschluß arbeiten.

In der Project Service-App-Version 2.4.4.30 oder älter in der Plattform 9,0 gibt es eine bedeutende Architekturänderung in den Geschäftsprozessflüssen, die eine Neufassung der Geschäftsprozessflussgeschäftslogik erforderlich machen. Daher wenn die Prozessbühnennamen nicht mit den erwarteten englischen Namen übereinstimmen, wird eine Fehlermeldung angezeigt. 

Wenn Sie den Projektphasegeschäftsprozessfluss für die Projektentität anpassen möchten, können Sie neue Phasen für den Standardgeschäftsprozessfluss für die nur Projektentität hinzufügen, und **Quote**, **Plan**und **Close** beibehalten. Diese Einschränkung stellt sicher, dass Sie keine Fehler in der Geschäftslogik haben, die nicht Ihren Vorstellungen entspricht und dass die englischen Phasennamen im Geschäftsprozessfluss erwartet werden.

In Version 2.4.5.48 oder später wurde die Geschäftslogik, die in diesem Artikel beschriebenen ist, vom vom Standardgeschäftsprozessfluss für die Projektentität entfernt. Upgraden auf dieser Version oder auf eine höhere macht es möglich, dass Sie den Standardgeschäftsprozessfluss durch gültige Werte aus Ihren Benutzern anzupassen oder ersetzen können. 

## <a name="workarounds-for-earlier-versions"></a>Problemumgehung für frühere Versionen:

Wenn Aktualisieren keine Option ist, können Sie den Projektphasegeschäftsprozessfluss für die Projektentität in einer der beiden folgenden Methoden anpassen:

1. Hinzufügen von zusätzlichen Phasen der Standardkonfiguration, unter Beibehaltung der englischen Phasenamen für, **Quote** und **Plan** und **Close**

   > [!div class="mx-imgBorder"] 
   > ![Screenshot des Hinzufügens von Phasen der Standard konfiguration](media/FAQ-Customize-BPF-1.png)
 
2. Erstellen Sie einen eigenen Geschäftsprozessfluss und erstellen Sie den primären Geschäftsprozessfluss für die Projektentität, mit der Sie alle Phasennamen haben, die Sie verwenden möchten. Wenn Sie dieselben Standardprojektphasen **Quote**, **Plan** und **Close** verwenden möchten, müssen Sie einige Schritte anpassen, die die benutzerdefinierten Phasennamen treiben werden. Je komplexer die Logik im Schließen des Projektumfangs ist, den Sie immer noch auslösen können durch Deaktivieren des Projektdatensatzes.

   > [!div class="mx-imgBorder"] 
   > ![Screebsgit der BPF-Anpassung](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Zusätzliche Überlegungen für Project Service-App-Version 2.4.4.30 oder älter auf und 9,0

Im Project Service 2.4.4.30 oder älter auf Plattform 9.0 mit einem benutzerdefinierten Geschäftsprozessfluss mit dem Feld **Phasenname** auf der Projektentität, die im Diagramm **Projekt nach Phase** und der Projektlistenansicht verwendet werden, werden die Ansichten nicht aktualisiert, weil es mit de Standard-Projektphasen mit dem Geschäftsprozessfluss verknüpft ist. Sie können dieses Problem mit folgenden Schritte adressieren:

- Hinzufügen eines benutzerdefinierten Felds, dass die aktuelle Geschäftsprozessflussphase erfasst, die aktualisiert wird, wenn der Benutzer über benutzerdefinierte Geschäftsprozessfluss wechselt.

- Diagramm **Projekt nach Phase** ändern, um mit dem benutzerdefinierten Feld anstelle der Standardkonfiguration zu arbeiten.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Schritte, um den eigenen Geschäftsprozessflusses für die Projektentität zu erstellen

Um den eigenen Geschäftsprozessflusses für die Projektentität zu erstellen, gehen Sie wie folgt vor:

1. Gehen Sie zu **Einstellungen** > **Prozesscenter**. Kopieren Sie nicht den Projektphasegeschäftsprozessfluss, da dies auch die Project Service-Geschäftslogik kopiert.

   > [!div class="mx-imgBorder"] 
   > ![Screebsgit der BPF-Anpassung](media/FAQ-Customize-BPF-3.png)

2. Verwenden Sie den Prozessdesigner, um die Bühnennamen zu erstellen, die angezeigt werden sollen. Wenn Sie die gleichen Funktionen wie die Standardphasen für **Quote**, **Plan** und **Close** wünschen, müssen Sie das anhand der Phasennamen des benutzerdefinierten Geschäftsprozessflusses erstellen.

   > [!div class="mx-imgBorder"] 
   > ![Screenshot des Prozessdesigners wird verwendet, um BPF anzupassen](media/FAQ-Customize-BPF-4.png) 

3. Im Prozessdesigner klicken sie auf **Auftragsprozessfluss**, um die benutzerdefinierten Geschäftsprozessflusse des primären Geschäftsprozessflusses für die Projektentität zu machen, indem Sie den Projektphasegeschäftsprozessfluss an den Anfang der Liste verschieben.

   > [!div class="mx-imgBorder"] 
   > ![Screenshot der Verwendung des Bestellvorgang-Prozessflusses](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Folgende Schritte gelten für die Project Service App 2.4.4.30 oder älter in der Plattform 9.0

4. Hinzufügen eines neuen benutzerdefinierten Feld der Projektentität, um die benutzerdefinierten Phasen im angepassten Geschäftsprozessfluss aufzuzeichnen. Sie müssen die Geschäftslogik (Plug-In/Workflow) hinzufügen, um das Feld zu aktualisieren, wenn die aktuelle Phase im angepassten Geschäftsprozessfluss aktualisiert wird.

   > [!div class="mx-imgBorder"] 
   > ![Screenshot zum Anpassen der Projektentität](media/FAQ-Customize-BPF-6-720.png)

5. **Projekt nach Phase** Ändern Sie das Diagramm, um Ihr neues benutzerdefiniertes Feld für Phasen zu verwenden.

   > [!div class="mx-imgBorder"] 
   > ![Screenshot des Projektumfangs der Anwendung durch Phasendiagramm](media/FAQ-Customize-BPF-7-720.png)

6. Ändern Sie alle Ansichten, damit die Projektentität Ihr neues benutzerdefiniertes Feld für Phasen können.

   > [!div class="mx-imgBorder"] 
   > ![Screenshot der Änderung von Ansichten auf der Projektentität](media/FAQ-Customize-BPF-8-720.png)

