---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 17, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 17, V3, verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915689"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation Update Release 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit.  Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für PSA V3, Updateversion 17, neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V3.10.6.34 und ist durch eine Selbstaktualisierung im März 2020 verfügbar.


## <a name="update-release-17"></a>Update Release 17

### <a name="bug-fixes"></a>Bugfixes

**Allgemein**

- Behoben: Aktualisieren Sie Project Service Automation, um Team Member-Lizenzen durchzusetzen (Project Resource Hub enthält die Metadaten für den Team Member Service-Plan 3.x).
 
**Zeit und Ausgaben**

- Behoben: Es ist nicht möglich, eine Kostenvorkalkulation von einem Preis ungleich Null auf Null (0) zu ändern. Die Änderung wird ignoriert.

**Projektmanagement**

- Behoben: Eine Prüfung auf Nullwerte wurde zum Positionsnamen eines Teammitglieds hinzugefügt.
- Behoben: Das Feld **msdyn_userresourceid** in der Entität **msdyn_resourceassignment** ist veraltet.
- Behoben: Das Upgrade von 2.x auf 3.x behandelt jetzt leere Aufwandskonturen bei Aufgabenzuweisungen.

**Vertrieb**

- Behoben: **Invoice.PreValidateInvoiceUpdate** behandelt jetzt das Szenario der ordnungsgemäßen Neuzuweisung von Datensatzbesitzern.
- Behoben: Wenn die Transaktionsklasse **Zeit** ist, kann **UnitGroup** nicht für alle Entitäten bearbeitet werden, einschließlich, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** und **ContractLineDetails**. Jedoch ist das Feld **Einheit** nur für **JournalLine** und **InvoiceLineDetails** nicht bearbeitbar.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
