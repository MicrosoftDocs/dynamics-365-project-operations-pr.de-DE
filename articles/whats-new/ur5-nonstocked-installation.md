---
title: Aktualisieren Sie Project Operations in Ihrer Finance Umgebung
description: Dieser Artikel beschreibt, wie Sie Project Operations in Ihrer Dynamics 365 Finance Umgebung aktualisieren können.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 0cf9da8cc9d1f29dc41d4b119278e545047020bc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912469"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Aktualisieren Sie Project Operations in Ihrer Finance Umgebung

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_


Dieser Artikel beschreibt, wie Sie Dynamics 365 Project Operations in Ihrer Dynamics 365 Finance Umgebung aktualisieren können. Es sind drei Verfahren erforderlich, um Project Operations auf Update 5 (UR5) zu aktualisieren:

- [Importieren Sie das Paket in Ihr Vorschauprojekt](#import)
- [Wenden Sie das Update](#apply)
- [Ihre Dataverse Umgebung einrichten](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importieren Sie das Paket in Ihr LCS Projekt

1. Melden Sie sich bei [Lifecycle Services (LCS)](https://lcs.dynamics.com/) als Projektbesitzer oder Umgebungsmanager.
2. Wählen Sie in der Liste Ihrer Projekte Ihre LCS Projekt aus.
3. Auf der Seite **Projekt** in der Gruppe **Umgebungen** öffnen Sie die Umgebung, die Sie aktualisieren möchten.
4. Überprüfen Sie, ob die Umgebung ausgeführt wird. Wenn sie nicht gestartet wird, starten Sie die Umgebung.
5. In dem Abschnitt **Neuer Release** unter **Verfügbare Updates** wählen Sie **Update anzeigen** für 10.0.15.

![Schaltfläche aktualisieren anzeigen.](media/view-update.png)

6. Wählen Sie auf der Seite **Binäre Updates** die Option **Paket speichern** aus.
7. Wählen Sie auf der Seite **Updates überprüfen und speichern** die Option **Paket speichern** aus.
8. Geben Sie auf dem sich öffnenden Bereich **Paket in der Anlagebibliothek speichern** den Paketnamen ein und wählen Sie dann **Paket speichern** aus.
9. Wenn LCS das Paket gespeichert hat, wird die Schaltfläche **Fertig** aktiviert. Wählen Sie **Fertig** aus. LCS überprüft das Paket. Die Überprüfung kann einige Minuten oder bis zu einer Stunde dauern.


## <a name="apply-the-package-update"></a><a name="apply"></a>Wenden Sie die Paketaktualisierung an

1. In LCS wählen Sie auf der Seite **Umgebungsdetails** die Option **Verwalten** > **Aktualisierungen übernehmen** aus, um eine Aktualisierung zu übernehmen.
2. Wählen Sie aus der Liste das Paket aus, das Sie zuvor gespeichert haben, und wählen Sie dann **Anwenden** aus.
3. Klicken Sie auf **Ja**, um zu bestätigen, dass Sie das Paket bereitstellen möchten.

![Bestätigen Sie das Dialogfeld für die Paketbereitstellung.](media/confirm-package-deployment.png)

4. Klicken Sie auf **Ja**, um zu bestätigen, dass Sie die Anwendung aktualisieren möchten.

![Bestätigen Sie das Dialogfeld Anwendungsaktualisierung.](media/confirm-application-update.png)

Die Bereitstellung und die Aktualisierung der Anwendung werden gestartet. 

Auf der Seite **Umgebungsdetails** in der oberen rechten Ecke wird der Umgebungsstatus auf **Wartung** aktualisiert. In ungefähr zwei Stunden ist die Aktualisierung abgeschlossen. Die Informationen zur Anwendungsversion werden auf **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** und der Umgebungsstatus auf **Bereitgestellt** aktualisiert.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Ihre Dataverse Umgebung einrichten

1. Melden Sie sich beim [Power Platform Admin Center](https://admin.powerplatform.com/) an.
2. Suchen und öffnen Sie in der Liste die Umgebung, in der Sie Project Operations installiert haben.
3. Auf der Seite **Umgebungen** wählen Sie **Ressource** > **Dynamics 365-Apps**.
4. Suchen Sie in der Liste **Microsoft Dynamics 365 Project Operations**, und in der Spalte **Status** wählen Sie **Aktualisierung verfügbar**.
5. Wählen Sie **Ich stimme den Nutzungsbedingungen zu** und Aktivieren Sie das Kontrollkästchen, und wählen Sie dann **Aktualisieren** aus. Die neueste Version der Lösung wird installiert.

Nach Abschluss der Installation ist die Version 4.5.0.134 installiert.

## <a name="configure-new-features"></a>Neue Funktionen konfigurieren

### <a name="enable-dual-write-mapping"></a>Duales Schreiben im Mapping aktivieren

Nachdem Sie die Aktualisierung auf Finance und Dataverse Umgebungen abgeschlossen haben, können Sie die erforderlichen Zuordnungen für duales Schreiben aktivieren. Folgende Abläufe für duales Schreiben aktivieren beenden.

- [Aktualisieren Sie die Sicherheitseinstellungen in der Customer Engagement Umgebung](#security)
- [Daten in Entitäten aktualisieren](#refresh)
- [Aktualisieren Sie die Zuordnungen für duales Schreiben und führen Sie sie aus](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Aktualisieren Sie die Sicherheitseinstellungen in der Dataverse Umgebung

Die folgenden Aktualisierungen der Sicherheitsberechtigungen für Entitäten sind im Rahmen der Aktualisierung auf UR5 erforderlich.

1. In Ihrer Dataverse Umgebung gehen Sie zu **Einstellungen** und in der **System** Gruppe wählen Sie **Sicherheit** aus.

![Dataverse-Umgebungseinstellungen.](media/Picture21.png)

2. Wählen Sie **Sicherheitsrollen** aus.
3. In der Liste der Rollen wählen Sie **App-Benutzer duales Schreiben** und wählen Sie die Registerkarte **Benutzerdefinierte Entitäten** aus. 
4. Stellen Sie sicher, dass die Rolle Berechtigung für **Lesen** und **Anfügen** hat:

      - **Währungswechselkurstyp eingeben**
      - **Kontenplan** 
      - **Steuerkalender** 
      - **Sachkonto**

5. Nachdem die Sicherheitsrolle aktualisiert wurde, gehen Sie zu **Einstellungen** > **Sicherheit** > **Teams**. Stellen Sie sicher, dass die Rolle **App Benutzer duales Schreiben** auf das Team angewendet wird. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Aktualisieren Sie Datenentitäten aus der Aktualisierung

1. Öffnen Sie in Ihrer Finance Umgebung den Arbeitsbereich **Datenverwaltung** und öffnen Sie dann die Seite **Framework-Parameter**.
2. Auf der **Entitätseinstellungen** Registerkarte wählen Sie **Entitätsliste aktualisieren** aus.
3. Wählen Sie **Schließen**, um die Aktualisierung der Entität zu bestätigen.

 > [!NOTE]
 > Dieser Prozess kann ungefähr 20 Minuten dauern. Sie werden benachrichtigt, wenn die Aktualisierung abgeschlossen ist.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Duales Schreiben im Mapping aktivieren

1. Wählen Sie **duales Schreiben** im Arbeitsbereich **Datenverwaltung** aus.
2. Wählen Sie **Lösungen anwenden** und wählen Sie beide Lösungen in der Liste aus und wählen Sie dann **Anwenden**.
3. Auf der Seite **duales Schreiben** wählen Sie die folgenden Tabellenzuordnungen aus und wählen Sie dann **Anhalten**.

    - **Tatsächliche Werte der Project Operations-Integration (msdyn_actuals)**
    - **Project Operations Integartion Projektausgabenkategorien (msdyn_expensecategories)**
    - **Project Operations Integartion tatsächliche Projektausgabenkategorien (msdyn_expenses)**

4. Auf der Seite **Tabellenzuordnungsversion** wenden Sie auf jede der drei Entitäten eine neue Version der Zuordnung an.
5. Auf der Seite **Duales Schreiben** wählen Sie ausführen aus, um die Zuordnungen neu zu starten.
6. Wählen Sie aus der Liste der Zuordnungen **Ledger (msdyn_ledgers)** mit allen Voraussetzungen aus und wählen Sie das Kontrollkästchen **Erstsynchronisation** aus. 
7. Wählen Sie in dem **Master für Erstsynchronisierung**-Feld **Finanz- und Betriebs-Apps** und dann **Ausführen**.
 
 ![Synchronisation der Ledger-Zuordnung.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]