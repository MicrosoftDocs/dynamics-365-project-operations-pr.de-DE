---
title: Preis- und Nachkalkulationsdimensions-Homepage
description: Dieses Thema enthält einen Überblick über Preisdimensionen.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3721965"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="de45e-103">Preis- und Nachkalkulationsdimensions-Homepage</span><span class="sxs-lookup"><span data-stu-id="de45e-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="de45e-104">Die Dimensionen, die in der Personalverwaltung zum Einrichten von Preisen und Kosten verwendet werden, lassen sich in zwei Kategorien einteilen:</span><span class="sxs-lookup"><span data-stu-id="de45e-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="de45e-105">Personen</span><span class="sxs-lookup"><span data-stu-id="de45e-105">People</span></span>
- <span data-ttu-id="de45e-106">Geplante Arbeit</span><span class="sxs-lookup"><span data-stu-id="de45e-106">Planned work</span></span>

<span data-ttu-id="de45e-107">Daher gibt es zwei Arten von Preisdimensionswerten, die in Project Service Automation (PSA) verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="de45e-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="de45e-108">**Optionssätze** – Dimensionen, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.</span><span class="sxs-lookup"><span data-stu-id="de45e-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="de45e-109">**Entität-basierte Werte** – Dimensionen, bei denen es sich um unterschiedliche Sätze von Werten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="de45e-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="de45e-110">Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="de45e-110">Pricing dimensions</span></span>

<span data-ttu-id="de45e-111">PSA wird mit einem Standardsatz an Preisdimensionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="de45e-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="de45e-112">Sie können diese anzeigen, indem Sie zu **Project Service** > **Parameter** navigieren.</span><span class="sxs-lookup"><span data-stu-id="de45e-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="de45e-113">Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="de45e-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="de45e-114">Dadurch können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.</span><span class="sxs-lookup"><span data-stu-id="de45e-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="de45e-116">Falls Sie die vorgegebenen Felder von Rolle und Organisationseinheit als Preisdimensionen vor Version 3 von PSA verwenden, gibt es keine wahrnehmbare Änderung.</span><span class="sxs-lookup"><span data-stu-id="de45e-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="de45e-117">Sie können Project Service wie gehabt verwenden.</span><span class="sxs-lookup"><span data-stu-id="de45e-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="de45e-118">Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="de45e-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="de45e-119">Weitere Informationen finden Sie in den folgenden Themen. Beachten Sie jedoch, dass Sie die Vorgehensweisen in der unten angegebenen Reihenfolge abschließen müssen:</span><span class="sxs-lookup"><span data-stu-id="de45e-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="de45e-120">Erstellen benutzerdefinierter Felder und Entitäten</span><span class="sxs-lookup"><span data-stu-id="de45e-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="de45e-121">Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten</span><span class="sxs-lookup"><span data-stu-id="de45e-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="de45e-122">Einrichten von benutzerdefinierten Feldern als Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="de45e-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="de45e-123">Aktualisieren von Plug-In-Attributen zum Einbinden neuer Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="de45e-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="de45e-124">Preise für die Personalzeit</span><span class="sxs-lookup"><span data-stu-id="de45e-124">Pricing human resource time</span></span>
<span data-ttu-id="de45e-125">Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt.</span><span class="sxs-lookup"><span data-stu-id="de45e-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="de45e-126">Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de45e-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="de45e-127">Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten.</span><span class="sxs-lookup"><span data-stu-id="de45e-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="de45e-128">Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen.</span><span class="sxs-lookup"><span data-stu-id="de45e-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="de45e-129">Sie sollten auch berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll.</span><span class="sxs-lookup"><span data-stu-id="de45e-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="de45e-130">Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, können Sie anstelle eines Optionssatzes eine Entität erstellen.</span><span class="sxs-lookup"><span data-stu-id="de45e-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="de45e-131">Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Benutzern durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="de45e-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="de45e-132">Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="de45e-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="de45e-133">Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="de45e-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="de45e-134">In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="de45e-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="de45e-135">**Beispielrechnungssätze**</span><span class="sxs-lookup"><span data-stu-id="de45e-135">**Sample bill rates**</span></span>

| <span data-ttu-id="de45e-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="de45e-136">Role</span></span>        | <span data-ttu-id="de45e-137">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="de45e-137">Org Unit</span></span>    |<span data-ttu-id="de45e-138">Einheit</span><span class="sxs-lookup"><span data-stu-id="de45e-138">Unit</span></span>      |<span data-ttu-id="de45e-139">Preis</span><span class="sxs-lookup"><span data-stu-id="de45e-139">Price</span></span>      |<span data-ttu-id="de45e-140">Währung</span><span class="sxs-lookup"><span data-stu-id="de45e-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="de45e-141">Entwickler</span><span class="sxs-lookup"><span data-stu-id="de45e-141">Developer</span></span>   | <span data-ttu-id="de45e-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="de45e-142">Contoso US</span></span>  |<span data-ttu-id="de45e-143">Hour</span><span class="sxs-lookup"><span data-stu-id="de45e-143">Hour</span></span> | <span data-ttu-id="de45e-144">200</span><span class="sxs-lookup"><span data-stu-id="de45e-144">200</span></span>|<span data-ttu-id="de45e-145">USD</span><span class="sxs-lookup"><span data-stu-id="de45e-145">USD</span></span>     |
| <span data-ttu-id="de45e-146">Entwickler</span><span class="sxs-lookup"><span data-stu-id="de45e-146">Developer</span></span>   | <span data-ttu-id="de45e-147">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="de45e-147">Contoso India</span></span> |<span data-ttu-id="de45e-148">Hour</span><span class="sxs-lookup"><span data-stu-id="de45e-148">Hour</span></span>|   <span data-ttu-id="de45e-149">112</span><span class="sxs-lookup"><span data-stu-id="de45e-149">112</span></span>|<span data-ttu-id="de45e-150">USD</span><span class="sxs-lookup"><span data-stu-id="de45e-150">USD</span></span>     |


<span data-ttu-id="de45e-151">**Beispielkostensätze**</span><span class="sxs-lookup"><span data-stu-id="de45e-151">**Sample cost rates**</span></span>

| <span data-ttu-id="de45e-152">Gehaltsspanne</span><span class="sxs-lookup"><span data-stu-id="de45e-152">Salary Band</span></span>     | <span data-ttu-id="de45e-153">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="de45e-153">Org Unit</span></span>    |<span data-ttu-id="de45e-154">Einheit</span><span class="sxs-lookup"><span data-stu-id="de45e-154">Unit</span></span>      |<span data-ttu-id="de45e-155">Preis</span><span class="sxs-lookup"><span data-stu-id="de45e-155">Price</span></span>      |<span data-ttu-id="de45e-156">Währung</span><span class="sxs-lookup"><span data-stu-id="de45e-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="de45e-157">Mein Unternehmen_Band1</span><span class="sxs-lookup"><span data-stu-id="de45e-157">My company_Band1</span></span> | <span data-ttu-id="de45e-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="de45e-158">Contoso US</span></span>  |<span data-ttu-id="de45e-159">Hour</span><span class="sxs-lookup"><span data-stu-id="de45e-159">Hour</span></span> | <span data-ttu-id="de45e-160">145</span><span class="sxs-lookup"><span data-stu-id="de45e-160">145</span></span>|<span data-ttu-id="de45e-161">USD</span><span class="sxs-lookup"><span data-stu-id="de45e-161">USD</span></span>     |
| <span data-ttu-id="de45e-162">Mein Unternehmen_Band2</span><span class="sxs-lookup"><span data-stu-id="de45e-162">My company_Band2</span></span> | <span data-ttu-id="de45e-163">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="de45e-163">Contoso India</span></span> |<span data-ttu-id="de45e-164">Hour</span><span class="sxs-lookup"><span data-stu-id="de45e-164">Hour</span></span>|   <span data-ttu-id="de45e-165">67</span><span class="sxs-lookup"><span data-stu-id="de45e-165">67</span></span>|<span data-ttu-id="de45e-166">USD</span><span class="sxs-lookup"><span data-stu-id="de45e-166">USD</span></span>     |
