---
title: Integration der Projektvorkalkulationen und Istwerte
description: Dieses Thema enthält Informationen zur Project Operations Dual-Write-Integration für Projektvorkalkulationen und Istwerte.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577189"
---
# <a name="project-estimates-and-actuals-integration"></a>Integration der Projektvorkalkulationen und Istwerte

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zur Project Operations Dual-Write-Integration für Projektvorkalkulationen und Istwerte.

## <a name="project-estimates"></a>Projektschätzungen

Projektarbeits-, Kosten- und Materialschätzungen werden in Microsoft Dataverse erstellt und gepflegt und für Buchhaltungszwecke mit Finanz- und Betriebs-Apps synchronisiert. Die Vorgänge Erstellen, Aktualisieren und Löschen werden von Finanz- und Betriebs-Apps nicht unterstützt.

Das Erstellen von Schätzungen erfordert eine gültige Buchhaltungskonfiguration für das Projekt. Projekte, die Vertragszeilen zugeordnet sind, müssen ein gültiges Projektkosten- und Umsatzprofil haben, das in den Regeln für das Projektkosten- und Umsatzprofil definiert ist. Weitere Informationen finden Sie unter [Konfigurieren der Buchhaltung für abrechnungsfähige Projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbeitsschätzungen

Arbeitsschätzungen werden vom Projektmanager oder Ressourcenmanager erstellt, der der Projektaufgabe auch eine generische oder benannte Ressource zuweist. Die Ressourcenzuweisungsdatensätze können auf der Registerkarte **Ressourcenzuweisungen** auf der Seite **Projektdetails** in Dataverse angezeigt werden. Ressourcenzuweisungsdatensätze in Dataverse erstellen Stundenprognosedatensätze in Finanz- und Betriebs-Apps mit **Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)**.

   ![Integration der Arbeitsvorkalkulationen.](./Media/DW4LaborEstimates.png)

Dual-Write synchronisiert Ressourcenzuweisungsdatensätze mit der Staging-Tabelle (**ProjCDSEstimateHoursImport**) und verwendet dann Geschäftslogik, um Stundenprognosedatensätze zu erstellen und zu aktualisieren (**ProjForecastEmpl**).

Der Projektbuchhalter überprüft die in Finanz- und Betriebs-Apps erstellten prognostizierten Stundenaufzeichnungen, indem er zu **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Stundenprognosen** wechselt.

## <a name="expense-estimates"></a>Ausgabenschätzungen

Kostenvoranschläge werden vom Projektmanager auf der Registerkarte **Kostenvoranschläge** auf der Seite **Projektdetails** in Dataverse erstellt. Kostenvoranschlagsdatensätze werden in der Entität **Schätzungszeile** in Dataverse gespeichert. Diese Schätzungsdatensätze haben die Transaktionsklasse **Ausgabe** und werden zu Ausgabeprognosedatensätzen in Finanz- und Betriebs-Apps synchronisiert. Dies geschieht mithilfe von **Project Operations-Integrationsentität für Kostenschätzungen (msdyn\_estimatelines)**.

   ![Integration der Kostenvoranschläge.](./Media/DW4ExpenseEstimates.png)

Dual-Write synchronisiert Kostenvoranschlagsdatensätze mit der Staging-Tabelle (**ProjCDSEstimateExpenseImport**) und verwendet dann Geschäftslogik, um Ausgabenprognosedatensätze zu erstellen und zu aktualisieren (**ProjForecastCost**). In den Schätzzeilen werden Umsatzschätzungs- und Kostenvoranschlagsdatensätze getrennt gespeichert. Die Geschäftslogik in Finanz- und Betriebs-Apps füllt einen einzelnen Ausgabenprognosedatensatz mit diesem Detail in der Staging-Tabelle.

Der Projektbuchhalter ksnn die in Finanz- und Betriebs-Apps erstellten prognostizierten Ausgabenaufzeichnungen überprüfgen, indem er zu **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Asugabenprognosen** wechselt.

## <a name="material-estimates"></a>Materialvorkalkulationen

Materialvorkalkulationen werden vom Projektmanager auf der Registerkarte **Materialvorkalkulationen** auf der Seite **Projektdetails** in Dataverse erstellt. Materialvorkalkulationsdatensätze werden in der Entität **Schätzungszeile** in Dataverse gespeichert. Diese Schätzungsdatensätze haben die Transaktionsklasse **Material** und werden zu Artikelprognosedatensätzen in Finanz- und Betriebs-Apps synchronisiert. Dies geschieht mithilfe von **Project Operations-Tabelle für M;aterialschätzungen (msdyn\_estimatelines)**.

   ![Integration der Materialvorkalkulationen.](./Media/DW4MaterialEstimates.png)

Dual-Write synchronisiert Materialvorkalkulationsdatensätze mit der Staging-Tabelle (**ProjForecastSalesImpor**) und verwendet dann Geschäftslogik, um Artikelprognosedatensätze zu erstellen und zu aktualisieren (**ForecastSales**). In den Schätzzeilen werden Umsatzschätzungs- und Kostenvoranschlagsdatensätze getrennt gespeichert. Die Geschäftslogik in Finanz- und Betriebs-Apps füllt einen einzelnen Artikelprognosedatensatz mit diesem Detail in der Staging-Tabelle.

Der Projektbuchhalter ksnn die in Finanz- und Betriebs-Apps erstellten prognostizierten Artikelaufzeichnungen überprüfgen, indem er zu **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Artikelprognosen** wechselt.

## <a name="project-actuals"></a>Projekt-Istwerte

Projekt-Istwerte werden in Dataverse erstellt, basierend auf Zeit, Kosten, Material und Abrechnungsaktivität. Alle operativen Attribute dieser Transaktionen, einschließlich Menge, Selbstkostenpreis, Verkaufspreis und Projekt, werden hier in dieser Dataverse-Entität erfasst. Weitere Informationen finden Sie unter [Istwerte](../actuals/actuals-overview.md). Tatsächliche Datensätze werden mithilfe der Tabellenzuordnung **Ist-Werte für die Project Operations-Integration (msdyn\_actuals)** für duales Schreiben für die nachgelagerte Buchhaltung mit Finanz- und Betriebs-Apps synchronisiert.

   ![Istwerteintegration.](./Media/DW4Actuals.png)

Die Tabellenzuordnung **Project Operations-Integration Istwerte** synchronisiert alle Datensätze aus der Entität **Istwerte** in Dataverse, wobei das Attribut **Synchronisierung überspringen (nur für den internen Gebrauch)** auf **False** gesetzt ist. Dieser Attributwert wird in Dataverse automatisch festgelegt, wenn der Datensatz erstellt wird. Beispiele, bei denen dieses Attribut auf **True** festgelegt ist, sind:

  - Projektkosten-Istwerte für konzerninterne Transaktionen. Weitere Informationen finden Sie unter [Erstellen unternehmensinterner Buchungen](../project-accounting/create-intercompany-transactions.md). Diese Datensätze werden übersprungen, da das System die tatsächlichen Projektkosten in Finanz- und Betriebs-Apps neu erstellt, wenn die Intercompany-Kreditorenrechnung gebucht wird.
  - Negative, nicht in Rechnung gestellte Verkaufsdatensätze werden erstellt, wenn die Proforma-Rechnung bestätigt wird. Diese Datensätze werden übersprungen, da das Nebenbuch des Projekts in Finanz- und Betriebs-Apps den nicht fakturierten Umsatzdatensatz bei der Rechnungsstellung nicht storniert, sondern den Status in vollständig fakturiert ändert.

Die Dual-Write-Tabellenzuordnung synchronisiert die tatsächlichen Datensätze mit der Staging-Tabelle **ProjCDSActualsImport**. Diese Datensätze werden durch den periodischen Prozess **Import aus Staging-Tabelle** beim Erstellen von Journalzeilen für die Project Operations-Integrationserfassungszeilen und Projektrechnungsvorschlagszeilen verarbeitet. Weitere Informationen finden Sie unter [Integrationsjournal in Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse erfasst auch die Verknüpfungen zwischen den tatsächlichen Transaktionen des Projekts in der **Transaktionsverbindung**-Entität. Weitere Informationen finden Sie unter [Verknüpfen der Istdaten mit Originaldatensätzen](../actuals/linkingactuals.md). Verknüpfungen zwischen tatsächlichen Transaktionen werden auch mithilfe der Tabellenzuordnung für duales Schreiben **Integrationsentität für Projekttransaktionsbeziehungen (msdyn\_transactionconnections)** mit Finanz- und Betriebs-Apps synchronisiert. Diese Datensätze werden durch den periodischen Prozess **Import aus Staging-Tabelle** beim Erstellen von Journalzeilen für die Project Operations-Integrationserfassungszeilen und Projektrechnungsvorschlagszeilen verarbeitet.

Das Buchen eines Project Operations-Integrationsjournals und eines Projektrechnungsvorschlags löst eine Aktualisierung der jeweiligen Datensätze in der Staging-Tabelle **ProjCDSActualsImport** aus. Das System erfasst und zeichnet die folgenden Abrechnungsattribute für tatsächliche Transaktionen auf:

- Buchhaltungswährungsbetrag
- Wechselkurs
- Belegnummer
- Umsatzsteuerbetrag

Die Tabellenzuordnung **Project Operations-Integration Istwerte** aktualisiert die jeweiligen Istwert-Datensätze in Dataverse mit diesen Informationen.
