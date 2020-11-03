---
title: Warum kann ich keine Datensätze aus der Ist-Werte-Entität löschen?
description: In diesem Thema erfahren Sie, warum Sie keine Datensätze aus der Ist-Werte-Entität löschen können.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076650"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Warum kann ich keine Datensätze aus der Ist-Werte-Entität löschen?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) können Sie Ist-Werte nicht löschen, da sie als Wahrheitsquelle für Transaktionen dienen, die finanzielle Auswirkungen auf nachgelagerte Systeme haben, z. B. das Sachkonto. Wenn Ist-Werte gelöscht werden könnten, könnte die Integrität der Finanzberichterstattungstransaktionen in Frage gestellt werden. Um einen Audit-Trail einzurichten, sollten Kunden Journale verwenden, um Ausgleichstransaktionen zu erstellen.

