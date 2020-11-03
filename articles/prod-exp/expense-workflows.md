---
title: Workflows für die Ausgabenverwaltung einrichten
description: Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076678"
---
# <a name="set-up-expense-management-workflows"></a>Workflows für die Ausgabenverwaltung einrichten

[!include [banner](../includes/banner.md)]

Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden. Zu den Belegen, für die Workflows definiert werden können, zählen Spesenabrechnungen, Reiseanforderungen und Vorauszahlungsanforderungen.

Ein Workflow repräsentiert einen Geschäftsprozess. Er definiert, wie ein Beleg durch das System geleitet wird, und zeigt an, wer eine Aufgabe ausführen oder einen Beleg genehmigen muss. Die Verwendung des Workflow-Systems in Ihrer Organisation bietet mehrere Vorteile:

-   **Konsistente Prozesse** – Sie können den Genehmigungsprozess für bestimmte Belege wie Bestellanforderungen und Spesenabrechnungen definieren. Die Nutzung des Workflowsystems hilft, dass Belege auf konsistente und effiziente Weise verarbeitet und genehmigt werden.

-   Prozesstransparenz – Sie können den Status, den Verlauf und die Leistungsmetriken einer bestimmten Workflowinstanz verfolgen. Dies hilft Ihnen zu bestimmen, ob Änderungen am Workflow vorgenommen werden sollten, um die Effizienz zu verbessern.

-   Zentralisierte Arbeitsliste – Benutzer können eine zentralisierte Arbeitsliste anzeigen, um die ihnen zugewiesenen Workflowaufgaben und Genehmigungen zu sehen. 

**Die Arten von Workflows, die Sie erstellen können**

Die folgende Tabelle enthält die Workflow-Typen, die Sie in **Ausgaben** erstellen können.


|              <strong>Typ</strong>              |                   <strong>Verwenden Sie diesen Typ, um</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Ausgabenbericht</strong>         |            Erstellen Sie Genehmigungsworkflows für Spesenabrechnungen.             |
|  <strong>Automatische Ausgabenabrechnungen buchen</strong>   |        Buchen Sie automatisch Workflows für Ausgabenabrechnungen.        |
|       <strong>Ausgabenzeilenelement</strong>        |     Erstellen Sie Genehmigungsworkflows für Ausgabenabrechnungen.      |
| <strong>Automatische Buchung von Ausgaben</strong> | Erstellen Sie automatische Buchungsworkflows für Ausgabenabrechnungen. |
|       <strong>Reiseanforderung</strong>       |          Erstellen Sie Genehmigungsworkflows für Reiseanforderungen.           |
|      <strong>Vorauskassenanfrage</strong>      |         Erstellen Sie Genehmigungsworkflows für Vorauszahlungsanfragen.          |
|        <strong>MWsT-Rückforderung</strong>        | Erstellen Sie Genehmigungsworkflows für die Erstattung der Mehrwertsteuer (MWsT).  |

