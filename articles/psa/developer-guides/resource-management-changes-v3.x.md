---
title: Änderungen bei der Ressourcenverwaltung (Project Service Automation 3.x)
description: Dieses Thema enthält Informationen zu den Änderungen am Ressourcenverwaltungsbereich.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: e888d55b93c40e08e51bd4480853fec37f2b6333
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007815"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Änderungen bei der Ressourcenverwaltung (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Die Abschnitte dieses Themas bieten Informationen zu den Änderungen, die am Ressourcenverwaltungsbereich von Dynamics 365 Project Service Automation Version 3.x vorgenommen wurden.

## <a name="project-estimates"></a>Projektschätzungen

Statt auf der Entität **msdyn\_projecttask** (**Projektaufgabe**) basieren Projektvorkalkulationen auf der Entität **msdyn\_resourceassignment** (**Ressourcenzuweisung**). Ressourcenzuweisungen haben sich zur „Quelle der Wahrheit“ für Aufgabenplanung und Preisberechnung entwickelt.

## <a name="line-tasks"></a>Positionsaufgaben

In PSA 3.x sind Positionsaufgaben veraltet. Zuweisungen zeigen jetzt auf die gesamte Aufgabe statt auf die Positionsaufgaben.

Das folgende Beispiel zeigt, wie eine Aufgabe mit der Bezeichnung „Testaufgabe“ in früheren Versionen von PSA und in PSA 3.x den Teammitgliedern A und B zugewiesen wird.

- **Vor PSA 3.x:**

    - Testaufgabe

        - Testaufgabe – Positionsaufgabe 1

            - Zuweisung zu A

        - Testaufgabe – Positionsaufgabe 2

            - Zuweisung zu B

- **PSA 3.x:**

    - Testaufgabe

        - Zuweisung zu A
        - Zuweisung zu B

## <a name="unassigned-assignment"></a>Nicht zugewiesene Zuweisung

In PSA 3.x handelt es sich bei einer nicht zugewiesenen Zuweisung um eine Zuweisung, die einem Teammitglied **NULL** und einer Ressource **NULL** zugewiesen ist. Nicht zugewiesene Zuweisungen können in verschiedenen Szenarien auftreten:

- Wenn eine Aufgabe erstellt wurde, die bisher noch keinem Teammitglied zugewiesen wurde, wird immer eine nicht zugewiesene Zuweisung erstellt. 
- Wenn alle Zugewiesenen für eine Aufgabe entfernt werden, wird für diese Aufgabe eine nicht zugewiesene Zuweisung erstellt.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Planungsfelder auf der Projektaufgabenentität

Die Felder auf der Entität **msdyn\_projecttask** sind veraltet oder wurden zur Entität **msdyn\_resourceassignment** verschoben oder werden jetzt von der Entität **msdyn\_projectteam** (**Projektteammitglied**) referenziert.

| Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe) | Neues Feld auf msdyn\_resourceassignment (Ressourcenzuweisung) | Kommentar |
|---|---|---|
| msdyn\_assignedresources | Keine | |
| msdyn\_assignedteammembers | Keine | |
| msdyn\_numberofresources | Keine | |
| msdyn\_scheduledhours | Keine | |
| msdyn\_effortcontour | msdyn\_plannedwork | Das Format der Datenstruktur JavaScript Object Notation (JSON), die im Feld gespeichert ist, wurde geändert. |

## <a name="schedule-contour"></a>Zeitplankontur

Die Zeitplankontur wird im Feld **Geplante Arbeit** (**msdyn\_plannedwork**) der einzelnen Entitäten **Ressourcenzuweisung** (**msdyn\_resourceassignment**) gespeichert.

### <a name="structure"></a>Struktur

Die neue Struktur der Zeitplankontur besteht aus flexiblen Zeiterfassungen, die für jeden Tag des Zeitplans definiert sind. Jede Zeiterfassung hat folgende Eigenschaften:

- **Start** – Der Start der Arbeitsstunden für den Tag laut Projektkalender.
- **Ende** – Das Ende der Arbeitsstunden für den Tag laut Projektkalender.
- **Stunden** – Die Stundenzahl, die am Tag zugewiesen werden.

**Beispiel**

In diesem Beispiel wird ein Projektkalender wird ein Arbeitstag von 9:00 Uhr bis 17:00 Uhr in der UTC-8-Zeitzone verwendet.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatische und manuelle Zeitplanung

Wenn die Zeitplanung für eine Aufgabe automatisch erfolgt, werden die Stunden vorab geladen und die Aufgabendauer kann sich verkürzen.

**Beispiel**

Die folgende Aufgabe wurde automatisch für 18 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Wenn eine Aufgabe manuell geplant wird, werden die Stunden gleichmäßig auf alle Tage verteilt.

**Beispiel**

Die folgende Aufgabe wurde manuell für 18 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Zuweisungseinheit

Die Zuweisungseinheit ist in PSA 3.x. veraltet. Die Aufgabenaufwandsstunden wurden pro Tag gleichmäßig unter allen zugewiesenen Ressourcen aufgeteilt.

**Beispiel**

In diesem Beispiel wird die Aufgabe zwei Ressourcen zugewiesen und automatisch für 36 Stunden über drei Tage geplant (3. Dezember 2018 bis 5. Dezember 2018).

- Zuweisung 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Zuweisung 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Preisdimensionen

In PSA 3.x wurden Preisdimensions-Felder (z. B. **Rolle** und **Organisationseinheit**) aus der Entität **msdyn\_projecttask** entfernt. Diese Felder können jetzt vom entsprechenden Projektteammitglied (**msdyn\_projectteam**) der Ressourcenzuweisung (**msdyn\_resourceassignment**) abgerufen werden, wenn Projektvorkalkulationen generiert werden. Das neue Feld **msdyn\_organizationalunit** wurde der Entität **msdyn\_projectteam** hinzugefügt.

| Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe) | Feld von msdyn\_projectteam (Projektteammitglied), das stattdessen verwendet wird |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Konturen

Die Konturfelder für die Preisberechnung und die Vorkalkulationen sind auf der Entität **msdyn\_projecttask** nicht mehr vorhanden. Sie wurden zur Entität **msdyn\_resourceassignment** verschoben.

| Veraltetes Feld auf msdyn\_projecttask (Projektaufgabe) | Neues Feld auf msdyn\_resourceassignment (Ressourcenzuweisung) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Die folgenden Felder wurden der Entität **msdyn\_resourceassignment** hinzugefügt:

* msdyn\_plannedcost
* msdyn\_plannedsales

Die folgenden Felder für geplante, tatsächliche und verbleibende Kosten und Vertrieb auf der Entität **msdyn\_projecttask** bleiben unverändert:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]