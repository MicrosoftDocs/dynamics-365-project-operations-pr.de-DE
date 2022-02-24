---
title: Allgemeine Ressourcenanforderungserfüllung
description: Dieses Thema enthält Informationen zum Buchen von benannten Ressourcen für eine generische Ressourcenanforderung.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130307"
---
# <a name="generic-resource-requirement-fulfillment"></a>Allgemeine Ressourcenanforderungserfüllung

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können eine benannte Ressource buchen, um eine allgemeine Ressource zu ersetzen, die über eine Ressourcenanforderung verfügt.

1. Auf der Seite **Projekte** wählen Sie die Registerkarte **Team**.
2. Wählen Sie in der Liste die allgemeine Ressource aus, die eine Ressourcenanforderung enthält, und wählen Sie **Buchen**. Alternativ öffnen Sie die Ressourcenanforderungen und wählen **Buchen**.
3. Wählen Sie auf der Seite **Zeitplan-Assistent** eine benannte Ressource aus, um sie für Ihr Projektteam zu buchen, und wählen Sie anschließend **Buchen**.

Wenn die Buchung abgeschlossen und von einer benannten Ressource ausgeführt wurde, wird die generische Ressource durch die benannte Ressource ersetzt.

Die Zuweisungen im Zeitplan werden mit der benannten Ressource ebenfalls aktualisiert.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Erfüllen einer generischen Ressource mit mehreren benannten Ressourcen
Das Erfüllen einer Anforderungen für eine generische Ressource mit mehreren benannten Ressourcen ähnelt dem Zuweisen einer einzelnen benannten Ressource. Zum Beispiel gibt es eine Aufgabe mit einer Dauer von fünf Tagen und einem Aufwand von 120 Stunden. Diese Aufgabe kann nicht von einer Ressource ausgeführt werden, die einen typischen Acht-Stunden-Tag über eine Fünf-Tage-Woche hat. 

Die Anforderung lautet 120 Stunden Robotertechnik an fünf Tagen, also 24 Stunden am Tag.

Dies ist ein Beispiel für den Fall, dass mehrere benannte Ressourcen benötigt werden, um eine generische Ressourcenanforderung zu erfüllen. Sie müssen mehrere Ressourcen buchen, um die Anforderung zu erfüllen.

Der Hauptunterschied in diesem Szenario besteht darin, dass die generische Ressource bei dem der Aufgabe zugewiesenen Team bleibt und die gebuchten Mitglieder des benannten Ressourcenteams nicht als Teil der Position zugewiesen werden. Der Projektmanager kann die Arbeit den genannten Ressourcen entsprechend zuweisen. Die Ansicht **Abstimmung** unterstützt einen Projektmanager bei der Aufteilung der Buchungen auf mehrere Ressourcen zu Aufgabenzuweisungen. Dies erfolgt nicht automatisch, da in jedem Szenario, das komplizierter ist als das obige einfache Beispiel, z. B. wenn Sie ein Bündel von Aufgaben haben, aus denen die Anforderung oder die Absicht besteht, wie der Projektmanager sie zuweisen möchte, vom System angenommen werden. Da das System Absichten nicht verstehen kann, weichen die Annahmen höchstwahrscheinlich von den Absichten ab und ein falsches oder unvorhersehbares Ergebnis tritt auf. Das vorhersagbare Ergebnis ist, dass die generische Ressource zugewiesen bleibt, bis der Projektmanager mit Hilfe der Ansicht **Abstimmung** willentlich Zuweisungen erstellt.


