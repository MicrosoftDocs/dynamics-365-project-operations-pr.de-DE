---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen von Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642956"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="7e4f9-103">Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden</span><span class="sxs-lookup"><span data-stu-id="7e4f9-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="7e4f9-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="7e4f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e4f9-105">In diesem Thema wird erläutert, wie Sie das Vorschau-/Partnerangebot abonnieren und die Project Operations-Umgebung bei Szenarien für vorrätige/nicht vorrätige Ressourcen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7e4f9-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7e4f9-106">Prerequisites</span></span>

- <span data-ttu-id="7e4f9-107">Sie erhalten eine E-Mail, in der Sie zur Teilnahme an der Vorschau eingeladen werden.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="7e4f9-108">Sie können eine Vorschau auf der [Project Operations-Website](https://dynamics.microsoft.com/en-us/project-operations/overview/) anfordern.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="7e4f9-109">Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="7e4f9-110">Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="7e4f9-111">Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/en-us/free/) verwenden, um zu starten.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="7e4f9-112">Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="7e4f9-113">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="7e4f9-113">Subscribe</span></span>

<span data-ttu-id="7e4f9-114">Wenn Ihre [Vorschauanforderung](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) genehmigt wird, erhalten Sie drei Angebote von Microsoft per E-Mail.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="7e4f9-115">Mit diesen Angeboten können Sie die Project Operations-Vorschau bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="7e4f9-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="7e4f9-116">Dynamics 365 Project Operations (CRM)-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="7e4f9-117">Office 365 Project Operations – Vorschau-Testversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="7e4f9-118">Dynamics 365 Finance – Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e4f9-119">Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="7e4f9-120">Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="7e4f9-121">Dynamics 365 Project Operations (CRM)-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="7e4f9-122">Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="7e4f9-123">Lösen Sie den ersten Angebotscode **Dynamics 365 Project Operations (CRM)-Vorschautestversion** durch Einfügen in die Browser-URL ein.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Angebot einlösen](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="7e4f9-125">Bestätigen Sie Ihre Bestellung.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-125">Confirm your order.</span></span>

![Bestellung bestätigen](./media/17ConfirmOrderNew.png)

<span data-ttu-id="7e4f9-127">Sie sehen, dass das Bestätigungsangebot erfolgreich eingelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-127">You will see confirmation offer was successfully redeemed.</span></span>

![Bestätigung](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="7e4f9-129">Office 365 Project Operations – Vorschau-Testversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="7e4f9-130">Wiederholen Sie die gleichen Schritte wie beim ersten Angebotscode.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="7e4f9-131">Stellen Sie sicher, dass Sie den zweiten Angebotscode mit demselben Benutzerkonto hinzufügen, das mit dem ersten Angebotscode verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="7e4f9-132">Dynamics 365 Finance-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="7e4f9-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="7e4f9-133">Wiederholen Sie dieselben Schritte mit dem letzten Angebot aus der Begrüßungs-E-Mail.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="7e4f9-134">Lizenzen zuweisen</span><span class="sxs-lookup"><span data-stu-id="7e4f9-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e4f9-135">Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="7e4f9-136">Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Startseite des Admin Center](./media/14AdminPortal.png)

2. <span data-ttu-id="7e4f9-138">Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Lizenzen zuweisen](./media/15AssignLicenses.png)

3. <span data-ttu-id="7e4f9-140">Stellen Sie sicher, dass die **Dynamics 365 Project Operations (CRM)-Vorschau**- und **Office 365 Project Operations – Vorschau**-Lizenz ausgewählt sind und wählen Sie **Änderungen speichern**.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="7e4f9-141">Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="7e4f9-142">Ein neues Projekt in LCS starten</span><span class="sxs-lookup"><span data-stu-id="7e4f9-142">Start a new project in LCS</span></span>

<span data-ttu-id="7e4f9-143">Erstellen Sie ein neues LCS-Projekt wie im Thema [Ein neues Projekt in LCS starten](create-lcs-project.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="7e4f9-144">Einem LCS-Projekt ein Azure-Abonnement hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7e4f9-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="7e4f9-145">Befolgen Sie zum Ausführen dieser Aufgabe die Schritte im Thema [Einem LCS-Projekt ein Azure-Abonnement hinzufügen](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="7e4f9-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="7e4f9-146">Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit</span><span class="sxs-lookup"><span data-stu-id="7e4f9-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="7e4f9-147">Befolgen Sie die Anweisungen im Thema [Eine neue Umgebung bereitstellen](resource-provision-new-environment.md), um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="7e4f9-148">Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="7e4f9-149">CDS-Einrichtungs- und Konfigurationsdaten installieren</span><span class="sxs-lookup"><span data-stu-id="7e4f9-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="7e4f9-150">Installieren Sie CDS-Einrichtungs- und Konfigurationsdaten wie im Thema [Konfigurationsdaten in Common Data Service einrichten und anwenden](resource-apply-pro-setup-config-data.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="7e4f9-151">Führen Sie diesen Schritt erst aus, nachdem die Finance-Demo-Umgebung bereitgestellt und die Demo-Daten in FO bereit sind.</span><span class="sxs-lookup"><span data-stu-id="7e4f9-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
