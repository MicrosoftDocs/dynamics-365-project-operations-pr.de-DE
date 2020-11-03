---
title: Eine neue Umgebung bereitstellen
description: Dieses Thema enthält Informationen zum Bereitstellen einer neuen Project Operations-Umgebung.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076411"
---
# <a name="provision-a-new-environment"></a>Eine neue Umgebung bereitstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema enthält Informationen zum Bereitstellen einer neuen Dynamics 365 Project Operations-Umgebung für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Automatisierte Project Operations-Bereitstellung in einem LCS-Projekt aktivieren

Führen Sie die folgenden Schritte aus, um den automatisierten Project Operations-Bereitstellungs-Flow für Ihr LCS-Projekt zu aktivieren.

1. Navigieren Sie zu [LCS](https://lcs.dynamics.com/v2), und wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.
2. Wählen Sie in der Liste **Vorschaufunktion** die Option **Project Operations-Funktion** und dann **Vorschaufunktion aktiviert** aus, um Project Operations zu aktivieren.

> [!NOTE]
> Dieser Schritt wird nur einmal pro LCS-Projekt ausgeführt.

## <a name="provision-a-project-operations-environment"></a>Eine Project Operations-Umgebung bereitstellen

1. Öffnen Sie eine neue Dynamics 365 Finance [Demo-Umgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) oder [Sandbox/Produktionsumgebungs-](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)Bereitstellung. 
2. Durchlaufen Sie den Assistenten zur **Umgebungsbereitstellung**. 

> [!IMPORTANT]
> Stellen Sie sicher, dass die ausgewählte Anwendungsversion 10.0.13 oder höher ist.

3. Um Project Operations bereitzustellen, wählen Sie unter **Erweiterte Einstellungen** **Common Data Service** aus. 
4. Aktivieren Sie die **Common Data Service-Einstellung** , indem Sie **Ja** auswählen und dann Informationen in die entsprechenden Felder eingeben:

  - Name des Dataflows
  - Region
  - Sprache
  - Währung
 
5. Wählen Sie im Feld **Common Data Service-Vorlage** **Project Operations** aus. 

6. Wählen Sie den Umgebungstyp für Ihre Bereitstellung aus. Mit einer abonnementbasierten Testversion können Sie eine CDS-Umgebung 30 Tage lang bereitstellen. 

![Bereitstellungseinstellungen](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Wählen Sie **Zustimmen** aus, um die Vertragsbedingungen zu bestätigen, und dann **Fertig** , um zu den Bereitstellungseinstellungen zurückzukehren.

![Bereitstellungseinwilligung](./media/2DeploymentConsent.png)

7. Füllen Sie die verbleibenden erforderlichen Felder im Assistenten aus, und bestätigen Sie die Bereitstellung. Die Zeit für die Umgebungsbereitstellung hängt vom Umgebungstyp ab. Die Bereitstellung kann bis zu sechs Stunden dauern.

  Nach erfolgreichem Abschluss der Bereitstellung wird die Umgebung als **Bereitgestellt** angezeigt.

8. Um zu bestätigen, dass die Umgebung erfolgreich bereitgestellt wurde, wählen Sie **Anmelden** aus, und melden Sie sich zur Bestätigung bei der Umgebung an.

![-Umgebungsdetails](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Project Operations Finance-Demodaten anwenden (optionaler Schritt)

Wenden Sie die Project Operations Finance-Demodaten auf die in der Cloud gehostete Umgebung Servicerelease 10.0.13, wie in [diesem Artikel](resource-apply-finance-demo-data.md) beschrieben, an.

## <a name="apply-updates-to-the-finance-environment"></a>Aktualisierungen auf die Finance-Umgebung anwenden

Project Operations erfordert eine Finance-Umgebung mit Anwendungsversion **10.0.13 (10.0.569.20009)** oder höher.

Möglicherweise müssen Sie Qualitätsupdates auf Ihre Finance-Umgebung anwenden, um diese Version zu erhalten.

1. Wählen Sie in LCS auf der Seite **Umgebungsdetails** im Abschnitt **Verfügbare Updates** die Option **Aktualisierung anzeigen** aus.

![Aktualisierungen anzeigen](./media/5ViewUpdates.png)

2. Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.

![Paket speichern](./media/6SavePackage.png)

3. Klicken Sie auf **Alle auswählen** , und wählen Sie dann **Paket speichern** aus.

![Aktualisierungen überprüfen und speichern](./media/7ReviewAndSaveUpdates.png)

4. Geben Sie einen Namen und eine Beschreibung zum Paket ein, und wählen Sie dann **Speichern** aus. Abhängig von der Internetverbindung kann dieser Vorgang einige Zeit dauern.

![Paket in Objektbibliothek hochladen](./media/8UploadPackageToAssetsLibrary.png)

5. Nachdem das Paket gespeichert wurde, wählen Sie **Fertig** aus, und speichern Sie dieses Paket in der Objektbibliothek in Ihrem LCS-Projekt.

Das Speichern und Validieren des Pakets kann ca. 15 Minuten dauern.

6. Um das Update anzuwenden, navigieren Sie zur Seite **Umgebungsdetails** in LCS und wählen Sie **Verwalten** > **Aktualisierungen übernehmen** aus.

![Umgebungen verwalten](./media/9MaintainEnvironment.png)

7. Wählen Sie in der Aktualisierungsliste das von Ihnen erstellte Paket und dann **Anwenden** aus.

![Aktualisierungen anwenden](./media/10ApplyUpdates.png)

Die Wartung der Umgebung wird einige Zeit dauern. Nach Abschluss des Vorgangs kehrt die Umgebung in den bereitgestellten Zustand zurück.

![Umgebungen bereitgestellt](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Eine Dual-Write-Verbindung herstellen 

1. Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.
2. Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.
3. Nachdem der Link vollständig ist, wählen Sie erneut **Link zu CDS für Apps** aus. Sie werden zu Dual Write in Finance weitergeleitet.

![Mit CDS verknüpfen](./media/12LinktoCDS.png)

4. Wählen Sie **Lösung anwenden** aus, um auf die Entitäten zuzugreifen, die in der Integration zugeordnet werden.

![Lösungen anwenden](./media/13ApplySolutions.png)

5. Wählen Sie beide Lösungen, **Dynamics 365 Finance and Operations Dual Write Entity Map** und **Dynamics 365 Project Operations Dual Write Entity Maps** und dann **Anwenden** aus.

![Lösungen bestätigen](./media/14ConfirmSolutions.png)

Nachdem die Lösungen angewendet wurden, werden die Dual Write-Entitäten auf die Umgebung angewendet.

![Anwenden von Lösungen](./media/15ApplyingSolutions.png)

Nachdem die Entitäten angewendet wurden, werden alle verfügbaren Zuordnungen in der Umgebung aufgelistet.

![Zuordnungen für duales Schreiben](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Die Datenentitäten nach der Aktualisierung aktualisieren

1. Navigieren Sie in Finance zum Arbeitsbereich **Datenverwaltung**.

![Datenverwaltungsarbeitsbereich](./media/16DataManagement.png)

2. Wählen Sie die Kachel **Framework-Parameter** aus.

![Framework-Parameter](./media/17FrameworkParameters.png)

3. Wählen Sie auf der Seite **Entitätseinstellungen** die Option **Entitätsliste aktualisieren** aus.

![Entitätsliste aktualisieren](./media/18RefreshEntityList.png)

Die Aktualisierung dauert ungefähr 20 Minuten. Sie erhalten eine Benachrichtigung, wenn der Vorgang abgeschlossen ist.

![Bestätigung aktualisieren](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Duales Schreiben für Project Operations-Zuordnungen ausführen

1. Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.
2. Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus. Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.
3. Starten Sie die Zuordnungen wie in der folgenden Tabelle beschrieben. Stellen Sie sicher, dass Sie die angegebene Reihenfolge einhalten.

| **Entitätszuordnung** | **Entität aktualisieren** | **Erste Synchronisierung** | **Master für Erstsynchronisierung** | **Voraussetzungen ausführen** | **Voraussetzungen für Erstsynchronisierung** |
| --- | --- | --- | --- | --- | --- |
| **Projektressourcenrollen für alle Unternehmen(bookableresourcecategories)** | Nr. | Ja | Common Data Service | Nr. | Nicht zutreffend |
| **Juristische Personen (cdm\_companies)** | Nr. | Ja | Finance and Operations-Apps | Nr. | Nicht zutreffend |
| **Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)** | Nr. | Nr. | Nicht zutreffend | Ja | Nr. |
| **Projektvertragszeilen (salesorderdetails)** | Nr. | Nr. | Nicht zutreffend | Nr. | Nr. |
| **Integrationsentität für die Projekttransaktionsbeziehungen (msdyn\_transactionconnections)** | Nr. | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |
| **Vertragszeilenmeilensteine der Project Operations-Integration (msdyn\_contractlinesscheduleofvalues)** | Nr. | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |
| **Project Operations-Integrationsentität für Ausgabenschätzungen (msdyn\_estimateslines)** | Nr. | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |
| **Exportentität für Projektkostenkategorien der Project Operations-Integration (msdyn\_expensecategories)** | Nr. | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |
| **Exportentität für Projektkosten der Project Operations-Integration (msdyn\_expenses)** | Ja | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |
| **Project Operations-Integrationsentität für Stundenschätzungen (msdyn\_resourceassignments)** | Ja | Nr. | Nicht zutreffend | Nr. | Nicht zutreffend |


4. Um die Entität zu aktualisieren, wählen Sie den Zuordnungsnamen und dann **Entitäten aktualisieren** aus. 


![Zuordnung aktualisieren](./media/20RefreshMapping.png)

5. Führen Sie nach dem Abschluss der Aktualisierung die Zuordnung aus. Bevor Sie die nächste Zuordnung aktivieren, stellen Sie sicher, dass sich die Zuordnung in der Tabelle im Status **Wird ausgeführt** befindet. Das Ausführen von Zuordnungen mit einer größeren Anzahl von Voraussetzungen kann einige Zeit dauern.

Um eine Zuordnung mit Voraussetzungen auszuführen, aktivieren Sie die Umschalttaste **Zugehörige Entitätszuordnungen anzeigen**. Wenn die Tabelle angibt, dass **Voraussetzungen für die Erstsynchronisierung** auf **Nein** festgelegt ist, stellen Sie sicher, dass die Kennzeichnung **Erstsynchronisation** in allen erforderlichen Voraussetzungszuordnungen auf **Aus** festgelegt ist, bevor Sie sie ausführen.

![Zuordnung ausführen](./media/21RunMap.png)

6. Überprüfen Sie, ob alle projektbezogenen Zuordnungen sich im Status „Wird ausgeführt“ befinden.

![Alle Zuordnungen werden ausgeführt](./media/22AllMapsRunning.png)

Ihre Project Operations-Umgebung ist jetzt bereitgestellt und konfiguriert.
