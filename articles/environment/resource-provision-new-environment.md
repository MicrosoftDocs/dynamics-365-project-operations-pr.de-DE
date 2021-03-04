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
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727789"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="adcc6-103">Eine neue Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="adcc6-103">Provision a new environment</span></span>

<span data-ttu-id="adcc6-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="adcc6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="adcc6-105">Dieses Thema enthält Informationen zur Bereitstellung einer neuen Dynamics 365 Project Operations-Umgebung für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="adcc6-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="adcc6-106">Automatisierte Project Operations-Bereitstellung in einem LCS-Projekt aktivieren</span><span class="sxs-lookup"><span data-stu-id="adcc6-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="adcc6-107">Führen Sie die folgenden Schritte aus, um den automatisierten Project Operations-Bereitstellungs-Flow für Ihr LCS-Projekt zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="adcc6-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="adcc6-108">Navigieren Sie zu [LCS](https://lcs.dynamics.com/v2), und wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="adcc6-109">Wählen Sie in der Liste **Vorschaufunktion** die Option **Project Operations-Funktion** und dann **Vorschaufunktion aktiviert** aus, um Project Operations zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="adcc6-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="adcc6-110">Dieser Schritt wird nur einmal pro LCS-Projekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adcc6-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="adcc6-111">Eine Project Operations-Umgebung bereitstellen</span><span class="sxs-lookup"><span data-stu-id="adcc6-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="adcc6-112">Öffnen Sie eine neue Dynamics 365 Finance [Demo-Umgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) oder [Sandbox/Produktionsumgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="adcc6-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="adcc6-113">Durchlaufen Sie den Assistenten zur **Umgebungsbereitstellung**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="adcc6-114">Stellen Sie sicher, dass die ausgewählte Anwendungsversion 10.0.13 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="adcc6-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="adcc6-115">Um Project Operations bereitzustellen, wählen Sie unter **Erweiterte Einstellungen** **Common Data Service** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="adcc6-116">Aktivieren Sie die **Common Data Service-Einstellung**, indem Sie **Ja** auswählen und dann Informationen in die entsprechenden Felder eingeben:</span><span class="sxs-lookup"><span data-stu-id="adcc6-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="adcc6-117">Name des Dataflows</span><span class="sxs-lookup"><span data-stu-id="adcc6-117">Name</span></span>
  - <span data-ttu-id="adcc6-118">Region</span><span class="sxs-lookup"><span data-stu-id="adcc6-118">Region</span></span>
  - <span data-ttu-id="adcc6-119">Sprache</span><span class="sxs-lookup"><span data-stu-id="adcc6-119">Language</span></span>
  - <span data-ttu-id="adcc6-120">Währung</span><span class="sxs-lookup"><span data-stu-id="adcc6-120">Currency</span></span>
 
5. <span data-ttu-id="adcc6-121">Wählen Sie im Feld **Common Data Service-Vorlage** **Project Operations** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="adcc6-122">Wählen Sie den Umgebungstyp für Ihre Bereitstellung aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="adcc6-123">Mit einer abonnementbasierten Testversion können Sie eine CDS-Umgebung 30 Tage lang bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="adcc6-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Bereitstellungseinstellungen](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="adcc6-125">Wählen Sie **Zustimmen** aus, um die Vertragsbedingungen zu bestätigen, und dann **Fertig**, um zu den Bereitstellungseinstellungen zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="adcc6-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Bereitstellungseinwilligung](./media/2DeploymentConsent.png)

7. <span data-ttu-id="adcc6-127">Optional – Wenden Sie Demodaten auf die Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="adcc6-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="adcc6-128">Gehen Sie zu **Erweiterte Einstellungen**, wählen Sie **Passen Sie die SQL-Datenbankkonfiguration an** und setzen **Geben Sie ein DataSet für die Anwendungsdatenbank an** auf **Demo**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="adcc6-129">Füllen Sie die verbleibenden erforderlichen Felder im Assistenten aus, und bestätigen Sie die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="adcc6-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="adcc6-130">Die Zeit zum Bereitstellen der Umgebung hängt vom Umgebungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="adcc6-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="adcc6-131">Die Bereitstellung kann bis zu sechs Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="adcc6-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="adcc6-132">Nach erfolgreichem Abschluss der Bereitstellung wird die Umgebung als **Bereitgestellt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adcc6-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="adcc6-133">Um zu bestätigen, dass die Umgebung erfolgreich bereitgestellt wurde, wählen Sie **Anmeldung** und melden Sie sich zur Bestätigung bei der Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="adcc6-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![-Umgebungsdetails](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="adcc6-135">Aktualisierungen auf die Finance-Umgebung anwenden</span><span class="sxs-lookup"><span data-stu-id="adcc6-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="adcc6-136">Project Operations erfordert eine Finance-Umgebung mit Anwendungsversion **10.0.13 (10.0.569.20009)** oder höher.</span><span class="sxs-lookup"><span data-stu-id="adcc6-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="adcc6-137">Möglicherweise müssen Sie Qualitätsupdates auf Ihre Finance-Umgebung anwenden, um diese Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="adcc6-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="adcc6-138">Wählen Sie in LCS auf der Seite **Umgebungsdetails** im Abschnitt **Verfügbare Updates** die Option **Aktualisierung anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Aktualisierungen anzeigen](./media/5ViewUpdates.png)

2. <span data-ttu-id="adcc6-140">Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-140">On the **Binary updates** page, select **Save package.**</span></span>

![Paket speichern](./media/6SavePackage.png)

3. <span data-ttu-id="adcc6-142">Klicken Sie auf **Alle auswählen**, und wählen Sie dann **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-142">Click **Select all** and then select **Save package**.</span></span>

![Aktualisierungen überprüfen und speichern](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="adcc6-144">Geben Sie einen Namen und eine Beschreibung zum Paket ein, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="adcc6-145">Abhängig von der Internetverbindung kann dieser Vorgang einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="adcc6-145">Depending on the internet connection, this process might take some time.</span></span>

![Paket in Objektbibliothek hochladen](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="adcc6-147">Nachdem das Paket gespeichert wurde, wählen Sie **Fertig** aus, und speichern Sie dieses Paket in der Objektbibliothek in Ihrem LCS-Projekt.</span><span class="sxs-lookup"><span data-stu-id="adcc6-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="adcc6-148">Das Speichern und Validieren des Pakets kann ca. 15 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="adcc6-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="adcc6-149">Um das Update anzuwenden, navigieren Sie zur Seite **Umgebungsdetails** in LCS und wählen Sie **Verwalten** > **Aktualisierungen übernehmen** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Umgebungen verwalten](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="adcc6-151">Wählen Sie in der Aktualisierungsliste das von Ihnen erstellte Paket und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aktualisierungen anwenden](./media/10ApplyUpdates.png)

<span data-ttu-id="adcc6-153">Die Wartung der Umgebung wird einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="adcc6-153">Environment servicing will take some time.</span></span> <span data-ttu-id="adcc6-154">Nach Abschluss des Vorgangs kehrt die Umgebung in den bereitgestellten Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="adcc6-154">After it is complete, the environment will return to a deployed state.</span></span>

![Umgebungen bereitgestellt](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="adcc6-156">Eine Dual-Write-Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="adcc6-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="adcc6-157">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="adcc6-158">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="adcc6-159">Nachdem der Link vollständig ist, wählen Sie erneut **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="adcc6-160">Sie werden zu Dual Write in Finance weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="adcc6-160">You will be redirected to Dual Write in Finance.</span></span>

![Mit CDS verknüpfen](./media/12LinktoCDS.png)

4. <span data-ttu-id="adcc6-162">Wählen Sie **Lösung anwenden** aus, um auf die Entitäten zuzugreifen, die in der Integration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="adcc6-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Lösungen anwenden](./media/13ApplySolutions.png)

5. <span data-ttu-id="adcc6-164">Wählen Sie beide Lösungen, **Dynamics 365 Finance and Operations Dual Write Entity Map** und **Dynamics 365 Project Operations Dual Write Entity Maps**, und dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Lösungen bestätigen](./media/14ConfirmSolutions.png)

<span data-ttu-id="adcc6-166">Nachdem die Lösungen angewendet wurden, werden die Dual Write-Entitäten auf die Umgebung angewendet.</span><span class="sxs-lookup"><span data-stu-id="adcc6-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Anwenden von Lösungen](./media/15ApplyingSolutions.png)

<span data-ttu-id="adcc6-168">Nachdem die Entitäten angewendet wurden, werden alle verfügbaren Zuordnungen in der Umgebung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="adcc6-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Zuordnungen für duales Schreiben](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="adcc6-170">Die Datenentitäten nach der Aktualisierung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="adcc6-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="adcc6-171">Navigieren Sie in Finance zum Arbeitsbereich **Datenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-171">In Finance, go to the **Data management** workspace.</span></span>

![Datenverwaltungsarbeitsbereich](./media/16DataManagement.png)

2. <span data-ttu-id="adcc6-173">Wählen Sie die Kachel **Framework-Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-173">Select the **Framework parameters** tile.</span></span>

![Framework-Parameter](./media/17FrameworkParameters.png)

3. <span data-ttu-id="adcc6-175">Wählen Sie auf der Seite **Entitätseinstellungen** die Option **Entitätsliste aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Entitätsliste aktualisieren](./media/18RefreshEntityList.png)

<span data-ttu-id="adcc6-177">Die Aktualisierung dauert ungefähr 20 Minuten.</span><span class="sxs-lookup"><span data-stu-id="adcc6-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="adcc6-178">Sie erhalten eine Benachrichtigung, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="adcc6-178">You will receive an alert when it is complete.</span></span>

![Bestätigung aktualisieren](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="adcc6-180">Aktualisieren Sie die Sicherheitseinstellungen für Project Operations in Dataverse</span><span class="sxs-lookup"><span data-stu-id="adcc6-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="adcc6-181">Gehen sie Project Operations in Ihrer Dataverse Umgebung.</span><span class="sxs-lookup"><span data-stu-id="adcc6-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="adcc6-182">Gehen Sie zu **Einstellungen** > **Sicherheit** > **Sicherheitsrollen**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="adcc6-183">Auf der Seite **Sicherheitsrollen** in der Liste der Rollen wählen Sie **Dual-Write-App-Benutzer** und wählen Sie die Registerkarte **Benutzerdefinierte Entitäten**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="adcc6-184">Stellen Sie sicher, dass die Rolle Berechtigung für **Lesen** und **Anfürgen** hat:</span><span class="sxs-lookup"><span data-stu-id="adcc6-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="adcc6-185">**Währungswechselkurstyp eingeben**</span><span class="sxs-lookup"><span data-stu-id="adcc6-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="adcc6-186">**Kontenplan**</span><span class="sxs-lookup"><span data-stu-id="adcc6-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="adcc6-187">**Steuerkalender**</span><span class="sxs-lookup"><span data-stu-id="adcc6-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="adcc6-188">**Sachkonto**</span><span class="sxs-lookup"><span data-stu-id="adcc6-188">**Ledger**</span></span>

5. <span data-ttu-id="adcc6-189">Nachdem die Sicherheitsrolle aktualisiert wurde, gehen Sie zu **Einstellungen** > **Sicherheit** > **Teams** und wählen Sie das Standardteam in der Teamansicht **Lokaler Geschäftsinhaber** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="adcc6-190">Wählen Sie **Rollen verwalten** und überprüfen Sie, ob die **Dual-Write-App-Benutzer** Sicherheitsberechtigung auf dieses Team angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="adcc6-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="adcc6-191">Duales Schreiben für Project Operations-Zuordnungen ausführen</span><span class="sxs-lookup"><span data-stu-id="adcc6-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="adcc6-192">Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="adcc6-193">Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="adcc6-194">Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="adcc6-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="adcc6-195">Starten Sie die Zuordnungen wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="adcc6-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="adcc6-196">Stellen Sie sicher, dass Sie die angegebene Reihenfolge einhalten.</span><span class="sxs-lookup"><span data-stu-id="adcc6-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="adcc6-197">**Entitätszuordnung**</span><span class="sxs-lookup"><span data-stu-id="adcc6-197">**Entity Map**</span></span> | <span data-ttu-id="adcc6-198">**Entität aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="adcc6-198">**Refresh entity**</span></span> | <span data-ttu-id="adcc6-199">**Erste Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="adcc6-199">**Initial sync**</span></span> | <span data-ttu-id="adcc6-200">**Master für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="adcc6-200">**Master for initial sync**</span></span> | <span data-ttu-id="adcc6-201">**Voraussetzungen ausführen**</span><span class="sxs-lookup"><span data-stu-id="adcc6-201">**Run prerequisites**</span></span> | <span data-ttu-id="adcc6-202">**Voraussetzungen für Erstsynchronisierung**</span><span class="sxs-lookup"><span data-stu-id="adcc6-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="adcc6-203">**Projektressourcenrollen für alle Unternehmen(bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="adcc6-204">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-204">No</span></span> | <span data-ttu-id="adcc6-205">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-205">Yes</span></span> | <span data-ttu-id="adcc6-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="adcc6-206">Common Data Service</span></span> | <span data-ttu-id="adcc6-207">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-207">No</span></span> | <span data-ttu-id="adcc6-208">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-208">N\A</span></span> |
| <span data-ttu-id="adcc6-209">**Juristische Personen (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="adcc6-210">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-210">No</span></span> | <span data-ttu-id="adcc6-211">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-211">Yes</span></span> | <span data-ttu-id="adcc6-212">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="adcc6-212">Finance and Operations apps</span></span> | <span data-ttu-id="adcc6-213">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-213">No</span></span> | <span data-ttu-id="adcc6-214">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-214">N\A</span></span> |
| <span data-ttu-id="adcc6-215">**Sachkonto (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="adcc6-216">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-216">No</span></span> | <span data-ttu-id="adcc6-217">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-217">Yes</span></span> | <span data-ttu-id="adcc6-218">Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="adcc6-218">Finance and Operations apps</span></span> | <span data-ttu-id="adcc6-219">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-219">Yes</span></span> | <span data-ttu-id="adcc6-220">Ja, Finance and Operations-Apps</span><span class="sxs-lookup"><span data-stu-id="adcc6-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="adcc6-221">**Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="adcc6-222">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-222">No</span></span> | <span data-ttu-id="adcc6-223">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-223">No</span></span> | <span data-ttu-id="adcc6-224">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-224">N\A</span></span> | <span data-ttu-id="adcc6-225">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-225">Yes</span></span> | <span data-ttu-id="adcc6-226">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-226">No</span></span> |
| <span data-ttu-id="adcc6-227">**Projektvertragszeilen (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="adcc6-228">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-228">No</span></span> | <span data-ttu-id="adcc6-229">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-229">No</span></span> | <span data-ttu-id="adcc6-230">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-230">N\A</span></span> | <span data-ttu-id="adcc6-231">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-231">No</span></span> | <span data-ttu-id="adcc6-232">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-232">No</span></span> |
| <span data-ttu-id="adcc6-233">**Integrationsentität für die Projekttransaktionsbeziehungen (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="adcc6-234">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-234">No</span></span> | <span data-ttu-id="adcc6-235">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-235">No</span></span> | <span data-ttu-id="adcc6-236">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-236">N\A</span></span> | <span data-ttu-id="adcc6-237">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-237">No</span></span> | <span data-ttu-id="adcc6-238">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-238">N\A</span></span> |
| <span data-ttu-id="adcc6-239">**Vertragszeilenmeilensteine der Project Operations-Integration (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="adcc6-240">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-240">No</span></span> | <span data-ttu-id="adcc6-241">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-241">No</span></span> | <span data-ttu-id="adcc6-242">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-242">N\A</span></span> | <span data-ttu-id="adcc6-243">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-243">No</span></span> | <span data-ttu-id="adcc6-244">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-244">N\A</span></span> |
| <span data-ttu-id="adcc6-245">**Project Operations-Integrationsentität für Ausgabenschätzungen (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="adcc6-246">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-246">No</span></span> | <span data-ttu-id="adcc6-247">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-247">No</span></span> | <span data-ttu-id="adcc6-248">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-248">N\A</span></span> | <span data-ttu-id="adcc6-249">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-249">No</span></span> | <span data-ttu-id="adcc6-250">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-250">N\A</span></span> |
| <span data-ttu-id="adcc6-251">**Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="adcc6-252">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-252">No</span></span> | <span data-ttu-id="adcc6-253">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-253">No</span></span> | <span data-ttu-id="adcc6-254">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-254">N\A</span></span> | <span data-ttu-id="adcc6-255">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-255">No</span></span> | <span data-ttu-id="adcc6-256">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-256">N\A</span></span> |
| <span data-ttu-id="adcc6-257">**Exportentität für Projektkosten der Project Operations-Integration (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="adcc6-258">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-258">Yes</span></span> | <span data-ttu-id="adcc6-259">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-259">No</span></span> | <span data-ttu-id="adcc6-260">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-260">N\A</span></span> | <span data-ttu-id="adcc6-261">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-261">No</span></span> | <span data-ttu-id="adcc6-262">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-262">N\A</span></span> |
| <span data-ttu-id="adcc6-263">**Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="adcc6-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="adcc6-264">Ja</span><span class="sxs-lookup"><span data-stu-id="adcc6-264">Yes</span></span> | <span data-ttu-id="adcc6-265">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-265">No</span></span> | <span data-ttu-id="adcc6-266">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-266">N\A</span></span> | <span data-ttu-id="adcc6-267">Nr.</span><span class="sxs-lookup"><span data-stu-id="adcc6-267">No</span></span> | <span data-ttu-id="adcc6-268">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="adcc6-268">N\A</span></span> |


4. <span data-ttu-id="adcc6-269">Um die Entität zu aktualisieren, wählen Sie den Zuordnungsnamen und dann **Entitäten aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Zuordnung aktualisieren](./media/20RefreshMapping.png)

5. <span data-ttu-id="adcc6-271">Führen Sie nach dem Abschluss der Aktualisierung die Zuordnung aus.</span><span class="sxs-lookup"><span data-stu-id="adcc6-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="adcc6-272">Bevor Sie die nächste Zuordnung aktivieren, stellen Sie sicher, dass sich die Zuordnung in der Tabelle im Status **Wird ausgeführt** befindet.</span><span class="sxs-lookup"><span data-stu-id="adcc6-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="adcc6-273">Das Ausführen von Zuordnungen mit einer größeren Anzahl von Voraussetzungen kann einige Zeit dauern.</span><span class="sxs-lookup"><span data-stu-id="adcc6-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="adcc6-274">Um eine Zuordnung mit Voraussetzungen auszuführen, aktivieren Sie die Umschalttaste **Zugehörige Entitätszuordnungen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="adcc6-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="adcc6-275">Wenn die Tabelle angibt, dass **Voraussetzungen für die Erstsynchronisierung** auf **Nein** festgelegt ist, stellen Sie sicher, dass die Kennzeichnung **Erstsynchronisation** in allen erforderlichen Voraussetzungszuordnungen auf **Aus** festgelegt ist, bevor Sie sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="adcc6-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Zuordnung ausführen](./media/21RunMap.png)

6. <span data-ttu-id="adcc6-277">Überprüfen Sie, ob alle projektbezogenen Zuordnungen sich im Status „Wird ausgeführt“ befinden.</span><span class="sxs-lookup"><span data-stu-id="adcc6-277">Validate all project related maps are in the running state.</span></span>

![Alle Zuordnungen werden ausgeführt](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="adcc6-279">Konfigurationsdaten in CDS für Project Operations anwenden (optional)</span><span class="sxs-lookup"><span data-stu-id="adcc6-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="adcc6-280">Wenn Sie Demodaten auf die Finanzumgebung angewendet haben, erhalten Sie weitere Informationen unter [Konfigurationsdaten in Common Data Service für Project Operations einrichten und anwenden](resource-apply-pro-setup-config-data.md), um Demodaten auf die CDS-Umgebung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="adcc6-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="adcc6-281">Ihre Project Operations-Umgebung ist jetzt bereitgestellt und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="adcc6-281">Your Project Operations environment is now provisioned and configured.</span></span> 
