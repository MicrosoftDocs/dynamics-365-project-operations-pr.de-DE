---
title: Planen Sie Ressourcen für ein Projekt.
description: Ressourcen für ein Projekt planen (Project Service)
author: JohnPBurrows
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583123"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Ressourcen für ein Projekt planen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sie können die Verfügbarkeit von Ressourcen überprüfen, um einen Gesamtüberblick darüber zu erhalten, wie stark Ihre Ressourcen gebucht sind. Sie können die Ansicht auch nach Qualifikationen, Team, Standort und anderen Optionen filtern.  
  
Die Zeitplanübersicht zeigt eine Ressourcenliste und deren Verfügbarkeit an. Wählen Sie einen Anzeigemodus aus, um die Verfügbarkeiten nach **Stunden**, **Tag**, **Woche** und **Monat** anzuzeigen.  
  
Bevor Sie die Zeitplanübersicht verwenden, müssen Sie diese einrichten. Weitere Informationen finden Sie unter [Konfigurieren der Zeitplanübersicht (Field Service oder Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Wenn Sie eine ältere Version verwenden, lesen Sie für die Ressourcenverfügbarkeit [Ressourcenverfügbarkeit anzeigen (Project Service Automation)](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Um die Zeitplanübersicht-Buchungsfunktion, Standorterfassung und Standortservices zu verwenden, müssen Sie Karten aktivieren.  
> 
> 1. Klicken Sie im Hauptmenü auf die Option für **Ressourcenplanung** > **Verwaltung**.  
> 2. Klicken Sie auf **Planungsparameter**.  
> 3. Öffnen Sie den Datensatz und führen Sie einen Bildlauf nach unten zum **Resource Scheduling Optimization** Abschnitt durch.  
> 4. Wählen Sie im Feld **Mit Karten verbinden** die Option **Ja** aus.  
> 5. Akzeptieren Sie die Bedingungen und speichern Sie den Datensatz.  
> 6. Klicken Sie im Hauptmenü auf **Project Service** > **Zeitplanübersicht**. Es gibt unterschiedliche Arten eine Buchungsanforderung manuell zu planen. Wählen Sie die Methode aus, die für Sie funktioniert.
  
## <a name="find-available-resources"></a>Verfügbare Ressourcen finden

1.  Rechtsklicken Sie in der Liste **Buchungsanforderung** auf eine ungeplante Buchung, und wählen Sie eine der folgenden Optionen aus:  
  
- Wählen Sie **Verfügbarkeit suchen – Aktuelle Ressourcen**, um verfügbaren Ressourcen in der Zeitplanübersicht zu suchen.  
- Wählen Sie **Verfügbarkeit suchen – Alle Ressourcen**, um verfügbare Ressourcen im System zu suchen.  
   > [!NOTE]
   >  Dabei werden die Filter die Optionen für die ausgewählte Buchungsanforderung anzeigen.  
  
2. Wenn Sie einen verfügbaren Zeitraum sehen, klicken Sie mit rechts in der Zeitplanübersicht auf den Zeitraum und wählen Sie **Hier buchen**. Oder Ziehen Sie die Buchungsanforderungen auf einen Zeitraum und legen Sie diese dort ab.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Buchen einer Ressource mithilfe der täglichen Ansicht und nicht ausgebuchte Personen suchen
  
1.  Auf der Zeitplanübersicht klicken Sie auf **Ansichtsmodus**, und wählen Sie **Tage** aus.  
  
    Dies zeigt eine Tabellenansicht der Anzahl der gebuchten Stunden einer Ressource pro Tag und die freien Tage an.  
  
2.  Klicken Sie auf den Namen der Ressource, die Sie buchen möchten, und klicken Sie dann auf **Buchen**.  
  
3.  Wählen Sie im Dialogfeld **Ressourcenbuchung (erstellen)** das Projekt, für das Sie die Ressource buchen möchten sowie die Buchungsmethode und die Start- und Endzeiten.  
  
4.  Wählen Sie **Buchen** aus, wenn Sie fertig sind.  
  
## <a name="view-to-the-schedule-board"></a>Anzeigen der Zeitplanübersicht
  
1.  Wählen Sie eine ungeplante Buchungsanforderung von der Liste unten aus.  
  
2.  Verschieben Sie die Buchungsanforderungen zu einer verfügbaren Ressource/einem verfügbaren Zeitfenster in der Zeitplanübersicht.  
  
3.  Wählen Sie **Buchen** aus, wenn Sie fertig sind.  
  
### <a name="additional-resources"></a>Zusätzliche Ressourcen  
 [Ressourcenmanagerhandbuch](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
