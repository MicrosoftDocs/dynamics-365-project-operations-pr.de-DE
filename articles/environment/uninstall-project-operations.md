---
title: Deinstallieren von Dynamics 365 Project Operations
description: Dieser Artikel informiert Sie darüber, wie Sie Dynamics 365 Project Operations deinstallieren können.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911963"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Deinstallieren von Dynamics 365 Project Operations 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Um Dynamics 365 Project Operations zu deinstallieren, muss Ihnen die Rolle „Administrator“ zugewiesen sein.

1. Gehen Sie zu **Einstellungen** > **Lösungen**.

    ![Einstellungsseite.](./media/uninstall-proj-ops-solutions.png)
  
2. Entfernen Sie die Lösungen in der genauen Reihenfolge, in der sie in der folgenden Tabelle aufgeführt sind. 

    | Schritt | Lösungsname                                    | Notiz                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 2 | ProjectOperations_Anchor                           | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 5 | ProjectService                                     | Keine weiteren Hinweise.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Keine weiteren Hinweise.                                                                         |
    | 7 | ProjectServiceCore                                 | Keine weiteren Hinweise.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 9 | FieldServiceCommon                                 | Erforderlich für duales Schreiben mit Dynamics 365 Finance oder Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Erforderlich für duales Schreiben mit Dynamics 365 Finance oder Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Erforderlich für Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 19 | Dynamics365Notes                                   | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 21 | DualWriteCore                                      | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 23 | Dynamics365AssetManagement                         | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 26 | HCMCommon                                          | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 28 | Partei                                              | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 29 | Dynamics365Company                                 | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 30 | CurrencyExchangeRates                              | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
    | 31 | AssetCommon                                        | Wenn die Lösung nicht gefunden wird, überspringen Sie diese Lösung.                                                            |
