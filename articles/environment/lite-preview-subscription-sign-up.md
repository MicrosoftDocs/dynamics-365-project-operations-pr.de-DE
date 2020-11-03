---
title: Für ein Vorschauabonnement anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen der Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076387"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Melden Sie sich für ein Vorschau-Abonnement für die Lite-Bereitstellung an – Abschluss zur Proforma-Rechnungsstellung

Dieses Thema erklärt, wie Sie das Vorschaupartnerangebot abonnieren und Dynamics 365 Project Operations Lite-Bereitstellung – Abschluss zur Proforma-Rechnungsstellung bereitstellen können.

> [!NOTE]
> Dieser Prozess wird sich in den kommenden Versionen von Project Operations ändern.

## <a name="prerequisites"></a>Voraussetzungen

- Sie erhalten eine E-Mail, in der Sie zur Teilnahme an der Vorschau eingeladen werden. Sie können eine Vorschau auf der [Project Operations-Website](https://dynamics.microsoft.com/en-us/project-operations/overview/) anfordern.
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.
- Überprüfen Sie alle allgemeinen Geschäftsbedingungen.

## <a name="subscribe"></a>Abonnieren

Wenn Sie eine Genehmigung für die [Vorschauanforderung](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) erhalten, erhalten Sie zwei Angebote von Microsoft per E-Mail. Mit diesen Angeboten können Sie die Project Operations-Vorschau bereitstellen:

- Dynamics 365 Project Operations (CRM) – Vorschau-Testversion
- Office 365 Project Operations – Vorschau-Testversion

> [!IMPORTANT]
> Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen. Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – Vorschau-Testversion 

Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.

1. Lösen Sie den ersten Angebotscode **Dynamics 365 Project Operations (CRM) – Vorschau-Testversion** ein, indem Sie ihn in die Browser-URL einfügen.

![Angebot einlösen](./media/16RedeemFirstOfferNew.png)

2. Bestätigen Sie Ihre Bestellung.
![Bestellung bestätigen](./media/17ConfirmOrderNew.png)

Sie sehen, dass das Bestätigungsangebot erfolgreich eingelöst wurde.

![Bestätigung](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – Vorschau-Testversion

Wiederholen Sie die gleichen Schritte wie beim ersten Angebotscode. Stellen Sie sicher, dass Sie den zweiten Angebotscode mit demselben Benutzerkonto hinzufügen, das mit dem ersten Angebotscode verwendet wurde.

## <a name="assign-licenses"></a>Lizenzen zuweisen

> [!IMPORTANT]
> Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.


1. Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.

![Startseite des Admin Center](./media/14AdminPortal.png)

2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.

![Lizenzen zuweisen](./media/15AssignLicenses.png)

3. Stellen Sie sicher, dass die Lizenzen **Dynamics 365 Project Operations (CRM) Vorschau** und **Office 365 Project Operations – Vorschau** ausgewählt sind. 
4. Wählen Sie **Änderungen speichern**.

## <a name="create-a-new-cds-environment"></a>Neue CDS-Umgebung erstellen

1. Stellen Sie eine neue Project Operations CDS-Bereitstellungsumgebung bereit, indem Sie den Anweisungen im Thema [CDS-Bereitstellungsmodell](lite-deployment.md) folgen. Stellen Sie bei der Auswahl des Umgebungstyps sicher, dass Sie **Testversion (abonnementbasiert)** auswählen.
![Neue Umgebung](./media/19CreateEnvironment.png)

2. Wählen Sie die Einstellung **Dynamics 365-Apps aktivieren** aus, und lassen Sie **Diese Apps automatisch bereitstellen** leer.  
3. Wählen Sie **Speichern** aus, um die Umgebung zu erstellen.

![Datenbank hinzufügen](./media/20CreateEnvironment1.png)

4. Installieren Sie nach dem Erstellen der Umgebung die **Microsoft Dynamics 365 Project Operations** -Lösung. 

![Lösung installieren](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-Konfigurations- und Einrichtungsdemodaten installieren

Installieren Sie die CDS-Konfiguration und richten Sie die Demo-Daten ein, indem Sie den Anweisungen im Thema [Demoeinrichtungs- und -konfigurationsdaten anwenden](lite-apply-demo-setup-config-data.md) folgen.
