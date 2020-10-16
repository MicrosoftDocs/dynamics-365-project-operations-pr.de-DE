---
title: Einem LCS-Projekt ein Azure-Abonnement hinzufügen
description: Dieses Thema enthält Informationen zum Verbinden Ihres Azure-Abonnements mit einem LCS-Projekt.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948871"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="9132a-103">Einem LCS-Projekt ein Azure-Abonnement hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9132a-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="9132a-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="9132a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9132a-105">In der Cloud gehostete Umgebungen müssen mit einem vorhandenen Azure-Abonnement bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9132a-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="9132a-106">Dieses Thema erklärt, wie Ihr vorhandenes Azure-Abonnement mit einem LCS-Projekt verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="9132a-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="9132a-107">Administratoreinwilligung erteilen</span><span class="sxs-lookup"><span data-stu-id="9132a-107">Grant admin consent</span></span>

1. <span data-ttu-id="9132a-108">Wählen Sie im Abschnitt **Umgebungen** in Ihrem LCS-Projekt die **Microsoft Azure-Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Einstellungen für die Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="9132a-110">Wählen Sie auf der Seite **Projekteinstellungen** auf der Registerkarte **Azure-Abonnements** die Option **Autorisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="9132a-111">Dadurch können Umgebungen für dieses Projekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9132a-111">This allows environments to be deployed to this project.</span></span>

![Azure-Konnektoren](./media/2AzureConnectors.png)

3. <span data-ttu-id="9132a-113">Wählen Sie erneut **Autorisieren** aus, um die Administratoreinwilligung zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="9132a-113">Select **Authorize** again to provide admin consent.</span></span>

![Administratoreinwilligung erteilen](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="9132a-115">Die Berechtigungsanforderung akzeptieren</span><span class="sxs-lookup"><span data-stu-id="9132a-115">Accept the permissions request.</span></span>

![Die Berechtigungsanforderung akzeptieren](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="9132a-117">Die Autorisierung ist jetzt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9132a-117">The authorization is now complete.</span></span> 

![Autorisierung erfolgreich](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="9132a-119">Dynamics Deployment Services den Zugriff auf Ihr Azure-Abonnement ermöglichen</span><span class="sxs-lookup"><span data-stu-id="9132a-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="9132a-120">Navigieren Sie zur [Microsoft Azure-Fakturierung](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), und wählen Sie Ihr Abonnement aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="9132a-121">Dynamics Deployment Services muss auf dieses Abonnement zugreifen, um Umgebungen bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="9132a-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure-Abonnementdetails](./media/6AzureSubscription.png)

2. <span data-ttu-id="9132a-123">Wählen Sie **Access Control (IAM)** im Navigationsbereich und dann **Rollenzuweisung hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="9132a-124">Wählen Sie im Schieberegler auf der rechten Seite **Rolle als Beitragender** aus. Suchen Sie **Dynamics Deployment Services**, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="9132a-125">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-125">Select **Save**.</span></span>

![Abonnementzugriff](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="9132a-127">Einem LCS-Projekt einen Azure-Konnektor hinzufügen</span><span class="sxs-lookup"><span data-stu-id="9132a-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="9132a-128">Wählen Sie auf der Seite **Microsoft Azure-Einstellungen** in Ihrem LCS-Projekt **Hinzufügen** aus, um einen neuen Konnektor hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9132a-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="9132a-129">Geben Sie die ID Ihres Azure-Abonnements ein.</span><span class="sxs-lookup"><span data-stu-id="9132a-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="9132a-130">Sie finden die ID Ihres Azure-Abonnements im [Azure-Portal](https://ms.portal.azure.com/) unter **Einstellungen** unten links im Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="9132a-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="9132a-131">Wählen Sie im Feld **Zur Verwendung von Azure Resource Manager konfigurieren** **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="9132a-132">Stellen Sie sicher, dass die AAD-Mandantendomäne des Azure-Abonnements mit dem Azure-Abonnement der Domäne, die Sie verwenden, übereinstimmt, und wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="9132a-133">Wählen Sie im Bildschirm **Microsoft Azure-Einrichtung** zur Bestätigung **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="9132a-134">Wenn auf diesem Bildschirm eine Fehlermeldung angezeigt wird, kehren Sie zum Abschnitt [Dynamics Deployment Services den Zugriff auf Ihr Azure-Abonnement ermöglichen](#provide) in diesem Thema zurück, und stellen Sie sicher, dass Sie alle Schritte abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="9132a-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="9132a-135">Laden Sie das Azure-Verwaltungszertifikat in einen lokalen Ordner auf Ihrem Computer herunter, und laden Sie es anschließend in das Azure-Verwaltungsportal hoch, indem Sie zu **Einstellungen** > **Verwaltungszertifikate** navigieren.</span><span class="sxs-lookup"><span data-stu-id="9132a-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="9132a-136">Mit diesem Zertifikat kann LCS in Ihrem Namen mit Azure kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9132a-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="9132a-137">Sie können diesen Schritt überspringen, wenn Ihr Benutzer Zugriff auf das Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="9132a-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="9132a-138">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-138">Select  **Next**.</span></span>
8. <span data-ttu-id="9132a-139">Wählen Sie die Azure-Region aus, in der die Bereitstellung erfolgen soll, und wählen Sie ein Rechenzentrum aus, das sich in der Nähe des Ortes befindet, an dem Sie dieses System verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9132a-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="9132a-140">Wählen Sie **Verbinden** aus.</span><span class="sxs-lookup"><span data-stu-id="9132a-140">Select  **Connect**.</span></span>

<span data-ttu-id="9132a-141">Sie haben Ihr Azure-Abonnement erfolgreich verbunden.</span><span class="sxs-lookup"><span data-stu-id="9132a-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="9132a-142">Sie können nun Cloud-gehostete Dynamics 365 Finance-Umgebungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9132a-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


