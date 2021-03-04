---
title: Buchungszuordnungsmethoden in Project Service Automation
description: Dieses Thema enthält Informationen zu den verschiedenen Möglichkeiten, wie Sie Zuordnungen buchen können.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: e1ceb7ea5484a1d099c4709eda48d34ecd9bac2e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151612"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Buchungszuordnungsmethoden in Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Unabhängig davon, ob Sie ein Teammitglied direkt zu einem Projekt auf der Registerkarte **Team** hinzufügen oder eine Ressource für ein Projekt oder eine Anforderung über die Zeitplanübersicht buchen, können Sie verschiedene Buchungszuweisungsmethoden verwenden. In diesem Thema wird erläutert, wie die einzelnen Methoden funktionieren und welche Methoden zu einer Überbuchung von Ressourcen führen können.

## <a name="full-capacity"></a>Volle Kapazität 
Die Methode „Volle Kapazität” bucht die volle Kapazität der Ressource für das angegebene Start- und Enddatum. Wenn für eine Ressource beispielsweise ein Kalender für acht Stunden pro Tag an fünf Tagen in der Woche festgelegt ist und ein Start- und Enddatum festgelegt wird, das fünf Arbeitstage umfasst, wird die Ressource für 40 Stunden gebucht. Die Anmeldung wird ohne Rücksicht auf die verbleibende Ressourcenrestkapazität ausgeführt. Wenn in diesem Zeitraum eine Ressource bereits für andere Projekte gebucht wurde, werden die 40 Stunden als zusätzliche Stunden gebucht, was möglicherweise zu Überbuchungen führt.

## <a name="remaining-capacity"></a>Verbleibende Kapazität
Die Methode „Verbleibende Kapazität” ist nur verfügbar, wenn Sie mithilfe der Zeitplanübersicht direkt für ein Projekt buchen. Die Ressource verfügt nicht über ausreichende Kapazität innerhalb des angegebenen Datumsbereichs. Wenn eine Ressource beispielsweise eine Kapazität von 40 Stunden pro Woche hat und bereits für 10 Stunden gebucht wurde, führt die Buchung für dieselbe Woche zur Buchung der verbleibenden Kapazität von 30 Stunden für diese Woche.

## <a name="percentage-capacity"></a>Kapazität in Prozent
Die Methode Kapazität in Prozent bucht die Ressource für einen Prozentsatz der Kapazität für das angegebene Start- und Enddatum. Wenn der Kalender einer Ressource beispielsweise auf acht Stunden pro Tag an fünf Tagen in der Woche eingestellt ist und ein Start- und Enddatum festgelegt wird, das fünf Arbeitstage bei 50% Kapazität umfasst, wird die Ressource für 20 Stunden gebucht. Die einzelnen Buchungen pro Tag werden gleichmäßig auf den Zeitraum verteilt – in diesem Beispiel vier Stunden pro Tag. Die Anmeldung wird ohne Rücksicht auf die verbleibende Ressourcenrestkapazität ausgeführt. Wenn die Ressource in diesem Zeitraum bereits für andere Projekte gebucht wurde, werden die 20 Stunden als zusätzliche Stunden gebucht, was möglicherweise zu Überbuchungen führt.

## <a name="evenly-distribute-hours"></a>Stunden gleichmäßig verteilen
Die Methode „Stunden gleichmäßig verteilen” bucht die Ressource für eine bestimmte Anzahl Stunden und verteilt die Zeit gleichmäßig pro Tag zwischen dem angegebenen Start- und Enddatum. Wenn Sie eine Ressource für 20 Stunden über einen Zeitraum von fünf Tagen buchen, verteilt diese Methode die 20 Stunden gleichmäßig bei vier Stunden pro Tag. Die Anmeldung wird ohne Rücksicht auf die verbleibende Ressourcenrestkapazität ausgeführt. Wenn die Ressource in diesem Zeitraum bereits für andere Projekte gebucht wurde, werden die 20 Stunden als zusätzliche Stunden gebucht, was möglicherweise zu Überbuchungen führt.

## <a name="front-load-hours"></a>Von vorn nach hinten verteilte Stunden
Die Methode „Nach Stunden von vorn nach hinten verteilen” bucht die Ressource für eine festgelegte Anzahl Stunden und verteilt die Stunden pro Tag von vorn nach hinten zwischen dem angegebenen Start- und Enddatum. Das Verteilen von vorne nach hinten nutzt die verfügbare Kapazität der Ressource in der Reihenfolge „zuerst zugewiesen, zuerst verbraucht” Wenn der Arbeitszeitplan einer Ressource beispielsweise acht Stunden pro Tag und fünf Tage pro Woche beträgt und keine aktuellen Buchungen vorliegen, führt das Buchen der Ressource für 20 Stunden über einen Zeitraum von fünf Arbeitstagen zu folgendem täglichen Buchungsmuster: 

|         Buchungen          |    Tag 1    |    Tag 2    |    Tag 3    |    Tag 4    |    Tag 5    |    Gesamt    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Vorhandene Buchungen    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Neue Buchung          |    8        |    8        |    4        |    0        |    0        |    20       |

Die Verteilungsmethode von vorne nach hinten berücksichtigt folgende bestehenden Anmeldungen und Kapazitäten. Wenn dieselbe Ressource beispielsweise in der Arbeitswoche bereits über 20 Stunden Buchungen verfügt, verbrauchen die neuen Buchungen die verbleibende Kapazität wie folgt:

|   Buchungen          | Tag 1 | Tag 2 | Tag 3 | Tag 4 | Tag 5 | Gesamt |
|---------------------|-------|-------|-------|-------|-------|-------|
| Vorhandene Buchungen | 8     | 8     | 4     | 0     | 0     | 20    |
| Neue Buchung       | 0     | 0     | 4     | 8     | 8     | 20    |

Da die verfügbare Kapazität berücksichtigt wird, wird möglicherweise eine Fehlermeldung zurückgegeben, wenn die Ressource nicht über Restkapazität verfügt, die nach der Anmeldung absorbiert werden kann. Auf diese Weise können Sie nicht überbuchen.

## <a name="none"></a>Keine
Diese Methode „Keine” ist nur verfügbar, wenn Sie über die Registerkarte **Team** innerhalb eines Projekts buchen. Diese Methode fügt die Ressource dem Team im Projekt hinzu erstellt aber keine Anmeldungen, um die Kapazität der Ressource zu absorbieren. Diese Methode wird verwendet, wenn das Projekt-Manager-Teammitglied hinzugefügt wird, wenn ein Projekt erstellt wird. Der Projekt-Manager-Benutzer, der das Projekt erstellt, wird standardmäßig dem Projekt hinzugefügt, damit der Projektentitätsdatensatz einen Besitzer hat und das Projekt einen Genehmiger hat. Da dieser Benutzer keine Buchungen hat, können Sie, wenn Sie die Ressource buchen möchten, diese entweder löschen und anschließend mithilfe einer anderen Zuordnungsmethode erneut hinzufügen, oder Sie können die Ressource Aufgaben hinzufügen, indem Sie auf der Registerkarte **Abstimmung** die Option **Buchungen erweitern** verwenden, um Buchungen für die Zuweisungen zu erstellen.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Zuordnungsmethoden, die zu Überbuchen führt
Zusammenfassend die folgenden Zuordnungsmethoden führen zu Überbuchen, wenn die Ressource bereits in anderen Projekten festgelegt ist (oder für andere Arbeitsaufträge oder planbare Entitäten):

- Volle Kapazität
- Kapazität in Prozent
- Stunden gleichmäßig verteilen

Wenn Sie eine dieser drei Möglichkeiten für Zuordnungen nutzen, werden Sie nicht darauf hingewiesen, dass die Ressource überbucht wird. Um die Überbuchung zu korrigieren, müssen Sie die Zeitplanübersicht verwenden.
