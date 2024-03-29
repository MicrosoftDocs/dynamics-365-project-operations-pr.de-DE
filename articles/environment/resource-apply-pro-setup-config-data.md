---
title: Konfigurationsdaten in Microsoft Dataverse einrichten und anwenden
description: Dieser Artikel informiert Sie über das Festlegen und Anwenden von Konfigurationsdaten in Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230236"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurationsdaten in Common Data Service einrichten und anwenden 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_



## <a name="prerequisites"></a>Anforderungen

Bevor Sie mit der Konfiguration von Daten im Microsoft Dataverse beginnen, müssen folgende Voraussetzungen erfüllt sein:

1.  Stellen Sie eine Dataverse-Umgebung und eine Dynamics 365 Finance-Umgebung für Project Operations bereit.
2.  Informationen zur juristischen Person aus Dynamics 365 Finance werden an die Dataverse-Umgebung weitergegeben. Dies bedeutet, dass die **Firma**-Entität in Dataverse die folgenden Firmendatensätze hat:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Einrichtungs- und Konfigurationsdaten installieren

1. Laden Sie das [Einrichtungs- und Konfigurationsdatenpaket](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip) herunter, und entpacken Sie es.
2. Navigieren Sie zum entpackten Ordner, und führen Sie die ausführbare Datei *DataMigrationUtility* aus.
3. Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.

![Konfigurationsmigration.](./media/1ConfigurationMigration.png)

4. Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als den **Bereitstellungstyp** aus.
5. Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.
6. Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein, und wählen Sie **Anmelden** aus.

![Konfigurationsanmeldung.](./media/2ConfigurationSignin.png)

7. Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten die Organisation aus, in die Sie die Demo-Daten importieren möchten, und dann **Anmelden**.
8. Wählen Sie auf Seite 4 die Zip-Datei *SampleSetupAndConfigData* aus dem entpackten Ordner aus.

![Auswahl der Zip-Datei.](./media/3ZipFile.png)

![Eine Datei auswählen.](./media/4SelectAFile.png)

9. Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.

![Daten importieren.](./media/5ImportData.png)

10. Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt. Beenden Sie nach Abschluss des Imports den CMT-Assistenten. 
11. Überprüfen Sie Ihre Organisation auf Daten in den folgenden 26 Entitäten:

  - Währung
  - Kontenplan
  - Steuerkalender
  - Währungswechselkurstypen eingeben
  - Zahlungstag
  - Zahlungsplan
  - Zahlungsbedingung
  - Organisationseinheit
  - Kontakt
  - Steuergruppe
  - Kundengruppe
  - Kreditorengruppe
  - Einheit
  - Einheitengruppe
  - Preisliste
  - Projektparameter-Preisliste
  - Rechnungshäufigkeit
  - Buchbare Ressourcenkategorie
  - Transaktionskategorie
  - Ausgabenkategorie
  - Rollenpreis
  - Transaktionskategoriepreis
  - Merkmal
  - Buchbare Ressource
  - Zuordnung der buchbaren Ressourcenkategorie
  - Merkmal der buchbaren Ressource

![Import abschließen.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations-Konfigurationen aktualisieren

1. Navigieren zur CE-Umgebung. Sie können sie finden, indem Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments) öffnen, die Umgebung und dann **Umgebung öffnen** auswählen. 

![Umgebung öffnen.](./media/7OpenEnvironment.png)

2. Navigieren Sie zu **Projekte** > **Ressourcen**, und wählen Sie dann **Neu** aus, um eine buchbare Ressource für Ihren Benutzer zu erstellen.

![Buchbare Ressourcen.](./media/8BookableResources.png)

3. Wählen Sie auf der Registerkarte **Allgemein** Ihren Administrator-Benutzer aus. Stellen Sie sicher, dass die Zeitzone mit der übereinstimmt, in der Sie sich befinden. 

![Neue buchbare Ressource.](./media/9NewBookableResource.png)

4. Wählen Sie auf der Registerkarte **Zeitplanung** im Feld **Unternehmen** das Unternehmen **USPM** und dann **Speichern** aus. 

![Registerkarte „Planung“.](./media/10SchedulingTab.png)

5. Wählen Sie die Registerkarte **Arbeitsstunden** aus.  

![Arbeitszeit.](./media/11WorkHours.png)

6. Doppelklicken Sie auf einen beliebigen Wert im Kalender, und wählen Sie **Bearbeiten** > **Alle Ereignisse in der Serie** aus. 

![Arbeitskalender.](./media/12WorkCalendar.png)

7. Ändern Sie die Arbeitszeit in einen Arbeitstag von acht (8) Stunden, markieren Sie Wochenenden als arbeitsfreie Tage, und stellen Sie sicher, dass die Zeitzone mit Ihrer übereinstimmt. 
8. Wählen Sie **Speichern und schließen** aus.

![Kalender aktualisieren.](./media/13UpdateCalendar.png)

9. Navigieren Sie zu **Einstellungen** > **Kalendervorlagen**, und wählen Sie **Neu** aus.
 
 ![Kalendervorlagen.](./media/14CalendarTemplates.png)
 
 10. Geben Sie einen Namen ein, wählen Sie die von Ihnen erstellte Vorlagenressource und dann **Speichern** aus. 
 
 ![Kalendervorlage speichern.](./media/15SaveCalendarTemplate.png)
 
 11. Navigieren Sie zu **Parameter**, und doppelklicken Sie auf den Datensatz. 
 
 ![Projektparameter.](./media/16ProjectParameters.png)
 
12. Aktualisieren Sie die folgenden Felder:

 - **Standardunternehmen**: USPM
 - **Standard-Organisationseinheit**: Contoso Robotics Global
 - **Rechnungshäufigkeit**: Siebter und letzter Tag
 - **Arbeitszeitvorlage**: Wechseln Sie zu der von Ihnen erstellten Vorlage.

13. Wählen Sie **Speichern** aus. 

![Aktualisierte Projektparameter.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
