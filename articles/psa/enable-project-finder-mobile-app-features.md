---
title: Aktivieren der Project Finder Mobile-App-Funktionen
description: So aktivieren Sie die Funktionen der Project Finder Mobile-App für Project Service
author: JohnPBurrows
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132962"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="2414e-103">Aktivieren der Project Finder Mobile-App-Funktionen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2414e-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2414e-104">Ihre Ressourcen können die Project Finder Mobile-App auf ihrem Telefon mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] verwenden, um neue Projekte zu suchen, an denen sie arbeiten können, und um ihre Qualifikationen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2414e-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="2414e-105">Die App ist für [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)]-Smartphones und [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2414e-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="2414e-106">Sie müssen ein paar Optionen in den Parametereinstellungen für ihre Organisationseinheit festlegen, damit Benutzer den Ressourcenbedarf von Projekten anzeigen können und ihre Qualifikationen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="2414e-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2414e-107">Die Project Finder Mobile-App funktioniert nur mit [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], nicht mit lokalen Installationen.</span><span class="sxs-lookup"><span data-stu-id="2414e-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="2414e-108">Gehen Sie zu **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="2414e-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="2414e-109">Klicken Sie auf die Parametereinstellung, die Sie verwenden möchten, um die Funktionen der Project Finder Mobile-App zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2414e-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="2414e-110">Legen Sie im Bereich **Allgemein** die Option **Ressourcenanforderungen für Ressourcen sichtbar** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="2414e-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="2414e-111">Legen Sie **Qualifikationsaktualisierung durch Ressource zulassen** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="2414e-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="2414e-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="2414e-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="2414e-113">Dies ist eine globale Einstellung.</span><span class="sxs-lookup"><span data-stu-id="2414e-113">This is a global setting.</span></span> <span data-ttu-id="2414e-114">Projektmanager können festlegen, ob ein Einzelprojekt auf der Seite **Projektteam** dieses Projekts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2414e-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="2414e-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="2414e-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="2414e-116">E-Mail-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2414e-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="2414e-117">sendet E-Mails bezüglich der Ressourcenanforderungen an die folgenden Empfänger zu den folgenden Zeiten:</span><span class="sxs-lookup"><span data-stu-id="2414e-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="2414e-118">Empfänger</span><span class="sxs-lookup"><span data-stu-id="2414e-118">Recipient</span></span>|<span data-ttu-id="2414e-119">Veranstaltung</span><span class="sxs-lookup"><span data-stu-id="2414e-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="2414e-120">Projektmanager</span><span class="sxs-lookup"><span data-stu-id="2414e-120">Project manager</span></span>|<span data-ttu-id="2414e-121">-   Wenn eine Ressource sich für ein Projekt mit der Project Finder Mobile-App anmeldet.</span><span class="sxs-lookup"><span data-stu-id="2414e-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="2414e-122">Ressource</span><span class="sxs-lookup"><span data-stu-id="2414e-122">Resource</span></span>|<span data-ttu-id="2414e-123">-   Wenn die Projektarbeit, für die die Ressource sich angemeldet hat, bereits von einer anderen Ressource ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2414e-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="2414e-124">-   Wenn die Qualifikationsgenehmigungsanforderung genehmigt oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="2414e-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="2414e-125">-   Wenn die Projektregistrierungsanforderung genehmigt oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="2414e-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="2414e-126">Datenschutzbestimmungen</span><span class="sxs-lookup"><span data-stu-id="2414e-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="2414e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2414e-127">See Also</span></span>  
 [<span data-ttu-id="2414e-128">Ressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="2414e-128">Set up resources</span></span>](../psa/set-up-resources.md)
