---
title: Microsoft Project Client-Integration
description: Das Planen und Verwalten eines Projektplans kann komplex sein. Daher müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe verwalten können. Die Integration mit Microsoft Project Client bietet Unterstützung beim Öffnen und Verwalten einer Projektstrukturplan.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076585"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="d563f-104">Microsoft Project Client-Integration</span><span class="sxs-lookup"><span data-stu-id="d563f-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d563f-105">Das Planen und Verwalten eines Projektplans kann komplex sein. Daher müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe verwalten können.</span><span class="sxs-lookup"><span data-stu-id="d563f-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="d563f-106">Die Integration mit Microsoft Project Client bietet Unterstützung beim Öffnen und Verwalten einer Projektstrukturplan.</span><span class="sxs-lookup"><span data-stu-id="d563f-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="d563f-107">Der Projektmanager kann alle Änderungen wieder im Dynamics 365 Finance Projektstrukturplan veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d563f-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="d563f-108">Wenn Sie das Juli-Update (Version 10.0.4) verwenden, müssen Sie Wissensdatenbank 4054797 und 4055884 installieren.</span><span class="sxs-lookup"><span data-stu-id="d563f-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="d563f-109">Konfigurieren Sie das Microsoft Project Client-Add-In</span><span class="sxs-lookup"><span data-stu-id="d563f-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="d563f-110">So aktivieren Sie die Integration mit Microsoft Project Client: Ein Microsoft Dynamics 365 Add-In muss in der Microsoft Project Anwendung des Benutzers installiert sein.</span><span class="sxs-lookup"><span data-stu-id="d563f-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="d563f-111">Dies erfolgt durch Öffnen des **Projektmanagement-Arbeitsbereichs**.</span><span class="sxs-lookup"><span data-stu-id="d563f-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="d563f-112">• Klicken Sie auf **Konfigurieren Sie das Projektclient-Add-In** aus dem Abschnitt **Verknüpfung** > **Einrichtung** des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="d563f-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="d563f-113">• Klicken Sie auf **Öffnen** und dann klicken Sie auf **Ausführen** , wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d563f-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="d563f-114">Öffnen und bearbeiten Sie einen vorhandenen Entwurf einer Projektstrukturplanstruktur in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d563f-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="d563f-115">Wenn ein Projekt in Dynamics 365 Finance bereits einen Projektstrukturplan hat, kann der Projektstrukturplan in der Microsoft Project Client-Anwendung geöffnet werden, wenn sich der Projektstrukturplan in einem Entwurfsstatus befindet.</span><span class="sxs-lookup"><span data-stu-id="d563f-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="d563f-116">Zum Öffnen von der Seite **Projekt** klicken Sie auf die Verknüpfung **In Microsoft Project öffnen** aus der Registerkarte **Plan**. Diese Seite kann auch in der Microsoft Project Client-Anwendung durch Klicken  von **Öffnen** in der Registerkarte **Microsoft Dynamics 365** geöffnet werden. Wählen Sie die **Juristische Entität** und **Projekt** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="d563f-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="d563f-117">Wenn Sie den Internet Explorer als Ihren Browser verwenden, müssen Sie auf **speichern** klicken, um manuell von dem Speicherort zu öffnen, an den die Datei heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="d563f-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="d563f-118">Oder klicken Sie auf **Speichern und öffnen** , um die Datei in Microsoft Project Client zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d563f-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="d563f-119">Benennen Sie den Dateinamen beim Speichern nicht um.</span><span class="sxs-lookup"><span data-stu-id="d563f-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="d563f-120">Bevor Sie mit Microsoft Project Client Änderungen an der Datei vornehmen, müssen Sie diese auschecken. Klicken Sie auf **Auschecken** in der Registerkarte **Microsoft Dynamics 365**. Dadurch wird verhindert, dass andere Benutzer gleichzeitig die Projektstrukturplan innerhalb von Finance bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d563f-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="d563f-121">Um den Projektstrukturplan nach Abschluss aller Änderungen zu veröffentlichen, klicken Sie auf **einchecken** auf der Registerkarte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d563f-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="d563f-122">Wenn dem Projekt in Finance bereits ein Projektteam hinzugefügt wurde, wird die Ressourcenliste mit den Teammitgliedern gefüllt.</span><span class="sxs-lookup"><span data-stu-id="d563f-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="d563f-123">Wenn dem Projekt noch kein Projektteam hinzugefügt wurde, können Sie Ressourcen auswählen und das Team in Microsoft Project Client erstellen, indem Sie auf die Schaltfläche **Ressourcen** auf der Registerkarte **Microsoft Dynamics 365** klicken.</span><span class="sxs-lookup"><span data-stu-id="d563f-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="d563f-124">Die folgenden Daten werden im Rahmen des Check-in-Vorgangs wieder mit Finance synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="d563f-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="d563f-125">• Aufgabenname</span><span class="sxs-lookup"><span data-stu-id="d563f-125">•   Task name</span></span>

<span data-ttu-id="d563f-126">• Startdatum</span><span class="sxs-lookup"><span data-stu-id="d563f-126">•   Start date</span></span>

<span data-ttu-id="d563f-127">• Fertigstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="d563f-127">•   Finish date</span></span>

<span data-ttu-id="d563f-128">• Vorgänger</span><span class="sxs-lookup"><span data-stu-id="d563f-128">•   Predecessors</span></span>

<span data-ttu-id="d563f-129">• Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="d563f-129">•   Resource names</span></span>

<span data-ttu-id="d563f-130">• Kategorie</span><span class="sxs-lookup"><span data-stu-id="d563f-130">•   Category</span></span>

<span data-ttu-id="d563f-131">• Ressourcenkategorie</span><span class="sxs-lookup"><span data-stu-id="d563f-131">•   Resource category</span></span>

<span data-ttu-id="d563f-132">• Arbeitsstunden</span><span class="sxs-lookup"><span data-stu-id="d563f-132">•   Work hours</span></span>

<span data-ttu-id="d563f-133">• Hinweise</span><span class="sxs-lookup"><span data-stu-id="d563f-133">•   Notes</span></span>

<span data-ttu-id="d563f-134">• Priorität</span><span class="sxs-lookup"><span data-stu-id="d563f-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="d563f-135">Wenn Sie Ihrer Microsoft Project Client Datei weitere Spalten hinzufügen, werden diese nicht in der Datei gespeichert und beim erneuten Öffnen der Datei nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d563f-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d563f-136">Erstellen Sie den Projektstrukturplan für ein vorhandenes Projekt mit Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d563f-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d563f-137">Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen, folgen Sie diesen Schritten:</span><span class="sxs-lookup"><span data-stu-id="d563f-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="d563f-138">Öffnen Sie Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d563f-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d563f-139">Auf der Registerkarte **Microsoft Dynamics 365** wählen Sie **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="d563f-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="d563f-140">Wählen Sie die **Juristische Entität** für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="d563f-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="d563f-141">Wählen Sie das **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="d563f-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="d563f-142">Klicken Sie auf **Auschecken** auf der Registerkarte **Microsoft Dynamics 365** -</span><span class="sxs-lookup"><span data-stu-id="d563f-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="d563f-143">Wenn Sie bereit sind, in Finance zu veröffentlichen, klicken Sie auf **Check-In** auf der Registerkarte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="d563f-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="d563f-144">Ersetzen Sie den bestehenden Projektstrukturplan für ein vorhandenes Projekt mit Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d563f-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="d563f-145">Gehen Sie folgendermaßen vor, um mit Microsoft Project Client einen neuen Projektstrukturplan zu erstellen und einen vorhandenen Projektstrukturplan für ein vorhandenes Projekt zu ersetzen:</span><span class="sxs-lookup"><span data-stu-id="d563f-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="d563f-146">Öffnen Sie den Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d563f-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d563f-147">Erstellen Sie den Zeitplan in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d563f-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d563f-148">Auf der Registerkarte **Microsoft Dynamics 365** klicken Sie auf **Änderungen speichern** > **Bestehendes Projekt ersetzen**.</span><span class="sxs-lookup"><span data-stu-id="d563f-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="d563f-149">Wählen Sie die **Juristische Entität** für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="d563f-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d563f-150">Wählen Sie das **Projekt** aus.</span><span class="sxs-lookup"><span data-stu-id="d563f-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="d563f-151">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d563f-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="d563f-152">Erstellen Sie ein neues Projekt in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="d563f-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="d563f-153">Öffnen Sie den Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d563f-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="d563f-154">Erstellen Sie den Zeitplan in Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="d563f-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="d563f-155">Auf der Registerkarte **Microsoft Dynamics 365** klicken Sie auf **Änderungen speichern** > **In neuem Projekt speichern**.</span><span class="sxs-lookup"><span data-stu-id="d563f-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="d563f-156">Wählen Sie die **Juristische Entität** für das Projekt.</span><span class="sxs-lookup"><span data-stu-id="d563f-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="d563f-157">Geben Sie die **Projekt-ID** falls benötigt ein.</span><span class="sxs-lookup"><span data-stu-id="d563f-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="d563f-158">Geben Sie den **Projektnamen** ein.</span><span class="sxs-lookup"><span data-stu-id="d563f-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="d563f-159">Wählen Sie **Projekttyp** , **Projektgruppe** und die **Projektvertrags-ID** aus.</span><span class="sxs-lookup"><span data-stu-id="d563f-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="d563f-160">Alternativ können Sie einen neuen Projektvertrag erstellen, indem Sie auf **Neu** klicken.</span><span class="sxs-lookup"><span data-stu-id="d563f-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="d563f-161">Wählen Sie den **Kalender** aus, der für die Beschaffung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d563f-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="d563f-162">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d563f-162">Click **OK**.</span></span>
