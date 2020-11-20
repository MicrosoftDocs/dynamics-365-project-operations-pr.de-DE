---
title: Korrigierte Rechnungen
description: Dieses Thema enthält Informationen zu korrigierten Rechnungen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122387"
---
# <a name="corrected-invoices"></a><span data-ttu-id="a7cb0-103">Korrigierte Rechnungen</span><span class="sxs-lookup"><span data-stu-id="a7cb0-103">Corrected invoices</span></span>

<span data-ttu-id="a7cb0-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="a7cb0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a7cb0-105">Bestätigte Rechnungen können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="a7cb0-106">Wenn Sie eine bestätigte Rechnung bearbeiten, wird eine neue korrigierte Rechnung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="a7cb0-107">Da davon ausgegangen wird, dass Sie alle Transaktionen und Mengen aus der ursprünglichen Rechnung umkehren möchten, enthält diese korrigierte Rechnung alle Transaktionen aus der ursprünglichen Rechnung, wobei sämtliche Mengen mit 0 (Null) ausgewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="a7cb0-108">Wenn Transaktionen keine Korrektur benötigen, können sie aus dem Korrekturrechnungsentwurf entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="a7cb0-109">Um eine Teilmenge umzukehren oder zurzuückgeben, können Sie das Feld Menge im Positionsdetail bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="a7cb0-110">Wenn Sie das Rechnungspositionsdetail öffnen, sehen Sie die ursprüngliche Rechnungsmenge.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="a7cb0-111">Sie können die aktuelle Rechnungsmenge bearbeiten, indem Sie die ursprüngliche Rechnungsmenge erhöhen oder reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="a7cb0-112">Wenn Sie eine Korrekturrechnung bestätigen, wird der ursprüngliche abgerechnete vertriebliche Ist-Wert umgekehrt und ein neuer abgerechneter vertrieblicher Ist-Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="a7cb0-113">Wenn die Menge reduziert wurde, wird aufgrund der Differenz auch ein neuer, nicht abgerechneter vertrieblicher Ist-Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="a7cb0-114">Wenn beispielsweise der ursprüngliche abgerechnete Wert acht Stunden war, und die korrigierte Rechnungszeile eine reduzierte Menge von sechs Stunden aufweist, wird die ursprüngliche abgerechnete Vertriebszeile stornier und zwei neue Ist-Werte werden erstellt:</span><span class="sxs-lookup"><span data-stu-id="a7cb0-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="a7cb0-115">Einen abgerechneten vertrieblichen Ist-Wert für sechs Stunden.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="a7cb0-116">Einen nicht abgerechneten vertrieblichen Ist-Wert für die verbleibenden zwei Stunden.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="a7cb0-117">Diese Transaktion kann – abhängig von den Verhandlungen mit dem Kunden – später entweder abgerechnet oder als nicht fakturierbar markiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7cb0-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
