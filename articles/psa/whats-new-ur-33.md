---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3
description: In diesem Thema sind die verfügbaren Funktionen und Fehlerbehebungen für Project Service Automation Update Release 33, V3 aufgeführt.
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
ms.openlocfilehash: 063290526c25e7073137fc88408be6a61d2d20ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601477"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

In diesem Thema sind die neuen oder geänderten Funktionen und Fehlerbehebungen für Project Service Automation V3, Update Release 33 aufgeführt. Diese Version hat die Build-Nummer V3.10.54.98 und ist allgemein über ein Self-Update im Juli 2021 verfügbar.

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
