---
title: Demoeinrichtungs- und -konfigurationsdaten anwenden – Lite
description: Dieses Thema enthält Informationen zum Anwenden von Demo-Einrichtungs- und Konfigurationsdaten für Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089118"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="5486f-103">Demoeinrichtungs- und -konfigurationsdaten für Project Operations anwenden – Lite</span><span class="sxs-lookup"><span data-stu-id="5486f-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="5486f-104">_\*\*Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="5486f-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="5486f-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5486f-105">Prerequisites</span></span>

<span data-ttu-id="5486f-106">Bevor Sie mit der Konfiguration beginnen, müssen Sie eine Common Data Service (CDS)-Umgebung für Dynamics 365 Project Operations haben.</span><span class="sxs-lookup"><span data-stu-id="5486f-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="5486f-107">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="5486f-107">Instructions</span></span>

1. <span data-ttu-id="5486f-108">Laden Sie das [Masterdatenpaket](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) herunter.</span><span class="sxs-lookup"><span data-stu-id="5486f-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="5486f-109">Navigieren Sie zum Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* und führen Sie die ausführbare Datei *DataMigrationUtility* aus.</span><span class="sxs-lookup"><span data-stu-id="5486f-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="5486f-110">Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="5486f-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="5486f-112">Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als **Bereitstellungstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="5486f-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="5486f-113">Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="5486f-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="5486f-114">Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein und wählen Sie dann **Einloggen**.</span><span class="sxs-lookup"><span data-stu-id="5486f-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="5486f-116">Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten aus, in welche Organisation Sie die Demo-Daten importieren möchten, und wählen Sie dann **Einloggen**.</span><span class="sxs-lookup"><span data-stu-id="5486f-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="5486f-117">Wählen Sie auf Seite 4 die Zip-Datei *MasterAndSetupData* aus dem entpackten Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* aus.</span><span class="sxs-lookup"><span data-stu-id="5486f-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![ZIP-Datei](./media/3ZipFile.png)

   ![Datei auswählen](./media/4SelectAFile.png)

9. <span data-ttu-id="5486f-120">Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.</span><span class="sxs-lookup"><span data-stu-id="5486f-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Daten importieren](./media/5ImportData.png)

10. <span data-ttu-id="5486f-122">Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5486f-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="5486f-123">Beenden Sie nach Abschluss den CMT-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="5486f-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="5486f-124">Überprüfen Sie Ihre Organisation auf Daten in den folgenden 20 Entitäten:</span><span class="sxs-lookup"><span data-stu-id="5486f-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="5486f-125">Währung</span><span class="sxs-lookup"><span data-stu-id="5486f-125">Currency</span></span>
    -   <span data-ttu-id="5486f-126">Konto</span><span class="sxs-lookup"><span data-stu-id="5486f-126">Account</span></span>
    -   <span data-ttu-id="5486f-127">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="5486f-127">Organizational Unit</span></span>
    -   <span data-ttu-id="5486f-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="5486f-128">Contact</span></span>
    -   <span data-ttu-id="5486f-129">Einheit</span><span class="sxs-lookup"><span data-stu-id="5486f-129">Unit</span></span>
    -   <span data-ttu-id="5486f-130">Einheitengruppe</span><span class="sxs-lookup"><span data-stu-id="5486f-130">Unit Group</span></span>
    -   <span data-ttu-id="5486f-131">Preisliste</span><span class="sxs-lookup"><span data-stu-id="5486f-131">Price List</span></span>
    -   <span data-ttu-id="5486f-132">Projektparameter-Preisliste</span><span class="sxs-lookup"><span data-stu-id="5486f-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="5486f-133">Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="5486f-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="5486f-134">Buchbare Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="5486f-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="5486f-135">Transaktionskategorie</span><span class="sxs-lookup"><span data-stu-id="5486f-135">Transaction Category</span></span>
    -   <span data-ttu-id="5486f-136">Ausgabenkategorie</span><span class="sxs-lookup"><span data-stu-id="5486f-136">Expense Category</span></span>
    -   <span data-ttu-id="5486f-137">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="5486f-137">Role Price</span></span>
    -   <span data-ttu-id="5486f-138">Transaktionskategoriepreis</span><span class="sxs-lookup"><span data-stu-id="5486f-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="5486f-139">Merkmal</span><span class="sxs-lookup"><span data-stu-id="5486f-139">Characteristic</span></span>
    -   <span data-ttu-id="5486f-140">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="5486f-140">Bookable Resource</span></span>
    -   <span data-ttu-id="5486f-141">Zuordnung der buchbaren Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="5486f-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="5486f-142">Merkmal der buchbaren Ressource</span><span class="sxs-lookup"><span data-stu-id="5486f-142">Bookable Resource Characteristic</span></span>

    ![Import abschließen](./media/6CompleteImport.png)
