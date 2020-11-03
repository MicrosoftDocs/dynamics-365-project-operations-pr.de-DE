---
title: Persönliche Ausgaben in einer Spesenabrechnung
description: In diesem Thema werden die beiden Methoden zur Behandlung der persönlichen Ausgaben eines Mitarbeiters in Microsoft Dynamics 365 Finance erläutert.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076673"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="e7749-103">Persönliche Ausgaben in einer Spesenabrechnung</span><span class="sxs-lookup"><span data-stu-id="e7749-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7749-104">Während einer Geschäftsreise belasten Mitarbeiter manchmal ihre Firmenkreditkarten mit persönlichen Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="e7749-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="e7749-105">Wenn Sie keinen Prozess für die Bearbeitung persönlicher Ausgaben definieren, wird der Genehmigungsprozess für Spesenabrechnungen möglicherweise unterbrochen, wenn Mitarbeiter ihre detaillierten Spesenabrechnungen einreichen.</span><span class="sxs-lookup"><span data-stu-id="e7749-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="e7749-106">Es gibt zwei Methoden, um mit den persönlichen Ausgaben eines Arbeitnehmers umzugehen:</span><span class="sxs-lookup"><span data-stu-id="e7749-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="e7749-107">**Auf Kosten des Mitarbeiters** – Ihre Organisation zahlt keine persönlichen Ausgaben, die auf der Rechnung für die Firmenkreditkarte angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e7749-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="e7749-108">Stattdessen wird ein Bericht erstellt, in dem die persönlichen Ausgaben zusammen mit den Unternehmensausgaben angezeigt werden, die der Unternehmenskreditkarte belastet wurden.</span><span class="sxs-lookup"><span data-stu-id="e7749-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="e7749-109">**Auf Kosten des Unternehmens** – Ihre Organisation bezahlt die gesamte Rechnung für die Firmenkreditkarte und belastet dann die persönlichen Ausgaben vom Konto des Arbeitnehmers.</span><span class="sxs-lookup"><span data-stu-id="e7749-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="e7749-110">Sie können die Methode auswählen, die Ihre Organisation für die Seite **Spesenverwaltungsparameter** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e7749-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
