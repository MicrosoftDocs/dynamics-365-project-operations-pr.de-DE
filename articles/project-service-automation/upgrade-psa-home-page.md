---
title: Homepage upgraden
description: In diesem Thema wird gezeigt, wo Sie wichtige Informationen über die neuen und geänderten Funktionen in Dynamics 365 Project Service Automation finden sowie den Prozess für das Upgraden auf die neueste Version.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3722010"
---
# <a name="upgrade-home-page"></a>Homepage upgraden

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Upgrade von PSA-Version 2.x oder 1.x auf Version 3.x

### <a name="new-instances"></a>Neue Instanzen

Ab 17. Mai, 2019, wird bei Auswahl von Project Service Automation während der Bereitstellung einer neuen Instanz standardmäßig Version 3.x installiert.

### <a name="existing-instances"></a>Vorhandene Instanzen

Vorher mussten Kunden, die eine Instanz von PSA Version 2.x haben, und auf Version 3.x upgraden müssen, welche die auf dem einheitlichen Client basierte (UCI) Version von PSA ist, sich an den Microsoft Support wenden und die Details ihrer Instanz angeben, damit der Support die Instanz für das Upgrade auf Version 3.x aktivieren konnte. Ab dem 1. März 2020 können Kunden, die über eine Instanz von PSA Version 2.x verfügen und auf Version 3.x aktualisieren müssen, ihre Instanzen direkt über das Admin-Portal aktualisieren, ohne sich an den Microsoft-Support wenden zu müssen.  

> [!NOTE]
> PSA Version 3.x umfasst wichtige Änderungen. Sie ist in das Framework der einheitlichen Oberfläche integriert, um eine verbesserte Benutzerfreundlichkeit zu bieten. Die neu gestaltete App bietet eine durchgängige, einheitliche Benutzeroberfläche (UI) und folgt den dynamischen Designgrundsätzen für eine optimale Anzeige auf jeder Bildschirmgröße oder jedem Gerät. Es sind weitere Änderungen in der gesamten Anwendung vorgenommen worden. Einige der Bereiche, die geändert wurden, umfassen Preise, Buchung und das Zuweisen von Ressourcen, Zeit, Ausgaben und Genehmigungen.

Bevor Sie mit dem Upgradeprozess beginnen, wird empfohlen, dass Sie die folgenden Aufgaben abschließen:

- Überprüfen Sie, ob sowohl Dynamics 365 Field Service als auch Project Service Automation in der identifizierten Instanz installiert sind. Wenn beide Lösungen installiert sind, sollten Sie das Upgrade für beide Planen, bevor Sie die reguläre Verwendung der Instanz fortsetzen.
- Überprüfen Sie sorgfältig die folgenden Themen. Kenntnis und Verstehen der Änderungen zwischen Versionen hilft Ihnen beim Upgradeprozess. Diese Themen bieten Informationen zu den Hauptänderungen in PSA, neben Überlegungen und Empfehlungen für die Planung Ihres Upgrades auf Version 3.x.

    - [Neuigkeiten und Änderungen in Project Service Automation, Version 3](whats-new-changed-v3.md)
    - [Überlegungen zum Upgrade – Project Service Automation Version 2.x oder 1.x auf Version 3](upgrade-v3.md)

- Aktualisieren Sie Ihre Sandkasteninstanz, um Änderungen in Ihrer Implementierung auszuwerten, bevor Sie Ihre Produktionsinstanz aktualisieren.

Nachdem Sie die Themen durchgesehen haben, die zuvor erwähnt wurden und bereit sind, das Upgrade auf PSA Version 3.x oder die UCI-basierte Version durchzuführen, senden Sie eine Anforderung an den Microsoft-Support, damit dieser das Upgrade vom Admin Center aus zur Verfügung stellt. Geben Sie in Ihrer Anforderung die Details Ihrer Instanz an.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Ältere Versionen von PSA (PSA Version 2.x) in einer neu erstellten Instanz

Seit dem 17. Mai 2019 haben alle neuen Instanzen UCI als Standardclient. Zur Ausrichtung an dieser Änderung werden PSA Version 3.x und Field Service 8.x standardmäßig bereitgestellt, da diese Versionen dazu entworfen wurden, mit dem UCI-Client zu funktionieren.

Ab dem 1. März 2020 können Kunden von Dynamics PSA keine neuen Umgebungen mehr mit älteren PSA-Versionen erstellen, z. B. PSA Version 2.x oder niedriger. In jeder neuen Umgebung wird nur Version 3.x von PSA bereitgestellt.

> [!NOTE]
> Für eine optimale Erfahrung, wenn Sie ältere Versionen von Field Service und PSA-Anwendungen verwenden, wechseln Sie zur Seite **Systemeinstellungen**, und für das Feld **Nur die neue einheitliche Oberfläche verwenden (empfohlen)** wählen Sie **Nein** aus, da diese Versionen nicht dazu entworfen sind, in UCI korrekt geladen zu werden. Nachdem Sie UCI deaktiviert haben, können Sie diese Versionen von Field Service und PSA mithilfe des alten Webclient öffnen und ausführen. Anweisungen dazu, wie Sie den UCI-Client deaktivieren, finden Sie unter [Nur einheitliche Oberfläche aktivieren](../admin/enable-unified-interface-only.md).
