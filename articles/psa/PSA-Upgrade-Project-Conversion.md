---
title: Funktionsänderungen für Project Service Automation auf Project Operations
description: Dieser Artikel gibt einen Überblick über die Änderungen der Funktionen für Microsoft Dynamics 365 Project Service Automation auf Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621241"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Funktionsänderungen für Project Service Automation auf Project Operations

Nachdem ein Projekt erfolgreich von Microsoft Dynamics 365 Project Service Automation 3.X auf Dynamics 365 Project Operations Lite aktualisiert wurde, ist die Bearbeitung von Projektaufgaben im Projektstrukturplan (PSP) des Aufgabenrasters nicht möglich. Kunden können die PSPs im Verfolgungsraster überprüfen, wo neue Felder hinzugefügt wurden, um alle Details bereitzustellen, die sich auf die Aufgabe beziehen. Für Projekte, bei denen Änderungen am PSP erforderlich sind, können Sie berechtigte Projekte selektiv in das neue „Project for the Web“-Planungsumgebung konvertieren.

## <a name="project-conversion-process"></a>Projektkonvertierungsprozess

Führen Sie diese Schritte aus, um ein Projekt zu konvertieren.

1. Öffnen Sie die Hauptseite des Projekts und wählen Sie im Aktionsbereich **Konvertieren** aus.
1. Wählen Sie im angezeigten Bestätigungsmeldungsfeld **OK**, um mit der Projektkonvertierung zu beginnen. Die folgenden Aktionen treten auf:

    1. Eine Meldungsleiste, die auf der Hauptseite des Projekts angezeigt wird, besagt: „Der Projektzeitplan wird konvertiert. Sie können das Projekt erst ändern, wenn die Konvertierung abgeschlossen ist.“
    1. Sie werden zur Projektliste weitergeleitet.

    Nachdem die Projektkonvertierung abgeschlossen ist, werden die folgenden Aktionen ausgeführt:

    1. Der zugewiesene Projektmanager erhält eine Benachrichtigung auf der rechten Seite der Anwendung.
    1. Die Meldungsleiste, die besagt, dass die Konvertierung ausgeführt wird, wird entfernt.
    1. Die Registerkarte **Zeitplan** zeigt die neue Planungsumgebung mit „Project for the Web“. Jeder Benutzer mit den entsprechenden Lizenzen und Sicherheitsrollen kann den PSP bearbeiten.
    1. Das Feld **Planungsmodul** wird auf **Project for the Web** aktualisiert.
    1. Die Schaltfläche **Konvertieren** wird aus dem Aktionsbereich entfernt.

> [!IMPORTANT]
> Die Massenkonvertierung von Projekten ist nicht zulässig. Jeder Versuch, eine große Anzahl von Projekten gleichzeitig zu aktualisieren, wird gedrosselt. Diese Einschränkung trägt dazu bei, eine hohe Leistung für alle Kunden sicherzustellen.

## <a name="manual-tasks-vs-automatic-tasks"></a>Manuelle Aufgaben vs. automatische Aufgaben

Wenn eine Umgebung von Project Service Automation auf Project Operations aktualisiert wird, gelten alle Aufgaben im PSP als automatisch geplant. Das Konzept manuell geplanter Aufgaben ist in Project for the Web nicht verfügbar. Sie können jedoch das bevorzugte Planungsverhalten für Ihre Projekte definieren, indem Sie die Einstellungen des [Planungsmodus](/project-management/scheduling-modes.md) verwenden, wenn Sie neue Projekte erstellen.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Eingeschränkter Betrieb für Projekte vor der Konvertierung

In diesem Abschnitt werden die funktionalen Unterschiede beschrieben, mit denen Sie rechnen müssen, wenn Projekte nicht konvertiert wurden.

### <a name="copy-project"></a>Projekt kopieren

Der Vorgang **Kopieren** wird nur für konvertierte Projekte unterstützt. Aktualisierte Projekte können vor der Konvertierung nicht kopiert werden.

### <a name="move-project"></a>Projekt verschieben

Eine Änderung des Startdatums eines Projekts verschiebt den Beginn der Aufgaben nicht proportional, es sei denn, das Projekt wurde konvertiert.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Welche Unterschiede gibt es zwischen konvertierten Projekten und neuen Projekten, die nach Abschluss des Upgrades erstellt werden?

Für Projekte, die konvertiert werden, nachdem die Umgebung aktualisiert wurde, wird ein Kennzeichen gesetzt, das den Zeitplan anweist, nur den Projektkalender zu berücksichtigen. Dieses Verhalten entspricht dem Verhalten in Project Service Automation. Das Kennzeichen wird jedoch nicht für neue Projekte gesetzt, die nach dem Upgrade erstellt werden. Daher berücksichtigt der Zeitplan die Arbeitszeiten von Ressourcen, wenn sie einer Aufgabe zugewiesen werden.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Was sollte ich tun, wenn die Konvertierung meines Projekts fehlschlägt?

Wenn Ihr Projekt nicht konvertiert werden kann, überprüfen Sie zuerst die Fehlerprotokolle, um allgemeine Probleme im Zusammenhang mit Ihrem PSP zu identifizieren. Wenn die Protokolle keinen bestimmten Fehler anzeigen, für den Sie Maßnahmen ergreifen können, wenden Sie sich an den Kundensupport, damit Ihr Fall weiter überprüft werden kann.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Wie werden Betriebsferien in Project for the Web gehandhabt?

Project for the Web berücksichtigt keine Betriebsferien, die das Unternehmen auf Organisationsebene festlegt. Es werden jedoch andere Arten von arbeitsfreien Tagen berücksichtigt, die in einer bestimmten Arbeitszeitvorlage definiert sind.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Welche Einschränkungen hat Project for the Web?

Siehe [Erstellen eines Projektstrukturplans: Projekteinschränkungen](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Muss ich mit Änderungen meiner Kosten- und Umsatzschätzungen rechnen?

In seltenen Fällen, in denen Ressourcenzuweisungsprofile neu berechnet werden oder auf eine andere Datumsgrenze als das Quellprojekt fallen, sehen Sie möglicherweise Unterschiede in den Umsatz- und Kostenschätzungen. Von den Kunden wird erwartet, dass sie im Rahmen des Upgrade-Prozesses eine repräsentative Stichprobe von Projekten testen, damit sie mögliche Änderungen des Zeitplans nachvollziehen können.
