---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 40, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 40, V3, zur Verfügung stehen.
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912791"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 40, V3 neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.61.61 und ist im Allgemeinen über ein Selbstupdate im Februar 2022 verfügbar.

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
