---
title: Homepage upgraden
description: Dieser Artikel zeigt, wo Sie wichtige Informationen über die neuen und geänderten Funktionen in Dynamics 365 Project Service Automation finden und wie Sie ein Upgrade auf die neueste Version durchführen.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
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
ms.openlocfilehash: 5dcf41af31a60b952ce82c08e3c082490d59d4f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926637"
---
# <a name="upgrade-home-page"></a>Homepage upgraden

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Upgrade von PSA-Version 2.x oder 1.x auf Version 3.x

### <a name="new-instances"></a>Neue Instanzen

Ab 17. Mai, 2019, wird bei Auswahl von Project Service Automation während der Bereitstellung einer neuen Instanz standardmäßig Version 3.x installiert.

### <a name="existing-instances"></a>Vorhandene Instanzen

Zuvor mussten Kunden, die eine Instanz von PSA Version 2.x hatten, und auf Version 3.x upgraden mussten, welche die auf dem einheitlichen Client basierte (UCI) Version von PSA war, sich an den Microsoft Support wenden und die Details ihrer Instanz angeben, damit der Support die Instanz für das Upgrade auf Version 3.x aktivieren kann. Ab dem 1. März 2020 können Kunden, die über eine Instanz von PSA Version 2.x verfügen und auf Version 3.x aktualisieren müssen, ihre Instanzen direkt über das Admin-Portal aktualisieren, ohne sich an den Microsoft-Support wenden zu müssen.  

> [!NOTE]
> PSA Version 3.x umfasst wichtige Änderungen. Sie ist in das Framework der einheitlichen Oberfläche integriert, um eine verbesserte Benutzerfreundlichkeit zu bieten. Die neu gestaltete App bietet eine durchgängige, einheitliche Benutzeroberfläche (UI) und folgt den dynamischen Designgrundsätzen für eine optimale Anzeige auf jeder Bildschirmgröße oder jedem Gerät. Es sind weitere Änderungen in der gesamten Anwendung vorgenommen worden. Einige der Bereiche, die geändert wurden, umfassen Preise, Buchung und das Zuweisen von Ressourcen, Zeit, Ausgaben und Genehmigungen.

Bevor Sie mit dem Upgradeprozess beginnen, wird empfohlen, dass Sie die folgenden Aufgaben abschließen:

- Überprüfen Sie, ob sowohl Dynamics 365 Field Service als auch Project Service Automation in der identifizierten Instanz installiert sind. Wenn beide Lösungen installiert sind, sollten Sie das Upgrade für beide Planen, bevor Sie die reguläre Verwendung der Instanz fortsetzen.
- Lesen Sie die folgenden Artikel sorgfältig durch. Kenntnis und Verstehen der Änderungen zwischen Versionen hilft Ihnen beim Upgradeprozess. Diese Artikel enthalten Informationen über die wichtigsten Änderungen in PSA sowie Überlegungen und Empfehlungen für die Planung Ihres Upgrades auf Version 3.x.

    - [Neuigkeiten und Änderungen in Project Service Automation, Version 3](whats-new-changed-v3.md)
    - [Überlegungen zum Upgrade – Project Service Automation Version 2.x oder 1.x auf Version 3](upgrade-v3.md)

- Aktualisieren Sie Ihre Sandkasteninstanz, um Änderungen in Ihrer Implementierung auszuwerten, bevor Sie Ihre Produktionsinstanz aktualisieren.

Nachdem Sie die oben genannten Artikel gelesen haben und bereit sind, auf PSA Version 3.x oder die UCI-basierte Version zu aktualisieren, senden Sie eine Anfrage an den Microsoft Support, um das Upgrade über das Admin Center bereitzustellen. Geben Sie in Ihrer Anforderung die Details Ihrer Instanz an.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Ältere Versionen von PSA (PSA Version 2.x) in einer neu erstellten Instanz

Seit dem 17. Mai 2019 haben alle neuen Instanzen UCI als Standardclient. Zur Ausrichtung an dieser Änderung werden PSA Version 3.x und Field Service 8.x standardmäßig bereitgestellt, da diese Versionen dazu entworfen wurden, mit dem UCI-Client zu funktionieren.

Ab dem 1. März 2020 können Kunden von Dynamics PSA keine neue Umgebung mehr mit älteren PSA-Versionen erstellen, z. B. PSA Version 2.x oder niedriger. In jeder neuen Umgebung wird nur Version 3.x von PSA bereitgestellt.

> [!NOTE]
> Für eine optimale Erfahrung, wenn Sie ältere Versionen von Field Service und PSA-Anwendungen verwenden, wechseln Sie zur Seite **Systemeinstellungen**, und für das Feld **Nur die neue einheitliche Oberfläche verwenden (empfohlen)** wählen Sie **Nein** aus, da diese Versionen nicht dazu entworfen sind, in UCI korrekt geladen zu werden. Nachdem Sie UCI deaktiviert haben, können Sie diese Versionen von Field Service und PSA mithilfe des alten Webclient öffnen und ausführen. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
