---
title: Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten
description: Dieses Thema enthält Informationen zum Aktualisieren von Plug-In-Attributen für Preisdimensionen.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147067"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="cd788-103">Plug-In-Attribute aktualisieren, damit sie neue Preisdimensionen enthalten</span><span class="sxs-lookup"><span data-stu-id="cd788-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="cd788-104">Wenn Sie die Funktionen zu Angebotserstellung und Vertragsabschluss der Project Service Automation (PSA) nicht verwenden, können Sie dieses Thema überspringen.</span><span class="sxs-lookup"><span data-stu-id="cd788-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="cd788-105">In diesem Thema wird davon ausgegangen, dass Sie die Prozeduren in den Themen [Benutzerdefinierte Felder und Entitäten erstellen](create-custom-fields-entities.md), [Benutzerdefinierte Felder zur Preiseinrichtung und zu Transaktionsentitäten hinzufügen](field-references.md) und [Benutzerdefinierte Felder als Preisdimensionen einrichten](set-up-pricing-dimensions.md) abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="cd788-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="cd788-106">Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, kehren Sie zurück und schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück.</span><span class="sxs-lookup"><span data-stu-id="cd788-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="cd788-107">Wenn ein Angebotspositionsdetail auf der Seite **Angebotsposition** für eine Projektangebotszeile erstellt wird, erstellt das System zwei Vorkalkulationspositionen im Hintergrund – eine Position für die Kostenseite der Vorkalkulation und eine für die Vertriebsseite.</span><span class="sxs-lookup"><span data-stu-id="cd788-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="cd788-108">Selbes gilt auch für Projektvertragspositionen.</span><span class="sxs-lookup"><span data-stu-id="cd788-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="cd788-109">Wenn Sie eine Änderung der Menge oder eines Felds auf der Kostenseite vornehmen, wird die Änderung auf die Vertriebsseite übertragen.</span><span class="sxs-lookup"><span data-stu-id="cd788-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="cd788-110">Dies ist möglich wegen der folgenden Plug-Ins, die nach einer Änderung der Preisdimensionen erneut registriert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cd788-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="cd788-111">PreOperationContractLineDetailUpdate – aktualisiert **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="cd788-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="cd788-112">PreOperationQuoteLineDetailUpdate – aktualisiert **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="cd788-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="cd788-113">Die folgenden Schritte führen Sie durch den Prozess der Registrierung der Plug-Ins.</span><span class="sxs-lookup"><span data-stu-id="cd788-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="cd788-114">Öffnen Sie das **PluginRegistrationTool**, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.</span><span class="sxs-lookup"><span data-stu-id="cd788-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="cd788-115">Klicken Sie auf **Suchen**, und suchen Sie nach dem Plug-In, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd788-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Screenshot der Suchstruktur](media/PRT-1.png)

3. <span data-ttu-id="cd788-117">Nachdem das Plug-In gefunden wurde, wählen Sie es aus, und klicken Sie dann auf **Hauptformular auswählen**.</span><span class="sxs-lookup"><span data-stu-id="cd788-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="cd788-118">Wählen Sie den Schritt des Plug-Ins, das aktualisiert werden soll, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="cd788-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Screenshot des Plug-Ins, das aktualisiert werden soll](media/PRT-2.png)
 
5. <span data-ttu-id="cd788-120">Klicken Sie im Updatefenster auf die Auslassungspunkte (**...**) in den Filterattributen.</span><span class="sxs-lookup"><span data-stu-id="cd788-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Screenshot der Informationen zu „Vorhandene Schrittkonfiguration aktualisieren”](media/PRT-3.png)
 
6. <span data-ttu-id="cd788-122">Aktivieren Sie die Preisattribut-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="cd788-122">Select the pricing attribute check boxes.</span></span>

 ![Screenshot, der die Kontrollkästchenauswahl für Preisattribute zeigt](media/PRT-4.png)

7. <span data-ttu-id="cd788-124">Klicken Sie auf **OK**, um die Seite zu schließen, und wählen Sie dann **Aktualisierungsschritt** aus.</span><span class="sxs-lookup"><span data-stu-id="cd788-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Screenshot, der die Schaltfläche „Aktualisierungsschritt” anzeigt](media/PRT-5.png)
 
8. <span data-ttu-id="cd788-126">Wiederholen Sie diesen Prozess für das zweite Plug-In, **PreOperationQuoteLineDetail – Update von msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="cd788-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="cd788-127">Schließen Sie das Plug-in-Registrierungstool.</span><span class="sxs-lookup"><span data-stu-id="cd788-127">Close the plug-in registration tool.</span></span>

