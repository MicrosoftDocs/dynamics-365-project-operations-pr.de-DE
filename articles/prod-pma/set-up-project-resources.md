---
title: Projektressourcen einrichten
description: Dieses Thema enthält Informationen zum Einrichten oder Anfordern von Projektressourcen.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9c8e4373da50999a0cc57f4eab672a98e7cf21edcfa5a5589d87691603a777de
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995715"
---
# <a name="set-up-project-resources"></a>Projektressourcen einrichten

[!include [banner](../includes/banner.md)]

Sie müssen einen Kalender einrichten und ihn einem Mitarbeiter oder einem Mitarbeiter zuordnen. Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen zu planen, die für das Projekt reserviert sind. Während der Kalendereinrichtung können Projektmanager im Rahmen der Ressourcenoptimierung eine Ressourcenebene erstellen. Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen festgelegt werden. Sie können einen Kalender auf der Seite **Kalender** einrichten.

Wenn Sie einen Mitarbeiter als Projektressource einrichten, können Sie aus Mitarbeitern auswählen, die in dem Unternehmen arbeiten, für das Sie Ressourcen einrichten. Alternativ können Sie Arbeiter aus anderen Unternehmen für Ihre Organisation auswählen. Diese Mitarbeiter werden als konzerninterne Ressourcen bezeichnet.

In den folgenden Verfahren wird erläutert, wie Sie einen Worker als Projektressource in Ihrem Unternehmen einrichten und eine konzerninterne Projektressource einrichten.

## <a name="set-up-a-worker-as-a-project-resource"></a>Richten Sie einen Worker als Projektressource ein

1. Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, den Sie als Projektressource hinzufügen, und öffnen Sie den Worker-Datensatz.
2. Wählen Sie im Aktionsbereich **Projekt** &gt; **Einrichtung** &gt; **Projekt einrichten**.
3. Wählen Sie einen Kalender aus, und schließen Sie die Seite.

Sie können auch Standardprojekte für eine Ressource als eine Art Vorzuweisung angeben. Vorabzuweisungen können verwendet werden, wenn der Ressourcenmanager oder Projektmanager im Voraus weiß, an welchen Projekten die Ressource arbeiten wird. Vorabzuweisungen können auch auf Anfrage eines Projektsponsors oder Kunden erfolgen. Um ein Projekt vorab zuzuweisen, klicken Sie auf die Seite **Projekte zuweisen** auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** und wählen Sie das entsprechende Projekt.

## <a name="set-up-an-intercompany-resource"></a>Richten Sie eine Intercompany-Ressource ein

Wenn Sie einen Mitarbeiter als konzerninterne Ressource einrichten, müssen Sie die Einrichtung sowohl im Kreditunternehmen als auch im Kreditunternehmen abschließen.

### <a name="in-the-lending-company"></a>In der Kreditgesellschaft

1. Vergewissern Sie sich unter Finanzen, dass das Kreditunternehmen ausgewählt ist, und führen Sie dann den Vorgang im vorherigen Abschnitt Einrichten eines Arbeitnehmers als Projektressource aus.
2. Klicken Sie auf der Seite **Intercompany-Buchhaltung** auf **Neu**.
3. In dem Feld **ID der juristischen Person** wählen Sie das kreditgebende Unternehmen aus. Füllen Sie die verbleibenden Felder aus, und klicken Sie dann auf **Speichern**.
4. Wählen Sie auf der Seite **Übertragungspreis** die Option **Neu** aus.
5. In dem Feld **Kreditgebende juristische Person** wählen Sie das entsprechende Unternehmen aus.
6. Um dem Kreditnehmer nur die Ressource zu verleihen, die Sie am Anfang dieses Abschnitts erstellt haben, wählen Sie im Feld **Ressource** den Namen der Ressource aus, die Sie erstellt haben. Um alle Ressourcen des kreditgebenden Unternehmens dem Kreditunternehmen zur Verfügung zu stellen, lassen Sie das Feld **Ressource** leer.
7. Auf der Seite **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Intercompany** legen Sie Option **Aktivieren Sie die unternehmensübergreifende Ressourcenplanung und Arbeitszeittabellen** auf **Ja** fest.

### <a name="in-the-borrowing-company"></a>Im Kreditunternehmen

- Auf der Seite **Ressourcenliste** geben Sie im Suchfilter auf der Seite den Namen der Ressource ein, die Sie für das kreditgebende Unternehmen erstellt haben, um zu überprüfen, ob der Name in der Ressourcenliste des kreditgebenden Unternehmens enthalten ist.

## <a name="request-project-resources"></a>Projektressourcen anfordern
Mit der Funktionalität für die Planung von Projektressourcen können Ressourcenmanager nur besetzte Ressourcen auf Aufträge oder Projekte verteilen. Um diese Funktionalität zu aktivieren, führen Sie die folgenden Aufgaben aus oder überprüfen Sie, ob sie abgeschlossen wurden:

- Nummernserien einrichten.
- Projektmanagement- und Buchhaltungsworkflows einrichten.
- Aktivieren Sie Workflows für Ressourcenanforderungen.

Nachdem die vorhergehenden Aufgaben abgeschlossen wurden, können Sie die folgenden Aufgaben nach Bedarf ausführen:

- Erstellen Sie eine Ressourcenanforderung aus einer mit Personal gebuchten Ressource.
- Ressourcenanforderungen überwachen.
- Erfüllen von Ressourcenanforderungen.
- Fordern Sie eine besetzte Ressource von einem PSP an.
- Buchen Sie Ressourcen für ein Projekt, ohne eine Personalressource anzufordern.


[!INCLUDE[footer-include](../includes/footer-banner.md)]