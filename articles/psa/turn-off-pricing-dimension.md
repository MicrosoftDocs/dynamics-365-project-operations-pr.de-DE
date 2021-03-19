---
title: Deaktivieren einer Preisdimension
description: In diesem Thema wird gezeigt, wie Preisdimensionen in der Project Service-Lösung eingerichtet werden.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281837"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="ec81b-103">Deaktivieren einer Preisdimension</span><span class="sxs-lookup"><span data-stu-id="ec81b-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ec81b-104">Möglicherweise müssen Sie Ihre Preisstrategie alle paar Jahre überprüfen und aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ec81b-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="ec81b-105">Alle Updates, die Sie vornehmen, erfordern möglicherweise, dass Sie sämtliche vorhandenen Preisdimensionen deaktivieren und eine neue erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec81b-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="ec81b-106">Beispielsweise haben Sie möglicherweise die Preise nach **Rolle** festgelegt, aber jetzt haben Sie sich entschieden, die Preise nach **Berufserfahrung** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ec81b-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="ec81b-107">Hierfür müssen sie möglicherweise **Rolle** als Preisdimension deaktivieren und **Berufserfahrung** als neue Preisdimension erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec81b-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="ec81b-108">Das Deaktivieren einer Preisdimension, unabhängig davon, ob sie vorkonfiguriert oder benutzerdefiniert ist, kann ausgeführt werden, indem die Felder **Gilt für Kosten** und **Gilt für Vertrieb** der Preisdimension auf **Nein** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec81b-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="ec81b-109">Dabei erhalten Sie aber möglicherweise die folgende Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="ec81b-109">However, when you do this, you might receive the following error message.</span></span>

![Geschäftsprozessfehler wahrscheinlich, wenn eine Preisdimension deaktiviert wird](media/Business-Process-Error.png)


<span data-ttu-id="ec81b-111">Diese Fehlermeldung gibt an, dass es Preisdatensätze gibt, die zuvor für die Dimension eingerichtet wurden, die gerade deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ec81b-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="ec81b-112">Alle **Rollenpreis**- und **Rollenpreisaufschlag**-Datensätze, die auf eine Dimension verweisen, müssen gelöscht werden, bevor die Anwendbarkeit der Dimension auf **Nein** festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec81b-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="ec81b-113">Diese Regel gilt sowohl für vorkonfigurierte Preisdimensionen als auch für sämtliche benutzerdefinierten Preisdimensionen, die Sie möglicherweise erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="ec81b-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="ec81b-114">Der Grund für diese Überprüfung liegt darin, dass Project Service eine Einschränkung hat, dass jeder **Rollenpreis**-Datensatz eine eindeutige Kombination von Dimensionen haben muss.</span><span class="sxs-lookup"><span data-stu-id="ec81b-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="ec81b-115">Für eine Preisliste mit der Bezeichnung **US-Kostensätze 2018** haben Sie die folgenden **Rollenpreis**-Zeilen.</span><span class="sxs-lookup"><span data-stu-id="ec81b-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="ec81b-116">Standardtitel</span><span class="sxs-lookup"><span data-stu-id="ec81b-116">Standard Title</span></span>         | <span data-ttu-id="ec81b-117">Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="ec81b-117">Org Unit</span></span>    |<span data-ttu-id="ec81b-118">Einheit</span><span class="sxs-lookup"><span data-stu-id="ec81b-118">Unit</span></span>   |<span data-ttu-id="ec81b-119">Preis</span><span class="sxs-lookup"><span data-stu-id="ec81b-119">Price</span></span>  |<span data-ttu-id="ec81b-120">Währung</span><span class="sxs-lookup"><span data-stu-id="ec81b-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="ec81b-121">Systemtechniker</span><span class="sxs-lookup"><span data-stu-id="ec81b-121">Systems Engineer</span></span>|<span data-ttu-id="ec81b-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ec81b-122">Contoso US</span></span>|<span data-ttu-id="ec81b-123">Hour</span><span class="sxs-lookup"><span data-stu-id="ec81b-123">Hour</span></span>| <span data-ttu-id="ec81b-124">100</span><span class="sxs-lookup"><span data-stu-id="ec81b-124">100</span></span>|<span data-ttu-id="ec81b-125">USD</span><span class="sxs-lookup"><span data-stu-id="ec81b-125">USD</span></span>|
| <span data-ttu-id="ec81b-126">Leitender Systemtechniker</span><span class="sxs-lookup"><span data-stu-id="ec81b-126">Senior Systems Engineer</span></span>|<span data-ttu-id="ec81b-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ec81b-127">Contoso US</span></span>|<span data-ttu-id="ec81b-128">Hour</span><span class="sxs-lookup"><span data-stu-id="ec81b-128">Hour</span></span>| <span data-ttu-id="ec81b-129">150</span><span class="sxs-lookup"><span data-stu-id="ec81b-129">150</span></span>| <span data-ttu-id="ec81b-130">USD</span><span class="sxs-lookup"><span data-stu-id="ec81b-130">USD</span></span>|


<span data-ttu-id="ec81b-131">Wenn Sie **Standardtitel** als Preisdimension deaktivieren und das Project Service-Preismodul nach einem Preis sucht, verwendet es nur den Wert **Organisationseinheit** aus dem Eingabekontext.</span><span class="sxs-lookup"><span data-stu-id="ec81b-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="ec81b-132">Wenn die **Organisationseinheit** des Eingabekontexts „Contoso US” ist, ist das Ergebnis nicht deterministisch, da beide Zeilen übereinstimmen werden.</span><span class="sxs-lookup"><span data-stu-id="ec81b-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="ec81b-133">Um dieses Szenario zu vermeiden, wenn Sie **Rollenpreis**-Datensätze erstellen, überprüft Project Service, dass die Kombination der Dimensionen eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="ec81b-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="ec81b-134">Wenn die Dimension deaktiviert wird, nachdem die **Rollenpreis**-Datensätze erstellt sind, kann gegen diese Einschränkung verstoßen werden.</span><span class="sxs-lookup"><span data-stu-id="ec81b-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="ec81b-135">Daher ist es erforderlich, dass Sie, bevor Sie eine Dimension deaktivieren, alle **Rollenpreis**- und **Rollenpreisaufschlag**-Zeilen löschen, bei denen dieser Dimensionswert aufgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ec81b-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]