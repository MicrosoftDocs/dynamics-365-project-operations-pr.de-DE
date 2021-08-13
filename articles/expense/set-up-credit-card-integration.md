---
title: Kreditkartenintegration einrichten
description: In diesem Thema wird erläutert, wie Sie mit kostenbezogenen Kreditkartentransaktionen arbeiten.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996210"
---
# <a name="set-up-credit-card-integration"></a>Kreditkartenintegration einrichten

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ausgabenbezogene Kreditkartentransaktionen können so eingerichtet werden, dass sie automatisch nach einem wiederkehrenden Zeitplan importiert werden. Alternativ können die Transaktionen bei Bedarf manuell importiert werden. Die Kreditkartentransaktionen werden über die Dateneinheit Kreditkartentransaktionen importiert.

## <a name="import-credit-card-transactions"></a>Kreditkartentransaktionen importieren

Gehen Sie folgendermaßen vor, um Kreditkartentransaktionen zu importieren:

1. Auf der Seite **Kreditkartentransaktionen** wählen Sie **Transaktionen importieren**. Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie fortfahren können.
2. Im Feld **Name** geben Sie eine eindeutige Beschreibung für den Importauftrag ein.
3. In dem Feld **Quelldatenformat** wählen Sie im Feld das Format der Datei aus, die die zu importierenden Kreditkartentransaktionen enthält.
4. Klicken Sie auf **Hochladen**. Finden Sie dann die Datei zum Importieren, und wählen Sie sie aus.
5. Überprüfen Sie nach dem Hochladen der Datei die Zuordnung der Kreditkartentransaktionsdatei und der Spalten der Entität der Kreditkartentransaktionsdaten, indem Sie den Link **Karte auswählen** auf der Kachel aus. Wenn Zuordnungsfehler vorliegen oder wenn Sie die Zuordnung ändern müssen, nehmen Sie die Zuordnungsänderungen entweder über die Registerkarte **Zuordnungsvisualisierung** oder die Registerkarte **Zuordnungsdetails** vor.
6. Wählen Sie **Wiederkehrenden Datenvorgang erstellen** aus, um die Kreditkartentransaktionen zu automatisieren. Anschließend können Sie die Wiederholung festlegen, die definiert, wie oft Kreditkartentransaktionen importiert werden sollen. Wenn Sie fertig sind, wählen Sie **OK** aus.
7. Um die ausgewählte Datei jetzt zu importieren, wählen Sie **Importieren** aus.
8. Wenn während des Imports Fehler auftreten, können Sie das Ausführungsprotokoll oder die Staging-Daten anzeigen, um die Fehler anzuzeigen, die Sie beheben müssen, um einen erfolgreichen Import sicherzustellen.

> [!NOTE]
> Wenn Sie mehr als ein Dateiformat importieren müssen, müssen Sie für jeden Formattyp separate Importaufträge erstellen.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Ordnen Sie die Kreditkartentransaktionen für gekündigte Mitarbeiter neu zu

Nach Beendigung eines Mitarbeiterdatensatzes ist das Active Directory Domain Services (AD DS) Konto des Mitarbeiters deaktiviert. Es kann jedoch aktive Kreditkartentransaktionen geben, die noch als Aufwand erfasst und erstattet werden müssen. Auf der Seite **Kreditkartentransaktionen** können Sie den Mitarbeiter für jede Kreditkartentransaktion neu zuweisen, bei der der zugehörige Mitarbeiter gekündigt wurde.

Wählen Sie eine oder mehrere Kreditkartentransaktionen aus und wählen Sie dann **Transaktionen neu zuweisen** aus. Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartentransaktionen zugewiesen werden sollen. Nachdem die Kreditkartentransaktionen neu zugewiesen wurden, können sie für eine Spesenabrechnung ausgewählt und nach dem üblichen Verfahren für die Erstattung von Spesenabrechnungen bezahlt werden.

## <a name="delete-credit-card-transactions"></a>Kreditkartentransaktionen löschen 

Manchmal müssen nach dem Import von Kreditkartentransaktionen bestimmte Transaktionen gelöscht werden. Dies kann daran liegen, dass es sich bei den Transaktionen um Duplikate handelt oder dass die Daten möglicherweise nicht korrekt sind. Administratoren können die Funktion **Kreditkartentransaktionen löschen** zum Auswählen und Löschen von Kreditkartentransaktionen, die einer Spesenabrechnung **nicht angehängt** sind. 

1. Gehen Sie zu **Periodische Aufgaben** > **Kreditkartentransaktionen löschen**.
2. Wählen Sie **Filter** und Informationen bereitstellen, um die einzuschließenden Datensätze zu identifizieren.
3. Um die Datensätze zu löschen, wählen Sie **OK** aus. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
