---
title: Spesenabrechnungen und mehrere Genehmiger
description: Dieses Thema enthält Informationen zu Ausgabenabrechnungen, die von mehr als einer Person genehmigt werden müssen.
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
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897090"
---
# <a name="expense-reports-and-multiple-approvers"></a>Spesenabrechnungen und mehrere Genehmiger

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine eingereichte Ausgabenabrechnung genehmigen. Wenn Sie den Workflowprozess für die Genehmigung von Ausgabenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Ausgabennabrechnungen enthalten. Beispielsweise können Sie verlangen, dass alle Ausgabenabrechnungen von zwei verschiedenen Personen genehmigt werden, dem Manager des Mitarbeiters, der den Bericht eingereicht hat, und dem Kreditorenkoordinator.

Wenn Sie mehrere Genehmiger für Ausgabenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:

- Fügen Sie ein Genehmigungselement mit einem Schritt hinzu. Für den Schritt muss beispielsweise eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt werden.
- Fügen Sie ein Genehmigungselement hinzu, die verschiedene Schritte hat. Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:

    1. Der Manager des Mitarbeiters, der die Ausgabenrechnung eingereicht hat, genehmigt sie.
    2. Der Kreditorenbuchhalter überprüft die Belege und die Ausgabenabrechnungsposten.
    3. Der Budgetinhaber genehmigt die Ausgabenabrechnung.

- Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat. Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:

    1. Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.
    2. Der Budgetinhaber genehmigt die Ausgabenabrechnung.