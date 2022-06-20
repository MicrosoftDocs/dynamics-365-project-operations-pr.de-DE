---
title: Standardwerte für Finanzdimensionen für projektbezogene Zeiteintragungen
description: Dieser Artikel informiert Sie darüber, wie standardmäßige finanzielle Dimensionen auf Zeiteinträge angewendet werden.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916563"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Standardwerte für Finanzdimensionen für projektbezogene Zeiteintragungen

[!include [banner](../includes/banner.md)]

Wenn Sie Finanzdimensionen für projektbezogene Zeiteintragungen verwenden, wird der Vorgabedimensionswert in der folgenden Reihenfolge bewertet:

1. Ressource
2. Project
3. Finanzierungsquelle

Wenn beispielsweise die Vorgabedimension für eine Ressource angegeben ist, wird der Standardwert über den Standardwert angewendet, der für das Projekt angegeben ist. Dem entsprechend wird, wenn die Vorgabedimension für ein Projekt angegeben ist, der Standardwert über den Standardwert angewendet, der für die Finanzierungsquelle angegeben ist.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
