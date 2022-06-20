---
title: Projektkalender definieren
description: In diesem Artikel erfahren Sie, wie Sie eine Kalendervorlage auf ein Projekt anwenden, um den Projektzeitplan zu verfolgen.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e195cdb0dc5acc2ea816fadce40811675a855de2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933537"
---
# <a name="define-project-calendars"></a>Projektkalender definieren

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

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
3. Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](/dynamics365/field-service/set-work-hours-resource) um die Kalenderregeln zu konfigurieren.

**Erstellen einer neuen Kalendervorlage.**

1. Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.
2. Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.

> [!NOTE]
> Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet. Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.

Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

