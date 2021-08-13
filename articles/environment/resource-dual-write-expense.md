---
title: Ausgabenverwaltungsintegration
description: Dieses Thema enthält Informationen zur Kostenberichtsintegration in Project Operations mit Dual-Write.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 06471532d2e41bb80ebf92f0a8b93c324b3f6d3e845cea8033d85d291ea237eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986580"
---
# <a name="expense-management-integration"></a>Ausgabenverwaltungsintegration

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zur Kostenberichtsintegration in Project Operations [vollständige Kostenbereitstellung](../expense/expense-overview.md) mit Dual-Write.

## <a name="expense-categories"></a>Spesenkategorien

Bei einer vollständigen Kostenbereitstellung werden Kostenkategorien in Finance and Operations Apps erstellt und verwaltet. Mit den folgenden Schritten können Sie eine neue Kostenkategorie erstellen:

1. Erstellen Sie in Microsoft Dataverse die Kategorie **Transaktion**. Durch die Dual-Write-Integration wird diese Transaktionskategorie mit Finance and Operations Apps synchronisiert. Weitere Informationen finden Sie unter [Projektkategorien konfigurieren](/dynamics365/project-operations/project-accounting/configure-project-categories) und [Project Operations-Einrichtung und Integration der Konfigurationsdaten](resource-dual-write-setup-integration.md). Als Ergebnis dieser Integration erstellt das System vier gemeinsam genutzte Kategoriedatensätze in Finance and Operations Apps.
2. Gehen Sie in Finance zu **Ausgabenmanagement** > **Einrichten** > **Gemeinsame Kategorien** und wählen Sie eine gemeinsame Kategorie mit einer **Ausgaben** Transaktionsklasse. Stellen Sie den Parameter **Kann in Ausgaben verwendet werden** auf **True** und definieren Sie die zu verwendende Aufwandsart.
3. Erstellen Sie mithilfe dieses Datensatzes für gemeinsam genutzte Kategorien eine neue Ausgabenkategorie, indem Sie zu **Ausgabenmanagement** > **Einrichten** > **Ausgabenkategorien** gehen und **Neu** auswählen. Wenn der Datensatz gespeichert wird, verwendet Dual-Write die Tabellenzuordnung **Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)**, um diesen Datensatz zu mit Dataverse synchronisieren.

  ![Ausgabenkategorienintegration.](./media/DW6ExpenseCategories.png)

Ausgabenkategorien in Finance and Operations-Apps sind unternehmensspezifisch oder juristische Person-spezifisch. Es gibt separate, zugehörige juristische Person-spezifische Datensätze in Dataverse. Wenn ein Projektmanager Ausgaben schätzt, kann er keine Ausgabenkategorien auswählen, die für ein Projekt erstellt wurden, das einem anderen Unternehmen gehört als dem Unternehmen, dem das Projekt gehört, an dem er arbeitet. 

## <a name="expense-reports"></a>Ausgabenberichte

Ausgabenberichte werden in Finance and Operations Apps erstellt und genehmigt. Weitere Informationen finden Sie unter [Erstellen und Verarbeiten der Spesenabrechnungen in Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Nachdem die Spesenabrechnung vom Projektmanager genehmigt wurde, wird sie in die Finanzbuchhaltung gebucht. In Project Operations werden projektbezogene Ausgabeberichtszeilen nach speziellen Buchungsregeln gebucht:

  - Projektbezogene Kosten (einschließlich nicht erstattungsfähiger Steuern) werden nicht sofort in der Finanzbuchhaltung auf das Projektkostenkonto gebucht, sondern auf das Kostenintegrationskonto. Dieses Konto wird in **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Project Operations in Dynamics 365 Customer Engagement** konfiguriert.
  - Dual-Write synchronisiert mit Dataverse mithilfe der Tabellenzuordnung **Project Operations-Integration Projektkosten-Exportentität (msdyn\_expenses)**.
  - Steuer-Untersachkonto, Lieferanten-Untersachkonto und andere Finanzbuchungen werden erfasst, wenn der Ausgabenbericht gebucht wird.

  ![Integration der Ausgabenabrechnungen.](./media/DW6ExpenseReports.png)

Wenn ein Datensatz in die Entität **Ausgaben** in Dataverse geschrieben wird, löst das System den automatisierten Genehmigungsprozess des Datensatzes aus. Bei Bedarf kann der Status des automatisierten Genehmigungsprozesses in Dataverse überprüft werden unter **Erweiterte Einstellungen** > **System** > **Systemjobs**. Nach Abschluss der Genehmigung werden die Ausgabenbuchungsklasse-Datensätze in der **Istwerte** Entität erstellt.

Ausgabenbezogene Istdaten werden dann unter Verwendung der Dual-Write-Tabellenzuordnung **Istwerte der Project Operations-Integration (msdyn\_actuals)** verarbeitet. Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md).

Auf Ausgabenbericht bezogene Project Operations-Integrationserfassungspositionen werden mithilfe eines periodischen Prozesses namens **Aus Stagingtabelle importieren** erstellt. Das Gegenkonto ist standardmäßig das Ausgabenintegrationskonto. Das Buchungsintegrationsjournal löscht den Kontostand für die Ausgabentransaktion und der Ausgabenbetrag wird auf das Projektkostenkonto verschoben. Vom System werden auch Buchungen des untergeordneten Projektsachkontos für nachgelagerte Fakturierungs- und Umsatzrealisierungszwecke erstellt.
