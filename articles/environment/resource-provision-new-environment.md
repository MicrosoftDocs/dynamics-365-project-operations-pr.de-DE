---
title: Eine neue Umgebung bereitstellen
description: Dieses Thema enthält Informationen zum Bereitstellen einer neuen Project Operations-Umgebung.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950533"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="31a76-103">Eine neue Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="31a76-103">Provision a new environment</span></span>

<span data-ttu-id="31a76-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="31a76-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="31a76-105">Dieses Thema enthält Informationen zur Bereitstellung einer neuen Dynamics 365 Project Operations-Umgebung für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="31a76-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="31a76-106">Automatisierte Project Operations-Bereitstellung in einem LCS-Projekt aktivieren</span><span class="sxs-lookup"><span data-stu-id="31a76-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="31a76-107">Führen Sie die folgenden Schritte aus, um den automatisierten Project Operations-Bereitstellungs-Flow für Ihr LCS-Projekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="31a76-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="31a76-108">Navigieren Sie zu [LCS](https://lcs.dynamics.com/v2), und wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="31a76-109">Wählen Sie in der Liste **Vorschaufunktion** die Option **Project Operations-Funktion** und dann **Vorschaufunktion aktiviert** aus, um Project Operations zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="31a76-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="31a76-110">Dieser Schritt wird nur einmal pro LCS-Projekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31a76-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="31a76-111">Eine Project Operations-Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="31a76-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="31a76-112">Öffnen Sie eine neue Dynamics 365 Finance [Demo-Umgebungs-](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) oder [Sandbox/Produktionsumgebungs-](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="31a76-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="31a76-113">Durchlaufen Sie den Assistenten zur **Umgebungsbereitstellung**.</span><span class="sxs-lookup"><span data-stu-id="31a76-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="31a76-114">Stellen Sie sicher, dass die ausgewählte Anwendungsversion 10.0.13 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="31a76-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="31a76-115">Um Project Operations bereitzustellen, wählen Sie unter **Erweiterte Einstellungen** **Common Data Service** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="31a76-116">Aktivieren Sie die **Common Data Service-Einstellung**, indem Sie **Ja** auswählen und dann Informationen in die entsprechenden Felder eingeben:</span><span class="sxs-lookup"><span data-stu-id="31a76-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="31a76-117">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="31a76-117">Name</span></span>
  - <span data-ttu-id="31a76-118">Region</span><span class="sxs-lookup"><span data-stu-id="31a76-118">Region</span></span>
  - <span data-ttu-id="31a76-119">Sprache</span><span class="sxs-lookup"><span data-stu-id="31a76-119">Language</span></span>
  - <span data-ttu-id="31a76-120">Währung</span><span class="sxs-lookup"><span data-stu-id="31a76-120">Currency</span></span>
 
5. <span data-ttu-id="31a76-121">Wählen Sie im Feld **Common Data Service-Vorlage** **Project Operations** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="31a76-122">Wählen Sie den Umgebungstyp für Ihre Bereitstellung aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="31a76-123">Mit einer abonnementbasierten Testversion können Sie eine CDS-Umgebung 30 Tage lang bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="31a76-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Bereitstellungseinstellungen](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="31a76-125">Wählen Sie **Zustimmen** aus, um die Vertragsbedingungen zu bestätigen, und dann **Fertig**, um zu den Bereitstellungseinstellungen zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="31a76-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Bereitstellungseinwilligung](./media/2DeploymentConsent.png)

7. <span data-ttu-id="31a76-127">Optional – Wenden Sie Demodaten auf die Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="31a76-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="31a76-128">Gehen Sie zu **Erweiterte Einstellungen**, wählen Sie **Passen Sie die SQL-Datenbankkonfiguration an** und setzen **Geben Sie ein DataSet für die Anwendungsdatenbank an** auf **Demo**.</span><span class="sxs-lookup"><span data-stu-id="31a76-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="31a76-129">Füllen Sie die verbleibenden erforderlichen Felder im Assistenten aus, und bestätigen Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="31a76-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="31a76-130">Die Zeit zum Bereitstellen der Umgebung hängt vom Umgebungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="31a76-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="31a76-131">Die Bereitstellung kann bis zu sechs Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="31a76-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="31a76-132">Nach erfolgreichem Abschluss der Bereitstellung wird die Umgebung als **Bereitgestellt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="31a76-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="31a76-133">Um zu bestätigen, dass die Umgebung erfolgreich bereitgestellt wurde, wählen Sie **Anmeldung** und melden Sie sich zur Bestätigung bei der Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="31a76-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-Umgebungsdetails](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="31a76-135">Aktualisierungen auf die Finance-Umgebung anwenden</span><span class="sxs-lookup"><span data-stu-id="31a76-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="31a76-136">Project Operations erfordert eine Finance-Umgebung mit Anwendungsversion **10.0.13 (10.0.569.20009)** oder höher.</span><span class="sxs-lookup"><span data-stu-id="31a76-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="31a76-137">Möglicherweise müssen Sie Qualitätsupdates auf Ihre Finance-Umgebung anwenden, um diese Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31a76-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="31a76-138">Wählen Sie in LCS auf der Seite **Umgebungsdetails** im Abschnitt **Verfügbare Updates** die Option **Aktualisierung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Aktualisierungen anzeigen](./media/5ViewUpdates.png)

2. <span data-ttu-id="31a76-140">Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-140">On the **Binary updates** page, select **Save package.**</span></span>

![Paket speichern](./media/6SavePackage.png)

3. <span data-ttu-id="31a76-142">Klicken Sie auf **Alle auswählen**, und wählen Sie dann **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-142">Click **Select all** and then select **Save package**.</span></span>

![Aktualisierungen überprüfen und speichern](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="31a76-144">Geben Sie einen Namen und eine Beschreibung zum Paket ein, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="31a76-145">Abhängig von der Internetverbindung kann dieser Vorgang einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="31a76-145">Depending on the internet connection, this process might take some time.</span></span>

![Paket in Objektbibliothek hochladen](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="31a76-147">Nachdem das Paket gespeichert wurde, wählen Sie **Fertig** aus, und speichern Sie dieses Paket in der Objektbibliothek in Ihrem LCS-Projekt.</span><span class="sxs-lookup"><span data-stu-id="31a76-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="31a76-148">Das Speichern und Validieren des Pakets kann ca. 15 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="31a76-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="31a76-149">Um das Update anzuwenden, navigieren Sie zur Seite **Umgebungsdetails** in LCS und wählen Sie **Verwalten** > **Aktualisierungen übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Umgebungen verwalten](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="31a76-151">Wählen Sie in der Aktualisierungsliste das von Ihnen erstellte Paket und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aktualisierungen anwenden](./media/10ApplyUpdates.png)

<span data-ttu-id="31a76-153">Die Wartung der Umgebung wird einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="31a76-153">Environment servicing will take some time.</span></span> <span data-ttu-id="31a76-154">Nach Abschluss des Vorgangs kehrt die Umgebung in den bereitgestellten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="31a76-154">After it is complete, the environment will return to a deployed state.</span></span>

![Umgebungen bereitgestellt](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="31a76-156">Eine Dual-Write-Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="31a76-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="31a76-157">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="31a76-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="31a76-158">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="31a76-159">Nachdem der Link vollständig ist, wählen Sie erneut **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="31a76-160">Sie werden zu Dual Write in Finance weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="31a76-160">You will be redirected to Dual Write in Finance.</span></span>

![Mit CDS verknüpfen](./media/12LinktoCDS.png)

4. <span data-ttu-id="31a76-162">Wählen Sie **Lösung anwenden** aus, um auf die Entitäten zuzugreifen, die in der Integration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="31a76-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Lösungen anwenden](./media/13ApplySolutions.png)

5. <span data-ttu-id="31a76-164">Wählen Sie beide Lösungen, **Dynamics 365 Finance and Operations Dual Write Entity Map** und **Dynamics 365 Project Operations Dual Write Entity Maps**, und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Lösungen bestätigen](./media/14ConfirmSolutions.png)

<span data-ttu-id="31a76-166">Nachdem die Lösungen angewendet wurden, werden die Dual Write-Entitäten auf die Umgebung angewendet.</span><span class="sxs-lookup"><span data-stu-id="31a76-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anwenden von Lösungen](./media/15ApplyingSolutions.png)

<span data-ttu-id="31a76-168">Nachdem die Entitäten angewendet wurden, werden alle verfügbaren Zuordnungen in der Umgebung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="31a76-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Zuordnungen für duales Schreiben](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="31a76-170">Die Datenentitäten nach der Aktualisierung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="31a76-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="31a76-171">Navigieren Sie in Finance zum Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="31a76-171">In Finance, go to the **Data management** workspace.</span></span>

![Datenverwaltungsarbeitsbereich](./media/16DataManagement.png)

2. <span data-ttu-id="31a76-173">Wählen Sie die Kachel **Framework-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-173">Select the **Framework parameters** tile.</span></span>

![Framework-Parameter](./media/17FrameworkParameters.png)

3. <span data-ttu-id="31a76-175">Wählen Sie auf der Seite **Entitätseinstellungen** die Option **Entitätsliste aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitätsliste aktualisieren](./media/18RefreshEntityList.png)

<span data-ttu-id="31a76-177">Die Aktualisierung dauert ungefähr 20 Minuten.</span><span class="sxs-lookup"><span data-stu-id="31a76-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="31a76-178">Sie erhalten eine Benachrichtigung, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="31a76-178">You will receive an alert when it is complete.</span></span>

![Bestätigung aktualisieren](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="31a76-180">Aktualisieren Sie die Sicherheitseinstellungen für Project Operations in Dataverse</span><span class="sxs-lookup"><span data-stu-id="31a76-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="31a76-181">Gehen sie Project Operations in Ihrer Dataverse Umgebung.</span><span class="sxs-lookup"><span data-stu-id="31a76-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="31a76-182">Gehen Sie zu **Einstellungen** > **Sicherheit** > **Sicherheitsrollen**.</span><span class="sxs-lookup"><span data-stu-id="31a76-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="31a76-183">Auf der Seite **Sicherheitsrollen** in der Liste der Rollen wählen Sie **Dual-Write-App-Benutzer** und wählen Sie die Registerkarte **Benutzerdefinierte Entitäten**.</span><span class="sxs-lookup"><span data-stu-id="31a76-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="31a76-184">Stellen Sie sicher, dass die Rolle Berechtigung für **Lesen** und **Anfürgen** hat:</span><span class="sxs-lookup"><span data-stu-id="31a76-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="31a76-185">**Währungswechselkurstyp eingeben**</span><span class="sxs-lookup"><span data-stu-id="31a76-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="31a76-186">**Kontenplan**</span><span class="sxs-lookup"><span data-stu-id="31a76-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="31a76-187">**Steuerkalender**</span><span class="sxs-lookup"><span data-stu-id="31a76-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="31a76-188">**Sachkonto**</span><span class="sxs-lookup"><span data-stu-id="31a76-188">**Ledger**</span></span>

5. <span data-ttu-id="31a76-189">Nachdem die Sicherheitsrolle aktualisiert wurde, gehen Sie zu **Einstellungen** > **Sicherheit** > **Teams** und wählen Sie das Standardteam in der Teamansicht **Lokaler Geschäftsinhaber** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="31a76-190">Wählen Sie **Rollen verwalten** und überprüfen Sie, ob die **Dual-Write-App-Benutzer** Sicherheitsberechtigung auf dieses Team angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="31a76-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="31a76-191">Duales Schreiben für Project Operations-Zuordnungen ausführen</span><span class="sxs-lookup"><span data-stu-id="31a76-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="31a76-192">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="31a76-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="31a76-193">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="31a76-194">Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="31a76-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="31a76-195">Starten Sie die Zuordnungen wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="31a76-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="31a76-196">Stellen Sie sicher, dass Sie die angegebene Reihenfolge einhalten.</span><span class="sxs-lookup"><span data-stu-id="31a76-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="31a76-197">**Entitätszuordnung**</span><span class="sxs-lookup"><span data-stu-id="31a76-197">**Entity Map**</span></span> | <span data-ttu-id="31a76-198">**Entität aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="31a76-198">**Refresh entity**</span></span> | <span data-ttu-id="31a76-199">**Erste Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="31a76-199">**Initial sync**</span></span> | <span data-ttu-id="31a76-200">**Master für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="31a76-200">**Master for initial sync**</span></span> | <span data-ttu-id="31a76-201">**Voraussetzungen ausführen**</span><span class="sxs-lookup"><span data-stu-id="31a76-201">**Run prerequisites**</span></span> | <span data-ttu-id="31a76-202">**Voraussetzungen für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="31a76-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="31a76-203">**Projektressourcenrollen für alle Unternehmen(bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="31a76-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="31a76-204">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-204">No</span></span> | <span data-ttu-id="31a76-205">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-205">Yes</span></span> | <span data-ttu-id="31a76-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="31a76-206">Common Data Service</span></span> | <span data-ttu-id="31a76-207">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-207">No</span></span> | <span data-ttu-id="31a76-208">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-208">N\A</span></span> |
| <span data-ttu-id="31a76-209">**Juristische Personen (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="31a76-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="31a76-210">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-210">No</span></span> | <span data-ttu-id="31a76-211">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-211">Yes</span></span> | <span data-ttu-id="31a76-212">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="31a76-212">Finance and Operations apps</span></span> | <span data-ttu-id="31a76-213">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-213">No</span></span> | <span data-ttu-id="31a76-214">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-214">N\A</span></span> |
| <span data-ttu-id="31a76-215">**Sachkonto (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="31a76-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="31a76-216">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-216">No</span></span> | <span data-ttu-id="31a76-217">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-217">Yes</span></span> | <span data-ttu-id="31a76-218">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="31a76-218">Finance and Operations apps</span></span> | <span data-ttu-id="31a76-219">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-219">Yes</span></span> | <span data-ttu-id="31a76-220">Ja, Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="31a76-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="31a76-221">**Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="31a76-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="31a76-222">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-222">No</span></span> | <span data-ttu-id="31a76-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-223">No</span></span> | <span data-ttu-id="31a76-224">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-224">N\A</span></span> | <span data-ttu-id="31a76-225">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-225">Yes</span></span> | <span data-ttu-id="31a76-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-226">No</span></span> |
| <span data-ttu-id="31a76-227">**Projektvertragszeilen (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="31a76-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="31a76-228">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-228">No</span></span> | <span data-ttu-id="31a76-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-229">No</span></span> | <span data-ttu-id="31a76-230">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-230">N\A</span></span> | <span data-ttu-id="31a76-231">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-231">No</span></span> | <span data-ttu-id="31a76-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-232">No</span></span> |
| <span data-ttu-id="31a76-233">**Integrationsentität für die Projekttransaktionsbeziehungen (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="31a76-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="31a76-234">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-234">No</span></span> | <span data-ttu-id="31a76-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-235">No</span></span> | <span data-ttu-id="31a76-236">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-236">N\A</span></span> | <span data-ttu-id="31a76-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-237">No</span></span> | <span data-ttu-id="31a76-238">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-238">N\A</span></span> |
| <span data-ttu-id="31a76-239">**Vertragszeilenmeilensteine der Project Operations-Integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="31a76-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="31a76-240">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-240">No</span></span> | <span data-ttu-id="31a76-241">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-241">No</span></span> | <span data-ttu-id="31a76-242">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-242">N\A</span></span> | <span data-ttu-id="31a76-243">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-243">No</span></span> | <span data-ttu-id="31a76-244">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-244">N\A</span></span> |
| <span data-ttu-id="31a76-245">**Project Operations-Integrationsentität für Ausgabenschätzungen (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="31a76-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="31a76-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-246">No</span></span> | <span data-ttu-id="31a76-247">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-247">No</span></span> | <span data-ttu-id="31a76-248">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-248">N\A</span></span> | <span data-ttu-id="31a76-249">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-249">No</span></span> | <span data-ttu-id="31a76-250">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-250">N\A</span></span> |
| <span data-ttu-id="31a76-251">**Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="31a76-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="31a76-252">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-252">No</span></span> | <span data-ttu-id="31a76-253">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-253">No</span></span> | <span data-ttu-id="31a76-254">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-254">N\A</span></span> | <span data-ttu-id="31a76-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-255">No</span></span> | <span data-ttu-id="31a76-256">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-256">N\A</span></span> |
| <span data-ttu-id="31a76-257">**Exportentität für Projektkosten der Project Operations-Integration (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="31a76-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="31a76-258">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-258">Yes</span></span> | <span data-ttu-id="31a76-259">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-259">No</span></span> | <span data-ttu-id="31a76-260">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-260">N\A</span></span> | <span data-ttu-id="31a76-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-261">No</span></span> | <span data-ttu-id="31a76-262">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-262">N\A</span></span> |
| <span data-ttu-id="31a76-263">**Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="31a76-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="31a76-264">Ja</span><span class="sxs-lookup"><span data-stu-id="31a76-264">Yes</span></span> | <span data-ttu-id="31a76-265">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-265">No</span></span> | <span data-ttu-id="31a76-266">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-266">N\A</span></span> | <span data-ttu-id="31a76-267">Nr.</span><span class="sxs-lookup"><span data-stu-id="31a76-267">No</span></span> | <span data-ttu-id="31a76-268">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="31a76-268">N\A</span></span> |


4. <span data-ttu-id="31a76-269">Um die Entität zu aktualisieren, wählen Sie den Zuordnungsnamen und dann **Entitäten aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Zuordnung aktualisieren](./media/20RefreshMapping.png)

5. <span data-ttu-id="31a76-271">Führen Sie nach dem Abschluss der Aktualisierung die Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="31a76-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="31a76-272">Bevor Sie die nächste Zuordnung aktivieren, stellen Sie sicher, dass sich die Zuordnung in der Tabelle im Status **Wird ausgeführt** befindet.</span><span class="sxs-lookup"><span data-stu-id="31a76-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="31a76-273">Das Ausführen von Zuordnungen mit einer größeren Anzahl von Voraussetzungen kann einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="31a76-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="31a76-274">Um eine Zuordnung mit Voraussetzungen auszuführen, aktivieren Sie die Umschalttaste **Zugehörige Entitätszuordnungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="31a76-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="31a76-275">Wenn die Tabelle angibt, dass **Voraussetzungen für die Erstsynchronisierung** auf **Nein** festgelegt ist, stellen Sie sicher, dass die Kennzeichnung **Erstsynchronisation** in allen erforderlichen Voraussetzungszuordnungen auf **Aus** festgelegt ist, bevor Sie sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="31a76-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Zuordnung ausführen](./media/21RunMap.png)

6. <span data-ttu-id="31a76-277">Überprüfen Sie, ob alle projektbezogenen Zuordnungen sich im Status „Wird ausgeführt“ befinden.</span><span class="sxs-lookup"><span data-stu-id="31a76-277">Validate all project related maps are in the running state.</span></span>

![Alle Zuordnungen werden ausgeführt](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="31a76-279">Konfigurationsdaten in CDS für Project Operations anwenden (optional)</span><span class="sxs-lookup"><span data-stu-id="31a76-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="31a76-280">Wenn Sie Demodaten auf die Finanzumgebung angewendet haben, erhalten Sie weitere Informationen unter [Konfigurationsdaten in Common Data Service für Project Operations einrichten und anwenden](resource-apply-pro-setup-config-data.md), um Demodaten auf die CDS-Umgebung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="31a76-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="31a76-281">Ihre Project Operations-Umgebung ist jetzt bereitgestellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="31a76-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]