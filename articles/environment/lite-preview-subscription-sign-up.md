---
title: Für ein Vorschauabonnement anmelden – Lite
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen der Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334781"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Für ein Vorschauabonnement anmelden – Lite 

In diesem Thema wird erklärt, wie Sie das Test-Angebot abonnieren und Dynamics 365 Project Operations Lite-Bereitstellung - Deal zur Proforma-Rechnung bereitstellen.

> [!NOTE]
> Dieser Prozess wird sich in den kommenden Versionen von Project Operations ändern.

## <a name="prerequisites"></a>Anforderungen
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen. Sie können einen Mandanten während der ersten Angebotseinlösung erstellen.

> [!IMPORTANT]
> Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen. Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.
> 
> Tests sind im Mandanten nur einmal verwendbar. Sie können einen Test nur ein einziges Mal ausführen. Wir empfehlen, dass Sie für den Test einen neuen Mandanten erstellen.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations-Testversion 

Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.

1. Gehen Sie zu [Project Operations Test](https://aka.ms/try-po), um den ersten Angebotscode einzulösen, **Dynamics 365 Project Operations**.
2. Bestätigen Sie Ihre Bestellung.

  Sie werden die Bestätigung sehen, dass das Angebot erfolgreich eingelöst wurde.

## <a name="assign-licenses"></a>Lizenzen zuweisen

> [!IMPORTANT]
> Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.


1. Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.
2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.
3. Stellen Sie sicher, dass die **Dynamics 365 Project Operations** Lizenz ausgewählt ist. 
4. Wählen Sie **Änderungen speichern**.

## <a name="create-a-new-dataverse-environment"></a>Neue Dataverse-Umgebung erstellen

1. Stellen Sie eine neue Project Operations Dataverse-Umgebung bereit, indem Sie den Anweisungen im Thema [Dataverse-Bereitstellungsmodell](lite-deployment.md) folgen. Stellen Sie bei der Auswahl des Umgebungstyps sicher, dass Sie **Testversion (abonnementbasiert)** auswählen.

  ![Neue Umgebung](./media/19CreateEnvironment.png)

2. Wählen Sie die Einstellung **Dynamics 365-Apps aktivieren** aus, und lassen Sie **Diese Apps automatisch bereitstellen** leer.  
3. Wählen Sie **Speichern** aus, um die Umgebung zu erstellen.

  ![Datenbank hinzufügen](./media/20CreateEnvironment1.png)

4. Installieren Sie nach dem Erstellen der Umgebung die **Microsoft Dynamics 365 Project Operations**-Lösung. 

![Lösung installieren](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-Konfigurations- und Einrichtungsdemodaten installieren

Installieren Sie die CDS-Konfiguration und richten Sie die Demo-Daten ein, indem Sie den Anweisungen im Thema [Demoeinrichtungs- und -konfigurationsdaten anwenden](lite-apply-demo-setup-config-data.md) folgen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
