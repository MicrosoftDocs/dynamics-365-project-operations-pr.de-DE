---
title: FAQ zur Ressourcenverwaltung
description: Dieses Thema liefert Antworten auf häufig gestellte Fragen zur Ressourcenverwaltung.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144367"
---
# <a name="resource-management-faq"></a>FAQ zur Ressourcenverwaltung

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Was ist der Unterschied zwischen einem Teammitglied und einer Ressourcenanforderung?

Ein Projektteammitglied kann Aufgaben zugewiesen, gebucht oder überbucht sowie als genehmigende Person festgelegt werden. Eine Ressourcenanforderung kann ohne ein Projektteammitglied existieren, als Entwurfsnotiz der Nachfrage. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Was ist der Unterschied zwischen vorgeschlagenen und unverbindlich gebuchten Stunden?

Vorgeschlagene Stunden und unverbindlich gebuchte Stunden unterscheiden sich hinsichtlich der Sichtbarkeit. Vorgeschlagene Stunden sind nur für die Ressourcenmanager und den Projektmanager sichtbar, die die Nachfrage mithilfe einer Ressourcenanfrage initiiert haben. Unverbindlich gebuchte Stunden sind für alle Personen sichtbar, die Zugriff auf die Zeitplanübersicht haben.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Wie können die unverbindlich gebuchten Stunden für Ressourcen in einem Team anzeigen?

Unverbindliche Buchungen können beim Buchen einer Ressourcenanforderung vorgenommen werden. Ressourcen, die für ein Projektteam unverbindlich gebucht werden, werden als Teammitglieder mit unverbindlich gebuchten Stunden angezeigt. Sie werden auch in der Zeitplanübersicht angezeigt.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Wie ändere ich die erforderlichen Stunden sowie das Start- und Enddatum für eine von mir gebuchte Ressource (generisch oder benannt)?

Wählen Sie nach dem Buchen von Ressourcen **Buchungen verwalten** aus, um erforderliche Änderungen vorzunehmen.

## <a name="what-resources-types-does-project-service-automation-support"></a>Welche Ressourcentypen werden von Project Service Automation unterstützt?

**Benutzer** und **Kontakt** sind die einzigen Ressourcentypen, die in Dynamics 365 Project Service Automation unterstützt werden. Obwohl Sie andere Ressourcentypen erstellen können (z. B. **Arbeitsgerät** und **Gruppe**), wird für sie kein End-to-End-Anwendungsfall unterstützt.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Was ist der Unterschied zwischen einer Zuweisung und einer Buchung?

Zuweisungen betreffen die Zuweisung von Ressourcen zu Projektaufgaben im Projektzeitplan. Bei den Ressourcen kann es sich entweder um reale oder um generische Ressourcen handeln. Buchungen betreffen die verbindliche oder unverbindliche Zuweisung von Ressourcen zu einem Projekt. Verbindliche Buchungen verbrauchen die Kapazität einer Ressource. Idealerweise sollten die Buchungen und Zuweisungen für reale Buchungen übereinstimmen, da sie sich nicht unterscheiden. Diese Vereinbarung wird von PSA jedoch nicht erzwungen. Die Abstimmungsansicht zeigt einem Projektmanager an, wo die Buchungen und Zuweisungen einer Ressource nicht übereinstimmen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]