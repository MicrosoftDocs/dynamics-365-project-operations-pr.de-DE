---
title: Verwenden Sie das Project Service-Add-In, um Ihre Arbeit in Microsoft Project planen | MicrosoftDocs
description: In diesem Artikel erfahren Sie, wie Sie das Microsoft Project Add-In für Microsoft Project Service hinzufügen, konfigurieren und verwenden.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925533"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Verwenden Sie das Project Service Automation-Add-In, um Ihre Arbeit in Microsoft Project planen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erleichtert Ihnen die Projektplanung und Schätzungen, einschließlich Schätzungen. Sie können die Arbeit so definieren, dass Kosten, Aufwand und Umsatzwert anschaulich dargelegt werden, wenn das endgültige Angebot gesendet wird.  

 Sie können jetzt [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] installieren und Ihre Planung in der gewohnten Umgebung von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] auszuführen. Verwenden Sie die leistungsfähigen Planungs- und Verwaltungsfunktionen von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] und aktualisieren Sie anschließend Ihren Projektplan in Project Service Automation.  

> [!IMPORTANT]
> - Wenn Sie die SharePoint Dokumentenverwaltungsfunktion verwenden wollen, um die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Dateien für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekte zu speichern, muss Ihr [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Administrator die Dokumentenverwaltung aktivieren. 
> - Das [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ist nur mit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition kompatibel.  

## <a name="download-and-install-the-add-in"></a>Laden Sie das Add-In herunter und installieren Sie es.  
 Halten Sie Ihre [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Anmeldeinformationen bereit. Sie benötigen diese Informationen, um eine Verbindung von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] herzustellen.  

1.  Im Download Center können Sie das Add-In für Ihre unterstützte Version von Project Service herunterladen, entweder [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) oder [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klicken Sie auf den Downloadlink.  

3.  Wenn das Herunterladen abgeschlossen ist, klicken Sie auf **Ja**, um das Add-In zu installieren.  

## <a name="configure-the-add-in"></a>Konfigurieren Sie das Add-In.  

1. Öffnen Sie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] und klicken Sie auf die Registerkarte **Project Service**.  

2. Klicken Sie auf **Verbinden**.  

3. Geben Sie die Anmeleinformationen ein und klicken Sie dann auf **Anmelden**.  

   Sie können das Add-In nun verwenden.  

## <a name="read-from-a-template"></a>Lesen aus einer Vorlage  
 Lesen aus einer Vorlage, die Sie in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erstellt und in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] kopiert haben, um Ihre Projektplanung zu beginnen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Erstellen einer Projektvorlage (Project Service Automation)](../psa/create-project-template.md)  

1.  Klicken Sie in der Registerkarte **Project Service** auf **Lesen** > **Project Service Automation-Projektvorlage**.  

2.  Wählen Sie eine Projektvorlage aus der Liste und klicken Sie dann auf **Öffnen**.  

    > [!NOTE]
    >  Standardmäßig werden die Aufgaben, die aus der Vorlage in Projekt kopiert werden, als „manuell geplant“ festgelegt.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Zuweisen von [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Rollen an Projektressourcen  

1.  Öffnen Sie ein Projekt und klicken Sie im Menüband auf **Aufgabe**.  

2.  Klicken Sie auf das Menü **Gantt-Diagramm** und dann auf **Ressourcen-Blatt**.  

3.  Klicken Sie im Ressourcen-Blatt auf das Dropdownmenü **Project Service-Ressourcenrolle** und wählen Sie eine Project Service Automation-Rolle aus.  

## <a name="staff-your-project-with-resources"></a>Besetzen Sie Ihr Projekt mit Ressourcen  

1.  Wählen Sie in der Project Service-Registerkarte eine Zeile aus und klicken Sie auf **Ressourcen suchen**.  

2.  Wählen Sie in der Ansicht **Ressource buchen** die Ressource aus, die Sie für das Projekt verwenden möchten.  

3.  Klicken Sie auf **Buchen**, und dann auf **OK**.  

## <a name="publish-your-project"></a>Veröffentlichen Sie Ihr Projekt  
Wenn Ihre Projektplanung abgeschlossen ist, wird im nächsten Schritt das Projekt in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert und veröffentlicht.  

Das Projekt wird in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert. Der Preisberechnungs- und Teamgenerierungsprozess wird angewendet. Öffnen Sie das Projekt in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], um zu überprüfen, ob das Team, Projektvorkalkulationen und der Projektstrukturplan generiert wurden. Die folgende Tabelle gibt Aufschluss darüber, wo Sie die Ergebnisse finden:

| Project | Informationen |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-Diagramme**   | Importe im Bildschirm in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektstrukturplan**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressourcenblatt** |   Importe im Bildschirm [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektteammitglieder**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Verwendungs-Verwendung**    |    Import im Bildschirm [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektschätzungen**.     |

**Projekt importieren und veröffentlichen**  
1. Klicken Sie in der Registerkarte **Project Service** auf **Veröffentlichen** > **New Project Service Automation**.  

2. Geben Sie im Dialogfeld **In einem neuen Projekt in Project Service veröffentlichen** den **Projektnamen** ein und wählen Sie **Kunde** aus.  

3. Überprüfen Sie optional **Projektplan mit Project Service Automation verknüpfen**, um die geplante Projektdatei mit Project Service Automation zu verknüpfen.  

4. Klicken Sie auf **Veröffentlichen**.  

   Durch das Verknüpfen der Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wird die Projektdatei zur Masterdatei und legt den Projektstrukturplan in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] auf schreibgeschützt fest.  Um Änderungen am Projektplan vorzunehmen, müssen Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vornehmen und sie als Aktualisierungen für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] veröffentlichen.  

## <a name="edit-a-project-thats-been-imported"></a>Ein Projekt, das importiert wurde, bearbeiten  
 Wenn Sie Änderungen an einem Projektplan vornehmen wollen, der in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert wurde, haben Sie zwei Möglichkeiten:  

- Öffnen Sie die Masterdatei und bearbeiten Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Enfernen Sie die Verknüpfung der Datei und bearbeiten Sie sie direkt in Project Service. Standardmäßig ist ein Projekt, das von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] hochgeladen wurde, gesperrt und kann nur in Projekt bearbeitet werden. Um die Datei in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zu bearbeiten, muß auch die Verknüpfung der Datei gelöscht werden.  

### <a name="edit-in-pn_microsoft_project"></a>Bearbeiten Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Klicken Sie im Hauptmenü auf **Project Service** > **Projekte**.  

2. Öffnen Sie in der Liste von Projekten das, das Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] erstellt haben.  

3. Klicken Sie im Menüband auf **In MS Project öffnen**. Die verknüpfte Masterdatei wird in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] geöffnet.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Enfernen Sie die Verknüpfung der Datei und bearbeiten Sie sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Klicken Sie im Hauptmenü auf **Project Service** > **Projekte**.  

2. Öffnen Sie in der Liste von Projekten das, das Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] erstellt haben.  

3. Klicken Sie im Menüband auf **Projekt von MS Project lösen**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Hochladen einer Projektdatei zu SharePoint oder Office-Gruppen  
 Sie können Ihre Projektdatei in SharePoint hochladen und sie unter den zugeordneten Dokumenten für Ihr [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Projekt suchen.  Ihr Administrator muss die -Dokumentenverwaltung für SharePoint konfigurieren und anschließend für die Projektentität aktivieren. 

 Wenn Sie Office-Gruppen eingerichtet haben, können Sie Ihre Projektdatei auch auf [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hochladen.

### <a name="upload-a-file-for-sharepoint"></a>Hochladen einer Datei für SharePoint  

1. Klicken Sie im Hauptmenü auf **Project Service** > **Hochladen**.  

2. Wählen Sie **An Project Service Automation-Projektdokumente**.  

3. Im Dialogfeld von **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wählen Sie **Ja** oder **Nein** aus.  

   - Wenn Sie auf **Ja** klicken, können Sie auf die **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** Schaltfläche in Project Service Automation klicken, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten und die Projektdatei aus der SharePoint Dokumentbibliothek laden.  

   - Wenn Sie **Nein** klicken, ist die Schaltfläche **Öfffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nicht aktiviert.  

4. Die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-Datei ist in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] unter **Dokumente** für das entsprechende [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekt verfügbar.  

### <a name="upload-a-file-for-office-groups"></a>Eine Datei für Office-Gruppen hochladen.  

1. Klicken Sie im Hauptmenü auf **Project Service** > **Hochladen**.  

2. Wählen Sie **An Project Service Automation-Projektdokumente**.  

3. Im Dialogfeld von **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wählen Sie **Ja** oder **Nein** aus.  

   - Wenn Sie auf **Ja** klicken, können Sie auf die Schaltfläche **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** in Project Service Automation klicken, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten und die Projektdatei aus der SharePoint Dokumentbibliothek laden.  

   - Wenn Sie **Nein** klicken, ist die Schaltfläche **Öfffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nicht aktiviert.  

4. Die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-Datei ist in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] unter **Dokumente** für das entsprechende [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekt verfügbar.  

## <a name="publish--your-project-as-a-template"></a>Veröffentlichen Ihres Projekts als Vorlage  
 Sie können das Projekt speichern und erneut verwenden, indem Sie es als Projektvorlage in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] speichern.  Projektvorlagen sind wieder verwendbare Projektpläne in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Erstellen einer Projektvorlage (Project Service Automation)](../psa/create-project-template.md)  

1. Klicken Sie in der Registerkarte **Project Service** auf **Veröffentlichen** > **Neue Project Service Automation Projekt-Vorlage**.  

2. Geben Sie im Dialogfeld **In einem neuen Projekt in Project Service-Vorlage veröffentlichen** den **Projektvorlagennamen** ein.  

3. Überprüfen Sie optional **Projektplan mit Project Service Automation verknüpfen**, um dann die geplante Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zu verknüpfen.  

4. Klicken Sie auf **Veröffentlichen**.  

Durch das Verknüpfen der Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wird die Projektdatei zur Masterdatei und legt den Projektstrukturplan in der [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Vorlage auf schreibgeschützt fest.  Um Änderungen am Projektplan vorzunehmen, müssen Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vornehmen und sie als Aktualisierungen für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] veröffentlichen.

## <a name="read-a-resource-loaded-schedule"></a>Lesen Sie einen Zeitplan mit geladenen Ressourcen

Beim Lesen eines Projekts aus Project Service Automation wird der Kalender der Ressource nicht mit dem Desktopclient synchronisiert. Wenn es Unterschiede in der Dauer, dem Aufwand oder dem Ende der Aufgabe gibt, liegt dies wahrscheinlich daran, dass auf die Ressourcen und den Desktopclient nicht derselbe Arbeitsstundenvorlagenkalender auf das Projekt angewendet wird.


## <a name="data-synchronization"></a>Datensynchronisierung

In der folgenden Tabelle wird beschrieben, wie Daten zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In synchronisiert werden.

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Projektaufgabe | Fälligkeits- datum | ● | - |
| Projektaufgabe | Geschätzter Aufwand | ● | - |
| Projektaufgabe | MS Project-Client-ID | ● | - |
| Projektaufgabe | Übergeordnete Aufgabe | ● | - |
| Projektaufgabe | Project | ● | - |
| Projektaufgabe | Projektaufgabe | ● | - |
| Projektaufgabe | Name der Projektaufgabe | ● | - |
| Projektaufgabe | Ressourcenzuordnungseinheit (veraltet in Version 3.0) | ● | - |
| Projektaufgabe | Geplante Dauer | ● | - |
| Projektaufgabe | Startdatum | ● | - |
| Projektaufgabe | PSP-ID | ● | - |

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Teammitglied | MS Project-Client-ID | ● | - |
| Teammitglied | Positionsname | ● | - |
| Teammitglied | Projekt | ● | ● |
| Teammitglied | Projektteam | ● | ● |
| Teammitglied | Ressourcenzuordnungseinheit | - | ● |
| Teammitglied | Rolle | - | ● |
| Teammitglied | Arbeitszeit | Nicht synchronisiert | Nicht synchronisiert |

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Ressourcenzuweisung | Startdatum | ● | - |
| Ressourcenzuweisung | Stunden | ● | - |
| Ressourcenzuweisung | MS Project-Client-ID | ● | - |
| Ressourcenzuweisung | Geplante Arbeit | ● | - |
| Ressourcenzuweisung | Project | ● | - |
| Ressourcenzuweisung | Projektteam | ● | - |
| Ressourcenzuweisung | Ressourcenzuweisung | ● | - |
| Ressourcenzuweisung | Task | ● | - |
| Ressourcenzuweisung | Bis heute | ● | - |

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Abhängigkeiten der Projektaufgaben | Abhängigkeit der Projektaufgaben | ● | - |
| Abhängigkeiten der Projektaufgaben | Verknüpfungstyp | ● | - |
| Abhängigkeiten der Projektaufgaben | Vorherige Aufgabe | ● | - |
| Abhängigkeiten der Projektaufgaben | Project | ● | - |
| Abhängigkeiten der Projektaufgaben | Nachfolgende Aufgabe | ● | - |

### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
