---
title: Neues Projekt erstellen
description: Dieses Thema bietet Informationen zum Erstellen eines neuen Projekts.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270722"
---
# <a name="create-a-new-project"></a>Neues Projekt erstellen

[!include [banner](../includes/banner.md)]

Führen Sie folgende Schritte aus, um ein neues Projekt zu erstellen.

1. Auf der Seite **Projektverwaltung** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:

    - **Projekttyp:** Zeit und Material
    - **Projektname:** XYZ-Upgrade-Phase 2
    - **Projektgruppe** TM\_WIP
    - **Projektvertrags-ID** 00000002

2. Wählen Sie **Projekt erstellen** aus.

## <a name="assign-a-resource-to-a-project"></a>Eine Ressource einem Projekt zuweisen

1. Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, für den Sie zuvor Kompetenzen eingerichtet haben und öffnen Sie den Worker-Datensatz.
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Projekt** in der Gruppe **Einrichten** die Option **Projekt zuweisen** aus.
3. Auf der Seite **Projektzuweisungen für die Ressourcenvalidierung** auf der Registerkarte **Projekte** im Feld **Fügen Sie das Projekt ausgewählten Projekten hinzu** Filter auf das Projekt **XYZ-Upgrade-Phase 2**.
4. In dem Bereich **Verbleibende Projekte** wählen Sie ein Projekt aus und klicken Sie dann auf die Pfeilschaltfläche, um es dem Bereich **Ausgewählte Projekte** hinzuzufügen.

Sie können nach Bedarf auch Kategorien für eine Ressource zuweisen. Der Kategorietyp ist entweder **Kosten** oder **Umsatz**. Der Kategorietyp wird von Ihrer Organisation festgelegt. Wenn für eine Ressource keine Kategorien zugewiesen sind, sucht Finance die Standardkategorie für Stundenpreise nach Kosten und Einnahmen.

## <a name="set-up-project-resource-and-role-characteristics"></a>Richten Sie Projektressourcen- und Rollenmerkmale ein

Ein Projektmanager kann die Projektresssourcen-Funktion verwenden, um die für das Projekt erforderlichen Rollen zu erstellen. Rollen können verwendet werden, wenn bestätigte Ressourcen noch unbekannt sind, wenn Ressourcen reserviert werden. Rollen können vorübergehend als geplante Ressourcen reserviert werden, sodass Sie die Projektplanungsphase fortsetzen können.

[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Szenario:** Contoso wurde beauftragt, ein Zeit- und Materialprojekt mit einer genehmigten Projektcharta abzuschließen. Der Junior-Projektmanager schließt den Projektumfang noch ab. Der Ressourcenmanager identifiziert derzeit bestimmte Ressourcen, die für die Arbeit an dem neuen Projekt reserviert werden. Aufgrund der kritischen Natur des Projekts forderte der Projektsponsor den Senior-Projektmanager als eine der Rollen an. Der Ressourcenmanager muss die neue Ressource erwerben und die Rolle im System definieren, falls der Junior-Projektmanager die Ressourceninformationen während der Projektplanung benötigt.

Die folgenden Schritte zeigen, wie der Ressourcenmanager die Rolle des Senior-Projektmanagers einrichten und ihr Ressourcenmerkmale zuordnen kann. Später kann die Rolle verwendet werden, um nach verfügbaren Ressourcen zu suchen, die den erforderlichen Ressourcenkompetenzen entsprechen.

1. Auf der Seite **Rollen einrichten** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:

    - **Rollen-ID:** Senior Projektmanager
    - **Beschreibung:** Senior Projektmanager

2. Wählen Sie **Erstellen** aus.
3. Wählen Sie die Rolle **Senior Projektmanager** aus und wählen Sie dann **Eigenschaften konfigurieren**.
4. In dem Feld **Eigenschaftentyp** wählen Sie **Fertigkeit**.
5. In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld die Fertigkeit ein, nach der gesucht werden soll.
6. In dem Feld **Eigenschaftentyp** wählen Sie **Zertifikat**.
7. In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld den Zertifikatstyp ein, nach dem gesucht werden soll.

## <a name="assign-a-project-resource-to-a-project"></a>Eine Projektressource einem Projekt zuweisen

1. Auf der Seite **Alle Projekte** wählen Sie das Projekt **XYZ-Upgrade-Phase 2** aus.
2. Auf der Registerkarte **Projektteam und Terminplanung** wählen Sie **Hinzufügen** aus.
3. In dem Feld **Rolle** wählen Sie **Teammitglied**.
4. Wählen Sie **Aus Kalender buchen** aus.
5. Auf der Seite **Verfügbarkeit von Ressourcen** wählen Sie **Einstellungen anzeigen**.
6. Auf der Seite **Passen Sie die Einstellungen an** geben Sie die folgenden Werte ein:

    - **Format für die Datumsbereichsansicht:** Tag
    - **Verfügbarkeitsbeschreibungen anzeigen:** Ja
    - **Restkapazität anzeigen:** Ja

7. Wählen Sie eine Ressource in der Liste der buchbaren Ressourcen aus.
8. Wählen Sie **Hartes Buch** und **Volle Kapazität** aus.

## <a name="assign-a-resource-to-a-default-role"></a>Zuweisen einer Ressource einer Standardrolle

Um Projekt- oder Ressourcenmanagern zu helfen, können Sie Drilldown zu den Ressourcen ausführen, die für ein Projekt reserviert werden können. Sie können einer vorhandenen Ressource oder einer neu erworbenen Ressource einer Standardrolle zuordnen. Als Daniel zum Beispiel eingestellt wurde, verfügte er über die Erfahrung und die Fähigkeiten, um die Rolle des Business Analyst zu übernehmen. Der Ressourcenmanager hat diese Rolle als Daniels Standardrolle zugewiesen. Aus diesem Grund hat der Ressourcenmanager Daniel zu einem Pool von Geschäftsanalysten hinzugefügt, die für die Arbeit an Projekten zur Verfügung stehen.

Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die für die Arbeit an Projekten verfügbar sind. Sie können diese Informationen als ein Kriterium verwenden, wenn sie während der Ressourcenerfüllung eine Entscheidungsanalyse mit mehreren Kriterien durchführen. Sie können dem Filter auch andere Ressourcenmerkmale hinzufügen, um nach Ressourcen zu suchen, die über bestimmte Fähigkeiten, Ausbildung und Erfahrung für ein bestimmtes Projekt verfügen.

**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Rolle des Senior-Projektmanagers wurde während der Projektplanungsphase als geplante Ressource reserviert. Der Ressourcenmanager hat jetzt eine Ressource erworben, um die Rolle des Senior-Projektmanagers zu erfüllen.

1. Auf der Seite **Ressourcenliste** wählen Sie **Daniel Goldschmidt**.
2. Auf der Seite **Rollenressourcen** wählen Sie **Neu** und geben die folgenden Werte ein:

    - **Wirksam:** Geben Sie das aktuelle Datum ein.
    - **Ablauf:** Geben Sie **Nie** ein.
    - **Rolle:** Geben Sie **Senior Project Manager** ein.

3. Wählen Sie **Speichern** aus, und schließen Sie die Seite.
4. Auf der Registerkarte **Kompetenzen** fügen Sie die Fertigkeit **ProjectMgmt** und **PMP** Zertifikat hinzu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]