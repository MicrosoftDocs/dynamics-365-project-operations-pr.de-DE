---
title: Preisdimensionen – Übersicht
description: Dieses Thema enthält Informationen zur Verwendung von Preisdimensionen in Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898215"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="fb013-103">Preisdimensionen – Übersicht</span><span class="sxs-lookup"><span data-stu-id="fb013-103">Pricing dimensions overview</span></span>

<span data-ttu-id="fb013-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="fb013-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb013-105">Die Dimensionen, die in der Personalverwaltung zum Einrichten von Preisen und Kosten verwendet werden, lassen sich in zwei Kategorien einteilen:</span><span class="sxs-lookup"><span data-stu-id="fb013-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="fb013-106">Personen</span><span class="sxs-lookup"><span data-stu-id="fb013-106">People</span></span>
- <span data-ttu-id="fb013-107">Geplante Arbeit</span><span class="sxs-lookup"><span data-stu-id="fb013-107">Planned work</span></span>

<span data-ttu-id="fb013-108">Aus diesem Grund stehen zwei Arten von Preisdimensionswerten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="fb013-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="fb013-109">**Optionssätze**: Dimensionen, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.</span><span class="sxs-lookup"><span data-stu-id="fb013-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="fb013-110">**Entität-basierte Werte**: Dimensionen, bei denen es sich um unterschiedliche Sätze von Werten handeln kann.</span><span class="sxs-lookup"><span data-stu-id="fb013-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="fb013-111">Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="fb013-111">Pricing dimensions</span></span>

<span data-ttu-id="fb013-112">Dynamics 365 Project Operations wird mit einem Standardsatz von Preisdimensionen geliefert.</span><span class="sxs-lookup"><span data-stu-id="fb013-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="fb013-113">Sie können diese Preisdimensionen anzeigen, indem Sie zu **Project Operations** > **Parameter** navigieren.</span><span class="sxs-lookup"><span data-stu-id="fb013-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="fb013-114">Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="fb013-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="fb013-115">Wenn diese Felder aktiviert sind, können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.</span><span class="sxs-lookup"><span data-stu-id="fb013-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="fb013-116">Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="fb013-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="fb013-117">Preise für die Personalzeit</span><span class="sxs-lookup"><span data-stu-id="fb013-117">Pricing human resource time</span></span>
<span data-ttu-id="fb013-118">Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt.</span><span class="sxs-lookup"><span data-stu-id="fb013-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="fb013-119">Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb013-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="fb013-120">Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten.</span><span class="sxs-lookup"><span data-stu-id="fb013-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="fb013-121">Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen.</span><span class="sxs-lookup"><span data-stu-id="fb013-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="fb013-122">Sie sollten ebenfalls berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll.</span><span class="sxs-lookup"><span data-stu-id="fb013-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="fb013-123">Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, können Sie anstelle eines Optionssatzes eine Entität erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb013-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="fb013-124">Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Benutzern durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb013-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="fb013-125">Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="fb013-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="fb013-126">Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="fb013-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="fb013-127">In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="fb013-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="fb013-128">**Beispielrechnungssätze**</span><span class="sxs-lookup"><span data-stu-id="fb013-128">**Sample bill rates**</span></span>

| <span data-ttu-id="fb013-129">Rolle</span><span class="sxs-lookup"><span data-stu-id="fb013-129">Role</span></span>        | <span data-ttu-id="fb013-130">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="fb013-130">Org Unit</span></span>    |<span data-ttu-id="fb013-131">Einheit</span><span class="sxs-lookup"><span data-stu-id="fb013-131">Unit</span></span>      |<span data-ttu-id="fb013-132">Preis</span><span class="sxs-lookup"><span data-stu-id="fb013-132">Price</span></span>      |<span data-ttu-id="fb013-133">Währung</span><span class="sxs-lookup"><span data-stu-id="fb013-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="fb013-134">Entwickler</span><span class="sxs-lookup"><span data-stu-id="fb013-134">Developer</span></span>   | <span data-ttu-id="fb013-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="fb013-135">Contoso US</span></span>  |<span data-ttu-id="fb013-136">Hour</span><span class="sxs-lookup"><span data-stu-id="fb013-136">Hour</span></span> | <span data-ttu-id="fb013-137">200</span><span class="sxs-lookup"><span data-stu-id="fb013-137">200</span></span>|<span data-ttu-id="fb013-138">USD</span><span class="sxs-lookup"><span data-stu-id="fb013-138">USD</span></span>     |
| <span data-ttu-id="fb013-139">Entwickler</span><span class="sxs-lookup"><span data-stu-id="fb013-139">Developer</span></span>   | <span data-ttu-id="fb013-140">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="fb013-140">Contoso India</span></span> |<span data-ttu-id="fb013-141">Hour</span><span class="sxs-lookup"><span data-stu-id="fb013-141">Hour</span></span>|   <span data-ttu-id="fb013-142">112</span><span class="sxs-lookup"><span data-stu-id="fb013-142">112</span></span>|<span data-ttu-id="fb013-143">USD</span><span class="sxs-lookup"><span data-stu-id="fb013-143">USD</span></span>     |


<span data-ttu-id="fb013-144">**Beispielkostensätze**</span><span class="sxs-lookup"><span data-stu-id="fb013-144">**Sample cost rates**</span></span>

| <span data-ttu-id="fb013-145">Gehaltsspanne</span><span class="sxs-lookup"><span data-stu-id="fb013-145">Salary Band</span></span>     | <span data-ttu-id="fb013-146">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="fb013-146">Org Unit</span></span>    |<span data-ttu-id="fb013-147">Einheit</span><span class="sxs-lookup"><span data-stu-id="fb013-147">Unit</span></span>      |<span data-ttu-id="fb013-148">Preis</span><span class="sxs-lookup"><span data-stu-id="fb013-148">Price</span></span>      |<span data-ttu-id="fb013-149">Währung</span><span class="sxs-lookup"><span data-stu-id="fb013-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="fb013-150">Mein Unternehmen_Band1</span><span class="sxs-lookup"><span data-stu-id="fb013-150">My company_Band1</span></span> | <span data-ttu-id="fb013-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="fb013-151">Contoso US</span></span>  |<span data-ttu-id="fb013-152">Hour</span><span class="sxs-lookup"><span data-stu-id="fb013-152">Hour</span></span> | <span data-ttu-id="fb013-153">145</span><span class="sxs-lookup"><span data-stu-id="fb013-153">145</span></span>|<span data-ttu-id="fb013-154">USD</span><span class="sxs-lookup"><span data-stu-id="fb013-154">USD</span></span>     |
| <span data-ttu-id="fb013-155">Mein Unternehmen_Band2</span><span class="sxs-lookup"><span data-stu-id="fb013-155">My company_Band2</span></span> | <span data-ttu-id="fb013-156">Koch Indien</span><span class="sxs-lookup"><span data-stu-id="fb013-156">Contoso India</span></span> |<span data-ttu-id="fb013-157">Hour</span><span class="sxs-lookup"><span data-stu-id="fb013-157">Hour</span></span>|   <span data-ttu-id="fb013-158">67</span><span class="sxs-lookup"><span data-stu-id="fb013-158">67</span></span>|<span data-ttu-id="fb013-159">USD</span><span class="sxs-lookup"><span data-stu-id="fb013-159">USD</span></span>     |
