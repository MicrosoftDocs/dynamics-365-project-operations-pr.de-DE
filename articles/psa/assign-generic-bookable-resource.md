---
title: Allgemeine buchbare Ressourcen einer Aufgabe und einem Projektteam zuweisen
description: Dieser Artikel enthält Informationen über das Buchen von allgemeinen Ressourcen auf Aufgaben und Projektteams.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 9f67ab7381747e5d780f8b0024dd98ae8420d05f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923555"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Zuweisen von allgemeinen buchbaren Ressourcen zu einer Aufgaben und Erstellen von Ressourcenanforderungen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Zusätzlich zur Buchung und Zuweisung von benannten oder echten Ressourcen zu Ihrem Projekt können Sie Projektaufgaben allgemeine Ressourcen zuweisen. Diese Ressourcen können als Platzhalter für benannte Ressourcen dienen, bis Sie bereit sind, Ihr Projekt mit benannten Ressourcen auszustatten. 

1. Öffnen Sie in Project Service Automation (PSA) die Seite **Projekt** und geben Sie auf der Registerkarte **Zeitplan** den Positionsnamen der generischen Ressource in der Zelle **Ressource** des Zeitplans ein. Sie können auch in der Zelle auf das Symbol **Ressource** klicken, um die Ressourcenauswahl zu öffnen, und dann den Namen der allgemeinen Ressource eingeben, die Sie erstellen möchten.

![Erstellen und Zuweisen eines allgemeinen Teammitglieds.](media/RM-how-to-9.png)

Dadurch wird der Bereich **Schnellerfassung: Projektteammitglied** geöffnet. 

2. Geben Sie die Rolle und Organisationseinheit des generischen Ressourcenteammitglieds ein und klicken Sie dann auf **Speichern**.

![Generisches Teammitglied – Schnellerfassung.](media/RM-how-to-10.png)

3. Nachdem Sie das neue generische Ressourcenteammitglied erstellt haben, wird es der Aufgabe zugewiesen. Sie können diese generische Ressource weiteren Aufgaben im Arbeitsplan zuweisen.

![Zuweisen vorhandener generischer Teammitglieder zu Aufgaben.](media/RM-how-to-11.png)

4. Nachdem Sie die generische Ressource zugewiesen haben, können Sie eine Ressourcenanforderung generieren und diese erfüllen, indem Sie eine Ressourcenanforderung direkt buchen oder an einen Ressourcen-Manager übermitteln.

![Generieren einer Anforderung für ein generisches Teammitglied.](media/RM-how-to-12.png)

Im Teammitgliedsraster können Sie nicht nur die Ressourcenauswahl wie oben erwähnt verwenden, sondern auch generische Ressourcen direkt hinzufügen. Die Ressourcen werden mit einer Ressourcenanforderung hinzugefügt, die auf dem Start- bzw. Enddatum und der Zuordnungsmethode basiert, die im Bereich **Schnellerfassung: Projektteammitglied** angegeben sind.

Sie können einen Unterschied feststellen, wenn Sie das generische Teammitglied direkt hinzufügen und der generischen Ressource dann mehr Aufgaben zuweisen, als Stunden angefordert wurden, um diese durchzuführen. Klicken Sie auf **Anforderung generieren**, um die Anforderung zum Abgleichen der erforderlichen Stunden mit den Zuweisungen neu zu generieren.

Sie können auch auf den Link **Ressourcenanforderung** im Teamraster klicken, um die Anforderung zu öffnen und Fähigkeiten, bevorzugte Ressourcen usw. hinzuzufügen.

![Ressourcenanforderung](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
