---
title: Bereitstellungstyp festlegen
description: Dieses Thema enthält Informationen, die Ihnen helfen, den korrekten Bereitstellungstyp von Projekt Operations für Ihr Unternehmen zu bestimmen.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076528"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="57355-103">Bereitstellungstyp festlegen</span><span class="sxs-lookup"><span data-stu-id="57355-103">Determine your deployment type</span></span>

<span data-ttu-id="57355-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="57355-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57355-105">Nachdem Sie die Lizenz gekauft haben, beginnen Sie hier, um das beste Bereitstellungsmodell für Dynamics 365 Project Operations mithilfe des [geführten Installationsablaufs](https://aka.ms/provisionprojectoperations) zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="57355-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="57355-106">Nachdem Sie den geführten Installationsablauf abgeschlossen haben, werden Sie zum richtigen Verwaltungsportal weitergeleitet, um Ihre Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="57355-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="57355-107">Weitere Informationen zum Abschluss der Installation finden Sie in den Bereitstellungsdetails.</span><span class="sxs-lookup"><span data-stu-id="57355-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="57355-108">Vorhandene Kunden von Dynamics, die Dynamics 365 Project Service Automation nutzen</span><span class="sxs-lookup"><span data-stu-id="57355-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="57355-109">Project Operations umfasst die Funktionen, die mit Project Service Automation geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="57355-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="57355-110">Für diese Kunden wird in Zukunft ein Upgrade-Pfad freigegeben.</span><span class="sxs-lookup"><span data-stu-id="57355-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="57355-111">Vorhandene Kunden von Dynamics 365 Finance, die Projektmanagement und -buchhaltung verwenden</span><span class="sxs-lookup"><span data-stu-id="57355-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="57355-112">Vorhandene Finanzkunden, die die Projektmanagement- und -buchhaltungsfunktion verwenden, können diese weiterhin nutzen.</span><span class="sxs-lookup"><span data-stu-id="57355-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="57355-113">Weitere Informationen finden Sie unter [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma).</span><span class="sxs-lookup"><span data-stu-id="57355-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="57355-114">Bereitstellungstypen</span><span class="sxs-lookup"><span data-stu-id="57355-114">Deployment types</span></span>
<span data-ttu-id="57355-115">Project Operations unterstützt mehrere Bereitstellungsoptionen, die Ihren Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="57355-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="57355-116">Unabhängig davon, ob Sie ein neuer oder vorhandener Dynamics 365-Kunde sind, kann Project Operations Ihre Anforderungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="57355-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="57355-117">Unsere [Bereitstellungsfragebogen](https://aka.ms/provisionprojectoperations) hilft Ihnen bei der Ermittlung der richtigen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="57355-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="57355-118">Die Ergebnisse führen Sie zu einem der folgenden Bereitstellungstypen:</span><span class="sxs-lookup"><span data-stu-id="57355-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="57355-119">Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="57355-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="57355-120">Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57355-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="57355-121">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="57355-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="57355-122">Project Operations unterstützt Lager-/Produktionsauftragsszenarien und nicht lagernde/ressourcenbasierte Szenarien in derselben Umgebung durch Konfigurationen auf der Ebene der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="57355-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="57355-123">Beispielsweise kann Contoso die Lagerbestands-/Produktionsauftragsfunktionen in seiner US-Produktionsstätte nutzen (juristische Person = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="57355-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="57355-124">Contoso kann die nicht vorrätigen/ressourcenbasierten Funktionen in seiner Contoso Robotics Arms-Serviceeinrichtung im Vereinigten Königreich (juristische Person = Contoso Robotics, Vereinigtes Königreich) verwenden.</span><span class="sxs-lookup"><span data-stu-id="57355-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="57355-125">Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="57355-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="57355-126">Die Lite-Bereitstellung umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="57355-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="57355-127">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="57355-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="57355-128">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="57355-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="57355-129">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="57355-129">Unified Resource Management</span></span>
- <span data-ttu-id="57355-130">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="57355-130">Time Tracking</span></span>
- <span data-ttu-id="57355-131">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="57355-131">Basic Expense</span></span>
- <span data-ttu-id="57355-132">Rechnungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="57355-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57355-133">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="57355-133">Deployment steps</span></span>
<span data-ttu-id="57355-134">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57355-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57355-135">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](lite-preview-subscription-sign-up.md) und [Neue Umgebung bereitstellen](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="57355-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="57355-136">Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="57355-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="57355-137">Der Projektbetrieb für Ressourcen-/nicht vorrätige Szenarien umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="57355-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="57355-138">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="57355-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="57355-139">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="57355-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="57355-140">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="57355-140">Unified Resource Management</span></span>
- <span data-ttu-id="57355-141">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="57355-141">Time Tracking</span></span>
- <span data-ttu-id="57355-142">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="57355-142">Basic Expense</span></span>
- <span data-ttu-id="57355-143">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57355-143">Full Expense</span></span>
- <span data-ttu-id="57355-144">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="57355-144">Receipt OCR</span></span>
- <span data-ttu-id="57355-145">Volle Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="57355-145">Full Invoicing</span></span>
- <span data-ttu-id="57355-146">Umsatzrealisierung</span><span class="sxs-lookup"><span data-stu-id="57355-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57355-147">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="57355-147">Deployment steps</span></span>
<span data-ttu-id="57355-148">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57355-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57355-149">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](resource-sign-up-preview-subscription.md) und [Neue Umgebung bereitstellen](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="57355-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="57355-150">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="57355-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="57355-151">Projektplanung mit WBS</span><span class="sxs-lookup"><span data-stu-id="57355-151">Project planning using WBS</span></span>
- <span data-ttu-id="57355-152">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="57355-152">Resource Management</span></span>
- <span data-ttu-id="57355-153">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="57355-153">Time Tracking</span></span>
- <span data-ttu-id="57355-154">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57355-154">Full Expense</span></span>
- <span data-ttu-id="57355-155">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="57355-155">Receipt OCR</span></span>
- <span data-ttu-id="57355-156">Volle Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="57355-156">Full Invoicing</span></span>
- <span data-ttu-id="57355-157">Umsatzrealisierung</span><span class="sxs-lookup"><span data-stu-id="57355-157">Revenue Recognition</span></span>
- <span data-ttu-id="57355-158">Produktionsaufträge</span><span class="sxs-lookup"><span data-stu-id="57355-158">Production Orders</span></span>
- <span data-ttu-id="57355-159">Materialienunterstützung</span><span class="sxs-lookup"><span data-stu-id="57355-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="57355-160">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="57355-160">Deployment steps</span></span>
<span data-ttu-id="57355-161">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="57355-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="57355-162">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) und [Neue Umgebung bereitstellen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="57355-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

