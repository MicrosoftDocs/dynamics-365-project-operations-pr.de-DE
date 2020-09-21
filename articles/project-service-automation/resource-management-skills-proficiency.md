---
title: Fähigkeiten und Kompetenzstufenmodelle
description: Dieses Thema enthält Informationen zur Verwendung der Fähigkeiten und Kompetenzstufenmodelle.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722049"
---
# <a name="skills-and-proficiency-models"></a>Fähigkeiten und Kompetenzstufenmodelle

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fähigkeiten sind Ressourceneigenschaften, die von Dynamics 365 Project Service Automation und, sofern installiert, Dynamics 365 Field Service gemeinsam genutzt werden. 

Um das Repository in Project Service Automation beizubehalten, navigieren Sie zu **Ressourcen** \> **Ressourcenqualifikationen**. 

> ![Ressourcenqualifikationen](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Kompetenzstufenmodelle zur Bewertung von Ressourcen verwenden

Fähigkeiten für Ressourcen werden durch Kompetenzstufenmodelle bewertet. Die einzelnen Bewertungen befinden sich in einem Kompetenzstufenmodell. 

1. Um ein Kompetenzstufenmodell zu erstellen, navigieren Sie zu **Ressourcen** \> **Kompetenzstufenmodelle** und wählen Sie dann **Neu** aus.
2. Geben Sie im neuen Bewertungsmodell den Mindestbewertungswert, dem Höchstbewertungswert und die bewertet Entität ein.
3. Im Unterraster **Bewertungswerte** können Sie die verschiedenen Bewertungswerte definieren, vom Mindest- bis zum Höchstwert.

> ![Definierte Mindest- und Höchstbewertungswerte](media/Resource-Management-image85.png)

Diese Bewertungswerte werden in den Filtern **Ressourcenanforderungen**, **Zeitplanübersicht** und **Zeitplan-Assistent** angezeigt.
