---
title: Projekt-Zeittabelle mobile Anwendung
description: Diese Thema bietet Informationen über die Microsoft Dynamics 365 Project Timesheet mobile Anwendung. Mit der mobilen App Project Timesheet können Benutzer Arbeitszeittabellen für Projekte auf ihrem Mobilgerät einreichen und genehmigen.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: e2eb387f-5bb3-419c-953b-3bbc2f050059
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 6cd4629e9380fbe3d1839ba31a819c9057d1258c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716496"
---
# <a name="project-timesheet-mobile-application"></a>Projekt-Zeittabelle mobile Anwendung

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Überblick

Mit der mobilen App Microsoft Dynamics 365 Project Timesheet können Benutzer Arbeitszeittabellen für Projekte auf ihrem Mobilgerät einreichen und genehmigen (iPhone oder Android). Diese mobile App zeigt die Arbeitszeittabellenfunktionalität an, die sich im Bereich Projektmanagement und Buchhaltung von Dynamics 365 Finance verbindet, verbessert die Produktivität und Effizienz der Benutzer und ermöglicht die rechtzeitige Eingabe und Genehmigung von Projektzeitplänen.

## <a name="download-and-install-the-mobile-app"></a>Die mobile App herunterladen und installieren

Laden Sie Microsoft Dynamics 365 Project Timesheet mobile App für Android oder iPhone aus dem Mobile Store für Ihr Gerät herunter und installieren sie diese.

## <a name="enable-the-app"></a>Aktivieren Sie die App 

In Finance muss die mobile App Project Timesheet aktiviert sein. Um die Funktionalität zu aktivieren, gehen Sie zu **Projektmanagement- und Buchhaltungsparameter \> Arbeitszeittabelle** und wählen Sie die Parameter **Aktivieren von Microsoft Dynamics 365 Project Timesheet** .

## <a name="sign-in-to-the-app"></a>Bei der App anmelden

1.  Starten Sie die App auf Ihrem mobilen Gerät.

2.  Geben Sie Ihre Finance URL ein.

3.  Wenn Sie sich zum ersten Mal anmelden, werden Sie dazu aufgefordert, Ihren Benutzernamen und Ihr Passwort einzugeben. Geben Sie Ihre Anmeldeinformationen ein.

4.  Sie werden bei Ihrer Standardfirma angemeldet.

## <a name="submit-a-project-timesheet"></a>Senden Sie eine Projektzeittabelle

Sie können eine Projektzeittabelle in der App erstellen und senden. Sie können eine neue Arbeitszeittabelle auf Informationen aus einer früheren Arbeitszeittabelle, gespeicherten Zeilen oder Projektzuweisungen basieren. Wenn Sie als Delegierter festgelegt sind, können Sie auch eine Arbeitszeittabelle für einen anderen Mitarbeiter eingeben. Um eine Arbeitszeittabelle als Stellvertretung zu erstellen, wählen Sie die Schaltfläche **Menü** und wählen Sie einen Ressourcennamen aus.

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

Um Kommentare zu den von Ihnen eingegebenen Stunden hinzuzufügen, klicken Sie auf **Fügen Sie Kommentare hinzu** und geben Sie dann Kommentare für ein internes Publikum, ein Kunden-Publikum oder beides ein.
Interne Kommentare können von Projektmanagern eingesehen werden. Kundenkommentare sind auf Rechnungen enthalten.

Um die Zeile als Favorit zu speichern, aktivieren Sie das Kontrollkästchen und klicken Sie dann auf **Als Favorit speichern**.

Finanzielle Dimension und Unterstützung für Anhänge werden in der mobilen Anwendung nicht bereitgestellt.

Fügen Sie nach Bedarf weitere Projektzeilen hinzu, um Ihre Arbeitszeittabelle zu vervollständigen.

Klicken Sie auf **übermitteln**, um die Arbeitszeittabelle an den Genehmigungsworkflow zu senden.

## <a name="review-timesheets"></a>Arbeitszeittabellen überprüfen

Eine Liste der Arbeitszeittabellen, die überprüft werden müssen, ist im Menü verfügbar. Diese Option ist nur verfügbar, wenn Sie als die den Workflow genehmigende Person festgelegt wurden. Sowohl die Header- als auch die Zeilengenehmigung werden unterstützt. Die Genehmigung auf Zeilenebene bietet die Möglichkeit, eine oder mehrere Zeilen zur Genehmigung zu markieren. Klicken Sie nach dem Überprüfen der Arbeitszeittabelleninformationen auf **Genehmigen**, **Delegieren**, oder **Rückgabe**, um den Workflow fortzusetzen.
