---
title: Erstellen einer Projektbuchung aus der Zeitplanübersicht
description: Dieses Thema enthält Informationen über die Erstellung einer Projektbuchung aus der Zeitplanübersicht.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146527"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Erstellen einer Projektbuchung aus der Zeitplanübersicht

[!include [banner](../includes/psa-now-project-operations.md)]

Sie können eine Ressource direkt auf der Registerkarte **Team** des Projekts für ein Projekt buchen oder eine Ressourcenanforderung aus einer allgemeinen Teammitgliedzuweisung generieren und dann die generierte Anforderung mit einem Projektteammitglied erfüllen.

Sie können eine Ressource für ein Projekt auch über die Zeitplanübersicht buchen. Dafür stehen drei Möglichkeiten zur Verfügung:

- **Von einer generierten Ressourcenanforderung buchen:** Sie können eine Ressourcenanforderung generieren, nachdem Sie eine generische Ressource erstellt und Aufgaben innerhalb eines Projekts zugewiesen haben.

- **Von der primären Anforderung buchen:** Die primären Anforderungen werden in der Zeitplanübersicht auf der Registerkarte **Projekt** angezeigt. 

- **Von einer neuen Ressourcenanforderungen buchen:** Sie können eine Ressourcenanforderung von Grund auf neu erstellen und sie einem Projekt zuordnen. Auf der Zeitplanübersicht werden diese Ressourcenanforderungen auf der Registerkarte **Offene Anforderungen** angezeigt.

## <a name="book-from-a-generated-resource-requirement"></a>Von einer generierten Ressourcenanforderung buchen

Sie können eine allgemeine Ressource erstellen und diesen einer oder mehreren Aufgaben innerhalb eines Projekts zuweisen. Anschließend können Sie aus dem generischen Teammitglied eine Ressourcenanforderung generieren. 

1.  Auf der Zeitplanübersicht wird diese Ressource auf der Registerkarte **Offene Anforderungen** angezeigt. Gegebenenfalls muss der Spaltenfilter im Raster verwendet werden, wenn Sie viele geöffnete Anforderungen haben. 

    ![Registerkarte Anforderungen auf der Zeitplanübersicht](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot der Anmeldungen und Zuweisungstabellen")

2. Wählen Sie die erforderliche Anforderung aus. Die Registerkarte **Verfügbarkeit durchsuchen** wird oben in der ausgewählten Zeile angezeigt.
 
3. Beim Auswählen der Registerkarte wird der Zeitplanassistent-Modus der Zeitplanübersicht geöffnet und die verfügbaren Ressourcen gefiltert, um die Ressourcenanforderungen zu erfüllen. Danach können Sie eine Ressource buchen.

4. Sie können die ausgewählte Zeile auch vom unteren Rand der Zeitplanübersicht in eine Ressourcenzelle im Raster darüber ziehen und dort ablegen. Dadurch wird der **Anmeldungsbereich erstellen** rechts geöffnet.

    **Buchen** auswählen, um die Ressource im Projektteam zu buchen.

![Ressourcen-Anmeldungsbereich erstellen](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Buch der primären Anforderung

Ein Projekt in Project Service erstellen erstellt automatisch eine Ressourcenanforderung, die die primäre Anforderung genannt wird. Dies ist eine leere Anforderung, mit der eine Ressource schnell über die Zeitplanübersicht gebucht werden kann, ohne eine Anforderung zu generieren oder von Grund auf neu zu erstellen. Da die Anforderung leer ist, müssen Sie die Termine und -stunden (falls zutreffend) sowie die Zuordnungsmethode angeben. 

1. Um eine Ressource mit einer primären Anforderung zu buchen, wählen Sie auf der Zeitplanübersicht die Registerkarte **Projekt** aus. Möglicherweise müssen Sie den Spaltenfilter auf der Spalte **Projekt** verwenden, wenn Sie viele Projekte haben.

   ![Spaltenfilter auf der Zeitplanübersicht anzeigen](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot der Anmeldungen und Zuweisungstabellen")

2. Wählen Sie die Anforderung aus, die nur den Projektnamen als Namen und eine Dauer von Null (0) hat.

3. Wählen Sie die Registerkarte **Verfügbarkeit durchsuchen**, die oben in der ausgewählten Zeile angezeigt wird. Dies hat zur Folge, dass die Zeitplanübersicht in den Zeitplanassistentenmodus wechselt und die verfügbaren Ressourcen anzeigt, die für das Projekt gebucht werden können.

4. Da eine **Primäre Anforderung** eine leere Anforderung mit einer Dauer von Null (0) ist, müssen Sie die Dauer im Bereich **Ressourcenbuchung erstellen** festlegen, wenn Sie eine Ressource auswählen und buchen.

5. Sie können die **Primäre Projektanforderung** am unteren Rand der Zeitplanübersicht auswählen, auf eine Ressource ziehen und dort ablegen, um sie zu zu buchen.
 
    Da die **Primäre Anforderung** eine leere Anforderung mit einer Dauer von Null (0) ist, müssen Sie die Dauer im Bereich **Ressourcenbuchung erstellen** festlegen, wenn Sie eine Ressource auswählen und buchen.
 
    Wenn Sie eine Ressource über die **Primäre Anforderung** in der Zeitplanübersicht buchen, fügen Sie sie dem Projektteam ohne Zuweisungen hinzu.
 
## <a name="book-from-a-new-resource-requirement"></a>Von einer neuen Ressourcenanforderung buchen
Führen Sie die folgenden Schritte aus, um aus einer neuen Ressourcenanforderung zu buchen. 

1. Gehen Sie zu **Ressourcenanforderungen** und wählen Sie dann **Neu** aus, um eine neue Ressourcenanforderung zu erstellen.

2. Wählen Sie auf der Registerkarte **Projekt** ein Projekt aus, um die Anforderung dem Projekt zuzuordnen.
 
    Auf der Zeitplanübersicht wird diese neue Anforderung als **Offene Anforderung** angezeigt, die Sie erfüllen können.

3. Buchen Sie die Ressource, um sie dem Projektteam hinzuzufügen.

4. Nachdem die Ressource gebucht wurde, müssen Sie Aufgaben manuell zuweisen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]