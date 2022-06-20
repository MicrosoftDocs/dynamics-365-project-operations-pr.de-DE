---
title: Konfigurieren Sie nicht vorrätige Materialien und ausstehende Lieferantenrechnungen
description: Dieser Artikel erklärt, wie Sie nicht vorrätige Materialien und ausstehende Lieferantenrechnungen aktivieren können.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6473ef3510f0d3641a2d61b6a1b1f28980993277
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913757"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurieren Sie nicht vorrätige Materialien und ausstehende Lieferantenrechnungen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

## <a name="minimum-version-requirement"></a>Mindestens erforderliche Version

Für die Verwendung nicht vorrätiger Materialien und ausstehender Lieferantenrechnungen für nicht vorrätige/ressourcenbasierte Szenarien in Dynamics 365 Project Operations sind die folgenden Versionen erforderlich:

Dynamics 365 Dataverse-Lösungen:

- Project Operations – 4.9.0.221 oder höher
- Dual-Write-Anwendungs-Orchestrierungslösung – 2.2.2.23 oder höher

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) oder höher. Stellen Sie sicher, dass Ihre Finanzumgebung aktuell ist und alle Qualitätsupdates angewendet werden, um die Mindestversionsanforderungen zu erfüllen.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Führen Sie Dual-Write-Karten für nicht vorrätige Materialien und die Integration von Lieferantenrechnungen aus

Dieser Abschnitt enthält Informationen zu den Karten, die für nicht vorrätige Materialien und Lieferantenrechnungen erforderlich sind. Vergewissern Sie sich, dass die Zuordnungen, die im Artikel [Bereitstellen einer neuen Umgebung](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) aufgeführt sind, in Ihrer Umgebung ausgeführt werden.

1. Gehen Sie zu Lifecycle Services (LCS), navigieren Sie zu Ihrem LCS-Projekt und gehen Sie zur Seite **Umgebungsdetails**.
2. Wählen Sie im Abschnitt **Common Data Service Umgebungsinformationen** die Option **Link zu CDS für Apps** aus. Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.
3. Stellen Sie sicher, dass die folgenden Karten ausgeführt werden. Wenn sie nicht ausgeführt werden, starten Sie sie und stellen Sie sicher, dass alle zugehörigen Tabellenzuordnungen enthalten sind.

    - CDS veröffentlichte verschiedene Produkte (Produkte)
    - Anbieter v2 (msdyn_vendors)
    - Project Operations-Tabelle für Materialschätzungen (msdyn_estimatelines)
    - Project Operations-Integrationsprojektanbieter-Rechnungsexportentität (msdyn_projectvendorinvoices)
    - Project Operations-Integrationsprojektanbieter-Rechnungszeilenexportentität (msdyn_projectvendorinvoicelines)
    - Tatsächliche Werte der Project Operations-Integration (msdyn_actuals) Stellen Sie sicher, dass Sie die Kartenversion 1.0.0.14 oder höher ausführen. Sie können die aktive Version der Karte in der Spalte **Version** auf der Seite **Dual Write** anzeigen. Sie können eine neue Version der Karte aktivieren, indem Sie **Tabellenkartenversion** auswählen und dann die ausgewählte Version speichern.

Wenn Sie Standarddemodaten verwenden, müssen Sie möglicherweise auch die folgenden Entitätszuordnungen mit der anfänglichen Synchronisierung stoppen und neu starten:
  - Zahlungstage CDS V2 (msdyn_paymentdays)
  - Zahlungsplan (msdyn_paymentschedules)
  - Zahlungsbedingungen (msdyn_paymentterms)
  - Zulieferergruppen (msdyn_vendorgroups)
  - Einheiten (uom)

> [!NOTE]
> Die anfängliche Synchronisierung für Zulieferergruppen und -einheiten schlägt möglicherweise für einige Datensätze in der vorhandenen Demodataset fehl. Sie können die Fehler ignorieren, da sie Sie nicht daran hindern, Demo-Daten mit Project Operations zu verwenden.

## <a name="configure-prerequisites-in-dataverse"></a>Voraussetzungen in Dataverse konfigurieren

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktivieren Sie den Workflow, um Konten basierend auf der Zuliefererentität zu erstellen

Die Dual Write Orchestration-Lösung biete t[ Anbieter-Masterintegration ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Voraussetzung für diese Funktion sind Lieferantendaten in der Entität **Konten**. Aktivieren Sie einen Vorlagen-Workflow-Prozess, um Hersteller in der Tabelle **Konten** zu erstellen, wie unter [Wechseln zwischen Herstellerentwürfen](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch) beschrieben.

### <a name="set-products-to-be-created-as-active"></a>Legen Sie fest, dass Produkte als aktiv erstellt werden sollen

Nicht vorrätige Materialien müssen als **Freigegebene Produkte** in Finance konfiguriert sein. Die Dual Write Orchestration-Lösung bietet eine sofort einsatzbereite [Integration von freigegebenen Produkten im Dataverse-Produktkatalog](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Standardmäßig werden Produkte aus Finance mit Dataverse in einem Entwurfszustand synchronisiert. Um das Produkt in einen aktiven Status zu synchronisieren, damit es direkt in Materialverwendungsdokumenten oder ausstehenden Lieferantenrechnungen verwendet werden kann, gehen Sie zu **System** > **Verwaltung** > **Systemadministration** > **Systemeinstellungen** und setzen Sie auf der Registerkarte **Vertrieb** die Option **Produkte im aktiven Status erstellen** auf **Ja**.

## <a name="configure-prerequisites-in-finance"></a>Voraussetzungen in Finance konfigurieren

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktivieren Sie den Funktionsschlüssel für ausstehende Lieferantenrechnungen

Führen Sie die folgenden Schritte aus, um die Funktionalität zum Hinzufügen von Projektdetails zu ausstehenden Lieferantenrechnungsposten zu aktivieren.

1. Navigieren Sie zum Arbeitsbereich **Funktionsverwaltung** in Finance.
2. Suchen Sie in der Funktionsliste **Ausstehende Lieferantenrechnungen für Project Operations für ressourcenbasierte/nicht vorrätige Szenarien aktivieren** und wählen Sie **Aktivieren**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definieren Sie Kategoriegruppen und Projektkategorien für Elemente

Konfigurieren Sie mindestens eine Kategoriegruppe für den Buchungstyp **Artikel** und mindestens eine Projektkategorie, die diese Gruppe verwendet. Weitere Informationen finden Sie unter [Produktkategorien konfigurieren](../project-accounting/configure-project-categories.md#category-groups).

Überprüfen Sie die Kosten- und Umsatzprofile des Projekts und konfigurieren Sie die Einrichtung der Sachkontobuchung für Artikelbuchungen. Weitere Informationen finden Sie unter [ Konfigurieren der Buchhaltung für abrechnungsfähige Projekte](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Manuell einzutragendes Produkt einrichten

In Project Operations können Sie Materialschätzungen und Nutzung für Katalogprodukte, die im freigegebenen Produktkatalog konfiguriert sind, und für manuell einzutragende Produkte aufzeichnen. Für die Verwendung von manuell einzutragenden Produkten ist ein einzelnes freigegebenes Produkt erforderlich, das in Finance für diesen Zweck konfiguriert wurde. Führen Sie die folgenden Schritte aus, um ein manuell einzutragendes Produkt zu konfigurieren. Wiederholen Sie diese Schritte in jeder juristischen Person, die Project Operations für Szenarien mit oder ohne Lagerbestand verwendet.

1. Navigieren Sie in Finance zu **Produktionsinformationsverwaltung** > **Produkte** > **Freigegebene Produkte** und wählen Sie **Neu**.
2. Wählen Sie im Feld **Produktart** **Artikel** aus und im Feld **Produktuntertyp** die Option **Produkt**.
3. Geben Sie die Produktnummer (WRITEIN) und den Produktnamen (Manuell einzutragendes Produkt) ein.
4. Wählen Sie die Artikelmodelluppe aus. Stellen Sie sicher, dass in der ausgewählten Artikelmodellgruppe das Feld **Inventarpolitik Lagerware** auf **False** gesetzt ist.
5. Wählen Sie Werte in den Feldern **Artikelgruppe**,**Speicherdimensionsgruppe** und **Verfolgungsdimensionsgruppe** aus. Verwenden Sie die Dimension **Lagerung** nur für **Standort**, und wählen Sie im Feld **Verfolgungsdimensionen** die Option **Keine**.
6. Wählen Sie Werte in den Feldern **Inventareinheit**,**Kaufeinheit** und **Verkaufseinheit**, und speichern Sie dann Ihre Änderungen.
7. Auf der Registerkarte **Plan** setzen Sie die Standardbestellungseinstellungen fest und auf der Registerkarte **Inventar** legen Sie den Standardstandort und das Standardlager fest.
8. Gehen Sie zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** und öffnen Sie **Project Operations in Dynamics 365 Dataverse**. 
9. Auf der Registerkarte **Materialien** im Feld **Manuell einzutragendes Produkt** wählen Sie das von Ihnen erstellte Produkt aus.
10. Öffnen Sie in der Dataverse-Umgebung in der Sitemap die Entität **Produkte** und suchen Sie den Datensatz für das manuell einzutragende Produkt. 
11. Öffnen Sie die Datensatzdetails und setzen Sie den Produktstatus auf **Zurückgezogen**. Dieser Produktstatus verhindert, dass jemand diesen Datensatz versehentlich direkt in Materialschätzungen und Verwendungsdokumenten verwendet.

### <a name="set-up-a-procurement-integration-account"></a>Richten Sie ein Beschaffungsintegrationskonto ein

Das Beschaffungsintegrationskonto wird als Verrechnungskonto verwendet, wenn eine ausstehende Lieferantenrechnung mit Zeilen gebucht wird, die einem Projekt zugeordnet sind.

Wenn das System eine ausstehende Lieferantenrechnung bucht, wird dieses Konto für den Projektkostenbetrag verwendet. Die Lieferantenrechnungsdetails werden in Dataverse verarbeitet und ein entsprechendes Projekt wird erstellt. Die Informationen aus dem aktuellen Projekt werden dem Project Operations Integrationsjournal hinzugefügt. Wenn Sie das Integrationsjournal buchen, wird der Betrag vom Beschaffungsintegrationskonto gelöscht und in den Projektkosten erfasst.

1. Um das Beschaffungsintegrationsjournal einzurichten, gehen Sie zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** und öffnen Sie **Project Operations in Dynamics 365 Dataverse**. 
2. Wählen Sie auf der Registerkarte **Materialien** im Feld **Beschaffungsintegrationskonto** einen Wert aus.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Richten Sie die Standardwerte für die Projektkategorie für ein Element ein

1. Gehen Sie in Finance zu **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** und öffnen Sie **Project Operations in Dynamics 365 Dataverse**. 
2. Auf der Registerkarte **Standardeinstellungen für Projektkategorien** im Feld **Artikel** wählen Sie einen Wert. Diese Projektkategorie wird für Materialtransaktionen verwendet, wenn die Projektkategorie nicht im Projektdatensatz festgelegt wurde.
