---
title: Preis- und Nachkalkulationsdimensions-Homepage
description: Dieses Thema enthält einen Überblick über Preisdimensionen.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368880"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="1ea0d-103">Preis- und Nachkalkulationsdimensions-Homepage</span><span class="sxs-lookup"><span data-stu-id="1ea0d-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1ea0d-104">Die Dimensionen, die zum Festlegen der Lohnkosten in projektbasierten Organisationen verwendet werden, werden von den folgenden Attributen beeinflusst:</span><span class="sxs-lookup"><span data-stu-id="1ea0d-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="1ea0d-105">Menschen, die entsprechend ihrer Erfahrung, Rolle oder Geografie arbeiten</span><span class="sxs-lookup"><span data-stu-id="1ea0d-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="1ea0d-106">Arbeiten, die entsprechend der Komplexität oder Tageszeit ausgeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="1ea0d-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="1ea0d-107">Angesichts der typischen Art dieser Arbeitsattribute und der für die Ausführung der Arbeit erforderlichen Personen stehen in Project Service Automation zwei Arten von Preisdimensionswerten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="1ea0d-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="1ea0d-108">**Optionssätze** – Attribute, bei denen es sich um feste Enumerationen für einen Satz von Werten handelt.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1ea0d-109">**Entitätsbasierte Werte** – Attribute, die unterschiedliche Werte haben können, die endlich sind, sich aber im Laufe der Zeit ändern können.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1ea0d-110">Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="1ea0d-110">Pricing dimensions</span></span>

<span data-ttu-id="1ea0d-111">PSA wird mit einem Standardsatz an Preisdimensionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1ea0d-112">Sie können diese anzeigen, indem Sie zu **Project Service** > **Parameter** navigieren.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="1ea0d-113">Prüfen Sie im Parameterdatensatz auf der Registerkarte **Betragsbasierte Preisdimensionen**, dass bei der Rolle **msdyn_resourcecategory** und der Organisationseinheit der Ressource **msdyn_organizationalunit** die Felder **Gilt für Vertrieb** und **Gilt für Kosten** auf **Ja** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1ea0d-114">Dadurch können Sie den Preis und die Kosten für jede Kombination aus Rolle und Organisationseinheit einrichten.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot der Project Service-Parameter mit Markierung von „Gilt für Vertrieb”](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="1ea0d-116">Falls Sie die vorgegebenen Felder von Rolle und Organisationseinheit als Preisdimensionen vor Version 3 von PSA verwenden, gibt es keine wahrnehmbare Änderung.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="1ea0d-117">Sie können Project Service wie gehabt verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="1ea0d-118">Wenn Sie einen Preis oder Kosten für Ihre Ressourcen mit zusätzlichen Attributen festlegen müssen, können Sie benutzerdefinierte Felder, Entitäten und Dimensionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="1ea0d-119">Weitere Informationen finden Sie in den folgenden Themen. Beachten Sie jedoch, dass Sie die Vorgehensweisen in der unten angegebenen Reihenfolge abschließen müssen:</span><span class="sxs-lookup"><span data-stu-id="1ea0d-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="1ea0d-120">Erstellen benutzerdefinierter Felder und Entitäten</span><span class="sxs-lookup"><span data-stu-id="1ea0d-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="1ea0d-121">Hinzufügen von benutzerdefinierten Feldern zum Preissetup und zu Transaktionsentitäten</span><span class="sxs-lookup"><span data-stu-id="1ea0d-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="1ea0d-122">Einrichten von benutzerdefinierten Feldern als Preisdimensionen </span><span class="sxs-lookup"><span data-stu-id="1ea0d-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="1ea0d-123">Aktualisieren von Plug-In-Attributen zum Einbinden neuer Preisdimensionen</span><span class="sxs-lookup"><span data-stu-id="1ea0d-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="1ea0d-124">Preise für die Personalzeit</span><span class="sxs-lookup"><span data-stu-id="1ea0d-124">Pricing human resource time</span></span>
<span data-ttu-id="1ea0d-125">Die Preisgestaltung der Personalzeit in einer Organisation ist häufig eine wichtige strategische Überlegung, die sich direkt auf die Rentabilität der Organisation auswirkt.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1ea0d-126">Arbeiten Sie mit den Finanzteams und Übungsleitern zusammen, wenn Ihre Organisation bereit ist, zu ermitteln, wie Rechnungs- und Kostensätze für die Personalzeit eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1ea0d-127">Zu den weiteren Überlegungen für Preise gehört, ob Felder oder Entitäten wiederverwendet werden sollen, die derzeit keine Preisdimensionen sind, jedoch für Ihre Organisation als Preisdimension gelten.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1ea0d-128">Felder wie **Transaktionskategorie** (**msdyn_transactioncategory**) und **Buchbare Ressource** (**bookableresource**) sind Beispiele für Kandidatendimensionen.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1ea0d-129">Sie sollten ebenfalls berücksichtigen, ob Ihre Preisdimension eine Tabelle oder ein Optionssatz sein soll.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1ea0d-130">Wenn Sie von mehr als 10 oder 12 Änderungen an den Werten einer Dimension ausgehen und Sie zusätzliche Attribute für diese Werte benötigen, erstellen Sie anstelle eines Optionssatzes eine Entität.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="1ea0d-131">Das Verwalten eines Optionssatzes, z. B. das Hinzufügen oder Entfernen von Werten, erfordert einen Administrator oder Entwickler, während das Hinzufügen neuer Zeilen zu einer Tabelle von den meisten Geschäftsbenutzern durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="1ea0d-132">Das folgende Beispiel zeigt Rechnungssätze, die basierend auf der Rolle und der Organisationseinheit der Ressource, zu der die Ressource gehört, eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1ea0d-133">Kostensätze basieren in der Regel auf der Gehaltsspanne des Mitarbeiters und der Organisationseinheit, die er zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1ea0d-134">In diesem Beispiel sehen die Abrechnungs- und Kostensatztabellen wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="1ea0d-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1ea0d-135">**Beispielrechnungssätze**</span><span class="sxs-lookup"><span data-stu-id="1ea0d-135">**Sample bill rates**</span></span>

| <span data-ttu-id="1ea0d-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="1ea0d-136">Role</span></span>        | <span data-ttu-id="1ea0d-137">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="1ea0d-137">Org Unit</span></span>    |<span data-ttu-id="1ea0d-138">Einheit</span><span class="sxs-lookup"><span data-stu-id="1ea0d-138">Unit</span></span>      |<span data-ttu-id="1ea0d-139">Preis</span><span class="sxs-lookup"><span data-stu-id="1ea0d-139">Price</span></span>      |<span data-ttu-id="1ea0d-140">Währung</span><span class="sxs-lookup"><span data-stu-id="1ea0d-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1ea0d-141">Developer</span><span class="sxs-lookup"><span data-stu-id="1ea0d-141">Developer</span></span>   | <span data-ttu-id="1ea0d-142">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="1ea0d-142">Contoso US</span></span>  |<span data-ttu-id="1ea0d-143">Stunde</span><span class="sxs-lookup"><span data-stu-id="1ea0d-143">Hour</span></span> | <span data-ttu-id="1ea0d-144">200</span><span class="sxs-lookup"><span data-stu-id="1ea0d-144">200</span></span>|<span data-ttu-id="1ea0d-145">US-Dollar</span><span class="sxs-lookup"><span data-stu-id="1ea0d-145">USD</span></span>     |
| <span data-ttu-id="1ea0d-146">Developer</span><span class="sxs-lookup"><span data-stu-id="1ea0d-146">Developer</span></span>   | <span data-ttu-id="1ea0d-147">Contoso Indien</span><span class="sxs-lookup"><span data-stu-id="1ea0d-147">Contoso India</span></span> |<span data-ttu-id="1ea0d-148">Stunde</span><span class="sxs-lookup"><span data-stu-id="1ea0d-148">Hour</span></span>|   <span data-ttu-id="1ea0d-149">112</span><span class="sxs-lookup"><span data-stu-id="1ea0d-149">112</span></span>|<span data-ttu-id="1ea0d-150">US-Dollar</span><span class="sxs-lookup"><span data-stu-id="1ea0d-150">USD</span></span>     |


<span data-ttu-id="1ea0d-151">**Beispielkostensätze**</span><span class="sxs-lookup"><span data-stu-id="1ea0d-151">**Sample cost rates**</span></span>

| <span data-ttu-id="1ea0d-152">Gehaltsspanne</span><span class="sxs-lookup"><span data-stu-id="1ea0d-152">Salary Band</span></span>     | <span data-ttu-id="1ea0d-153">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="1ea0d-153">Org Unit</span></span>    |<span data-ttu-id="1ea0d-154">Einheit</span><span class="sxs-lookup"><span data-stu-id="1ea0d-154">Unit</span></span>      |<span data-ttu-id="1ea0d-155">Preis</span><span class="sxs-lookup"><span data-stu-id="1ea0d-155">Price</span></span>      |<span data-ttu-id="1ea0d-156">Währung</span><span class="sxs-lookup"><span data-stu-id="1ea0d-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1ea0d-157">Mein Unternehmen_Band1</span><span class="sxs-lookup"><span data-stu-id="1ea0d-157">My company_Band1</span></span> | <span data-ttu-id="1ea0d-158">Contoso (USA)</span><span class="sxs-lookup"><span data-stu-id="1ea0d-158">Contoso US</span></span>  |<span data-ttu-id="1ea0d-159">Stunde</span><span class="sxs-lookup"><span data-stu-id="1ea0d-159">Hour</span></span> | <span data-ttu-id="1ea0d-160">145</span><span class="sxs-lookup"><span data-stu-id="1ea0d-160">145</span></span>|<span data-ttu-id="1ea0d-161">US-Dollar</span><span class="sxs-lookup"><span data-stu-id="1ea0d-161">USD</span></span>     |
| <span data-ttu-id="1ea0d-162">Mein Unternehmen_Band2</span><span class="sxs-lookup"><span data-stu-id="1ea0d-162">My company_Band2</span></span> | <span data-ttu-id="1ea0d-163">Contoso Indien</span><span class="sxs-lookup"><span data-stu-id="1ea0d-163">Contoso India</span></span> |<span data-ttu-id="1ea0d-164">Stunde</span><span class="sxs-lookup"><span data-stu-id="1ea0d-164">Hour</span></span>|   <span data-ttu-id="1ea0d-165">67</span><span class="sxs-lookup"><span data-stu-id="1ea0d-165">67</span></span>|<span data-ttu-id="1ea0d-166">US-Dollar</span><span class="sxs-lookup"><span data-stu-id="1ea0d-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]