---
title: Ressourcenverwaltungsmodi – Übersicht
description: Dieses Thema enthält Informationen zu den Funktionen für die Ressourcenverwaltung in Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930090"
---
# <a name="resource-management-modes-overview"></a>Ressourcenverwaltungsmodi – Übersicht

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_


Dynamics 365 Project Operations unterstützt zwei Modi, damit Sie den gesamten Buchungsablauf ausführen können. Der Verwaltungsmodus ist als Projektparameter definiert und kann geändert werden, wenn sich Ihre Geschäftsanforderungen ändern.    

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
