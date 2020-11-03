---
title: Projektvorlagen mit Projekt kopieren erstellen
description: Dieses Thema enthält Informationen zum Erstellen von Projektvorlagen mithilfe der benutzerdefinierten Aktion „Projekt kopieren“.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076464"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektvorlagen mit Projekt kopieren erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dynamics 365 Project Operations unterstützt die Möglichkeit, ein Projekt zu kopieren und alle Zuweisungen auf die allgemeinen Ressourcen zurückzusetzen, die die Rolle darstellen. Kunden können diese Funktionalität verwenden, um grundlegende Projektvorlagen zu erstellen.

Wenn Sie **Projekt kopieren** auswählen, wird der Status des Zielprojekts aktualisiert. Verwenden Sie **Statusgrund** , um festzustellen, wann die Kopieraktion abgeschlossen ist. Durch Auswahl von **Projekt kopieren** wird auch das Startdatum des Projekts auf das aktuelle Startdatum aktualisiert, wenn in der Zielprojektentität kein Zieldatum erkannt wird.

## <a name="copy-project-custom-action"></a>Benutzerdefinierte Aktion „Projekt kopieren“ 

### <a name="name"></a>Name des Dataflows 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Eingabeparameter
Es gibt drei Eingabeparameter:

| Parameter          | Art   | Werte                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** oder **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitätsreferenz | Quellprojekt |
| Zielsprache             | Entitätsreferenz | Zielprojekt |


- **{"clearTeamsAndAssignments":true}** : Das Standardverhalten für Project für das Web. Dadurch werden alle Arbeitsaufträge und Teammitglieder entfernt.
- **{"removeNamedResources":true}** Das Standardverhalten für Project Operations, bei dem Zuweisungen zu generischen Ressourcen zurückgesetzt werden.

Weitere Standardinformationen über Aktionen finden Sie unter [Nutzen von Web-API-Aktionen](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions).

## <a name="specify-fields-to-copy"></a>Zu kopierende Felder angeben 
Wenn die Aktion aufgerufen wird, wird mit **Projekt kopieren** die Ansicht **Projektspalten kopieren** betrachtet, um zu bestimmen, welche Felder kopiert werden sollen, wenn das Projekt kopiert wird.
