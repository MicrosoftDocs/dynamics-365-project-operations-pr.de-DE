---
title: Fähigkeiten und Kompetenzstufenmodelle
description: Dieses Thema enthält Informationen zur Verwendung der Fähigkeiten und Kompetenzstufenmodelle.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73509fda4a715a4131781645736e49cfb02115da2c3650c5a966e35360e7703f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990495"
---
# <a name="skills-and-proficiency-models"></a>Fähigkeiten und Kompetenzstufenmodelle

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fähigkeiten sind Ressourceneigenschaften, die von Dynamics 365 Project Service Automation und, sofern installiert, Dynamics 365 Field Service gemeinsam genutzt werden. 

Um das Repository in Project Service Automation beizubehalten, navigieren Sie zu **Ressourcen** \> **Ressourcenqualifikationen**. 

> ![Ressourcenqualifikationen.](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Kompetenzmodelle verwenden, um Ressourcen zu bewerten

Ressourcenqualifikationen sind nach Kompetenzstufenmodellen bewertet. Die einzelnen Bewertungen befinden sich in einem Kompetenzstufenmodell. 

1. Um ein Kompetenzstufenmodell zu erstellen, navigieren Sie zu **Ressourcen** \> **Kompetenzstufenmodelle** und wählen Sie dann **Neu** aus.
2. Geben Sie im neuen Bewertungsmodell den Mindestbewertungswert, dem Höchstbewertungswert und die bewertet Entität ein.
3. Im Unterraster **Bewertungswerte** können Sie die verschiedenen Bewertungswerte vom Minimum bis zum Maximum festlegen.

> ![Definierte Mindest- und Höchstbewertungswerte.](media/Resource-Management-image85.png)

Diese Bewertungswerte werden in den Filtern **Ressourcenanforderungen**, **Zeitplanübersicht** und **Zeitplan-Assistent** angezeigt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]