---
title: Installation der Beispieldaten
description: In diesem Thema finden Sie Informationen zum Installieren von Beispieldaten in Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132422"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installation von Beispieldaten für die Project Service-Anwendung

Um Ihre eigenen Demoumgebungen zu erstellen, bietet Microsoft herunterladbare Beispieldatenpakete, die die Funktionen Ihrer Apps zeigen. Es gibt zwei Typen von Beispiel-Datenapketen:
- Referenz/Daten einrichten
- Demodaten (Verweis/einrichten und transaktionale Daten wie Arbeitsaufträge Projekte)

Die Beispieldaten **Referenz** Paketeikönnen in drei unterschiedlichen Paketen heruntergeladen werden, sodass Sie Daten nur für Project Service oder nur für Field Service installieren können. Alternativ können Sie Beispieldaten für beide Anwendungen gleichzeitig installieren.

Die Beispiel-Referenz-/Einrichtungs-Datenpakete sind:

- [**V902PSMasterData** – nur Project Service-Version 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – nur Field Service-Version 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – Field Service 8.x und Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Das letzten **Demo** Datenpaket ist.

 - [**FPSDemoData** - Field Service 8.x und Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Installationsanweisungen variieren leicht in den Abschnitten, um Benutzer zu erstellen und zu konfigurieren, der Bereich ist identisch mit der vorherigen [**Blog-Nachricht**](https://aka.ms/fpsdemodatablog). Diese PaketFunktionen reduziertes diesen Demodatebsatz und braucht ungefähr 3 Stunden zum Installieren.

Diese Beispieldatenpakete sind nur in englischer Sprache verfügbar.

> [!IMPORTANT]
> **Es ist nicht möglich, Beispieldaten zu deinstallieren.** Sie sollten diese Pakete nur auf Demonstrations-, Auswertungs-, Schulungs- oder Prüfsystemen installieren. Beachten Sie auch, dass das Installieren eines einzelnen Pakets und die anschließende Installation des anderen einzelnen Pakets nicht unterstützt wird. (Das bedeutet, Sie können nicht zuerst **FSMasterData** und dann **PSMasterData** installieren oder umgekehrt.) Wenn Sie in Zukunft Beispieldaten für beide Anwendungen benötigen, sollten Sie das Paket **v902FPSMasterData** installieren.

Wenn Sie Beispieldatenpakete installieren, werden im Rahmen des Installationsprozesses folgende Aktionen ausgeführt:

- Es werden Standardparameter für die Verwendung von Project Service, Field Service oder beide Anwendungen erstellt oder festgelegt (sofern zutreffend).

- Es werden Beispieldaten für die Anwendungen importiert, wie buchbare Ressourcen, anwendungsspezifische Rollen, Vertriebs- und Einstandspreislisten, Organisationseinheiten, Vertriebsprozessdatensätze und andere Entitäten, um die Schlüsselfunktionen zu veranschaulichen.  

Mit dem **Demodaten** - Paket erhalten Sie die obigen und zusätzlichen transaktionalen Daten wie Arbeitsaufträge und Projekte.

Sie fragen sich, welche Funktionen Sie mit den Beispieldaten demonstrieren können? Sehen Sie sich das fiktive Szenario von Fabrikam Robotics an unten unter [Technischen Hinweisen](#technical-notes).

Wenn Sie Fragen zum Installieren der Beispieldatenpakete haben, [senden Sie uns eine E-Mail an fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com)

## <a name="requirements"></a>Anforderungen

Das Installationsprotokoll geht für Ihre Zielinstanz (Organisation) von Folgendem aus:

- Ausgangssprache ist English und die Basiswährung ist US-Dollar (USD, $).

- Die Organisation hat noch keine Project Service oder Field Service-Daten oder nur Barebone-Standarddaten, die bei jeder neuen Organisation vorhanden sind.

- Die richtige Version einer Geschäftsanwendung ist bereits installiert:
       
    - **Für v902FPSMasterData:** Die Organisation hat die Field Service-Version 8.x und die Project Service-Version 3.x installiert.

    - **Für v902PSMasterData:** Die Organisation hat die Project Service-Version 3.x installiert.

    - **Für v902FSMasterData:** Die Organisation hat die Field Service-Version 8.x installiert.

> [!NOTE]
> Wenn Sie die Beispieldaten zusätzlich zu einer vorhandenen Project Service- und Field Service-Testversion oder -Demoumgebung installieren möchten, die bereits über Daten verfügt (nicht empfohlen), müssen Sie die durch das Installationsprogramm durchgeführten Sicherheitsvorkontrollen ausschalten. Weitere Informationen finden Sie unten in den technischen Hinweisen.

## <a name="prepare-for-installation"></a>Vorbereitung für die Installation

Sie müssen das Installationsprogramm auf einem Computer mit einer aktuellen Version von Windows (Windows 10 bevorzugt) ausführen.

Sie sollten einplanen, dass der Computer mit einem Netzwerk verknüpft bleibt, und dass die Installation bis zu **1 Stunde** lang ausgeführt wird für **Daten einrichten/referenzieren**. (Die erstmalige Installation dauert 30 Minuten für **FPSMasterData**, und enthält Beispieldaten für beide Anwendungen). Für **FPSDemoData** dauert die Installation rund **3 Stunden**.

Bei dem Computer muss die Bildschirmschonerfunktion deaktiviert sein. Andernfalls gehen die Sitzungsanmeldeinformationen für die Installation möglicherweise verloren, wenn der Bildschirmschoner aktiviert wird (es sei denn, Sie sorgen währenddessen dafür, dass die Sitzung aktiv bleibt).

> [!div class="mx-imgBorder"]
> ![Screenshot der Bildschirmschonereinstellungen bei deaktiviertem Bildschirmschoner](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Herunterladen und entpacken

Das Installationsprogramm für die Project Service- und Field Service-Beispieldaten wird als selbstextrahierende ausführbare Datei vertrieben. Die Dateinamen können je nach Beispieldatenpaket unterschiedlich ausfallen, ansonsten sind die Schritte aber gleich, unabhängig davon, welches Paket Sie installieren.

Nachdem Sie ein Paket heruntergeladen haben, führen Sie die .exe-Datei aus und akzeptieren Sie dann die Nutzungsbedingungen, um die komprimierte ZIP-Datei zu entpacken. Sie müssen anschließend die Inhalte dieser Datei in einen Ordner auf dem Computer extrahieren.

Je nach Betriebssystem und Sicherheitseinstellungen müssen Sie unter Umständen folgende Schritte ausführen, nachdem Sie die ZIP-Datei entpackt haben:

1. Suchen Sie die Datei **FPSDemoData.dll** im Ordner **v902FPSMasterData**  / und klicken Sie mit der rechten Maustaste auf **PackageDeployer_FPSDemoData**.

2. Wählen Sie **Sperre aufheben** aus.

3. Wählen Sie **Übernehmen** aus.

4. Wählen Sie **OK** aus.


## <a name="create-or-configure-users"></a>Erstellen oder Konfigurieren von Benutzern

Das Paket **FPSDemoData** erfordert sechs Benutzer, während **FPSMasterData** Pakete einen Benutzer erfordert. Gehen Sie zum richtigen Beispieldatenpaket.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Erstellen oder Konfigurieren Sie Benutzer - Stammdatenpakete Referenz/Einrichtung

Das Paket **FPSMasterData** ist so konzipiert, dass es mit einem Benutzer names Bernhard Anhalter mit den hier beschriebenen Einstellungen installiert wird. Um das Paket ordnungsgemäß zu installieren, müssen Sie Benutzer in Ihrer Umgebung erstellen (oder dort vorübergehend umbenennen), damit sie der eingehenden Beispieldatenkonfiguration entsprechen.

Um Benutzer zu erstellen oder zu konfigurieren, wechseln Sie zu **Einstellungen** > **Sicherheit** > **Benutzer** und gehen Sie dann folgendermaßen vor:

1. Legen Sie UserFullname=„Bernhard Anhalter” mit dem Benutzernamen „bernharda” (**Kleinschreibung**) für die Projektmanager- und Practice Manager-Rollen fest.

2. Wählen Sie den Benutzer **Bernhard Anhalter** und anschließend **Rollen verwalten** aus. Suchen Sie nach der Rolle **Systemadministrator** und wählen Sie aus. Wählen Sie anschließend **OK** aus, Bernhard Anhalter die vollständigen Administratorrechte zu erteilen. Dieser Schritt ist erforderlich, um sicherzustellen, dass Beispieldatensätze mit den korrekten Benutzerbesitzrechten erstellt werden, und somit Ansichten korrekt ausgefüllt werden.

3. Im heruntergeladenen Paket müssen Sie eine Datenzuordnungsdatei mit E-Mail-Adressen des Standardbenutzerkontexts aktualisieren. Dazu öffnen Sie **PkgFolder** und suchen nach der Datei **ImportUserMapFile.xml** in Notepad (oder Visual Studio oder einem anderen XML-Editor) und öffnen sie dort. Legen Sie das Feld **DefaultUserToMapTo=** für die E-Mail-Adresse des Benutzers Bernhard Anhalter fest.

4. Wenn Sie Bernhard Anhalter nicht mit dem Benutzernamen **bernharda** verwenden, müssen Sie eine weitere Datei aktualisieren. Öffnen Sie die Datei **DemoDataPreImportConfig.xml** und suchen Sie dann nach dem Tag **userstocreateandconfigure**. Aktualisieren Sie das **\<login\>**-Tag mit dem Benutzernamen des Benutzers Bernhard Anhalter. Weitere Details finden Sie unten in den [Technischen Hinweisen](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Erstellen oder Konfigurieren Sie Benutzer - Demodatenenpaket

Das Demodatenenpaket erfordert sechs Benutzer. Damit das Paket richtig eingerichtet wird, gehen Sie folgendermaßen vor:

 1. Stellen Sie oder benennen Sie vorübergehend vorhandenen Benutzer, um eingehende Beispieldatenkonfiguration anzupassen, indem Sie zur Seite **Einstellungen**  > **Sicherheit** > **Benutzer** gehen.
 
    Diese Rollen werden nur für Persona-basierte Demos benötigt.  
    - Benutzer vollständiger Name= „Johannes Meyer-Hartfeld” als Field Service Mechaniker   
    - Benutzer vollständiger Name= „Kai Larenz” als Customer Service & Field Service Dispatcher   
    - Benutzer vollständiger Name = „Ulla Graf” als Clark Kundenbetreuer   
    - Benutzer vollständiger Name = „Karl Gäller” als Practice und Project Manager  
    - Benutzer vollständige Name= „Leonie Simon” als Teammitglied   
    - Benutzer vollständiger Name = „Bernhard Koch”
  
2. Der Zweck des Demodatenimports ist es, die sechs Benutzer zur Administratorrolle zuzuweisen, um Beispieldatensätze ordnungsgemäß zu importieren. 

3. Öffnen Sie **PkgFolder** und dann suchen und öffnen Sie **ImportUserMapFile.xml**. Aktualisieren der Felder **Neu=** zu den E-Mail-Adressen von entsprechenden Benutzern im System.

   > [!div class="mx-imgBorder"]
   > ![Screenshot von UserMapFile](media/sample-data-7.png)

4. Wenn „Karl Gäller” Benutzer vollständiger Name eine andere Benutzer-ID hat als  **„karlg"**, müssen Sie eine weitere Datei aktualisieren. Öffnen Sie die Datei **DemoDataPreImportConfig.xml** und suchen Sie dann nach dem Tag **userstocreateandconfigure**. Aktualisieren Sie das **\<login\>**-Tag mit dem loginId (Groß-/Kleinschreibung beachtet). 

5. Der erste Kalender des Benutzers (im **userstocreateandconfigure**-Tag) wird verwendet, um die Arbeitszeiten für alle buchbaren Rssourcen für den Import von Demodaten aufzufüllen. Navigieren Sie zu **Einstellungen**  > **Sicherheit**  > **Benutzer** und succhen Sie Benutzer „Karl Gäller” und öffnen Sie die Option „Arbeitszeit”. Bearbeiten Sie die vorhandenen Arbeitszeiten und die Option **Gesamter wöchentlicher Serienzeitplan vom Beginn bis zum Ende**. Stellen Sie unter **Arbeitszeiten werden auf 8 - 5 Uhr morgens (9 Stunden), Montag bis Freitag und Stunden mit der Zeitzone festgelegt auf Pacific Time (USA und Kanada)** sicher. Dies ist erforderlich, um sicherzustellen, dass die Projekt- und Zeitplanübersicht wie erwartet dargestellt wird.

**Empfehlung:** Sie sollten jetzt eine Sicherung für Ihre Organisation vornehmen, falls Sie während der Installation der Beispieldaten wieder alles zurücksetzen müssen, wenn etwas schiefgehen sollte. Weitere Informationen finden Sie unter [Sicherung und Wiederherstellung von Instanzen](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Führen Sie den Package Deployer aus.

1. Suchen Sie nach **PackageDeployer.exe** im Ordner **v902FPSMasterData** oder **PackageDeployer_FPSDemoData**.

2. Akzeptieren Sie die Nutzungsbedingungen.

3. Im nächsten Fenster:

   a. Bereitstellungstyp **Office 365** auswählen.

   b. Verwenden Sie den Benutzer und das Kennwort des Systemadministratorbenutzers, der unter „Benutzer erstellen oder konfigurieren” („Bernhard Anhalter” mit dem Benutzernamen „bernharda”) konfiguriert wurde.

   c. Stellen Sie sicher, dass **Liste der verfügbaren Organisationen anzeigen** ausgewählt ist.

      > [!div class="mx-imgBorder"]
      > ![Screenshot des Package Deployer-Fensters mit aktivierter Option „Liste der verfügbaren Organisationen anzeigen”](media/sample-data-2.png)

4. Wählen Sie die Organisation aus, in der Sie die Beispieldaten installieren möchten.

5. Wählen Sie **Weiter** aus, bis Sie das Dialogfeld **Demodateneinrichtung** sehen.

   > [!div class="mx-imgBorder"]
   > ![Screenshot des Fensters für den Demodaten-Installationsprogrammstatus](media/sample-data-3.png)

6. Beachten Sie, bevor Sie fortfahren, dass das Installieren der Beispieldaten bis zu eine Stunde (in der Regel ~10 Minuten) dauern kann. Sie müssen sicherstellen, dass der Computer während des Installationsprozesses eingeschaltet und mit einem Netzwerk verbunden bleibt, und dass Ihre Sitzung aktiv bleibt.   

7. Wenn Sie bereit sind, klicken Sie auf **Weiter**, um den Installationsvorgang für die Beispieldaten zu starten. Nachdem die Beispieldaten geladen sind, klicken Sie auf **Fertig stellen**.

## <a name="verify-the-sample-data-installation"></a>Überprüfen der Installation der Beispieldaten

Überprüfen Sie für die Plausibilitätsprüfung, ob die Anzahl der Datensätze und die Arten der Entitäten, die im fiktiven Szenario für Fabrikam Robotics angezeigt werden, wie erwartet erscheinen.

Nachdem die Beispieldaten vollständig geladen sind, melden Sie sich als Benutzer Bernhard Anhalter an und bestätigen Sie Folgendes:

- Wenn die Project Service-Anwendung installiert ist, gehen Sie zu **Project Service** > **Einstellungen** > **Preislisten**. Bestätigen Sie, dass die Rechnungs- und Kostensätze mit der entsprechenden Währung für jedes Land bzw. jede Region im Datensatz vorhanden sind.

- Wenn die Project Service-Anwendung installiert ist, gehen Sie zu **Universal Resource Scheduling** > **Einstellungen** > **Organisationseinheiten**. Überprüfen Sie, ob eine Einstandspreisliste mit der entsprechenden Währung jeder Organisationseinheit zugeordnet wurde (mit Ausnahme von Stadteinträgen). Sollten einige fehlen, suchen sie nach der richtigen Einstandspreisliste und weisen Sie diese zu.

- Wenn die Field Service-Anwendung installiert ist, gehen Sie zu **Project Service** > **Einstellungen** > **Preislisten**. Überprüfen Sie, ob die Rechnungs- und Kostensätze vorhanden sind. Gehen Sie zu **Field Service** > **Einstellungen** > **Preislisten** und prüfen Sie, ob die Rechnungs- und Kostensätze vorhanden sind und ob die entsprechende Währung für jedes Land bzw. jede Region im Datensatz zugeordnet ist.

  > [!div class="mx-imgBorder"]
  > ![Screenshot aktiver Preislisten](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Screenshot aktiver Organisationseinheiten](media/sample-data-5.png)

## <a name="technical-notes"></a>Technische Hinweise

Unten finden Sie weitere technische Informationen zu der Installation dieser Daten.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installation von Beispieldaten zusätzlich zu vorhandenen Daten (nicht empfohlen)

Wenn Sie die Beispieldaten zusätzlich zu einer vorhandenen Field Service- oder Project Service-Testversion oder -Demoumgebung installieren möchten, die bereits über Daten verfügt, müssen Sie die durch das Installationsprogramm durchgeführten Sicherheitsvorkontrollen ausschalten.

Gehen Sie dazu zum Ordner **PkgFolder**, um die Datei **DemoDataPreImportConfig.xml** in Notepad (oder einem anderen XML-Editor) zu finden und zu öffnen.

Suchen Sie den folgenden Wert und ändern Sie dann die Einstellung von „true” in „false”:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Diese Änderung sorgt dafür, dass das einige wichtige Sicherheitsprüfungen umgangen werden, darunter:

- Die Bestätigung, dass es nicht mehr als einen aktiven **Organisationseinheit**-Datensatz gibt, und die anschließende Umbenennung in **Fabrikam US**

- Die Bestätigung, dass es nicht mehr als einen aktiven **Arbeitsvorlage**-Datensatz gibt

- Die Bestätigung, dass es nicht mehr als einen aktiven **Projektparameter**-Datensatz gibt, und die anschließende Umbenennung dieses Eintrags in **Parameter**

### <a name="configuration-components"></a>Konfigurationskomponenten

Es gibt einige andere Konfigurationskomponenten in dieser Vorimport-Konfigurationsdatei. Davon enthalten einige Folgendes für technische Benutzer:

- **\<RequiredSolutions\>** gibt die erforderlichen Lösungsinstallationen und ihre Versionsnummern an.

- **\<InstallSampleData\>** legt fest, ob vorgegebene Beispieldaten für die Apps installiert sind.

    - false – überspringt die Installation dieser integrierten Daten (kann entfernt werden)

    - true – installiert die integrierten Daten gleichzeitig mit der Installation der FS- und PSA-Beispieldaten

- **\<PreImportDataCollection\>** gibt Datenzuordnungen von flachen Dateien und verknüpfte Datensätze an, die vor der Installation der Hauptbeispieldaten importiert werden.

- **\<EntitiesToEnableScheduling\>** gibt an, welche Entitäten für die Buchung in der Microsoft Dynamics Scheduling aktiviert werden sollen (alias Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** gibt buchbare Ressourcen an, die erstellt werden (sofern sie noch nicht vorhanden sind), bevor der Beispieldatenimport ausgeführt wird. Bitte beachten Sie, dass die buchbaren Ressourcen der Beispieldaten des Quellsystems mit den Datensätzen mit buchbaren Ressourcen des Zielsystems bei dem vollständigen Namen und dem Login jeder Ressource übereinstimmen. Es ist daher NICHT möglich, die Namen in dieser Vorkonfigurationsdatei zu ändern, es sei denn, Sie importieren die Beispieldaten zuerst in ein Zielsystem unter Verwendung dieser Namen und ändern dann die Namen der buchbaren Ressourcen sowie der aktivierten Benutzerdatensätze in die gewünschten Namen um. Anschließend exportieren Sie die Daten dann erneut für den Import in Ihr finales Zielsystem (alte und neue Einträge von **ImportUserMapFile.xml** müssen entsprechend aktualisiert werden).

- **\<PluginsToDisable\>** gibt ein einzelnes Positions-Plug-in an, das während des Beispieldatenimports deaktiviert und anschließend erneut aktiviert werden muss.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics – fiktives Szenario

Durch die Field Service- und Project Service-Beispielrefernzdatenpakete wird die **Lösung Fabrikam-Herstellungsmasterdaten (v3.0.0.0)** neben den ca. 4.000 Datensätzen und ca. 40 verschiedenen Einträgen installiert. Die separaten Beispieldatenpakete für Field Service oder Project Service enthalten eine Teilmenge der Beispieldaten **v902FPSMasterData** für diese Anwendung. Das Paket **Demo-Daten** installiert einen **Fabrikam Manufacturing Demo Daten-Lösung (v 3.0.0.7)** mit bis zu 22.000 Datensätze über 148 Entitäten.

Das fiktive Unternehmen Fabrikam Robotics ist ein Hersteller von elektronischen Gerätemontagelinien-Robotern und für seine Produktqualität, Innovation und soliden Kundenservice bekannt, u. a. bei der Installationsplanung, Implementierung und laufenden Wartungsservices. Fabrikam hat seinen Hauptsitz in den Vereinigten Staaten (Fabrikam USA) und verfügt über projektbasierte Serviceabläufe in Frankreich, Indien, im Vereinigten Königreich und der Schweiz.

Field Service Vorgänge werden in den Vereinigten Staaten, hauptsächlich im größeren Seattle-Bereich, zentriert. Das Unternehmen konzentriert sich auf die Nutzung der Internet der Dinge(IdD)-Konnektivität zur Überwachung der Kundenanlagenleistung und für die Bereitstellung von immer proaktiveren Services vor Ort.

Eine allgemeine Übersicht der Beispieldaten sieht wie folgt aus:

- Allgemeine Beispieldatenelemente (bei beiden Anwendungen enthalten)

    - 1 Benutzer

    - 71 Konten

    - 137 Kontakte

    - Verschiedene Transaktionstypen und -kategorien

    - 50 Produkte mit 1 Produktpreisliste

    - 14 Preis-/Kostenlisten

    - 31 Eigenschaften (Ressourcenfähigkeiten) bei 2 Bewertungsmodellen mit 3 Ebenen (Bewertungswerte)

- Project Service

    - 8 Organisationseinheiten

    - 6 rollenspezifische Nutzungsebenen

    - 2,8k+ Rollenpreisspezifikationen

- Field Service

    - 4 Gebiete

    - 5 Arbeitsauftragstypen

    - 22 Kundenanlagen

    - 9 Vorfalltypen mit einer Vielzahl von zugeordneten Ressourceneigenschaften (9), Services (13) und Service Aufgaben (13)
   
Das Paket **Demo-Daten** installiert ungefähr 179 Arbeitsaufträge, 12 Projekte zugeordnete transaktionale Daten. 

### <a name="change-the-work-hours-for-sample-resources"></a>Ändern der Arbeitszeit für Beispielressourcen

Standardmäßig haben alle buchbaren Ressourcen einen Standardkalender mit 24 Arbeitsstunden.

Wenn Sie die Arbeitszeit für buchbare Beispielressourcen ändern möchten, gehen Sie zu **Universal Resource Scheduling** > **Planung** > **Ressourcen**.

Wählen Sie einen Benutzer (beispielsweise Bernhard Anhalter) aus und ändern Sie die Arbeitszeiten für Bernhard Anhalter auf die Stunden, die Sie auf mehrere Benutzer anwenden möchten. Gehen Sie zu **Universal Resource Scheduling** > **Einstellungen** > **Arbeitszeitvorlagen** und ändern Sie den Datensatz **Standardarbeitsvorlage**. Wählen Sie im Feld **Vorlagenressource** einen Benutzer mit einer Arbeitszeit aus, die Sie auf andere Ressourcen anwenden möchten. Gehen Sie zu **Universal Resource Scheduling** > **Planung** > **Ressourcen** > **Aktive buchbare Ressourcen**. Wählen Sie die Ressourcen aus, die Sie ändern möchten, und wählen Sie dann **Kalender festlegen** aus. Wählen Sie in der Dropdownliste **Arbeitsvorlage** die Vorlage **Standardarbeitszeit** oder eine andere Vorlage mit der richtigen Vorlagenenressource aus. Wenn Sie die Zeitplanübersicht öffnen, sollten Sie sehen, dass die Ressourcen jetzt aktualisierte Arbeitszeiten haben.

> [!div class="mx-imgBorder"]
> ![Screenshot aktiver buchbaren Ressourcen](media/sample-data-6.png)
