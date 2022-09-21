---
title: Kreditorenrechnungen erstellen
description: Dieser Artikel beschreibt das Konzept der Lieferantenrechnungen und erklärt, wie Sie Lieferantenrechnungen in Microsoft Dynamics 365 Project Operations erstellen.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475418"
---
# <a name="create-vendor-invoices"></a>Kreditorenrechnungen erstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Um die in diesem Artikel beschriebene Funktionalität verwenden zu können, müssen Sie die Funktion **Ermöglichen Sie die Ist-Verarbeitung von Unteraufträgen mit Project Operations für ressourcenbasierte Szenarien** im Arbeitsbereich **Funktionsverwaltung** aktivieren.

Die Kreditorenrechnungsstellung in Microsoft Dynamics 365 Project Operations kann verwendet werden, um Kosten aus Lieferungen von Dienstleistungen und/oder Materialien für ein Projekt, das vom Zulieferer abgeschlossen wurde, zu erfassen.

Wenn Dienstleistungen und/oder Materialien an einen Kreditor vergeben werden, stellt eine Fremdarbeit die vertragliche Vereinbarung mit diesem Lieferanten dar. Wenn der Kreditor die Dienstleistungen erbringt oder die Materialien empfangen und für Projektaufgaben verwendet werden, werden die Kosten für das Projekt erfasst. Der Lieferant sendet dann periodisch Rechnungen. Diese Rechnungen werden geprüft und mit den im Projekt erfassten Kosten abgeglichen. Nach Abschluss des Verifizierungsprozesses wird die Kreditorenrechnung bestätigt und zur Zahlung freigegeben.

## <a name="scenarios-for-use"></a>Anwendungsszenarien

Kreditorenrechnungen in Project Operations können verwendet werden, um zwei unterschiedliche Szenarien zu unterstützen:

- Kunden nutzen die vollständige Fremdarbeitserfahrung.
- Kunden nutzen nicht die vollständigen Fremdvergabeerfahrungen, möchten aber eine einheitliche Ansicht der Kosten für Projekte in Project Operations haben:

### <a name="customers-use-the-full-subcontracting-experiences"></a>Kunden nutzen die vollständigen Fremdarbeitserfahrung

Erfahrungen mit Kreditorenrechnungen bieten eine Möglichkeit zum Überprüfen und Abgleichen von Zeiteinträgen, Materialverbrauch und Ausgabeneinträgen, die dann auf fremdvergebene Komponenten mit Kreditorenrechnungspositionen verweisen. Dieser Prozess kann verwendet werden, um die Genauigkeit der Kreditorenrechnungspositionen zu überprüfen. Nachdem der Überprüfungsprozess abgeschlossen und die Kreditorenrechnung bestätigt wurde, storniert das System die Ist-Werte, die durch genehmigte Zeit-, Ausgaben- und Materialverwendungsprotokolle erfasst wurden, und erstellt mithilfe der Kreditorenrechnungspositionen neue Ist-Kosten.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Kunden nutzen nicht die vollständigen Fremdvergabeerfahrungen, möchten aber eine einheitliche Ansicht der Kosten für Projekte in Project Operations haben

Wenn Sie den Fremdarbeitsprozess in einem Drittsystem verfolgen, können Sie Kosten aus diesem Drittsystem in Project Operations erfassen, indem Sie Kreditorenrechnungen erstellen, die nicht auf Fremdarbeit verweisen. Auf diese Weise haben Ihre Projektmanager einen einzigen, einheitlichen Überblick über alle Kosten eines bestimmten Projekts.

## <a name="create-vendor-invoices-in-project-operations"></a>Erstellen von Kreditorenrechnungen in Project Operations

Kreditorenrechnungen werden in Dynamics 365 Finance unter Verwendung vom Modul **Kreditoren** erstellt. Sie können Kreditorenrechnungen nicht direkt in Dataverse erstellen.

### <a name="set-up-vendor-invoice-verification"></a>Kreditorenrechnungsüberprüfungen einrichten

Wenn die Lieferantenrechnung für einen Unterauftrag in Dataverse bestimmt ist, müssen Sie die Parameter **Eine manuelle Überprüfung per PM ist erforderlich** einrichten. Die Einstellung der Option bestimmt, ob die Lieferantenrechnung automatisch in Dataverse bestätigt werden soll oder ob eine manuelle Bestätigung erforderlich ist. Der Kopf jeder Projektlieferantenrechnung enthält eine gleichnamige Option. Standardmäßig ist die Option im Kopf aller Kreditorenrechnungen des Projekts auf den Wert eingestellt, den Sie hier festlegen. Sie können den Wert jedoch nach Bedarf im Kopf der einzelnen Kreditorenrechnungen aktualisieren.

Wenn die Option auf **Ja** festgelegt ist, wird die Kreditorenrechnung, die in Finance erstellt und mit Dataverse synchronisiert wird, mit dem Status **Entwurf** dargestellt. Die Rechnung muss dann vom Projektmanager validiert und verifiziert und bestätigt werden, bevor sie verarbeitet und auf die spezifischen Projekt- und Sachkonten in Finance gebucht wird.

Wenn die Option auf **Nein** festgelegt ist, wird die Kreditorenrechnung automatisch bestätigt. Es ist keine weitere Maßnahme erforderlich.

Gehen Sie folgendermaßen vor, um die Überprüfung der Kreditorenrechnungen einzurichten.

1. Navigieren Sie in Finance zu **Projektmanagement und -buchhaltung** \> **Einrichtung** \> **Projektmanagement- und Buchhaltungsparameter**.
1. Auf der Registerkarte **Finanzen** legen Sie die Option **Eine manuelle Überprüfung per PM ist erforderlich** auf **Ja** fest, wenn die Unternehmensrichtlinie die Überprüfung der Lieferantenrechnungen von Subunternehmern erfordert. Wenn eine Überprüfung durch den Projektmanager in Dataverse nicht erforderlich ist, legen Sie den Optionssatz auf **Nein** fest. Standardmäßig wird die Einstellung auf der Seite **Ausstehende Lieferantenrechnung** verwendet.

> [!NOTE]
> Kreditorenrechnungen, die für Unteraufträge in Dataverse erstellt werden, können nur korrekt verarbeitet werden, wenn die Option **Eine manuelle Überprüfung per PM ist erforderlich** auf **Ja** festgelegt ist. Ist-Kosten für Zeit, Material und Aufwand, die Subunternehmer erstellen, können vom Projektmanager nur dann manuell mit Kreditorenrechnungspositionen abgeglichen werden, wenn diese Option auf **Ja** festgelegt ist.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Richten Sie ein Beschaffungsintegrationskonto für Zuliefererrechnungen ein

Wenn eine Kreditorenrechnung in Finance for Project Operations – integrierte Umgebung (kein Lagerbestand) gebucht wird, werden Finanzdaten auf das Procurement-Integrationskonto gebucht. Das System erzeugt die Istwerte in Dataverse für die gebuchte Rechnung. Diese Ist-Werte werden in Finance gebucht, indem das Projektintegrationsjournal verwendet wird. Durch das Buchen im Projektintegrationskontos wird der tatsächliche Betrag gebucht und auf dem Beschaffungsintegrationskonto ausgeglichen.

Um das Beschaffungsintegrationskonto für Zuliefererrechnungen einzurichten, folgen Sie diesen Schritten.

1. Navigieren Sie in Finance zu **Projektmanagement und -buchhaltung** \> **Einrichtung** \> **Projektmanagement- und Buchhaltungsparameter**.
1. Auf der Registerkarte **Project Operations in Dynamics 365 Customer Engagement** wählen Sie **Materialien** \> **Beschaffungsintegrationskonto**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Erstellen und buchen von Rechnungen für Fremdarbeit

Wenn ein Kreditor eine Rechnung vom Subunternehmer erhält, wird in Finance eine neue Rechnung erstellt.

1. Navigieren Sie in Finance zu **Kreditorenkonten** \> **Rechnungen** \> **Ausstehene Kreditorenrechnungen**.
1. Um eine neue Zuliefererrechnung zu erstellen, gehen Sie zum **Aktionsbereich** und wählen **Neu** aus.
1. Im Rechnungskopf im Feld **Rechnungskonto** wählen Sie **Subunternehmer**.
1. Wählen Sie das Rechnungsdatum.
1. Auf der Registerkarte **Header** wählen Sie **Eine manuelle Überprüfung per PM ist erforderlich** und legen die Option auf **Ja** fest. Die Standardeinstellung dieser Option stammt von der Seite **Projektmanagement und Abrechnungsparameter**. Sie kann jedoch auf Kreditorenrechnungsebene geändert werden.
1. Im Inforegister **Rechnungszeile** wählen Sie **Zeile hinzufügen**, um eine Kreditorenrechnungsposition zu erstellen.
1. Wählen Sie die Beschaffungskategorie aus, die für Unterauftragspositionen erstellt wurde, und geben Sie den Einheitspreis, die Maßeinheit und die Menge ein.
1. Im Abschnitt Kreditorenrechnungspositionen auf der Registerkarte **Projekt** wählen Sie das Projekt aus, für das der Subunternehmer die Subunternehmerrechnung aufteilt.
1. Wählen Sie die Projektkategorie. Es kann **Artikel**, **Aufwand**, **Materialien** oder **Stunden** sein.
1. Wählen Sie die Rolle nur aus, wenn die ausgewählte Projektkategorie zum Typ **Stunde** gehört.
1. Wählen Sie **Buchen** aus, um die Zuliefererrechnung zu buchen.

Alternativ können Sie eine Lieferantenrechnung erstellen, indem Sie zu **Abbrechnungsverbindlichkeiten** \> **Rechnungen** \> **Öffnen Sie Lieferantenrechnungen** gehen und **Neu** auswählen.

Wenn die Kreditorenrechnung gebucht wird, wird sie in Dataverse zur Verifizierung und Bearbeitung durch den Projektleiter verfügbar.

## <a name="vendor-invoice-processing-in-dataverse"></a>Zuliefererrechnungen in Dataverse verarbeiten

In der Kreditorenrechnung, die in Dataverse erstellt wird, stammen einige Feldwerte aus der Kreditorenrechnung, die in Finance erfasst wird. Andere Werte sind Vorschlagswerte, die aus dem Untervertrag stammen.

Die folgenden Felder und zugehörigen Datensätze werden aus dem Untervertrag in die Kopfzeile der Kreditorenrechnung kopiert:

- Währungen
- Vertragsschlusseinheit
- Zahlungsbedingungen

Auf den Kreditorenrechnungspositionen verwendet Project Operations die folgenden Feldwerte, um den standardmäßigen Untervertrag und die Untervertragspositionsreferenz einzugeben:

- Transaktionsklasse
- Role
- Transaktionskategorie
- Produktfelder
- Project
- Task

> [!NOTE]
> Fremdvertragspositionen mit Festpreis werden in Project Operations nicht unterstützt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
