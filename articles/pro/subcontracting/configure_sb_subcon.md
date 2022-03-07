---
title: Zeitplanübersicht konfigurieren für die Anzeige von Vertragsmitarbeitern und Fremdarbeitskapazität
description: In diesem Thema wird beschrieben, wie Sie die Zeitplanübersicht in Microsoft Dynamics 365 Project Operations konfigurieren, um die Ressourcenkapazität für Fremdarbeit bei den Anforderungen zur Besetzung von Projektressourcen anzuzeigen.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902865"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Zeitplanübersicht konfigurieren für die Anzeige von Vertragsmitarbeitern und Fremdarbeitskapazität 

[!include [banner](../../includes/dataverse-preview.md)]

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Die Zeitplanübersich in Microsoft Dynamics 365 Project Operations kann auf zwei Arten für die Suche nach Ressourcen verwendet werden:

- Allgemeine Ressourcensuche ohne den Kontext einer spezifischen projektbasierten Ressourcenanforderung.
- Anforderungsspezifische Ressourcensuche, bei der die Projektanforderung den Kontext für die vorgeschlagenen Ressourcen bereitstellt.

Um die Zeitplanübersicht zur Ressourcenkapazität für Fremdarbeit und Vertragsmitarbeiter zu benachrichtigen, müssen Sie die Einstellungen für die Zeitplanübersicht aktualisieren. Diese Aktualisierungen umfassen: 
- Aktualisieren der Zeitplanübersicht-Einstellungen für die allgemeine Ressourcensuche.
- Aktualisieren der Zeitplanübersicht-Einstellungen für die anforderungsbasierte Ressourcensuche.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aktualisieren der Zeitplanübersicht-Einstellungen für die allgemeine Ressourcensuche
### <a name="update-filters-for-general-resource-search"></a>Filter für die allgemeine Ressourcensuche aktualisieren
Wenn Sie nach einer Ressource suchen, sollten die in der Zeitplanübersicht verfügbaren Filter aktualisiert werden, damit Sie auch nach externen Ressourcen suchen können, indem Sie eine oder alle der folgenden Optionen angeben:
  - Arbeitertyp, ob es sich bei den angezeigten Ressourcen um Vertragsmitarbeiter oder Angestellte handeln soll.
  - Zuliefererunternehmen, zu dem eine Ressource gehören soll.
  - Ressourcen, die zu einer bestimmten Fremdarbeit oder einer bestimmten Fremdarbeitsposition gehören.
    
### <a name="update-retrieve-resource-query"></a>Abfrage „Ressource abrufen“ aktualisieren
Die für die Suche verwendete Abfrage sollte ebenfalls aktualisiert werden, um diese zusätzlichen Filterattribute zu verwenden. Führen Sie die folgenden Schritte aus, um die Zeitplanübersicht-Konfiguration für die allgemeine Ressourcensuche zu aktualisieren:  
1. Öffnen Sie **Zeitplanübersicht-Einstellungen** für eine bestimmte Zeitplanübersicht.
2. Öffnen Sie den **Allgemeine Einstellungen**-Tab und scrollen Sie zu **Andere Einstellungen**.
3. Aktualisieren Sie in der Liste der Einstellungen in diesem Abschnitt das **Filterlayout** zu **Standardmäßiges Filterlayout für Project Operations Lite**.
4. Aktualisieren Sie **Abfrage „Ressource abrufen“** zu **Standardabfrage zum Abrufen von Ressourcen für Project Operations Lite**.

![Aktualisieren der Zeitplanübersicht-Einstellungen für die allgemeine Ressourcensuche](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aktualisieren der Zeitplanübersicht-Einstellungen für die anforderungsbasierte Ressourcensuche
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filter für die anforderungsspezifische Ressourcensuche aktualisieren 
Wenn Sie nach einer Ressource suchen, sollten die in der Zeitplanübersicht verfügbaren Filter aktualisiert werden, damit Sie auch nach externen Ressourcen suchen können, indem Sie eine oder alle der folgenden Optionen angeben:
 - Arbeitertyp, ob es sich bei den angezeigten Ressourcen um Vertragsmitarbeiter oder Angestellte handeln soll.
 - Zuliefererunternehmen, zu dem eine Ressource gehören soll.
 - Ressourcen, die zu einer bestimmten Fremdarbeit oder einer bestimmten Fremdarbeitsposition gehören.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Abfrage „Ressource abrufen“ für anforderungsspezifische Ressourcensuche aktualisieren 
Die für die Suche verwendete Abfrage sollte ebenfalls aktualisiert werden, um diese zusätzlichen Filterattribute zu verwenden. Führen Sie die folgenden Schritte aus, um die Zeitplanübersicht-Konfiguration für die anforderungsbasierte Ressourcensuche zu aktualisieren:

1. Öffnen Sie **Zeitplanübersicht-Einstellungen** für eine bestimmte Zeitplanübersicht und wählen Sie dann **Standardeinstellungen öffnen**, um die Einstellungen für die anforderungsspezifische Suche zu öffnen.
2. Öffnen Sie den **Allgemeine Einstellungen**-Tab und scrollen Sie zu **Andere Einstellungen**.
3. Aktualisieren Sie in der Liste der Einstellungen in diesem Abschnitt das **Filterlayout** zu **Standardmäßiges Filterlayout für Project Operations Lite**.
4. Aktualisieren Sie **Abfrage „Ressource abrufen“** zu **Standardabfrage zum Abrufen von Ressourcen für Project Operations Lite**.
5. Öffnen Sie den **Zeitplantypen**-Tab und gehen Sie zu **Projekt**.
6. Unter den Einstellungen für **Projekt**, aktualisieren Sie **Abfrage „Ressourcen abrufen“ des Zeitplan-Assistenten** zu **Standardabfrage zum Abrufen von Ressourcen für Project Operations Lite** und aktualisieren Sie **Abfrage „Einschränkungen abrufen“ des Zeitplan-Assistenten** zu **Standardabfrage zum Abrufen von Einschränkungen für Project Operations Lite**.

![Aktualisieren der Zeitplanübersicht-Einstellungen für die anforderungsbasierte Ressourcensuche](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
