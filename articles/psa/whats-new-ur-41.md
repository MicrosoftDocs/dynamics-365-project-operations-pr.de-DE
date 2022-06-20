---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 41, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 41, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930547"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 41, V3 neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V3.10.62.162 und ist durch eine Selbstaktualisierung im März 2022 verfügbar.

## <a name="update-release-41"></a>Update Release 41

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Projektmanagement**
- Wenn Sie versuchen, ein Projekt aus einer Vorlage zu erstellen, die auf einem mit dem Desktop-Add-In erstellten Projekt basiert, wird die folgende Fehlermeldung angezeigt: „Überprüfung des Feldes „Geplante Arbeit“ der Ressourcenzuweisung: Das Enddatum jedes Zeitsegments der Ressourcenzuweisung darf nicht vor dem Startdatum liegen".

**Zeit und Ausgaben**
- Wenn Sie versuchen, einen Zeiteintrag zu löschen, wird die folgende Fehlermeldung angezeigt: „Unerwarteter Fehler im ISV-Code“.

**Vertrieb**
- Wenn Sie eine Rechnung für einen Festpreis-Meilenstein erstellen, werden die Felder **Beschreibung** und **Externe Beschreibung** nicht ausgefüllt. 
