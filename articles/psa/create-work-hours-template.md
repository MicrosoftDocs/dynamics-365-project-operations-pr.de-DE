---
title: Eine Arbeitsstundenvorlage erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Arbeitszeitvorlage in Project Service erstellen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987390"
---
# <a name="create-a-work-hours-template-project-service"></a>Erstellen Sie eine Arbeitszeitvorlage (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden. Die Kalendervorlage definiert die folgenden Projektattribute:

- Arbeitszeit einschließlich Start- und Endzeit
- Werktags
- Kalenderausnahmen wie arbeitsfreie Tage

Die Kalendervorlage, die auf ein Projekt angewendet wird, ist eine Kopie der Kalendervorlage, die in den Einstellungen Ihrer Organisation definiert ist.

> [!NOTE]
> Wenn Sie die Kalendervorlage ändern, werden diese Änderungen nicht auf die Arbeitszeiten des Projekts übertragen. Um die Arbeitszeiten des Projekts zu ändern, muss eine neue Vorlage angewendet werden.

Um eine Kalendervorlage für Ihre Organisation zu erstellen, gibt es zwei Hauptanforderungen:

- Definieren Sie die gewünschten Arbeitszeiten der Vorlage mithilfe einer neuen oder vorhandenen buchbaren Ressource.
- Erstellen Sie eine neue Kalendervorlage und ordnen Sie die Vorlage der buchbaren Ressource zu.

**Arbeitsstunden der Vorlage definieren**

1. Navigieren Sie zu **Ressourcen** \> **Ressourcen**.
2. Erstellen Sie eine neue Ressource, auf die in der Kalendervorlage verwiesen werden soll, oder wählen Sie eine vorhandene Ressource aus.
3. Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](/dynamics365/field-service/set-work-hours-resource.md) um die Kalenderregeln zu konfigurieren.

**Erstellen einer neuen Kalendervorlage.**

1. Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.
2. Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.


> [!NOTE]
> Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet. Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.


### <a name="see-also"></a>Siehe auch  
 [Ressourcen einrichten](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
