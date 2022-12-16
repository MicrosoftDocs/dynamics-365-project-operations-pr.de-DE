---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: In diesem Artikel erfahren Sie, wie Sie Project Operations für ressourcenbasierte/nicht vorrätige Szenarien abonnieren und bereitstellen können.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3164add153d77a52f85c2aac442dcf90baa24440
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2022
ms.locfileid: "9842014"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_



Dieser Artikel erklärt, wie Sie das Test-Angebot abonnieren und eine Project Operations Umgebung für ressourcenbasierte/nicht vorrätige Szenarien bereitstellen können.

## <a name="prerequisites"></a>Anforderungen
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen. Sie können einen Mandanten während der ersten Angebotseinlösung erstellen. 
- Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird. Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/free/) verwenden, um zu starten. Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.

> [!IMPORTANT]
> Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen. Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.
> 
> Tests sind im Mandanten nur einmal verwendbar. Sie können einen Test nur ein einziges Mal ausführen. Wir empfehlen, dass Sie für den Test einen neuen Mandanten erstellen.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Vorschau Test 

Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.

1. Lösen Sie den ersten Angebotscode ein, **Dynamics 365 Project Operations** hier [Project Operations Test](https://aka.ms/try-po).
2. Bestätigen Sie Ihre Bestellung.

  Sie sehen, dass das Bestätigungsangebot erfolgreich eingelöst wurde.

### <a name="dynamics-365-finance-preview-trial"></a>Vorschau-Testversion von Dynamics 365 Finance

Gehen Sie zu [Dynamics 365 for Finance Vorschau Test](https://aka.ms/trypoche) und wiederholen Sie die Schritte aus dem vorherigen Abschnitt mit dem Angebot, Melden Sie sich für die Cloud Hosted Umgebung an.  

## <a name="assign-licenses"></a>Lizenzen zuweisen

> [!IMPORTANT]
> Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.

1. Gehen Sie zum [Microsoft 365 Admin Center](https://portal.office.com/), um die Lizenzen Ihren Benutzern zuzuweisen.

2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.

3. Vergewissern Sie sich, dass die **Dynamics 365 Project Operations** Lizenz ausgewählt wurde und wählen Sie **Änderungen speichern**.

> [!NOTE]
> Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.

## <a name="start-a-new-project-in-lcs"></a>Ein neues Projekt in LCS starten

Erstellen Sie ein neues LCS Projekt wie in dem Artikel [Starten Sie ein neues Projekt in LCS](create-lcs-project.md) beschrieben.

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Einem LCS-Projekt ein Azure-Abonnement hinzufügen

Um diese Aufgabe zu erledigen, folgen Sie den Schritten im Artikel [Hinzufügen eines Azure Abonnements zum LCS Projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit

Folgen Sie der Anleitung im Artikel [Bereitstellen einer neuen Umgebung](resource-provision-new-environment.md), um die Bereitstellung abzuschließen. Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS-Einrichtungs- und Konfigurationsdaten installieren

Installieren Sie die CDS-Einrichtungs- und Konfigurationsdaten wie im Artikel [Konfigurationsdaten in der Common Data Service](resource-apply-pro-setup-config-data.md) festgelegt und anwenden.
Schließen Sie diesen Schritt erst ab, wenn die Finance-Demo-Umgebung bereitgestellt ist und die Demo-Daten bereitstehen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
