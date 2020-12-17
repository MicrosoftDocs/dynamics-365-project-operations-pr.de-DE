---
title: Aktualisieren von Plug-In-Attributen mit neuen Preisdimensionen
description: Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643217"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="3c131-103">Plug-In-Attribute mit neuen Preisdimensionen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3c131-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="3c131-104">Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.</span><span class="sxs-lookup"><span data-stu-id="3c131-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="3c131-105">Dieses Thema gilt nur für die Angebots- und Vertragsfunktionen in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3c131-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3c131-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c131-106">Prerequisites</span></span>
<span data-ttu-id="3c131-107">Bevor Sie die Schritte in diesem Thema ausführen, müssen Sie die Verfahren in den folgenden Themen ausgeführt haben:</span><span class="sxs-lookup"><span data-stu-id="3c131-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="3c131-108">Erstellen von benutzerdefinierten Feldern und Entitäten</span><span class="sxs-lookup"><span data-stu-id="3c131-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="3c131-109">Hinzufügen von benutzerdefinierten Feldern zur Preisgestaltung und zu Transaktionsentitäten </span><span class="sxs-lookup"><span data-stu-id="3c131-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="3c131-110">[Einrichten von benutzerdefinierten Feldern als Preisdimensionen](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3c131-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="3c131-111">Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="3c131-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="3c131-112">Registrieren eines Plug-Ins</span><span class="sxs-lookup"><span data-stu-id="3c131-112">Register a plug-in</span></span>
<span data-ttu-id="3c131-113">Wenn ein Angebotszeilendetail auf der **Angebotszeile**-Seite für eine Projektangebotszeile erstellt wird, erstellt das System zwei Schätzzeilen.</span><span class="sxs-lookup"><span data-stu-id="3c131-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="3c131-114">Eine Zeile ist für die Kostenseite der Schätzung und die andere Zeile ist für den Verkauf auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="3c131-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="3c131-115">Selbes gilt auch für Projektvertragspositionen.</span><span class="sxs-lookup"><span data-stu-id="3c131-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3c131-116">Wenn Sie eine Änderung der Menge oder eines Felds auf der Kostenseite vornehmen, wird die Änderung auf der Vertriebsseite übernommen.</span><span class="sxs-lookup"><span data-stu-id="3c131-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="3c131-117">Dies ist möglich, weil die PreOperation-Plug-Ins für Quotelinedetail- und Contractline-Detailentitäten bestimmte Attribute auf der Kostenseite mit der Verkaufsseite der Transaktion verbinden.</span><span class="sxs-lookup"><span data-stu-id="3c131-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="3c131-118">Wenn Änderungen an den Werten der Preisdimension auf der Verkaufsseite auch auf der Kostenseite vorgenommen werden müssen, müssen die folgenden Plug-Ins nach Änderungen an einer Preisdimension erneut registriert werden.</span><span class="sxs-lookup"><span data-stu-id="3c131-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="3c131-119">Dies sind die Plug-Ins zum Aktualisieren und erneuten Registrieren:</span><span class="sxs-lookup"><span data-stu-id="3c131-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="3c131-120">PreOperationContractLineDetailUpdate – **msdyn_orderlinetransaction aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="3c131-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="3c131-121">PreOperationQuoteLineDetailUpdate – **msdyn_quotelinetransaction aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="3c131-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="3c131-122">Führen Sie die folgenden Schritte aus, um die Plug-Ins zu aktualisieren und neu zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="3c131-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="3c131-123">Öffnen Sie **PluginRegistrationTool** und stellen Sie eine Verbindung zu Ihrer Project Operations Dataverse-Umgebung her.</span><span class="sxs-lookup"><span data-stu-id="3c131-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="3c131-124">Wählen Sie **Suche** und geben Sie die ersten Buchstaben des zu aktualisierenden Plug-Ins ein.</span><span class="sxs-lookup"><span data-stu-id="3c131-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="3c131-125">Nachdem das Plug-In gefunden wurde, wählen Sie es aus, und klicken Sie dann auf **Hauptformular auswählen**.</span><span class="sxs-lookup"><span data-stu-id="3c131-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="3c131-126">Wählen Sie den Schritt **msdyn_orderlinetransaction aktualisieren** aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="3c131-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="3c131-127">Klicken Sie im **Update**-Dialogfeld auf die Auslassungspunkte (**...**) in den Filterattributen.</span><span class="sxs-lookup"><span data-stu-id="3c131-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="3c131-128">Das Fenster „Filterattribute“ wird geöffnet und enthält eine Liste aller Attribute in der Entität und der Preisdimensionen.</span><span class="sxs-lookup"><span data-stu-id="3c131-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="3c131-129">Aktivieren Sie die Kontrollkästchen für die Preisdimensionsattribute.</span><span class="sxs-lookup"><span data-stu-id="3c131-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="3c131-130">Wählen Sie **OK**, um die Seite zu schließen, und wählen Sie dann **Aktualisierungsschritt** aus.</span><span class="sxs-lookup"><span data-stu-id="3c131-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="3c131-131">Wiederholen Sie die Schritte 2 bis 7 für das zweite Plug-In, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="3c131-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="3c131-132">Für dieses Plug-In müssen Sie den Schritt **msdyn_quotelinetransaction aktualisieren** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3c131-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="3c131-133">Schließen Sie das **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="3c131-133">Close **PluginRegistrationTool**.</span></span>
