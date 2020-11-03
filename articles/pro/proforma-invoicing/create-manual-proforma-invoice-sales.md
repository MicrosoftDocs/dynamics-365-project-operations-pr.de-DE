---
title: Erstellen einer manuellen Proforma-Rechnung
description: Dieses Thema bietet Informationen zum Erstellen einer manuellen Proforma-Rechnung in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4076753"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="6cf8a-103">Erstellen einer manuellen Proforma-Rechnung</span><span class="sxs-lookup"><span data-stu-id="6cf8a-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="6cf8a-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="6cf8a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6cf8a-105">In Dynamics 365 Project Operations können Proforma-Rechnungen nach Bedarf manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="6cf8a-106">Sie können manuell eine Proforma-Rechnung über die Listenseite **Projektverträge** oder über die Listenseite **Projektvertrag** erstellen.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="6cf8a-107">Listenseite „Projektverträge“</span><span class="sxs-lookup"><span data-stu-id="6cf8a-107">Project Contracts list page</span></span>

<span data-ttu-id="6cf8a-108">Wählen Sie über die Listenseite **Projektverträge** eine oder mehrere Projektverträge aus, und erstellen Sie Rechnungen für alle ausgewählten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="6cf8a-109">Das System prüft, um zu erkennen, welcher der ausgewählten Projektverträge einen Rückstand in **Bereit für die Rechnungsstellung** vor dem heutigen Datum aufweist.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="6cf8a-110">Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="6cf8a-111">Wenn ein Projektvertrag mehrere Kunden hat, wird möglicherweise eine Rechnung pro Kunde und mehrere Rechnungen pro Projektvertrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="6cf8a-112">Alle erstellten Projektrechnungen sind auf der Seite **Rechnung** im Abschnitt **Abrechnung** des Bereichs **Umsatz** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="6cf8a-113">Detailseite zu Projektverträgen</span><span class="sxs-lookup"><span data-stu-id="6cf8a-113">Project Contract details page</span></span>

<span data-ttu-id="6cf8a-114">Eine Proforma-Rechnung kann auch über die Detailseite **Projektvertrag** erstellt werden, auf der die Rechnung für diesen bestimmten Projektvertrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="6cf8a-115">Das System prüft, ob der Projektvertrag einen Rückstand für **Bereit für die Rechnungsstellung** aufweist, der vor dem heutigen Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="6cf8a-116">Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen basierend auf der Anzahl der Kunden in jeder Vertragszeile.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="6cf8a-117">Wenn eine einzelne Proforma-Rechnung erstellt wird, wird die Seite **Rechnung** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="6cf8a-118">Wenn für diesen Projektvertrag mehrere Rechnungen erstellt wurden, wird die Listenseite **Rechnungen** geöffnet, um alle erstellten Rechnungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6cf8a-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
