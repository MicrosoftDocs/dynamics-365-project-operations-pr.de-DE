---
title: Ressourcenkapazität synchronisieren
description: Dieses Thema enthält Informationen zum Synchronisieren der Kapazität einer Ressource über Kalender und Projekte hinweg.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076502"
---
# <a name="synchronize-resource-capacity"></a>Ressourcenkapazität synchronisieren

[!include [banner](../includes/banner.md)]

Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass Informationen für den Kalender und den Basiskalender in die Projektressourcenplanung einfließen. Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen an der Planung der Projektressourcen vor. Die Prozesse tragen auch zur Verbesserung der Leistung bei, da die Ressourceninformationen des Kalenders im Voraus synchronisiert werden. Daher werden Aktualisierungen der Ressourcenzeitplanungsinformationen schneller durchgeführt. Wir empfehlen, dass Sie die Prozesse als Stapel anstatt einzeln planen. Andernfalls besteht die Gefahr, dass jemand die Inklusivdaten vergisst, an denen die Informationen zuletzt synchronisiert wurden. Wenn keine Inklusivdaten verwendet werden, können während der Datumssynchronisierung Lücken auftreten.

![Kalendersynchronisation](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchronisation der Rollup-Kapazität

Der Synchronisierungsprozess dient zum Synchronisieren aller Ressourcenkalenderinformationen. Diese Informationen enthalten Basiskalenderinformationen zu Änderungen an der Kapazitätstabelle des Ressourcenkalenders des Projekts. Wenn dem Projekt neue Ressourcen hinzugefügt werden, stellt die Synchronisierung sicher, dass die aktualisierten Kalenderinformationen verfügbar sind. Diese Synchronisation kann jederzeit durchgeführt werden.

Es wird empfohlen, dass Sie einen Batch verwenden. Die Optionen stehen während der Synchronisierung von Kapazitätsreservierungen zur Verfügung.

1. Wählen Sie **Projektmanagement und Buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisation** &gt; **Synchronisieren Sie Rollups der Ressourcenkapazität**.
2. Legen Sie die Optionen in der nachfolgenden Tabelle fest.

    | Option      | Beschreibung |
    |-------------|-------------|
    | Periodencode | Wählen Sie optional den Intervallcode für das Hauptbuchdatum aus, um das Start- und Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität festzulegen. |
    | Startdatum  | Geben Sie das Startdatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein. |
    | Enddatum    | Geben Sie das Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein. |

[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]