---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 36, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 36, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924981"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 36, V3, neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V3.10.57.152 und ist im durch ein Selbst-Update im Oktober 2021 verfügbar.

## <a name="update-release-36"></a>Update Release 36

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Allgemein**
- Der Feldname **Standardarbeitszeitvorlage** ist auf der Seite **Projektparameter** falsch übersetzt.
- Asynchrone Plug-Ins behandeln Ausnahmen im Zusammenhang mit **SharedVariableService** nicht korrekt.

**Zeit und Ausgaben**
- Wenn Journalzeilen fehlen oder der Benutzer nicht über die richtigen Berechtigungen zum Lesen von Journalzeilen verfügt, tritt ein falscher Fehler auf, wenn Projektgenehmigungen storniert werden.
- Benutzer können eine Genehmigung nicht stornieren, wenn der Aufwands- oder Zeitbuchung mehr als eine Projektgenehmigung zugeordnet ist.
- **Abwesenheit** und **Ferien** werden bei einer Suche auf der Schnellerfassungsseite **Zeiteingabe** falsch für die chinesische Sprache übersetzt.

**Ressourcenverwaltung**
- Benutzer können nicht nach Ressourcen im **Zeitplan-Assistent** suchen, wenn der Ansichtsmodus auf **Tag**, **Woche**, oder **Monat** eingestellt ist.
- Generische Ressourcen dürfen fälschlicherweise leere Positionsnamen haben. 
- Wenn Sie einen Vertrag als verloren schließen, werden zukünftige Buchungen nicht storniert.

**Vertrieb**
- Wenn eine Umgebung eine große Menge an Produkten enthält, nimmt die Leistung im Netz **Materialschätzung** ab.
- Beim Anlegen eines Projekts aus einer Vorlage wird die Projektwährung nicht standardmäßig auf die Vertragseinheit des jeweiligen Projektleiters eingestellt.
- Die tatsächlichen Beträge stimmen nicht immer mit den fälligen Projektbeträgen überein, oder die Beträge werden in bestimmten Rückrufszenarien negativ.
- Ein Fehler tritt auf, wenn Sie ein Projekt, das aus einer Projektvorlage erstellt wurde, einer Vertragsposition zuordnen.
- Benutzer können eine Vertragszeile mit den Meilensteinen **Bereit zur Rechnung** und **Rechnung erstellt** löschen. Dies sollte nicht erlaubt sein.
- Wenn Kostenvoranschläge aus einem Projekt importiert werden, wird die Detailkostenberechnung der Angebotsposition falsch eingestellt, wenn die aufgabenbasierte Fakturierung für die Angebotsposition aktiviert ist.
- Wenn Sie einen Meilenstein für die Festpreisabrechnung hinzufügen, wird der Meilenstein erst nach der Aktualisierung der Seite im Meilenstein-Unterraster angezeigt.
- Eine Nullverweisausnahme wird generiert, wenn Sie einen Projektvertrag mit einem Angebotsnamen erstellen, der null ist.
- Aufgaben im manuellen Modus, bei denen die Projektwährung von der Währung der Ressource abweicht, führen zu falschen Preisschätzungen.
- Benutzer können eine Transaktion, die durch eine Korrekturrechnung erfolgreich korrigiert wurde, nicht zurückrufen.
- Deaktivierte Transaktionskategorien erscheinen im Netz **Kostenschätzungen**.



