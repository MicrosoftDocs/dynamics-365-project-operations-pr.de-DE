---
title: Eine neue Umgebung bereitstellen
description: In diesem Artikel erfahren Sie, wie Sie eine neue Umgebung für Project Operations bereitstellen.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 78f40ebe79c038799fbc59902442ad6c23fb94d4
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028517"
---
# <a name="provision-a-new-environment"></a>Eine neue Umgebung bereitstellen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_



In diesem Artikel erfahren Sie, wie Sie eine neue Dynamics 365 Project Operations-Umgebung für ressourcenbasierte/nicht vorrätige Szenarien bereitstellen.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Automatisierte Project Operations-Bereitstellung in einem LCS-Projekt aktivieren

Führen Sie die folgenden Schritte aus, um den automatisierten Project Operations-Bereitstellungs-Flow für Ihr LCS-Projekt zu aktivieren.

1. Navigieren Sie zu [LCS](https://lcs.dynamics.com/v2), und wählen Sie die Kachel **Verwaltung von Vorschaufunktionen** aus.
2. Wählen Sie in der Liste **Vorschaufunktion** die Option **Project Operations-Funktion** und dann **Vorschaufunktion aktiviert** aus, um Project Operations zu aktivieren.

   > [!NOTE]
   > Dieser Schritt wird nur einmal pro LCS-Projekt ausgeführt.

## <a name="provision-a-project-operations-environment"></a>Eine Project Operations-Umgebung bereitstellen

1. Öffnen Sie eine neue Dynamics 365 Finance-[Demoumgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) oder [Sandbox-/Produktionsumgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure)-Bereitstellung. 
2. Durchlaufen Sie den Assistenten zur **Umgebungsbereitstellung**. 

   > [!IMPORTANT]
   > Stellen Sie sicher, dass die ausgewählte Anwendungsversion 10.0.13 oder höher ist.

3. Um Project Operations bereitzustellen, wählen Sie unter **Erweiterte Einstellungen** **Common Data Service** aus. 
4. Aktivieren Sie die **Common Data Service-Einstellung**, indem Sie **Ja** auswählen und dann Informationen in die entsprechenden Felder eingeben:

  - Name des Dataflows
  - Region
  - Sprache
  - Währung
 
5. Wählen Sie im Feld **Common Data Service-Vorlage** **Project Operations** aus. 
6. Wählen Sie den Umgebungstyp für Ihre Bereitstellung aus. Mit einer abonnementbasierten Testversion können Sie eine CDS-Umgebung 30 Tage lang bereitstellen. 

     ![Bereitstellungseinstellungen.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Wählen Sie **Zustimmen** aus, um die Vertragsbedingungen zu bestätigen, und dann **Fertig**, um zu den Bereitstellungseinstellungen zurückzukehren.
    >
    >![Bereitstellungseinwilligung.](./media/2DeploymentConsent.png)

7. Optional – Wenden Sie Demodaten auf die Umgebung an. Gehen Sie zu **Erweiterte Einstellungen**, wählen Sie **Passen Sie die SQL-Datenbankkonfiguration an** und setzen **Geben Sie ein DataSet für die Anwendungsdatenbank an** auf **Demo**.
8. Füllen Sie die verbleibenden erforderlichen Felder im Assistenten aus, und bestätigen Sie die Bereitstellung. Die Zeit zum Bereitstellen der Umgebung hängt vom Umgebungstyp ab. Die Bereitstellung kann bis zu sechs Stunden dauern.

   Nach erfolgreichem Abschluss der Bereitstellung wird die Umgebung als **Bereitgestellt** angezeigt.

9. Um zu bestätigen, dass die Umgebung erfolgreich bereitgestellt wurde, wählen Sie **Anmeldung** und melden Sie sich zur Bestätigung bei der Umgebung an.

    ![Umgebungsdetails.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aktualisierungen auf die Finance-Umgebung anwenden

Project Operations erfordert eine Finance-Umgebung mit Anwendungsversion **10.0.13 (10.0.569.20009)** oder höher.

Möglicherweise müssen Sie Qualitätsupdates auf Ihre Finance-Umgebung anwenden, um diese Version zu erhalten.

1. Wählen Sie in LCS auf der Seite **Umgebungsdetails** im Abschnitt **Verfügbare Updates** die Option **Aktualisierung anzeigen** aus.

    ![Aktualisierungen anzeigen.](./media/5ViewUpdates.png)

2. Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.

    ![Paket speichern.](./media/6SavePackage.png)

3. Klicken Sie auf **Alle auswählen**, und wählen Sie dann **Paket speichern** aus.

    ![Aktualisierungen überprüfen und speichern.](./media/7ReviewAndSaveUpdates.png)

4. Geben Sie einen Namen und eine Beschreibung zum Paket ein, und wählen Sie dann **Speichern** aus. Abhängig von der Internetverbindung kann dieser Vorgang einige Zeit dauern.

    ![Paket in Objektbibliothek hochladen.](./media/8UploadPackageToAssetsLibrary.png)

5. Nachdem das Paket gespeichert wurde, wählen Sie **Fertig** aus, und speichern Sie dieses Paket in der Objektbibliothek in Ihrem LCS-Projekt.

   Das Speichern und Validieren des Pakets kann ca. 15 Minuten dauern.

6. Um das Update anzuwenden, navigieren Sie zur Seite **Umgebungsdetails** in LCS und wählen Sie **Verwalten** > **Aktualisierungen übernehmen** aus.

    ![Umgebungen verwalten.](./media/9MaintainEnvironment.png)

7. Wählen Sie in der Aktualisierungsliste das von Ihnen erstellte Paket und dann **Anwenden** aus.

    ![Aktualisierungen anwenden.](./media/10ApplyUpdates.png)

   Die Wartung der Umgebung wird einige Zeit dauern. Nach Abschluss des Vorgangs kehrt die Umgebung in den bereitgestellten Zustand zurück.

    ![Umgebung bereitgestellt.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Eine Dual-Write-Verbindung herstellen 

1. Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.
2. Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus.
3. Nachdem der Link vollständig ist, wählen Sie erneut **Link zu CDS für Apps** aus. Sie werden zu Dual Write in Finance weitergeleitet.

    ![Mit CDS verknüpfen.](./media/12LinktoCDS.png)

4. Wählen Sie **Lösung anwenden** aus, um auf die Entitäten zuzugreifen, die in der Integration zugeordnet werden.

    ![Lösungen anwenden.](./media/13ApplySolutions.png)

5. Wählen Sie beide Lösungen aus, **Dynamics 365 Finance-Entitätszuordnung für duales Schreiben** und **Dynamics 365 Project Operations-Entitätszuordnungen für duales Schreiben** und wählen Sie dann **Anwenden**.

    ![Lösungen bestätigen.](./media/14ConfirmSolutions.png)

    Nachdem die Lösungen angewendet wurden, werden die Dual Write-Entitäten auf die Umgebung angewendet.

    ![Anwenden von Lösungen.](./media/15ApplyingSolutions.png)

    Nachdem die Entitäten angewendet wurden, werden alle verfügbaren Zuordnungen in der Umgebung aufgelistet.

    ![Zuordnungen für duales Schreiben.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Die Datenentitäten nach der Aktualisierung aktualisieren

1. Navigieren Sie in Finance zum Arbeitsbereich **Datenverwaltung**.

    ![Datenverwaltungsarbeitsbereich.](./media/16DataManagement.png)

2. Wählen Sie die Kachel **Framework-Parameter** aus.

    ![Framework-Parameter.](./media/17FrameworkParameters.png)

3. Wählen Sie auf der Seite **Entitätseinstellungen** die Option **Entitätsliste aktualisieren** aus.

    ![Entitätsliste aktualisieren.](./media/18RefreshEntityList.png)

Die Aktualisierung dauert ungefähr 20 Minuten. Sie erhalten eine Benachrichtigung, wenn der Vorgang abgeschlossen ist.

  ![Bestätigung aktualisieren.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Aktualisieren Sie die Sicherheitseinstellungen für Project Operations in Dataverse

1. Gehen sie Project Operations in Ihrer Dataverse Umgebung. 
2. Gehen Sie zu **Einstellungen** > **Sicherheit** > **Sicherheitsrollen**. 
3. Auf der Seite **Sicherheitsrollen** in der Liste der Rollen wählen Sie **Dual-Write-App-Benutzer** und wählen Sie die Registerkarte **Benutzerdefinierte Entitäten**.  
4. Stellen Sie sicher, dass die Rolle die Berechtigungen **Lesen** und **Anhängen** für die folgenden Entitäten besitzt:
      
      - **Währungswechselkurstyp eingeben**
      - **Kontenplan**
      - **Steuerkalender**
      - **Sachkonto**
      - **Firma**
      - **Ausgaben**

5. Nachdem die Sicherheitsrolle aktualisiert wurde, gehen Sie zu **Einstellungen** > **Sicherheit** > **Teams** und wählen Sie das Standardteam in der Teamansicht **Lokaler Geschäftsinhaber** aus.
6. Wählen Sie **Rollen verwalten** und überprüfen Sie, ob die **Dual-Write-App-Benutzer** Sicherheitsberechtigung auf dieses Team angewendet wird.

## <a name="run-project-operations-dual-write-maps"></a>Duales Schreiben für Project Operations-Zuordnungen ausführen

1. Navigieren Sie in Ihrem LCS-Projekt zur Seite **Umgebungsdetails**.
2. Wählen Sie unter **Common Data Service-Umgebungsinformationen** die Option **Link zu CDS für Apps** aus. Nachdem Sie den Link ausgewählt haben, werden Sie zur Liste der Entitäten in den Zuordnungen weitergeleitet.
3. Starten Sie die Zuordnungen. Weitere Informationen finden Sie unter [Project Operations-Zuordnungsversionen für duales Schreiben](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Überprüfen Sie, ob alle projektbezogenen Zuordnungen sich im Status „Wird ausgeführt“ befinden.

    ![Alle Zuordnungen werden ausgeführt.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigurationsdaten in CDS für Project Operations anwenden (optional)

Wenn Sie Demodaten auf die Finanzumgebung angewendet haben, erhalten Sie weitere Informationen unter [Konfigurationsdaten in Common Data Service für Project Operations einrichten und anwenden](resource-apply-pro-setup-config-data.md), um Demodaten auf die CDS-Umgebung anzuwenden.


Ihre Project Operations-Umgebung ist jetzt bereitgestellt und konfiguriert. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
