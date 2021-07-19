---
title: Leistung von Projektrechnungsvorschlägen
description: Dieses Thema enthält Informationen zu Leistungsverbesserungen bei Projektrechnungsvorschlägen.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269789"
---
# <a name="project-invoice-proposal-performance"></a>Leistung von Projektrechnungsvorschlägen

[!include [banner](../includes/banner.md)]

Wenn Sie einen neuen Rechnungsvorschlag erstellen, können Leistungsprobleme auftreten, wenn die Anzahl der Projekte und Teilprojekte zunimmt. Um die Leistung zu verbessern, steht eine Funktion zur Verfügung, die den Zeitaufwand für die Erstellung eines neuen Rechnungsvorschlags für gebuchte Projekttransaktionen verkürzt.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Leistungsverbesserung von Projektrechnungsvorschlägen aktivieren
Führen Sie die folgenden Schritte aus, um die Leistungsverbesserungsfunktion für Projektrechnungsvorschläge zu aktivieren.

1.  Gehen Sie zu **Funktionsverwaltung** > **Alle**. Suchen Sie in der Funktionsliste nach **Leistungsverbesserung von Projektrechnungsvorschlägen**.
2.  Wählen Sie **Jetzt aktivieren** aus.
3.  Aktualisieren Sie Ihren Browser und erstellen Sie einen neuen Rechnungsvorschlag.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Leistungsverbesserung von Projektrechnungsvorschlägen deaktivieren
Führen Sie die folgenden Schritte aus, um die Leistungsverbesserungsfunktion für Projektrechnungsvorschläge zu deaktivieren.

1.  Gehen Sie zu **Funktionsverwaltung** > **Alle**. Suchen Sie in der Funktionsliste nach **Leistungsverbesserung von Projektrechnungsvorschlägen**.
2.  Wählen Sie **Deaktivieren**.
3.  Aktualisieren Sie Ihren Browser.

> [!NOTE]
> Die Leistung von Rechnungsvorschlägen kann nicht angewendet werden, wenn Abrechnungsregeln aktiviert sind.
> 
> Während des Batch-Prozesses zum Erstellen von Rechnungsvorschlägen wird die Anzahl der Teilaufgaben auf eine maximale Anzahl basierend auf der Anzahl der Verträge mit abrechenbaren Transaktionen aufgeteilt, unabhängig davon, was Sie eingegeben haben. Wenn Sie z.B. **3** für die Anzahl der Teilaufgaben für die Erstellung von Rechnungsvorschlägen im Batch eingeben und es nur zwei Verträge mit abrechenbaren Transaktionen gibt, werden nur zwei Teilaufgaben erstellt.
