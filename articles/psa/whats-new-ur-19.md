---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 19, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 19, V3, verfügbar sind.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: a17275220eec726107e8ce5f82bdf5cdd403033e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915505"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation Update Release 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, das neueste Update für die Project Service Automation-Anwendung für Dynamics 365 bekannt zu geben. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Diese Version ist mit Dynamics 365 9.x kompatibel. Um auf diese Version zu aktualisieren, wechseln Sie zum Admin Center für Dynamics 365 online, und rufen Sie die Lösungsseite auf, um das Update zu installieren. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in PSA V3, Updateversion 19, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.30.41 und ist allgemein über ein Selbstupdate im Mail 2020 verfügbar.

## <a name="update-release-19"></a>Update Release 19

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben: 

- Fehler, die aus Zeiteintragsimporten stammen, werden nicht korrekt angezeigt.
- Das Zeiteintragsraster unterstützt das Verhalten des Felds **Nur Datum** nicht.
- Projektressourcen können keine Ausgaben mit einem Projekt erstellen.

**Projektmanagement**

Die folgenden Probleme wurden behoben: 

-  Um zwei Ebenen untergeordnete Aufgabe verursacht eine falsche Aufwandsschätzung während der Abschlussberechnung (BK).

**Vertrieb**

Die folgenden Probleme wurden behoben: 

- Die Aktion **Neu berechnen** funktioniert nicht mit Details zu Ausgabenvertragszeilen oder Angebotszeilen.
- **Preise aktualisieren** fehlt für Ausgabenschätzungen.
-  Kunden können keine benutzerdefinierten Vertragsstatusgründe auf der Seite **Projektvertrag** auswählen.
- Kunden können beim Erstellen einer benutzerdefinierten Preisliste aus einem Angebot eine Leistungsverschlechterung feststellen.
- Kunden erleben Inkonsistenzen bei Standardeinstellungen für **Einheit** auf den Seiten **Detailinformationen zur Angebotsposition** und **Vertragszeile Details**.
- Wenn nicht fakturierbare Transaktionskategorieartikel einer fakturierbaren Vertragszeile hinzugefügt werden, wird der Fakturierungstyp **Nicht fakturierbar** der Transaktionskategorie nicht beachtet.
- Kunden können die neu hinzugefügten Rollen und Kategorien nicht für zuvor erstellte Verträge verwenden.
- Kunden erleben Leistungsverschlechterungen. Unnötige Abrufe in PreValidateProjectTeamMemberUpdate.cs
- Rollen, die in der Liste **Ressourcenkategorien** als nicht fakturierbar festgelegt sind, sollten der Registerkarte **Fakturierbare Rollen** als **Nicht fakturierbar** in der Vertragszeile für ein Projekt hinzugefügt werden.
- Kunden können beim Erstellen eines Projekts eine Leistungsminderung feststellen, weil **GetBookableResourceIdFromUser** alle Spalten buchbarer Ressourcen und nicht nur die primäre ID abruft.
- Der Entität **TransactionType** fehlt das Plug-In zur Updatevorüberprüfung, das verhindert, dass Benutzer **Einheiten** und **Einheitengruppen** eingeben, die für Transaktionstypen nicht gültig sind.
- Der Schritt **Entfernen** funktioniert nicht beim Zeiteintragsimport.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
