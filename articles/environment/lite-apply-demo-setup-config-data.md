---
title: Demoeinrichtungs- und -konfigurationsdaten anwenden – Lite
description: In diesem Artikel erfahren Sie, wie Sie die Demo-Einrichtung und die Konfigurationsdaten für Project Operations anwenden.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9409989"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demoeinrichtungs- und -konfigurationsdaten für Project Operations anwenden – Lite 

_**Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung_



## <a name="prerequisites"></a>Anforderungen

Bevor Sie mit der Konfiguration beginnen, müssen Sie eine Dataverse Umgebung für Dynamics 365 Project Operations haben.


## <a name="instructions"></a>Anweisungen

1. Laden Sie das [Masterdatenpaket](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) herunter. 
2. Navigieren Sie zum Ordner *rojOpsSampleSetupData – CE nur CMT* und führen Sie die ausführbare Datei aus *DataMigrationUtility*.
3. Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.

    ![Konfigurationsmigration.](./media/1ConfigurationMigration.png)

4. Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als den **Bereitstellungstyp** aus.
5. Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.
6. Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein und wählen Sie dann **Einloggen**.

   ![Konfigurationsanmeldung.](./media/2ConfigurationSignin.png)

7. Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten aus, in welche Organisation Sie die Demo-Daten importieren möchten, und wählen Sie dann **Einloggen**.
8. Wählen Sie auf Seite 4 die ZIP-Datei aus *SampleSetupAndConfigData* aus dem entpackten Ordner *ProjOpsSampleSetupData – CE nur CMT*.

   ![ZIP-Datei.](./media/3ZipFile.png)

   ![Eine Datei auswählen.](./media/4SelectAFile.png)

9. Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.

   ![Daten importieren.](./media/5ImportData.png)

10. Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt. Beenden Sie nach Abschluss den CMT-Assistenten. 
11. Überprüfen Sie Ihre Organisation auf Daten in den folgenden 18 Entitäten:

    -   Währung
    -   Konto
    -   Organisationseinheit
    -   Kontakt
    -   Einheit
    -   Einheitengruppe
    -   Preisliste
    -   Projektparameter-Preisliste 
    -   Rechnungshäufigkeit
    -   Buchbare Ressourcenkategorie
    -   Transaktionskategorie
    -   Ausgabenkategorie
    -   Rollenpreis
    -   Transaktionskategoriepreis
    -   Merkmal
    -   Buchbare Ressource
    -   Zuordnung der buchbaren Ressourcenkategorie
    -   Merkmal der buchbaren Ressource

    ![Import abschließen.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
