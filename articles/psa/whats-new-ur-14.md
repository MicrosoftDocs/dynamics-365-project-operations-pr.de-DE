---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 14, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Update Release 14, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: b811bf7ccfb626e6944801dffa943d2afab0c5e8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124817"
---
# <a name="project-service-automation-update-release-14-v3"></a>Project Service Automation Update Release 14, V3
Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für PSA V3, Update Release 14 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.4.21 und ist nach folgendem Zeitplan verfügbar:

- **Allgemeine Verfügbarkeit (Selbstaktualisierung):** Januar 2020
- **Automatischer Update:** Februar 2020

## <a name="update-release-14"></a>Update Release 14

### <a name="enhancements"></a>Verbesserungen

- Sales

     - Benutzerdefinierte Feldwerte von **Angebot Zeilendetails** werden kopiert nach **Projektvertragspositionsdetails**, wenn ein Angebot aktualisiert wird auf **Wie gewonnen geschlossen**.
     - Bestätigte Projekte können **Als verloren geschlossen** sein.

- Ressourcenverwaltung

     - Beim Erweitern von Buchungen werden Benutzer in einem Bestätigungsdialogfeld aufgefordert, die Buchungsergebnisse zusammenzufassen und einen Link zum Verwalten von Buchungen bereitzustellen.


### <a name="bug-fixes"></a>Bugfixes

- Zeit und Ausgaben

     - Behoben: Verbesserte Benutzererfahrung, wenn der Benutzer keine zu korrigierenden Einträge ausgewählt hat.

- Ressourcenverwaltung

     - Behoben: Das mehrfache Buchen einer Ressource überläuft den Namen der buchbaren Ressource.

- Sales

     - Behoben: Der Gesamtverkaufspreis wird erst berechnet, wenn der Benutzer auch einen Selbstkostenpreis für Kostenvoranschläge für ein Projekt eingibt.
     - Behoben: Schließen eines Zitats als **Gewonnen** schlägt fehl, wenn der zugehörige Projektvertrag nicht im **Entwurf** Zustand ist.

