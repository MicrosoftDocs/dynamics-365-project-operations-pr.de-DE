---
title: Projektzeitplan-APIs mit Power Automate verwenden
description: Dieser Artikel enthält einen beispielhaften Flow, der die Programmierschnittstellen (APIs) von Project Schedule verwendet.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404398"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projektzeitplan-APIs mit Power Automate verwenden

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Dieser Artikel beschreibt einen beispielhaften Flow, der zeigt, wie Sie einen vollständigen Projektplan mit Hilfe von Microsoft Power Automate erstellen, wie Sie ein Operation Set festlegen und wie Sie eine Entität aktualisieren. Das Beispiel zeigt, wie Sie ein Projekt, ein Projektteammitglied, Vorgangssätze, Projektaufgaben und Ressourcenzuweisungen erstellen. Dieser Artikel erklärt auch, wie Sie eine Entität aktualisieren und einen Vorgang festlegen.

Im Folgenden finden Sie eine vollständige Liste der Schritte, die im Beispiel-Flow in diesem Artikel dokumentiert sind:

1. [Erstellen eines PowerApps-Triggers](#1)
2. [Erstellen eines Projekts](#2)
3. [Initialisieren einer Variable für das Teammitglied](#3)
4. [Erstellen eines generischen Teammitglieds](#4)
5. [Einen Optionssatz erstellen](#5)
6. [Einen Projekt-Bucket erstellen](#6)
7. [Initialisieren einer Variable für den Verknüpfungsstatus](#7)
8. [Initialisieren einer Variable für die Anzahl der Aufgaben](#8)
9. [Initialisieren einer Variable für die Projektaufgabenkennung](#9)
10. [Erledigen bis](#10)
11. [Eine Projektaufgabe festlegen](#11)
12. [Eine Aufgaben erstellen](#12)
13. [Eine Ressourcenzuweisung erstellen](#13)
14. [Eine Variable verringern](#14)
15. [Eine Projektaufgabe umbenennen](#15)
16. [Einen Optionssatz ausführen](#16)

## <a name="assumptions"></a>Voraussetzungen

Dieser Artikel setzt voraus, dass Sie über grundlegende Kenntnisse der Dataverse-Plattform, der Cloud-Flows und der Projektplanungs-Anwendungsprogrammierschnittstelle (API) verfügen. Weitere Informationen finden Sie im Abschnitt [Referenzen](#references) weiter unten in diesem Artikel.

## <a name="create-a-flow"></a>Workflow erstellen

### <a name="select-an-environment"></a>Umgebung auswählen

Sie können den Power Automate-Flow in Ihrer Umgebung erstellen.

1. Gehen Sie zu <https://flow.microsoft.com> und verwenden Sie Ihre Administrator-Anmeldeinformationen, um sich anzumelden.
2. Wählen Sie oben rechts **Umgebungen** aus.
3. Wählen Sie in der Liste die Umgebung aus, in der Dynamics 365 Project Operations installiert ist.

### <a name="create-a-solution"></a>Lösung erstellen

Mithilfe der folgenden Anleitung können Sie einen [lösungsfähigen Flow](/power-automate/overview-solution-flows) erstellen. Indem Sie einen lösungsorientierten Flow erstellen, können Sie den Flow einfacher exportieren, um ihn später zu verwenden.

1. Wählen Sie im Navigationsbereich **Lösungen**.
2. Wählen Sie auf der Seite **Lösungen** die Option **Neue Lösung** aus.
3. Legen Sie im Dialogfeld **Neue Lösung** die erforderlichen Felder fest, und wählen Sie dann **Erstellen**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Schritt 1: Einen PowerApps-Trigger erstellen

1. Wählen Sie auf der Seite **Lösungen** die Lösung aus, die Sie erstellt haben, und wählen Sie dann **Neu**.
2. Wählen Sie im linken Bereich **Cloud-Flows** \> **Automatisierung** \>**Cloud-Flow** \> **Sofort**.
3. Geben Sie im **Flow-Name**-Feld **API-Demo-Flow planen** ein.
4. In der Liste **Trigger für diesen Flow auswählen** wählen Sie **Power Apps** aus. Beim Erstellen eines Power Apps-Triggers liegt die Logik bei Ihnen als Autor. In diesem Artikel lassen Sie die Eingabeparameter zu Testzwecken leer.
5. Wählen Sie **Erstellen**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Schritt 2: Ein Projekt erstellen

Führen Sie diese Schritte aus, um ein Beispielprojekt zu erstellen.

1. Wählen Sie in dem von Ihnen erstellten Flow **Neuer Schritt**.

    ![Hinzufügen eines neuen Schritts](media/newstep.png)

2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.

    ![Auswählen eines Vorgangs](media/chooseactiontab.png)

3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.

![Umbenennen eines Schritts](media/renamestep.png)

4. Benennen Sie den Schritt in **Projekt erstellen** um.
5. Wählen Sie im Feld **Aktionsname** **msdyn\_CreateProjectV1** aus.
6. Im **msdyn\_subject**-Feld wählen Sie **Dynamische Inhalte hinzufügen**.
7. Auf der **Ausdruck**-Registerkarte geben Sie im Funktionsfeld **Projektname – utcNow()** ein.
8. Klicken Sie auf **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Schritt 3: Initialisieren einer Variable für das Teammitglied

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable initialisieren** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Mitglied des Init-Teams** um.
5. Geben Sie im Feld **Name** den Text **TeamMemberAction** ein.
6. Wählen Sie im Feld **Typ** **Zeichenfolge** aus.
7. Geben Sie im Feld **Wert** **msdyn\_CreateTeamMemberV1** ein.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Schritt 4: Ein generisches Teammitglied erstellen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Teammitglied erstellen** um.
5. Im **Aktionsname**-Feld wählen Sie **TeamMemberAction** in der **Dynamische Inhalte**-Dialogbox.
6. Im **Aktionsparameter**-Feld geben Sie die folgenden Parameterinformationen ein.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Hier finden Sie eine Erklärung der Parameter:

    - **\@\@odata.type** – der Entitätstypname. Geben Sie beispielsweise **"Microsoft.Dynamics.CRM.msdyn\_projectteam"** ein.
    - **msdyn\_projectteamid** – der Primärschlüssel der Projektteam-ID. Der Wert ist eine Globally Unique Identifier- bzw. GUID-Ausdruck.   Die ID wird aus der Registerkarte „Ausdruck“ generiert.

    - **msdyn\_project\@odata.bind** – Die Projekt-ID des verantwortlichen Projekts. Der Wert ist dynamischer Inhalt, der aus der Antwort des Schritts „Projekt erstellen“ stammt. Stellen Sie sicher, dass Sie den vollständigen Pfad eingeben und dynamische Inhalte zwischen den Klammern hinzufügen. Anführungszeichen sind erforderlich. Geben Sie beispielsweise **"/msdyn\_projects(DYNAMISCHEN INHALT HINZUFÜGEN)"** ein.
    - **msdyn\_name** – Der Name des Teammitglieds. Geben Sie zum Beispiel **"ScheduleAPIDemoTM1"** ein.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Schritt 5: Einen Optionssatz erstellen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Operationsset erstellen** um.
5. Im **Aktionsname**-Feld wählen Sie die benutzerdefinierte Dataverse-Aktion **msdyn\_ CreateOperationSetV1** aus.
6. Geben Sie im Feld **Zuordnungsdemo** **ScheduleAPIDemoOperationSet** ein.
7. Geben Sie im Feld **Projekt** **/msdyn\_projects(** ein.
8. Wählen Sie im Dialogfeld **Dynamischer Inhalt** Kästchen **msdyn\_CreateProjectV1Response ProjectId**.
9. Geben Sie im Feld **Projekt** **)** ein.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Schritt 6: Einen Projekt-Bucket erstellen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Neue Zeile hinzufügen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Bucket erstellen** um.
5. Wählen Sie im Feld **Tabellenname** **Projekt-Buckets** aus.
6. Geben Sie im Feld **Name** den Text **ScheduleAPIDemoBucket1** ein.
7. Im Feld **Projekt** geben Sie **msdyn\_CreateProjectV1Response ProjectId** im Dialogfeld **Dynamischer Inhalt** ein.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Schritt 7: Initialisieren einer Variable für den Verknüpfungsstatus

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable initialisieren** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Verbindungsstatus initialisieren** um.
5. Geben Sie im Feld **Name** den Text **linkstatus** ein.
6. Wählen Sie im Feld **Typ** den Wert **Ganzzahl** aus.
7. Geben Sie im Feld **Wert** die Zahl **192350000** ein.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Schritt 8: Initialisieren einer Variable für die Anzahl der Aufgaben

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable initialisieren** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Anzahl der Aufgaben initialisieren** um.
5. Geben Sie im Feld **Name** den Text **Anzahl der Aufgaben** ein.
6. Wählen Sie im Feld **Typ** den Wert **Ganzzahl** aus.
7. Geben Sie im Feld **Wert** die Zahl **5** ein.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Schritt 9: Initialisieren einer Variable für die Projektaufgabenkennung

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable initialisieren** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Init ProjectTaskID** um.
5. Geben Sie im Feld **Name** den Text **Anzahl der Aufgaben** ein.
6. Wählen Sie im Feld **Typ** **Zeichenfolge** aus.
7. Im **Wert**-Feld geben Sie **guid()** im Ausdrucks-Generator ein.

## <a name="step-10-do-until"></a><a id="10"></a>Schritt 10: Erledigen bis

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Erledigen bis** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. Legen Sie den ersten Wert in der bedingten Anweisung auf die **Anzahl der Aufgaben**-Variable aus der **Dynamische Inhalte**-Dialogbox fest.
4. Legen Sie die Bedingung auf **kleiner oder gleich** fest.
5. Setzen Sie den zweiten Wert in der bedingten Anweisung auf **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Schritt 11: Eine Projektaufgabe festlegen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable festlegen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem neuen Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Projektaufgabe festlegen** um.
5. Wählen Sie im **Name**-Feld **msdyn\_projecttaskid** aus.
6. Im **Wert**-Feld geben Sie **guid()** im Ausdrucks-Generator ein.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Schritt 12: Eine Projektaufgabe erstellen

Befolgen Sie diese Schritte, um eine Projektaufgabe mit einer eindeutigen ID zu erstellen, die zum aktuellen Projekt und dem von Ihnen erstellten Projekt-Bucket gehört.

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Projektaufgabe erstellen** um.
5. Wählen Sie im Feld **Aktionsname** **msdyn\_PssCreateV1** aus.
6. Im **Entität**-Feld geben Sie die folgenden Parameterinformationen ein.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Hier finden Sie eine Erklärung der Parameter:

    - **\@\@odata.type** – der Entitätstypname. Geben Sie beispielsweise **"Microsoft.Dynamics.CRM.msdyn\_projecttask"** ein.
    - **msdyn\_projecttaskid** – die eindeutige ID der Aufgabe. Der Wert sollte auf eine dynamische Variable von **msdyn\_projecttaskid** gesetzt werden.
    - **msdyn\_project\@odata.bind** – Die Projekt-ID des verantwortlichen Projekts. Der Wert ist dynamischer Inhalt, der aus der Antwort des Schritts „Projekt erstellen“ stammt. Stellen Sie sicher, dass Sie den vollständigen Pfad eingeben und dynamische Inhalte zwischen den Klammern hinzufügen. Anführungszeichen sind erforderlich. Geben Sie beispielsweise **"/msdyn\_projects(DYNAMISCHEN INHALT HINZUFÜGEN)"** ein.
    - **msdyn\_subject** – beliebiger Aufgabenname.
    - **msdyn\_projectbucket\@odata.bind** – der Projekt-Bucket, der die Aufgaben enthält. Der Wert ist dynamischer Inhalt, der aus der Antwort des Schritts „Bucket erstellen“ stammt. Stellen Sie sicher, dass Sie den vollständigen Pfad eingeben und dynamische Inhalte zwischen den Klammern hinzufügen. Anführungszeichen sind erforderlich. Geben Sie beispielsweise **"/msdyn\_projectbuckets(DYNAMISCHEN INHALT HINZUFÜGEN)"** ein.
    - **msdyn\_start** – dynamische Inhalte für das Startdatum. Beispielsweise wird der nächste Tag als **"addDays(utcNow(), 1)"** dargestellt.
    - **msdyn\_scheduledstart** – das eingeplante Startdatum. Beispielsweise wird der nächste Tag als **"addDays(utcNow(), 1)"** dargestellt.
    - **msdyn\_scheduleend** – Das geplante Enddatum. Wählen Sie ein Datum in der Zukunft aus. Geben Sie zum Beispiel **"addDays(utcNow(), 5)"** an.
    - **msdyn\_LinkStatus** – der Linkstatus. Geben Sie z. B. **"192350000"** ein.

7. Im Feld **OperationSetId** geben Sie **msdyn\_CreateOperationSetV1Response** im Dialogfeld **Dynamischer Inhalt** ein.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Schritt 13: Erstellen einer Ressourcenzuweisung

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Zuweisung erstellen** um.
5. Wählen Sie im Feld **Aktionsname** **msdyn\_PssCreateV1** aus.
6. Im **Entität**-Feld geben Sie die folgenden Parameterinformationen ein.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Im Feld **OperationSetId** geben Sie **msdyn\_CreateOperationSetV1Response** im Dialogfeld **Dynamischer Inhalt** ein.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Schritt 14: Eine Variable verringern

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **Variable verringern** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. Wählen Sie im Feld **Name** den Text **Anzahl der Aufgaben** aus.
4. Geben Sie im Feld **Wert** die Zahl **1** ein.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Schritt 15: Eine Projektaufgabe umbenennen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Projektaufgabe umbenennen** um.
5. Wählen Sie im Feld **Aktionsname** **msdyn\_PssUpdateV1** aus.
6. Im **Entität**-Feld geben Sie die folgenden Parameterinformationen ein.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Im Feld **OperationSetId** geben Sie **msdyn\_CreateOperationSetV1Response** im Dialogfeld **Dynamischer Inhalt** ein.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Schritt 16: Einen Optionssatz ausführen

1. Wählen Sie im Flow **Neuer Schritt**.
2. Geben Sie im Dialogfeld **Vorgang auswählen** im Suchfeld **ungebundene Aktion ausführen** ein. Wählen Sie dann auf der **Aktionen**-Registerkarte die Operation in der Ergebnisliste aus.
3. In dem Schritt wählen Sie die Ellipse (**...**) und dann **Umbenennen** aus.
4. Benennen Sie den Schritt in **Operationsset ausführen** um.
5. Wählen Sie im Feld **Aktionsname** **msdyn\_ExecuteOperationSetV1** aus.
6. Im Feld **OperationSetId** geben Sie **msdyn\_CreateOperationSetV1Response OperationSetId** im Dialogfeld **Dynamischer Inhalt** ein.

## <a name="references"></a>Referenzen

- [Übersicht über die Integration von Flows mit Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Verwenden von Projektplanungs-APIs zur Durchführung von Vorgängen mit Entitäten der Zeitplanung](schedule-api-preview.md)
- [Übersicht der Cloud-Flows - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Übersicht der lösungsfähigen Flows - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
