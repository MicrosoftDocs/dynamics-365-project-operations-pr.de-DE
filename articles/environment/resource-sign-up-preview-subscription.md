---
title: Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden
description: Dieses Thema enthält Informationen zum Abonnieren und Bereitstellen von Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 75ee31e67018fe2a7655d8a8f11e40b433a9a5db6f8f2addac27844f18fffe8d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007865"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Sich für Szenarien bei Project Operations-Vorschauabonnements für vorrätige/nicht vorrätige Ressourcen anmelden

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dieses Thema erklärt, wie Sie das Test-Angebot abonnieren und die Project Operations Umgebung für ressourcenbasierte/nicht vorrätige Szenarien bereitstellen.

## <a name="prerequisites"></a>Anforderungen
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen. Sie können einen Mandanten während der ersten Angebotseinlösung erstellen. 
- Für die Bereitstellung einer Finance-Umgebung ist ein gültiges Azure-Abonnement erforderlich, das pro Umgebung in Rechnung gestellt wird. Sie können das vorhandene Abonnement Ihrer Organisation oder eine [Azure-Testversion](https://azure.microsoft.com/en-us/free/) verwenden, um zu starten. Die CDS-Umgebung wird für einen begrenzten Zeitraum von 30 Tagen kostenlos zur Verfügung gestellt.

> [!IMPORTANT]
> Nur eine Person in der Organisation, der Mandanten-Administrator, muss diese Aufgabe ausführen. Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.
> 
> Tests sind im Mandanten nur einmal verwendbar. Sie können einen Test nur ein einziges Mal ausführen. Wir empfehlen, dass Sie für den Test einen neuen Mandanten erstellen.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - Vorschau Test 

Bevor Sie beginnen, stellen Sie sicher, dass Sie bei einem Browser mit dem Benutzerarbeitskonto im Mandanten angemeldet sind, in dem Sie die Vorschau des Projektvorgangs anzeigen möchten.

1. Lösen Sie den ersten Angebotscode ein, **Dynamics 365 Project Operations** hier [Project Operations Test](https://aka.ms/try-po).
2. Bestätigen Sie Ihre Bestellung.

  Sie sehen, dass das Bestätigungsangebot erfolgreich eingelöst wurde.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-Vorschautestversion

Gehen Sie zu [Dynamics 365 for Finance Vorschau Test](https://aka.ms/trypoche) und wiederholen Sie die Schritte aus dem vorherigen Abschnitt mit dem Angebot, Melden Sie sich für die Cloud Hosted Umgebung an.  

## <a name="assign-licenses"></a>Lizenzen zuweisen

> [!IMPORTANT]
> Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.

1. Navigieren Sie zu [Microsoft 365 Admin Center](https://portal.office.com/), um Ihren Benutzern die Lizenzen zuzuweisen.

2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.

3. Vergewissern Sie sich, dass die **Dynamics 365 Project Operations** Lizenz ausgewählt wurde und wählen Sie **Änderungen speichern**.

> [!NOTE]
> Das Finance-Testangebot muss keinem Benutzer zugewiesen werden.

## <a name="start-a-new-project-in-lcs"></a>Ein neues Projekt in LCS starten

Erstellen Sie ein neues LCS-Projekt wie im Thema [Ein neues Projekt in LCS starten](create-lcs-project.md) beschrieben.

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Einem LCS-Projekt ein Azure-Abonnement hinzufügen

Befolgen Sie zum Ausführen dieser Aufgabe die Schritte im Thema [Einem LCS-Projekt ein Azure-Abonnement hinzufügen](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Stellen Sie die Finance-Demoumgebung mit Project Operations für Szenarien mit vorrätigen/nicht vorrätigen Ressourcen bereit

Befolgen Sie die Anweisungen im Thema [Eine neue Umgebung bereitstellen](resource-provision-new-environment.md), um die Bereitstellung abzuschließen. Verwenden Sie den Bereitstellungstyp [Demo-Umgebung](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) für die Vorschau. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS-Einrichtungs- und Konfigurationsdaten installieren

Installieren Sie CDS-Einrichtungs- und Konfigurationsdaten wie im Thema [Konfigurationsdaten in Common Data Service einrichten und anwenden](resource-apply-pro-setup-config-data.md) beschrieben.
Schließen Sie diesen Schritt erst ab, wenn die Finance-Demo-Umgebung bereitgestellt ist und die Demo-Daten bereitstehen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
