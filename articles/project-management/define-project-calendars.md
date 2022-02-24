---
title: Projektkalender definieren
description: Dieses Thema enthält Informationen zum Anwenden einer Kalendervorlage auf ein Projekt, um den Projektplan zu verfolgen.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981299"
---
# <a name="define-project-calendars"></a>Projektkalender definieren

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Um ein Projekt zu erstellen und zu verwalten, müssen Sie eine Kalendervorlage auf das Projekt anwenden. Die Kalendervorlage definiert die folgenden Projektattribute:

- Arbeitszeit einschließlich Start- und Endzeit
- Arbeitstage
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
3. Wählen Sie die Registerkarte **Arbeitsstunden** der Ressource und vervollständigen Sie die Anweisungen in [Arbeitszeiten für eine Ressource festlegen](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) um die Kalenderregeln zu konfigurieren.

**Erstellen einer neuen Kalendervorlage.**

1. Wechseln Sie zu **Einstellungen** \> **Kalendervorlage**.
2. Wählen Sie **Neu** und geben Sie einen Namen, eine Beschreibung und eine Vorlagenressource ein.

> [!NOTE]
> Wenn in einer Kalendervorlage auf eine Ressource verwiesen wird, wird der Kalendervorlage eine Kopie des Kalenders der Ressource zugeordnet. Wenn die Arbeitszeiten der kopierten Vorlage sich ändern, werden diese Änderungen nicht auf die Kalendervoralge übertragen.

Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

