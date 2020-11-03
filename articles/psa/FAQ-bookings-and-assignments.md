---
title: Ressourcenbuchungen und wie sie Aufgabenzuweisungen zugeordnet sind
description: Dieses Thema enthält Informationen zum Verwalten benannter Ressourcen, Ressourcenbuchungen und Aufgabenzuweisungen sowie zu deren Beziehung zueinander.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 03285d324e855ecf933b155559e5a4826420ab25
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076711"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Ressourcenbuchungen und wie sie Aufgabenzuweisungen zugeordnet sind


Es gibt zwei Möglichkeiten, benannte Ressourcen für ein Projektteam und für zugewiesene Projektaufgaben zu buchen:

- Die Ressource kann direkt für ein Projekt gebucht und dann später Projektaufgaben zugewiesen werden.
- Die Aufgaben können einer generischen Ressource zugewiesen werden, die dann verwendet wird, um die generische mit einer benannten Ressource zu ersetzen. 

In beiden Fällen reserviert die Buchung der Ressource schon die Kapazität der Ressource.

Der Projektmanager, der das Projekt plant, besitzt den Projektplan sowie den Zeitplan. Indem der Projektmanager die generische Ressource für die Zuweisung verwendet und daraus eine Ressourcenanforderung generiert, kann er Ressourcen mit den im Projektplan angegebenen Konturen für das Projekt buchen. Sie können Ressourcen für ein Projekt buchen und sie dann Aufgaben zuweisen. Es gibt jedoch keine Möglichkeit, die Buchungskonturen an den Konturen der Aufgaben auszurichten. Buchungen haben keinen Einfluss auf den Projektzeitplan.

Sehen Sie sich ein komplexes Projekt mit mehreren überlappenden Aufgaben an, das mehrere Ressourcen desselben Typs gleichzeitig bearbeiten muss. Wenn eine Ressource eine Kontur erhält, die vom Aggregat der Zuweisungen abweicht, ist es schwierig, die Aufgaben zu ändern, damit die Kontur der Anmeldungen mit ihren eigenen Aufgaben und den Ursprungskonturen zusammen passt.

Im Beispiel unten ist der Gesamtaufwand, der von der selben Ressource aus einer Reihe von vier Aufgaben erforderlich ist, 62 Stunden über einen Zeitraum von zwei Wochen in einer bestimmten Kontur. Wenn die Ressource für 62 Stunden während derselben zwei Wochen gebucht ist aber mit einer anderen Kontur, stimmt die Anforderung und die Buchung überein.

| **Aufgabenkonturen**    | **Gesamtstunden** | Mo 6/4 | Di 6/5 | Mi 6/6 | Do 6/7 | Fr 6/8 | Sa 6/9 | So 6/10 | Mo 6/11 | Di 6/12 | Mi 6/13 | Do 6/14 | Fr 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Aufgabe 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Aufgabe 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Aufgabe 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Aufgabe 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Gesamtergebnis**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Verfügbarkeit von Bob
| **Ressourcenbuchung** | **Gesamtstunden** | Mo 6/4 | Di 6/5 | Mi 6/6 | Do 6/7 | Fr 6/8 | Sa 6/9 | So 6/10 | Mo 6/11 | Di 6/12 | Mi 6/13 | Do 6/14 | Fr 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bob                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Es gibt keine systematische Möglichkeit, die gebuchte Stundenkontur Aufgaben auf der Basis pro Tag zuzuweisen. Wenn dem Projektmanager bereit ist, den Projektzeitplan zu ändern, um der Verfügbarkeit der Ressource zu entsprechen, müssen die Zuweisung entfernt und alle Aufgaben überarbeitet werden, um den Anmeldungskonturen zu entsprechen.

Wenn eine Organisation die Aufgabe der Projektplanung dem Projektmanager und dem Ressourcen-Manager zugewiesen hat, legt der Projektmanager den Zeitplan fest und integriert die erforderlichen Konturen der Arbeit. Der Ressourcen-Manager sollte nicht in der Lage sein, den Zeitplan ohne das Wissen des Projekt-Managers zu ändern, indem er Aufwandskonturen vornimmt, während die tatsächliche Ressource gebucht wird. Wenn der Ressourcen-Manager etwas anderes ausführt als vom Projektmanager gewünscht, müssen Sie sich einigen, welche Änderungen im Projektzeitplan erforderlich sind.

Da Buchungen und Zuweisungen nicht eng miteinander verbunden sind, können Sie Konturen buchen, die sich von den Aufgabenkonturen unterscheiden, oder die Zuweisungen ändern und dadurch Umstände zu schaffen, in denen Buchungen und Zuweisungen nicht aufeinander abgestimmt sind.

In der **Abstimmungsansicht** kann der Projektmanager die Buchungen und Zuordnungen für jedes Projektteammitglied anzeigen. Die Ansicht verwendet Farben und Schattierung, um anzuzeigen, wo es ein Konflikt zwischen Teammitgliedsanmeldungen und -Zuweisungen gibt. Auf Grundlage dieser Informationen kann der Projektmanager korrektive Maßnahmen ergreifen, um die Ressourcenanmeldungen für Anfragen erweitern, bei denen es Zuweisungen und keine Anmeldungen oder Anmeldungen stornieren, wenn Ressourcen gebucht werden, es aber keine Zuweisungen gibt.

> [!NOTE]
> Wenn Sie eine Aufgabe verschieben, die Sie konturiert haben, werden diese Konturen nicht beibehalten. Die Konturen werden nach dem Projektkalender neu erstellt, um Änderungen bei Arbeitszeiten und Feiertagen zu erläutern. Dies ist entwurfsbedingt, da das System nicht die Absicht der ursprünglichen Kontur kennt und nicht bestimmen kann, ob es Sinn ergibt, diese Kontur in einem neuen Zeitraum zu halten. Da Buchungen und Zuweisungen getrennt sind, behalten diese Buchungen die ursprünglichen Buchungskonturen. In diesem Fall müssen Sie stornieren und die neuen Zuweisungskontur neu buchen.

