---
title: Was ist neu Juni 2022 - Project Operations Lite-Bereitstellung
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Microsoft Dynamics 365 Project Operations im Juni 2022 verfügbar sind.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031192"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Was ist neu Juni 2022 - Project Operations Lite-Bereitstellung

_**Gilt für:** Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel gilt für die folgenden Komponenten und Versionen von Microsoft Dynamics 365 Project Operations:

- Project Operations in einer Dataverse-Umgebung der Versionen 4.43.0.77 oder 4.43.0.119

## <a name="quality-updates"></a>Qualitätsupdates

| Funktionsbereich | Referenznummer | Qualitätsupdate |
| --- | --- | --- |
| Fremdarbeit | 2708885 | Die Fehlermeldung, die angezeigt wird, wenn ein Benutzer einen Datensatz für den Buchungskopf einer buchbaren Ressource erstellt, in dem keine buchbare Ressource eingetragen ist, wurde behoben. |
| Projektplanung und -nachverfolgung | 2629441 | Die Logik zum Auslösen von Workflows wurde korrigiert, um eine Endlosschleife zu verhindern, wenn Projektaufgaben aktualisiert werden. |
| Zeit und Ausgaben | 2641209 | Zeitbuchungsimporte aus Zuweisungen/Buchungen müssen eine buchbare Ressourcenreferenz beibehalten. |
| Projektplanung und -nachverfolgung | 2651148 | Der Projektdokumentenkopf muss geschützt werden.|
| Projektplanung und -nachverfolgung | 2653145 | Es wurden Validierungen hinzugefügt, um sicherzustellen, dass kein Datensatz erstellt werden kann, der nicht gültige Zeichen in seinem Namen enthält. |
| Zeit und Ausgaben | 2654710 | Die Filterung auf der Seite **Genehmigungen** wurde korrigiert. |
| Preise und Abrechnung | 2667805 | Es wurden Validierungen hinzugefügt, um zu verhindern, dass fakturierte Umsätze erstellt werden, wenn noch keine nicht fakturierten Umsätze vorhanden sind. |
| Preise und Abrechnung | 2668378 | Es wurden Validierungen hinzugefügt, um zu verhindern, dass eine angepasste Dimension für die Preisgestaltung hinzugefügt wird, wenn kein logischer Name und kein Feldname eingegeben wird. |
| Zeit und Ausgaben | 2700428 | Die Genehmigungslogik wurde verbessert, um sicherzustellen, dass andere Genehmigungssätze für das Projekt auch dann verarbeitet werden können, wenn einer der Genehmigungssätze in Systemaufträgen festhängt. |
