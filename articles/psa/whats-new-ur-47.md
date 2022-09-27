---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 47, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 47, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477232"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 47, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 45, V3 neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.78.8 und ist allgemein über ein Self-Update im Juli 2022 verfügbar.

## <a name="update-release-47"></a>Update Release 47

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Ressourcenverwaltung**
- Eine Validierung wurde aktualisiert, um sicherzustellen, dass Benutzer keine Nullreferenz-Ausnahme auslösen können, wenn sie versuchen, ein Projektteammitglied ohne eine **Buchbare Ressource** zu erstellen.
