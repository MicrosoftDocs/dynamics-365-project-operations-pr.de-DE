---
title: Ausgabenverwaltungsworkflow
description: In diesem Thema wird erläutert, wie Sie das Workflowsystem in Microsoft Dynamics 365 Finance verwenden können, um einen Prüfprozess für Spesenabrechnungen in der Spesenverwaltung einzurichten.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eb4d57194ce2dd7f80d75c2c765f1cfa48b0348
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684273"
---
# <a name="expense-management-workflow"></a>Ausgabenverwaltungsworkflow

Sie können das Workflow-System verwenden, um einen Überprüfungsprozess für Spesenabrechnungen in der Ausgabenverwaltung einzurichten. Sie können einen Workflow einrichten, der anhand der folgenden Kriterien ermittelt, wer Spesenabrechnungen genehmigt:

- Die Mitarbeiterberichtshierarchie und vordefinierte Genehmigungsgrenzen
- Mehrstufige Genehmigung, die vorläufige genehmigende Personen und eine endgültige genehmigende Person unterstützt
- Finanzielle Dimensionen und Projektverantwortung
- Zuordnung zu bestimmten Benutzern oder Benutzergruppen

Workflow-Genehmigungen können für Spesenabrechnungen, Reiseanforderungen, Bargeldvorschüsse und die Erstattung von Mehrwertsteuer (MwSt.) erstellt werden.

**Beispiel**

Der folgende Prozess ist ein Beispiel für den Workflow der Kostenverwaltung für eine Spesenabrechnung.

1. Ein Mitarbeiter erstellt und speichert eine Spesenabrechnung.
2. Der Mitarbeiter reicht die Spesenabrechnung zur Genehmigung ein. Die genehmigende Person wird anhand der Regeln identifiziert, die beim Einrichten des Workflows definiert wurden.
3. Die genehmigende Person erhält eine Benachrichtigung, dass eine Spesenabrechnung zur Genehmigung bereit ist. Die genehmigende Person überprüft die Spesenabrechnung und stellt sicher, dass die folgenden Bedingungen erfüllt sind:

    - Die Ausgaben verstoßen nicht gegen Ausgabenrichtlinien. Wenn eine Ausgabe gegen eine Richtlinie verstößt, überprüft die genehmigende Person, ob die Spesenabrechnung eine gültige geschäftliche Begründung enthält.
    - Elektronische Belege sind der Spesenabrechnung beigefügt.

4. Die genehmigende Person genehmigt die Spesenabrechnung.
5. Die Spesenabrechnung wird dem Kreditorenkoordinator zur Buchung zugeordnet.
6. Je nachdem, ob die automatische Buchung konfiguriert ist, wird einer der folgenden Schritte ausgeführt:

    - Wenn die automatische Buchung konfiguriert ist, wird die Spesenabrechnung zur Zahlung verarbeitet und der Status der Spesenabrechnung aktualisiert.
    - Wenn die automatische Buchung nicht konfiguriert ist, überprüft der Kreditorenkoordinator, ob alle Originalbelege übermittelt wurden und ob die Belege mit den Ausgaben in der Spesenabrechnung übereinstimmen. Alle Steuerkennzeichen, die in der Spesenabrechnung eingegeben wurden, müssen ebenfalls als korrekt überprüft werden.

Nachdem diese Anforderungen überprüft wurden, wird die Spesenabrechnung gebucht.

Nachdem die Spesenabrechnung gebucht wurde, wird die Zahlung für die Spesenabrechnung autorisiert und der Mitarbeiter erhält eine Rückerstattung.


[!INCLUDE[footer-include](../includes/footer-banner.md)]