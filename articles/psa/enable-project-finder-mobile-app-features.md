---
title: Aktivieren der Project Finder Mobile-App-Funktionen
description: So aktivieren Sie die Funktionen der Project Finder Mobile-App für Project Service
author: JohnPBurrows
ms.prod: ''
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
ms.openlocfilehash: f068c32ac957dc5921ccabc989b3b7a347585c19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007725"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Aktivieren der Project Finder Mobile-App-Funktionen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ihre Ressourcen können die Project Finder Mobile-App auf ihrem Telefon mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] verwenden, um neue Projekte zu suchen, an denen sie arbeiten können, und um die Qualifikationen zu aktualisieren.  
  
 Die App ist für [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-Smartphones und [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] verfügbar.  
    
 Optionen in den Parametereinstellungen für ihre Organisationseinheit müssen ausgewählt sein, damit Benutzer den Ressourcenbedarf von Projekten anzeigen können und ihre Qualifikationen aktualisieren können.
  
> [!NOTE]
>  Die Project Finder Mobile-App funktioniert nur mit [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], nicht mit lokalen Installationen.  
  
1. Gehen Sie zu **Project Service > Parameter**.  
  
2. Klicken Sie auf die Parametereinstellung, die Sie verwenden möchten, um die Funktionen der Project Finder Mobile-App zu verwenden.  
  
3. Legen Sie im Bereich **Allgemein** die Option **Ressourcenanforderungen für Ressourcen sichtbar** auf **Ja** fest.  
  
4. Legen Sie **Qualifikationsaktualisierung durch Ressource zulassen** auf **Ja** fest.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Dies ist eine globale Einstellung. Projektmanager können festlegen, ob ein Einzelprojekt auf der Seite **Projektteam** dieses Projekts angezeigt wird.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-Mail-Benachrichtigungen  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sendet E-Mails bezüglich der Ressourcenanforderungen an die folgenden Empfänger zu den folgenden Zeiten:  
  
|Empfänger|Veranstaltung|  
|---------------|-----------|  
|Projektmanager|- Wenn eine Ressource sich für ein Projekt mit der Project Finder Mobile-App anmeldet.|  
|Ressource|- Die Projektarbeit, für die die Ressource sich angemeldet hat, wird bereits von einer anderen Ressource ausgeführt.<br />- Die Qualifikationsgenehmigungsanforderung wurde genehmigt oder abgelehnt.<br />- Die Projektregistrierungsanforderung wurde genehmigt oder abgelehnt.|  
  
## <a name="privacy-notice"></a>Datenschutzbestimmungen  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Siehe auch  
 [Ressourcen einrichten](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]