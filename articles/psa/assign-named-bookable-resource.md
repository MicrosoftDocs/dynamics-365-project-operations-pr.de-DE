---
title: Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen
description: Dieses Thema enthält Informationen zum Buchen benannter Ressourcen für Projektteams und zum Zuweisen dieser Ressourcen zu Aufgaben.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575349"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können Ihrem Projektteam eine benannte Ressource hinzufügen, indem Sie diese direkt für das Team buchen. Führen Sie dazu folgende Schritte aus.

1. Wechseln Sie in Project Service Automation zu **Projekte**, wählen Sie das Projekt aus, für das Sie buchen möchten und öffnen Sie es.
2. Klicken Sie auf der Seite **Projekt** auf der Registerkarte **Team** auf **Neu**. 

![Hinzufügen eines Teammitglieds über die Registerkarte „Team“.](media/RM-how-to-1.png)

3. Wählen Sie im Dialogfeld **Schnellerfassung: Projektteammitglied** die buchbare Ressource aus. Das Feld **Rolle** wird mit der Standardrolle der Ressource vorausgefüllt, sofern eine zugewiesen wurde. Sie können die Rolle bei Bedarf ändern. 
4. Wählen Sie das Start- und Enddatum aus, an denen die Ressource benötigt wird, und wählen Sie die Zuweisungsmethode für die Ressourcenkapazität aus. 
5. Wenn das Teammitglied ein Projektgenehmiger sein soll, wählen Sie im Feld **Projektgenehmiger** **Ja** aus. Dies bedeutet, dass das Teammitglied übermittelte Zeit- und Ausgabeneinträge für dieses Projekt genehmigen kann. 
6. Klicken Sie auf **Speichern**.

![Hinzufügen eines Teammitglieds über das Formular „Schnellerfassung“.](media/RM-how-to-2.png)


Sie können die gebuchte Ressource nun Aufgaben im Projekt zuweisen. Klicken Sie auf der Seite **Projekt** auf die Registerkarte **Zeitplan**, um der neuen Ressource Aufgaben zuzuweisen. Die Ressourcenauswahl, die über das Feld **Ressourcen** im Aufgabenraster gestartet wird, zeigt die Teammitglieder an, die Sie auswählen können.

![Zuweisen eines Teammitglieds einer Aufgabe über die Registerkarte „Zeitplan“.](media/RM-how-to-3.png)

In Version 3 von Project Service Automation (PSA) sind Ressourcenbuchungen und Aufgabenzuweisungen nicht eng miteinander verknüpft. Wenn Sie also die Ressourcenauswahl im Zeitplan verwenden, können Sie Teammitgliedern Aufgaben für mehr Stunden zuweisen, als ihre Buchungen für das Projekt umfassen.
Sie sehen die Unterschiede zwischen Buchungen und Zuweisungen von Teammitgliedern auf der Registerkarte **Team** oder auf der Registerkarte **Ressourcenabstimmung**. Sie können die Unterschiede zwischen Buchungen und Zuweisungen für Ressourcen auch im Einzelnen abstimmen.

![Registerkarte „Ressourcenabstimmung“.](media/RM-how-to-4.png)

Sie können auch die Ressourcenauswahl auf der Registerkarte **Zeitplan** verwenden, um nach buchbaren Ressourcen zu suchen und sie auszuwählen, die nicht bereits Teil des Projektteams sind. Diese werden in der Ressourcenauswahl als **Weitere Ressourcen** angezeigt.

![Zuweisen einer Nicht-Teammitgliedressource zu einer Aufgabe.](media/RM-how-to-5.png)

Dabei wird die Ressource dem Projektteam hinzugefügt und der Aufgabe zugewiesen, es werden jedoch keine Buchungen generiert.

![Teammitglied mit Zuweisungen und ohne Buchungen.](media/RM-how-to-6.png)

Mithilfe der Funktion „Buchung erweitern“ auf der Registerkarte **Abstimmung** oder der **Zeitplanübersicht** können Sie die Kapazität der Ressource für das Projekt buchen.

![„Buchungen erweitern“ für ein Teammitglied auf der Registerkarte „Ressourcenabstimmung“.](media/RM-how-to-7.png)

Nachdem ein Teammitglied für Ihr Projekt gebucht wurde, können Sie zum Verwalten seiner Buchungen die Funktion „Buchungen verwalten“ oder die Zeitplanübersicht direkt verwenden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
