---
title: Konfigurationsdaten in Common Data Service einrichten und anwenden
description: Dieses Thema enthält Informationen zum Einrichten und Anwenden von Konfigurationsdaten in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401127"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="44ef8-103">Konfigurationsdaten in Common Data Service einrichten und anwenden</span><span class="sxs-lookup"><span data-stu-id="44ef8-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="44ef8-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="44ef8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="44ef8-105">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44ef8-105">Prerequisites</span></span>

<span data-ttu-id="44ef8-106">Bevor Sie beginnen, Daten in Common Data Service (CDS) zu konfigurieren, müssen folgende Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="44ef8-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="44ef8-107">Bereitstellung einer CDS-Umgebung und einer Dynamics 365 Finance-Umgebung für Project Operations.</span><span class="sxs-lookup"><span data-stu-id="44ef8-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="44ef8-108">Informationen zu juristischen Personen von Dynamics 365 Finance werden für die CDS-Umgebung freigegeben.</span><span class="sxs-lookup"><span data-stu-id="44ef8-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="44ef8-109">Dies bedeutet, dass die **Firma**-Entität in CDS die folgenden Firmendatensätze hat:</span><span class="sxs-lookup"><span data-stu-id="44ef8-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="44ef8-110">THPM</span><span class="sxs-lookup"><span data-stu-id="44ef8-110">THPM</span></span>
  - <span data-ttu-id="44ef8-111">USPM</span><span class="sxs-lookup"><span data-stu-id="44ef8-111">USPM</span></span>
  - <span data-ttu-id="44ef8-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="44ef8-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="44ef8-113">Einrichtungs- und Konfigurationsdaten installieren</span><span class="sxs-lookup"><span data-stu-id="44ef8-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="44ef8-114">Laden Sie das [Einrichtungs- und Konfigurationsdatenpaket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip) herunter, und entpacken Sie es.</span><span class="sxs-lookup"><span data-stu-id="44ef8-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="44ef8-115">Navigieren Sie zum entpackten Ordner, und führen Sie die ausführbare Datei *DataMigrationUtility* aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="44ef8-116">Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="44ef8-118">Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als **Bereitstellungstyp** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="44ef8-119">Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="44ef8-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="44ef8-120">Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein, und wählen Sie **Anmelden** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="44ef8-122">Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten die Organisation aus, in die Sie die Demo-Daten importieren möchten, und dann **Anmelden**.</span><span class="sxs-lookup"><span data-stu-id="44ef8-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="44ef8-123">Wählen Sie auf Seite 4 die Zip-Datei *SampleSetupAndConfigData* aus dem entpackten Ordner aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Auswahl der Zip-Datei](./media/3ZipFile.png)

![Datei auswählen](./media/4SelectAFile.png)

9. <span data-ttu-id="44ef8-126">Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.</span><span class="sxs-lookup"><span data-stu-id="44ef8-126">After the zip file is selected, select **Import Data**.</span></span>

![Importdaten](./media/5ImportData.png)

10. <span data-ttu-id="44ef8-128">Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44ef8-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="44ef8-129">Beenden Sie nach Abschluss des Imports den CMT-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="44ef8-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="44ef8-130">Überprüfen Sie Ihre Organisation auf Daten in den folgenden 19 Entitäten:</span><span class="sxs-lookup"><span data-stu-id="44ef8-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="44ef8-131">Währung</span><span class="sxs-lookup"><span data-stu-id="44ef8-131">Currency</span></span>
  - <span data-ttu-id="44ef8-132">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="44ef8-132">Organizational Unit</span></span>
  - <span data-ttu-id="44ef8-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="44ef8-133">Contact</span></span>
  - <span data-ttu-id="44ef8-134">Steuergruppe</span><span class="sxs-lookup"><span data-stu-id="44ef8-134">Tax Group</span></span>
  - <span data-ttu-id="44ef8-135">Kundengruppe</span><span class="sxs-lookup"><span data-stu-id="44ef8-135">Customer Group</span></span>
  - <span data-ttu-id="44ef8-136">Einheit</span><span class="sxs-lookup"><span data-stu-id="44ef8-136">Unit</span></span>
  - <span data-ttu-id="44ef8-137">Einheitengruppe</span><span class="sxs-lookup"><span data-stu-id="44ef8-137">Unit Group</span></span>
  - <span data-ttu-id="44ef8-138">Preisliste</span><span class="sxs-lookup"><span data-stu-id="44ef8-138">Price List</span></span>
  - <span data-ttu-id="44ef8-139">Projektparameter-Preisliste</span><span class="sxs-lookup"><span data-stu-id="44ef8-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="44ef8-140">Rechnungshäufigkeit</span><span class="sxs-lookup"><span data-stu-id="44ef8-140">Invoice Frequency</span></span>
  - <span data-ttu-id="44ef8-141">Buchbare Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="44ef8-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="44ef8-142">Transaktionskategorie</span><span class="sxs-lookup"><span data-stu-id="44ef8-142">Transaction Category</span></span>
  - <span data-ttu-id="44ef8-143">Ausgabenkategorie</span><span class="sxs-lookup"><span data-stu-id="44ef8-143">Expense Category</span></span>
  - <span data-ttu-id="44ef8-144">Rollenpreis</span><span class="sxs-lookup"><span data-stu-id="44ef8-144">Role Price</span></span>
  - <span data-ttu-id="44ef8-145">Transaktionskategoriepreis</span><span class="sxs-lookup"><span data-stu-id="44ef8-145">Transaction Category Price</span></span>
  - <span data-ttu-id="44ef8-146">Merkmal</span><span class="sxs-lookup"><span data-stu-id="44ef8-146">Characteristic</span></span>
  - <span data-ttu-id="44ef8-147">Buchbare Ressource</span><span class="sxs-lookup"><span data-stu-id="44ef8-147">Bookable Resource</span></span>
  - <span data-ttu-id="44ef8-148">Zuordnung der buchbaren Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="44ef8-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="44ef8-149">Merkmal der buchbaren Ressource</span><span class="sxs-lookup"><span data-stu-id="44ef8-149">Bookable Resource Characteristic</span></span>

![Import abschließen](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="44ef8-151">Project Operations-Konfigurationen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="44ef8-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="44ef8-152">Navigieren zur CE-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="44ef8-152">Navigate to the CE environment.</span></span> <span data-ttu-id="44ef8-153">Sie können sie finden, indem Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments) öffnen, die Umgebung und dann **Umgebung öffnen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="44ef8-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Umgebung öffnen](./media/7OpenEnvironment.png)

2. <span data-ttu-id="44ef8-155">Navigieren Sie zu **Projekte** > **Ressourcen**, und wählen Sie dann **Neu** aus, um eine buchbare Ressource für Ihren Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44ef8-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Buchbare Ressourcen](./media/8BookableResources.png)

3. <span data-ttu-id="44ef8-157">Wählen Sie auf der Registerkarte **Allgemein** Ihren Administrator-Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="44ef8-158">Stellen Sie sicher, dass die Zeitzone mit der übereinstimmt, in der Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="44ef8-158">Verify that the time zone matches the one you are in.</span></span> 

![Neue buchbare Ressource](./media/9NewBookableResource.png)

4. <span data-ttu-id="44ef8-160">Wählen Sie auf der Registerkarte **Zeitplanung** im Feld **Unternehmen** das Unternehmen **USPM** und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Registerkarte „Planung“](./media/10SchedulingTab.png)

5. <span data-ttu-id="44ef8-162">Wählen Sie die Registerkarte **Arbeitsstunden** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-162">Select the **Work hours** tab.</span></span>  

![Arbeitszeit](./media/11WorkHours.png)

6. <span data-ttu-id="44ef8-164">Doppelklicken Sie auf einen beliebigen Wert im Kalender, und wählen Sie **Bearbeiten** > **Alle Ereignisse in der Serie** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbeitskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="44ef8-166">Ändern Sie die Arbeitszeit in einen Arbeitstag von acht (8) Stunden, markieren Sie Wochenenden als arbeitsfreie Tage, und stellen Sie sicher, dass die Zeitzone mit Ihrer übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="44ef8-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="44ef8-167">Wählen Sie **Speichern und schließen** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-167">Select **Save and close**.</span></span>

![Kalender aktualisieren](./media/13UpdateCalendar.png)

9. <span data-ttu-id="44ef8-169">Navigieren Sie zu **Einstellungen** > **Kalendervorlagen**, und wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendervorlagen](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="44ef8-171">Geben Sie einen Namen ein, wählen Sie die von Ihnen erstellte Vorlagenressource und dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendervorlage speichern](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="44ef8-173">Navigieren Sie zu **Parameter**, und doppelklicken Sie auf den Datensatz.</span><span class="sxs-lookup"><span data-stu-id="44ef8-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektparameter](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="44ef8-175">Aktualisieren Sie die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="44ef8-175">Update the following fields:</span></span>

 - <span data-ttu-id="44ef8-176">**Standardunternehmen**: USPM</span><span class="sxs-lookup"><span data-stu-id="44ef8-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="44ef8-177">**Standard-Organisationseinheit**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="44ef8-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="44ef8-178">**Rechnungshäufigkeit**: Siebter und letzter Tag</span><span class="sxs-lookup"><span data-stu-id="44ef8-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="44ef8-179">**Arbeitszeitvorlage**: Wechseln Sie zu der von Ihnen erstellten Vorlage.</span><span class="sxs-lookup"><span data-stu-id="44ef8-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="44ef8-180">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="44ef8-180">Select **Save**.</span></span> 

![Aktualisierte Projektparameter](./media/17UpdatedProjectParameters.png)
