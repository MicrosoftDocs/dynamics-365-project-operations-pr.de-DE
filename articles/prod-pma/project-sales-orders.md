---
title: Projektvertriebsaufträge für Zeit- und Materialprojekte
description: In diesem Thema wird erläutert, wie projektbasierte Kundenaufträge für Zeit- und Materialprojekte erstellt werden.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009660"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektvertriebsaufträge für Zeit- und Materialprojekte

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie einen Vertriebsauftrag für ein Projekt erstellen. Vertriebsaufträge können nur für Projekte vom Typ **Zeit und Material** erstellt werden.

Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag enthält, müssen Sie die Option aktivieren Parameter **Vertriebsaufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**. 

> [!NOTE]
> - Die Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist ab Anwendungsversion 10.0.2 und höher verfügbar.
> - Der Parameter zum Aktivieren der Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen wird in der Release-Welle vom April 2020 entfernt. Danach wird die Funktionalität immer aktiviert.

Sie können projektbasierte Kundenaufträge auf zwei Arten erstellen:

- Gehen Sie zum Projekt selber. Wählen Sie im Aktionsbereich **Verwalten > Artikelaufgabe > Vertriebsauftrag** aus. Die Projektinformationen beziehen sich standardmäßig auf den Kundenauftrag aus dem Projekt. Wenn der Projektvertrag mehr als eine Finanzierungsquelle enthält, müssen Sie die Finanzierungsquelle auswählen, um den Kunden für den Kundenauftrag festzulegen. Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Kunde automatisch festgelegt.
- Gehen Sie zu Listenseite **Alle Vertriebsaufträge** und erstellen Sie einen neuen Vertriebsauftrag. Sie müssen das Projekt für den Vertriebsauftrag auswählen. Nachdem das Projekt ausgewählt wurde, wird der Kunde aus der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen enthält.



[!INCLUDE[footer-include](../includes/footer-banner.md)]