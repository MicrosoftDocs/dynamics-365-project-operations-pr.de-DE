---
title: Project Operations-Demodaten auf eine in der Cloud gehostete Finance-Umgebung anwenden
description: In diesem Thema wird erläutert, wie Demodaten aus Project Operations auf eine Cloud-gehostete Dynamics 365 Finance-Umgebung angewendet werden.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096621"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Project Operations-Demodaten auf eine in der Cloud gehostete Finance-Umgebung anwenden

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

> [!IMPORTANT]
> Dieses Thema gilt nur für die Microsoft Dynamics 365 Finance Version 10.0.13 und kann nur in einer Cloud-gehosteten Umgebung ausgeführt werden. Führen Sie die Schritte in diesem Thema aus, **BEVOR** Sie Qualitätsaktualisierungen auf die Umgebung anwenden.

1. Öffnen Sie in Ihrem LCS-Projekt die Seite **Umgebungsdetails**. Beachten Sie, dass es die Details enthält, die für die Verbindung mit der Umgebung mithilfe des RDP (Remote Desktop Protocol) erforderlich sind.

![-Umgebungsdetails](./media/1EnvironmentDetails.png)

Die ersten hervorgehobenen Anmeldeinformationen sind die Anmeldeinformationen des lokalen Kontos und enthalten einen Hyperlink zur Remotedesktopverbindung. Zu den Anmeldeinformationen gehören der Benutzername und das Kennwort des Umgebungsadministrators. Der zweite Satz von Anmeldeinformationen wird verwendet, um sich in dieser Umgebung beim SQL Server anzumelden.

2. Stellen Sie über den Hyperlink in **Lokale Konten** eine Verbindung her, und verwenden Sie die **Anmeldeinformationen für das lokale Konto** , um sich zu authentifizieren.
3. Navigieren Sie zu **Internetinformationsdienste** > **Anwendungspools** > **AOSService** , und beenden Sie den Dienst. Sie beenden den Dienst an dieser Stelle, damit Sie die SQL-Datenbank weiterhin ersetzen können.

![AOS beenden](./media/2StopAOS.png)

4. Navigieren Sie zu **Dienste** , und beenden Sie die folgenden zwei Elemente:

- Microsoft Dynamics 365 Unified Operations: Batchverwaltungsdienst
- Microsoft Dynamics 365 Unified Operations: Datenimport/-export-Framework

![Dienste anhalten](./media/3StopServices.png)

5. Öffnen Sie Microsoft SQL Server Management Studio. Melden Sie sich mit SQL Server-Anmeldeinformationen an, und verwenden Sie den Benutzer axdbadmin und das Kennwort von der LCS-Seite **Umgebungsdetails**.

![SQL Server Management Studio](./media/4SSMS.png)

6. Suchen Sie in den **Datenbanken** von Object Explorer **AXDB**. Sie ersetzen die Datenbank durch eine neue Datenbank, die sich im [Download-Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) befindet. 
7. Kopieren Sie die Zip-Datei in die VM, mit der Sie remote verbunden sind, und extrahieren Sie die Zip-Inhalte.
8. Klicken Sie in SQL Server Management Studio mit der rechten Maustaste auf **AxDB** , und wählen Sie dann **Aufgaben** > **Wiederherstellen** > **Datenbank** aus.

![Datenbank wiederherstellen](./media/5RestoreDatabase.png)

9. Wählen Sie **Quellgerät** aus, und navigieren Sie zu der Datei, die aus der von Ihnen kopierten Zip-Datei extrahiert wurde.

![Quellgeräte](./media/6SourceDevice.png)

10. Wählen Sie **Optionen** und dann **Vorhandene Datenbank überschreiben** sowie **Vorhandene Verbindungen zur Zieldatenbank schließen** aus. 
11. Klicken Sie auf **OK**.

![Einstellungen wiederherstellen](./media/7RestoreSetting.png)

Sie erhalten eine Bestätigung, dass die AXDB-Wiederherstellung erfolgreich war. Nachdem Sie diese Bestätigung erhalten haben, können Sie SQL Services Management Studio schließen.

12. Navigieren Sie zu **Internetinformationsdienste** > **Anwendungspools** > **AOSService** , und starten Sie AOSService.
13. Navigieren Sie zu **Dienste** , und starten Sie die zwei Dienste, die Sie zuvor angehalten haben.

14. Suchen Sie das AdminUserProvisioning-Tool auf dieser VM. Schauen Sie unter K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe nach.
15. Führen Sie die .ext-Datei mit Ihrer Benutzeradresse im Feld **E-Mail-Adresse** aus. 
16. Wählen Sie **Übermitteln** aus.

![Administratorbenutzerbereitstellung](./media/8AdminUserProvisioning.png)

Dies kann einige Minuten dauern. Sie sollten eine Bestätigungsnachricht erhalten, dass der Administratorbenutzer erfolgreich aktualisiert wurde.

17. Führen Sie abschließend die Eingabeaufforderung als Administrator aus, und führen Sie iisreset durch.

![IIS-Neustart](./media/9IISReset.png)

18. Schließen Sie die Remotedesktopsitzung, und verwenden Sie die LCS-Seite **Umgebungsdetails** , um sich bei der Umgebung anzumelden und zu bestätigen, dass sie wie erwartet funktioniert.

![Finance and Operations](./media/10FinanceAndOperations.png)
