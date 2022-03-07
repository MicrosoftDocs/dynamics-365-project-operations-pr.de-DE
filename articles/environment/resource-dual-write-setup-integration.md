---
title: Project Operations-Einrichtung und Konfigurationsdatenintegration
description: Dieses Thema enthält Informationen zum Einrichten und Konfigurieren von Dual-Write-Zuordnungen für Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986535"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Project Operations-Einrichtung und Konfigurationsdatenintegration

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zu den Einrichtungs- und Konfigurationsentitäten zur Dual-Write-zur Integration für Project Operations.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektverträge, Vertragszeilen und Projekte

Projektverträge, Vertragszeilen und Projekte werden in Dataverse erstellt und mit Finance and Operations Apps für zusätzliche Buchhaltung synchronisiert. Die Datensätze in diesen Entitäten können nur in Dataverse erstellt und gelöscht werden. Buchhaltungsattribute wie Standardwerte für Umsatzsteuergruppen und finanzielle Dimensionen können diesen Datensätzen jedoch in Finance and Operations Apps hinzugefügt werden.

  ![Integrationskonzepte für Projektverträge.](./media/1ProjectContract.jpg)

Leads, Verkaufschancen und Angebote für Vertriebsaktivitäten werden in Dataverse nachverfolgt und werden nicht mit Finance and Operations-Apps synchronisiert, da dieser Aktivität keine nachgelagerte Buchhaltung zugeordnet ist.

Die Projektvertragsfunktionalität in Dataverse erstellt einen Projektvertragsdatensatz in Finance and Operations-Apps mit der Tabellenzuordnung **Projektvertragskopfzeilen (salesorders)**. Speichern eines Projektvertrags in Dataverse startet auch die Erstellung eines Projektvertrags-Kundenentitätsdatensatzes. Dieser Datensatz wird mit Finance and Operations Apps mit der Tabellenzuordnung **Projektfinanzierungsquelle (msdyn\_ projectcontractssplitbillingrules)** synchronisiert. Diese Zuordnung synchronisiert auch das Hinzufügen, Aktualisieren und Löschen von Projektvertragskunden. Geteilte Abrechnungsprozentsätze zwischen Projektvertragskunden werden nur in Dataverse ausgeführt und nicht mit Finance and Operations Apps synchronisiert.

Nachdem ein Projektvertrag in Dataverse erstellt wurde, kann der Projektbuchhalter die Buchhaltungsattribute für diesen Projektvertrag in Finance and Operations Apps aktualisieren, und zwar unter **Projektmanagement und Buchhaltung** > **Projektverträge** > **Einrichten** > **Standardabrechnung anzeigen**. Der Buchhalter kann die operativen Projektvertragsattribute wie den angeforderten Liefertermin und den Vertragsbetrag überprüfen, indem er die Projektvertrags-ID in Finance and Operations Apps auswählt, die den zugehörigen Projektvertragsdatensatz in Dataverse öffnet.

Die Projektentität wird mit Finance and Operations Apps mit der Tabellenzuordnung **Projekte V2 (msdyn\_projects)** synchronisiert. Der Projektbuchhalter kann:

  - Überprüfen Sie Projekte in Finance and Operations Apps, indem Sie zu **Projektmanagement und Buchhaltung** > **Alle Projekte** gehen. 
  - Aktualisieren Sie die Abrechnungsattribute für das Projekt in Finance and Operations Apps, indem Sie zu **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Einrichten** > **Standardabrechnung anzeigen** gehen.  
  - Überprüfen Sie die operativen Projektattribute, z. B. das geschätzte Start- und Enddatum, indem Sie die Projekt-ID in Finance and Operations Apps auswählen, die den zugehörigen Projektdatensatz in Dataverse öffnet.

Ein Projekt ist mit einem Projektvertrag über die Entität **Projektvertragszeile** verbunden.

Die Projektvertragszeilen in Dataverse erstellt eine Projektvertragsabrechnungsregel in Finance and Operations-Apps mit der Tabellenzuordnung **Projektvertragszeilen (salesorderdetails)**. Die Abrechnungsmethode definiert den Abrechnungsregeltyp des Projektvertrags in Finance and Operations Apps:

  - Projektvertragszeilen mit einer Abrechnungsmethode für Zeit und Material erstellen eine Abrechnungsregel für Zeit und Materialart.
  - Festpreis-Abrechnungsmethode Vertragslinien erstellen eine Meilenstein-Abrechnungsregel.

Projektvertragslinien können vom Projektbuchhalter in Finance and Operations Apps überprüft werden, indem Sie zu **Projektmanagement und Buchhaltung** > **Projektverträge** > **Einrichten** > **Standardabrechnung anzeigen** und Details auf der Registerkarte überprüfen **Vertragszeilen**. Auf dieser Registerkarte kann der Buchhalter auch finanzielle Standarddimensionen für die Vertragszeilen der Festpreisabrechnungsmethode festlegen.

## <a name="billing-milestones"></a>Fakturierungsmeilensteine

Projektvertragszeilen nach der Festpreis-Abrechnungsmethode werden über Abrechnungsmeilensteine in Rechnung gestellt. Abrechnungsmeilensteine werden synchronisiert, um Buchungen auf dem Konto in Finance and Operations-Apps mit der Tabellenzuordnung **Vertragszeilen-Meilensteine der Project Operations-Integration (msdyn\_ contractlinescheduleofvalues)**.

  ![Integration der Fakturierungsmeilensteine.](./media/2Milestones.jpg)

Der Buchhalter kann Transaktionen auf dem Konto überprüfen und die Buchhaltungsattribute für diese Transaktionen anpassen, indem er zu **Projektmanagement und Buchhaltung** > **Projektverträge** > **Pflegen** > **Transaktionen auf Rechnung** oder **Projektmanagement und Buchhaltung** > **Alle Projekte** > **Pflegen** > **Transaktionen auf Rechnung** geht.

Wenn Sie zum ersten Mal einen Abrechnungsmeilenstein für eine bestimmte Projektvertragszeile erstellen, erstellt das System automatisch ein Projekt zur Schätzung des Festpreisumsatzes für das dieser Vertragslinie zugeordnete Projekt. Projekte zur Schätzung des Festpreisumsatzes können unter **Projektmanagement und Buchhaltung** > **Projekte zur Schätzung von Festpreiseinnahmen** überprüft werden.

### <a name="project-tasks"></a>Projektaufgaben

Projektaufgaben werden mit Finance and Operations Apps durch die Tabellenzuordnung **Projektaufgaben (msdyn\_ Projektaufgaben)** nur zu Referenzzwecken synchronisiert. Das Erstellen, Aktualisieren und Löschen von Vorgängen durch Finance and Operations-Apps wird nicht unterstützt.

  ![Projektaufgabenintegration.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektressourcen

Die Entität **Projektressourcenrollen** wird mit Finance and Operations Apps mit der Tabellenzuordnung **Projektressourcenrollen für alle Unternehmen (bookableresourcecategories)** nur zu Referenzzwecken synchronisiert. Weil Ressourcenrollen in Dataverse nicht unternehmensspezifisch sind, erstellt das System automatisch entsprechende unternehmensspezifische Ressourcenrollendatensätze in Finance and Operations Apps für alle juristischen Personen, die in den Dual-Write-Integrationsbereich aufgenommen wurden.

![Ressourcenrollenintegration.](./media/5Resources.jpg)

Projektressourcen im Project Operations werden in Dataverse verwaltet und sind nicht mit Finance and Operations Apps synchronisiert.

### <a name="transaction-categories"></a>Transaktionskategorien

Transaktionskategorien werden in Dataverse gepflegt und mit Finance and Operations Apps mit der Tabellenzuordnung **Projekttransaktionskategorien (msdyn\_transactioncategories)** synchronisiert. Nachdem der Transaktionskategoriedatensatz synchronisiert wurde, erstellt das System automatisch vier gemeinsam genutzte Kategoriedatensätze. Jeder Datensatz entspricht einem Transaktionstyp in Finance and Operations Apps und verknüpft sie mit dem Transaktionskategoriedatensatz.

![Transaktionskategorienintegration.](./media/4TransactionCategories.jpg)

Für die Verwendung von Transaktionskategorien für Schätzungen und Istwerte muss der Projektbuchhalter oder das System Administrator in jeder juristischen Person entsprechende Projektkategorien erstellen. Weitere Informationen finden Sie unter [Produktkategorien konfigurieren](../project-accounting/configure-project-categories.md).
