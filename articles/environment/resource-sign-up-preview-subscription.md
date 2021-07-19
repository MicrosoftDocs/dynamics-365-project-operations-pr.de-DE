---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen von Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334826"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="a80cc-103">Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden</span><span class="sxs-lookup"><span data-stu-id="a80cc-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="a80cc-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="a80cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a80cc-105">Dieses Thema erklärt, wie Sie das Test-Angebot abonnieren und die Project Operations Umgebung für ressourcenbasierte/nicht vorrätige Szenarien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a80cc-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a80cc-106">Prerequisites</span></span>
- <span data-ttu-id="a80cc-107">Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="a80cc-108">Sie können einen Mandanten während der ersten Angebotseinlösung erstellen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="a80cc-109">Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a80cc-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="a80cc-110">Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/en-us/free/) verwenden, um zu starten.</span><span class="sxs-lookup"><span data-stu-id="a80cc-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="a80cc-111">Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="a80cc-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a80cc-112">Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="a80cc-113">Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="a80cc-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="a80cc-114">Tests sind im Mandanten nur einmal verwendbar.</span><span class="sxs-lookup"><span data-stu-id="a80cc-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="a80cc-115">Sie können einen Test nur ein einziges Mal ausführen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-115">You can only run a trial one time.</span></span> <span data-ttu-id="a80cc-116">Wir empfehlen, dass Sie für den Test einen neuen Mandanten erstellen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="a80cc-117">Dynamics 365 Project Operations (CE) - Vorschau Test</span><span class="sxs-lookup"><span data-stu-id="a80cc-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="a80cc-118">Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="a80cc-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="a80cc-119">Lösen Sie den ersten Angebotscode ein, **Dynamics 365 Project Operations** hier [Project Operations Test](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="a80cc-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="a80cc-120">Bestätigen Sie Ihre Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a80cc-120">Confirm your order.</span></span>

  <span data-ttu-id="a80cc-121">Sie sehen, dass das Bestätigungsangebot erfolgreich eingelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="a80cc-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="a80cc-122">Dynamics 365 Finance-Vorschautestversion</span><span class="sxs-lookup"><span data-stu-id="a80cc-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="a80cc-123">Gehen Sie zu [Dynamics 365 for Finance Vorschau Test](https://aka.ms/trypoche) und wiederholen Sie die Schritte aus dem vorherigen Abschnitt mit dem Angebot, Melden Sie sich für die Cloud Hosted Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="a80cc-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="a80cc-124">Lizenzen zuweisen</span><span class="sxs-lookup"><span data-stu-id="a80cc-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a80cc-125">Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="a80cc-126">Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="a80cc-127">Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="a80cc-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="a80cc-128">Vergewissern Sie sich, dass die **Dynamics 365 Project Operations** Lizenz ausgewählt wurde und wählen Sie **Änderungen speichern**.</span><span class="sxs-lookup"><span data-stu-id="a80cc-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="a80cc-129">Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a80cc-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="a80cc-130">Ein neues Projekt in LCS starten</span><span class="sxs-lookup"><span data-stu-id="a80cc-130">Start a new project in LCS</span></span>

<span data-ttu-id="a80cc-131">Erstellen Sie ein neues LCS-Projekt wie im Thema [Ein neues Projekt in LCS starten](create-lcs-project.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a80cc-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="a80cc-132">Einem LCS-Projekt ein Azure-Abonnement hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a80cc-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="a80cc-133">Befolgen Sie zum Ausführen dieser Aufgabe die Schritte im Thema [Einem LCS-Projekt ein Azure-Abonnement hinzufügen](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="a80cc-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="a80cc-134">Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit</span><span class="sxs-lookup"><span data-stu-id="a80cc-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="a80cc-135">Befolgen Sie die Anweisungen im Thema [Eine neue Umgebung bereitstellen](resource-provision-new-environment.md), um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="a80cc-136">Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau.</span><span class="sxs-lookup"><span data-stu-id="a80cc-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="a80cc-137">CDS-Einrichtungs- und Konfigurationsdaten installieren</span><span class="sxs-lookup"><span data-stu-id="a80cc-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="a80cc-138">Installieren Sie CDS-Einrichtungs- und Konfigurationsdaten wie im Thema [Konfigurationsdaten in Common Data Service einrichten und anwenden](resource-apply-pro-setup-config-data.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a80cc-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="a80cc-139">Schließen Sie diesen Schritt erst ab, wenn die Finance-Demo-Umgebung bereitgestellt ist und die Demo-Daten bereitstehen.</span><span class="sxs-lookup"><span data-stu-id="a80cc-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
