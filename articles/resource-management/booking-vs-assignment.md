---
title: Buchungen gegenüber Arbeitsaufträge
description: In diesem Artikel finden Sie Informationen zu den Unterschieden zwischen Ressourcenbuchungen und Ressourcenzuweisungen.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918587"
---
# <a name="bookings-vs-assignments"></a>Buchungen gegenüber Arbeitsaufträge

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt. Verbindliche Buchungen verbrauchen die Kapazität einer Ressource. Buchungen stellen Organisationskonzepte für Teams dar, damit diese verstehen können, wie die Ressourcen projektübergreifend eingesetzt werden. Dynamics 365 Project Operations betrachtet Buchungen als ein Konzept auf Projektebene. 

Im Gegensatz zu Buchungen sind Zuweisungen die Bindung von Ressourcen an Projektaufgaben im Projektplan. Die Ressourcen können benannt oder generisch sein.  Wenn eine Ressourcenanforderung aus den Projektaufgabenzuweisungen abgeleitet wird, verwendet Project Operations die Aufwandskonturen der Ressourcenzuweisung, um die Konturen der Ressourcenanforderungsdetails zu erstellen. Eine Bezugnahme auf die Ressourcenzuweisungen wird jedoch nicht beibehalten. Aktualisierungen der Buchungen, die aus der Ressourcenanforderung abgeleitet wurden, aktualisieren keine Ressourcenzuweisungen.

Normalerweise entspricht die Summe der Buchungen für eine Ressource der Summe der Zuweisungen der Ressource für eine oder mehrere Aufgaben. Project Operations erzwingt diese Vereinbarung jedoch nicht. Die **Abstimmungsansicht** zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]