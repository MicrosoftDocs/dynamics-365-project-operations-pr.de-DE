---
title: Eine neue Umgebung bereitstellen
description: Dieses Thema enthält Informationen zum Bereitstellen einer neuen Project Operations-Umgebung.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076411"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="e6d41-103">Eine neue Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="e6d41-103">Provision a new environment</span></span>

<span data-ttu-id="e6d41-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="e6d41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e6d41-105">Dieses Thema enthält Informationen zum Bereitstellen einer neuen Dynamics 365 Project Operations-Umgebung für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e6d41-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="e6d41-106">Automatisierte Project Operations-Bereitstellung in einem LCS-Projekt aktivieren</span><span class="sxs-lookup"><span data-stu-id="e6d41-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="e6d41-107">Führen Sie die folgenden Schritte aus, um den automatisierten Project Operations-Bereitstellungs-Flow für Ihr LCS-Projekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e6d41-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="e6d41-108">Navigieren Sie zu [LCS](https://lcs.dynamics.com/v2), und wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="e6d41-109">Wählen Sie in der Liste **Vorschaufunktion** die Option **Project Operations-Funktion** und dann **Vorschaufunktion aktiviert** aus, um Project Operations zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e6d41-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e6d41-110">Dieser Schritt wird nur einmal pro LCS-Projekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6d41-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="e6d41-111">Eine Project Operations-Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="e6d41-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="e6d41-112">Öffnen Sie eine neue Dynamics 365 Finance [Demo-Umgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) oder [Sandbox/Produktionsumgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e6d41-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="e6d41-113">Durchlaufen Sie den Assistenten zur **Umgebungsbereitstellung**.</span><span class="sxs-lookup"><span data-stu-id="e6d41-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e6d41-114">Stellen Sie sicher, dass die ausgewählte Anwendungsversion 10.0.13 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="e6d41-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="e6d41-115">Um Project Operations bereitzustellen, wählen Sie unter **Erweiterte Einstellungen** **Common Data Service** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="e6d41-116">Aktivieren Sie die **Common Data Service-Einstellung** , indem Sie **Ja** auswählen und dann Informationen in die entsprechenden Felder eingeben:</span><span class="sxs-lookup"><span data-stu-id="e6d41-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="e6d41-117">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="e6d41-117">Name</span></span>
  - <span data-ttu-id="e6d41-118">Region</span><span class="sxs-lookup"><span data-stu-id="e6d41-118">Region</span></span>
  - <span data-ttu-id="e6d41-119">Sprache</span><span class="sxs-lookup"><span data-stu-id="e6d41-119">Language</span></span>
  - <span data-ttu-id="e6d41-120">Währung</span><span class="sxs-lookup"><span data-stu-id="e6d41-120">Currency</span></span>
 
5. <span data-ttu-id="e6d41-121">Wählen Sie im Feld **Common Data Service-Vorlage** **Project Operations** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="e6d41-122">Wählen Sie den Umgebungstyp für Ihre Bereitstellung aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="e6d41-123">Mit einer abonnementbasierten Testversion können Sie eine CDS-Umgebung 30 Tage lang bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e6d41-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Bereitstellungseinstellungen](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="e6d41-125">Wählen Sie **Zustimmen** aus, um die Vertragsbedingungen zu bestätigen, und dann **Fertig** , um zu den Bereitstellungseinstellungen zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="e6d41-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Bereitstellungseinwilligung](./media/2DeploymentConsent.png)

7. <span data-ttu-id="e6d41-127">Füllen Sie die verbleibenden erforderlichen Felder im Assistenten aus, und bestätigen Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="e6d41-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="e6d41-128">Die Zeit für die Umgebungsbereitstellung hängt vom Umgebungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="e6d41-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="e6d41-129">Die Bereitstellung kann bis zu sechs Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="e6d41-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="e6d41-130">Nach erfolgreichem Abschluss der Bereitstellung wird die Umgebung als **Bereitgestellt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6d41-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="e6d41-131">Um zu bestätigen, dass die Umgebung erfolgreich bereitgestellt wurde, wählen Sie **Anmelden** aus, und melden Sie sich zur Bestätigung bei der Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="e6d41-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-Umgebungsdetails](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="e6d41-133">Project Operations Finance-Demodaten anwenden (optionaler Schritt)</span><span class="sxs-lookup"><span data-stu-id="e6d41-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="e6d41-134">Wenden Sie die Project Operations Finance-Demodaten auf die in der Cloud gehostete Umgebung Servicerelease 10.0.13, wie in [diesem Artikel](resource-apply-finance-demo-data.md) beschrieben, an.</span><span class="sxs-lookup"><span data-stu-id="e6d41-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="e6d41-135">Aktualisierungen auf die Finance-Umgebung anwenden</span><span class="sxs-lookup"><span data-stu-id="e6d41-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="e6d41-136">Project Operations erfordert eine Finance-Umgebung mit Anwendungsversion **10.0.13 (10.0.569.20009)** oder höher.</span><span class="sxs-lookup"><span data-stu-id="e6d41-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="e6d41-137">Möglicherweise müssen Sie Qualitätsupdates auf Ihre Finance-Umgebung anwenden, um diese Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e6d41-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="e6d41-138">Wählen Sie in LCS auf der Seite **Umgebungsdetails** im Abschnitt **Verfügbare Updates** die Option **Aktualisierung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Aktualisierungen anzeigen](./media/5ViewUpdates.png)

2. <span data-ttu-id="e6d41-140">Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-140">On the **Binary updates** page, select **Save package.**</span></span>

![Paket speichern](./media/6SavePackage.png)

3. <span data-ttu-id="e6d41-142">Klicken Sie auf **Alle auswählen** , und wählen Sie dann **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-142">Click **Select all** and then select **Save package**.</span></span>

![Aktualisierungen überprüfen und speichern](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="e6d41-144">Geben Sie einen Namen und eine Beschreibung zum Paket ein, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="e6d41-145">Abhängig von der Internetverbindung kann dieser Vorgang einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="e6d41-145">Depending on the internet connection, this process might take some time.</span></span>

![Paket in Objektbibliothek hochladen](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="e6d41-147">Nachdem das Paket gespeichert wurde, wählen Sie **Fertig** aus, und speichern Sie dieses Paket in der Objektbibliothek in Ihrem LCS-Projekt.</span><span class="sxs-lookup"><span data-stu-id="e6d41-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="e6d41-148">Das Speichern und Validieren des Pakets kann ca. 15 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="e6d41-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="e6d41-149">Um das Update anzuwenden, navigieren Sie zur Seite **Umgebungsdetails** in LCS und wählen Sie **Verwalten** > **Aktualisierungen übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Umgebungen verwalten](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="e6d41-151">Wählen Sie in der Aktualisierungsliste das von Ihnen erstellte Paket und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aktualisierungen anwenden](./media/10ApplyUpdates.png)

<span data-ttu-id="e6d41-153">Die Wartung der Umgebung wird einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="e6d41-153">Environment servicing will take some time.</span></span> <span data-ttu-id="e6d41-154">Nach Abschluss des Vorgangs kehrt die Umgebung in den bereitgestellten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="e6d41-154">After it is complete, the environment will return to a deployed state.</span></span>

![Umgebungen bereitgestellt](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="e6d41-156">Eine Dual-Write-Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="e6d41-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="e6d41-157">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="e6d41-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e6d41-158">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="e6d41-159">Nachdem der Link vollständig ist, wählen Sie erneut **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="e6d41-160">Sie werden zu Dual Write in Finance weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e6d41-160">You will be redirected to Dual Write in Finance.</span></span>

![Mit CDS verknüpfen](./media/12LinktoCDS.png)

4. <span data-ttu-id="e6d41-162">Wählen Sie **Lösung anwenden** aus, um auf die Entitäten zuzugreifen, die in der Integration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e6d41-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Lösungen anwenden](./media/13ApplySolutions.png)

5. <span data-ttu-id="e6d41-164">Wählen Sie beide Lösungen, **Dynamics 365 Finance and Operations Dual Write Entity Map** und **Dynamics 365 Project Operations Dual Write Entity Maps** und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Lösungen bestätigen](./media/14ConfirmSolutions.png)

<span data-ttu-id="e6d41-166">Nachdem die Lösungen angewendet wurden, werden die Dual Write-Entitäten auf die Umgebung angewendet.</span><span class="sxs-lookup"><span data-stu-id="e6d41-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anwenden von Lösungen](./media/15ApplyingSolutions.png)

<span data-ttu-id="e6d41-168">Nachdem die Entitäten angewendet wurden, werden alle verfügbaren Zuordnungen in der Umgebung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e6d41-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Zuordnungen für duales Schreiben](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="e6d41-170">Die Datenentitäten nach der Aktualisierung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="e6d41-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="e6d41-171">Navigieren Sie in Finance zum Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="e6d41-171">In Finance, go to the **Data management** workspace.</span></span>

![Datenverwaltungsarbeitsbereich](./media/16DataManagement.png)

2. <span data-ttu-id="e6d41-173">Wählen Sie die Kachel **Framework-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-173">Select the **Framework parameters** tile.</span></span>

![Framework-Parameter](./media/17FrameworkParameters.png)

3. <span data-ttu-id="e6d41-175">Wählen Sie auf der Seite **Entitätseinstellungen** die Option **Entitätsliste aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitätsliste aktualisieren](./media/18RefreshEntityList.png)

<span data-ttu-id="e6d41-177">Die Aktualisierung dauert ungefähr 20 Minuten.</span><span class="sxs-lookup"><span data-stu-id="e6d41-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="e6d41-178">Sie erhalten eine Benachrichtigung, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e6d41-178">You will receive an alert when it is complete.</span></span>

![Bestätigung aktualisieren](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="e6d41-180">Duales Schreiben für Project Operations-Zuordnungen ausführen</span><span class="sxs-lookup"><span data-stu-id="e6d41-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="e6d41-181">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="e6d41-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e6d41-182">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="e6d41-183">Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e6d41-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="e6d41-184">Starten Sie die Zuordnungen wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6d41-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="e6d41-185">Stellen Sie sicher, dass Sie die angegebene Reihenfolge einhalten.</span><span class="sxs-lookup"><span data-stu-id="e6d41-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="e6d41-186">**Entitätszuordnung**</span><span class="sxs-lookup"><span data-stu-id="e6d41-186">**Entity Map**</span></span> | <span data-ttu-id="e6d41-187">**Entität aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="e6d41-187">**Refresh entity**</span></span> | <span data-ttu-id="e6d41-188">**Erste Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="e6d41-188">**Initial sync**</span></span> | <span data-ttu-id="e6d41-189">**Master für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="e6d41-189">**Master for initial sync**</span></span> | <span data-ttu-id="e6d41-190">**Voraussetzungen ausführen**</span><span class="sxs-lookup"><span data-stu-id="e6d41-190">**Run prerequisites**</span></span> | <span data-ttu-id="e6d41-191">**Voraussetzungen für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="e6d41-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="e6d41-192">**Projektressourcenrollen für alle Unternehmen(bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="e6d41-193">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-193">No</span></span> | <span data-ttu-id="e6d41-194">Ja</span><span class="sxs-lookup"><span data-stu-id="e6d41-194">Yes</span></span> | <span data-ttu-id="e6d41-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e6d41-195">Common Data Service</span></span> | <span data-ttu-id="e6d41-196">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-196">No</span></span> | <span data-ttu-id="e6d41-197">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-197">N\A</span></span> |
| <span data-ttu-id="e6d41-198">**Juristische Personen (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="e6d41-199">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-199">No</span></span> | <span data-ttu-id="e6d41-200">Ja</span><span class="sxs-lookup"><span data-stu-id="e6d41-200">Yes</span></span> | <span data-ttu-id="e6d41-201">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="e6d41-201">Finance and Operations apps</span></span> | <span data-ttu-id="e6d41-202">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-202">No</span></span> | <span data-ttu-id="e6d41-203">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-203">N\A</span></span> |
| <span data-ttu-id="e6d41-204">**Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="e6d41-205">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-205">No</span></span> | <span data-ttu-id="e6d41-206">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-206">No</span></span> | <span data-ttu-id="e6d41-207">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-207">N\A</span></span> | <span data-ttu-id="e6d41-208">Ja</span><span class="sxs-lookup"><span data-stu-id="e6d41-208">Yes</span></span> | <span data-ttu-id="e6d41-209">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-209">No</span></span> |
| <span data-ttu-id="e6d41-210">**Projektvertragszeilen (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="e6d41-211">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-211">No</span></span> | <span data-ttu-id="e6d41-212">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-212">No</span></span> | <span data-ttu-id="e6d41-213">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-213">N\A</span></span> | <span data-ttu-id="e6d41-214">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-214">No</span></span> | <span data-ttu-id="e6d41-215">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-215">No</span></span> |
| <span data-ttu-id="e6d41-216">**Integrationsentität für die Projekttransaktionsbeziehungen (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="e6d41-217">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-217">No</span></span> | <span data-ttu-id="e6d41-218">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-218">No</span></span> | <span data-ttu-id="e6d41-219">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-219">N\A</span></span> | <span data-ttu-id="e6d41-220">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-220">No</span></span> | <span data-ttu-id="e6d41-221">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-221">N\A</span></span> |
| <span data-ttu-id="e6d41-222">**Vertragszeilenmeilensteine der Project Operations-Integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="e6d41-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-223">No</span></span> | <span data-ttu-id="e6d41-224">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-224">No</span></span> | <span data-ttu-id="e6d41-225">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-225">N\A</span></span> | <span data-ttu-id="e6d41-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-226">No</span></span> | <span data-ttu-id="e6d41-227">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-227">N\A</span></span> |
| <span data-ttu-id="e6d41-228">**Project Operations-Integrationsentität für Ausgabenschätzungen (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="e6d41-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-229">No</span></span> | <span data-ttu-id="e6d41-230">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-230">No</span></span> | <span data-ttu-id="e6d41-231">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-231">N\A</span></span> | <span data-ttu-id="e6d41-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-232">No</span></span> | <span data-ttu-id="e6d41-233">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-233">N\A</span></span> |
| <span data-ttu-id="e6d41-234">**Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="e6d41-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-235">No</span></span> | <span data-ttu-id="e6d41-236">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-236">No</span></span> | <span data-ttu-id="e6d41-237">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-237">N\A</span></span> | <span data-ttu-id="e6d41-238">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-238">No</span></span> | <span data-ttu-id="e6d41-239">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-239">N\A</span></span> |
| <span data-ttu-id="e6d41-240">**Exportentität für Projektkosten der Project Operations-Integration (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="e6d41-241">Ja</span><span class="sxs-lookup"><span data-stu-id="e6d41-241">Yes</span></span> | <span data-ttu-id="e6d41-242">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-242">No</span></span> | <span data-ttu-id="e6d41-243">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-243">N\A</span></span> | <span data-ttu-id="e6d41-244">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-244">No</span></span> | <span data-ttu-id="e6d41-245">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-245">N\A</span></span> |
| <span data-ttu-id="e6d41-246">**Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e6d41-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e6d41-247">Ja</span><span class="sxs-lookup"><span data-stu-id="e6d41-247">Yes</span></span> | <span data-ttu-id="e6d41-248">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-248">No</span></span> | <span data-ttu-id="e6d41-249">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-249">N\A</span></span> | <span data-ttu-id="e6d41-250">Nr.</span><span class="sxs-lookup"><span data-stu-id="e6d41-250">No</span></span> | <span data-ttu-id="e6d41-251">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6d41-251">N\A</span></span> |


4. <span data-ttu-id="e6d41-252">Um die Entität zu aktualisieren, wählen Sie den Zuordnungsnamen und dann **Entitäten aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Zuordnung aktualisieren](./media/20RefreshMapping.png)

5. <span data-ttu-id="e6d41-254">Führen Sie nach dem Abschluss der Aktualisierung die Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="e6d41-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="e6d41-255">Bevor Sie die nächste Zuordnung aktivieren, stellen Sie sicher, dass sich die Zuordnung in der Tabelle im Status **Wird ausgeführt** befindet.</span><span class="sxs-lookup"><span data-stu-id="e6d41-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="e6d41-256">Das Ausführen von Zuordnungen mit einer größeren Anzahl von Voraussetzungen kann einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="e6d41-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="e6d41-257">Um eine Zuordnung mit Voraussetzungen auszuführen, aktivieren Sie die Umschalttaste **Zugehörige Entitätszuordnungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="e6d41-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="e6d41-258">Wenn die Tabelle angibt, dass **Voraussetzungen für die Erstsynchronisierung** auf **Nein** festgelegt ist, stellen Sie sicher, dass die Kennzeichnung **Erstsynchronisation** in allen erforderlichen Voraussetzungszuordnungen auf **Aus** festgelegt ist, bevor Sie sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6d41-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Zuordnung ausführen](./media/21RunMap.png)

6. <span data-ttu-id="e6d41-260">Überprüfen Sie, ob alle projektbezogenen Zuordnungen sich im Status „Wird ausgeführt“ befinden.</span><span class="sxs-lookup"><span data-stu-id="e6d41-260">Validate all project related maps are in the running state.</span></span>

![Alle Zuordnungen werden ausgeführt](./media/22AllMapsRunning.png)

<span data-ttu-id="e6d41-262">Ihre Project Operations-Umgebung ist jetzt bereitgestellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e6d41-262">Your Project Operations environment is now provisioned and configured.</span></span>
