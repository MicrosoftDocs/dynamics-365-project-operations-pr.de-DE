---
title: Fähigkeiten und Kompetenzstufen definieren
description: Dieses Thema enthält Informationen zur Einrichtung der Fähigkeiten und Kompetenzstufenmodelle, um Ressourcen zu bewerten.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076468"
---
# <a name="define-skills-and-proficiencies"></a>Fähigkeiten und Kompetenzstufen definieren

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Fähigkeiten sind Ressourceneigenschaften, die zwischen Dynamics 365 Project Operations und, sofern installiert, Dynamics 365 Field Service gemeinsam genutzt werden. 

- Um das Repository in Project Operations beizubehalten, navigieren Sie zu **Ressourcen** \> **Ressourcenqualifikationen**. 

## <a name="use-proficiency-models-to-rate-resources"></a>Kompetenzstufenmodelle zur Bewertung von Ressourcen verwenden

Fähigkeiten für Ressourcen werden durch Kompetenzstufenmodelle bewertet. Die einzelnen Bewertungen befinden sich in einem Kompetenzstufenmodell. 

1. Um ein Kompetenzstufenmodell zu erstellen, navigieren Sie zu **Ressourcen** \> **Kompetenzstufenmodelle** und wählen Sie dann **Neu** aus.
2. Geben Sie im neuen Bewertungsmodell den Mindestbewertungswert, dem Höchstbewertungswert und die bewertet Entität ein.
3. Im Unterraster **Bewertungswerte** können Sie die verschiedenen Bewertungswerte definieren, vom Mindest- bis zum Höchstwert.


Diese Bewertungswerte werden in den Filtern **Ressourcenanforderungen** , **Zeitplanübersicht** und **Zeitplan-Assistent** angezeigt.
