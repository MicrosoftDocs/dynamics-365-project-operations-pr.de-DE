---
title: Bereitstellungstyp festlegen
description: Dieses Thema enthält Informationen, die Ihnen helfen, den korrekten Bereitstellungstyp von Projekt Operations für Ihr Unternehmen zu bestimmen.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401217"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="842b0-103">Bereitstellungstyp festlegen</span><span class="sxs-lookup"><span data-stu-id="842b0-103">Determine your deployment type</span></span>

<span data-ttu-id="842b0-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="842b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="842b0-105">Nachdem Sie die Lizenz gekauft haben, beginnen Sie hier, um das beste Bereitstellungsmodell für Dynamics 365 Project Operations mithilfe des [geführten Installationsablaufs](https://aka.ms/provisionprojectoperations) zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="842b0-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="842b0-106">Nachdem Sie den geführten Installationsablauf abgeschlossen haben, werden Sie zum richtigen Verwaltungsportal weitergeleitet, um Ihre Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="842b0-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="842b0-107">Weitere Informationen zum Abschluss der Installation finden Sie in den Bereitstellungsdetails.</span><span class="sxs-lookup"><span data-stu-id="842b0-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="842b0-108">Vorhandene Kunden von Dynamics, die Dynamics 365 Project Service Automation nutzen</span><span class="sxs-lookup"><span data-stu-id="842b0-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="842b0-109">Project Operations umfasst die Funktionen, die mit Project Service Automation geliefert werden.</span><span class="sxs-lookup"><span data-stu-id="842b0-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="842b0-110">Für diese Kunden wird in der Veröffentlichungswelle 1 2021 ein Upgrade-Pfad freigegeben.</span><span class="sxs-lookup"><span data-stu-id="842b0-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="842b0-111">Vorhandene Kunden von Dynamics 365 Finance, die Projektmanagement und -buchhaltung verwenden</span><span class="sxs-lookup"><span data-stu-id="842b0-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="842b0-112">Bestehende Finance-Kunden, die die Projektmanagement- und Buchhaltungsfunktion verwenden, können sie weiterhin unverändert verwenden.</span><span class="sxs-lookup"><span data-stu-id="842b0-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="842b0-113">Weitere Informationen finden Sie unter [Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen](#pma).</span><span class="sxs-lookup"><span data-stu-id="842b0-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="842b0-114">Bereitstellungstypen</span><span class="sxs-lookup"><span data-stu-id="842b0-114">Deployment types</span></span>
<span data-ttu-id="842b0-115">Project Operations unterstützt mehrere Bereitstellungsoptionen, die Ihren Anforderungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="842b0-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="842b0-116">Unabhängig davon, ob Sie ein neuer oder vorhandener Dynamics 365-Kunde sind, kann Project Operations Ihre Anforderungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="842b0-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="842b0-117">Unsere [Bereitstellungsfragebogen](https://aka.ms/provisionprojectoperations) hilft Ihnen bei der Ermittlung der richtigen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="842b0-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="842b0-118">Die Ergebnisse führen Sie zu einem der folgenden Bereitstellungstypen:</span><span class="sxs-lookup"><span data-stu-id="842b0-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="842b0-119">Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="842b0-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="842b0-120">Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="842b0-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="842b0-121">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="842b0-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="842b0-122">Project Operations unterstützt Lager-/Produktionsauftragsszenarien und nicht lagernde/ressourcenbasierte Szenarien in derselben Umgebung durch Konfigurationen auf der Ebene der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="842b0-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="842b0-123">Beispielsweise kann Contoso die Lagerbestands-/Produktionsauftragsfunktionen in seiner US-Produktionsstätte nutzen (juristische Person = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="842b0-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="842b0-124">Contoso kann die nicht vorrätigen/ressourcenbasierten Funktionen in seiner Contoso Robotics Arms-Serviceeinrichtung im Vereinigten Königreich (juristische Person = Contoso Robotics, Vereinigtes Königreich) verwenden.</span><span class="sxs-lookup"><span data-stu-id="842b0-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="842b0-125">Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="842b0-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="842b0-126">Die Lite-Bereitstellung umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="842b0-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="842b0-127">Verkaufsprozess für Projekte, der die Anwendungserfahrung von Dynamics 365 Sales erweitert</span><span class="sxs-lookup"><span data-stu-id="842b0-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="842b0-128">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="842b0-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="842b0-129">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="842b0-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="842b0-130">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="842b0-130">Unified resource management</span></span>
- <span data-ttu-id="842b0-131">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="842b0-131">Time tracking</span></span>
- <span data-ttu-id="842b0-132">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="842b0-132">Basic expense</span></span>
- <span data-ttu-id="842b0-133">Proforma und kundenorientierte Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="842b0-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="842b0-134">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="842b0-134">Deployment steps</span></span>
<span data-ttu-id="842b0-135">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="842b0-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="842b0-136">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](lite-preview-subscription-sign-up.md) und [Neue Umgebung bereitstellen](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="842b0-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="842b0-137">Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="842b0-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="842b0-138">Der Projektbetrieb für Ressourcen-/nicht vorrätige Szenarien umfasst die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="842b0-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="842b0-139">Verkaufsprozess für Projekte, der die Anwendung von Dynamics 365 Sales erweitert</span><span class="sxs-lookup"><span data-stu-id="842b0-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="842b0-140">Projektplanung mit Microsoft Project für das Web</span><span class="sxs-lookup"><span data-stu-id="842b0-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="842b0-141">Mehrdimensionale Preisberechnung</span><span class="sxs-lookup"><span data-stu-id="842b0-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="842b0-142">Vereinheitlichte Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="842b0-142">Unified resource management</span></span>
- <span data-ttu-id="842b0-143">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="842b0-143">Time tracking</span></span>
- <span data-ttu-id="842b0-144">Grundkosten</span><span class="sxs-lookup"><span data-stu-id="842b0-144">Basic expense</span></span>
- <span data-ttu-id="842b0-145">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="842b0-145">Full expense</span></span>
- <span data-ttu-id="842b0-146">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="842b0-146">Receipt OCR</span></span>
- <span data-ttu-id="842b0-147">Proforma und kundenorientierte Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="842b0-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="842b0-148">Umsatzerkennung für Projekte</span><span class="sxs-lookup"><span data-stu-id="842b0-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="842b0-149">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="842b0-149">Deployment steps</span></span>
<span data-ttu-id="842b0-150">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="842b0-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="842b0-151">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](resource-sign-up-preview-subscription.md) und [Neue Umgebung bereitstellen](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="842b0-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="842b0-152">Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="842b0-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="842b0-153">Projektplanung mit WBS</span><span class="sxs-lookup"><span data-stu-id="842b0-153">Project planning using WBS</span></span>
- <span data-ttu-id="842b0-154">Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="842b0-154">Resource Management</span></span>
- <span data-ttu-id="842b0-155">Zeitnachverfolgung</span><span class="sxs-lookup"><span data-stu-id="842b0-155">Time Tracking</span></span>
- <span data-ttu-id="842b0-156">Volle Ausgaben</span><span class="sxs-lookup"><span data-stu-id="842b0-156">Full Expense</span></span>
- <span data-ttu-id="842b0-157">Zugangs-OCR</span><span class="sxs-lookup"><span data-stu-id="842b0-157">Receipt OCR</span></span>
- <span data-ttu-id="842b0-158">Volle Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="842b0-158">Full Invoicing</span></span>
- <span data-ttu-id="842b0-159">Umsatzrealisierung</span><span class="sxs-lookup"><span data-stu-id="842b0-159">Revenue Recognition</span></span>
- <span data-ttu-id="842b0-160">Produktionsaufträge</span><span class="sxs-lookup"><span data-stu-id="842b0-160">Production Orders</span></span>
- <span data-ttu-id="842b0-161">Materialienunterstützung</span><span class="sxs-lookup"><span data-stu-id="842b0-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="842b0-162">Bereitstellungsschritte</span><span class="sxs-lookup"><span data-stu-id="842b0-162">Deployment steps</span></span>
<span data-ttu-id="842b0-163">Bestimmen Sie das beste Bereitstellungsmodell für Project Operations mithilfe des [Bereitstellungsfragebogens](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="842b0-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="842b0-164">Informationen zu dieser Bereitstellung finden Sie unter [Registrieren für Vorschau-Abonnements](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) und [Neue Umgebung bereitstellen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="842b0-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

