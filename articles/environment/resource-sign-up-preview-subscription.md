---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen von Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076410"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In diesem Thema wird erläutert, wie Sie das Vorschau-/Partnerangebot abonnieren und die Project Operations-Umgebung bei Szenarien für vorrätige/nicht vorrätige Ressourcen bereitstellen.

## <a name="prerequisites"></a>Voraussetzungen

- Sie erhalten eine E-Mail, in der Sie zur Teilnahme an der Vorschau eingeladen werden. Sie können eine Vorschau auf der [Project Operations-Website](https://dynamics.microsoft.com/en-us/project-operations/overview/) anfordern.
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.
- Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird. Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/en-us/free/) verwenden, um zu starten. Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.

## <a name="subscribe"></a>Abonnieren

Wenn Ihre [Vorschauanforderung](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) genehmigt wird, erhalten Sie drei Angebote von Microsoft per E-Mail. Mit diesen Angeboten können Sie die Project Operations-Vorschau bereitstellen:

- Dynamics 365 Project Operations (CRM) – Vorschau-Testversion
- Office 365 Project Operations – Vorschau-Testversion
- Dynamics 365 Finance – Vorschautestversion

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

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-Vorschautestversion

Wiederholen Sie dieselben Schritte mit dem letzten Angebot aus der Begrüßungs-E-Mail.

## <a name="assign-licenses"></a>Lizenzen zuweisen

> [!IMPORTANT]
> Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.

1. Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.

![Startseite des Admin Center](./media/14AdminPortal.png)

2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.

![Lizenzen zuweisen](./media/15AssignLicenses.png)

3. Stellen Sie sicher, dass die Lizenzen **Dynamics 365 Project Operations (CRM) Vorschau** und **Office 365 Project Operations - Vorschau** ausgewählt sind, und wählen Sie **Änderungen speichern** aus.

> [!NOTE]
> Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.

## <a name="start-a-new-project-in-lcs"></a>Ein neues Projekt in LCS starten

Erstellen Sie ein neues LCS-Projekt wie im Thema [Ein neues Projekt in LCS starten](create-lcs-project.md) beschrieben.

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Einem LCS-Projekt ein Azure-Abonnement hinzufügen

Befolgen Sie zum Ausführen dieser Aufgabe die Schritte im Thema [Einem LCS-Projekt ein Azure-Abonnement hinzufügen](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit

Befolgen Sie die Anweisungen im Thema [Eine neue Umgebung bereitstellen](resource-provision-new-environment.md), um die Bereitstellung abzuschließen. Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS-Einrichtungs- und Konfigurationsdaten installieren

Installieren Sie CDS-Einrichtungs- und Konfigurationsdaten wie im Thema [Konfigurationsdaten in Common Data Service einrichten und anwenden](resource-apply-pro-setup-config-data.md) beschrieben.
Führen Sie diesen Schritt erst aus, nachdem die Finance-Demo-Umgebung bereitgestellt und die Demo-Daten in FO bereit sind.
