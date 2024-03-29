---
title: Anforderungen für unverbindliches Buchen
description: Dieser Artikel informiert Sie darüber, wie Sie die Anforderungen für das Softbooking einrichten können.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 8192047639823bc594803d6d10759be28f6db3ed
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928937"
---
# <a name="soft-book-requirements"></a>Anforderungen für unverbindliches Buchen

[!include [banner](../includes/psa-now-project-operations.md)]

Eine Ressourcenanforderung kann verbindlich gebucht werden. Eine verbindliche Buchung erstellt einen Vorschlag, der die Kapazität einer Ressource verbraucht. Der Vorschlag wird dann zur Genehmigung an den Anforderer zurückgesendet. Eine unverbindliche Buchung fügt vorläufig eine Ressource zu einem Projektteam hinzu und hat einen anderen Status in der Zeitplanübersicht. Sie verbraucht jedoch keine Kapazität der Ressource. Um über die Zeitplanübersicht eine Ressource unverbindlich zu buchen, legen Sie für das Feld **Buchungsstatus** den Status **Unverbindlich** fest.

![Auf „Unverbindlich“ festgelegter Buchungsstatus.](media/Resource-Management-image77.png)

Wenn die Registerkarte **Team** in der Ansicht **Benannte Teammitglieder** vorhanden ist, wird die Ressource dort angezeigt. Die unverbindlich gebuchten Stunden werden in der Spalte **Unverbindlich gebuchte Stunden** angegeben.

![Unverbindlich gebuchte Stunden in der Ansicht „Benannte Teammitglieder“.](media/Resource-Management-image78.png)

Unverbindlich gebuchte Teammitglieder können Aufgaben zugewiesen werden.

![Unverbindlich gebuchtes Teammitglied, das einer Aufgabe zugewiesen ist.](media/Resource-Management-image79.png)

Auf der Registerkarte **Abstimmung** werden für eine unverbindlich gebuchte Ressource keine Buchungen angezeigt, weil die Registerkarte **Abstimmung** nur verbindliche Buchungen berücksichtigt.

![Unverbindlich gebuchte Ressource ohne Buchungen auf der Registerkarte „Abstimmung“.](media/Resource-Management-image80.png)

> [!NOTE]
> Sie können eine Ressource aus einer Anforderung, die von einem generischen Teammitglied generiert wurde, nicht unverbindlich buchen.

In der Zeitplanübersicht wird für unverbindliche Buchungen für eine Ressource eine andere Farbgebung verwendet.

![Unverbindliche Buchungen in der Zeitplanübersicht.](media/Resource-Management-image81.png)

Um eine unverbindliche in eine verbindliche Buchung zu konvertieren, klicken Sie in der Zeitplanübersicht mit der rechten Maustaste auf die unverbindliche Buchung und wählen Sie dann **Status ändern** \> **Verbindlich buchen** \> **Verbindlich** aus.

![Ändern des Buchungsstandards in „Verbindlich“.](media/Resource-Management-image82.png)

Die Buchung sowie der Status in der Zeitplanübersicht werden geändert. Da für den Buchungsstatus nunmehr **Verbindlich** festgelegt ist, wird die Ressource als gebucht angezeigt und ihre Kapazität und Verfügbarkeit werden angepasst.

Auf dieselbe Weise können Sie eine verbindliche oder eine unverbindliche Buchung in der Zeitplanübersicht stornieren.

Um eine unverbindlich gebuchte Ressource auf der Registerkarte **Team** des Projekts in eine verbindlich gebuchte Ressource zu konvertieren, wählen Sie die Ressource und anschließend **Bestätigen** aus.

![Befehl bestätigen.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
