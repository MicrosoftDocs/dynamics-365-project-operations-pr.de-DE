---
title: Spesenabrechnungen und mehrere Genehmiger
description: Dieses Thema enthält Informationen zu Ausgabenabrechnungen, die von mehr als einer Person genehmigt werden müssen.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2acae2d518a02539f01d5498450236999fe609d1e8f26b5f90e18b986b83cab1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988425"
---
# <a name="expense-reports-and-multiple-approvers"></a>Spesenabrechnungen und mehrere Genehmiger

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Abhängig von den Richtlinien zur Ausgabengenehmigung Ihres Unternehmens muss möglicherweise mehr als eine Person eine eingereichte Ausgabenabrechnung genehmigen. Wenn Sie den Workflowprozess für die Genehmigung von Spesenabrechnungen einrichten, können Sie Workflowelemente hinzufügen, die Aufgaben oder Schritte für einen oder mehrere Genehmiger von Spesenabrechnungen enthalten. Beispielsweise können Sie verlangen, dass alle Spesenabrechnungen von zwei verschiedenen Personen genehmigt werden, dem Manager des Mitarbeiters, der den Bericht eingereicht hat, und dem Kreditorenkontenkoordinator.

Wenn Sie mehrere Genehmiger für Spesenabrechnungen benötigen, können Sie die Workflowelemente auf eine der folgenden Arten hinzufügen:

- Fügen Sie ein Genehmigungselement mit einem Schritt hinzu. Für den Schritt kann beispielsweise erforderlich sein, dass eine Spesenabrechnung einer Benutzergruppe zugewiesen und von 50 Prozent der Mitglieder der Benutzergruppe genehmigt wird.
- Fügen Sie ein Genehmigungselement mit mehreren Schritten hinzu. Das Genehmigungselement kann beispielsweise die folgenden Schritte ausführen:

    1. Der Manager des Mitarbeiters, der die Spesenabrechnung eingereicht hat, genehmigt sie.
    2. Der Kreditorenbuchhalter überprüft die Belege und die Spesenabrechnungsposten.
    3. Der Budgetbesitzer genehmigt die Spesenabrechnung.

- Fügen Sie mehrere Genehmigungselemente hinzu, von denen jedes einen Schritt hat. Beispielsweise können Sie für jeden der folgenden Schritte ein separates Genehmigungselement hinzufügen:

    1. Der Manager des Mitarbeiters genehmigt die Ausgabenabrechnung.
    2. Der Budgetinhaber genehmigt die Ausgabenabrechnung.


[!INCLUDE[footer-include](../includes/footer-banner.md)]