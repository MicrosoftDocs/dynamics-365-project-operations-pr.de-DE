---
title: Mehrere genehmigende Personen in einer Spesenabrechnunng
description: Dieses Thema enthält Informationen zu Spesenabrechnungen, die von mehreren Personen genehmigt werden müssen.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076680"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Mehrere genehmigende Personen in einer Spesenabrechnunng

[!include [banner](../includes/banner.md)]

Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine Spesenabrechnung genehmigen, die von einem Mitarbeiter eingereicht wurde. Wenn Sie den Workflowprozess für die Genehmigung von Ausgabenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Ausgabennabrechnungen enthalten. Beispielsweise können Sie verlangen, dass alle Spesenabrechnungen zunächst vom Manager des Mitarbeiters genehmigt werde müssen, der die Abrechnung eingereicht hat, und dann vom Kreditorenkoordinator.

Wenn Sie mehrere Genehmiger für Ausgabenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:

- Fügen Sie ein Genehmigungselement mit einem Schritt hinzu. Für den Schritt muss beispielsweise eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt werden.
- Fügen Sie ein Genehmigungselement hinzu, die verschiedene Schritte hat. Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:

    1. Der Manager des Mitarbeiters, der die Ausgabenrechnung eingereicht hat, genehmigt sie.
    2. Der Kreditorenbuchhalter überprüft die Belege und die Ausgabenabrechnungsposten.
    3. Der Budgetinhaber genehmigt die Ausgabenabrechnung.

- Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat. Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:

    1. Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.
    2. Der Budgetinhaber genehmigt die Ausgabenabrechnung.
