---
title: Ansicht für Zeitplan-Assistent
description: Dieses Thema enthält Informationen zur Arbeit mit dem Zeitplan-Assistenten zum Buchen von Ressourcen.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125627"
---
# <a name="schedule-assistant-overview"></a>Ansicht für Zeitplan-Assistent

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Mit dem Zeitplan-Assistenten werden Ressourcen basierend auf den vom Projektmanager festgelegten Anforderungen gebucht. Der Zeitplan-Assistent stützt sich auf die in der Ressourcenanforderung angegebenen Parameter, um die Ressource zu finden. Der Zeitplan-Assistent empfiehlt Ressourcen, die den relevanten Anforderungen entsprechen, z. B. Zeitfenster oder erforderliche Fähigkeiten.

Nachdem geeignete Ressourcen identifiziert wurden, kann der Ressourcen- oder Projektmanager die Ressource für die Arbeit buchen.

## <a name="prerequisites"></a>Voraussetzungen

Der Zeitplan-Assistent ist Teil der Universal Resource Scheduling-Lösung. Diese Lösung ist in Dynamics 365 Project Operations, Dynamics 365 Field Service und Dynamics 365 Customer Service enthalten und installiert.

## <a name="matching-requirements-and-resources"></a>Übereinsteimmende Anforderungen und Ressourcen

Ein generierter Ressourcenbedarf basiert auf Details wie:

-   Merkmale
-   Rollen
-   Unternehmenseinheiten
-   Bevorzugte Ressourcen
-   Aufwandskonturen
-   Zeitzone

Der Zeitplan-Assistent verwendet diese Details, um Ressourcen zu filtern.

## <a name="launch-the-schedule-assistant"></a>Den Zeitplan-Assistenten starten

Es gibt zwei Möglichkeiten, wie der Zeitplan-Assistent gestartet wird. Wenn Sie den Hybridmodus verwenden, können Sie im Teammitgliedsraster jedes Teammitglied mit einem nicht erfüllten Ressourcenbedarf und dann **Buchen** auswählen. Wenn Sie den zentralen Modus verwenden, findet der Ressourcenmanager die Ressource und wählt sie aus.

## <a name="schedule-assistant-filters"></a>Zeitplan-Assistent-Filter

Nachdem der Zeitplan-Assistent ausgeführt wurde, werden die Details aus der Ressourcenanforderung als gefilterte Werte im linken Bereich angezeigt. Der Ressourcenmanager oder der Projektmanager kann die Ergebnisse optimieren, indem er die Filter an die Planungsanforderungen anpasst.

Im Filterbereich werden arbeitsbezogene Optionen angezeigt, darunter:

-   Arbeitsstart- und Enddatum
-   Merkmale
-   Rollen
-   Organisationseinheiten
-   Ressourcenzuordnungsunternehmen
-   Ressourcentypen
-   Bevorzugte Ressourcen


[!INCLUDE[footer-include](../includes/footer-banner.md)]