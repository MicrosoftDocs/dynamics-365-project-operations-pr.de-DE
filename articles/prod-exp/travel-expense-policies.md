---
title: Ausgabenrichtlinien einrichten
description: Sie können die Ausgabenrichtlinien einrichten, die Ihre Mitarbeiter beim Eingeben und Senden von Spesenabrechnungen und Reiseanforderungen in Microsoft Dynamics 365 Finance befolgen müssen.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005745"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="00c4a-103">Ausgabenrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="00c4a-103">Set up expense policies</span></span>

<span data-ttu-id="00c4a-104">Sie können Ausgabenrichtlinien definieren, denen Ihre Mitarbeiter beim Eingeben und Senden von Ausgabeabrechnungen und Reiseanforderungen folgen müssen.</span><span class="sxs-lookup"><span data-stu-id="00c4a-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="00c4a-105">Durch die Implementierung von Spesenrichtlinien können Sie Spesen effektiv verwalten.</span><span class="sxs-lookup"><span data-stu-id="00c4a-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="00c4a-106">Sie können beispielsweise eine Richtlinie für Hotelkosten in New York City festlegen, die besagt, dass die Kosten pro Nacht USD 250 nicht überschreiten dürfen.</span><span class="sxs-lookup"><span data-stu-id="00c4a-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="00c4a-107">Wenn ein Mitarbeiter eine Spesenabrechnung oder eine Reiseanforderung einreicht, bei der der Zimmerpreis diesen Betrag überschreitet, benachrichtigt das System den</span><span class="sxs-lookup"><span data-stu-id="00c4a-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="00c4a-108">Arbeitnehmer, dass der Richtlinienbetrag für die Ausgabe überschritten wurde.</span><span class="sxs-lookup"><span data-stu-id="00c4a-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="00c4a-109">Sie können die Nachricht konfigurieren, die der Worker erhält</span><span class="sxs-lookup"><span data-stu-id="00c4a-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="00c4a-110">definieren der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="00c4a-110">define the policy.</span></span>      
        
<span data-ttu-id="00c4a-111">Sie können drei Arten von Richtlinien definieren:</span><span class="sxs-lookup"><span data-stu-id="00c4a-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="00c4a-112">Warnung – Ermöglicht dem Mitarbeiter, eine Spesenabrechnung oder Reiseanforderung einzureichen, die Ausgaben werden jedoch für alle Genehmigenden markiert und</span><span class="sxs-lookup"><span data-stu-id="00c4a-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="00c4a-113">für die spätere Berichterstattung.</span><span class="sxs-lookup"><span data-stu-id="00c4a-113">for later reporting.</span></span>        

- <span data-ttu-id="00c4a-114">Fehler – Fordert den Arbeitnehmer auf, die Ausgaben zu überarbeiten, um die Richtlinien einzuhalten, bevor er die Spesenabrechnung oder die Reiseanforderung einreicht</span><span class="sxs-lookup"><span data-stu-id="00c4a-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="00c4a-115">Rechtfertigung – Fordert den Arbeitnehmer oder einen Manager auf, vor dem Einreichen der Spesenabrechnung oder der Reiseanforderung eine Begründung für die Überschreitung des Richtlinienbetrags einzugeben.</span><span class="sxs-lookup"><span data-stu-id="00c4a-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="00c4a-116">Richtlinientipps</span><span class="sxs-lookup"><span data-stu-id="00c4a-116">Policy tips</span></span>
<span data-ttu-id="00c4a-117">Im Folgenden finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für das Ausgabenmanagement unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="00c4a-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="00c4a-118">Richtlinien haben das Datum des Inkrafttretens. Eine Richtlinie wird nicht wirksam, wenn sie mit einem Datum nach dem Datum erstellt wird, an dem die Ausgaben entstanden sind.</span><span class="sxs-lookup"><span data-stu-id="00c4a-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="00c4a-119">Wenn Sie beispielsweise heute eine neue Richtlinie erstellen, um maximale Mahlzeitkosten von 50 USD durchzusetzen, werden alle ab gestern eingegebenen Ausgaben nicht mit dieser Richtlinie verglichen.</span><span class="sxs-lookup"><span data-stu-id="00c4a-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="00c4a-120">Wenn Sie eine Richtlinie für eine Ausgabenkategorie erstellen, die aufgelistet werden kann, sollten Sie eine Bedingung für den Ausgabenzeilentyp hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00c4a-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="00c4a-121">Einige Richtlinien, z. B. die Erfordernis einer Quittung, sind für Einzelposten möglicherweise nicht sinnvoll und sollten nur auf die Kopfzeile oder eine nicht Einzelpostenzeile angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="00c4a-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="00c4a-122">Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet.</span><span class="sxs-lookup"><span data-stu-id="00c4a-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="00c4a-123">Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie für die Zielentität (Kreditinstanz) ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="00c4a-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="00c4a-124">Um die Richtlinien für die Zielentität auszuführen, aktivieren Sie die Funktion „Bewerten Sie die Ausgabenpolitik gegen die Aufnahme einer juristischen Person“ im Arbeitsbereich **Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="00c4a-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="00c4a-125">Wann müssen die Richtlinien bewertet werden</span><span class="sxs-lookup"><span data-stu-id="00c4a-125">When to evaluate policies</span></span>

<span data-ttu-id="00c4a-126">In den Ausgabenverwaltungsparametern können Sie auswählen, ob die Ausgabenverwaltungsrichtlinien ausgewertet werden sollen, wenn eine Zeile gespeichert wird oder wenn eine Spesenabrechnung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="00c4a-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="00c4a-127">Wenn Sie auswerten, wann eine Zeile gespeichert wird, stellt dies sicher, dass Benutzer früher einen Überblick darüber erhalten, was sie tun müssen, um ihre Spesenabrechnung auf einmal zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="00c4a-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="00c4a-128">Andernfalls können Sie die Richtlinienbewertung verzögern und Zeit sparen, wenn am Ende während der Übermittlung an den Workflow eine Überprüfung ansteht.</span><span class="sxs-lookup"><span data-stu-id="00c4a-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]