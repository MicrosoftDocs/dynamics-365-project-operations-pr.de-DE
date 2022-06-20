---
title: Ressourcenverwaltungsmodi – Übersicht
description: Dieser Artikel enthält Informationen über die Funktionen zur Verwaltung von Ressourcen in Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928431"
---
# <a name="resource-management-modes-overview"></a>Ressourcenverwaltungsmodi – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dynamics 365 Project Operations unterstützt zwei Modi, mit denen Sie den gesamten Buchungsflow ausführen können. Der Verwaltungsmodus ist als Projektparameter definiert und kann geändert werden, wenn sich Ihre Geschäftsanforderungen ändern.    

## <a name="central-mode"></a>Zentraler Modus
Für Organisationen, die die Zuweisung von Ressourcen zu Projekten zentralisieren, bietet der Zentralmodus eine Möglichkeit, um sicherzustellen, dass Projektmanager Ressourcenanforderungen auf Projektebene definieren können. Die Erfüllung der Ressourcenanforderungen wird an einen Ressourcenmanager delegiert. Projektmanager können Ressourcen akzeptieren oder ablehnen, die vom Ressourcenmanager vorgeschlagen werden.

![Zentraler Modus.](./media/resource-management-central.png)

Informationen zum Verwalten von Ressourcen im zentralen Modus finden Sie unter:

- [Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen](/dynamics365/project-service/assign-generic-bookable-resource)
- [Benannte Ressourcen aus Ressourcenanforderungen buchen](/dynamics365/project-service/book-named-resource)
- [Eine Ressourcenanforderung übermitteln](/dynamics365/project-service/submit-resource-request)
- [Eine Ressourcenanfrage erfüllen](/dynamics365/project-service/resource-management-fulfill-requests)
- [Eine vorgeschlagene Projektressource aus einer Ressourcenanfrage annehmen oder ablehnen](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridmodus
Für Organisationen, die Flexibilität bei der Zuweisung von Ressourcen benötigen, bietet der Hybridmodus sowohl Projektmanagern als auch Ressourcenmanagern die Möglichkeit, Ressourcen zu buchen.

![Hybridmodus.](./media/resource-management-hybrid.png)

Zusätzlich zu dem unterstützten Prozess im Zentralmodus lesen Sie die folgenden Artikel, um alle anderen unterstützten Flows im Hybridmodus zu verwalten:

Eine Ressource direkt auf ein Projekt buchen:
- [Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen](/dynamics365/project-service/assign-named-bookable-resource)

Eine Ressource aus einer Ressourcenanforderung buchen:
- [Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen](/dynamics365/project-service/assign-generic-bookable-resource)
- [Benannte Ressourcen aus Ressourcenanforderungen buchen](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]