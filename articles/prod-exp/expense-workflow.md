---
title: Ausgabenverwaltungsworkflow
description: In diesem Thema wird erläutert, wie Sie das Workflow-System in Microsoft Dynamics 365 Finance verwenden können, um einen Überprüfungsprozess für Spesenabrechnungen in der Ausgabenverwaltung einzurichten.
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
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076679"
---
# <a name="expense-management-workflow"></a>Ausgabenverwaltungsworkflow

[!include [banner](../includes/banner.md)]

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
