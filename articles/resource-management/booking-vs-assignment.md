---
title: Buchungen gegenüber Arbeitsaufträge
description: Dieses Thema enthält Informationen zu den Unterschieden zwischen Ressourcenbuchungen und Ressourcenarbeitsaufträgen.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008450"
---
# <a name="bookings-vs-assignments"></a>Buchungen gegenüber Arbeitsaufträge

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt. Verbindliche Buchungen verbrauchen die Kapazität einer Ressource. Buchungen stellen Organisationskonzepte für Teams dar, damit diese verstehen können, wie die Ressourcen projektübergreifend eingesetzt werden. Dynamics 365 Project Operations betrachtet Buchungen als ein Konzept auf Projektebene. 

Im Gegensatz zu Buchungen sind Zuweisungen die Bindung von Ressourcen an Projektaufgaben im Projektplan. Die Ressourcen können benannt oder generisch sein.  Wenn eine Ressourcenanforderung aus den Projektaufgabenzuweisungen abgeleitet wird, verwendet Project Operations die Aufwandskonturen der Ressourcenzuweisung, um die Konturen der Ressourcenanforderungsdetails zu erstellen. Eine Bezugnahme auf die Ressourcenzuweisungen wird jedoch nicht beibehalten. Aktualisierungen der Buchungen, die aus der Ressourcenanforderung abgeleitet wurden, aktualisieren keine Ressourcenzuweisungen.

Normalerweise entspricht die Summe der Buchungen für eine Ressource der Summe der Zuweisungen der Ressource für eine oder mehrere Aufgaben. Project Operations erzwingt diese Vereinbarung jedoch nicht. Die **Abstimmungsansicht** zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]