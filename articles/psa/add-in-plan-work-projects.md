---
title: Arbeit in Microsoft Project mit dem Project Service-Add-In planen
description: Dieses Thema enthält Informationen zum Hinzufügen, Konfigurieren und Verwenden des Microsoft Project-Add-Ins für Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014565"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Arbeit in Microsoft Project mit dem Project Service-Add-In planen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erleichtert Ihnen die Projektplanung und Schätzungen, einschließlich Schätzungen. Sie können die Arbeit so definieren, dass Kosten, Aufwand und Umsatzwert anschaulich dargelegt werden, wenn das endgültige Angebot gesendet wird.  

Sie können [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] installieren und Ihre Planung in der gewohnten Umgebung von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ausführen. Verwenden Sie die leistungsfähigen Planungs- und Verwaltungsfunktionen von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] und aktualisieren Sie anschließend Ihren Projektplan in Project Service Automation.  

> [!IMPORTANT]
> - Wenn Sie die SharePoint Dokumentenverwaltungsfunktion verwenden wollen, um die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Dateien für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekte zu speichern, muss Ihr [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Administrator die Dokumentenverwaltung aktivieren. 
> - Das [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] ist nur mit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition kompatibel.  

## <a name="download-and-install-the-add-in"></a>Laden Sie das Add-In herunter und installieren Sie es.  
 Halten Sie Ihre [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Anmeldeinformationen bereit. Sie benötigen diese Informationen, um eine Verbindung von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] herzustellen.  

1.  Im Download Center können Sie das Add-In für Ihre unterstützte Version von Project Service herunterladen, entweder [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) oder [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Wählen Sie den Link zum Herunterladen.  

3.  Wenn das Herunterladen abgeschlossen ist, wählen Sie **Ja** aus, um das Add-In zu installieren.  

## <a name="configure-the-add-in"></a>Konfigurieren Sie das Add-In.  

1. Öffnen Sie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] und wählen Sie die Registerkarte **Project Service** aus.  

2. Wählen Sie **Verbinden** aus.  

3. Geben Sie die Anmeleinformationen ein und wählen Sie dann **Anmelden** aus.  

   Sie können das Add-In nun verwenden.  

## <a name="read-from-a-template"></a>Lesen aus einer Vorlage  
 Lesen aus einer Vorlage, die Sie in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erstellt und in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] kopiert haben, um Ihre Projektplanung zu beginnen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Erstellen einer Projektvorlage (Project Service Automation)](../psa/create-project-template.md)  

1.  Wählen Sie in der Registerkarte **Project Service** und dann **Lesen** > **Project Service Automation-Projektvorlage** aus.  

2.  Wählen Sie eine Projektvorlage aus der Liste und wählen Sie dann **Öffnen**.  

    > [!NOTE]
    >  Standardmäßig werden die Aufgaben, die aus der Vorlage in Projekt kopiert werden, als „manuell geplant” festgelegt.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Zuweisen von [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Rollen an Projektressourcen  

1.  Öffnen Sie ein Projekt und wählen Sie im Menüband **Aufgabe** aus.  

2. Wählen Sie das Menü **Gantt-Diagramm** und dann **Ressourcen-Blatt**.  

3. Wählen Sie im Ressourcen-Blatt das Dropdownmenü **Project Service-Ressourcenrolle** aus und wählen Sie eine Project Service Automation-Rolle aus.  

## <a name="staff-your-project-with-resources"></a>Besetzen Sie Ihr Projekt mit Ressourcen  

1.  Wählen Sie in der Project Service-Registerkarte eine Zeile aus und wählen Sie **Ressourcen suchen**.  

2.  Wählen Sie in der Ansicht **Ressource buchen** die Ressource aus, die Sie für das Projekt verwenden möchten.  

3.  Wählen Sie **Nestermann** aus und dann **OK**.  

## <a name="publish-your-project"></a>Veröffentlichen Sie Ihr Projekt  
Wenn Ihre Projektplanung abgeschlossen ist, wird im nächsten Schritt das Projekt in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert und veröffentlicht.  

Das Projekt wird in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert. Der Preisberechnungs- und Teamgenerierungsprozess wird angewendet. Öffnen Sie das Projekt in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], um zu überprüfen, ob das Team, Projektvorkalkulationen und der Projektstrukturplan generiert wurden. Die folgende Tabelle gibt Aufschluss darüber, wo Sie die Ergebnisse finden.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-Diagramme**   | Importe im Bildschirm in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektstrukturplan**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressourcenblatt** |   Importe im Bildschirm [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektteammitglieder**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Verwendungs-Verwendung**    |    Import im Bildschirm [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektschätzungen**.     |

**Projekt importieren und veröffentlichen**  
1. Gehen Sie in der Registerkarte **Project Service** zu **Veröffentlichen** > **New Project Service Automation**.  

2. Im Dialogfeld **In einem neuen Projekt in Project Service veröffentlichen** geben Sie den **Projektnamen** ein und wählen Sie **Kunde** aus.  

3. Überprüfen Sie dann optional **Projektplan mit Project Service Automation verknüpfen**, um die geplante Projektdatei mit Project Service Automation zu verknüpfen.  

4. Wählen Sie **Veröffentlichen** aus.  

   Durch das Verknüpfen der Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wird die Projektdatei zur Masterdatei und legt den Projektstrukturplan in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] auf schreibgeschützt fest.  Um Änderungen am Projektplan vorzunehmen, müssen Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vornehmen und sie als Aktualisierungen für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] veröffentlichen.  

## <a name="edit-a-project-thats-been-imported"></a>Ein Projekt, das importiert wurde, bearbeiten  
 Wenn Sie Änderungen an einem Projektplan vornehmen wollen, der in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] importiert wurde, haben Sie zwei Möglichkeiten:  

- Öffnen Sie die Masterdatei und bearbeiten Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Enfernen Sie die Verknüpfung der Datei und bearbeiten Sie sie direkt in Project Service. Standardmäßig ist ein Projekt, das von [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] hochgeladen wurde, gesperrt und kann nur in Projekt bearbeitet werden. Um die Datei in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zu bearbeiten, muß auch die Verknüpfung der Datei gelöscht werden.  

### <a name="edit-in-pn_microsoft_project"></a>In [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] bearbeiten  

1. Im Hauptmenü gehen Sie zu **Project Service** > **Projekte**.  

2. Öffnen Sie in der Liste von Projekten jenes, das Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] erstellt haben.  

3. Wählen Sie im Menüband **In MS Project öffnen**. Die verknüpfte Masterdatei wird in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] geöffnet.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Enfernen Sie die Verknüpfung der Datei und bearbeiten Sie sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Im Hauptmenü gehen Sie zu **Project Service** > **Projekte**.  

2. Öffnen Sie in der Liste von Projekten jenes, das Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] erstellt haben.  

3. Wählen Sie im Menüband **Projekt von MS Project lösen**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Hochladen einer Projektdatei zu SharePoint oder Office-Gruppen  
 Sie können Ihre Projektdatei in SharePoint hochladen und sie unter den zugeordneten Dokumenten für Ihr [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Projekt suchen.  Ihr Administrator muss die -Dokumentenverwaltung für SharePoint konfigurieren und anschließend für die Projektentität aktivieren. 

 Wenn Sie Office-Gruppen eingerichtet haben, können Sie Ihre Projektdatei auch auf [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hochladen.

### <a name="upload-a-file-for-sharepoint"></a>Hochladen einer Datei für SharePoint  

1. Im Hauptmenü gehen Sie zu **Project Service** > **Hochladen**.  

2. Wählen Sie **An Project Service Automation-Projektdokumente**.  

3. Im Dialogfeld **Aktivierung öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wählen Sie **Ja** oder **Nein** aus.  

   - Wenn Sie **Ja** wählen, können Sie auf die **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-Schaltfläche in Project Service Automation klicken, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten und die Projektdatei aus der SharePoint-Dokumentbibliothek laden.  

   - Wenn Sie **Nein** wählen, wird der Link für **Öffnen Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nicht funktionieren.  

4. Die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-Datei ist in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] unter **Dokumente** für das entsprechende [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekt verfügbar.  

### <a name="upload-a-file-for-office-groups"></a>Eine Datei für Office-Gruppen hochladen.  

1. Im Hauptmenü gehen Sie zu **Project Service** > **Hochladen**.  

2. Wählen Sie **An Project Service Automation-Projektdokumente**.  

3. Im Dialogfeld **Aktivierung öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** wählen Sie **Ja** oder **Nein** aus.  

   - Wenn Sie **Ja** wählen, können Sie auf die **Öffnen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-Schaltfläche in Project Service Automation klicken und [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten und die Projektdatei aus der SharePoint-Dokumentbibliothek laden.  

   - Wenn Sie **Nein** wählen, wird der Link für **Öffnen Sie in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nicht funktionieren.  

4. Die [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-Datei ist in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] unter **Dokumente** für das entsprechende [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Projekt verfügbar.  

## <a name="publish--your-project-as-a-template"></a>Veröffentlichen Ihres Projekts als Vorlage  
 Sie können das Projekt speichern und erneut verwenden, indem Sie es als Projektvorlage in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] speichern. Projektvorlagen sind wieder verwendbare Projektpläne in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Weitere Informationen finden Sie unter [Projektvorlage erstellen (Project Service Automation)](../psa/create-project-template.md). 

1. Gehen Sie in der Registerkarte **Project Service** zu **Veröffentlichen** > **Neue Project Service Automation Projektvorlage**.  

2. Geben Sie im Dialogfeld **In einem neuen Projekt in Project Service-Vorlage veröffentlichen** den **Projektvorlagennamen** ein.  

3. Wählen Sie optional **Projektplan mit Project Service Automation verknüpfen**, um die geplante Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zu verknüpfen.  

4. Wählen Sie **Veröffentlichen** aus.  

Durch das Verknüpfen der Projektdatei mit [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wird die Projektdatei zur Masterdatei und legt den Projektstrukturplan in der [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Vorlage auf schreibgeschützt fest.  Um Änderungen am Projektplan vorzunehmen, müssen Sie diese in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vornehmen und sie als Aktualisierungen für [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] veröffentlichen.

## <a name="read-a-resource-loaded-schedule"></a>Lesen Sie einen Zeitplan mit geladenen Ressourcen

Beim Lesen eines Projekts aus Project Service Automation wird der Kalender der Ressource nicht mit dem Desktopclient synchronisiert. Wenn es Unterschiede in der Dauer, dem Aufwand oder dem Ende der Aufgabe gibt, liegt dies wahrscheinlich daran, dass auf die Ressourcen und den Desktopclient nicht derselbe Arbeitsstundenvorlagenkalender auf das Projekt angewendet wird.


## <a name="data-synchronization"></a>Datensynchronisierung
Die Tabellen in diesem Abschnitt enthalten Informationen zur Synchronisierung von Entitätsdaten zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In.

### <a name="project-task-entity-table"></a>Entitätstabelle für Projektaufgaben
In der folgenden Tabelle wird beschrieben, wie Entitätsdaten zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In synchronisiert werden.

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Projektaufgabe | Fälligkeits- datum | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Geschätzter Aufwand | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | MS Project-Client-ID | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Übergeordnete Aufgabe | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Project | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Projektaufgabe | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Name der Projektaufgabe | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Ressourcenzuordnungseinheit (veraltet in Version 3.0) | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Geplante Dauer | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | Startdatum | Synchronisiert | Nicht synchronisiert |
| Projektaufgabe | PSP-ID | Synchronisiert | Nicht synchronisiert |

### <a name="team-member-entity-table"></a>Entitätstabelle für Teammitglieder
In der folgenden Tabelle wird beschrieben, wie Entitätsdaten von Teammitgliedern zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In synchronisiert werden

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Teammitglied | MS Project-Client-ID | Synchronisiert | Nicht synchronisiert |
| Teammitglied | Positionsname | Synchronisiert | Nicht synchronisiert |
| Teammitglied | Projekt | Synchronisiert | Synchronisiert |
| Teammitglied | Projektteam | Synchronisiert | Synchronisiert |
| Teammitglied | Ressourcenzuordnungseinheit | Nicht synchronisiert | Synchronisiert |
| Teammitglied | Rolle | Nicht synchronisiert | Synchronisiert |
| Teammitglied | Arbeitszeit | Nicht synchronisiert | Nicht synchronisiert |

### <a name="resource-assignment-entity-table"></a>Entitätstabelle für die Ressourcenzuweisung
In der folgenden Tabelle wird beschrieben, wie Entitätsdaten von Ressourcenzuweisungen zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In synchronisiert werden

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Ressourcenzuweisung | Startdatum | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Stunden | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | MS Project-Client-ID | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Geplante Arbeit | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Project | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Projektteam | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Ressourcenzuweisung | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Aufgabe | Synchronisiert | Nicht synchronisiert |
| Ressourcenzuweisung | Bis heute | Synchronisiert | Nicht synchronisiert |

### <a name="project-task-dependencies-entity-table"></a>Entitätstabellenabhängigkeiten für Projektaufgaben
In der folgenden Tabelle wird beschrieben, wie Entitätsdaten von Projektaufgabenabhängigkeiten zwischen Project Service Automation und dem Microsoft Project-Desktop-Add-In synchronisiert werden

| **Entität** | **Feld** | **Microsoft Project zu Project Service Automation** | **Project Service Automation zu Microsoft Project** |
| --- | --- | --- | --- |
| Abhängigkeiten der Projektaufgaben | Abhängigkeit der Projektaufgaben | Synchronisiert | Nicht synchronisiert |
| Abhängigkeiten der Projektaufgaben | Verknüpfungstyp | Synchronisiert | Nicht synchronisiert |
| Abhängigkeiten der Projektaufgaben | Vorherige Aufgabe | Synchronisiert | Nicht synchronisiert |
| Abhängigkeiten der Projektaufgaben | Project | Synchronisiert | Nicht synchronisiert |
| Abhängigkeiten der Projektaufgaben | Nachfolgende Aufgabe | Synchronisiert | Nicht synchronisiert |

### <a name="additional-resources"></a>Zusätzliche Ressourcen
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]