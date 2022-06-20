---
title: Problembehandlung für die Arbeit im Aufgabenraster
description: Dieser Artikel enthält Informationen zur Problembehandlung bei der Arbeit im Raster für Aufgaben.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911043"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problembehandlung für die Arbeit im Aufgabenraster 


_**Gilt für:** Die Basisbereitstellung ist für die Szenarien Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen und Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung verfügbar, Project for the web_

Das Aufgabenraster, das von Dynamics 365 Project Operations genutzt wird, ist ein gehosteter iframe innerhalb von Microsoft Dataverse. Aufgrund dieser Verwendung müssen bestimmte Anforderungen erfüllt werden, um sicherzustellen, dass Authentifizierung und Autorisierung korrekt funktionieren. Dieser Artikel beschreibt die allgemeinen Probleme, die das Rendern des Rasters oder die Verwaltung von Aufgaben im Projektstrukturplan (PSP) beeinträchtigen können.

Häufige Probleme umfassen:

- Die Registerkarte **Aufgabe** im Aufgabenraster ist leer.
- Beim Öffnen des Projekts wird das Projekt nicht geladen und die Benutzeroberfläche (UI) bleibt auf dem Spinner hängen.
- Rechteverwaltung für **Project for the Web**.
- Änderungen werden nicht gespeichert, wenn Sie eine Aufgabe erstellen, aktualisieren oder löschen.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Die Registerkarte „Aufgabe“ ist leer

### <a name="mitigation-1-enable-cookies"></a>Risikominderung 1: Cookies aktivieren

Project Operations erfordert, dass Drittanbieter-Cookies aktiviert sind, um den Projektstrukturplan zu rendern. Wenn Cookies von Drittanbietern nicht aktiviert sind, wird anstelle von Aufgaben eine leere Seite angezeigt, wenn Sie die Registerkarte **Aufgaben** auf der Seite **Projekt** auswählen.

Für Microsoft Edge oder Google Chrome Browser beschreiben die folgenden Verfahren, wie Sie Ihre Browsereinstellungen aktualisieren, um Cookies von Drittanbietern zu aktivieren.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Öffnen Sie Ihren Edge Browser.
2. Wählen Sie in der oberen rechten Ecke die **Auslassungspunkte** (...) aus, und wählen Sie dann **Einstellungen** aus.
3. Unter **Cookies und Standort-Berechtigungen**, wählen Sie **Cookies und Standort-Daten**.
4. Deaktivieren Sie **Blockieren Sie Cookies von Drittanbietern**.
5. Aktualisieren Sie Ihren Browser. 

#### <a name="google-chrome"></a>Google Chrome

1. Öffnen Sie Ihren Chrome Browser.
2. Wählen Sie in der oberen rechten Ecke die drei vertikalen Punkte und wählen Sie dann **Einstellungen** aus.
3. Unter **Datenschutz und Sicherheit** wählen Sie **Cookies und andere Standort-Daten**.
4. Wählen Sie **Alle Cookies zulassen** aus.
5. Aktualisieren Sie Ihren Browser. 

> [!NOTE]
> Wenn Sie Cookies von Drittanbietern blockieren, werden alle Cookies und Standort-Daten von anderen Standorten blockiert, auch wenn der Standort in Ihrer Ausnahmeliste zulässig ist.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Risikominderung 2: Überprüfen Sie, ob die PEX Endpunkt richtig konfiguriert wurde

Für Project Operations muss ein Projektparameter auf PEX Endpunkt verweisen. Dieses Endpunkt ist erforderlich, um mit dem Dienst zu kommunizieren, der zum Rendern des Projektstrukturplans verwendet wird. Wenn der Parameter nicht aktiviert ist, wird die Fehlermeldung der Projektparameter ist ungültig angezeigt. Führen Sie die folgenden Schritte aus, um den PEX Endpunkt zu aktualisieren.

1. Ergänzen Sie das Feld **PEX Endpunkt** auf der Seite **Projektparameter**.
2. Identifizieren Sie den Produkttyp, den Sie verwenden. Dieser Wert wird verwendet, wenn der PEX-Endpunkt gesetzt ist. Beim Abruf ist der Produkttyp bereits im PEX Endpunkt definiert. Behalten Sie diesen Wert bei.
3. Aktualisieren Sie das Feld mit dem folgenden Wert: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Die folgende Tabelle enthält den Typparameter, der basierend auf dem Produkttyp verwendet werden sollte.

      | **Produkttyp**                     | **Typenparameter** |
      |--------------------------------------|--------------------|
      | Project for the Web der Standardorganisation   | Typ=0             |
      | Project for the Web der benannten CDS-Organisation | Typ=1             |
      | Project Operations                   | Typ=2             |

4. Entfernen Sie das Feld aus der Seite **Projektparameter**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Risikominderung 3: Melden Sie sich bei project.microsoft.com an
Öffnen Sie eine neue Registerkarte in Ihrem Microsoft Edge-Browser, gehen Sie zu project.microsoft.com und melden Sie sich mit der Benutzerrolle an, die Sie für den Zugriff auf Project Operations verwenden.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Das Projekt wird nicht geladen und die Benutzeroberfläche bleibt im Spinner hängen

Zum Zwecke der Authentifizierung müssen Pop-ups aktiviert sein, damit das Aufgabenraster geladen wird. Wenn Popups nicht aktiviert sind, bleibt der Bildschirm auf dem Ladespinner hängen. Die folgende Grafik zeigt die URL mit einem blockierten Popup-Label in der Adressleiste, was dazu führt, dass der Spinner beim Versuch, die Seite zu laden, hängen bleibt. 

   ![Stecken Spinner und Pop-up-Block.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Risikominderung 1: Pop-ups aktivieren

Wenn Ihr Projekt im Spinner hängen bleibt, ist es möglich, dass Pop-ups nicht aktiviert sind.

#### <a name="microsoft-edge"></a>Microsoft Edge

Es gibt zwei Möglichkeiten, Pop-ups in Ihrem Edge-Browser zu aktivieren.

1. Wählen Sie in Ihrem Edge-Browser die Benachrichtigung oben rechts im Browser aus.
2. Wählen Sie **Popups und Weiterleitungen von imm er erlauben** die spezifische Dataverse-Umgebung.
 
     ![Pop-ups blockiertes Fenster.](media/enablepopups.png)

Alternativ können Sie die folgenden Schritte ausführen.

1. Öffnen Sie Ihren Edge Browser.
2. Wählen Sie in der oberen rechten Ecke die **Ellipse** (...) und wählen Sie dann **Einstellungen** > **Site-Berechtigungen** > **Pop-ups und Weiterleitungen**.
3. Deaktivieren Sie **Pop-ups und Weiterleitungen**, um Pop-ups zu blockieren, oder aktivieren Sie, um Pop-ups auf Ihrem Gerät zuzulassen.
4. Aktualisieren Sie Ihren Browser, nachdem Sie Pop-ups aktiviert haben. 

#### <a name="google-chrome"></a>Google Chrome
1. Öffnen Sie Ihren Chrome Browser.
2. Navigieren Sie zu einer Seite, auf der Pop-ups blockiert sind.
3. Wählen Sie in der Adressleiste **Pop-Up blockiert**.
4. Wählen Sie den Link für das Pop-up aus, das Sie sehen möchten.
5. Aktualisieren Sie Ihren Browser, nachdem Sie Pop-ups aktiviert haben. 

> [!NOTE]
> Um immer Pop-ups für die Website anzuzeigen, wählen Sie **Pop-ups und Weiterleitungen von [Site] immer zulassen** und dann **Fertig**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Rechteverwaltung für Project for the Web

Project Operations ist auf einen externen Planungsservice angewiesen. Der Dienst erfordert, dass einem Benutzer mehrere Rollen zugewiesen sind, die es ihm ermöglichen, Entitäten im Zusammenhang mit dem PSP zu lesen und zu schreiben. Diese Entitäten umfassen Projektaufgaben, Ressourcenzuweisungen und Aufgabenabhängigkeiten. Wenn ein Benutzer den PSP nicht rendern kann, wenn er zur Registerkarte **Aufgaben** navigiert, liegt es wahrscheinlich daran, dass **Projekt** für **Project Operations** nicht aktiviert wurde. Ein Benutzer erhält möglicherweise entweder einen Sicherheitsrollen-Fehler oder einen Fehler im Zusammenhang mit einer Zugriffsverweigerung.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Risikominderung1: Überprüfen Sie die Sicherheitsrollen des Anwendungsbenutzers und des Endbenutzers

1. Gehen Sie zu **Einstellung** > **Sicherheit** > **Benutzer** > **Anwendungsbenutzer**.  

   ![Anwendungsleser.](media/applicationuser.jpg)
   
2. Doppelklicken Sie auf den Anwendungsbenutzerdatensatz, um Folgendes zu überprüfen:

     - Der Benutzer verfügt über Zugriff auf das Projekt. Sie können dies tun, indem Sie überprüfen, ob der Benutzer über die Sicherheitsrolle **Projektmanager** verfügt.
     - Der Benutzer der Microsoft Project-Anwendung ist vorhanden und korrekt konfiguriert.
 
3. Wenn dieser Benutzer nicht vorhanden ist, erstellen Sie einen neuen Benutzerdatensatz. 
4. Wählen Sie **Neue Benutzer**, ändern Sie das Eingabeformular zu **Anwendungsbenutzer**, und fügen Sie dann die **Anwendungs-ID** hinzu.

   ![Anwendungsbenutzer-Details.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Änderungen werden nicht gespeichert, wenn Sie eine Aufgabe erstellen, aktualisieren oder löschen

Wenn Sie eine oder mehrere Aktualisierungen am PSP vornehmen, schlagen die Änderungen fehl und werden nicht gespeichert. Im Zeitplanraster tritt ein Fehler mit der Meldung „Die von Ihnen vorgenommene letzte Änderung konnte nicht gespeichert werden“ auf.

### <a name="mitigation-1-validate-the-license-assignment"></a>Risikominderung 1: Überprüfen Sie die Lizenzzuweisung

1. Stellen Sie sicher, dass dem Benutzer die richtige Lizenz zugewiesen wurde und dass der Dienst in den Serviceplandetails der Lizenz aktiviert ist.  
2. Stellen Sie sicher, dass der Benutzer **project.microsoft.com** öffnen kann.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Risikominderung 2: Validierungskonfiguration des Projektanwendungsbenutzers
1. Überprüfen, dass der Projekt-Anwendungbenutzer erstellt worden ist.
2. Wenden Sie die folgenden Sicherheitsrollen auf den Benutzer an:
  
  - Dataverse Benutzer oder Basisbenutzer
  - Project Operations-System
  - Projektsystem
  - Systeme mit dualem Schreiben für Project Operations. Diese Rolle ist erforderlich für Project Operations für Szenario basierend auf vorrätigen/nicht-vorrätigen Ressourcen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
