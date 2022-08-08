---
title: Projekt-Zeittabelle mobile Anwendung
description: Dieser Artikel enthält Informationen über die mobile Anwendung Microsoft Dynamics 365 Project Timesheet. Mit der mobilen App Project Timesheet können Benutzer Arbeitszeittabellen für Projekte auf ihrem Mobilgerät einreichen und genehmigen.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110974"
---
# <a name="project-timesheet-mobile-application"></a>Projekt-Zeittabelle mobile Anwendung

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Überblick

Mit der mobilen App Microsoft Dynamics 365 Project Timesheet können Benutzer Arbeitszeittabellen für Projekte auf ihrem Mobilgerät einreichen und genehmigen (iPhone oder Android). Diese mobile App wird in der Arbeitszeitnachweis-Funktion in der Projektverwaltung und im Buchungskreis von Dynamics 365 Finance angezeigt Es hilft bei der Verbesserung der Benutzerproduktivität und -Effizienz und ermöglicht rechtzeitige Eingabe und Genehmigung von Projektzeittabellen.

## <a name="download-and-install-the-mobile-app"></a>Die mobile App herunterladen und installieren

Laden Sie Microsoft Dynamics 365 Project Timesheet mobile App für Android oder iPhone aus dem Mobile Store für Ihr Gerät herunter und installieren sie diese.

## <a name="enable-the-app"></a>Aktivieren Sie die App 

In Finance muss die mobile App Project Timesheet aktiviert sein. Um die Funktionalität zu aktivieren, gehen Sie zu **Projektmanagement- und Buchhaltungsparameter \> Arbeitszeittabelle** und wählen Sie die Parameter **Aktivieren von Microsoft Dynamics 365 Project Timesheet** .

### <a name="resolve-sign-in-issues"></a>Beheben von Anmeldeproblemen

**Ausgabe:** Während der Anmeldung bei der Project Timesheet Mobile-App erhalten Benutzer eine Fehlermeldung, die besagt, dass sie „nicht auf die Anwendung '2bc50526-cdc3-4e36-a970-c284c34cbd6e' in diesem Mandanten zugreifen können.

**Problem:** Während der Anmeldung bei der mobilen App Project Timesheet erhalten Benutzer eine Fehlermeldung, die einem der folgenden Beispiele ähnelt:

- "AADSTS50020: Benutzerkonto '[Benutzername]' vom Identitätsanbieter 'https://sts.windows.net/ [App-ID]“ existiert nicht im Mandanten „[Mandanten-ID]“ und kann nicht auf die Anwendung „[App-ID]“ in diesem Mandanten zugreifen.“
- „Das ausgewählte Benutzerkonto ist im Mandanten '[tenant id]' nicht vorhanden“ und kann nicht auf die Anwendung '[app id]' in diesem Mandanten zugreifen“

**Erläuterung:** Diese Probleme werden durch eine Änderung verursacht, die im May 2022 an Azure Active Directory (Azure AD) vorgenommen und bezieht sich auf externe Nutzer. Da diese Änderung nicht an Finanz- und Betriebs-Apps vorgenommen wurde, kann sie Kunden auf jeder Version der Plattform oder Anwendung betreffen.

**Fix:** Alle externen Benutzer müssen über Azure AD für den Mandanten eingeladen worden sein. Weitere Informationen finden Sie unter [Einladen von Benutzern mit Azure Active Directory B2B Collaboration ](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Bei der App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.

2.  Geben Sie Ihre Finance URL ein.

3.  Wenn Sie sich zum ersten Mal anmelden, werden Sie dazu aufgefordert, Ihren Benutzernamen und Ihr Passwort einzugeben. Geben Sie Ihre Anmeldeinformationen ein.

4. Sie werden bei Ihrer Standardfirma angemeldet.

## <a name="submit-a-project-timesheet"></a>Senden Sie eine Projektzeittabelle

Sie können eine Projektzeittabelle in der App erstellen und senden. Sie können eine neue Arbeitszeittabelle auf Informationen aus einer früheren Arbeitszeittabelle, gespeicherten Zeilen oder Projektzuweisungen basieren. Wenn Sie als Stellvertretung festgelegt sind, können Sie auch eine Arbeitszeittabelle für einen anderen Mitarbeiter eingeben. Um eine Arbeitszeittabelle als Stellvertretung zu erstellen, wählen Sie die Schaltfläche **Menü** aus und bestimmen einen Ressourcennamen.

Auf der Seite mit der Arbeitszeittabelle wird basierend auf dem aktuellen Datum eine neue Arbeitszeittabelle für den Arbeitszeittabellenzeitraum erstellt. Die Arbeitswoche wird angezeigt. Wenn der Arbeitszeittabellenzeitraum mehrere Wochen umfasst, können Sie auf den Registerkarten Arbeitswoche eine andere Arbeitswoche auswählen.
Wenn für das aktuelle Datum eine Arbeitszeittabelle vorhanden ist, wird diese angezeigt. Wenn Sie eine neue Arbeitszeittabelle in einem anderen Arbeitszeittabellenzeitraum erstellen müssen, wählen Sie die Schaltfläche **Menü** und wählen Sie dann **Neue Arbeitszeittabelle**.

Sie können Projektinformationen eingeben, indem Sie auf die Aktion **Zeit hinzufügen** oder die Aktion **Zeit kopieren von** klicken. Die Aktion **Zeit kopieren von** kopiert die Projektzeileninformationen, jedoch nicht die Stunden. Das Menü **Zeit kopieren von** umfasst die folgenden Optionen:

- **Von vorhandener Arbeitszeittabelle kopieren** – Kopieren Sie Arbeitszeittabellenzeilen aus einer vorhandenen Arbeitszeittabelle.

- **Vom Favoriten kopieren** – Erstellen Sie neue Arbeitszeittabellenzeilen mithilfe der Arbeitszeittabelleneinstellungen, die Sie als Favoriten ausgewählt haben.

- **Vom Arbeitsauftrag kopieren** – Erstellen Sie neue Arbeitszeittabellenzeilen aus zugewiesenen Projekten.

Die angezeigten Projektinformationen hängen von den mobilen Parametern ab, die Sie auf der Website definiert haben auf der Seite **Projektmanagement- und Buchhaltungsparameter**.

In dem Feld **Juristische Person** wählen Sie die juristische Person aus, für die Sie die Projektarbeit ausgeführt haben. Das Feld **Juristische Person** ist nur verfügbar, wenn für Ihre juristische Person die Unterstützung für konzerninterne Arbeitszeittabellen aktiviert wurde.

Wählen Sie den Kunden aus, der dem Projekt für die Arbeitszeittabelle zugeordnet ist. Für die Erstveröffentlichung auf Android wird die Eingabe durch den Kunden nicht unterstützt, da Sie zuerst das Projekt auswählen müssen. Wenn Sie das Projekt zuerst ausgewählt haben, wird das Feld **Kunde** automatisch ausgefüllt.

In dem Feld **Projekt** wählen Sie das Projekt aus, für das Sie die Zeit eingeben. Das Feld **Kunde** wird automatisch ausgefüllt.

Die Kunden- und Projektsuche ermöglicht die Suche über Kunden und Projekte hinweg.

Wählen Sie Informationen in den Feldern **Kategorie**, **Aktivität**, **Zeilen-Eigenschaft**, **Umsatzsteuergruppe** und **Artikel-Umsatzsteuergruppe** nach Bedarf. Diese Felder können überschrieben werden.

Das Feld **Zeilen-Eigenschaft** wird basierend auf den Projektmanagement- und Buchhaltungsparametern auf einen Standardwert gesetzt. Wenn die Parameter Projekt/Kategorie und Kategorie/Ressource aktiviert sind, wird der Wert **Zeilen-Eigenschaft** auf den Standardwert gesetzt, den Sie für diese Validierung definiert haben. Wenn die Projekt-/Kategorie- und Kategorie-/Ressourcenparameter nicht aktiviert sind, wird der Wert **Zeilen-Eigenschaft** standardmäßig gemäß dem Feld **Aktivieren Sie die Standardzeileneigenschaft** auf der Seite **Projektmanagement- und Buchhaltungsparameter** dargestellt. Der Wert **Zeilen-Eigenschaft** kann überschrieben werden.

Wählen Sie einen Tag aus, um die Zeit hinzuzufügen. Geben Sie die Anzahl der Stunden ein, die Sie jeden Tag gearbeitet haben.

Um Kommentare zu den von Ihnen eingegebenen Stunden hinzuzufügen, klicken Sie auf **Kommentare hinzufügen** und geben Sie dann Kommentare für ein internes Publikum, ein Kunden-Publikum oder beides ein.
Interne Kommentare können von Projektmanagern eingesehen werden. Kundenkommentare sind auf Rechnungen enthalten.

Um die Zeile als Favorit zu speichern, aktivieren Sie das Kontrollkästchen und klicken Sie dann auf **Als Favorit speichern**.

Finanzielle Dimension und Unterstützung für Anhänge werden in der mobilen Anwendung nicht bereitgestellt.

Fügen Sie nach Bedarf weitere Projektzeilen hinzu, um Ihre Arbeitszeittabelle zu vervollständigen.

Klicken Sie auf **übermitteln**, um die Arbeitszeittabelle an den Genehmigungsworkflow zu senden.

## <a name="review-timesheets"></a>Arbeitszeittabellen überprüfen

Eine Liste der Arbeitszeittabellen, die überprüft werden müssen, ist im Menü verfügbar. Diese Option ist nur verfügbar, wenn Sie als die den Workflow genehmigende Person festgelegt wurden. Sowohl die Header- als auch die Zeilengenehmigung werden unterstützt. Die Genehmigung auf Zeilenebene bietet die Möglichkeit, eine oder mehrere Zeilen zur Genehmigung zu markieren. Klicken Sie nach dem Überprüfen der Arbeitszeittabelleninformationen auf **Genehmigen**, **Delegieren**, oder **Rückgabe**, um den Workflow fortzusetzen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
