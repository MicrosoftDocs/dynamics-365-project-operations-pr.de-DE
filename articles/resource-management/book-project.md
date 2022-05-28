---
title: Zu einem Projekt buchen
description: Dieses Thema enthält Informationen zum Buchen einer Ressource für ein Projekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591364"
---
# <a name="book-to-a-project"></a>Zu einem Projekt buchen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Es gibt Zeiten, in denen ein Projektmanager oder Ressourcenmanager dem Projekt eine Ressource zuweisen muss, ohne dass eine bestimmte Anforderung von einem generischen Teammitglied definiert wird. Dies kann auf eine von drei Wegen erreicht werden.

- Buchen aus dem Teammitgliedsraster
- Über die Zeitplanübersicht buchen
- Buchen aus dem **Projekt**-Forumar

## <a name="book-from-the-team-member-grid"></a>Buchen aus dem Teammitgliedsraster

Wenn Ihre Organisation im hybriden Ressourcenzuweisungsmodus arbeitet, kann der Projektmanager eine Ressource direkt für das Projekt buchen, indem er die folgenden Schritte ausführt.

1. Gehen Sie im Projekt zum Teammitgliedsraster und wählen Sie **Neu**.
2. Definieren Sie den Positionsnamen und die Rolle der Ressource.
3. Wählen Sie in der verfügbaren Suche die entsprechende buchbare Ressource aus.
4. Legen Sie die folgenden Feldinformationen fest, um die Ressource zu buchen, nachdem Sie die Ressource ausgewählt haben:

    - Startdatum
    - Abschlussdatum
    - Zuordnungsmethode
    - Stunden, falls zutreffend
    - Projektgenehmiger

6. Wählen Sie **Speichern und schließen** aus

## <a name="book-from-the-schedule-board"></a>Über die Zeitplanübersicht buchen

Wenn ein Ressourcenmanager eine Ressource direkt für ein Projekt buchen muss, kann er die Zeitplanübersicht und die Projektanforderungen verwenden. Die Projektanforderung ist eine Ressourcenanforderung, für die immer gebucht werden kann. Um direkt aus der Zeitplanübersicht für ein Projekt zu buchen, führen Sie die folgenden Schritte aus.

1. Navigieren Sie zur Zeitplanübersicht und filtern Sie auf der linken Seite nach den Ressourcen, die Sie für die Anforderung in Betracht ziehen.
2. Wählen Sie im unteren Bereich die Registerkarte **Projekt** aus, um eine Liste der Projektanforderungen anzuzeigen.
3. Ziehen Sie die Anforderung auf eine Ressource und definieren Sie die folgenden Informationen:

    - Startdatum
    - Abschlussdatum
    - Buchungsstatus
    - Buchungsmethode
    - Duration
   
   > [!NOTE]
   > Momentan unterstützt Dynamics 365 Project Operations die Zeitplanübersicht nicht.   

## <a name="book-from-the-project-form"></a>Buchen aus dem Projekt-Forumar

Als Projektmanager müssen Sie möglicherweise eine Ressource für ein Projekt buchen, kennen jedoch nur die Kriterien und nicht den Namen der Ressource. Führen Sie die folgenden Schritte aus, um mithilfe des Zeitplanassistenten eine Ressource basierend auf verfügbaren Attributen der Ressource zu finden. 

1. Navigieren Sie zum Projekt und wählen Sie **Buchen** aus, um den Zeitplanassistenten zu öffnen.
2. Grenzen Sie die Kriterien mithilfe der Filter auf der linken Seite des Zeitplanassistenten ein und wählen Sie **Suchen** aus.
3. Basierend auf den in den Ergebnissen zurückgegebenen Ressourcen können Sie eine Ressource buchen.

> [!NOTE]
> Diese Methode erstellt keine Buchungen für die Ressource. Stattdessen wird die Ressource dem Team hinzugefügt. Nachdem das Teammitglied dem Projekt hinzugefügt wurde, kann der Projektmanager Buchungen verwalten oder Buchungen erweitern, um die erforderlichen Buchungen zur Ressource hinzuzufügen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
