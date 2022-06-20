---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 33, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915415"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die für Project Service Automation V3, Updateversion 33, neu sind oder geändert wurden. Diese Version hat die Build-Nummer V3.10.54.98 und ist allgemein über ein Self-Update im Juli 2021 verfügbar.

## <a name="update-release-33"></a>Update Release 33

### <a name="bug-fixes"></a>Fehlerkorrekturen

**Zeit und Ausgaben**

Die folgenden Probleme wurden behoben:

- Zwei gesperrte Felder, **msdyn_description** und **msdyn_externaldescription** sind nach dem Absenden editierbar.
- Es erscheint eine Fehlermeldung, wenn eine Leistung erstellt wird, die nicht mit einem Projekt verbunden ist.
- Wenn ein Zeiteintrag erstellt wird, wird die Ressourcenrolle standardmäßig auf eine inaktive Rolle gesetzt.
- Erfassungszeilen, die mit einer zurückgerufenen und gelöschten Leistung verbunden sind, werden nicht gelöscht.
- Aktualisieren Sie auf dem **Formular zum schnellen Erstellen von Zeiteinträgen** die Ansicht **Projektaufgabenliste**, um das standardmäßig angezeigte Datum auf das Startdatum der Aufgabe zu ändern.
- Wenn Sie einen Zeiteintrag über die Registerkarte **Bezogen** der buchbaren Ressource erstellen, wird der Zeiteintrag fälschlicherweise für den angemeldeten Benutzer erstellt und nicht für die übergeordnete buchbare Ressource.
- Dem Dialogfeld **Gesamtgenehmigung MDD** wurden neue Felder hinzugefügt.

**Projektplanung**

Die folgenden Probleme wurden behoben:
- Langsame Leistung bei der Projekterstellung, wenn Projektarbeitsstundenvorlagen mit komplexen Kalendern angewendet werden.
- Wenn das Startdatum größer als das Enddatum ist, wird in der Projektvorlage zum Kopieren ein Fehler angezeigt, da die Zeitkomponente der einzelnen Felder unterschiedlich ist.

**Ressourcenverwaltung**

Die folgenden Probleme wurden behoben:
- Ein falscher Parameter wird in der Abfrage der Ressourcenauslastung verwendet und die XML führt zu falschen Filterergebnissen im **Ressourcenauslastung** Raster.
- Die Bestätigung **Buchungen verlängern** zeigt ein falsches Enddatum für Buchungen an.

**Vertrieb**

Die folgenden Probleme wurden behoben:
- Es tritt eine Fehlermeldung auf, wenn eine Kategorie Preis mit fehlenden Werten erstellt wird.
- Es tritt eine Fehlermeldung auf, wenn ein Meilenstein für eine Vertragszeile ohne eine Auftragszeile erstellt wird.
