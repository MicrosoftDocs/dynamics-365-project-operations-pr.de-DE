---
title: So verfolgen Sie ein Projektstatus
description: Nachverfolgen eines Projektstatus (Project Service)
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149587"
---
# <a name="track-a-projects-status-project-service"></a>Nachverfolgen eines Projektstatus (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Verwenden Sie [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], um den Fortschritt des Projektes eines Kunden nachzuverfolgen.  

Wenn das Engagement voranschreitet, werden die Projektphasen aktualisiert, um die Phase des Engagements darzustellen:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Neu**    | Wenn Sie ein Projekt erstellen, wird die Phase auf **Neu** festgelegt. Wenn Sie das Projekt aus einer Vorlage erstellt haben, verfügt das Projekt zu diesem Zeitpunkt möglicherweise über einen Zeitplan, Schätzungen und Teamdaten. Andernfalls ist es der Entwurf des Projektes, und Sie müssen den Rest der Projektkomponenten manuell eintragen. |
|  **Angebot**   |      Wenn Sie ein Projekt einem Angebot zuweisen oder es aus einem Angebot erstellen, wird die Projektphase auf **Angebot** festgelegt, und auch die geschätzten Start- und Enddaten werden aktualisiert. Wenn das Projekt in der Angebotsphase ist, werden die Angebotsdetails auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt.      |
|   **Planen**   |                                     Wenn Sie ein Angebot gewinnen, das einem Projekt zugewiesen ist, und wenn das Engagement bis zur Vertragsphase fortschreitet, wird die Projektphase auf **Planen** aktualisiert. Vertragsdetails werden auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt.                                      |
| **Abschließen** |                    Wenn die Projektarbeit abgeschlossen ist, können Sie die Phase auf **Abgeschlossen** ändern. Wenn die Projektphase auf "Abgeschlossen" festgelegt ist, ist die Arbeit zu 100 % abgeschlossen, aber das Projekt bleibt offen, damit alle ausstehenden Zeit- oder Ausgabeneingaben notiert werden können.                     |
|  **Schließen**   |           Wenn alle Transaktionen auf dem Projekt aufgezeichnet worden sind und Sie keine weiteren mehr erwartet werden, können Sie die Phase manuell auf **Schließen** festlegen. Wenn das Projekt auf **Schließen** festlegen, können Sie keine weiteren Geschäfte auf dem Projekt aufzeichnen und das Projekt nur lesen.           |

## <a name="to-track-a-projects-status"></a>So verfolgen Sie ein Projektstatus  

1.  Wechseln Sie zu **Project Service > Projekte**.  

2.  Klicken Sie auf das gewünschte Projekt.  

3.  Wählen Sie auf der Leiste oben auf dem Bildschirm den Abwärtspfeil neben dem Projektnamen, und klicken Sie dann auf **Projektnachverfolgung**.  

4.  Wählen Sie **Aufwandsnachverfolgung** oder **Kostennachverfolgung** in der Dropdownliste über der Aufgabenliste aus.  

5.  Doppelklicken Sie auf jede Aufgabe, um sie zu bearbeiten. Sie können die Balken im Gantt-Diagramm auch bewegen oder die Größe anpassen, um die Zeit und den Fortschritt für eine Aufgabe zu ändern.  

### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)
