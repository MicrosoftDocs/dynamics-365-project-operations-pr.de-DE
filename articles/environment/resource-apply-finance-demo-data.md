---
title: Demodaten auf eine in der Cloud gehostete Finance-Umgebung anwenden
description: In diesem Thema wird erläutert, wie Demodaten aus Project Operations auf eine Cloud-gehostete Dynamics 365 Finance-Umgebung angewendet werden.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000149"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="f004f-103">Demodaten auf eine in der Cloud gehostete Finance-Umgebung anwenden</span><span class="sxs-lookup"><span data-stu-id="f004f-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="f004f-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="f004f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f004f-105">Dieses Thema gilt nur für die Microsoft Dynamics 365 Finance Version 10.0.13 und kann nur in einer Cloud-gehosteten Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f004f-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="f004f-106">Führen Sie die Schritte in diesem Thema aus, **BEVOR** Sie Qualitätsaktualisierungen auf die Umgebung anwenden.</span><span class="sxs-lookup"><span data-stu-id="f004f-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="f004f-107">Öffnen Sie in Ihrem LCS-Projekt die Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="f004f-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="f004f-108">Beachten Sie, dass es die Details enthält, die für die Verbindung mit der Umgebung mithilfe des RDP (Remote Desktop Protocol) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f004f-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![-Umgebungsdetails](./media/1EnvironmentDetails.png)

<span data-ttu-id="f004f-110">Die ersten hervorgehobenen Anmeldeinformationen sind die Anmeldeinformationen des lokalen Kontos und enthalten einen Hyperlink zur Remotedesktopverbindung.</span><span class="sxs-lookup"><span data-stu-id="f004f-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="f004f-111">Zu den Anmeldeinformationen gehören der Benutzername und das Kennwort des Umgebungsadministrators.</span><span class="sxs-lookup"><span data-stu-id="f004f-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="f004f-112">Der zweite Satz von Anmeldeinformationen wird verwendet, um sich in dieser Umgebung beim SQL Server anzumelden.</span><span class="sxs-lookup"><span data-stu-id="f004f-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="f004f-113">Stellen Sie über den Hyperlink in **Lokale Konten** eine Verbindung her, und verwenden Sie die **Anmeldeinformationen für das lokale Konto**, um sich zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f004f-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="f004f-114">Navigieren Sie zu **Internetinformationsdienste** > **Anwendungspools** > **AOSService**, und beenden Sie den Dienst.</span><span class="sxs-lookup"><span data-stu-id="f004f-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="f004f-115">Sie beenden den Dienst an dieser Stelle, damit Sie die SQL-Datenbank weiterhin ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="f004f-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS beenden](./media/2StopAOS.png)

4. <span data-ttu-id="f004f-117">Navigieren Sie zu **Dienste**, und beenden Sie die folgenden zwei Elemente:</span><span class="sxs-lookup"><span data-stu-id="f004f-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="f004f-118">Microsoft Dynamics 365 Unified Operations: Batchverwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="f004f-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="f004f-119">Microsoft Dynamics 365 Unified Operations: Datenimport/-export-Framework</span><span class="sxs-lookup"><span data-stu-id="f004f-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Dienste anhalten](./media/3StopServices.png)

5. <span data-ttu-id="f004f-121">Öffnen Sie Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="f004f-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="f004f-122">Melden Sie sich mit SQL Server-Anmeldeinformationen an, und verwenden Sie den Benutzer axdbadmin und das Kennwort von der LCS-Seite **Umgebungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="f004f-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="f004f-124">Suchen Sie in den **Datenbanken** von Object Explorer **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="f004f-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="f004f-125">Sie ersetzen die Datenbank durch eine neue Datenbank, die sich im [Download-Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) befindet.</span><span class="sxs-lookup"><span data-stu-id="f004f-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="f004f-126">Kopieren Sie die Zip-Datei in die VM, mit der Sie remote verbunden sind, und extrahieren Sie die Zip-Inhalte.</span><span class="sxs-lookup"><span data-stu-id="f004f-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="f004f-127">Klicken Sie in SQL Server Management Studio mit der rechten Maustaste auf **AxDB**, und wählen Sie dann **Aufgaben** > **Wiederherstellen** > **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="f004f-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Datenbank wiederherstellen](./media/5RestoreDatabase.png)

9. <span data-ttu-id="f004f-129">Wählen Sie **Quellgerät** aus, und navigieren Sie zu der Datei, die aus der von Ihnen kopierten Zip-Datei extrahiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f004f-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Quellgeräte](./media/6SourceDevice.png)

10. <span data-ttu-id="f004f-131">Wählen Sie **Optionen** und dann **Vorhandene Datenbank überschreiben** sowie **Vorhandene Verbindungen zur Zieldatenbank schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="f004f-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="f004f-132">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f004f-132">Select **OK**.</span></span>

![Einstellungen wiederherstellen](./media/7RestoreSetting.png)

<span data-ttu-id="f004f-134">Sie erhalten eine Bestätigung, dass die AXDB-Wiederherstellung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f004f-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="f004f-135">Nachdem Sie diese Bestätigung erhalten haben, können Sie SQL Services Management Studio schließen.</span><span class="sxs-lookup"><span data-stu-id="f004f-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="f004f-136">Navigieren Sie zu **Internetinformationsdienste** > **Anwendungspools** > **AOSService**, und starten Sie AOSService.</span><span class="sxs-lookup"><span data-stu-id="f004f-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="f004f-137">Navigieren Sie zu **Dienste**, und starten Sie die zwei Dienste, die Sie zuvor angehalten haben.</span><span class="sxs-lookup"><span data-stu-id="f004f-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="f004f-138">Suchen Sie das AdminUserProvisioning-Tool auf dieser VM.</span><span class="sxs-lookup"><span data-stu-id="f004f-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="f004f-139">Schauen Sie unter K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe nach.</span><span class="sxs-lookup"><span data-stu-id="f004f-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="f004f-140">Führen Sie die .ext-Datei mit Ihrer Benutzeradresse im Feld **E-Mail-Adresse** aus.</span><span class="sxs-lookup"><span data-stu-id="f004f-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="f004f-141">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="f004f-141">Select **Submit**.</span></span>

![Administratorbenutzerbereitstellung](./media/8AdminUserProvisioning.png)

<span data-ttu-id="f004f-143">Dies kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="f004f-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="f004f-144">Sie sollten eine Bestätigungsnachricht erhalten, dass der Administratorbenutzer erfolgreich aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f004f-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="f004f-145">Führen Sie abschließend die Eingabeaufforderung als Administrator aus, und führen Sie iisreset durch.</span><span class="sxs-lookup"><span data-stu-id="f004f-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS-Neustart](./media/9IISReset.png)

18. <span data-ttu-id="f004f-147">Schließen Sie die Remotedesktopsitzung, und verwenden Sie die LCS-Seite **Umgebungsdetails**, um sich bei der Umgebung anzumelden und zu bestätigen, dass sie wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f004f-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]