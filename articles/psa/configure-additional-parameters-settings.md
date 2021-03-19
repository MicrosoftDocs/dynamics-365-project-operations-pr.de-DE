---
title: Konfigurieren von zusätzlichen Parametereinstellungen
description: Konfigurieren Sie zusätzliche Parametereinstellungen (Project Service)
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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290763"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="287e2-103">Konfigurieren Sie zusätzliche Parametereinstellungen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="287e2-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="287e2-104">Sobald Sie die Elemente in den vorherigen Themen konfiguriert haben, müssen Sie zusätzliche Projektparameter festlegen, die für die Projekte benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="287e2-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="287e2-105">Bei der Installation des [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] haben Sie eine Parametereinstellungen für die erste Erstellung aller für den [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erforderlichen Datensätze erstellt.</span><span class="sxs-lookup"><span data-stu-id="287e2-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="287e2-106">Jetzt ist es Zeit zurückzukehren und zusätzliche Felder für diese Parametereinstellung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="287e2-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="287e2-107">Sie müssen die folgenden Einstellungen konfiguriert haben:</span><span class="sxs-lookup"><span data-stu-id="287e2-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="287e2-108">Organisationseinheit:</span><span class="sxs-lookup"><span data-stu-id="287e2-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="287e2-109">Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="287e2-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="287e2-110">Arbeitszeitvorlage</span><span class="sxs-lookup"><span data-stu-id="287e2-110">Work hours template</span></span>  
  
-   <span data-ttu-id="287e2-111">Preisliste</span><span class="sxs-lookup"><span data-stu-id="287e2-111">Price list</span></span>  
 
<span data-ttu-id="287e2-112">In diesem Schritt geben Sie an, welche der Ressourcenzuordnung Sie wünschen:</span><span class="sxs-lookup"><span data-stu-id="287e2-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="287e2-113">**Zentral**.</span><span class="sxs-lookup"><span data-stu-id="287e2-113">**Central**.</span></span> <span data-ttu-id="287e2-114">Nur Ressourcen-Manager können Ressourcen zu Projekten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="287e2-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="287e2-115">**Hybrid**.</span><span class="sxs-lookup"><span data-stu-id="287e2-115">**Hybrid**.</span></span> <span data-ttu-id="287e2-116">Ressourcen-Manager, Projektmanager und Account Manager können und den Projekten Ressourcen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="287e2-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="287e2-117">Um die Projektparameter festzulegen:</span><span class="sxs-lookup"><span data-stu-id="287e2-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="287e2-118">Gehen Sie zu **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="287e2-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="287e2-119">Klicken Sie auf die Sie die Parameter, die Sie konfigurieren möchten (die, die sie bei der ersten Installation des [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erstellt haben), oder klicken Sie auf **Neu**, um eine neue Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="287e2-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="287e2-120">Legen Sie im Bereich **Allgemein** alle Optionen für die Projektparameter fest.</span><span class="sxs-lookup"><span data-stu-id="287e2-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="287e2-121">Klicken Sie im Bereich **Preisliste** auf **+**, um einer Preisliste hinzuzufügen, wählen Sie eine Preisliste in der Dropdownliste **Projekt-Parameter-Preisliste** aus, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="287e2-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="287e2-122">Klicken Sie auf die Schaltfläche **Speichern** in der unteren rechten Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="287e2-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="287e2-123">Der Projektparametersatz muss gepflegt sein, damit Project Service ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="287e2-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="287e2-124">Dieser Datensatz sollte nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="287e2-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="287e2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="287e2-125">See Also</span></span>  
 [<span data-ttu-id="287e2-126">Ressourcen einrichten</span><span class="sxs-lookup"><span data-stu-id="287e2-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]