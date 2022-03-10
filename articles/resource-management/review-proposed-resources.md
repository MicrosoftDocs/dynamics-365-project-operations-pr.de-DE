---
title: Vorgeschlagene Ressourcen überprüfen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403794"
---
# <a name="review-proposed-resources"></a>Vorgeschlagene Ressourcen überprüfen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ressourcenmanager können dem Projektmanager eine Ressource vorschlagen, indem sie eine Ressourcenanforderung verwenden.

Führen Sie die folgenden Schritte aus, um vorgeschlagene Ressourcen zu überprüfen:

1. Wählen Sie im Raster **Anfragen** oder in der Anfrage selbst **Ressourcen suchen** aus.
2. Wählen Sie auf der **Zeitplan-Assistent**-Seite die Ressource aus und bestätigen Sie dann, dass alle vorgeschlagenen Stunden in der vorgeschlagenen Buchung enthalten sind.
3. Stellen Sie im **Ressourcenbuchung erstellen**-Bereich das **Buchungsstatus**-Feld auf **Vorgeschlagen** und wählen Sie dann **Buchen**.

    > [!NOTE]
    > Das Einstellen des **Buchungsstatus** auf **Vorgeschlagen** bucht die Ressource nicht fest und ersetzt die generische Ressource nicht durch das genannte Teammitglied.

    Die folgenden Statusaktualisierungen finden statt:

    - Auf der Seite **Planungsassistent** werden die Statusanzeigen aktualisiert, um anzuzeigen, dass die Buchung vorgeschlagen (nicht fest gebucht) ist.
    - In der Ressourcenanforderung wird der Status auf **Überprüfung erforderlich** geändert.
    - Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** des generischen Teammitglieds auf **Überprüfung erforderlich** geändert.

Der Projektmanager kann den Vorschlag annehmen oder ablehnen.

Wenn Ressourcenmanager Ressourcenanfragen bearbeiten, können sie einen der folgenden Ansätze verwenden:

- Mehrere Ressourcen vorschlagen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die geforderten Stunden zu erfüllen. Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind. In diesem Szenario können sich die Stunden nicht überschneiden.
- Schlagen Sie weniger Ressourcen als erforderlich vor. In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die der Anfragende angegeben hat. Wenn der Anfragende die vorgeschlagenen Ressourcen akzeptiert, wird eine nicht erfüllte Ressourcenanforderung erstellt, um den restlichen Bedarf zu erfassen.
- Mehrere Ressourcen buchen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die Arbeit zu erledigen.
- Weniger Ressourcen buchen als benötigt. In diesem Szenario sind die gebuchten Stunden geringer als die benötigten Stunden. Das System gibt Ihnen eine Anleitung zum Vorschlagen von Ressourcen anstelle von Buchungen, sodass der Anfragende den verbleibenden Bedarf überprüfen und im Auge behalten kann.

## <a name="resource-availability"></a>Ressourcenverfügbarkeit

Ressourcenmanager müssen die Verfügbarkeit von Ressourcen anzeigen und Buchungen aktualisieren können. In einigen Fällen liegt keine formelle Nachfrage vor (Ressourcenanforderung). Ein Ressourcenmanager muss jedoch auf eine ungeplante Nachfrage reagieren, die über andere Kanäle wie E-Mails, Telefonanrufe oder Instant Messages eingeht. Ressourcenmanager verwenden die **Zeitplanübersicht**, um Ressourcen und Buchungen zu aktualisieren.

Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet. Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.

Die **Zeitplanübersicht** verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen. Eine Einstellung auf der **Zeitplanübersicht** lässt Sie eine Legende anzeigen.

Wenn neben einer einzelnen buchbaren Ressource in der **Zeitplanübersicht** ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.

Da Dynamics 365 Project Operations die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.

Um zusätzliche Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
