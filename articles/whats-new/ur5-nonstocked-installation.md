---
title: Aktualisieren Sie Project Operations in Ihrer Finance Umgebung
description: Dieses Thema enthält Informationen zum Aktualisieren von Project Operations in Ihrer Dynamics 365 Finance Umgebung.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816624"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="d7bb0-103">Aktualisieren Sie Project Operations in Ihrer Finance Umgebung</span><span class="sxs-lookup"><span data-stu-id="d7bb0-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="d7bb0-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="d7bb0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="d7bb0-105">Dieses Thema enthält Informationen zum Aktualisieren von Dynamics 365 Project Operations in Ihrer Dynamics 365 Finance Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="d7bb0-106">Es sind drei Verfahren erforderlich, um Project Operations auf Update 5 (UR5) zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="d7bb0-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="d7bb0-107">Importieren Sie das Paket in Ihr Vorschauprojekt</span><span class="sxs-lookup"><span data-stu-id="d7bb0-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="d7bb0-108">Wenden Sie das Update</span><span class="sxs-lookup"><span data-stu-id="d7bb0-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="d7bb0-109">Ihre Dataverse Umgebung einrichten</span><span class="sxs-lookup"><span data-stu-id="d7bb0-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><span data-ttu-id="d7bb0-110"><a name="import">Importieren Sie das Paket in Ihr LCS Projekt</a></span><span class="sxs-lookup"><span data-stu-id="d7bb0-110"><a name="import"></a>Import the package into your LCS project</span></span>

1. <span data-ttu-id="d7bb0-111">Melden Sie sich bei [Lifecycle Services (LCS)](https://lcs.dynamics.com/) als Projektbesitzer oder Umgebungsmanager.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="d7bb0-112">Wählen Sie in der Liste Ihrer Projekte Ihre LCS Projekt aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="d7bb0-113">Auf der Seite **Projekt** in der Gruppe **Umgebungen** öffnen Sie die Umgebung, die Sie aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="d7bb0-114">Überprüfen Sie, ob die Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-114">Verify that the environment is running.</span></span> <span data-ttu-id="d7bb0-115">Wenn sie nicht gestartet wird, starten Sie die Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="d7bb0-116">In dem Abschnitt **Neuer Release** unter **Verfügbare Updates** wählen Sie **Update anzeigen** für 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Schaltfläche aktualisieren anzeigen](media/view-update.png)

6. <span data-ttu-id="d7bb0-118">Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="d7bb0-119">Wählen Sie auf der Seite **Updates überprüfen und speichern** die Option **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="d7bb0-120">Geben Sie auf dem sich öffnenden Bereich **Paket in der Anlagebibliothek speichern** den Paketnamen ein und wählen Sie dann **Paket speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="d7bb0-121">Wenn LCS das Paket gespeichert hat, wird die Schaltfläche **Fertig** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="d7bb0-122">Wählen Sie **Fertig** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-122">Select **Done**.</span></span> <span data-ttu-id="d7bb0-123">LCS überprüft das Paket.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-123">LCS will verify the package.</span></span> <span data-ttu-id="d7bb0-124">Die Überprüfung kann einige Minuten oder bis zu einer Stunde dauern.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="d7bb0-125">Wenden Sie die Paketaktualisierung an</span><span class="sxs-lookup"><span data-stu-id="d7bb0-125">Apply the package update</span></span>

1. <span data-ttu-id="d7bb0-126">In LCS wählen Sie auf der Seite **Umgebungsdetails** die Option **Verwalten** > **Aktualisierungen übernehmen** aus, um eine Aktualisierung zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="d7bb0-127">Wählen Sie aus der Liste das Paket aus, das Sie zuvor gespeichert haben, und wählen Sie dann **Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="d7bb0-128">Klicken Sie auf **Ja**, um zu bestätigen, dass Sie das Paket bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Bestätigen Sie das Dialogfeld für die Paketbereitstellung](media/confirm-package-deployment.png)

4. <span data-ttu-id="d7bb0-130">Klicken Sie auf **Ja**, um zu bestätigen, dass Sie die Anwendung aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Bestätigen Sie das Dialogfeld Anwendungsaktualisierung](media/confirm-application-update.png)

<span data-ttu-id="d7bb0-132">Die Bereitstellung und die Aktualisierung der Anwendung werden gestartet.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="d7bb0-133">Auf der Seite **Umgebungsdetails** in der oberen rechten Ecke wird der Umgebungsstatus auf **Wartung** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="d7bb0-134">In ungefähr zwei Stunden ist die Aktualisierung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="d7bb0-135">Die Informationen zur Anwendungsversion werden auf **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** und der Umgebungsstatus auf **Bereitgestellt** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><span data-ttu-id="d7bb0-136"><a name="update">Ihre Dataverse Umgebung einrichten</a></span><span class="sxs-lookup"><span data-stu-id="d7bb0-136"><a name="update"></a>Update your Dataverse environment</span></span>

1. <span data-ttu-id="d7bb0-137">Melden Sie sich beim [Power Platform Admin Center](https://admin.powerplatform.com/) an.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="d7bb0-138">Suchen und öffnen Sie in der Liste die Umgebung, in der Sie Project Operations installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="d7bb0-139">Auf der Seite **Umgebungen** wählen Sie **Ressource** > **Dynamics 365-Apps**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="d7bb0-140">Suchen Sie in der Liste **Microsoft Dynamics 365 Project Operations**, und in der Spalte **Status** wählen Sie **Aktualisierung verfügbar**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="d7bb0-141">Wählen Sie **Ich stimme den Nutzungsbedingungen zu** und Aktivieren Sie das Kontrollkästchen, und wählen Sie dann **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="d7bb0-142">Die neueste Version der Lösung wird installiert.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="d7bb0-143">Nach Abschluss der Installation ist die Version 4.5.0.134 installiert.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="d7bb0-144">Neue Funktionen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="d7bb0-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="d7bb0-145">Duales Schreiben im Mapping aktivieren</span><span class="sxs-lookup"><span data-stu-id="d7bb0-145">Enable dual-write mapping</span></span>

<span data-ttu-id="d7bb0-146">Nachdem Sie die Aktualisierung auf Finance und Dataverse Umgebungen abgeschlossen haben, können Sie die erforderlichen Zuordnungen für duales Schreiben aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="d7bb0-147">Folgende Abläufe für duales Schreiben aktivieren beenden.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="d7bb0-148">Aktualisieren Sie die Sicherheitseinstellungen in der Customer Engagement Umgebung</span><span class="sxs-lookup"><span data-stu-id="d7bb0-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="d7bb0-149">Daten in Entitäten aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d7bb0-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="d7bb0-150">Aktualisieren Sie die Zuordnungen für duales Schreiben und führen Sie sie aus</span><span class="sxs-lookup"><span data-stu-id="d7bb0-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="d7bb0-151">Aktualisieren Sie die Sicherheitseinstellungen in der Dataverse Umgebung</span><span class="sxs-lookup"><span data-stu-id="d7bb0-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="d7bb0-152">Die folgenden Aktualisierungen der Sicherheitsberechtigungen für Entitäten sind im Rahmen der Aktualisierung auf UR5 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="d7bb0-153">In Ihrer Dataverse Umgebung gehen Sie zu **Einstellungen** und in der **System** Gruppe wählen Sie **Sicherheit** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse Umgebungseinstellungen](media/Picture21.png)

2. <span data-ttu-id="d7bb0-155">Wählen Sie **Sicherheitsrollen** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="d7bb0-156">In der Liste der Rollen wählen Sie **App-Benutzer duales Schreiben** und wählen Sie die Registerkarte **Benutzerdefinierte Entitäten** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="d7bb0-157">Stellen Sie sicher, dass die Rolle Berechtigung für **Lesen** und **Anfügen** hat:</span><span class="sxs-lookup"><span data-stu-id="d7bb0-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="d7bb0-158">**Währungswechselkurstyp eingeben**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="d7bb0-159">**Kontenplan**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="d7bb0-160">**Steuerkalender**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="d7bb0-161">**Sachkonto**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-161">**Ledger**</span></span>

5. <span data-ttu-id="d7bb0-162">Nachdem die Sicherheitsrolle aktualisiert wurde, gehen Sie zu **Einstellungen** > **Sicherheit** > **Teams**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="d7bb0-163">Stellen Sie sicher, dass die Rolle **App Benutzer duales Schreiben** auf das Team angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="d7bb0-164">Aktualisieren Sie Datenentitäten aus der Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="d7bb0-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="d7bb0-165">Öffnen Sie in Ihrer Finance Umgebung den Arbeitsbereich **Datenverwaltung** und öffnen Sie dann die Seite **Framework-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="d7bb0-166">Auf der **Entitätseinstellungen** Registerkarte wählen Sie **Entitätsliste aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="d7bb0-167">Wählen Sie **Schließen**, um die Aktualisierung der Entität zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d7bb0-168">Dieser Prozess kann ungefähr 20 Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="d7bb0-169">Sie werden benachrichtigt, wenn die Aktualisierung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="d7bb0-170">Duales Schreiben im Mapping aktivieren</span><span class="sxs-lookup"><span data-stu-id="d7bb0-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="d7bb0-171">Wählen Sie **duales Schreiben** im Arbeitsbereich **Datenverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="d7bb0-172">Wählen Sie **Lösungen anwenden** und wählen Sie beide Lösungen in der Liste aus und wählen Sie dann **Anwenden**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="d7bb0-173">Auf der Seite **duales Schreiben** wählen Sie die folgenden Tabellenzuordnungen aus und wählen Sie dann **Anhalten**.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="d7bb0-174">**Tatsächliche Werte der Project Operations-Integration (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="d7bb0-175">**Project Operations Integartion Projektausgabenkategorien (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="d7bb0-176">**Project Operations Integartion tatsächliche Projektausgabenkategorien (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="d7bb0-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="d7bb0-177">Auf der Seite **Tabellenzuordnungsversion** wenden Sie auf jede der drei Entitäten eine neue Version der Zuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="d7bb0-178">Auf der Seite **Duales Schreiben** wählen Sie ausführen aus, um die Zuordnungen neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="d7bb0-179">Wählen Sie aus der Liste der Zuordnungen **Ledger (msdyn_ledgers)** mit allen Voraussetzungen aus und wählen Sie das Kontrollkästchen **Erstsynchronisation** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="d7bb0-180">In dem Feld **Master für die Erstsynchronisation** wählen Sie **Finance and Operations Apps** und dann **Ausführen** aus.</span><span class="sxs-lookup"><span data-stu-id="d7bb0-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronisation der Ledger Zuordnung](media/DW6.png)
 
