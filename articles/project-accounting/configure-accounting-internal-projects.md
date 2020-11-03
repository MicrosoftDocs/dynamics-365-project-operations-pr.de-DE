---
title: Buchhaltung für interne Projekte konfigurieren
description: Dieses Thema enthält Informationen zum Einrichten von Buchhaltungspraktiken für interne Projekte in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076458"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="75c86-103">Buchhaltung für interne Projekte konfigurieren</span><span class="sxs-lookup"><span data-stu-id="75c86-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="75c86-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="75c86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="75c86-105">Interne Projekte ermöglichen es Unternehmen, Kosten im Zusammenhang mit Aktivitäten zu verfolgen, die keinem Kunden in Rechnung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="75c86-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="75c86-106">Beispiele für interne Projekte sind:</span><span class="sxs-lookup"><span data-stu-id="75c86-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="75c86-107">Entwicklung eines Produkts, z. B. einer mobilen App, und Verfolgung der mit der Entwicklung verbundenen Kosten</span><span class="sxs-lookup"><span data-stu-id="75c86-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="75c86-108">Verwalten von Zeit und Ausgaben vor dem Verkauf</span><span class="sxs-lookup"><span data-stu-id="75c86-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="75c86-109">Dieses interne Vorverkaufsprojekt kann später in ein fakturierbares Projekt umgewandelt werden, wenn das Angebot gewonnen wird.</span><span class="sxs-lookup"><span data-stu-id="75c86-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="75c86-110">Jedes Projekt, das in Dynamics 365 Project Operations keinem Vertrag zugeordnet ist, wird als intern behandelt.</span><span class="sxs-lookup"><span data-stu-id="75c86-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="75c86-111">Projektkosten und Umsatzprofile werden nicht dazu verwendet, Buchhaltungsregeln für das Projekt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="75c86-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="75c86-112">Interne Projektkosten werden immer nach Gewinn- und Verlustprinzipien gebucht.</span><span class="sxs-lookup"><span data-stu-id="75c86-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="75c86-113">Sachkonten für Buchungen werden auf der Seite **Sachkontobuchungseinstellungen** definiert.</span><span class="sxs-lookup"><span data-stu-id="75c86-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="75c86-114">Zeittransaktionen werden durch Belastung des Kontos **Kosten** und Gutschriften für das Konto **Lohnzuweisung** gebucht.</span><span class="sxs-lookup"><span data-stu-id="75c86-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="75c86-115">Ausgabentransaktionen werden durch Belastung des Kontos **Kosten** und Gutschriften für das Konto **Gegenkonto für Ausgaben** gebucht.</span><span class="sxs-lookup"><span data-stu-id="75c86-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="75c86-116">Nachdem Transaktionen in das Projekt gebucht wurden und das Projekt einem Projektvertrag zugeordnet ist, storniert das System alle kumulierten Transaktionen und erstellt neue fakturierbare Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="75c86-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="75c86-117">Die fakturierbaren Transaktionen folgen den Buchhaltungsregeln, die im jeweiligen Projektkosten- und Ertragsprofil definiert sind.</span><span class="sxs-lookup"><span data-stu-id="75c86-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


