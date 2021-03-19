---
title: Komplexe Einheiten für produktbasierte Vertragszeilen verwalten – Lite
description: Dieses Thema enthält Informationen zur Unterstützung des Verkaufs von abonnementbasierten Produkten.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273332"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="db5c3-103">Komplexe Einheiten für produktbasierte Vertragszeilen verwalten – Lite</span><span class="sxs-lookup"><span data-stu-id="db5c3-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="db5c3-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="db5c3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db5c3-105">Dynamics 365 Project Operations verwendet Mengenfaktoren, um den Verkauf von Abonnement-basierten Produkten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db5c3-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="db5c3-106">Für Abonnement-basierte Produkte wird die Menge im Vertrag oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.</span><span class="sxs-lookup"><span data-stu-id="db5c3-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="db5c3-107">Der Preis der Abonnement-Software im Katalog wird als Preis pro Benutzer pro Monat gespeichert.</span><span class="sxs-lookup"><span data-stu-id="db5c3-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="db5c3-108">Während des Vertriebsprozesses wird der Preis in der Vertragszeile in der Regel als Preis pro Benutzer pro Monat angegeben, der vom Vertriebsmitarbeiter verhandelt und diskontiert wurde.</span><span class="sxs-lookup"><span data-stu-id="db5c3-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="db5c3-109">Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate.</span><span class="sxs-lookup"><span data-stu-id="db5c3-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="db5c3-110">Die Menge, die verwendet wird, um die Menge der Vertragszeile zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.</span><span class="sxs-lookup"><span data-stu-id="db5c3-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="db5c3-111">Um diese Art des Verkaufs zu unterstützen, unterstützt Project Operations das Konzept der *Mengenfaktoren*.</span><span class="sxs-lookup"><span data-stu-id="db5c3-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="db5c3-112">Mengenfaktoren basieren auf den Produktattributen.</span><span class="sxs-lookup"><span data-stu-id="db5c3-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="db5c3-113">Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, können Sie eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren markieren.</span><span class="sxs-lookup"><span data-stu-id="db5c3-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="db5c3-114">Project Operations stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="db5c3-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="db5c3-115">Wenn ein Produkt mit konfigurierten Mengenfaktoren zu einer Vertragszeile hinzugefügt wird, wird das **Menge**-Feld schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="db5c3-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="db5c3-116">Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, berechnet Project Operations die Menge der Vertragszeile.</span><span class="sxs-lookup"><span data-stu-id="db5c3-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="db5c3-117">Beispielsweise kann Dynamics 365 Sales die folgenden Eigenschaften aufweisen:</span><span class="sxs-lookup"><span data-stu-id="db5c3-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="db5c3-118">**Anzahl der Benutzer**: Die Anzahl der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="db5c3-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="db5c3-119">**Anzahl der Monate**: Die Anzahl der Abonnementmonate.</span><span class="sxs-lookup"><span data-stu-id="db5c3-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="db5c3-120">**Produkt-SKU**: Die Lagereinheit (SKU) für das Produkt.</span><span class="sxs-lookup"><span data-stu-id="db5c3-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="db5c3-121">Die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** können durch Bearbeitung der Produktposition als Mengenfaktoren gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="db5c3-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="db5c3-122">Führen Sie die folgenden Schritte aus, um Mengenfaktoren aus Produkteigenschaften zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db5c3-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="db5c3-123">Wählen Sie in **Project Operations** **Vertriebsprodukte** aus.</span><span class="sxs-lookup"><span data-stu-id="db5c3-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="db5c3-124">Öffnen Sie das Produkt, für das Sie Mengenfaktoren einrichten müssen.</span><span class="sxs-lookup"><span data-stu-id="db5c3-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="db5c3-125">Stellen Sie sicher, dass für das Produkt bereits Eigenschaften eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="db5c3-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="db5c3-126">Auf der **Projektinformations**-Seite wählen Sie die **Mengenfaktoren**-Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="db5c3-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="db5c3-127">Wählen Sie im Unterraster **+Neue Feldermittlung** aus.</span><span class="sxs-lookup"><span data-stu-id="db5c3-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="db5c3-128">Geben Sie den Namen des **Mengenfaktors** ein, und wählen Sie den Eigenschaftswert aus, der der Feldermittlung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db5c3-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="db5c3-129">Speichert und schließt das Formular.</span><span class="sxs-lookup"><span data-stu-id="db5c3-129">Save and close the form.</span></span>
7. <span data-ttu-id="db5c3-130">Wiederholen Sie die Schritte 2 bis 6 für alle Eigenschaften, die zusammen die Menge für die produktbasierte Vertragszeile bilden.</span><span class="sxs-lookup"><span data-stu-id="db5c3-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="db5c3-131">Wenn Mengenfaktoren eingerichtet sind und der Benutzer eine Vertragszeile für dieses Produkt erstellt, wird die Menge der Vertragszeile gesperrt.</span><span class="sxs-lookup"><span data-stu-id="db5c3-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="db5c3-132">Die Menge wird dann als Produkt der Eigenschaftswerte für diese Vertragszeile berechnet.</span><span class="sxs-lookup"><span data-stu-id="db5c3-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]