---
title: Homepage upgraden
description: In diesem Thema wird gezeigt, wo Sie wichtige Informationen über die neuen und geänderten Funktionen in Dynamics 365 Project Service Automation finden sowie den Prozess für das Upgraden auf die neueste Version.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e30da3a5ade6d8bafcdc45801b830196841997bf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150082"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="5e84f-103">Homepage upgraden</span><span class="sxs-lookup"><span data-stu-id="5e84f-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="5e84f-104">Upgrade von PSA-Version 2.x oder 1.x auf Version 3.x</span><span class="sxs-lookup"><span data-stu-id="5e84f-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="5e84f-105">Neue Instanzen</span><span class="sxs-lookup"><span data-stu-id="5e84f-105">New instances</span></span>

<span data-ttu-id="5e84f-106">Ab 17. Mai, 2019, wird bei Auswahl von Project Service Automation während der Bereitstellung einer neuen Instanz standardmäßig Version 3.x installiert.</span><span class="sxs-lookup"><span data-stu-id="5e84f-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="5e84f-107">Vorhandene Instanzen</span><span class="sxs-lookup"><span data-stu-id="5e84f-107">Existing instances</span></span>

<span data-ttu-id="5e84f-108">Zuvor mussten Kunden, die eine Instanz von PSA Version 2.x hatten, und auf Version 3.x upgraden mussten, welche die auf dem einheitlichen Client basierte (UCI) Version von PSA war, sich an den Microsoft Support wenden und die Details ihrer Instanz angeben, damit der Support die Instanz für das Upgrade auf Version 3.x aktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="5e84f-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="5e84f-109">Ab dem 1. März 2020 können Kunden, die über eine Instanz von PSA Version 2.x verfügen und auf Version 3.x aktualisieren müssen, ihre Instanzen direkt über das Admin-Portal aktualisieren, ohne sich an den Microsoft-Support wenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="5e84f-110">PSA Version 3.x umfasst wichtige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="5e84f-111">Sie ist in das Framework der einheitlichen Oberfläche integriert, um eine verbesserte Benutzerfreundlichkeit zu bieten.</span><span class="sxs-lookup"><span data-stu-id="5e84f-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="5e84f-112">Die neu gestaltete App bietet eine durchgängige, einheitliche Benutzeroberfläche (UI) und folgt den dynamischen Designgrundsätzen für eine optimale Anzeige auf jeder Bildschirmgröße oder jedem Gerät.</span><span class="sxs-lookup"><span data-stu-id="5e84f-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="5e84f-113">Es sind weitere Änderungen in der gesamten Anwendung vorgenommen worden.</span><span class="sxs-lookup"><span data-stu-id="5e84f-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="5e84f-114">Einige der Bereiche, die geändert wurden, umfassen Preise, Buchung und das Zuweisen von Ressourcen, Zeit, Ausgaben und Genehmigungen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="5e84f-115">Bevor Sie mit dem Upgradeprozess beginnen, wird empfohlen, dass Sie die folgenden Aufgaben abschließen:</span><span class="sxs-lookup"><span data-stu-id="5e84f-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="5e84f-116">Überprüfen Sie, ob sowohl Dynamics 365 Field Service als auch Project Service Automation in der identifizierten Instanz installiert sind.</span><span class="sxs-lookup"><span data-stu-id="5e84f-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="5e84f-117">Wenn beide Lösungen installiert sind, sollten Sie das Upgrade für beide Planen, bevor Sie die reguläre Verwendung der Instanz fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="5e84f-118">Überprüfen Sie sorgfältig die folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-118">Carefully review the following topics.</span></span> <span data-ttu-id="5e84f-119">Kenntnis und Verstehen der Änderungen zwischen Versionen hilft Ihnen beim Upgradeprozess.</span><span class="sxs-lookup"><span data-stu-id="5e84f-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="5e84f-120">Diese Themen bieten Informationen zu den Hauptänderungen in PSA, neben Überlegungen und Empfehlungen für die Planung Ihres Upgrades auf Version 3.x.</span><span class="sxs-lookup"><span data-stu-id="5e84f-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="5e84f-121">Neuigkeiten und Änderungen in Project Service Automation, Version 3</span><span class="sxs-lookup"><span data-stu-id="5e84f-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="5e84f-122">Überlegungen zum Upgrade – Project Service Automation Version 2.x oder 1.x auf Version 3</span><span class="sxs-lookup"><span data-stu-id="5e84f-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="5e84f-123">Aktualisieren Sie Ihre Sandkasteninstanz, um Änderungen in Ihrer Implementierung auszuwerten, bevor Sie Ihre Produktionsinstanz aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5e84f-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="5e84f-124">Nachdem Sie die Themen durchgesehen haben, die zuvor erwähnt wurden und bereit sind, das Upgrade auf PSA Version 3.x oder die UCI-basierte Version durchzuführen, senden Sie eine Anforderung an den Microsoft-Support, damit dieser das Upgrade vom Admin Center aus zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="5e84f-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="5e84f-125">Geben Sie in Ihrer Anforderung die Details Ihrer Instanz an.</span><span class="sxs-lookup"><span data-stu-id="5e84f-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="5e84f-126">Ältere Versionen von PSA (PSA Version 2.x) in einer neu erstellten Instanz</span><span class="sxs-lookup"><span data-stu-id="5e84f-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="5e84f-127">Seit dem 17. Mai 2019 haben alle neuen Instanzen UCI als Standardclient.</span><span class="sxs-lookup"><span data-stu-id="5e84f-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="5e84f-128">Zur Ausrichtung an dieser Änderung werden PSA Version 3.x und Field Service 8.x standardmäßig bereitgestellt, da diese Versionen dazu entworfen wurden, mit dem UCI-Client zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5e84f-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="5e84f-129">Ab dem 1. März 2020 können Kunden von Dynamics PSA keine neue Umgebung mehr mit älteren PSA-Versionen erstellen, z. B. PSA Version 2.x oder niedriger.</span><span class="sxs-lookup"><span data-stu-id="5e84f-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="5e84f-130">In jeder neuen Umgebung wird nur Version 3.x von PSA bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5e84f-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="5e84f-131">Für eine optimale Erfahrung, wenn Sie ältere Versionen von Field Service und PSA-Anwendungen verwenden, wechseln Sie zur Seite **Systemeinstellungen**, und für das Feld **Nur die neue einheitliche Oberfläche verwenden (empfohlen)** wählen Sie **Nein** aus, da diese Versionen nicht dazu entworfen sind, in UCI korrekt geladen zu werden.</span><span class="sxs-lookup"><span data-stu-id="5e84f-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="5e84f-132">Nachdem Sie UCI deaktiviert haben, können Sie diese Versionen von Field Service und PSA mithilfe des alten Webclient öffnen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e84f-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
