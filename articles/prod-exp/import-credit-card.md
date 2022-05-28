---
title: Kreditkartentransaktionen importieren und verwalten
description: In diesem Thema wird erläutert, wie kostenbezogene Kreditkartentransaktionen importiert und verwaltet werden. Diese Transaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden, oder sie können bei Bedarf manuell importiert werden.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bd7ca997e18bf3c11fa188b603c899cc470df035
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683767"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Kreditkartentransaktionen importieren und verwalten

Ausgabenbezogene Kreditkartentransaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden. Alternativ können die Transaktionen bei Bedarf manuell importiert werden. Die Kreditkartentransaktionen werden über die Dateneinheit Kreditkartentransaktionen importiert.

Weitere Informationen zu Datenentitäten finden Sie unter [Datenentitäten](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Kreditkartentransaktionen importieren

1. Auf der Seite **Kreditkartentransaktionen** wählen Sie **Transaktionen importieren**. Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie fortfahren können.
2. Geben Sie im Feld **Name** eine eindeutige Bezeichnung des Importauftrags ein.
3. Wählen Sie im Feld **Quelldatenformat** das Format der Datei aus, die die zu importierenden Kreditkartentransaktionen enthält.
4. Klicken Sie auf **Hochladen**. Finden Sie dann die Datei zum Importieren, und wählen Sie sie aus.
5. Überprüfen Sie nach dem Hochladen der Datei die Zuordnung der Kreditkartentransaktionsdatei und der Spalten der Entität der Kreditkartentransaktionsdaten, indem Sie den Link **Karte auswählen** auf der Kachel aus. Wenn Zuordnungsfehler vorliegen oder wenn Sie die Zuordnung ändern müssen, nehmen Sie die Zuordnungsänderungen entweder über die Registerkarte **Zuordnungsvisualisierung** oder die Registerkarte **Zuordnungsdetails** vor.
6. Wählen Sie **Wiederkehrenden Datenvorgang erstellen** aus, um die Kreditkartentransaktionen zu automatisieren. Anschließend können Sie die Wiederholung festlegen, die definiert, wie oft Kreditkartentransaktionen importiert werden sollen. Wenn Sie fertig sind, wählen Sie **OK** aus.
7. Um die ausgewählte Datei jetzt zu importieren, wählen Sie **Importieren** aus.
8. Wenn während des Imports Fehler auftreten, können Sie das Ausführungsprotokoll oder die Staging-Daten anzeigen, um die Fehler anzuzeigen, die Sie beheben müssen, um einen erfolgreichen Import zu gewährleisten.

> [!NOTE]
> Wenn Sie mehr als ein Dateiformat importieren müssen, müssen Sie für jeden Formattyp separate Importaufträge erstellen.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ordnen Sie die Kreditkartentransaktionen für gekündigte Mitarbeiter neu zu

Nach Beendigung eines Mitarbeiterdatensatzes ist das Active Directory Domain Services (AD DS) Konto des Mitarbeiters deaktiviert. Es kann jedoch aktive Kreditkartentransaktionen geben, die noch als Aufwand erfasst und erstattet werden müssen. Von der Seite **Kreditkartentransaktionen** können Sie den Mitarbeiter für jede Kreditkartentransaktion neu zuweisen, bei der der zugehörige Mitarbeiter gekündigt wurde.

Wählen Sie eine oder mehrere Kreditkartentransaktionen aus und wählen Sie dann **Transaktionen neu zuweisen** aus. Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartentransaktionen zugewiesen werden sollen. Nachdem die Kreditkartentransaktionen neu zugewiesen wurden, können sie für eine Spesenabrechnung ausgewählt und nach dem üblichen Verfahren für die Erstattung von Spesenabrechnungen bezahlt werden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]