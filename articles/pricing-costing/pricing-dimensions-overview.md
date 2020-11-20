---
title: Preisdimensionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung von Preisdimensionen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128462"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="4e4e9-103">Preisdimensionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="4e4e9-103">Pricing dimensions overview</span></span>

<span data-ttu-id="4e4e9-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="4e4e9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4e4e9-105">Die Dimensionen, die in der Personalverwaltung zum Einrichten von Preisen und Kosten verwendet werden, lassen sich in zwei Kategorien einteilen:</span><span class="sxs-lookup"><span data-stu-id="4e4e9-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="4e4e9-106">Personen</span><span class="sxs-lookup"><span data-stu-id="4e4e9-106">People</span></span>
- <span data-ttu-id="4e4e9-107">Geplante Arbeit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-107">Planned work</span></span>

<span data-ttu-id="4e4e9-108">Aus diesem Grund stehen zwei Arten von Preisdimensionswerten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="4e4e9-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="4e4e9-109">**Optionssätze**: Dimensionen, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="4e4e9-110">**Entität-basierte Werte**: Dimensionen, bei denen es sich um unterschiedliche Sätze von Werten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="4e4e9-111">Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="4e4e9-111">Pricing dimensions</span></span>

<span data-ttu-id="4e4e9-112">Dynamics 365 Project Operations wird mit einem Standardsatz von Preisdimensionen geliefert.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="4e4e9-113">Sie können diese Preisdimensionen anzeigen, indem Sie zu **Project Operations** > **Parameter** navigieren.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="4e4e9-114">Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="4e4e9-115">Wenn diese Felder aktiviert sind, können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="4e4e9-116">Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="4e4e9-117">Preise für die Personalzeit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-117">Pricing human resource time</span></span>
<span data-ttu-id="4e4e9-118">Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="4e4e9-119">Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="4e4e9-120">Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="4e4e9-121">Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="4e4e9-122">Sie sollten ebenfalls berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="4e4e9-123">Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, können Sie anstelle eines Optionssatzes eine Entität erstellen.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="4e4e9-124">Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Benutzern durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="4e4e9-125">Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="4e4e9-126">Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="4e4e9-127">In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="4e4e9-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="4e4e9-128">**Beispielrechnungssätze**</span><span class="sxs-lookup"><span data-stu-id="4e4e9-128">**Sample bill rates**</span></span>

| <span data-ttu-id="4e4e9-129">Rolle</span><span class="sxs-lookup"><span data-stu-id="4e4e9-129">Role</span></span>        | <span data-ttu-id="4e4e9-130">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-130">Org Unit</span></span>    |<span data-ttu-id="4e4e9-131">Einheit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-131">Unit</span></span>      |<span data-ttu-id="4e4e9-132">Preis</span><span class="sxs-lookup"><span data-stu-id="4e4e9-132">Price</span></span>      |<span data-ttu-id="4e4e9-133">Währung</span><span class="sxs-lookup"><span data-stu-id="4e4e9-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4e4e9-134">Entwickler</span><span class="sxs-lookup"><span data-stu-id="4e4e9-134">Developer</span></span>   | <span data-ttu-id="4e4e9-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4e4e9-135">Contoso US</span></span>  |<span data-ttu-id="4e4e9-136">Hour</span><span class="sxs-lookup"><span data-stu-id="4e4e9-136">Hour</span></span> | <span data-ttu-id="4e4e9-137">200</span><span class="sxs-lookup"><span data-stu-id="4e4e9-137">200</span></span>|<span data-ttu-id="4e4e9-138">USD</span><span class="sxs-lookup"><span data-stu-id="4e4e9-138">USD</span></span>     |
| <span data-ttu-id="4e4e9-139">Entwickler</span><span class="sxs-lookup"><span data-stu-id="4e4e9-139">Developer</span></span>   | <span data-ttu-id="4e4e9-140">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="4e4e9-140">Contoso India</span></span> |<span data-ttu-id="4e4e9-141">Hour</span><span class="sxs-lookup"><span data-stu-id="4e4e9-141">Hour</span></span>|   <span data-ttu-id="4e4e9-142">112</span><span class="sxs-lookup"><span data-stu-id="4e4e9-142">112</span></span>|<span data-ttu-id="4e4e9-143">USD</span><span class="sxs-lookup"><span data-stu-id="4e4e9-143">USD</span></span>     |


<span data-ttu-id="4e4e9-144">**Beispielkostensätze**</span><span class="sxs-lookup"><span data-stu-id="4e4e9-144">**Sample cost rates**</span></span>

| <span data-ttu-id="4e4e9-145">Gehaltsspanne</span><span class="sxs-lookup"><span data-stu-id="4e4e9-145">Salary Band</span></span>     | <span data-ttu-id="4e4e9-146">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-146">Org Unit</span></span>    |<span data-ttu-id="4e4e9-147">Einheit</span><span class="sxs-lookup"><span data-stu-id="4e4e9-147">Unit</span></span>      |<span data-ttu-id="4e4e9-148">Preis</span><span class="sxs-lookup"><span data-stu-id="4e4e9-148">Price</span></span>      |<span data-ttu-id="4e4e9-149">Währung</span><span class="sxs-lookup"><span data-stu-id="4e4e9-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="4e4e9-150">Mein Unternehmen_Band1</span><span class="sxs-lookup"><span data-stu-id="4e4e9-150">My company_Band1</span></span> | <span data-ttu-id="4e4e9-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4e4e9-151">Contoso US</span></span>  |<span data-ttu-id="4e4e9-152">Hour</span><span class="sxs-lookup"><span data-stu-id="4e4e9-152">Hour</span></span> | <span data-ttu-id="4e4e9-153">145</span><span class="sxs-lookup"><span data-stu-id="4e4e9-153">145</span></span>|<span data-ttu-id="4e4e9-154">USD</span><span class="sxs-lookup"><span data-stu-id="4e4e9-154">USD</span></span>     |
| <span data-ttu-id="4e4e9-155">Mein Unternehmen_Band2</span><span class="sxs-lookup"><span data-stu-id="4e4e9-155">My company_Band2</span></span> | <span data-ttu-id="4e4e9-156">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="4e4e9-156">Contoso India</span></span> |<span data-ttu-id="4e4e9-157">Hour</span><span class="sxs-lookup"><span data-stu-id="4e4e9-157">Hour</span></span>|   <span data-ttu-id="4e4e9-158">67</span><span class="sxs-lookup"><span data-stu-id="4e4e9-158">67</span></span>|<span data-ttu-id="4e4e9-159">USD</span><span class="sxs-lookup"><span data-stu-id="4e4e9-159">USD</span></span>     |
