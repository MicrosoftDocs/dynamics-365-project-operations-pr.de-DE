---
title: Kaufen von nicht vorrätigen Materialien mithilfe einer ausstehenden Lieferantenrechnung
description: In diesem Thema wird erläutert, wie ausstehende Lieferantenrechnungen erfasst werden.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993791"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="52b8a-103">Kaufen von nicht vorrätigen Materialien mithilfe einer ausstehenden Lieferantenrechnung</span><span class="sxs-lookup"><span data-stu-id="52b8a-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="52b8a-104">_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_</span><span class="sxs-lookup"><span data-stu-id="52b8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="52b8a-105">Wenn ein Unternehmen nicht vorrätige Materialien für ein Projekt beschafft, können die Kosten sofort gegen das Projekt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="52b8a-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="52b8a-106">Beispielsweise führt Contoso Robotics US ein Projekt zur Erneuerung der Ausrüstung durch und benötigt Softwarelizenzen.</span><span class="sxs-lookup"><span data-stu-id="52b8a-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="52b8a-107">Diese Lizenzen werden von einem Drittanbieter bezogen.</span><span class="sxs-lookup"><span data-stu-id="52b8a-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="52b8a-108">Mithilfe von Dynamics 365 Finance zeichnet der Kreditorenbuchhalter einen ausstehenden Lieferantenrechnungsbeleg auf und ordnet die Lizenzkosten direkt dem Projekt zur Geräteerneuerung zu.</span><span class="sxs-lookup"><span data-stu-id="52b8a-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="52b8a-109">Bevor Sie die in diesem Thema beschriebenen Funktionen verwenden, überprüfen Sie die erforderlichen Konfigurationen und wenden Sie sie an.</span><span class="sxs-lookup"><span data-stu-id="52b8a-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="52b8a-110">Weitere Informationen finden Sie unter [Aktivieren von nicht vorrätigen Materialien und ausstehenden Lieferantenrechnungen](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="52b8a-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="52b8a-111">Buchen Sie eine projektbezogene ausstehende Lieferantenrechnung</span><span class="sxs-lookup"><span data-stu-id="52b8a-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="52b8a-112">Ausstehende Lieferantenrechnungen können auf der Seite **Ausstehende Lieferantenrechnungen** (**Kreditoren** > **Rechnungen** > **Ausstehende Lieferantenrechnungen**) erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="52b8a-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="52b8a-113">Führen Sie die folgenden Schritte aus, um eine projektbezogene ausstehende Lieferantenrechnung zu buchen:</span><span class="sxs-lookup"><span data-stu-id="52b8a-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="52b8a-114">Gehen Sie zu **Kreditoren** > **Rechnungen** und wählen Sie **Neu**.</span><span class="sxs-lookup"><span data-stu-id="52b8a-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="52b8a-115">Wählen Sie im Feld **Rechnungskonto** einen Lieferanten aus und geben Sie im Feld **Nummer** die Lieferantenrechnungskennung ein.</span><span class="sxs-lookup"><span data-stu-id="52b8a-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="52b8a-116">Fügen Sie der Lieferantenrechnung eine Zeile hinzu und wählen Sie im Feld **Artikelnummer** den nicht vorrätigen Artikel aus, den Sie beim Lieferanten gekauft haben.</span><span class="sxs-lookup"><span data-stu-id="52b8a-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="52b8a-117">Lieferantenrechnungsposten, die auf einer Beschaffungskategorie basieren, können nicht für das Projekt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="52b8a-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="52b8a-118">Fügen Sie die gekaufte Menge hinzu.</span><span class="sxs-lookup"><span data-stu-id="52b8a-118">Add the quantity purchased.</span></span> <span data-ttu-id="52b8a-119">Das System füllt den Stückpreis basierend auf der nicht vorrätigen Artikelpreiskonfiguration auf.</span><span class="sxs-lookup"><span data-stu-id="52b8a-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="52b8a-120">Überprüfen Sie den Gesamtbetrag und andere erforderliche Details in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="52b8a-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="52b8a-121">Wählen Sie in den Zeilendetails, auf der Registerkarte **Projekt** die ID des Projekts aus, in dem dieses Element aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="52b8a-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="52b8a-122">Wählen Sie optional die Aktivitätsnummer aus und aktualisieren Sie die Projektkategorie und die Zeileneigenschaft.</span><span class="sxs-lookup"><span data-stu-id="52b8a-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="52b8a-123">Ausstehende Kreditorenrechnung buchen</span><span class="sxs-lookup"><span data-stu-id="52b8a-123">Post pending vendor invoice.</span></span> <span data-ttu-id="52b8a-124">Wenn die Rechnung gebucht wird, zeichnet das System Folgendes auf:</span><span class="sxs-lookup"><span data-stu-id="52b8a-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="52b8a-125">Saldobetrag des Lieferanten.</span><span class="sxs-lookup"><span data-stu-id="52b8a-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="52b8a-126">Der Umsatzsteuerbetrag</span><span class="sxs-lookup"><span data-stu-id="52b8a-126">The sales tax amount.</span></span>
    - <span data-ttu-id="52b8a-127">Die Kosten für das Projekt werden auf dem Konto für die Beschaffungsintegration erfasst.</span><span class="sxs-lookup"><span data-stu-id="52b8a-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="52b8a-128">Die tatsächliche Projekttransaktion in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="52b8a-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="52b8a-129">Diese Transaktion wird mithilfe des  [Project Operations-Integrationsjournals](../project-accounting/project-operations-integration-journal.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="52b8a-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="52b8a-130">Durch das Buchen dieses Journals wird der Betrag vom Beschaffungsintegrationskonto auf das Projektkostenkonto verschoben.</span><span class="sxs-lookup"><span data-stu-id="52b8a-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
