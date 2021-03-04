---
title: Konfigurationsdaten in Common Data Service einrichten und anwenden
description: Dieses Thema enthält Informationen zum Einrichten und Anwenden von Konfigurationsdaten in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642227"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurationsdaten in Common Data Service einrichten und anwenden 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Anforderungen

Bevor Sie beginnen, Daten in Common Data Service (CDS) zu konfigurieren, müssen folgende Voraussetzungen erfüllt sein:

1.  Bereitstellung einer CDS-Umgebung und einer Dynamics 365 Finance-Umgebung für Project Operations.
2.  Informationen zu juristischen Personen von Dynamics 365 Finance werden für die CDS-Umgebung freigegeben. Dies bedeutet, dass die **Firma**-Entität in CDS die folgenden Firmendatensätze hat:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Einrichtungs- und Konfigurationsdaten installieren

1. Laden Sie das [Einrichtungs- und Konfigurationsdatenpaket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip) herunter, und entpacken Sie es.
2. Navigieren Sie zum entpackten Ordner, und führen Sie die ausführbare Datei *DataMigrationUtility* aus.
3. Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.

![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als **Bereitstellungstyp** aus.
5. Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.
6. Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein, und wählen Sie **Anmelden** aus.

![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten die Organisation aus, in die Sie die Demo-Daten importieren möchten, und dann **Anmelden**.
8. Wählen Sie auf Seite 4 die Zip-Datei *SampleSetupAndConfigData* aus dem entpackten Ordner aus.

![Auswahl der Zip-Datei](./media/3ZipFile.png)

![Datei auswählen](./media/4SelectAFile.png)

9. Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.

![Importdaten](./media/5ImportData.png)

10. Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt. Beenden Sie nach Abschluss des Imports den CMT-Assistenten. 
11. Überprüfen Sie Ihre Organisation auf Daten in den folgenden 19 Entitäten:

  - Währung
  - Organisationseinheit
  - Kontakt
  - Steuergruppe
  - Kundengruppe
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

![Import abschließen](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations-Konfigurationen aktualisieren

1. Navigieren zur CE-Umgebung. Sie können sie finden, indem Sie das [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments) öffnen, die Umgebung und dann **Umgebung öffnen** auswählen. 

![Umgebung öffnen](./media/7OpenEnvironment.png)

2. Navigieren Sie zu **Projekte** > **Ressourcen**, und wählen Sie dann **Neu** aus, um eine buchbare Ressource für Ihren Benutzer zu erstellen.

![Buchbare Ressourcen](./media/8BookableResources.png)

3. Wählen Sie auf der Registerkarte **Allgemein** Ihren Administrator-Benutzer aus. Stellen Sie sicher, dass die Zeitzone mit der übereinstimmt, in der Sie sich befinden. 

![Neue buchbare Ressource](./media/9NewBookableResource.png)

4. Wählen Sie auf der Registerkarte **Zeitplanung** im Feld **Unternehmen** das Unternehmen **USPM** und dann **Speichern** aus. 

![Registerkarte „Planung“](./media/10SchedulingTab.png)

5. Wählen Sie die Registerkarte **Arbeitsstunden** aus.  

![Arbeitszeit](./media/11WorkHours.png)

6. Doppelklicken Sie auf einen beliebigen Wert im Kalender, und wählen Sie **Bearbeiten** > **Alle Ereignisse in der Serie** aus. 

![Arbeitskalender](./media/12WorkCalendar.png)

7. Ändern Sie die Arbeitszeit in einen Arbeitstag von acht (8) Stunden, markieren Sie Wochenenden als arbeitsfreie Tage, und stellen Sie sicher, dass die Zeitzone mit Ihrer übereinstimmt. 
8. Wählen Sie **Speichern und schließen** aus.

![Kalender aktualisieren](./media/13UpdateCalendar.png)

9. Navigieren Sie zu **Einstellungen** > **Kalendervorlagen**, und wählen Sie **Neu** aus.
 
 ![Kalendervorlagen](./media/14CalendarTemplates.png)
 
 10. Geben Sie einen Namen ein, wählen Sie die von Ihnen erstellte Vorlagenressource und dann **Speichern** aus. 
 
 ![Kalendervorlage speichern](./media/15SaveCalendarTemplate.png)
 
 11. Navigieren Sie zu **Parameter**, und doppelklicken Sie auf den Datensatz. 
 
 ![Projektparameter](./media/16ProjectParameters.png)
 
12. Aktualisieren Sie die folgenden Felder:

 - **Standardunternehmen**: USPM
 - **Standard-Organisationseinheit**: Contoso Robotics Global
 - **Rechnungshäufigkeit**: Siebter und letzter Tag
 - **Arbeitszeitvorlage**: Wechseln Sie zu der von Ihnen erstellten Vorlage.

13. Wählen Sie **Speichern** aus. 

![Aktualisierte Projektparameter](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]