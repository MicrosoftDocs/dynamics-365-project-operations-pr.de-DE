---
title: Projektvertriebsaufträge für Zeit- und Materialprojekte
description: In diesem Thema wird erläutert, wie projektbasierte Kundenaufträge für Zeit- und Materialprojekte erstellt werden.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716484"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektvertriebsaufträge für Zeit- und Materialprojekte

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie Sie einen Vertriebsauftrag für ein Projekt erstellen. Vertriebsaufträge können nur für Projekte vom Typ **Zeit und Material** erstellt werden.

Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag enthält, müssen Sie die Option aktivieren Parameter **Vertriebsaufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**. 

> [!NOTE]
> - Die Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist ab Anwendungsversion 10.0.2 und höher verfügbar.
> - Der Parameter zum Aktivieren der Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen wird in der Release-Welle vom April 2020 entfernt. Danach wird die Funktionalität immer aktiviert.

Sie können projektbasierte Kundenaufträge auf zwei Arten erstellen:

- Gehen Sie zum Projekt selber. Wählen Sie im Aktionsbereich **Verwalten > Artikelaufgabe > Vertriebsauftrag** aus. Die Projektinformationen beziehen sich standardmäßig auf den Kundenauftrag aus dem Projekt. Wenn der Projektvertrag mehr als eine Finanzierungsquelle enthält, müssen Sie die Finanzierungsquelle auswählen, um den Kunden für den Kundenauftrag festzulegen. Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Kunde automatisch festgelegt.
- Gehen Sie zu Listenseite **Alle Vertriebsaufträge** und erstellen Sie einen neuen Vertriebsauftrag. Sie müssen das Projekt für den Vertriebsauftrag auswählen. Nachdem das Projekt ausgewählt wurde, wird der Kunde aus der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen enthält.

