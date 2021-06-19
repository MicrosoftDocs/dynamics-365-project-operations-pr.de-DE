---
title: Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen und anwenden
description: Dieses Thema enthält Informationen zum Einrichten und Verwalten von Bedingungen für die Einbehaltung von Kreditorenzahlungen.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006324"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="9230d-103">Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen und anwenden</span><span class="sxs-lookup"><span data-stu-id="9230d-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="9230d-104">Das Einrichten von Bedingungen für die Einbehaltung von Kreditorenzahlungen für ein Projekt ist nützlich, wenn Ihre Organisation einen Teil der an einen Kreditor geleisteten Zahlungen einbehalten möchte.</span><span class="sxs-lookup"><span data-stu-id="9230d-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="9230d-105">Wenn Sie die Zahlung an einen Kreditor beispielsweise so lange einbehalten möchten, bis die gelieferten Produkte, Ihren Erwartungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9230d-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="9230d-106">Bedingungen für die Einbehaltung von Kreditorenzahlungen können angegeben werden, wenn Sie einen Kreditorenvertrag aushandeln.</span><span class="sxs-lookup"><span data-stu-id="9230d-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="9230d-107">Bedingungen für die Einbehaltung von Kreditorenzahlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="9230d-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="9230d-108">Sie können den Prozentsatz der Kreditorenzahlung für die Einbehaltung und den Prozentsatz der zuvor einbehaltenden Beträge eingeben, die freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9230d-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="9230d-109">Beträge werden automatisch auf Kreditorenrechnungen einbehalten, bis der Vertrag den angegebenen Fertigstellungsstatus erreicht.</span><span class="sxs-lookup"><span data-stu-id="9230d-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="9230d-110">Nachdem Sie die Bedingungen für die Einbehaltung eingerichtet haben, können Sie sie auf jedes Projekt für diesen Kreditor anwenden.</span><span class="sxs-lookup"><span data-stu-id="9230d-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="9230d-111">Führen Sie die folgenden Schritte aus, um Bedingungen für die Einbehaltung von Kreditorenzahlungen einzurichten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9230d-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="9230d-112">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Einbehaltung** > **Bedingungen für einbehaltene Kreditorenzahlungen**.</span><span class="sxs-lookup"><span data-stu-id="9230d-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="9230d-113">Wählen Sie **Neu** aus, um eine neue Bedingung für die Einbehaltung von Kreditorenzahlungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9230d-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="9230d-114">Der Wert **Regel-ID** für die neue Bedingung wird automatisch eingegeben.</span><span class="sxs-lookup"><span data-stu-id="9230d-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="9230d-115">Geben Sie eine kurze Beschreibung in das Feld **Beschreibung** ein, und wählen Sie im Inforegister **Bedingungen** die Option **Zeile hinzufügen** aus, um Werte für die Bedingung für folgende Optionen einzugeben:</span><span class="sxs-lookup"><span data-stu-id="9230d-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="9230d-116">**Prozentsatz der gelieferten Einheiten**: Geben Sie einen Prozentsatz für die Fertigstellung für die Bedingung ein.</span><span class="sxs-lookup"><span data-stu-id="9230d-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="9230d-117">Beträge werden automatisch auf Kreditorenrechnungen einbehalten, bis der Projektstatus des Abschlusses dem angegebenen Prozentsatz entspricht.</span><span class="sxs-lookup"><span data-stu-id="9230d-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="9230d-118">Wenn Sie beispielsweise 50,00 eingeben, werden die Beträge einbehalten, bis das Projekt zu 50 Prozent abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9230d-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="9230d-119">**Einzubehaltender Prozentsatz** : Geben Sie einen Prozentsatz des Kreditorenrechnungsbetrags ein, der einbehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="9230d-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="9230d-120">Wenn Sie beispielsweise 10,00 eingeben, werden 10 Prozent des Betrags auf einer Kreditorenrechnung einbehalten, bis das Projekt den im Abschnitt festgelegten Prozentsatz des Abschlusses, wie in **Prozentsatz der gelieferten Einheiten** festgelegt, erreicht.</span><span class="sxs-lookup"><span data-stu-id="9230d-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="9230d-121">**Freizugebender Prozentsatz**: Wählen Sie **Zeile hinzufügen** aus, um einen Prozentsatz aller zuvor einbehaltenen Beträge einzugeben, die für die ausgewählte Stufe des Projektabschlusses freigegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9230d-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="9230d-122">Wenn Sie mehr als einen Meilenstein für verschiedene Stufen des Projektabschlusses haben, geben Sie für jede Einbehaltungsregel eine separate Zeile für die Bedingung zum Einbehalt der Kreditorenrechnung ein.</span><span class="sxs-lookup"><span data-stu-id="9230d-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="9230d-123">Jede Zeile kann für jede festgelegte Projektabschlussstufe einen anderen Prozentsatz für die Einbehaltung und einen anderen Prozentsatz für die Freigabe angeben.</span><span class="sxs-lookup"><span data-stu-id="9230d-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="9230d-124">Nachdem Sie Bedingungen für die Einbehaltung von Kreditorenzahlungen für einen Kreditor eingegeben haben, können Sie die Bedingungen auf ein Projekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="9230d-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="9230d-125">Bedingungen für die Einbehaltung von Kreditorenzahlungen auf ein Projekt anwenden</span><span class="sxs-lookup"><span data-stu-id="9230d-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="9230d-126">Navigieren Sie zu **Projektmanagement und -buchhaltung** > **Projekte** > **Alle Projekte**, und öffnen Sie ein Projekt aus der Projektlistenseite aus.</span><span class="sxs-lookup"><span data-stu-id="9230d-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="9230d-127">Wählen Sie im Inforegister **Kreditorenvereinbarungen** die Option **Zeile hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="9230d-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="9230d-128">Wählen Sie im Feld **Kontocode** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="9230d-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="9230d-129">**Tabelle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für einen einzelnen Kreditor.</span><span class="sxs-lookup"><span data-stu-id="9230d-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="9230d-130">**Gruppe** : Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren in einer Kreditorengruppe.</span><span class="sxs-lookup"><span data-stu-id="9230d-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="9230d-131">**Alle**: Die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten für alle Kreditoren.</span><span class="sxs-lookup"><span data-stu-id="9230d-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="9230d-132">Wählen Sie im Feld **Kreditor/Kreditorengruppe** den Kreditor oder die Kreditorengruppe aus, für die die Bedingungen für die Einbehaltung von Kreditorenzahlungen gelten soll.</span><span class="sxs-lookup"><span data-stu-id="9230d-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="9230d-133">Wenn Sie im vorherigen Schritt **Alle** ausgewählt haben, ist dieses Feld nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9230d-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="9230d-134">Wählen Sie im Feld **Bedingungen für einbehaltene Kreditorenbeträge** die Bedingungen für die Einbehaltung aus, die Sie im vorherigen Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9230d-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="9230d-135">Wenn für das Projekt auch Bedingungen zur Zahlung bei Zahlungsempfang für den Kreditor eingerichtet wurden, geben Sie den Schwellenwertprozentsatz für das Projekt im Feld **Pay When Paid - Schwellenwertprozentsatz** ein.</span><span class="sxs-lookup"><span data-stu-id="9230d-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="9230d-136">Die Bedingungen für die Einbehaltung von Kreditorenzahlungen werden auch in Bestellungen angezeigt, die Sie für den Kreditor erstellen.</span><span class="sxs-lookup"><span data-stu-id="9230d-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]