---
title: Sicherheit und Genehmigungen
description: Dieser Artikel enthält Informationen über die Sicherheitseinrichtung für Genehmigungen in Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709396"
---
# <a name="security-and-approvals"></a>Sicherheit und Genehmigungen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Microsoft Dynamics 365 Project Operations verwendet zwei Sicherheitsrollen, um die Genehmigung von Zeit-, Ausgaben- und Materialeinträgen zu ermöglichen:

- Projektgenehmiger
- Projektgenehmiger-Admin

## <a name="project-approver"></a>Projektgenehmiger

Sie müssen die **Projektgenehmiger**-Sicherheitsrolle haben, um Projektzeit-, Ausgaben- und Materialeinträge zu genehmigen. Sie müssen auch Zugang zu den relevanten verbundenen Unternehmen haben, wie z. B. **Projekt**. Dieser Zugriff kann von jemandem zugewiesen werden, der die **Projektmanager**-Rolle hat. Außerdem müssen Sie ein Teammitglied des Projekts und als Genehmiger gekennzeichnet sein.

Um Nicht-Projektbeiträge zu genehmigen, müssen Sie der Vorgesetzte des Einreichers sein.

## <a name="project-approver-admin"></a>Projektgenehmiger-Admin

> [!NOTE]
> Die [Genehmigungssets](approval-sets.md)-Funktion muss aktiviert werden, bevor Sie die Projektgenehmiger-Admin-Funktion verwenden können.

Die **Projektgenehmiger-Admin**-Sicherheitsrolle ermöglicht Benutzern das Umgehen von Richtlinien und die Genehmigung von Einträgen für alle Projekte. Durch die Zuweisung dieser Rolle wird die Validierungslogik umgangen, die eine Teammitgliedschaft und die Kennzeichnung als Genehmiger erfordert. Sie müssen über die Ihnen zugewiesenen Sicherheitsrollen Zugriff auf die entsprechenden Bezugstabellen haben, wie z.B. **Projekt**.

Der SYSTEM-Benutzerkontext umgeht Validierungen auf die gleiche Weise wie der Project Approver Admin Sicherheitsrolle.
