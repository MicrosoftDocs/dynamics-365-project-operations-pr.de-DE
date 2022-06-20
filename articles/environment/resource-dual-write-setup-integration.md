---
title: Project Operations-Einrichtung und Konfigurationsdatenintegration
description: Dieser Artikel informiert Sie über die Einrichtung und Konfiguration von Dual-write Zuordnungen in Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 173ff01e938af48d2d6488d5e59cf4e74b3af8e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914539"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations-Einrichtung und Konfigurationsdatenintegration

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieser Artikel enthält Informationen über die Project Operations Dual-write Integration für Einrichtung und Konfiguration von Entitäten.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektverträge, Vertragszeilen und Projekte

Projektverträge, Vertragspositionen und Projekte werden in Dataverse erstellt und für zusätzliche Buchhaltung mit Finanz- und Betriebs-Apps synchronisiert. Die Datensätze in diesen Entitäten können nur in Dataverse erstellt und gelöscht werden. Buchhaltungsattribute wie Mehrwertsteuergruppenvorgaben und Finanzdimensionen können diesen Datensätzen jedoch in den Finanz- und Betriebs-Apps hinzugefügt werden.

  ![Integrationskonzepte für Projektverträge.](./media/1ProjectContract.jpg)

Verkaufsaktivitäts-Leads, Verkaufschancen und Angebote werden in Dataverse nachverfolgt und nicht mit Finanz- und Betriebs-Apps synchronisiert, da dieser Aktivität keine nachgelagerte Buchhaltung zugeordnet ist.

Die Projektvertragsfunktion in Dataverse erstellt einen Projektvertragsdatensatz in Finanz- und Betriebs-Apps mithilfe der Tabellenzuordnung **Projektvertragsheader (Kundenaufträge)**. Speichern eines Projektvertrags in Dataverse startet auch die Erstellung eines Projektvertrags-Kundenentitätsdatensatzes. Dieser Datensatz wird mithilfe der Tabellenzuordnung **Projektfinanzierungsquelle (msdyn\_projectcontractssplitbillingrules)** mit Finanz- und Betriebs-Apps synchronisiert. Diese Zuordnung synchronisiert auch das Hinzufügen, Aktualisieren und Löschen von Projektvertragskunden. Aufgeteilte Abrechnungsprozentsätze zwischen Projektvertragskunden werden nur in Dataverse verwaltet und nicht mit Finanz- und Betriebs-Apps synchronisiert.

Nachdem ein Projektvertrag in Dataverse erstellt wurde, kann der Projektbuchhalter die Buchhaltungsattribute für diesen Projektvertrag in Finanz- und Betriebs-Apps aktualisieren, indem er zu **Projektmanagement und Rechnungswesen** > **Projektverträge** > **Konfiguration** > **Standardbuchhaltung anzeigen** wechselt. Der Buchhalter kann operative Projektvertragsattribute wie das gewünschte Lieferdatum und den Vertragsbetrag überprüfen, indem er die Projektvertrags-ID in den Finanz- und Betriebs-Apps auswählt, wodurch der zugehörige Projektvertragsdatensatz in Dataverse geöffnet wird.

Die Projektentität wird mithilfe der Tabellenzuordnung **Projekte V2 (msdyn\_projects)** mit Finanz- und Betriebs-Apps synchronisiert. Der Projektbuchhalter kann:

  - Überprüfen Sie Projekte in Finanz- und Betriebs-Apps, indem Sie zu **Projektmanagement und Rechnungswesen** > **Alle Projekte** wechseln. 
  - Aktualisieren Sie Buchhaltungsattribute für das Projekt in Finanz- und Betriebs-Apps, indem Sie zu **Projektmanagement und Rechnungswesen** > **Alle Projekte** > **Konfiguration** > **Standardbuchhaltung anzeigen** wechseln.  
  - Überprüfen Sie operative Projektattribute wie geschätzte Start- und Enddaten, indem Sie die Projekt-ID in Finanz- und Betriebs-Apps auswählen, die den zugehörigen Projektdatensatz in Dataverse öffnen.

Ein Projekt ist mit einem Projektvertrag über die Entität **Projektvertragszeile** verbunden.

Projektvertragspositionen in Dataverse erstellen eine Projektvertragsabrechnungsregel in Finanz- und Betriebs-Apps mithilfe der Tabellenzuordnung **Projektvertragspositionen (salesorderdetails)**. Die Abrechnungsmethode definiert den Abrechnungsregeltyp des Projektvertrags in Finanz- und Betriebs-Apps:

  - Projektvertragszeilen mit einer Abrechnungsmethode für Zeit und Material erstellen eine Abrechnungsregel für Zeit und Materialart.
  - Festpreis-Abrechnungsmethode Vertragslinien erstellen eine Meilenstein-Abrechnungsregel.

Projektvertragspositionen können vom Projektbuchhalter in Finanz- und Betriebs-Apps überprüft werden, indem Sie zu **Projektmanagement und Rechnungswesen** > **Projektverträge** > **Konfiguration** > **Standardbuchhaltung anzeigen** wechseln und die Details auf der Registerkarte **Vertragspositionen** überprüfen. Der Buchhalter kann auf dieser Registerkarte auch Standardfinanzdimensionen für die Vertragspositionen der Festpreisabrechnungsmethode festlegen.

## <a name="billing-milestones"></a>Fakturierungsmeilensteine

Projektvertragszeilen nach der Festpreis-Abrechnungsmethode werden über Abrechnungsmeilensteine in Rechnung gestellt. Abrechnungsmeilensteine werden mithilfe der Tabellenzuordnung **Meilensteine der Project Operations-Integrationsvertragslinie (msdyn\_contractlinescheduleofvalues)** mit Projektakontotransaktionen in Finanz- und Betriebs-Apps synchronisiert.

  ![Integration der Fakturierungsmeilensteine.](./media/2Milestones.jpg)

Der Buchhalter kann Transaktionen auf dem Konto überprüfen und die Buchhaltungsattribute für diese Transaktionen anpassen, indem er zu **Projektmanagement und Buchhaltung** > **Projektverträge** > **Pflegen** > **Transaktionen auf Rechnung** oder **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Pflegen** > **Transaktionen auf Rechnung** geht.

Wenn Sie zum ersten Mal einen Abrechnungsmeilenstein für eine bestimmte Projektvertragszeile erstellen, erstellt das System automatisch ein Projekt zur Schätzung des Festpreisumsatzes für das dieser Vertragslinie zugeordnete Projekt. Projekte zur Schätzung des Festpreisumsatzes können unter **Projektmanagement und Buchhaltung** > **Projekte zur Schätzung von Festpreiseinnahmen** überprüft werden.

### <a name="project-tasks"></a>Projektaufgaben

Projektaufgaben werden über die Tabellenzuordnung **Projektaufgaben (msdyn\_projecttasks)** nur zu Referenzzwecken mit Finanz- und Betriebs-Apps synchronisiert. Das Erstellen, Aktualisieren und Löschen von Vorgängen wird von Finanz- und Betriebs-Apps nicht unterstützt.

  ![Projektaufgabenintegration.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektressourcen

Die **Projektressourcenrollen**-Entität wird mithilfe der Tabellenzuordnung **Projektressourcenrollen für alle Unternehmen (bookableresourcecategories)** nur zu Referenzzwecken mit Finanz- und Betriebs-Apps synchronisiert. Da Ressourcenrollen in Dataverse nicht unternehmensspezifisch sind, erstellt das System automatisch entsprechende unternehmensspezifische Ressourcenrollendatensätze in Finanz- und Betriebs-Apps für alle Entitäten, die in den Dual-Write-Integrationsumfang eingeschlossen sind.

![Ressourcenrollenintegration.](./media/5Resources.jpg)

Projektressourcen in Project Operations werden in Dataverse verwaltet und nicht mit Finanz- und Betriebs-Apps synchronisiert.

### <a name="transaction-categories"></a>Transaktionskategorien

Transaktionskategorien werden in Dataverse gepflegt und mithilfe der Tabellenzuordnung **Projektbuchungskategorien (msdyn\_transactioncategories)** mit Finanz- und Betriebs-Apps synchronisiert. Nachdem der Transaktionskategoriedatensatz synchronisiert wurde, erstellt das System automatisch vier gemeinsam genutzte Kategoriedatensätze. Jeder Datensatz entspricht einem Transaktionstyp in Finanz- und Betriebs-Apps und verknüpft sie mit dem Datensatz der Transaktionskategorie.

![Transaktionskategorienintegration.](./media/4TransactionCategories.jpg)

Für die Verwendung von Transaktionskategorien für Schätzungen und Istwerte muss der Projektbuchhalter oder das System Administrator in jeder juristischen Person entsprechende Projektkategorien erstellen. Weitere Informationen finden Sie unter [Produktkategorien konfigurieren](../project-accounting/configure-project-categories.md).
