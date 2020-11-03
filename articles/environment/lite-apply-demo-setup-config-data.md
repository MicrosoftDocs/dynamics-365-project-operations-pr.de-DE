---
title: Anwenden von Demo-Einrichtungs- und Konfigurationsdaten
description: Dieses Thema enthält Informationen zum Anwenden von Demo-Einrichtungs- und Konfigurationsdaten für Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076389"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="2766e-103">Anwenden der Demo-Einrichtungs- und Konfigurationsdaten für die Bereitstellung des Project Operations Lite - Abschluss zur Proforma-Rechnungsstellung</span><span class="sxs-lookup"><span data-stu-id="2766e-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="2766e-104">_\*\*Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="2766e-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="2766e-105">Laden Sie das [Masterdatenpaket](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) herunter.</span><span class="sxs-lookup"><span data-stu-id="2766e-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="2766e-106">Navigieren Sie zum Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* und führen Sie die ausführbare Datei *DataMigrationUtility* aus.</span><span class="sxs-lookup"><span data-stu-id="2766e-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="2766e-107">Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="2766e-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="2766e-109">Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als **Bereitstellungstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="2766e-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="2766e-110">Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="2766e-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="2766e-111">Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein und wählen Sie dann **Einloggen**.</span><span class="sxs-lookup"><span data-stu-id="2766e-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="2766e-113">Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten aus, in welche Organisation Sie die Demo-Daten importieren möchten, und wählen Sie dann **Einloggen**.</span><span class="sxs-lookup"><span data-stu-id="2766e-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="2766e-114">Wählen Sie auf Seite 4 die Zip-Datei *MasterAndSetupData* aus dem entpackten Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* aus.</span><span class="sxs-lookup"><span data-stu-id="2766e-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![ZIP-Datei](./media/3ZipFile.png)

![Datei auswählen](./media/4SelectAFile.png)

9. <span data-ttu-id="2766e-117">Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.</span><span class="sxs-lookup"><span data-stu-id="2766e-117">After the zip file is selected, select **Import Data**.</span></span>

![Daten importieren](./media/5ImportData.png)

10. <span data-ttu-id="2766e-119">Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2766e-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="2766e-120">Beenden Sie nach Abschluss den CMT-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="2766e-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="2766e-121">Überprüfen Sie Ihre Organisation auf Daten in den folgenden 20 Entitäten:</span><span class="sxs-lookup"><span data-stu-id="2766e-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="2766e-122">Währung</span><span class="sxs-lookup"><span data-stu-id="2766e-122">Currency</span></span>
- <span data-ttu-id="2766e-123">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="2766e-123">Organizational Unit</span></span>
- <span data-ttu-id="2766e-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="2766e-124">Contact</span></span>
- <span data-ttu-id="2766e-125">Steuergruppe</span><span class="sxs-lookup"><span data-stu-id="2766e-125">Tax Group</span></span>
- <span data-ttu-id="2766e-126">Kundengruppe</span><span class="sxs-lookup"><span data-stu-id="2766e-126">Customer Group</span></span>
- <span data-ttu-id="2766e-127">Einheit</span><span class="sxs-lookup"><span data-stu-id="2766e-127">Unit</span></span>
- <span data-ttu-id="2766e-128">Einheitengruppe</span><span class="sxs-lookup"><span data-stu-id="2766e-128">Unit Group</span></span>
- <span data-ttu-id="2766e-129">Preisliste</span><span class="sxs-lookup"><span data-stu-id="2766e-129">Price List</span></span>
- <span data-ttu-id="2766e-130">Projektparameter-Preisliste</span><span class="sxs-lookup"><span data-stu-id="2766e-130">Project Parameter Price List</span></span>
- <span data-ttu-id="2766e-131">Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2766e-131">Invoice Frequency</span></span>
- <span data-ttu-id="2766e-132">Detail zur Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="2766e-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="2766e-133">Buchbare Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="2766e-133">Bookable Resource Category</span></span>
- <span data-ttu-id="2766e-134">Transaktionskategorie</span><span class="sxs-lookup"><span data-stu-id="2766e-134">Transaction Category</span></span>
- <span data-ttu-id="2766e-135">Ausgabenkategorie</span><span class="sxs-lookup"><span data-stu-id="2766e-135">Expense Category</span></span>
- <span data-ttu-id="2766e-136">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="2766e-136">Role Price</span></span>
- <span data-ttu-id="2766e-137">Transaktionskategoriepreis</span><span class="sxs-lookup"><span data-stu-id="2766e-137">Transaction Category Price</span></span>
- <span data-ttu-id="2766e-138">Merkmal</span><span class="sxs-lookup"><span data-stu-id="2766e-138">Characteristic</span></span>
- <span data-ttu-id="2766e-139">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="2766e-139">Bookable Resource</span></span>
- <span data-ttu-id="2766e-140">Zuordnung der buchbaren Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="2766e-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="2766e-141">Merkmal der buchbaren Ressource</span><span class="sxs-lookup"><span data-stu-id="2766e-141">Bookable Resource Characteristic</span></span>

![Import abschließen](./media/6CompleteImport.png)
