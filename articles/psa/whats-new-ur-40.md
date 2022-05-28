---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 40, V3
description: Dieses Thema listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Update-Version 40, V3 verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588643"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 40 aufgeführt. Diese Version hat die Build-Nummer V3.10.61.61 und ist im Allgemeinen über ein Selbstupdate im Februar 2022 verfügbar.

## <a name="update-release-40"></a>Update Release 40

### <a name="features"></a>Funktionen
Phase 1 des Upgrades von Project Service Automation auf Project Operations – Lite wird im Februar 2022 für alle Kunden freigegeben. Ihre Berechtigung können Sie unter [Upgrade von Project Service Automation auf Project Operations](upgrade-project-operations-non-stocked.md) überprüfen Wenn die Anwendung in Ihrer Instanz nicht im Power Platform Admin Center angezeigt wird, wenden Sie sich an den Support und fordern Sie an, dass der Flight für Ihre Umgebungen aktiviert wird. Ihre Anfrage muss eine Liste mit Umgebungs-IDs enthalten, in denen der Flight aktiviert werden muss.

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Zeit und Ausgaben**
- Ein Notizeintrag fehlt, wenn eine Zeitbuchung abgelehnt oder storniert wird. 

**Vertrieb**

- Wenn Sie Kosten- oder Umsatzschätzungen mit vorkonfigurierten Plug-Ins aktualisieren, dürfen Sie fälschlicherweise JSON-Nutzlasten senden, die außerhalb der Benutzeroberfläche nicht gültig sind.
- Wenn Sie Angebotspositionen über die Schnellansicht aktualisieren, können Sie Angebote aktivieren.
