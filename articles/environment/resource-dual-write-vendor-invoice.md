---
title: Zuliefererrechnungsintegration
description: Dieses Thema enthält Informationen zur Zuliefererrechnungsintegration in Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955754"
---
# <a name="vendor-invoice-integration"></a>Zuliefererrechnungsintegration

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Projektbezogene Beschaffung in Dynamics 365 Project Operations kann aufgezeichnet werden, indem Sie zu **Kreditoren** > **Rechnungen** > **Ausstehende Lieferantenrechnungen** gehe und einen ausstehenden Lieferantenrechnungsbeleg verwenden. Weitere Informationen finden Sie unter [Beschaffen von nicht vorrätigen Materialien mithilfe einer ausstehenden Lieferantenrechnung](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Bevor Sie die in diesem Thema beschriebenen Funktionen verwenden, überprüfen Sie die erforderlichen Konfigurationen und wenden Sie sie an. Weitere Informationen finden Sie unter [Aktivieren von nicht vorrätigen Materialien und ausstehenden Lieferantenrechnungen](../procurement/configure-materials-nonstocked.md).

In Project Operations werden projektbezogene Lieferantenrechnungen nach speziellen Buchungsregeln gebucht:

- Projektbezogene Kosten (einschließlich nicht erstattungsfähiger Steuern) werden nicht sofort in der Finanzbuchhaltung auf das Projektkostenkonto gebucht. Stattdessen werden die Kosten auf das **Beschaffungsintegrationskonto** gebucht. Dieses Konto wird in **Projektmanagement und Buchhaltung** > **Einrichten** > **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Project Operations in Dynamics 365 Customer Engagement** konfiguriert.
- Dual-Write synchronisiert die Rechnungsdetails des Lieferanten mit Microsoft Dataverse unter Verwendung der folgenden Tabellenkarten:

     - **Project Operations Integrationsprojektanbieter-Rechnungsexportentität (msdyn_projectvendorinvoices)**: Diese Tabellenzuordnung synchronisiert die Rechnungskopfinformationen des Anbieters. Es werden nur Lieferantenrechnungen mit mindestens einer Zeile, die eine Projekt-ID enthält, mit Dataverse synchronisiert.
     - **Project Operations Integrationsprojektanbieter-Rechnungsexportzeilen-Entität (msdyn_projectvendorinvoicelines)**: Diese Tabellenzuordnung synchronisiert die Rechnungszeilenformationen des Anbieters. Es werden nur Zeilen mit einer Projekt-ID mit Dataverse synchronisiert.

     > [!NOTE]
     > Angaben zur Lieferantenrechnung in Dataverse sind nicht bearbeitbar.

Steuer-Untersachkonto, Lieferanten-Untersachkonto und andere Finanzbuchungen werden in Dynamics 365 Finance erfasst, wenn die Lieferantenrechnung gebucht wird.

![Zuliefererrechnungsintegration](media/DW7VendorInvoice.png)

Wenn Datensätze in eine **Lieferantenrechnung**-Entität in Dataverse geschrieben werden, beginnt ein automatisierter Genehmigungsprozess der Datensätze. Bei Bedarf kann der Status des automatisierten Genehmigungsprozesses in Dataverse überprüft werden unter **Erweiterte Einstellungen** > **System** > **Systemjobs**. Nach Abschluss der Genehmigung erstellt das System Materialbuchungsklassen-Datensätze in der **Istwerte** Entität.

Materialbezogene Istdaten werden dann unter Verwendung der Dual-Write-Tabellenzuordnung **Istwerte der Project Operations-Integration (msdyn_actuals)** verarbeitet. Weitere Informationen finden Sie unter [Projektvorkalkulationen und Ist-Werte](resource-dual-write-estimates-actuals.md).

Auf Lieferantenrechnung bezogene Project Operations-Integrationserfassungspositionen werden mithilfe eines periodischen Prozesses namens **Aus Stagingtabelle importieren** erstellt. Das Gegenkonto ist standardmäßig das Beschaffungsintegrationskonto. Wenn das Integrationsjournal gebucht wird, wird der Kontostand für die Lieferantenrechnungstransaktion gelöscht und der Zeilenbetrag auf das Projektkostenkonto verschoben. Buchungen des untergeordneten Projektsachkontos werden auch für nachgelagerte Fakturierungs- und Umsatzrealisierungszwecke erstellt.
