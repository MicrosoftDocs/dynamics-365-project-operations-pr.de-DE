---
title: Eine Projektvorkalkulation entfernen
description: Dieses Thema enthält Informationen zum Entfernen einer Projektkalkulation nach deren Abschluss.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006915"
---
# <a name="eliminate-a-project-estimate"></a>Eine Projektvorkalkulation entfernen

[!include [banner](../includes/banner.md)]

Projektvorkalkulationen stellen die Finanzansicht für die Arbeit bereit, die für ein Projekt geschätzt und geplant wird. Um mit Vorkalkulationen für ein Projekt arbeiten zu können, müssen Sie das Projekt an ein Vorkalkulationsprojekt anhängen. Ein Vorkalkulationsprojekt basiert immer auf einem vorhandenen Projekt. Mehrere Projekte können sich jedoch auf ein einzelnes Vorkalkulationsprojekt beziehen. An Vorkalkulationsprojekte können nur Festpreis- und Investitionsprojekte angehängt werden, und diese Projekte müssen zur selben Projektgruppe gehören wie das Vorkalkulationsprojekt.

Um ein Vorkalkulationsprojekt zu löschen, muss es vollständig sein. In den folgenden Schritten wird erläutert, wie Sie eine Vorkalkulation entfernen.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung** > **All Projekte**, und öffnen Sie das Projekt. 
2. Wählen Sie auf der Registerkarte **Verwalten** **Vorkalkulationen** und auf der Seite **Schätzung** die Option **Entfernen** aus.
3. Legen Sie auf der Seite **Vorkalkulation löschen** auf der Registerkarte **Allgemein** die folgenden Optionen fest:

   - **Periodencode**: Wählen Sie den Periodencode aus, um die entsprechenden Vorkalkulationsprojekte auszuwählen. 
   - **Vorkalkulationsdatum**: Wählen Sie das geeignete Vorkalkulationsdatum für das Entfernen aus.
   - **Mit WIP-Warnungen löschen**: Aktivieren Sie diese Option, um eine Benachrichtigung bereitzustellen, wenn eine Vorkalkulation, die mit einem WIP (Work in Progress) verknüpft ist, entfernt wird. Wenn diese Option nicht aktiviert ist, kann das Entfernen nicht fortgesetzt werden, wenn nicht geschätzte Transaktionen vorhanden sind. 
   > [!NOTE]
   > Diese Option ist nur verfügbar, wenn das Entfernen auf ein Vorkalkulationsprojekt angewendet wird. Es ist nicht verfügbar, wenn Sie regelmäßige Buchungen verwenden. Diese Einstellung funktioniert mit den Einstellungen auf der Registerkarte **Schätzung** auf der Seite **Projektparameter** in der Feldgruppe **Löschung bei nicht vorkalkulierten Buchungen zulassen**.
   - **Phase als 'abgeschlossen' festlegen**: Aktivieren Sie diese Option, um die Phase des Vorkalkulationsprojekts als **Abgeschlossen** festzulegen, nachdem Sie das Entfernen ausgeführt haben.
   - **Vorkalkulationsliste drucken**: Wählen Sie die Informationen aus, die beim Drucken der Vorkalkulationsliste berücksichtigt werden sollen.
   - **Infolog anzeigen**: Aktivieren Sie diese Option, um das Infolog anzuzeigen.
   - **Buchungsdatum**: Wählen Sie das Buchungsdatum der Finanzbuchhaltung für die Vorkalkulation ein.

4.  Klicken Sie auf **OK**.
5. Nach Abschluss des Entfernungsprozesses wird das entfernte Vorkalkulationsprojekt mit einem negativen Wert angezeigt. 

Wenn das Entfernen der Vorkalkulation nicht beabsichtigt war, können Sie die entfernte Vorkalkulation und dann **Entfernen stornieren** auswählen.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]