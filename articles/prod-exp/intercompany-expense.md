---
title: Intercompany-Ausgaben
description: Dieses Thema enthält Informationen zur Nutzung von konzerninternen Ausgaben, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005070"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="39741-103">Intercompany-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39741-103">Intercompany expenses</span></span>

<span data-ttu-id="39741-104">Ein Arbeitnehmer, der bei einer juristischen Person in einer Organisation beschäftigt ist, kann Arbeiten für eine andere juristische Person in derselben Organisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="39741-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="39741-105">In dieser Situation können Sie die konzerninterne Ausgaben verwenden, um die Kosten des Arbeitnehmers der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="39741-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="39741-106">Die juristische Person, die den Arbeitnehmer beschäftigt, wird als leihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39741-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="39741-107">Die juristische Person, für die dem Arbeitnehmer Kosten entstehen, wird als leihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39741-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="39741-108">Bevor ein Mitarbeiter konzerninterne Ausgaben erstellen und einreichen kann, müssen Sie konzerninterne Ausgabenzeilen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39741-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="39741-109">In der ausleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** wählen Sie **Konzerninterne Ausgabenzeilen zulassen**.</span><span class="sxs-lookup"><span data-stu-id="39741-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="39741-110">Steuerbuchung für konzerninterne Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39741-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39741-111">Bevor Sie Ihre Steuergruppen verwenden können, die der ausleihenden juristischen Person anstelle der ausleihenden juristischen Person zugeordnet sind, müssen Sie diese auf der Seite Hauptbuchparameter im Inforegister Mehrwertsteuer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="39741-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="39741-112">Wenn der Parameter **Juristische Person für konzerninterne-Steuerbuchungen** auf **Quelle** und das Feld **Mehrwertsteuerregeln anwenden** auf **Nein** festgelegt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="39741-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="39741-113">Wenn der gleiche Parameter auf **Ziel** eingestellt wird, wird die Steuerkombination für die ausleihende juristischen Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="39741-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="39741-114">Wenn der Parameter bei juristischen Personen in den USA auf **Quelle** festgelegt ist, muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="39741-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="39741-115">Das Buchhaltungsmodul verwendet die Informationen aus diesem Feld für steuerbezogene Buchhaltungseinträge.</span><span class="sxs-lookup"><span data-stu-id="39741-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="39741-116">Das Verhalten ist für Vorkalkulationspositionen konsistent, die mit oder ohne Projekt gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="39741-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]