---
title: Für ein Vorschauabonnement anmelden – Lite
description: In diesem Artikel erfahren Sie, wie Sie die Lite-Bereitstellung von Project Operations abonnieren und bereitstellen können - für die Proforma-Rechnungsstellung.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410010"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Für ein Vorschauabonnement anmelden – Lite 

Dieser Artikel erklärt, wie Sie das Test-Angebot abonnieren und eine Lite-Bereitstellung von Dynamics 365 Project Operations bereitstellen können - Umgang mit Proforma-Rechnungen.

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


1. Gehen Sie zum [Microsoft 365 Admin Center](https://portal.office.com/), um die Lizenzen Ihren Benutzern zuzuweisen.
2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.
3. Stellen Sie sicher, dass die **Dynamics 365 Project Operations** Lizenz ausgewählt ist. 
4. Wählen Sie **Änderungen speichern**.

## <a name="create-a-new-dataverse-environment"></a>Neue Dataverse-Umgebung erstellen

1. Stellen Sie eine neue Umgebung für Project Operations Dataverse bereit, indem Sie den Anweisungen im Artikel [Dataverse Bereitstellungsmodell](lite-deployment.md) folgen. Stellen Sie bei der Auswahl des Umgebungstyps sicher, dass Sie **Testversion (abonnementbasiert)** auswählen.

  ![Neue Umgebung.](./media/19CreateEnvironment.png)

2. Wählen Sie die Einstellung **Dynamics 365-Apps aktivieren** aus, und lassen Sie **Diese Apps automatisch bereitstellen** leer.  
3. Wählen Sie **Speichern** aus, um die Umgebung zu erstellen.

  ![Datenbank hinzufügen.](./media/20CreateEnvironment1.png)

4. Installieren Sie nach dem Erstellen der Umgebung die **Microsoft Dynamics 365 Project Operations**-Lösung. 

![Lösung installieren.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Demodaten einrichten

Installieren Sie die Demodaten, indem Sie den Anweisungen im Artikel [Demo-Einrichtung und Konfigurationsdaten anwenden](lite-apply-demo-setup-config-data.md) folgen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
