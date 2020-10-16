---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen von Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948872"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8d172-103">Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden</span><span class="sxs-lookup"><span data-stu-id="8d172-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8d172-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="8d172-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8d172-105">In diesem Thema wird erläutert, wie Sie das Vorschau-/Partnerangebot abonnieren und die Project Operations-Umgebung bei Szenarien für vorrätige/nicht vorrätige Ressourcen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8d172-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d172-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8d172-106">Prerequisites</span></span>

- <span data-ttu-id="8d172-107">Sie erhalten eine E-Mail, in der Sie zur Teilnahme an der Vorschau eingeladen werden.</span><span class="sxs-lookup"><span data-stu-id="8d172-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="8d172-108">Sie können eine Vorschau auf der [Project Operations-Website](https://dynamics.microsoft.com/en-us/project-operations/overview/) anfordern.</span><span class="sxs-lookup"><span data-stu-id="8d172-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="8d172-109">Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.</span><span class="sxs-lookup"><span data-stu-id="8d172-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="8d172-110">Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d172-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8d172-111">Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/en-us/free/) verwenden, um zu starten.</span><span class="sxs-lookup"><span data-stu-id="8d172-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8d172-112">Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="8d172-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="8d172-113">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="8d172-113">Subscribe</span></span>

<span data-ttu-id="8d172-114">Wenn Ihre [Vorschauanforderung](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) genehmigt wird, erhalten Sie zwei Angebote von Microsoft per E-Mail.</span><span class="sxs-lookup"><span data-stu-id="8d172-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="8d172-115">Mit diesen Angeboten können Sie die Project Operations-Vorschau bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="8d172-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="8d172-116">Dynamics 365 Project Operations – Vorschau-Testversion</span><span class="sxs-lookup"><span data-stu-id="8d172-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="8d172-117">Dynamics 365 for Finance and Operations-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="8d172-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d172-118">Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d172-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8d172-119">Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="8d172-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="8d172-120">Dynamics 365 Project Operations – Vorschau-Testversion</span><span class="sxs-lookup"><span data-stu-id="8d172-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="8d172-121">Lösen Sie das erste Angebot, **Dynamics 365 Project Operations-Testversion**, mit der in Ihrer Begrüßungs-E-Mail angegebenen URL ein.</span><span class="sxs-lookup"><span data-stu-id="8d172-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Erstes Angebot](./media/1FirstOffer.png)

2. <span data-ttu-id="8d172-123">Stellen Sie sicher, dass Sie als der Benutzer angemeldet sind, der zu der Organisation gehört, die den Dienst abonniert.</span><span class="sxs-lookup"><span data-stu-id="8d172-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="8d172-124">Fahren Sie mit dem Einlösen des Angebots fort.</span><span class="sxs-lookup"><span data-stu-id="8d172-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="8d172-125">Wählen Sie **Ja, zu meinem Konto hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="8d172-125">Select **Yes, add it to my account**.</span></span>

![Angebot einlösen](./media/2RedeemFirstOffer.png)

![Angebot bestätigen](./media/3ConfirmFirstOffer.png)

![Angebot eingelöst](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8d172-129">Dynamics 365 Finance-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="8d172-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8d172-130">Wiederholen Sie dieselben Schritte mit dem zweiten Angebot aus der Begrüßungs-E-Mail.</span><span class="sxs-lookup"><span data-stu-id="8d172-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="8d172-131">Lizenzen zuweisen</span><span class="sxs-lookup"><span data-stu-id="8d172-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d172-132">Sie benötigen Administratorzugriff auf das Office 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d172-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8d172-133">Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern Lizenzen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8d172-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office-Verwaltungsportal](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="8d172-135">Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="8d172-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Lizenzen zuweisen](./media/6AssignLicenses.png)

3. <span data-ttu-id="8d172-137">Stellen Sie sicher, dass die Project Operations-Lizenz ausgewählt wurde, und wählen Sie **Änderungen speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8d172-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8d172-138">Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8d172-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8d172-139">Ein neues Projekt in LCS starten</span><span class="sxs-lookup"><span data-stu-id="8d172-139">Start a new project in LCS</span></span>

<span data-ttu-id="8d172-140">Erstellen Sie ein neues LCS-Projekt wie im Thema [Ein neues Projekt in LCS starten](create-lcs-project.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d172-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8d172-141">Einem LCS-Projekt ein Azure-Abonnement hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8d172-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8d172-142">Befolgen Sie zum Ausführen dieser Aufgabe die Schritte im Thema [Einem LCS-Projekt ein Azure-Abonnement hinzufügen](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="8d172-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8d172-143">Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit</span><span class="sxs-lookup"><span data-stu-id="8d172-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8d172-144">Befolgen Sie die Anweisungen im Thema [Eine neue Umgebung bereitstellen](resource-provision-new-environment.md), um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8d172-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8d172-145">Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="8d172-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8d172-146">CDS-Einrichtungs- und Konfigurationsdaten installieren</span><span class="sxs-lookup"><span data-stu-id="8d172-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8d172-147">Installieren Sie CDS-Einrichtungs- und Konfigurationsdaten wie im Thema [Konfigurationsdaten in Common Data Service einrichten und anwenden](resource-apply-pro-setup-config-data.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8d172-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

