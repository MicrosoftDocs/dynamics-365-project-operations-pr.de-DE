---
title: Problembehandlung für die Arbeit im Aufgabenraster
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die beim Arbeiten im Aufgabenraster erforderlich sind.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031536"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="27d12-103">Problembehandlung für die Arbeit im Aufgabenraster</span><span class="sxs-lookup"><span data-stu-id="27d12-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="27d12-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="27d12-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27d12-105">In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Kostenmanagement auftreten können.</span><span class="sxs-lookup"><span data-stu-id="27d12-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="27d12-106">Aktivieren Sie Cookies</span><span class="sxs-lookup"><span data-stu-id="27d12-106">Enable cookies</span></span>

<span data-ttu-id="27d12-107">Für Project Operations müssen Cookies von Drittanbietern aktiviert sein, um den Projektstrukturplan zu rendern.</span><span class="sxs-lookup"><span data-stu-id="27d12-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="27d12-108">Wenn Cookies von Drittanbietern nicht aktiviert sind, wird anstelle von Aufgaben eine leere Seite angezeigt, wenn Sie die Registerkarte **Aufgaben** auf der Seite **Projekt** auswählen.</span><span class="sxs-lookup"><span data-stu-id="27d12-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Leere Registerkarte, wenn Cookies von Drittanbietern nicht aktiviert sind](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="27d12-110">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="27d12-110">Workaround</span></span>
<span data-ttu-id="27d12-111">Für Microsoft Edge oder Google Chrome Browser beschreiben die folgenden Verfahren, wie Sie Ihre Browsereinstellungen aktualisieren, um Cookies von Drittanbietern zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27d12-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="27d12-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="27d12-112">Microsoft Edge</span></span>

1. <span data-ttu-id="27d12-113">Öffnen Sie Ihren Edge Browser.</span><span class="sxs-lookup"><span data-stu-id="27d12-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="27d12-114">Wählen Sie in der oberen rechten Ecke die **Auslassungspunkte** (...) aus, und wählen Sie dann **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="27d12-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="27d12-115">Unter **Cookies und Standort-Berechtigungen**, wählen Sie **Cookies und Standort-Daten**.</span><span class="sxs-lookup"><span data-stu-id="27d12-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="27d12-116">Deaktivieren Sie **Blockieren Sie Cookies von Drittanbietern**.</span><span class="sxs-lookup"><span data-stu-id="27d12-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="27d12-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="27d12-117">Google Chrome</span></span>

1. <span data-ttu-id="27d12-118">Öffnen Sie Ihren Chrome Browser.</span><span class="sxs-lookup"><span data-stu-id="27d12-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="27d12-119">Wählen Sie in der oberen rechten Ecke die drei vertikalen Punkte und wählen Sie dann **Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="27d12-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="27d12-120">Unter **Datenschutz und Sicherheit** wählen Sie **Cookies und andere Standort-Daten**.</span><span class="sxs-lookup"><span data-stu-id="27d12-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="27d12-121">Wählen Sie **Alle Cookies zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="27d12-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27d12-122">Wenn Sie Cookies von Drittanbietern blockieren, werden alle Cookies und Standort-Daten von anderen Standorten blockiert, auch wenn der Standort in Ihrer Ausnahmeliste zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="27d12-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="27d12-123">PEX-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="27d12-123">PEX Endpoint</span></span>

<span data-ttu-id="27d12-124">Für Project Operations muss ein Projektparameter auf PEX Endpunkt verweisen.</span><span class="sxs-lookup"><span data-stu-id="27d12-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="27d12-125">Dieser Endpunkt ist erforderlich, um mit dem Dienst zu kommunizieren, der zum Rendern des Projektstrukturplans verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="27d12-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="27d12-126">Wenn der Parameter nicht aktiviert ist, wird die Fehlermeldung der Projektparameter ist ungültig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27d12-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="27d12-127">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="27d12-127">Workaround</span></span>
 ![PEX Endpunkt Feld im Projektparameter](media/projectparameter.png)

1. <span data-ttu-id="27d12-129">Ergänzen Sie das Feld **PEX Endpunkt** auf der Seite **Projektparameter**.</span><span class="sxs-lookup"><span data-stu-id="27d12-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="27d12-130">Aktualisieren Sie das Feld mit dem folgenden Wert: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="27d12-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="27d12-131">Entfernen Sie das Feld aus der Seite **Projektparameter**.</span><span class="sxs-lookup"><span data-stu-id="27d12-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="27d12-132">Berechtigungen für Project für das Web</span><span class="sxs-lookup"><span data-stu-id="27d12-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="27d12-133">Project Operations ist auf einen externen Planungsservice angewiesen.</span><span class="sxs-lookup"><span data-stu-id="27d12-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="27d12-134">Der Dienst erfordert, dass einem Benutzer mehrere Rollen zum Lesen und Schreiben in Entitäten zugewiesen sind, die sich auf die Projektstrukturplan beziehen.</span><span class="sxs-lookup"><span data-stu-id="27d12-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="27d12-135">Diese Entitäten umfassen Projektaufgaben, Ressourcenzuweisungen und Aufgabenabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="27d12-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="27d12-136">Wenn ein Benutzer die Projektstrukturplan nicht rendern kann, wenn er zur Registerkarte **Aufgaben** geht,  liegt dies wahrscheinlich daran, dass Project for Project Operations nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="27d12-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="27d12-137">Ein Benutzer erhält möglicherweise entweder einen Sicherheitsrollen-Fehler oder einen Fehler im Zusammenhang mit einer Zugriffsverweigerung.</span><span class="sxs-lookup"><span data-stu-id="27d12-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="27d12-138">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="27d12-138">Workaround</span></span>

1. <span data-ttu-id="27d12-139">Gehen Sie zu **Einstellung > Sicherheit > Benutzer > Anwendungsbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="27d12-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Anwendungsleser](media/applicationuser.jpg)
   
2. <span data-ttu-id="27d12-141">Doppelklicken Sie auf den Anwendungsbenutzerdatensatz, um Folgendes zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="27d12-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="27d12-142">Der Benutzer verfügt über Zugriff auf das Projekt.</span><span class="sxs-lookup"><span data-stu-id="27d12-142">The user has access to the project.</span></span> <span data-ttu-id="27d12-143">Diese Überprüfung erfolgt normalerweise, indem sichergestellt wird, dass der Benutzer über die Sicherheitsrolle **Projektmanager** verfügt.</span><span class="sxs-lookup"><span data-stu-id="27d12-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="27d12-144">Der Benutzer der Microsoft Project-Anwendung ist vorhanden und korrekt konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="27d12-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="27d12-145">Wenn dieser Benutzer nicht vorhanden ist, können Sie einen neuen Benutzerdatensatz erstellen.</span><span class="sxs-lookup"><span data-stu-id="27d12-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="27d12-146">Wählen Sie **Neuer Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="27d12-146">Select **New Users**.</span></span> <span data-ttu-id="27d12-147">Ändern Sie das Anmeldeformular in **Anwendungsbenutzer** und fügen Sie dann die **Anwendungs-ID** hinzu.</span><span class="sxs-lookup"><span data-stu-id="27d12-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Anwendungsbenutzer-Details](media/applicationuserdetails.jpg)

4. <span data-ttu-id="27d12-149">Stellen Sie sicher, dass dem Benutzer die richtige Lizenz zugewiesen wurde und dass der Dienst in den Serviceplandetails der Lizenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27d12-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="27d12-150">Stellen Sie sicher, dass der Benutzer project.microsoft.com öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="27d12-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="27d12-151">Überprüfen Sie anhand der Projektparameter, ob das System auf den korrekten Projekt-Endpunkt verweist.</span><span class="sxs-lookup"><span data-stu-id="27d12-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="27d12-152">Überprüfen, dass der Projekt-Anwendungbenutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="27d12-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="27d12-153">Wenden Sie die folgenden Sicherheitsrollen auf den Benutzer an:</span><span class="sxs-lookup"><span data-stu-id="27d12-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="27d12-154">Dataverse-Benutzer</span><span class="sxs-lookup"><span data-stu-id="27d12-154">Dataverse User</span></span>
  - <span data-ttu-id="27d12-155">Project Operations System</span><span class="sxs-lookup"><span data-stu-id="27d12-155">Project Operations System</span></span>
  - <span data-ttu-id="27d12-156">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="27d12-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="27d12-157">Fehler beim Aktualisieren des Projektstrukturplans</span><span class="sxs-lookup"><span data-stu-id="27d12-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="27d12-158">Wenn eine oder mehrere Aktualisierungen am Projektstrukturplan vorgenommen werden, schlagen die Änderungen schließlich fehl und werden nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="27d12-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="27d12-159">Im Zeitplanraster tritt ein Fehler auf, der besagt, dass die zuletzt vorgenommenen Änderungen nicht gespeichert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="27d12-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="27d12-160">Problemumgehung</span><span class="sxs-lookup"><span data-stu-id="27d12-160">Workaround</span></span>

1. <span data-ttu-id="27d12-161">Stellen Sie sicher, dass dem Benutzer die richtige Lizenz zugewiesen wurde und dass der Dienst in den Serviceplandetails der Lizenz aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="27d12-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="27d12-162">Stellen Sie sicher, dass der Benutzer project.microsoft.com öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="27d12-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="27d12-163">Überprüfen Sie anhand der Projektparameter, ob das System auf den korrekten Projekt-Endpunkt verweist.</span><span class="sxs-lookup"><span data-stu-id="27d12-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="27d12-164">Überprüfen, dass der Projekt-Anwendungbenutzer erstellt worden ist.</span><span class="sxs-lookup"><span data-stu-id="27d12-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="27d12-165">Wenden Sie die folgenden Sicherheitsrollen auf den Benutzer an:</span><span class="sxs-lookup"><span data-stu-id="27d12-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="27d12-166">Dataverse Benutzer oder Basisbenutzer</span><span class="sxs-lookup"><span data-stu-id="27d12-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="27d12-167">Project Operations System</span><span class="sxs-lookup"><span data-stu-id="27d12-167">Project Operations System</span></span>
  - <span data-ttu-id="27d12-168">Projektsystem</span><span class="sxs-lookup"><span data-stu-id="27d12-168">Project System</span></span>
  - <span data-ttu-id="27d12-169">System duales Schreiben für Project Operations (Diese Rolle ist erforderlich, wenn Sie das Szenario ressourcen/nicht vorrätig von Project Operations bereitstellen.)</span><span class="sxs-lookup"><span data-stu-id="27d12-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
