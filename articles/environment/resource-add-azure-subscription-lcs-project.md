---
title: Einem LCS-Projekt ein Azure-Abonnement hinzufügen
description: Dieses Thema enthält Informationen zum Verbinden Ihres Azure-Abonnements mit einem LCS-Projekt.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076395"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Einem LCS-Projekt ein Azure-Abonnement hinzufügen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

In der Cloud gehostete Umgebungen müssen mit einem vorhandenen Azure-Abonnement bereitgestellt werden. Dieses Thema erklärt, wie Ihr vorhandenes Azure-Abonnement mit einem LCS-Projekt verbunden wird. 

## <a name="grant-admin-consent"></a>Administratoreinwilligung erteilen

1. Wählen Sie im Abschnitt **Umgebungen** in Ihrem LCS-Projekt die **Microsoft Azure-Einstellungen** aus.

![Einstellungen für die Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Wählen Sie auf der Seite **Projekteinstellungen** auf der Registerkarte **Azure-Abonnements** die Option **Autorisieren** aus. Dadurch können Umgebungen für dieses Projekt bereitgestellt werden.

![Azure-Konnektoren](./media/2AzureConnectors.png)

3. Wählen Sie erneut **Autorisieren** aus, um die Administratoreinwilligung zu erteilen.

![Administratoreinwilligung erteilen](./media/3GrantAdminConsent.png)

4. Die Berechtigungsanforderung akzeptieren

![Die Berechtigungsanforderung akzeptieren](./media/4AcceptPermissionRequest.png)

Die Autorisierung ist jetzt abgeschlossen. 

![Autorisierung erfolgreich](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Dynamics Deployment Services den Zugriff auf Ihr Azure-Abonnement ermöglichen

1. Navigieren Sie zur [Microsoft Azure-Fakturierung](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), und wählen Sie Ihr Abonnement aus. Dynamics Deployment Services muss auf dieses Abonnement zugreifen, um Umgebungen bereitstellen zu können.

![Azure-Abonnementdetails](./media/6AzureSubscription.png)

2. Wählen Sie **Access Control (IAM)** im Navigationsbereich und dann **Rollenzuweisung hinzufügen** aus.
3. Wählen Sie im Schieberegler auf der rechten Seite **Rolle als Beitragender** aus. Suchen Sie **Dynamics Deployment Services** , und wählen Sie es aus. 
4. Wählen Sie **Speichern** aus.

![Abonnementzugriff](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Einem LCS-Projekt einen Azure-Konnektor hinzufügen

1. Wählen Sie auf der Seite **Microsoft Azure-Einstellungen** in Ihrem LCS-Projekt **Hinzufügen** aus, um einen neuen Konnektor hinzuzufügen.
2. Geben Sie die ID Ihres Azure-Abonnements ein. Sie finden die ID Ihres Azure-Abonnements im [Azure-Portal](https://ms.portal.azure.com/) unter **Einstellungen** unten links im Bildschirm.
3. Wählen Sie im Feld **Zur Verwendung von Azure Resource Manager konfigurieren** **Ja** aus.
4. Stellen Sie sicher, dass die AAD-Mandantendomäne des Azure-Abonnements mit dem Azure-Abonnement der Domäne, die Sie verwenden, übereinstimmt, und wählen Sie **Weiter** aus.
5. Wählen Sie im Bildschirm **Microsoft Azure-Einrichtung** zur Bestätigung **Weiter** aus. Wenn auf diesem Bildschirm eine Fehlermeldung angezeigt wird, kehren Sie zum Abschnitt [Dynamics Deployment Services den Zugriff auf Ihr Azure-Abonnement ermöglichen](#provide) in diesem Thema zurück, und stellen Sie sicher, dass Sie alle Schritte abgeschlossen haben.
6. Laden Sie das Azure-Verwaltungszertifikat in einen lokalen Ordner auf Ihrem Computer herunter, und laden Sie es anschließend in das Azure-Verwaltungsportal hoch, indem Sie zu **Einstellungen** > **Verwaltungszertifikate** navigieren. Mit diesem Zertifikat kann LCS in Ihrem Namen mit Azure kommunizieren. Sie können diesen Schritt überspringen, wenn Ihr Benutzer Zugriff auf das Abonnement hat.
7. Wählen Sie **Weiter** aus.
8. Wählen Sie die Azure-Region aus, in der die Bereitstellung erfolgen soll, und wählen Sie ein Rechenzentrum aus, das sich in der Nähe des Ortes befindet, an dem Sie dieses System verwenden möchten.
9.  Wählen Sie **Verbinden** aus.

Sie haben Ihr Azure-Abonnement erfolgreich verbunden. Sie können nun Cloud-gehostete Dynamics 365 Finance-Umgebungen bereitstellen.


