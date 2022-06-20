---
title: Projektvertriebsaufträge für Zeit- und Materialprojekte
description: Dieser Artikel erklärt, wie Sie projektbezogene Verkaufsaufträge für Zeit- und Materialprojekte erstellen.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3a040de6d22b626b9e3d462272f43c5763b5b90f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933813"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektvertriebsaufträge für Zeit- und Materialprojekte

[!include[banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie einen Verkaufsauftrag für ein Projekt erstellen. Vertriebsaufträge können nur für Projekte vom Typ **Zeit und Material** erstellt werden.

Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag enthält, müssen Sie die Option aktivieren Parameter **Vertriebsaufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement- und Buchhaltungsparameter**. 

> [!NOTE]
> - Die Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist ab Anwendungsversion 10.0.2 und höher verfügbar.
> - Der Parameter zum Aktivieren der Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen wird in der Release-Welle vom April 2020 entfernt. Danach wird die Funktionalität immer aktiviert.

Sie können projektbasierte Kundenaufträge auf zwei Arten erstellen:

- Gehen Sie zum Projekt selber. Wählen Sie im Aktionsbereich **Verwalten > Artikelaufgabe > Vertriebsauftrag** aus. Die Projektinformationen beziehen sich standardmäßig auf den Kundenauftrag aus dem Projekt. Wenn der Projektvertrag mehr als eine Finanzierungsquelle enthält, müssen Sie die Finanzierungsquelle auswählen, um den Kunden für den Kundenauftrag festzulegen. Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Kunde automatisch festgelegt.
- Gehen Sie zu Listenseite **Alle Vertriebsaufträge** und erstellen Sie einen neuen Vertriebsauftrag. Sie müssen das Projekt für den Vertriebsauftrag auswählen. Nachdem das Projekt ausgewählt wurde, wird der Kunde aus der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen enthält.



[!INCLUDE[footer-include](../includes/footer-banner.md)]