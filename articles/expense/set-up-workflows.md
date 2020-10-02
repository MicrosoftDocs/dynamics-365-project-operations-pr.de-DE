---
title: Richten Sie Workflows für die Ausgabenverwaltung ein
description: Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896550"
---
# <a name="set-up-workflows-for-expense-management"></a>Richten Sie Workflows für die Ausgabenverwaltung ein

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie können einen Workflow-Prozess einrichten, mit dem Reise- und Ausgabenabrechnungen überprüft und genehmigt werden. Sie können Workflows für Ausgabenabrechnungen, Reiseanforderungen und Vorauszahlungen definieren.

Ein Workflow stellt einen Geschäftsprozess dar und definiert, wie ein Dokument durch das System fließt. Der Workflow gibt auch an, wer eine Aufgabe ausführen oder ein Dokument genehmigen muss. Die Verwendung des Workflow-Systems in Ihrer Organisation bietet mehrere Vorteile:

- **Konsistente Prozesse**: Sie können den Genehmigungsprozess für bestimmte Dokumente wie Bestellanforderungen und Spesenabrechnungen definieren. Die Nutzung des Workflowsystems hiflt, dass Dokumente auf konsistente und effiziente Weise verarbeitet und genehmigt werden.
- **Prozesstransparenz**: Sie können den Status, den Verlauf und die Leistungsmetriken einer bestimmten Workflowinstanz verfolgen. Dies hilft Ihnen zu bestimmen, ob Änderungen am Workflow vorgenommen werden sollten, um die Effizienz zu verbessern.
- **Zentralisierte Arbeitsliste**: Benutzer können eine zentralisierte Arbeitsliste anzeigen, um die ihnen zugewiesenen Workflowaufgaben und Genehmigungen zu sehen. 

## <a name="workflow-types"></a>Workflowregeln

Die folgende Tabelle enthält die Workflow-Typen, die Sie in der **Ausgabenverwaltung** erstellen können.


|              <strong>Typ</strong>              |                   <strong>Verwenden Sie diesen Typ, um</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Ausgabenberichte automatisch genehmigen</strong> |            Erstellen Sie Genehmigungsworkflows für Spesenabrechnungen.             |
|  <strong>Automatische Ausgabenabrechnungen buchen</strong>   |        Buchen Sie automatisch Workflows für Ausgabenabrechnungen.        |
|       <strong>Ausgabenzeilenelement</strong>        |     Erstellen Sie Genehmigungsworkflows für Ausgabenabrechnungen.      |
| <strong>Automatische Buchung von Ausgaben</strong> | Erstellen Sie automatische Buchungsworkflows für Ausgabenabrechnungen. |
|       <strong>Reiseanforderung</strong>       |          Erstellen Sie Genehmigungsworkflows für Reiseanforderungen.           |
|      <strong>Vorauskassenanfrage</strong>      |         Erstellen Sie Genehmigungsworkflows für Vorauszahlungsanfragen.          |
|        <strong>MWsT-Rückforderung</strong>        | Erstellen Sie Genehmigungsworkflows für die Erstattung der Mehrwertsteuer (MWsT).  |
