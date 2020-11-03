---
title: Intercompany-Ausgaben
description: Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen. In dieser Situation können Sie die konzerninterne Kostenfunktion verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076675"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="49158-104">Intercompany-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49158-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49158-105">Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="49158-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="49158-106">In dieser Situation können Sie die konzerninterne Kostenfunktion verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="49158-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="49158-107">Die juristische Person, die den Arbeitnehmer beschäftigt, wird als leihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49158-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="49158-108">Die juristische Person, für die dem Arbeitnehmer Kosten entstehen, wird als leihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49158-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="49158-109">Bevor ein Arbeitnehmer Ausgaben für Arbeiten erstellen und einreichen kann, die für eine andere juristische Person ausgeführt werden, wählen Sie in der ausleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** die Option **Konzerninterne Ausgabenpositionen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="49158-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="49158-110">Steuerbuchung für konzerninterne Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49158-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49158-111">Wenn Sie in Ihrer Spesenabrechnung Steuergruppen verwenden möchten, die der juristischen Person des Darlehens (Quelle) anstelle der juristischen Person des Darlehens (Ziel) zugeordnet sind, müssen Sie dies in der eingerichteten Umsatzsteuer der Finanzbuchhaltung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="49158-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="49158-112">Wenn der Parameter der Finanzbuchhaltung **Juristische Person für innerbetriebliche Steuerbuchungen** auf **Quelle** und **Mehrwertsteuerregeln anwenden** auf **Nein** eingestellt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="49158-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="49158-113">Wenn der gleiche Parameter auf **Ziel** eingestellt wird, wird die Steuerkombination für die ausleihende juristischen Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="49158-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="49158-114">Wenn der Parameter bei juristischen Personen in den USA auf **Quelle** festgelegt ist, muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="49158-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="49158-115">Das Buchhaltungsmodul verwendet die Informationen aus diesem Feld für steuerliche Buchhaltungseinträge.</span><span class="sxs-lookup"><span data-stu-id="49158-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="49158-116">Das Verhalten ist für Vorkalkulationspositionen konsistent, die mit oder ohne Projekt gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="49158-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
