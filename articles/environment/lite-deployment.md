---
title: Bereitstellen der Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung
description: Dieses Thema enthält Informationen zur Installation der Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076388"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="72106-103">Bereitstellen der Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="72106-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="72106-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="72106-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72106-105">Project Operations unterstützt mehrere Bereitstellungsmodelle.</span><span class="sxs-lookup"><span data-stu-id="72106-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="72106-106">Informationen zum Ermitteln des besten Bereitstellungsmodells finden Sie unter [Bereitstellungstypen](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="72106-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="72106-107">Diese Bereitstellung, Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung führt zu einer reinen **Common Data Service-Bereitstellung von Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="72106-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="72106-108">Project Operations in einer neuen CDS-Umgebung installieren</span><span class="sxs-lookup"><span data-stu-id="72106-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="72106-109">In einer vorhandenen CDS-Umgebung installieren</span><span class="sxs-lookup"><span data-stu-id="72106-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="72106-110">Project Operations in einer neuen CDS-Umgebung installieren</span><span class="sxs-lookup"><span data-stu-id="72106-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="72106-111">Als der [Globale oder Power Platform-Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz erstellen Sie eine neue CDS-Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="72106-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="72106-112">Stellen Sie sicher das **CDS-Datenbank** und **Dynamics 365-Apps** aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="72106-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="72106-113">Weitere Informationen finden Sie unter [Erstellen und Verwalten von Umgebungen im Power Platform-Admin Center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="72106-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="72106-114">Wählen Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="72106-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="72106-115">Project Operations in einer vorhandenen CDS-Umgebung installieren</span><span class="sxs-lookup"><span data-stu-id="72106-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="72106-116">Als der [globale oder Power Platform-Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) mit einer Project Operations-Lizenz suchen Sie die Umgebung im [PowerPlatform-Admin Center](https://admin.powerplatform.com), wo Sie Project Operations installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="72106-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="72106-117">Installieren Sie **Microsoft Dynamics 365 Project Operations** aus der Bereitstellungsliste der Dynamics 365-Apps.</span><span class="sxs-lookup"><span data-stu-id="72106-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="72106-118">Weitere Informationen finden Sie unter [Verwalten von Dynamics 365-Apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="72106-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


