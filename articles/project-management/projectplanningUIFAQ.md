---
title: Problembehandlung für die Arbeit im Aufgabenraster
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die beim Arbeiten im Aufgabenraster erforderlich sind.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031536"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problembehandlung für die Arbeit im Aufgabenraster 

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit dem Kostenmanagement auftreten können.

## <a name="enable-cookies"></a>Aktivieren Sie Cookies

Für Project Operations müssen Cookies von Drittanbietern aktiviert sein, um den Projektstrukturplan zu rendern. Wenn Cookies von Drittanbietern nicht aktiviert sind, wird anstelle von Aufgaben eine leere Seite angezeigt, wenn Sie die Registerkarte **Aufgaben** auf der Seite **Projekt** auswählen.

![Leere Registerkarte, wenn Cookies von Drittanbietern nicht aktiviert sind](media/blankschedule.png)


### <a name="workaround"></a>Problemumgehung
Für Microsoft Edge oder Google Chrome Browser beschreiben die folgenden Verfahren, wie Sie Ihre Browsereinstellungen aktualisieren, um Cookies von Drittanbietern zu aktivieren.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Öffnen Sie Ihren Edge Browser.
2. Wählen Sie in der oberen rechten Ecke die **Auslassungspunkte** (...) aus, und wählen Sie dann **Einstellungen** aus.
3. Unter **Cookies und Standort-Berechtigungen**, wählen Sie **Cookies und Standort-Daten**.
4. Deaktivieren Sie **Blockieren Sie Cookies von Drittanbietern**.

#### <a name="google-chrome"></a>Google Chrome

1. Öffnen Sie Ihren Chrome Browser.
2. Wählen Sie in der oberen rechten Ecke die drei vertikalen Punkte und wählen Sie dann **Einstellungen** aus.
3. Unter **Datenschutz und Sicherheit** wählen Sie **Cookies und andere Standort-Daten**.
4. Wählen Sie **Alle Cookies zulassen** aus.

> [!IMPORTANT]
> Wenn Sie Cookies von Drittanbietern blockieren, werden alle Cookies und Standort-Daten von anderen Standorten blockiert, auch wenn der Standort in Ihrer Ausnahmeliste zulässig ist.

## <a name="pex-endpoint"></a>PEX-Endpunkt

Für Project Operations muss ein Projektparameter auf PEX Endpunkt verweisen. Dieser Endpunkt ist erforderlich, um mit dem Dienst zu kommunizieren, der zum Rendern des Projektstrukturplans verwendet wird. Wenn der Parameter nicht aktiviert ist, wird die Fehlermeldung der Projektparameter ist ungültig angezeigt. 

### <a name="workaround"></a>Problemumgehung
 ![PEX Endpunkt Feld im Projektparameter](media/projectparameter.png)

1. Ergänzen Sie das Feld **PEX Endpunkt** auf der Seite **Projektparameter**.
2. Aktualisieren Sie das Feld mit dem folgenden Wert: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Entfernen Sie das Feld aus der Seite **Projektparameter**.

## <a name="privileges-for-project-for-the-web"></a>Berechtigungen für Project für das Web

Project Operations ist auf einen externen Planungsservice angewiesen. Der Dienst erfordert, dass einem Benutzer mehrere Rollen zum Lesen und Schreiben in Entitäten zugewiesen sind, die sich auf die Projektstrukturplan beziehen. Diese Entitäten umfassen Projektaufgaben, Ressourcenzuweisungen und Aufgabenabhängigkeiten. Wenn ein Benutzer die Projektstrukturplan nicht rendern kann, wenn er zur Registerkarte **Aufgaben** geht,  liegt dies wahrscheinlich daran, dass Project for Project Operations nicht aktiviert wurde. Ein Benutzer erhält möglicherweise entweder einen Sicherheitsrollen-Fehler oder einen Fehler im Zusammenhang mit einer Zugriffsverweigerung.


## <a name="workaround"></a>Problemumgehung

1. Gehen Sie zu **Einstellung > Sicherheit > Benutzer > Anwendungsbenutzer**.  

   ![Anwendungsleser](media/applicationuser.jpg)
   
2. Doppelklicken Sie auf den Anwendungsbenutzerdatensatz, um Folgendes zu überprüfen:

 - Der Benutzer verfügt über Zugriff auf das Projekt. Diese Überprüfung erfolgt normalerweise, indem sichergestellt wird, dass der Benutzer über die Sicherheitsrolle **Projektmanager** verfügt.
 - Der Benutzer der Microsoft Project-Anwendung ist vorhanden und korrekt konfiguriert.
 
3. Wenn dieser Benutzer nicht vorhanden ist, können Sie einen neuen Benutzerdatensatz erstellen. Wählen Sie **Neuer Benutzer** aus. Ändern Sie das Anmeldeformular in **Anwendungsbenutzer** und fügen Sie dann die **Anwendungs-ID** hinzu.

   ![Anwendungsbenutzer-Details](media/applicationuserdetails.jpg)

4. Stellen Sie sicher, dass dem Benutzer die richtige Lizenz zugewiesen wurde und dass der Dienst in den Serviceplandetails der Lizenz aktiviert ist.
5. Stellen Sie sicher, dass der Benutzer project.microsoft.com öffnen kann.
6. Überprüfen Sie anhand der Projektparameter, ob das System auf den korrekten Projekt-Endpunkt verweist.
7. Überprüfen, dass der Projekt-Anwendungbenutzer erstellt wurde.
8. Wenden Sie die folgenden Sicherheitsrollen auf den Benutzer an:

  - Dataverse-Benutzer
  - Project Operations System
  - Projektsystem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Fehler beim Aktualisieren des Projektstrukturplans

Wenn eine oder mehrere Aktualisierungen am Projektstrukturplan vorgenommen werden, schlagen die Änderungen schließlich fehl und werden nicht gespeichert. Im Zeitplanraster tritt ein Fehler auf, der besagt, dass die zuletzt vorgenommenen Änderungen nicht gespeichert werden konnten.

### <a name="workaround"></a>Problemumgehung

1. Stellen Sie sicher, dass dem Benutzer die richtige Lizenz zugewiesen wurde und dass der Dienst in den Serviceplandetails der Lizenz aktiviert ist.
2. Stellen Sie sicher, dass der Benutzer project.microsoft.com öffnen kann.
3. Überprüfen Sie anhand der Projektparameter, ob das System auf den korrekten Projekt-Endpunkt verweist.
4. Überprüfen, dass der Projekt-Anwendungbenutzer erstellt worden ist.
5. Wenden Sie die folgenden Sicherheitsrollen auf den Benutzer an:
  
  - Dataverse Benutzer oder Basisbenutzer
  - Project Operations System
  - Projektsystem
  - System duales Schreiben für Project Operations (Diese Rolle ist erforderlich, wenn Sie das Szenario ressourcen/nicht vorrätig von Project Operations bereitstellen.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]