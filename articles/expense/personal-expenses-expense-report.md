---
title: Mit persönliche Ausgaben in einer Ausgabenabrechnung arbeiten
description: Dieses Thema enthält Informationen zum Umgang mit persönlichen Ausgaben, die Mitarbeitern auf Geschäftsreisen entstehen.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025683"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="bfa24-103">Mit persönliche Ausgaben in einer Ausgabenabrechnung arbeiten</span><span class="sxs-lookup"><span data-stu-id="bfa24-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="bfa24-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="bfa24-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bfa24-105">Gelegentlich können Mitarbeiter ihre Firmenkreditkarte für persönliche Ausgaben während den Geschäftsreisen belasten.</span><span class="sxs-lookup"><span data-stu-id="bfa24-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="bfa24-106">Wenn Sie keinen Prozess für die Behandlung persönlicher Ausgaben beim Einreichen detaillierter Ausgabenabrechnungen durch Mitarbeiter definieren, kann der Genehmigungsprozess für Ausgabenabrechnungen unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="bfa24-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="bfa24-107">Es gibt zwei Methoden, mit denen Sie mit den persönlichen Ausgaben eines Mitarbeiters arbeiten können:</span><span class="sxs-lookup"><span data-stu-id="bfa24-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="bfa24-108">**Auf Kosten des Mitarbeiters**: Ihre Organisation zahlt keine persönlichen Ausgaben, die auf der Rechnung für die Firmenkreditkarte angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bfa24-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="bfa24-109">Stattdessen bezahlt der Mitarbeiter den Kreditkartenanbieter direkt für die Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="bfa24-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="bfa24-110">**Von der Firma bezahlt**: Ihre Organisation bezahlt die vollständige Rechnung für die Firmenkreditkarte und belastet dann die persönlichen Ausgaben vom Konto des Arbeitnehmers.</span><span class="sxs-lookup"><span data-stu-id="bfa24-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="bfa24-111">Sie können die Methode auswählen, die Ihre Organisation für die Seite **Spesenverwaltungsparameter** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfa24-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="bfa24-112">Aktivieren Sie die Aufteilungsausgabenfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat</span><span class="sxs-lookup"><span data-stu-id="bfa24-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="bfa24-113">Das Merkmal **Aktivieren Sie die Ausgabenaufteilungsfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat** gilt nur für Ausgabenabrechnungen, die mit einem Workflow auf Zeilenebene genehmigt wurden.</span><span class="sxs-lookup"><span data-stu-id="bfa24-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="bfa24-114">Berichte werden genehmigt, indem Sie zu **Ausgabenabrechnungen verarbeiten** > **Mir zugewiesene Ausgabenabrechnungen** > **Ausgabenabrechnung öffnen** gehen.</span><span class="sxs-lookup"><span data-stu-id="bfa24-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="bfa24-115">Um diese Funktion zu aktivieren, gehen Sie zu **Arbeitsbereiche** > **Funktionsverwaltung**, wählen **Aktivieren Sie die Aufteilungsfunktion, wenn das persönliche Betragsfeld einen Wert definiert hat**, und wählen Sie dann **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="bfa24-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="bfa24-116">Wenn die Funktion aktiviert ist, generieren Ausgabenzeilen, die diese Funktion verwenden, beim Senden des Berichts zwei Zeilen.</span><span class="sxs-lookup"><span data-stu-id="bfa24-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="bfa24-117">Es werden zwei Zeilen generiert, damit der Genehmiger jede Zeile separat genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="bfa24-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
