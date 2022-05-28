---
title: So verfolgen Sie ein Projektstatus
description: Nachverfolgen eines Projektstatus (Project Service)
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593381"
---
# <a name="track-a-projects-status-project-service"></a>Nachverfolgen eines Projektstatus (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Verwenden Sie [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], um den Fortschritt des Projektes eines Kunden nachzuverfolgen.  

Wenn das Engagement voranschreitet, werden die Projektphasen aktualisiert, um die Phase des Engagements darzustellen:  

| Task | Beschreibung des Dataflows | 
|------------|----------|
| **New** | Wenn Sie ein Projekt erstellen, wird die Phase auf **Neu** festgelegt. Wenn Sie das Projekt aus einer Vorlage erstellt haben, verfügt das Projekt zu diesem Zeitpunkt möglicherweise über einen Zeitplan, Schätzungen und Teamdaten. Andernfalls ist es der Entwurf des Projektes, und Sie müssen den Rest der Projektkomponenten manuell eintragen. |
| **Angebot** |  Wenn Sie ein Projekt einem Angebot zuweisen oder es aus einem Angebot erstellen, wird die Projektphase auf **Angebot** festgelegt, und auch die geschätzten Start- und Enddaten werden aktualisiert. Wenn das Projekt in der Angebotsphase ist, werden die Angebotsdetails auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt. |
| **Planen** |  Wenn Sie ein Angebot gewinnen, das einem Projekt zugewiesen ist, und wenn das Engagement bis zur Vertragsphase fortschreitet, wird die Projektphase auf **Planen** aktualisiert. Vertragsdetails werden auf der Registerkarte **Vertrieb** auf der Seite **Projekt** angezeigt. |
| **Abschließen** | Wenn die Projektarbeit abgeschlossen ist, können Sie die Phase auf **Abgeschlossen** ändern. Wenn die Projektphase auf "Abgeschlossen" festgelegt ist, ist die Arbeit zu 100 % abgeschlossen, aber das Projekt bleibt offen, damit alle ausstehenden Zeit- oder Ausgabeneingaben notiert werden können. |
| **Schließen** | Wenn alle Transaktionen auf dem Projekt aufgezeichnet worden sind und Sie keine weiteren mehr erwartet werden, können Sie die Phase manuell auf **Schließen** festlegen. Wenn das Projekt auf **Schließen** festlegen, können Sie keine weiteren Geschäfte auf dem Projekt aufzeichnen und das Projekt nur lesen. |

## <a name="to-track-a-projects-status"></a>So verfolgen Sie ein Projektstatus  

1.  Wechseln Sie zu **Project Service > Projekte**.  

2.  Klicken Sie auf das gewünschte Projekt.  

3.  Wählen Sie auf der Leiste oben auf dem Bildschirm den Abwärtspfeil neben dem Projektnamen, und klicken Sie dann auf **Projektnachverfolgung**.  

4.  Wählen Sie **Aufwandsnachverfolgung** oder **Kostennachverfolgung** in der Dropdownliste über der Aufgabenliste aus.  

5.  Doppelklicken Sie auf jede Aufgabe, um sie zu bearbeiten. Sie können die Balken im Gantt-Diagramm auch bewegen oder die Größe anpassen, um die Zeit und den Fortschritt für eine Aufgabe zu ändern.  

### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
