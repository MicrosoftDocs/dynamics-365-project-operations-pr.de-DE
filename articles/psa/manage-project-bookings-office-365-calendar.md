---
title: Verwalten von Projekten und Buchungen in Ihrem Office 365-Kalender
description: So verwalten Sie Projekte und Buchungen in Ihrem Office 365-Kalender
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
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: cf51333179d2d972af84de7adb4b718b6e17d038
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598901"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Verwalten von Projekten und Anmeldungen in Ihrem Kalender (Project Service)

> [!Note]
> VERALTET: Diese Funktion ist veraltet und nicht mehr verfügbar.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Anzeigen der persönlichen Terminen, Projektarbeitbuchungen und Außendienst-Arbeitsaufträgen im [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-Kalender.  
  
 Wenn alles an einem Ort ist, können Sie Ihren Tag ganz einfach verwalten. Ihre Besprechungen, Termine, Buchungen und Aufgaben sind alle im [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Kalender verfügbar.  
  
 Wenn Sie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] verwenden, können Sie Ihre persönlichen Terminen in der Project Service-Zeiteintragungsansicht eingeben. So sind Projekt und Ressourcen-Manager über Ihre Verfügbarkeit für Projekte informiert. Es speichert auch Ihre Zeit, denn Sie müssen keine Informationen zu Ihren persönlichen Terminen doppelt eingeben. Sie können persönliche Termine einfach aus Ihrem Kalender in die Project Service-Zeiteintragsansicht importieren.  
  
 Ihr Kalender synchronisiert Projekt- und Arbeitsauftragsanmeldungen ab heute für die kommenden vier Wochen. Dieser Einstellung kann nicht geändert werden.  
  
 Das Synchronisieren ist nur auf eine Art unterstützt, von PSA zu Ihrem [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Kalender. Sie können in umgekehrter Reihenfolge synchronisieren. 
  
 Informationen zur Verwendung des [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] finden Sie im [Kalender in Outlook im Netz für Unternehmen](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)  
  
## <a name="setup"></a>Einrichtung  
 Bevor Sie Ihre Buchungen im [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-Kalender sehen und verwalten können, müssen Sie einige Punkte festlegen.  
  
- Sie benötigen Anmeldeinformationen für den Globalen Administrator oder den [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Systemadministrator.  
  
- Ihr Administrator muss das E-Mail-Serverprofil konfigurieren jeder Benutzer muss sein Postfach konfigurieren. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Einrichten der E-Mail-Verarbeitung durch serverseitige Synchronisierung](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Aktivieren der Synchronisierung für Ihre Organisation (Administratoraufgabe)  
  
1.  Klicken Sie im Hauptmenü auf **Einstellungen** > **Administration**.  
  
2.  Klicken Sie auf **Systemeinstellungen**.  
  
3.  Klicken Sie auf die Registerkarte **Synchronisation**.  
  
4.  Wählen Sie unter **Auswählen, ob das Synchronisieren der Ressourcen aktiviert werden soll** die Option **Ressourcenbuchung mit Outlook synchronisieren**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Die Synchronisierung für Ihr Benutzerprofil einschalten (Benutzeraufgabe)  
  
1.  Wählen Sie die Schaltfläche **Einstellungen** in der oberen rechten Ecke des Bildschirms.  
  
2.  Klicken Sie auf **Optionen**.  
  
3.  Klicken Sie auf die Registerkarte **Synchronisation**.  
  
4.  Aktivieren Sie unter **Ressourcenbuchungsynchronisierung mit Outlook** die Option **Ressourcenbuchung mit Outlook synchronisieren**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importieren Ihrer persönlichen Terminen (Benutzeraufgabe)  
 Sie können persönliche Termine einfach aus Ihrem Kalender in die Project Service Automation-Zeiteintragsansicht importieren.  
  
1. Öffnen Sie den [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-Kalender Office und klicken Sie auf **Daten importieren**.  
  
2. Wählen Sie auf der Filter-Seite **Termine von Exchange** und klicken Sie auf **Übernehmen**.  
  
3. Das System zieht aber der aktuellen Woche Termine in die Zeiteintragungsansicht. Um Einträge für eine andere Woche hinzuzufügen, klicken Sie auf **Vorherige** oder **Nächste**.  
  
4. Wählen Sie den Termin aus, den Sie zur Project Service Automation-Zeiteintragungsansicht hinzufügen möchten.  
  
5. Wählen Sie im **Zeiteintrag**-Popup die entsprechenden Optionen zur Konvertierung des Termins in eine Project Service Automation Zeiteintragsansciht aus.  
  
6. Klicken Sie auf **Speichern**.  
  
### <a name="see-also"></a>Siehe auch  
 [Handbuch Zeit, Ausgaben und Zusammenarbeit](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
