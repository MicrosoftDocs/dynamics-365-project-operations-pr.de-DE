---
title: Standardwerte für Finanzdimensionen für projektbezogene Zeiteintragungen
description: Dieses Thema bietet Informationen zur Vorgehensweise beim Anwenden von Standardwerten für Fianazdimensionen, die bei Zeiteinträgen angewendet werden.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597935"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Standardwerte für Finanzdimensionen für projektbezogene Zeiteintragungen

[!include [banner](../includes/banner.md)]

Wenn Sie Finanzdimensionen für projektbezogene Zeiteintragungen verwenden, wird der Vorgabedimensionswert in der folgenden Reihenfolge bewertet:

1. Ressource
2. Project
3. Finanzierungsquelle

Wenn beispielsweise die Vorgabedimension für eine Ressource angegeben ist, wird der Standardwert über den Standardwert angewendet, der für das Projekt angegeben ist. Dem entsprechend wird, wenn die Vorgabedimension für ein Projekt angegeben ist, der Standardwert über den Standardwert angewendet, der für die Finanzierungsquelle angegeben ist.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
