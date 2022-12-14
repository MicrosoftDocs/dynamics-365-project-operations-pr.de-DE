---
title: Demoeinrichtungs- und -konfigurationsdaten anwenden – Lite
description: In diesem Artikel erfahren Sie, wie Sie die Demo-Einrichtung und die Konfigurationsdaten für Project Operations anwenden.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811024"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demoeinrichtungs- und -konfigurationsdaten für Project Operations anwenden – Lite 

_**Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung_



## <a name="prerequisites"></a>Anforderungen

Bevor Sie mit der Konfiguration beginnen, müssen Sie eine Dataverse Umgebung für Dynamics 365 Project Operations haben.


## <a name="instructions"></a>Anweisungen

1. Laden Sie das [Datenpaket einrichten](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) herunter. 
1. Navigieren Sie zum Ordner *rojOpsSampleSetupData – CE nur CMT* und führen Sie die ausführbare Datei aus *DataMigrationUtility*.
1. Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.

    ![Konfigurationsmigration.](./media/1ConfigurationMigration.png)

1. Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Microsoft 365** als den **Bereitstellungstyp** aus.
1. Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.
1. Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein und wählen Sie dann **Einloggen**.

   ![Konfigurationsanmeldung.](./media/2ConfigurationSignin.png)

1. Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten aus, in welche Organisation Sie die Demo-Daten importieren möchten, und wählen Sie dann **Einloggen**.
1. Wählen Sie auf Seite 4 die ZIP-Datei aus *SampleSetupAndConfigData* aus dem entpackten Ordner *ProjOpsSampleSetupData – CE nur CMT*.

   ![ZIP-Datei.](./media/3ZipFile.png)

   ![Eine Datei auswählen.](./media/4SelectAFile.png)

1. Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.

   ![Daten importieren.](./media/5ImportData.png)

1. Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt. Beenden Sie nach Abschluss den CMT-Assistenten. 
1. Überprüfen Sie Ihre Organisation auf Daten in den folgenden 18 Entitäten:

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
