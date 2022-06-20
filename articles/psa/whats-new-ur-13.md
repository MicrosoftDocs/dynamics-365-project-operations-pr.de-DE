---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 13, V3
description: Dieser Artikel informiert Sie über die Neuerungen in der Project Service Automation Updateversion 13, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930685"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation Update Release 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Dynamics 365 Project Service Automation (PSA) Anwendung bekanntzugeben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, besuchen Sie das Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 13, neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V3.10.3.18 und ist nach folgendem Zeitplan verfügbar:

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




[!INCLUDE[footer-include](../includes/footer-banner.md)]
