---
title: Bereitstellungstypen
description: Dieses Thema enthält Informationen, die Ihnen helfen, den korrekten Bereitstellungstyp von Projekt Operations für Ihr Unternehmen zu bestimmen.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948868"
---
# <a name="deployment-types"></a><span data-ttu-id="f8fc4-103">Bereitstellungstypen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-103">Deployment types</span></span>

<span data-ttu-id="f8fc4-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="f8fc4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8fc4-105">Nachdem Sie die Lizenz gekauft haben, beginnen Sie hier, um das beste Bereitstellungsmodell für Dynamics 365 Project Operations mithilfe des [geführten Installationsablaufs](https://aka.ms/provisionprojectoperations) zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="f8fc4-106">Nachdem Sie den geführten Installationsablauf abgeschlossen haben, werden Sie zum richtigen Verwaltungsportal weitergeleitet, um Ihre Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="f8fc4-107">Weitere Informationen zum Abschluss der Installation finden Sie in den folgenden Bereitstellungsdetails.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="f8fc4-108">Vorhandene Kunden von Dynamics, die Dynamics 365 Project Service Automation nutzen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="f8fc4-109">Project Operations umfasst die Funktionen, die mit Project Service Automation geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="f8fc4-110">Für diese Kunden wird in Zukunft ein Upgrade-Pfad freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="f8fc4-111">Vorhandene Kunden von Dynamics 365 Finance, die Projektmanagement und -buchhaltung verwenden</span><span class="sxs-lookup"><span data-stu-id="f8fc4-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="f8fc4-112">Vorhandene Finanzkunden, die die Projektmanagement- und -buchhaltungsfunktion verwenden, können diese weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="f8fc4-113">Weitere Informationen finden Sie unter [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="f8fc4-114">Project Operations unterstützt mehrere Bereitstellungsoptionen, die Ihren Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="f8fc4-115">Unabhängig davon, ob Sie ein neuer oder vorhandener Dynamics 365-Kunde sind, kann Project Operations Ihre Anforderungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="f8fc4-116">Unsere [Bereitstellungsfragebogen](https://aka.ms/provisionprojectoperations) hilft Ihnen bei der Ermittlung der richtigen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="f8fc4-117">Die Ergebnisse führen Sie zu einem der folgenden Bereitstellungstypen:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="f8fc4-118">Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="f8fc4-119">Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="f8fc4-120">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="f8fc4-121">Project Operations unterstützt Lager-/Produktionsauftragsszenarien und nicht lagernde/ressourcenbasierte Szenarien in derselben Umgebung durch Konfigurationen auf der Ebene der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="f8fc4-122">Beispielsweise kann Contoso die Lagerbestands-/Produktionsauftragsfunktionen in seiner US-Produktionsstätte (juristische Person = Contoso Manufacturing USA) und die nicht vorrätigen/ressourcenbasierten Funktionen in seiner Contoso Robotics Arms-Serviceeinrichtung in Großbritannien (juristische Person = Contoso Robotics Vereintes Königreich) nutzen.</span><span class="sxs-lookup"><span data-stu-id="f8fc4-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="f8fc4-123"><a name="lite"><a/>Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="f8fc4-124">Die Lite-Bereitstellung umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="f8fc4-125">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="f8fc4-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f8fc4-126">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f8fc4-127">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-127">Unified Resource Management</span></span>
- <span data-ttu-id="f8fc4-128">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-128">Time Tracking</span></span>
- <span data-ttu-id="f8fc4-129">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="f8fc4-129">Basic Expense</span></span>
- <span data-ttu-id="f8fc4-130">Rechnungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="f8fc4-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="f8fc4-131">Bereitstellungsschritte:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-131">Deployment steps:</span></span>
<span data-ttu-id="f8fc4-132">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8fc4-133">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](lite-preview-subscription-sign-up.md) und [Neue Umgebung bereitstellen](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="f8fc4-134"><a name="integrated"><a/>Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="f8fc4-135">Der Projektbetrieb für Ressourcen-/nicht vorrätige Szenarien umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="f8fc4-136">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="f8fc4-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f8fc4-137">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f8fc4-138">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-138">Unified Resource Management</span></span>
- <span data-ttu-id="f8fc4-139">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-139">Time Tracking</span></span>
- <span data-ttu-id="f8fc4-140">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="f8fc4-140">Basic Expense</span></span>
- <span data-ttu-id="f8fc4-141">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8fc4-141">Full Expense</span></span>
- <span data-ttu-id="f8fc4-142">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="f8fc4-142">Receipt OCR</span></span>
- <span data-ttu-id="f8fc4-143">Volle Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-143">Full Invoicing</span></span>
- <span data-ttu-id="f8fc4-144">Umsatzrealisierung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="f8fc4-145">Bereitstellungsschritte:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-145">Deployment steps:</span></span>
<span data-ttu-id="f8fc4-146">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8fc4-147">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](resource-sign-up-preview-subscription.md) und [Neue Umgebung bereitstellen](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="f8fc4-148">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="f8fc4-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="f8fc4-149">Projektplanung mit WBS</span><span class="sxs-lookup"><span data-stu-id="f8fc4-149">Project planning using WBS</span></span>
- <span data-ttu-id="f8fc4-150">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-150">Resource Management</span></span>
- <span data-ttu-id="f8fc4-151">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-151">Time Tracking</span></span>
- <span data-ttu-id="f8fc4-152">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8fc4-152">Full Expense</span></span>
- <span data-ttu-id="f8fc4-153">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="f8fc4-153">Receipt OCR</span></span>
- <span data-ttu-id="f8fc4-154">Volle Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-154">Full Invoicing</span></span>
- <span data-ttu-id="f8fc4-155">Umsatzrealisierung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-155">Revenue Recognition</span></span>
- <span data-ttu-id="f8fc4-156">Produktionsaufträge</span><span class="sxs-lookup"><span data-stu-id="f8fc4-156">Production Orders</span></span>
- <span data-ttu-id="f8fc4-157">Materialienunterstützung</span><span class="sxs-lookup"><span data-stu-id="f8fc4-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="f8fc4-158">Bereitstellungsschritte:</span><span class="sxs-lookup"><span data-stu-id="f8fc4-158">Deployment steps:</span></span>
<span data-ttu-id="f8fc4-159">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f8fc4-160">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) und [Neue Umgebung bereitstellen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f8fc4-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



