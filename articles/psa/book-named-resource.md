---
title: Buchen von benannten Ressourcen aus Ressourcenanforderungen
description: Dieses Thema enthält Informationen zum Buchen von benannten Ressourcen für eine generische Ressourcenanforderung.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 92a61012beb9aa200f4ea65b777acb0fae04e7e6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590069"
---
# <a name="book-named-resources-from-resource-requirements"></a>Buchen von benannten Ressourcen aus Ressourcenanforderungen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sie können eine benannte Ressource buchen, um eine allgemeine Ressource zu ersetzen, die über eine Ressourcenanforderung verfügt.

1. Klicken Sie in Project Service Automation (PSA) auf der Seite **Projekte** auf die Registerkarte **Team**.
2. Wählen Sie in der Liste die allgemeine Ressource aus, die eine Ressourcenanforderung enthält, und klicken Sie dann auf **Buchen**. Alternativ öffnen Sie die Ressourcenanforderungen und klicken Sie dann auf **Buchen**.


![Buchen eines generischen Teammitglieds.](media/RM-how-to-14.png)


3. Wählen Sie auf der Seite **Zeitplan-Assistent** eine benannte Ressource aus, um sie für Ihr Projektteam zu buchen, und klicken Sie anschließend auf **Buchen**.

![Buchen eines generischen Teammitglieds mithilfe des Zeitplan-Assistenten.](media/RM-how-to-15.png)

Wenn die Buchung abgeschlossen und von einer benannten Ressource ausgeführt wurde, wird die generische Ressource durch die benannte Ressource ersetzt.

![Benanntes Teammitglied, das ein generisches Teammitglied ersetzt.](media/RM-how-to-16.png)

Die Zuweisungen im Zeitplan werden mit der benannten Ressource ebenfalls aktualisiert.

![Benanntes Teammitglied, das Projektaufgaben zugewiesen ist.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Erfüllen einer generischen Ressource mit mehreren benannten Ressourcen
Das Erfüllen einer Anforderungen für eine generische Ressource mit mehreren benannten Ressourcen ähnelt dem Zuweisen einer einzelnen benannten Ressource. Zum Beispiel gibt es eine Aufgabe mit einer Dauer von fünf Tagen und einem Aufwand von 120 Stunden. Diese Aufgabe kann nicht von einer Ressource ausgeführt werden, die einen typischen Acht-Stunden-Tag über eine Fünf-Tage-Woche hat. 

![Aufgabe, die einen Aufwand von 120 Stunden über fünf Tage erfordert.](media/RM-how-to-21.png)

Die Anforderung lautet 120 Stunden Robotertechnik an fünf Tagen, also 24 Stunden am Tag.

![Anforderung pro Tag.](media/RM-how-to-22.png)

Dies ist ein Beispiel für den Fall, dass mehrere benannte Ressourcen benötigt werden, um eine generische Ressourcenanforderung zu erfüllen. Sie müssen mehrere Ressourcen buchen, um die Anforderung zu erfüllen.

![Buchen von mehreren Ressourcen, um die Anforderung zu erfüllen.](media/RM-how-to-23.png)

Der Hauptunterschied in diesem Szenario besteht darin, dass die generische Ressource bei dem der Aufgabe zugewiesenen Team bleibt und die gebuchten Mitglieder des benannten Ressourcenteams nicht als Teil der Position zugewiesen werden. Der Projektmanager kann die Arbeit den genannten Ressourcen entsprechend zuweisen. Die Ansicht **Abstimmung** unterstützt einen Projektmanager bei der Aufteilung der Buchungen auf mehrere Ressourcen zu Aufgabenzuweisungen. Dies erfolgt nicht automatisch, da in jedem Szenario, das komplizierter ist als das obige einfache Beispiel, z. B. wenn Sie ein Bündel von Aufgaben haben, aus denen die Anforderung besteht, muss die Absicht, wie der Projektmanager sie zuweisen möchte, vom System angenommen werden. Da das System Absichten nicht verstehen kann, ist es wahrscheinlich, dass die Annahmen anders als beabsichtigt sind und ein falsches oder unvorhersagbares Ergebnis auftritt. Das vorhersagbare Ergebnis ist, dass die generische Ressource zugewiesen bleibt, bis der Projektmanager mit Hilfe der Ansicht **Abstimmung** willentlich Zuweisungen erstellt.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
