---
title: Ressourcenverwaltungsmodi – Übersicht
description: Dieses Thema enthält Informationen zur Ressourcenverwaltungsfunktionalität in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279452"
---
# <a name="resource-management-modes-overview"></a>Ressourcenverwaltungsmodi – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dynamics 365 Project Operations unterstützt zwei Modi, mit denen Sie den gesamten Buchungsflow ausführen können. Der Verwaltungsmodus ist als Projektparameter definiert und kann geändert werden, wenn sich Ihre Geschäftsanforderungen ändern.    

## <a name="central-mode"></a>Zentraler Modus
Für Organisationen, die die Zuweisung von Ressourcen zu Projekten zentralisieren, bietet der Zentralmodus eine Möglichkeit, um sicherzustellen, dass Projektmanager Ressourcenanforderungen auf Projektebene definieren können. Die Erfüllung der Ressourcenanforderungen wird an einen Ressourcenmanager delegiert. Projektmanager können Ressourcen akzeptieren oder ablehnen, die vom Ressourcenmanager vorgeschlagen werden.

![Zentraler Modus](./media/resource-management-central.png)

Informationen zum Verwalten von Ressourcen im zentralen Modus finden Sie unter:

- [Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Benannte Ressourcen aus Ressourcenanforderungen buchen](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Eine Ressourcenanforderung übermitteln](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Eine Ressourcenanfrage erfüllen](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Eine vorgeschlagene Projektressource aus einer Ressourcenanfrage annehmen oder ablehnen](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hybridmodus
Für Organisationen, die Flexibilität bei der Zuweisung von Ressourcen benötigen, bietet der Hybridmodus sowohl Projektmanagern als auch Ressourcenmanagern die Möglichkeit, Ressourcen zu buchen.

![Hybridmodus](./media/resource-management-hybrid.png)

Weitere Informationen zum Verwalten aller anderen unterstützten Buchungsabläufe im Hybridmodus finden Sie neben dem unterstützten Prozess im zentralen Modus in den folgenden Themen:

Eine Ressource direkt auf ein Projekt buchen:
- [Genannte buchbare Ressourcen für ein Projektteam buchen und Aufgaben zuweisen](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Eine Ressource aus einer Ressourcenanforderung buchen:
- [Allgemeine buchbare Ressourcen einer Aufgabe zuweisen und Ressourcenanforderungen erstellen](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Benannte Ressourcen aus Ressourcenanforderungen buchen](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]