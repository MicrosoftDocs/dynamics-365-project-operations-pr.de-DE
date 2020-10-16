---
title: Anwenden von Demo-Einrichtungs- und Konfigurationsdaten
description: Dieses Thema enthält Informationen zum Anwenden von Demo-Einrichtungs- und Konfigurationsdaten für Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948867"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Anwenden der Demo-Einrichtungs- und Konfigurationsdaten für die Bereitstellung des Project Operations Lite - Abschluss zur Proforma-Rechnungsstellung

_**Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung_

1. Laden Sie das [Masterdatenpaket](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) herunter. 
2. Navigieren Sie zum Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* und führen Sie die ausführbare Datei *DataMigrationUtility* aus.
3. Auf Seite 1 des Assistenten für Common Data Service-Konfigurationsmigration (CMT) wählen Sie **Daten importieren** und dann **Fortsetzen** aus.

![Konfigurationsmigration](./media/1ConfigurationMigration.png)

4. Wählen Sie auf Seite 2 des CMT-Assistenten die Option **Office 365** als den **Bereitstellungstyp** aus.
5. Aktivieren Sie die Kontrollkästchen **Eine Liste der verfügbaren Organisationen anzeigen** und **Erweitert anzeigen**.
6. Wählen Sie die Region Ihres Mandanten aus, geben Sie Ihre Anmeldeinformationen ein und wählen Sie dann **Einloggen**.

![Konfigurations-Login](./media/2ConfigurationSignin.png)

7. Wählen Sie auf Seite 3 aus der Liste der Organisationen im Mandanten aus, in welche Organisation Sie die Demo-Daten importieren möchten, und wählen Sie dann **Einloggen**.
8. Wählen Sie auf Seite 4 die Zip-Datei *MasterAndSetupData* aus dem entpackten Ordner *ProjOpsDemoDataSetupAndMaster – integriertes CMT* aus.

![ZIP-Datei](./media/3ZipFile.png)

![Datei auswählen](./media/4SelectAFile.png)

9. Nachdem die Zip-Datei ausgewählt wurde, wählen Sie **Daten importieren**.

![Daten importieren](./media/5ImportData.png)

10. Der Import wird je nach Netzwerkgeschwindigkeit ungefähr zwei bis zehn Minuten lang ausgeführt. Beenden Sie nach Abschluss den CMT-Assistenten. 
11. Überprüfen Sie Ihre Organisation auf Daten in den folgenden 20 Entitäten:

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
- Detail zur Rechnungshäufigkeit
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
