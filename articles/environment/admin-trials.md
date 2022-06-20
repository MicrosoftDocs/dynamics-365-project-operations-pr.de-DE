---
title: Für Testversionen von Project Operations anmelden
description: Dieser Artikel beschreibt, wie Sie einen Test von Dynamics 365 Project Operations bereitstellen können.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 7db7ea6b3cffe6eb43ee0519bbaccfc9092c9311
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959490"
---
# <a name="sign-up-for-project-operations-trials"></a>Für Testversionen von Project Operations anmelden 

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung, Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigung_ 



Dieser Artikel erklärt, wie Sie das Preview-Partnerangebot abonnieren und eine Dynamics 365 Project Operations-Umgebung bereitstellen können.

Mit der neuen Project Operations-Testversion können Sie jedes der drei unterstützten Bereitstellungsszenarien automatisch bereitstellen, indem Sie einen Fragebogen ausfüllen, der den besten Bereitstellungsansatz empfiehlt. Dieser Artikel informiert Sie darüber, wie Sie:

- Lösen Sie Ihr Testangebot ein.
- Initiieren Sie die Bereitstellung.
- Konfigurieren Sie duales Schreiben.
- Weitere Informationen zu Project Operations. 

Die folgende Tabelle enthält die Details des neuen Testangebots.

| **Angebotsartikel**               | **Informationen**                                  |
|------------------------------|----------------------------------------------|
| Angebotstyp                   | Dieser Angebotstyp ist Admin-Lead, daher ist zum Einlösen ein Mandantenadministrator erforderlich. |
| Angebotsnutzung                    | Einmal pro M;andant                          |
| Angebotsdauer               | 30 Kalendertage                             |
| Einlösungen pro Mandant       | 1                                            |
| Erweiterung                    | 1 Verlängerung, 30 Kalendertage               |
| Anzahl der Testumgebungen | 3                                            |


## <a name="admin-trial-details"></a>Details zur Admin-Testversion
In der folgenden Tabelle sind die Testdetails und deren Anwendung auf die einzelnen Bereitstellungstypen aufgeführt.

| **Artikel**                      | **Lite**                                     | **Nicht vorrätige Materialien** | **Vorrätige Materialien** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Setup-Daten bereitgestellt           | Ja                                          | Ja                       | Ja (USSI)            |
| Transaktionsdaten            | Keine                                           | Keine                        | Keine                    |
| Bereitstellungszeit in Minuten  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Anforderungen
Die folgenden Voraussetzungen sind bei der Bereitstellung einer Testversion von Dynamics 365 Project Operations erforderlich.

- Registrieren Sie sich für die [Dynamics 365 Project Operations - Vorschautestversion](https://www.aka.ms/try-po).
- Der Benutzer, der die Vorschau bereitstellt, muss über die globalen Administratorrechte für den Azure-Mandanten verfügen.

> [!IMPORTANT]
> Nur eine Person in einer Organisation, der Mandant-Administrator, muss diese Aufgabe ausführen. Wenn Sie nicht Abonnent dieser Version sind, warten Sie, bis Ihre Organisation angemeldet wurde und Sie Ihre Benutzeranmeldeinformationen erhalten haben.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations-Vorschautestversion 

Bevor Sie beginnen, melden Sie sich bei einem Browser mit dem Arbeitskonto des Benutzers in dem Mandanten an, in dem Sie die Vorschauversion von Project Operations anzeigen möchten.

1. Lösen Sie den ersten Angebotscode **Dynamics 365 Project Operations - Vorschautestversion** durch Einfügen in die Browser-URL ein.

    ![Angebot einlösen](./media/16RedeemFirstOfferNew.png)

2. Bestätigen Sie Ihre Bestellung.

    ![Bestellung bestätigen](./media/17ConfirmOrderNew.png)

  Sie werden die Bestätigung sehen, dass das Angebot erfolgreich eingelöst wurde.

   ![Bestätigung](./media/18OrderConfirmationNew.png)

  Sie werden zum [Power Platform-Admin-Center](https://admin.powerplatform.microsoft.com/projectoperationstrial) weitergeleitet.

## <a name="questionnaire-and-provisioning"></a>Fragebogen und Bereitstellung

1.  Wechseln Sie zum [Power Platform-Admin Center](https://admin.powerplatform.com/projectoperationstrial) und vervollständigen Sie den Fragebogen.  
2.  Überprüfen Sie den empfohlenen Bereitstellungstyp und wählen Sie **Einrichtung starten** aus, um die Bereitstellung zu initiieren.
3.  Wiederholen Sie die Bedingungen, und wählen Sie dann **Starten** aus.

   Nach dem Start der Bereitstellung werden Sie zur Umgebungsliste im Power Platform-Admin-Center weitergeleitet. Während der Bereitstellung ist der Status Ihrer Umgebung **PreparingInstance**.
 
  Wenn die Bereitstellung abgeschlossen ist, ist der Status Ihrer Umgebung **Bereit**. Die Bereitstellung der Umgebung umfasst die Bereitstellung von Demodaten.
 
4.  Wählen Sie die jeweilige Microsoft Dataverse-URL und die Finanz- und Betriebs-Apps-URLs, um die Bereitstellung zu überprüfen.

## <a name="configuring-dual-write"></a>Konfigurieren von dualem Schreiben
- Informationen zum Konfigurieren von Sicherheitsrollen für duales Schreiben finden Sie unter [Sicherheitseinstellungen in Project Operations in Dataverse aktualisieren](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Um auf die Dual-write Konfiguration zuzugreifen, navigieren Sie zur Finance and Operations-Instanz und dann zu **Datenverwaltung** > **Duales Schreiben**.
- Informationen zum Konfigurieren von Zuordnungen für duales Schreiben finden Sie unter [Zuordnungen für duales Schreiben in Project Operations ausführen](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Lizenzen zuweisen

Sie benötigen Administratorzugriff auf das Microsoft 365-Portal Ihrer Organisation, um die folgenden Schritte auszuführen.

1. Gehen Sie zum [Microsoft 365 Admin Center](https://portal.office.com/), um die Lizenzen Ihren Benutzern zuzuweisen.

   ![Startseite des Admin Center](./media/14AdminPortal.png)

2. Wählen Sie auf der Seite **Aktive Benutzer** die Benutzer aus, denen Sie eine Lizenz zuweisen möchten.

   ![Lizenzen zuweisen](./media/15AssignLicenses.png)

3. Vergewissern Sie sich, dass die **Dynamics 365 Project Operations-Vorschauversion**-Lizenz ausgewählt wurde, und wählen Sie dann **Änderungen speichern**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Die folgenden Ressourcen bieten hilfreiche Anleitungen, wenn Sie Ihre Journey mit Project Operations beginnen:

- [Videoserie – Überblick über Project Operations mit detaillierten Einblicken und Roadmap](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Bereitstellungstyp festlegen](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Was ist, wenn ich ALM oder ELM für meine Finanz- und Betriebs-Apps-Umgebung benötige?

- Partner, die umfassende Funktionen für das Lebenszyklusmanagement der Umgebung benötigen, finden Informationen unter [Anfrage zur Partner-Sandbox-Lizenz](https://experience.dynamics.com/requestlicense), um das neue Partnerangebot zu prüfen. 
- Partner, die weitere Informationen zu internen Nutzungsrechten suchen, finden Informationen unter [Cloud für interne Nutzungsrechte und Software-Nutzen (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kann ich meine Testversion über 30 Tage hinaus verlängern?
Führen Sie die folgenden Schritte aus, um Ihre Testversion zu verlängern.

1. Im **Microsoft 365 Admin Center** wechseln Sie zu **Fakturierung** > **Ihre Produkte**.
2. Wählen Sie **Dynamics 365 Project Operations (CE) - Vorschautestversion**.
3. Wählen Sie unter **Ablaufdatum** **Datum verlängern** aus.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kann ich ein Upgrade von der Lite-Bereitstellung auf die ressourcen-/nicht lagerbasierte Szenariobereitstellung durchführen?
Derzeit gibt es keine Unterstützung für das Upgrade einer Umgebung von einer Lite- auf eine Bereitstellung ohne Lagerbestand.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Kann ich auf Lifecycle Services (LCS) für meine Finance-Umgebungen zugreifen?  
Nr. Für diese Testversionen erfolgt die Bereitstellung über das Power Platform-Admin-Center. Der Zugriff auf die Finance-Umgebung ist beschränkt.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kann ich meine Testversion in einer bestehenden Umgebung installieren?
Wenn Sie über eine vorhandene Umgebung verfügen, können Sie die Lite-Bereitstellung auf einer vorhandenen Sales-Dataverse-Umgebung aus dem Power Platform-Admin-Center installieren.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
