---
title: Neuigkeiten und Änderungen in Project Service Automation, Update Release 39, V3
description: Dieser Artikel listet die Funktionen und Korrekturen auf, die in Microsoft Dynamics 365 Project Service Automation Updateversion 39, V3, zur Verfügung stehen.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922451"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Neuigkeiten und Änderungen in Project Service Automation, Update Release 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Wir freuen uns, die neueste Aktualisierung für die Microsoft Dynamics 365 Project Service Automation App anzukündigen. Diese Version enthält einige wichtige Verbesserungen in Bezug auf Qualität, Leistung und Benutzerfreundlichkeit. Es ist kompatibel mit Dynamics 365 9.x. Um auf diese Version zu aktualisieren, besuchen Sie die Seite Admin Center für Dynamics 365-Onlinelösungen und installieren Sie das Update. Weitere Informationen: [Installieren, Aktualisieren oder Entfernen einer bevorzugten Lösung](/power-platform/admin/install-remove-preferred-solution).

Dieser Artikel listet die Funktionen und Korrekturen auf, die in der Project Service Automation Updateversion 39, V3, neu sind oder geändert wurden. Diese Version hat eine Build-Nummer von V3.10.60.170 und ist im durch ein Selbst-Update im Januar 2022 verfügbar.

## <a name="update-release-39"></a>Update Release 39

### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Probleme wurden behoben.

**Allgemein**

- An der Sitemap für die arabische Übersetzung wurden mehrere Verbesserungen vorgenommen.

**Projektmanagement**

- Ein Fehler tritt auf, wenn Sie den Projektmanager eines Projekts zu einem Benutzer ändern, der bereits Teammitglied des Projekts ist.

**Vertrieb**

- Der Besitzer der **Projektvertragspreisliste** ist falsch, wenn die Preisliste automatisch erstellt wird. 
- Die Datumsgültigkeit einer Preisliste wird nicht berücksichtigt, wenn die Preisliste auf den Projektparameter angewendet wird.
- Die Vertragseinheit hat möglicherweise nicht den korrekten Standardwert, wenn zwei separate Angebote bearbeitet werden.
