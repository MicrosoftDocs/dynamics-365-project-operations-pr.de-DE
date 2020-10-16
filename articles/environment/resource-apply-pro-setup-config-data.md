---
title: Konfigurationsdaten in Common Data Service für Project Operations einrichten und anwenden
description: Dieses Thema enthält Informationen zum Einrichten und Anwenden von Konfigurationsdaten in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948870"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="149fa-103">Konfigurationsdaten in Common Data Service für Project Operations einrichten und anwenden</span><span class="sxs-lookup"><span data-stu-id="149fa-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="149fa-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="149fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="149fa-105">Einrichtungs- und Konfigurationsdaten installieren</span><span class="sxs-lookup"><span data-stu-id="149fa-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="149fa-106">Laden Sie das [Einrichtungs- und Konfigurationsdatenpaket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip) herunter, und entpacken Sie es.</span><span class="sxs-lookup"><span data-stu-id="149fa-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="149fa-107">Navigieren Sie zum entpackten Ordner, und führen Sie die ausführbare Datei *DataMigrationUtility* aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="149fa-108">Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="149fa-110">Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Office 365** als den **Bereitstellungstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="149fa-111">Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="149fa-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="149fa-112">Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein, und wählen Sie **Anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="149fa-114">Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten die Organisation aus, in die Sie die Demo-Daten importieren möchten, und dann **Anmelden**.</span><span class="sxs-lookup"><span data-stu-id="149fa-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="149fa-115">Wählen Sie auf Seite 4 die Zip-Datei *SampleSetupAndConfigData* aus dem entpackten Ordner aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Auswahl der Zip-Datei](./media/3ZipFile.png)

![Datei auswählen](./media/4SelectAFile.png)

9. <span data-ttu-id="149fa-118">Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.</span><span class="sxs-lookup"><span data-stu-id="149fa-118">After the zip file is selected, select **Import Data**.</span></span>

![Importdaten](./media/5ImportData.png)

10. <span data-ttu-id="149fa-120">Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="149fa-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="149fa-121">Beenden Sie nach Abschluss des Imports den CMT-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="149fa-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="149fa-122">Überprüfen Sie Ihre Organisation auf Daten in den folgenden 19 Entitäten:</span><span class="sxs-lookup"><span data-stu-id="149fa-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="149fa-123">Währung</span><span class="sxs-lookup"><span data-stu-id="149fa-123">Currency</span></span>
  - <span data-ttu-id="149fa-124">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="149fa-124">Organizational Unit</span></span>
  - <span data-ttu-id="149fa-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="149fa-125">Contact</span></span>
  - <span data-ttu-id="149fa-126">Steuergruppe</span><span class="sxs-lookup"><span data-stu-id="149fa-126">Tax Group</span></span>
  - <span data-ttu-id="149fa-127">Kundengruppe</span><span class="sxs-lookup"><span data-stu-id="149fa-127">Customer Group</span></span>
  - <span data-ttu-id="149fa-128">Einheit</span><span class="sxs-lookup"><span data-stu-id="149fa-128">Unit</span></span>
  - <span data-ttu-id="149fa-129">Einheitengruppe</span><span class="sxs-lookup"><span data-stu-id="149fa-129">Unit Group</span></span>
  - <span data-ttu-id="149fa-130">Preisliste</span><span class="sxs-lookup"><span data-stu-id="149fa-130">Price List</span></span>
  - <span data-ttu-id="149fa-131">Projektparameter-Preisliste</span><span class="sxs-lookup"><span data-stu-id="149fa-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="149fa-132">Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="149fa-132">Invoice Frequency</span></span>
  - <span data-ttu-id="149fa-133">Buchbare Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="149fa-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="149fa-134">Transaktionskategorie</span><span class="sxs-lookup"><span data-stu-id="149fa-134">Transaction Category</span></span>
  - <span data-ttu-id="149fa-135">Ausgabenkategorie</span><span class="sxs-lookup"><span data-stu-id="149fa-135">Expense Category</span></span>
  - <span data-ttu-id="149fa-136">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="149fa-136">Role Price</span></span>
  - <span data-ttu-id="149fa-137">Transaktionskategoriepreis</span><span class="sxs-lookup"><span data-stu-id="149fa-137">Transaction Category Price</span></span>
  - <span data-ttu-id="149fa-138">Merkmal</span><span class="sxs-lookup"><span data-stu-id="149fa-138">Characteristic</span></span>
  - <span data-ttu-id="149fa-139">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="149fa-139">Bookable Resource</span></span>
  - <span data-ttu-id="149fa-140">Zuordnung der buchbaren Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="149fa-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="149fa-141">Merkmal der buchbaren Ressource</span><span class="sxs-lookup"><span data-stu-id="149fa-141">Bookable Resource Characteristic</span></span>

![Import abschließen](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="149fa-143">Project Operations-Konfigurationen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="149fa-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="149fa-144">Navigieren zur CE-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="149fa-144">Navigate to the CE environment.</span></span> <span data-ttu-id="149fa-145">Sie können sie finden, indem Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments) öffnen, die Umgebung und dann **Umgebung öffnen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="149fa-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Umgebung öffnen](./media/7OpenEnvironment.png)

2. <span data-ttu-id="149fa-147">Navigieren Sie zu **Projekte** > **Ressourcen**, und wählen Sie dann **Neu** aus, um eine buchbare Ressource für Ihren Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="149fa-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Buchbare Ressourcen](./media/8BookableResources.png)

3. <span data-ttu-id="149fa-149">Wählen Sie auf der Registerkarte **Allgemein** Ihren Administrator-Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="149fa-150">Stellen Sie sicher, dass die Zeitzone mit der übereinstimmt, in der Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="149fa-150">Verify that the time zone matches the one you are in.</span></span> 

![Neue buchbare Ressource](./media/9NewBookableResource.png)

4. <span data-ttu-id="149fa-152">Wählen Sie auf der Registerkarte **Zeitplanung** im Feld **Unternehmen** das Unternehmen **USPM** und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Registerkarte „Planung“](./media/10SchedulingTab.png)

5. <span data-ttu-id="149fa-154">Wählen Sie die Registerkarte **Arbeitsstunden** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-154">Select the **Work hours** tab.</span></span>  

![Arbeitszeit](./media/11WorkHours.png)

6. <span data-ttu-id="149fa-156">Doppelklicken Sie auf einen beliebigen Wert im Kalender, und wählen Sie **Bearbeiten** > **Alle Ereignisse in der Serie** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbeitskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="149fa-158">Ändern Sie die Arbeitszeit in einen Arbeitstag von acht (8) Stunden, markieren Sie Wochenenden als arbeitsfreie Tage, und stellen Sie sicher, dass die Zeitzone mit Ihrer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="149fa-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="149fa-159">Wählen Sie **Speichern und schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-159">Select **Save and close**.</span></span>

![Kalender aktualisieren](./media/13UpdateCalendar.png)

9. <span data-ttu-id="149fa-161">Navigieren Sie zu **Einstellungen** > **Kalendervorlagen**, und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendervorlagen](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="149fa-163">Geben Sie einen Namen ein, wählen Sie die von Ihnen erstellte Vorlagenressource und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendervorlage speichern](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="149fa-165">Navigieren Sie zu **Parameter**, und doppelklicken Sie auf den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="149fa-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparameter](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="149fa-167">Aktualisieren Sie die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="149fa-167">Update the following fields:</span></span>

 - <span data-ttu-id="149fa-168">**Standardunternehmen**: USPM</span><span class="sxs-lookup"><span data-stu-id="149fa-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="149fa-169">**Standard-Organisationseinheit**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="149fa-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="149fa-170">**Rechnungshäufigkeit**: Siebter und letzter Tag</span><span class="sxs-lookup"><span data-stu-id="149fa-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="149fa-171">**Arbeitszeitvorlage**: Wechseln Sie zu der von Ihnen erstellten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="149fa-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="149fa-172">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="149fa-172">Select **Save**.</span></span> 

![Aktualisierte Projektparameter](./media/17UpdatedProjectParameters.png)
