---
title: Erstellen einer Preisliste
description: Erstellen einer Preisliste (Project Service)
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122027"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="f3bc6-103">Erstellen einer Preisliste (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f3bc6-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f3bc6-104">Preislisten sind eine Vorlage, die Ihre Kontomanager verwenden können, um Angebote und Projekte zu erstellen und die Kosten eines Projekts festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="f3bc6-105">Sie liefern eine Positionsliste von Rollen und Ausgaben und den Preis, den Sie dafür berechnen.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="f3bc6-106">Sie können mehrere Preislisten erstellen, damit Sie gesonderte Preisstrukturen für verschiedene Regionen, in denen Sie Ihre Produkte verkaufen oder für verschiedene Vertriebskanäle verwalten können.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="f3bc6-107">Es ist eine gute Idee, mindestens eine Preisliste für jede Währung zu erstellen, in der Sie Kunden etwas in Rechnung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="f3bc6-108">Um finanzielle Vorkalkulationen für die zu liefernde Arbeit zu berechnen, müssen Sie sicherstellen, dass für jedes Projekt eine Kosten- und Verkaufspreisliste hinterlegt ist.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="f3bc6-109">Richten Sie eine Standard-Kosten- und Verkaufspreisliste ein, die für alle Projekte gilt, die in der Organisation erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="f3bc6-110">Preislisten beruhen auf Rollen und Ausgabenkategorien. Deshalb sollten Sie, ehe Sie eine Preisliste erstellen, sicherstellen, dass Sie beim Erstellen der Preisliste die Rollen und Ausgabenkategorien konfiguriert haben, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="f3bc6-111">Wechseln Sie zu **Project Service > Preislisten**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="f3bc6-112">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="f3bc6-113">Legen Sie unter **Kontext** fest, ob die Preisliste für **Kosten**, **Kaufen** oder **Vertrieb** gilt.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="f3bc6-114">Geben Sie unter **Namen** einen Namen für die Preisliste ein.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="f3bc6-115">Wählen Sie unter **Währung** die Währung, die Sie für Kosten und Rechnungsstellung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="f3bc6-116">Geben Sie unter **Zeiteinheit** die Zeitspanne an, für die die Preise gilt, beispielsweise Tag oder Stunde.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="f3bc6-117">Füllen Sie die Felder **Startdatum**, **Enddatum** und **Beschreibung** wie erforderlich aus.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="f3bc6-118">Klicken Sie auf **Speichern**, um den Datensatz zu erstellen, sodass Sie ihn weiter bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="f3bc6-119">Zum Hinzufügen eines Rollenpreises klicken Sie auf **+** unter **Rollenpreise**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="f3bc6-120">Geben Sie im Fensterbereich **Rollenpreis** die Details ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f3bc6-121">Fügen Sie bei Bedarf weitere Rollenpreise hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="f3bc6-122">Klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="f3bc6-123">Zum Hinzufügen eines Ausgabenkategoriepreises zur Preisliste klicken Sie auf **+** unter **Kategoriepreise**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="f3bc6-124">Geben Sie im Fensterbereich **Transaktionskategoriepreis** die Details ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f3bc6-125">Fügen Sie bei Bedarf weitere Kategoriepreise hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="f3bc6-126">Klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="f3bc6-127">Um Preislistenelemente zur Preisliste hinzuzufügen, klicken Sie auf **+** unter **Preislistenelemente.**</span><span class="sxs-lookup"><span data-stu-id="f3bc6-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="f3bc6-128">Geben Sie im Fensterbereich **Preislistenelement** die Details ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f3bc6-129">Fügen Sie bei Bedarf weitere Preislistenelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="f3bc6-130">Klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="f3bc6-131">Um Gebietsbeziehungen zur Preisliste hinzuzufügen, klicken Sie auf **+** unter **Gebietsbeziehungen**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="f3bc6-132">Geben Sie im Fenster **Neue Verbindung** die Details ein, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="f3bc6-133">Fügen Sie bei Bedarf weitere Gebietsbeziehungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="f3bc6-134">Klicken Sie auf **Speichern** in der unteren rechten Ecke des Bildschirms, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="f3bc6-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f3bc6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3bc6-135">See Also</span></span>  
 [<span data-ttu-id="f3bc6-136">Project Service Automation konfigurieren</span><span class="sxs-lookup"><span data-stu-id="f3bc6-136">Configure Project Service Automation</span></span>](../psa/configure.md)
