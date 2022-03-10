---
title: Integration der Projektvorkalkulationen und Istwerte
description: Dieses Thema enthält Informationen zur Project Operations Dual-Write-Integration für Projektvorkalkulationen und Istwerte.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006290"
---
# <a name="project-estimates-and-actuals-integration"></a>Integration der Projektvorkalkulationen und Istwerte

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zur Project Operations Dual-Write-Integration für Projektvorkalkulationen und Istwerte.

## <a name="project-estimates"></a>Projektschätzungen

Projektarbeits-, Kosten- und Materialschätzungen werden in Microsoft Dataverse erstellt und verwaltet und mit Finance and Operations Apps für Buchhaltungszwecke synchronisiert. Das Erstellen, Aktualisieren und Löschen durch die Finance and Operations-Apps wird nicht unterstützt.

Das Erstellen von Schätzungen erfordert eine gültige Buchhaltungskonfiguration für das Projekt. Projekte, die Vertragszeilen zugeordnet sind, müssen ein gültiges Projektkosten- und Umsatzprofil haben, das in den Regeln für das Projektkosten- und Umsatzprofil definiert ist. Weitere Informationen finden Sie unter [Konfigurieren der Buchhaltung für abrechnungsfähige Projekte](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Arbeitsschätzungen

Arbeitsschätzungen werden vom Projektmanager oder Ressourcenmanager erstellt, der der Projektaufgabe auch eine generische oder benannte Ressource zuweist. Die Ressourcenzuweisungsdatensätze können auf der Registerkarte **Ressourcenzuweisungen** auf der Seite **Projektdetails** in Dataverse angezeigt werden. Ressourcenzuweisungsdatensätze in Dataverse erstellen Stundenprognosedatensätze in Finance and Operations Apps mit **Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)**.

   ![Integration der Arbeitsvorkalkulationen.](./Media/DW4LaborEstimates.png)

Dual-Write synchronisiert Ressourcenzuweisungsdatensätze mit der Staging-Tabelle (**ProjCDSEstimateHoursImport**) und verwendet dann Geschäftslogik, um Stundenprognosedatensätze zu erstellen und zu aktualisieren (**ProjForecastEmpl**).

Der Projektbuchhalter überprüft die Prognosestundendatensätze in Finance and Operations Apps unter **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Stundenvorhersagen**.

## <a name="expense-estimates"></a>Ausgabenschätzungen

Kostenvoranschläge werden vom Projektmanager auf der Registerkarte **Kostenvoranschläge** auf der Seite **Projektdetails** in Dataverse erstellt. Kostenvoranschlagsdatensätze werden in der Entität **Schätzungszeile** in Dataverse gespeichert. Diese Schätzungsdatensätze haben die Transaktionsklasse: **Ausgabe** und werden mit Ausgabenprognosedatensätzen in Finance and Operations Apps mit der **Project Operations-Integrationsentität für Kostenvoranschläge (msdyn\_estimatelines)** synchronisiert.

   ![Integration der Kostenvoranschläge.](./Media/DW4ExpenseEstimates.png)

Dual-Write synchronisiert Kostenvoranschlagsdatensätze mit der Staging-Tabelle (**ProjCDSEstimateExpenseImport**) und verwendet dann Geschäftslogik, um Ausgabenprognosedatensätze zu erstellen und zu aktualisieren (**ProjForecastCost**). In den Schätzzeilen werden Umsatzschätzungs- und Kostenvoranschlagsdatensätze getrennt gespeichert. Die Geschäftslogik in Finance and Operations Apps füllt einen einzelnen Ausgabenprognosedatensatz mit diesem Detail in der Staging-Tabelle.

Der Projektbuchhalter überprüft die Ausgabenprognosendatensätze in Finance and Operations Apps unter **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Ausgabevorhersagen**.

## <a name="material-estimates"></a>Materialvorkalkulationen

Materialvorkalkulationen werden vom Projektmanager auf der Registerkarte **Materialvorkalkulationen** auf der Seite **Projektdetails** in Dataverse erstellt. Materialvorkalkulationsdatensätze werden in der Entität **Schätzungszeile** in Dataverse gespeichert. Diese Schätzungsdatensätze haben die Transaktionsklasse: **Material** und werden mit Artikelprognosedatensätzen in Finance and Operations Apps mit der **Project Operations-Integrationstabelle für Materialvorkalkulationen (msdyn\_estimatelines)** synchronisiert.

   ![Integration der Materialvorkalkulationen.](./Media/DW4MaterialEstimates.png)

Dual-Write synchronisiert Materialvorkalkulationsdatensätze mit der Staging-Tabelle (**ProjForecastSalesImpor**) und verwendet dann Geschäftslogik, um Artikelprognosedatensätze zu erstellen und zu aktualisieren (**ForecastSales**). In den Schätzzeilen werden Umsatzschätzungs- und Kostenvoranschlagsdatensätze getrennt gespeichert. Die Geschäftslogik in Finance and Operations Apps füllt einen einzelnen Elementprognosedatensatz mit diesem Detail in der Staging-Tabelle.

Der Projektbuchhalter überprüft die Elementprognosendatensätze in Finance and Operations Apps unter **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Planen** > **Elementprognosen**.

## <a name="project-actuals"></a>Projekt-Istwerte

Projekt-Istwerte werden in Dataverse erstellt, basierend auf Zeit, Kosten, Material und Abrechnungsaktivität. Alle operativen Attribute dieser Transaktionen, einschließlich Menge, Selbstkostenpreis, Verkaufspreis und Projekt, werden hier in dieser Dataverse-Entität erfasst. Weitere Informationen finden Sie unter [Istwerte](../actuals/actuals-overview.md). Istwert-Datensätze werden mit Finance and Operations-Apps mithilfe der Dual-Write-Zuordnung **Project Operations Integrationsistwerte (msdyn\_actuals) für nachgelagerte Buchhaltung synchronisiert.**

   ![Istwerteintegration.](./Media/DW4Actuals.png)

Die Tabellenzuordnung **Project Operations-Integration Istwerte** synchronisiert alle Datensätze aus der Entität **Istwerte** in Dataverse, wobei das Attribut **Synchronisierung überspringen (nur für den internen Gebrauch)** auf **False** gesetzt ist. Dieser Attributwert wird in Dataverse automatisch festgelegt, wenn der Datensatz erstellt wird. Beispiele, bei denen dieses Attribut auf **True** festgelegt ist, sind:

  - Projektkosten-Istwerte für konzerninterne Transaktionen. Weitere Informationen finden Sie unter [Erstellen unternehmensinterner Buchungen](../project-accounting/create-intercompany-transactions.md). Diese Datensätze werden übersprungen, da das System die tatsächlichen Projektkosten in Finance and Operations Apps neu erstellt, wenn die konzerninterne Lieferantenrechnung gebucht wird.
  - Negative, nicht in Rechnung gestellte Verkaufsdatensätze werden erstellt, wenn die Proforma-Rechnung bestätigt wird. Diese Datensätze werden übersprungen, da das untergeordnete Projekt-Sachkonto in Finance and Operations-Apps den nicht in Rechnung gestellten Verkaufsrekord bei der Rechnungsstellung nicht umkehrt, sondern den Status in "Vollständig in Rechnung gestellt" ändert.

Die Dual-Write-Tabellenzuordnung synchronisiert die tatsächlichen Datensätze mit der Staging-Tabelle **ProjCDSActualsImport**. Diese Datensätze werden durch den periodischen Prozess **Import aus Staging-Tabelle** beim Erstellen von Journalzeilen für die Project Operations-Integrationserfassungszeilen und Projektrechnungsvorschlagszeilen verarbeitet. Weitere Informationen finden Sie unter [Integrationsjournal in Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse erfasst auch die Verknüpfungen zwischen den tatsächlichen Transaktionen des Projekts in der **Transaktionsverbindung**-Entität. Weitere Informationen finden Sie unter [Verknüpfen der Istdaten mit Originaldatensätzen](../actuals/linkingactuals.md). Verknüpfungen zwischen tatsächlichen Transaktionen werden ebenfalls mit Finance and Operations Apps synchronisiert, die die Dual-Write-Tabellenzuordnung **Integrationsentität für die Projekttransaktion Beziehungen (msdyn\_transactionconnections)** verwenden. Diese Datensätze werden durch den periodischen Prozess **Import aus Staging-Tabelle** beim Erstellen von Journalzeilen für die Project Operations-Integrationserfassungszeilen und Projektrechnungsvorschlagszeilen verarbeitet.

Das Buchen eines Project Operations-Integrationsjournals und eines Projektrechnungsvorschlags löst eine Aktualisierung der jeweiligen Datensätze in der Staging-Tabelle **ProjCDSActualsImport** aus. Das System erfasst und zeichnet die folgenden Abrechnungsattribute für tatsächliche Transaktionen auf:

- Buchhaltungswährungsbetrag
- Wechselkurs
- Belegnummer
- Umsatzsteuerbetrag

Die Tabellenzuordnung **Project Operations-Integration Istwerte** aktualisiert die jeweiligen Istwert-Datensätze in Dataverse mit diesen Informationen.
