---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 13, V3
description: Diese Thema enthält Informationen zu den Neuerungen in Project Service Automation Release 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147247"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation Update Release 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 13 aufgeführt. Diese Version hat eine Build-Nummer von V3.10.3.18 und ist nach folgendem Zeitplan verfügbar:

- **Allgemeine Verfügbarkeit (Selbstaktualisierung):** November 2019
- **Automatischer Update:** Dezember 2019


## <a name="update-release-13"></a>Update Release 13 

### <a name="bug-fixes"></a>Bugfixes

- Zeit und Ausgaben

     - Behoben: Suchfunktion auf der **Kostenfreigabe** Seite funktioniert nicht bei Suche nach Spesenzweck.

- Ressourcenverwaltung

     - Behoben: Zahlen in der Abstimmung wurden aktualisiert, um die richtige Ausrichtung zu gewährleisten.
     - Behoben: Benannte Ressourcen können Aufgaben nicht über die Registerkarte **Zeitplan** zugewiesen werden.

- Projektmanagement

     - Behoben: Null-Referenz-Ausnahme beim Zuweisen von Teammitgliedern, wenn dem **Art der Transaktion** Setup-Informationen für **Einheit** und **DefaultGroup** fehlt.

- Sales

     - Behoben: Doppelte Transaktionstypdatensätze geben einen Fehler zurück, wenn Rollenpreisdatensätze erstellt werden.
     - Behoben: Zusätzliche Schaltflächen für **Neue Verkaufschance**, **Angebot**, **Auftragsposition** und **Produkt hinzufügen** werden in Befehlen für Verkaufschancen, Angebote, Bestellprodukte und projektbasierte Zeilenunterraster angezeigt.


