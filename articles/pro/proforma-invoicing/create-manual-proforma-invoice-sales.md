---
title: Eine manuelle Proforma-Rechnung erstellen – Lite
description: Dieses Thema bietet Informationen zum Erstellen einer manuellen Proforma-Rechnung in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274187"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="27fb9-103">Eine manuelle Proforma-Rechnung erstellen – Lite</span><span class="sxs-lookup"><span data-stu-id="27fb9-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="27fb9-104">_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="27fb9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27fb9-105">In Dynamics 365 Project Operations können Proforma-Rechnungen nach Bedarf manuell erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27fb9-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="27fb9-106">Sie können manuell eine Proforma-Rechnung über die Listenseite **Projektverträge** oder über die Listenseite **Projektvertrag** erstellen.</span><span class="sxs-lookup"><span data-stu-id="27fb9-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="27fb9-107">Listenseite „Projektverträge“</span><span class="sxs-lookup"><span data-stu-id="27fb9-107">Project Contracts list page</span></span>

<span data-ttu-id="27fb9-108">Wählen Sie über die Listenseite **Projektverträge** eine oder mehrere Projektverträge aus, und erstellen Sie Rechnungen für alle ausgewählten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="27fb9-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="27fb9-109">Das System prüft, um zu erkennen, welcher der ausgewählten Projektverträge einen Rückstand in **Bereit für die Rechnungsstellung** vor dem heutigen Datum aufweist.</span><span class="sxs-lookup"><span data-stu-id="27fb9-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="27fb9-110">Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen.</span><span class="sxs-lookup"><span data-stu-id="27fb9-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="27fb9-111">Wenn ein Projektvertrag mehrere Kunden hat, wird möglicherweise eine Rechnung pro Kunde und mehrere Rechnungen pro Projektvertrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="27fb9-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="27fb9-112">Alle erstellten Projektrechnungen sind auf der Seite **Rechnung** im Abschnitt **Abrechnung** des Bereichs **Umsatz** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27fb9-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="27fb9-113">Seite „Projektvertragsdetails“</span><span class="sxs-lookup"><span data-stu-id="27fb9-113">Project Contract details page</span></span>

<span data-ttu-id="27fb9-114">Eine Proforma-Rechnung kann auch aus der **Projektvertrag** Detailseite erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="27fb9-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="27fb9-115">Das System prüft, ob der Projektvertrag das Rechnungsrückstandsprotokoll **Bereit für die Rechnungsstellung** aufweist, der vor dem heutigen Datum datiert ist.</span><span class="sxs-lookup"><span data-stu-id="27fb9-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="27fb9-116">Aus diesen Verträgen erstellt das System Entwürfe von Proforma-Rechnungen basierend auf der Anzahl der Kunden in jeder Vertragszeile.</span><span class="sxs-lookup"><span data-stu-id="27fb9-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="27fb9-117">Wenn eine einzelne Proforma-Rechnung erstellt wird, wird die Seite **Rechnung** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="27fb9-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="27fb9-118">Wenn für diesen Projektvertrag mehrere Rechnungen erstellt wurden, wird die Listenseite **Rechnungen** geöffnet, um alle erstellten Rechnungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="27fb9-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]