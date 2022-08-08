---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 45, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 45, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169155"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 45, V3 neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.76.168 und ist allgemein über ein Self-Update im Juli 2022 verfügbar.

## <a name="update-release-45"></a>Update Release 45

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Vertrieb**

- Benutzer können keine Rechnungen erstellen, nachdem sie versucht haben, eine Rechnung ohne nicht fakturierte Verkäufe zu erstellen, wenn sie auch dieselbe Instanz der Seite anzeigen und sie nicht aktualisieren.

**Zeit und Ausgaben**

- Wenn „Moderne Genehmigungen” aktiviert sind und eine zurückgerufene Projektgenehmigung genehmigt wird, wird die Datensatzphase fälschlicherweise auf **Rückrufanforderung genehmigt** aktualisiert.
- Wenn „Moderne Genehmigungen” aktiviert und Cloud Flows inaktiv ist, ist der Genehmigungsprozess nicht erfolgreich und die einreichenden oder genehmigenden Benutzer werden nicht benachrichtigt.
