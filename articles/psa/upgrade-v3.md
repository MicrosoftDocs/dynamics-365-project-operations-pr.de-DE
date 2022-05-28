---
title: Überlegungen zum Upgrade – Microsoft Dynamics 365 Project Service Automation Version 2.x oder 1.x auf Version 3
description: Dieses Thema enthält Informationen zu Überlegungen, die Sie vornehmen müssen, wenn Sie von Project Service Automation Version 2.x oder 1.x auf Version 3 aktualisieren.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: c37c30b7c694cec8c07b68492d935128881e6317
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601753"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Überlegungen zum Upgrade von PSA-Version 2.x oder 1.x auf Version 3.x

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation und Field Service
Sowohl Dynamics 365 Project Service Automation wie auch Dynamics 365 Field Service verwenden die Universal Resourcing Scheduling (URS) Lösung für die Ressourcenplanung. Wenn Sie in Ihrer Instanz Project Service Automation und Field Service haben, müssen Sie beide Lösungen auf die neueste Version aktualisieren. Für Project Service Automation ist das Version 3.x. Für Field Service ist es Version 8.x. Durch das Aktualisieren von Project Service Automation oder Field Service wird die neueste Version von URS installiert. Wenn sowohl die Project Service Automation- als auch die Field Service-Lösung in derselben Instanz nicht auf die neueste Version aktualisiert werden, liegt möglicherweise ein inkonsistentes Verhalten vor.

## <a name="resource-assignments"></a>Ressourcenzuweisungen
In Project Service Automation Version 2 und Version 1 wurden Aufgabenzuordnungen als untergeordnete Aufgaben (auch Positionsaufgaben genannt) in der **Aufgabenentität** gespeichert und indirekt mit der Entität **Ressourcenzuweisung** verknüpft. Die Positionsaufgabe wurde im Zuweisungspopupfenster im Projektstrukturplan (PSP) angezeigt.

![Linienaufgaben auf dem PSP in Project Service Automation Version 2 und Version 1.](media/upgrade-line-task-01.png)

In Version 3 von Project Service Automation wurde das zugrunde liegende Schema bei der Zuweisung von buchbaren Ressourcen zu Aufgaben geändert. Die Positionsaufgabe ist veraltet und es gibt eine direkte 1:1-Beziehung zwischen der Aufgabe in der **Aufgabenentität** und dem Teammitglied in der Entität **Ressourcenzuweisung**. Aufgaben, die einem Projektteammitglied zugeordnet sind, werden jetzt direkt in der Ressourcenzuweisungsentität gespeichert.  

Diese Änderungen wirken sich auf das Upgrade aller vorhandenen Projekte aus, die Ressourcenzuweisungen für benannte buchbare Ressourcen und allgemeine Ressourcen in einem Projektteam haben. Dieses Thema enthält Überlegungen, die Sie für Ihre Projekte berücksichtigen müssen, wenn Sie auf Version 3 aktualisieren. 

### <a name="tasks-assigned-to-named-resources"></a>Aufgaben, die benannten Ressourcen zugewiesen sind
Mithilfe der zugrunde liegenden Aufgabenentität konnten Teammitglieder in und Version 2 und Version 1 eine andere Rolle als die Standardrolle darstellen. Zum Beispiel kann Helga Grämer, der standardmäßig die Rolle des Projektleiters zugewiesen ist, eine Aufgabe mit der Rolle Entwickler zugewiesen werden. In Version 3 ist die Rolle eines benannten Teammitglieds immer der Standard, sodass jede Aufgabe, die Helga Grämer zugewiesen wird, die Standardrolle der Projektleiterin Helga erhält.

Wenn Sie eine Ressource zu einer Aufgabe außerhalb der Standardrolle in Version 2 und Version 1 zugewiesen haben, wird der benannten Ressource nach einem Upgrade die Standardrolle für alle Aufgabenzuordnungen zugewiesen, unabhängig von der Rollenzuweisung in Version 2. Durch diese Arbeitsauftragsergebnisse entstehen Unterschiede der berechneten Schätzungen von Version 2 oder Version 1 zu Version 3, da Schätzungen anhand der Rolle der Ressource und nicht der Positionsaufgabenzuordnung berechnet werden. In Version 2 wurden Bruna Schöffer beispielsweise zwei Aufgaben zugewiesen. Die Rolle in der Positionsaufgabe für Aufgabe 1 ist Entwickler und für Aufgabe 2 Projektleiter. Bruna Schöffer hat die Standardrolle Projektleiterin.

![Mehrere Rollen sind einer Ressource zugeordnet.](media/upgrade-multiple-roles-02.png)

Da die Rollen Entwickler und Projektleiter sich unterscheiden, lauten die Kosten- und Verkaufsschätzungen wie folgt:

![Kostenvorkalkulationen für Ressourcenrollen.](media/upggrade-cost-estimates-03.png)

![Verkausschätzungen für Ressourcenrollen.](media/upgrade-sales-estimates-04.png)

Wenn Sie ein Upgrade auf Version 3 ausführen, werden Positionsaufgaben in der Aufgabe des buchbaren Ressourcenteammitglieds durch Ressourcenzuweisungen ersetzt. Die Zuweisung nutzt die Standardrolle der buchbaren Ressource. In der folgenden Grafik ist Bruna Schöffer, die die Rolle der Projektleiterin hat, die Ressource.

![Ressourcenzuweisungen.](media/resource-assignment-v2-05.png)

Da die Schätzungen auf der Standardrolle für die Ressource basieren, können sich Vertriebs- und die Kostenvoranschläge ändern. Beachten Sie in der folgenden Grafik, dass die Rolle **Entwickler** nicht mehr angezeigt wird, da die Rolle jetzt aus der Standardrolle der buchbaren Ressource entfernt wurde.

![Kostenvoranschläge für Standardrollen.](media/resource-assignment-cost-estimate-06.png)
![Verkaufsschätzungen für Standardrollen.](media/resource-assignment-sales-estimate-07.png)

Nach Abschluss des Upgrades können Sie die Rolle eines Teammitglieds bearbeiten, um eine andere als die Standardrolle anzunehmen. Wenn Sie eine Teammitgliedsrolle ändern, wird sie in allen zugeteilten Aufgaben geändert, da in Version 3 Teammitgliedern nicht mehrere Rollen zugewiesen werden können.

![Aktualisieren einer Ressourcenrolle.](media/resource-role-assignment-08.png)

Dies gilt auch für Positionsaufgaben, die benannten Ressourcen zugewiesen wurden, wenn Sie die Organisationseinheit von der Standardeinstellung in eine andere Organisationseinheit ändern. Nach dem Upgrade auf Version 3 verwendet die Zuweisung die Standardorganisationseinheit Ressource anstatt des eines Satzes in der Positionsaufgabe.

### <a name="tasks-assigned-to-generic-resources"></a>Aufgaben, die allgemeinen Ressourcen zugewiesen sind
In Version 2 und Version 1 können Sie die Rollen- und Organisationseinheiten einer Aufgabe festlegen und dann die Funktion **Team erstellen** verwenden, um allgemeine Ressourcen anhand der Attribute zu generieren, die in der Aufgabe festgelegt wurden. In Version 3 erstellen Sie die allgemeinen Teammitglieder mit Rollen- und Organisationseinheit und weisen dann die Teammitglieder zur Aufgabe zu.

In Version 2 und Version 1 können Projekte mit generischen Ressourcen zwei Status haben oder eine Mischung der beieden auf Aufgabenebene. Angenommen, es liegen folgende Szenarien vor:

- Aufgaben mit festgelegten Rollen- und Organisationseinheiten, jedoch ohne dazugehörige generierte Ressourcenzuweisung.
- Aufgaben mit allgemeinen Teammitgliedsressourcenzuweisungen, die zugeordnet wurden, indem eine allgemeine Ressource mithilfe der Funktion **Team erstellen** erstellt wurde.

Bevor Sie mit dem Upgrade beginnen, wird empfohlen, das Projekt für jedes Team erneut zu generieren, das Aufgaben für generische Ressourcen zugewiesen hat oder bei dem der Teamerstellungsprozess noch ausgeführt werden muss.

Bei Aufgaben, die generischen Teammitgliedern zugeordnet sind, die mit **Team erstellen** erstellt wurden, wird beim Upgrade die allgemeine Ressource im Team und die Zuweisung beim allgemeinen Teammitglied belassen. Es wird empfohlen, dass Sie die Ressourcenanforderungen für das allgemeine Teammitglied nach der Aktualisierung erstellen, jedoch bevor Sie eine Ressourcenanforderung buchen oder senden. Dies erhält alle Organisationseinheiten-Zuweisungen der generischen Teammitglieder, die sich von der Organisationseinheit des Projektvertrags unterscheiden.

Im Projekt Z-Projekt ist die Vertragsorganisation beispielsweise Contoso US. Testaufgaben in der Implementierung wurden im Projektplan der Rolle des technischen Beraters zugewiesen und zugewiesene Organisationseinheit ist Contoso India.

![Zuweisung der Implementierungsphasenorganisation.](media/org-unit-assignment-09.png)

Nach der Implementierungsphase wird die Integrationstestaufgabe der Rolle des technischen Beraters zugewiesen, die Organisation ist jedoch auf Contoso US festgelegt.  

![Zuweisung der Integrationstestaufgabenorganisation.](media/org-unit-generate-team-10.png)

Wenn Sie ein Team für das Projekt erstellen, werden aufgrund der zwei unterschiedlichen Organisationseinheiten der Aufgaben zwei allgemeine Teammitglieder erstellt. Der technische Berater 1 erhält die Aufgaben von Contoso India und der technische Berater 2 die Aufgaben von Contoso US.  

![Erstellte Generische Teammitglieder.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> In Project Service Automation Version 2 und Version 1 hat das Teammitglied nicht die Organisationseinheit, die in der Positionsaufgabe verwaltet wird.

![Linienaufgaben in Project Service Automation Version 2 und Version 1.](media/line-tasks-12.png)

Sie sehen die Organisationseinheit in der Schätzungsansicht. 

![Organisationseinheitenschätzungen.](media/org-unit-estimates-view-13.png)
 
Wenn das Upgrade abgeschlossen ist, wird die Organisationseinheit in der Positionsaufgabe, die dem generischen Teammitglied entspricht, dem generischen Teammitglied hinzugefügt und die Positionsaufgabe wird entfernt. Aus diesem Grund wird empfohlen, dass vor dem Upgrade die Teams in den Projekten, die allgemeine Ressourcen enthalten, zu erstellen oder erneut zu generieren.

Bei Aufgaben, die einer Rolle in einer Organisationseinheit zugewiesen sind, die sich von der Organisationseinheit des Vertragsprojekts unterscheidet, und für die kein Team erstellt wurde, erstellt das Upgrade ein allgemeines Teammitglied für die Rolle, verwendet jedoch auch die Vertragseinheit des Projekts für die Organisationseinheit des Teammitglieds. Im Beispiel von Projekt Z bedeutet dies, dass die Vertragsorganisationseinheit Contoso US ist und die Projektplantestaufgaben in der Implementierungsphase der Rolle des technischen Beraters mit der Organisationseinheit Contoso India zugewiesen wurden. Die Integrationstestaufgabe, die nach der Implementierungsphase abgeschlossen wird, wurde der Rolle des technischen Beraters zugewiesen. Die Organisationsheit ist Contoso US und es wurde kein Team erstellt. Das Upgrade erstellt ein allgemeines Teammitglied, einen technischen Berater, dem Stunden für drei Aufgaben zugewiesen sind, und eine Organisationseinheit Contoso US, die Vertragsorganisationseinheit des Projekts.   
 
Das Ändern der standardmäßigen Ressourcenorganisationseinheit für nicht erneut generierte Teammitglieder ist der Grund dafür, dass wir empfehlen, dass Sie die Teams in den Projekten vor dem Upgrade erstellen oder erneut generieren, sodass die Organisationseinheitenzuweisungen nicht verloren gehen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
