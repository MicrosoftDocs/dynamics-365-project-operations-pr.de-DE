---
title: Pro Tag
description: Dieses Thema enthält Informationen zu den Tagessatzregeln, die in der Ausgabenverwaltung verwendet werden.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128507"
---
# <a name="per-diems"></a><span data-ttu-id="c556e-103">Pro Tag</span><span class="sxs-lookup"><span data-stu-id="c556e-103">Per diems</span></span>

<span data-ttu-id="c556e-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="c556e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="c556e-105">Ein Tagessatz ist eine Zulage, die an einen Arbeitnehmer gezahlt wird, der zur Arbeit reist.</span><span class="sxs-lookup"><span data-stu-id="c556e-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="c556e-106">In der Ausgabenverwaltung können Sie Tagessatzregeln für verschiedene Reisesituationen erstellen.</span><span class="sxs-lookup"><span data-stu-id="c556e-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="c556e-107">Die Tagessätze können auf der Jahreszeit, dem Reiseort oder beiden basieren.</span><span class="sxs-lookup"><span data-stu-id="c556e-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="c556e-108">Wenn Sie eine Tagessatzregel erstellen, können Sie festlegen, dass ein Prozentsatz des Tagessatzes einbehalten wird, wenn ein Mitarbeiter kostenlose Mahlzeiten oder Dienstleistungen erhält.</span><span class="sxs-lookup"><span data-stu-id="c556e-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="c556e-109">Sie können auch eine minimale und maximale Anzahl von Stunden festlegen, für die der Tagessatz für die Reise eines Arbeitnehmers gelten kann.</span><span class="sxs-lookup"><span data-stu-id="c556e-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="c556e-110">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c556e-110">Configuration</span></span> 

1. <span data-ttu-id="c556e-111">Um Tagessätze hinzuzufügen, gehen Sie zu **Einrichten** > **Berechnungen und Codes** > **Tagessatz (Lagerplätze)**.</span><span class="sxs-lookup"><span data-stu-id="c556e-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="c556e-112">Wählen Sie für jeden der oben hinzugefügten Standorte einen Tagessatz und eine Währung aus, die zwischen einem bestimmten Start- und Enddatum für Hotel, Mahlzeiten und andere Ausgaben gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c556e-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="c556e-113">Tagessätze und Währungen werden unter **Einrichten** > **Berechnungen und Codes** > **Tagessätze** konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c556e-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="c556e-114">Konfigurieren Sie auf der Seite **Tagessatz (Lagerplätze)** die Tagessatzstufen.</span><span class="sxs-lookup"><span data-stu-id="c556e-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="c556e-115">Mit den Tagessatzstufen können Sie die prozentuale Aufteilung eines Tagegelds für Hotel-, Verpflegungs- und andere Ausgaben festlegen.</span><span class="sxs-lookup"><span data-stu-id="c556e-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="c556e-116">Um die prozentuale Aufteilung der Mahlzeit für Frühstück, Mittag- oder Abendessen festzulegen, aktualisieren Sie die Felder auf der Seite **Ausgabenverwaltungsparameter** auf der Registerkarte **Pro Tag**.</span><span class="sxs-lookup"><span data-stu-id="c556e-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="c556e-117">Ausgaben mit „Pro Tag“ einreichen</span><span class="sxs-lookup"><span data-stu-id="c556e-117">Submit expenses using per diem</span></span>
<span data-ttu-id="c556e-118">Um Ausgaben mit Tagessätzen einzureichen, verwenden Sie die Ausgabenkategorie **Pro Tag**, wenn Sie eine Spesenabrechnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="c556e-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="c556e-119">Geben Sie **Tagessatz von Datum**, **Tagessatz bis Datum** und **Tagessatz (Lagerplätze)** ein.</span><span class="sxs-lookup"><span data-stu-id="c556e-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="c556e-120">Der Betrag wird basierend auf den Tagessätzen für den ausgewählten Standort berechnet, und die Reduzierung der Mahlzeiten wird basierend auf den Tagessätzen berechnet.</span><span class="sxs-lookup"><span data-stu-id="c556e-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
