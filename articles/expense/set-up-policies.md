---
title: Kostenrichtlinien definieren
description: Sie können Ausgabenrichtlinien definieren, die Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen befolgen müssen.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896640"
---
# <a name="define-expense-policies"></a><span data-ttu-id="3d865-103">Kostenrichtlinien definieren</span><span class="sxs-lookup"><span data-stu-id="3d865-103">Define expense policies</span></span>

<span data-ttu-id="3d865-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="3d865-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d865-105">Sie können Ausgabenrichtlinien definieren, denen Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen folgen müssen.</span><span class="sxs-lookup"><span data-stu-id="3d865-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="3d865-106">Durch die Implementierung von Ausgabenrichtlinien können Sie Ausgaben effektiv verwalten.</span><span class="sxs-lookup"><span data-stu-id="3d865-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="3d865-107">Sie können beispielsweise eine Richtlinie für Hotelkosten in New York City festlegen, die besagt, dass die Kosten pro Nacht USD 250 nicht überschreiten dürfen.</span><span class="sxs-lookup"><span data-stu-id="3d865-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="3d865-108">Wenn ein Mitarbeiter eine Ausgabenabrechnung oder eine Reiseanforderung einreicht, bei der der Zimmerpreis diesen Betrag überschreitet, benachrichtigt das System den</span><span class="sxs-lookup"><span data-stu-id="3d865-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="3d865-109">Arbeitnehmer, dass der Richtlinienbetrag für die Ausgabe überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="3d865-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3d865-110">Sie können die Nachricht konfigurieren, die der Worker erhält</span><span class="sxs-lookup"><span data-stu-id="3d865-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="3d865-111">definieren der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="3d865-111">define the policy.</span></span>      
        
<span data-ttu-id="3d865-112">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="3d865-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="3d865-113">**Warnung**: Ermöglicht dem Mitarbeiter, eine Ausgabenabrechnung oder Reiseanforderung einzureichen, die Ausgaben werden jedoch für alle Genehmigenden markiert und</span><span class="sxs-lookup"><span data-stu-id="3d865-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="3d865-114">für die spätere Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="3d865-114">for later reporting.</span></span>        

- <span data-ttu-id="3d865-115">**Fehler**: Fordert den Arbeitnehmer auf, die Ausgaben zu überarbeiten, um die Richtlinien einzuhalten, bevor er die Spesenabrechnung oder die Reiseanforderung einreicht.</span><span class="sxs-lookup"><span data-stu-id="3d865-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="3d865-116">**Rechtfertigung**: Fordert den Arbeitnehmer oder einen Manager auf, vor dem Einreichen der Ausgabenabrechnung oder der Reiseanforderung eine Begründung für die Überschreitung des Richtlinienbetrags einzugeben.</span><span class="sxs-lookup"><span data-stu-id="3d865-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="3d865-117">Richtlinienhinweise</span><span class="sxs-lookup"><span data-stu-id="3d865-117">Policy tips</span></span>
<span data-ttu-id="3d865-118">Im Folgenden finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für das Ausgabenmanagement unterstützen können:</span><span class="sxs-lookup"><span data-stu-id="3d865-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="3d865-119">Richtlinien haben das Datum des Inkrafttretens. Dies bedeutet, dass eine Richtlinie nicht wirksam wird, wenn sie mit einem Datum nach dem Datum erstellt wird, an dem die Ausgabe entstanden sind.</span><span class="sxs-lookup"><span data-stu-id="3d865-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="3d865-120">Beispielsweise erstellen Sie heute eine neue Richtlinie, um eine maximale Essensausgabe von $50 durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="3d865-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="3d865-121">Bestehende Ausgaben, die ab gestern eingegeben wurden, werden nicht mit dieser Richtlinie verglichen.</span><span class="sxs-lookup"><span data-stu-id="3d865-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="3d865-122">Wenn Sie eine Richtlinie für eine Ausgabenkategorie erstellen, die aufgelistet werden kann, sollten Sie eine Bedingung für den Ausgabenzeilentyp hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d865-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="3d865-123">Einige Richtlinien, z. B. das Erfordernis einer Quittung, sind für einzelne Zeilen möglicherweise nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="3d865-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="3d865-124">In dieser Situation wird die Richtlinie nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Zeile angewendet.</span><span class="sxs-lookup"><span data-stu-id="3d865-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="3d865-125">Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet.</span><span class="sxs-lookup"><span data-stu-id="3d865-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="3d865-126">Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie anhand der Zielentität (Kreditinstanz) bewertet wird.</span><span class="sxs-lookup"><span data-stu-id="3d865-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="3d865-127">Aktivieren Sie die Funktion **Bewerten Sie die Ausgabenpolitik gegen die Aufnahme einer juristischen Person** im Arbeitsbereich **Funktionsverwaltung**, um die Richtlinien für die Zielentität auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3d865-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="3d865-128">Wann müssen die Richtlinien bewertet werden</span><span class="sxs-lookup"><span data-stu-id="3d865-128">When to evaluate policies</span></span>

<span data-ttu-id="3d865-129">In den Ausgabenmanagementparametern können Sie auswählen, ob die Ausgabenmanagementrichtlinien ausgewertet werden sollen, wenn eine Zeile gespeichert wird oder wenn eine Ausgabenabrechnung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d865-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="3d865-130">Wenn Sie auswerten möchten, wann eine Zeile gespeichert wird, haben Benutzer früher einen Überblick darüber, was sie tun müssen, um ihre Ausgabenabrechnung auf einmal zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="3d865-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="3d865-131">Andernfalls können Sie die Richtlinienbewertung verzögern und Zeit sparen, indem Sie am Ende während der Übermittlung an den Workflow validieren.</span><span class="sxs-lookup"><span data-stu-id="3d865-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
