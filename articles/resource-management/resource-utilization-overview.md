---
title: Ressourcennutzung – Übersicht
description: Dieses Thema enthält Informationen zur Ressourcennutzung in Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000795"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="a1e4e-103">Ressourcennutzung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a1e4e-103">Resource utilization overview</span></span>

<span data-ttu-id="a1e4e-104">_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_</span><span class="sxs-lookup"><span data-stu-id="a1e4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1e4e-105">Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a1e4e-106">Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a1e4e-107">Die Berechnung der Nutzung basiert auf den tatsächlichen Stunden, die Ressourcen in ihren genehmigten Zeiteinträgen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a1e4e-108">Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:</span><span class="sxs-lookup"><span data-stu-id="a1e4e-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="a1e4e-109">Fakturierbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="a1e4e-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="a1e4e-110">Nicht fakturierbare Nutzung = Tatsächliche Zeit mit Fakturierungstyp-ID = Nicht fakturierbar, komplementär oder nicht verfügbar ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="a1e4e-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="a1e4e-111">Intern = Tatsächliche Zeit ohne Kaufvertrag ÷ Ressourcenkapazität</span><span class="sxs-lookup"><span data-stu-id="a1e4e-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="a1e4e-112">Ressourcenkapazität = Ressourcenarbeitsstunden – Abwesend – Arbeitsfreie Tage</span><span class="sxs-lookup"><span data-stu-id="a1e4e-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a1e4e-113">Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="a1e4e-114">Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a1e4e-115">Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:</span><span class="sxs-lookup"><span data-stu-id="a1e4e-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="a1e4e-116">**Grün**: Verrechenbare Nutzung >= Ressourcen-Zielnutzung</span><span class="sxs-lookup"><span data-stu-id="a1e4e-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="a1e4e-117">**Gelb**: Zielnutzung – 20 <= Verrechenbare Nutzung < Zielnutzung</span><span class="sxs-lookup"><span data-stu-id="a1e4e-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="a1e4e-118">**Rot**: Verrechenbare Nutzung < Zielnutzung – 20</span><span class="sxs-lookup"><span data-stu-id="a1e4e-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="a1e4e-119">Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a1e4e-120">Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a1e4e-121">Navigieren Sie hierfür zu **Ressourcen** > **Ressourcenrollen**.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="a1e4e-122">Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a1e4e-123">Navigieren Sie zu **Ressourcen** > **Ressourcen**.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="a1e4e-124">Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="a1e4e-125">Sie können zusätzliche Rollen hinzufügen, für die **Ist Standard** = **Nein** gilt.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="a1e4e-126">Die Rolle mit **Ist Standard** = **Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="a1e4e-127">Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a1e4e-128">Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a1e4e-129">Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.</span><span class="sxs-lookup"><span data-stu-id="a1e4e-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]