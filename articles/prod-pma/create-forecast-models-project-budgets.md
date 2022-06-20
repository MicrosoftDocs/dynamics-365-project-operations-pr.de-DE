---
title: Prognosemodelle für Projektbudgets erstellen
description: Dieser Artikel beschreibt, wie Sie ein Planungsmodell für Restbudgets erstellen können.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916701"
---
# <a name="create-forecast-models-for-project-budgets"></a>Prognosemodelle für Projektbudgets erstellen 

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie ein Planungsmodell für Restbudgets erstellen können. Ein Projekt, das der Budgetkontrolle unterliegt, verwendet zwei Arten von Budgets: ursprünglich und verbleibend. Wenn Sie ein Projektbudget erstellen, müssen Sie die ursprünglichen und verbleibenden Budgetprognosemodelle angeben, die auf der Seite **Prognosemodelle** erstellt wurden. Projektbudgets, die auf den angegebenen Modellen basieren, werden erstellt, wenn Sie das Projektbudget festlegen.

> [!NOTE]
> Ein Prognosemodell, das für die Budgetkontrolle verwendet wird, kann kein Untermodell haben oder als Untermodell verwendet werden.

1. Wählen Sie **Projektmanagement und -buchhaltung** > **Einrichtung** > **Prognosen**  > **Prognosemodelle** aus.
2. Wählen Sie **Neu** aus, um ein neues Prognosemodell zu erstellen, und geben Sie dann eine Modell-ID-Nummer und einen Namen für das neue Modell ein. 
3. Legen Sie die Option **Angehalten** auf **Ja** fest, um Änderungen an den Prognosezeilen für das Prognosemodell zu verhindern. 
4. Wenn die Prognosezeilen, mit denen das Modell verknüpft ist, Cashflow-Prognosen in der Finanzbuchhaltung generieren sollen, legen Sie **In Cashflowplanungen einbeziehen** auf **Ja** fest. 
5. Um das Projektdatum als Rechnungsdatum zu verwenden, legen Sie **Datum der Planungsrechnung** auf **Ja** fest. 
6. Wählen Sie im Feld **Budgettyp** eines der folgenden Modelltypen aus:

   - **Ursprüngliches Budget**: Verwenden Sie die ursprünglichen Budgetbeträge, die bei der Erstellung und Genehmigung des ursprünglichen Budgets festgelegt wurden.
   - **Übriges Budget**: Verwenden Sie die verbleibenden Budgetbeträge während der Laufzeit des Projekts. Die Salden in diesem Prognosemodell werden durch tatsächliche Transaktionen reduziert und durch Budgetüberarbeitungen erhöht oder verringert.
   - **Vortrag**: Verwenden Sie die Vortragsbudgetbeträge für das Projekt. Ein Vortrag ist ein optionaler Prozess, der ausgeführt werden kann, um nicht verwendete Budgetbeträge von einem Geschäftsjahr in ein anderes zu übertragen.

7. Legen Sie bei Bedarf die folgenden Optionen fest:

   - Aktivieren Sie **Datum der Planungsrechnung**, um das Projektdatum als Rechnungsdatum zu verwenden.
   - Aktivieren Sie **Planung mit WIP**, um basierend auf WIP zu prognostizieren. Wählen Sie dann die Art der WIP aus. 
   - Sie können die Standardeinstellung für **Budgettyp** als **Keiner** beibehalten, oder einen neuen Typ eingeben. Der Budgettyp kann nicht geändert werden, nachdem Sie einen Datensatz geändert haben.     
    > [!NOTE]
    > Wenn Sie den Standardbudgettyp ändern, stehen alle anderen Optionen nicht mehr für Aktualisierungen zur Verfügung, und Sie können dieses Prognosemodell nicht wiederverwenden. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]