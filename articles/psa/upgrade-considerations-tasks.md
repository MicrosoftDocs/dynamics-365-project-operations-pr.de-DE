---
title: Upgrade-Überlegungen für den Projektstrukturplan
description: Dieses Thema enthält Informationen zum Aktualisieren des Projektstrukturplans von Project Service Automation 2.x auf 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005610"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Upgrade-Überlegungen für den Projektstrukturplan

[!include [banner](../includes/psa-now-project-operations.md)]

Dieses Thema enthält Informationen zum Aktualisieren des Projektstrukturplans von Project Service Automation 2.x auf 3.x. Dieses Thema definiert den fehlerfreien Status eines Projekts in Project Service Automation (PSA), der für ein erfolgreiches Upgrade erforderlich ist. Es gibt auch Informationen über die allgemeinen Sperrbedingungen, die zum Fehlschlag eines Upgrades führen können. Weitere Informationen über das Definieren von Projektaufgaben und deren Funktionen innerhalb eines Projektzeitplans finden Sie unter [Projektzeitpläne](project-creating.md).

## <a name="key-entities"></a>Schlüsselentitäten
Für einen akkuraten Projektstrukturplan, für den bereits Ressourcen geladen sind, sind die folgenden Entitäten erforderlich:

- [Projekt](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Projektteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Projektaufgabe](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Ressourcenzuweisungen](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Abhängigkeit der Projektaufgaben](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Buchbare Ressourcen](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Um eine Ressource zu definieren, die in einen Projektstrukturplan geladen wird, müssen Sie die folgenden Schritte ausführen:

1. Erstellen Sie ein neues Projekt. Weitere Informationen darüber, wie ein neues Projekt erstellt wird, finden Sie unter [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Erstellen Sie mindestens eine Aufgabe. Weitere Informationen darüber, wie Sie eine Aufgabe erstellen, finden Sie unter [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definieren Sie die Aufgabenabhängigkeiten. Weitere Informationen finden Sie unter [Projektaufgabenabhängigkeit](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Weisen Sie dem Projekt Projektteam-Mitglieder zu. Weitere Informationen finden Sie unter [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Weisen Sie den Aufgaben Projektteam-Mitglieder zu. Weitere Informationen finden Sie unter [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Projektteambeziehungen

Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:
- Alle Projektteam-Mitglieder müssen einer buchbaren Ressource zugeordnet werden.
- Alle Projektteam-Mitglieder müssen demselben Projekt zugeordnet werden. 

## <a name="project-task-relationships"></a>Projektaufgabenbeziehungen
Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:

- Alle zugehörigen Aufgaben müssen demselben Projekt zugeordnet werden.
- Jede Positionsaufgabe muss eine übergeordnete Aufgabe haben.
- Jede Aufgabe muss ein übergeordnetes Projekt haben.

### <a name="valid-conditions"></a>Gültige Bedingungen

- Alle Aufgabendauern müssen größer oder gleich (>=) eine Stunde und weniger als 1.800.000 Minuten (1.250 Tage) sein.*
- Alle Aufgaben müssen ein Startdatum haben, das nicht vor dem 01.01.2000 liegen darf.*
- Alle Aufgaben müssen ein Startdatum haben, das nicht mehr als 17 Jahre nach dem heutigen Tag liegen darf.*
- Alle Aufgaben müssen ein Startdatum haben, das gleich ihrem Abschlussdatum ist oder vor diesem liegt.
- Alle Transaktionstypen für Klassifizierungen (Ausgaben, Material, Steuern und Zeit) müssen über Werte für **Standardeinheit** und **Einheitengruppe** verfügen.
- Datumsformate mit Buchstaben sollten vermieden werden.

### <a name="potential-mitigation-steps"></a>Potentielle Risikominderungsschritte
- Verwenden Sie die erweiterte Suche, um Projektaufgaben zu identifizieren, die keine Projekt-ID enthalten.
- Verwenden Sie die erweiterte Suche, um Projektaufgaben zu identifizieren, deren geplante Dauer größer als> 1.800.000 ist.
- Bevor Sie Datenänderungen vornehmen, sollten Sie Anpassungen untersuchen, die der Entität zugeordnet sind und dazu geführt haben, dass die Daten möglicherweise in einen fehlerhaften Zustand versetzt wurden. Diese Anpassungen sollten behoben werden, bevor Sie mit datenbezogenen Aktualisierungen fortfahren.
- Erwägen Sie für die identifizierten Aufgaben, die verwaist sind, das Löschen dieser Aufgaben, wenn sie nicht benötigt werden oder dem richtigen übergeordneten Projekt zugeordnet werden sollen.
- Bei Aufgaben mit einer Dauer von mehr als 1.250 Tagen sollten Sie mehrere Aufgaben hinzufügen, um die Gesamtdauer darzustellen, sofern dies möglich ist.

> [!NOTE]
> Elemente, die mit einem Sternchen (\*) markiert sind, haben Begrenzungen, die daran liegen, dass die Kundenbeziehungsverwaltung (CRM) nur 7.320 Serienerweiterungen unterstützt. Sie müssen unter diesem Grenzwert bleiben.

## <a name="resource-assignment-relationships"></a>Ressourcenarbeitsauftragbeziehungen
Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:

- Alle Ressourcenarbeitsaufträge in einem Projektstrukturplan müssen mit demselben Projekt verknüpft sein.
- Alle Ressourcenarbeitsaufträge in einem Projektstrukturplan müssen Projektteam-Mitgliedern im selben Projekt zugeordnet sein.

### <a name="potential-mitigation-steps"></a>Potentielle Risikominderungsschritte
- Identifizieren Sie alle Aufgaben, die außerhalb der oben beschriebenen Bedingungen liegen.  
- Alle Ressourcenarbeitsaufträge, die nicht mehr gültig sind, sollten gelöscht werden.

## <a name="project-task-dependency-relationships"></a>Projektaufgaben-Abhängigkeitsbeziehungen
Um ein erfolgreiches Upgrade zu gewährleisten, müssen die folgenden Beziehungen korrekt gewartet werden:

- Alle Projektaufgabenabhängigkeiten müssen mit demselben Projekt verknüpft sein.
- Auf eine Aufgabe kann nicht mehrmals dieselbe Abhängigkeit verwiesen werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]