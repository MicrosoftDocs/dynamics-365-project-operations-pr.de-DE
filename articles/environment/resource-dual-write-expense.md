---
title: Ausgabenverwaltungsintegration
description: Dieser Artikel enthält Informationen über die Integration von Spesenabrechnungen in Project Operations mit Dual-write.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e11f1cfd714212691146eed59bcfb5b5facd750c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029208"
---
# <a name="expense-management-integration"></a>Ausgabenverwaltungsintegration

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel enthält Informationen über die Integration von Spesenabrechnungen in Project Operations [Vollständige Bereitstellung von Spesen](../expense/expense-overview.md) unter Verwendung von Dual-write.

## <a name="expense-categories"></a>Spesenkategorien

Bei einer vollständigen Ausgabenbereitstellung werden Ausgabenkategorien in Finanz- und Betriebs-Apps erstellt und verwaltet. Mit den folgenden Schritten können Sie eine neue Kostenkategorie erstellen:

1. Erstellen Sie in Microsoft Dataverse die Kategorie **Transaktion**. Die Integration für duales Schreiben synchronisiert diese Transaktionskategorie mit Finanz- und Betriebs-Apps. Weitere Informationen finden Sie unter [Projektkategorien konfigurieren](/dynamics365/project-operations/project-accounting/configure-project-categories) und [Project Operations-Einrichtung und Integration der Konfigurationsdaten](resource-dual-write-setup-integration.md). Als Ergebnis dieser Integration erstellt das System vier freigegebene Kategoriedatensätze in Finanz- und Betriebs-Apps.
2. Gehen Sie in Finance zu **Ausgabenmanagement** > **Einrichten** > **Gemeinsame Kategorien** und wählen Sie eine gemeinsame Kategorie mit einer **Ausgaben** Transaktionsklasse. Stellen Sie den Parameter **Kann in Ausgaben verwendet werden** auf **True** und definieren Sie die zu verwendende Aufwandsart.
3. Erstellen Sie mithilfe dieses Datensatzes für gemeinsam genutzte Kategorien eine neue Ausgabenkategorie, indem Sie zu **Ausgabenmanagement** > **Einrichten** > **Ausgabenkategorien** gehen und **Neu** auswählen. Wenn der Datensatz gespeichert wird, verwendet Dual-Write die Tabellenzuordnung **Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)**, um diesen Datensatz zu mit Dataverse synchronisieren.

  ![Ausgabenkategorienintegration.](./media/DW6ExpenseCategories.png)

Ausgabenkategorien in Finanz- und Betriebs-Apps sind spezifisch für das Unternehmen oder die juristische Person. Es gibt separate, zugehörige juristische Person-spezifische Datensätze in Dataverse. Wenn ein Projektmanager Ausgaben schätzt, kann er keine Ausgabenkategorien auswählen, die für ein Projekt erstellt wurden, das einem anderen Unternehmen gehört als dem Unternehmen, dem das Projekt gehört, an dem er arbeitet. 

## <a name="expense-reports"></a>Ausgabenberichte

Spesenabrechnungen werden in Finanz- und Betriebs-Apps erstellt und genehmigt. Weitere Informationen finden Sie unter [Erstellen und Verarbeiten der Spesenabrechnungen in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Nachdem die Spesenabrechnung vom Projektmanager genehmigt wurde, wird sie in die Finanzbuchhaltung gebucht. In Project Operations werden projektbezogene Ausgabeberichtszeilen nach speziellen Buchungsregeln gebucht:

  - Projektbezogene Kosten (einschließlich nicht erstattungsfähiger Steuern) werden nicht sofort in der Finanzbuchhaltung auf das Projektkostenkonto gebucht, sondern auf das Kostenintegrationskonto. Dieses Konto wird in **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Project Operations in Dynamics 365 Customer Engagement** konfiguriert.
  - Dual-Write synchronisiert mit Dataverse mithilfe der Tabellenzuordnung **Project Operations-Integration Projektkosten-Exportentität (msdyn\_expenses)**.
  - Steuer-Untersachkonto, Lieferanten-Untersachkonto und andere Finanzbuchungen werden erfasst, wenn der Ausgabenbericht gebucht wird.

  ![Integration der Ausgabenabrechnungen.](./media/DW6ExpenseReports.png)

Wenn ein Datensatz in die Entität **Ausgaben** in Dataverse geschrieben wird, löst das System den automatisierten Genehmigungsprozess des Datensatzes aus. Bei Bedarf kann der Status des automatisierten Genehmigungsprozesses in Dataverse überprüft werden unter **Erweiterte Einstellungen** > **System** > **Systemjobs**. Nach Abschluss der Genehmigung werden die Ausgabenbuchungsklasse-Datensätze in der **Istwerte** Entität erstellt.

Ausgabenbezogene Istdaten werden dann unter Verwendung der Dual-Write-Tabellenzuordnung **Istwerte der Project Operations-Integration (msdyn\_actuals)** verarbeitet. Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md).

Auf Ausgabenbericht bezogene Project Operations-Integrationserfassungspositionen werden mithilfe eines periodischen Prozesses namens **Aus Stagingtabelle importieren** erstellt. Das Gegenkonto ist standardmäßig das Ausgabenintegrationskonto. Das Buchungsintegrationsjournal löscht den Kontostand für die Ausgabentransaktion und der Ausgabenbetrag wird auf das Projektkostenkonto verschoben. Vom System werden auch Buchungen des untergeordneten Projektsachkontos für nachgelagerte Fakturierungs- und Umsatzrealisierungszwecke erstellt.
