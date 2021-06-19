---
title: Ein Projektteam erstellen
description: Dieses Thema bietet Informationen zum Erstellen und Verwalten von Projektteams.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006195"
---
# <a name="create-a-project-team"></a>Ein Projektteam erstellen

[!include [banner](../includes/banner.md)]

Um die Rollen zu verwenden, die zuvor in einem Projekt eingerichtet wurden, muss ein Projektmanager die Rollen dem Projekt zuordnen. Für ein Projekt können mehrere Rollen zugewiesen werden. Um Verwirrung zu vermeiden, werden diese Rollen während der Reservierung automatisch gekennzeichnet. Wenn der Projektmanager beispielsweise drei Softwareentwickler und drei Softwareentwicklerrollen benötigt wie **Softwareentwickler 1**, **Softwareentwickler 2** und **Softwareentwickler 3**, werden ihre Beschriftungen automatisch generiert werden. Wenn zuvor Rollenmerkmale für die Rolle festgelegt wurden, werden sie bei der Suche nach einer Ressource als Filter angewendet. Bei Bedarf können zusätzliche Merkmale hinzugefügt werden, um die Suche weiter zu verfeinern.

Die Ansichtseinstellungen können auch angepasst werden, um eine bessere Ansicht der Ressourcenverfügbarkeit zu erhalten. Es gibt Optionen zur Anzeige der stündlichen, täglichen, wöchentlichen, monatlichen, vierteljährlichen und jährlichen Verfügbarkeit. Es besteht auch die Option, die verfügbare und verbleibende Kapazität der Ressourcen anzuzeigen. Diese Option ist nützlich für die Zeitverwaltung, wenn Sie die verfügbare Zeit für Aktivitäten oder die Verfügbarkeit von Ressourcen schätzen.

Der Projektmanager kann eine Rolle auf der Seite auswählen und dann, wenn eine Ressource verfügbar ist, die der Anforderung entspricht, eine Ressource reservieren, um die Rolle zu füllen. Beachten Sie, dass die Ressourcen zu diesem Zeitpunkt in der Planungsphase nicht reserviert werden müssen. Wenn Sie einen PSP erstellen, können Sie Rollen durch besetzte Ressourcen für das Projekt ersetzen. Wenn Rollen im PSP durch besetzte Ressourcen ersetzt werden, aktualisiert das Ressourcen-Setup automatisch die Liste und Planung des Projektteams.

[![Projektteamliste, die sowohl Rollen als auch tatsächliche Ressourcen enthält](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Der Projektmanager hat verschiedene Möglichkeiten, eine Ressource für ein Projekt zu buchen, wie **Verbleibende Kapazität**, **Volle Kapazität**, **Kapazitätsprozentsatz**, und **Stunden definieren**. Diese Buchungsoptionen können jederzeit storniert werden, wenn sich die Ressourcenzuweisungen ändern. Es werden zwei Buchungsarten unterstützt:

- **Verbindlich buchen** – Die Ressourcenreservierung wurde genehmigt und bestätigt, um für die angegebene Dauer an dem Auftrag zu arbeiten.
- **Unverbindlich buchen** – Die Ressourcenreservierung wurde genehmigt und bestätigt, um für die angegebene Dauer an dem Auftrag zu arbeiten.

Der folgende Prozess erläutert, wie Sie ein Projektteam erstellen.

## <a name="create-a-project-team"></a>Ein Projektteam erstellen

1. Auf der **Alle Projekte** Listenseite, wählen Sie ein Projekt aus und wählen Sie dann **Bearbeiten**.
2. Auf der Registerkarte **Projektteam und Zeitplan** im Feld **Planen Sie das Enddatum** geben Sie im Feld das Startdatum des Zeitplans plus einen Monat ein. Wenn das Startdatum des Zeitplans beispielsweise der 24. Juni 2017 (24.06.2017) ist, geben Sie Folgendes ein **24/07/2017**.
3. Wählen Sie **Hinzufügen**.
4. In dem Bereich **Fügen Sie dem Projekt Rollen hinzu** geben Sie im Feld **Rolle** ein und wählen **Senior Projektmanager**.
5. Wählen Sie **Erforderliche Kompetenzen**.
6. Auf der Seite **Wählen Sie Eigenschaften** werden die Merkmale, die Sie zuvor für den Senior-Projektmanager festgelegt haben, standardmäßig die Merkmale ausgewählt, die Sie zuvor für die Rolle des Senior-Projektmanagers festgelegt haben. Klicken Sie auf **OK**.
7. Auf der Seite **Fügen Sie dem Projekt Rollen hinzu** im Feld **Anzahl der Ressourcen** geben Sie **1** ein.
8. In dem Feld **Ressource** zeigt die Suche alle Ressourcen, die die erforderlichen Kompetenzen haben. Wählen Sie **Daniel Goldschmidt** und dann **erstellen** aus.
9. Auf der Seite **Projekt** wählen Sie **Hinzufügen** aus.
10. In dem Bereich **Fügen Sie dem Projekt Rollen hinzu** und wählen Sie im Feld **Rolle** **Teammitglied** aus. Geben Sie **5** im Feld **Anzahl der Ressourcen** ein.
11. Wählen Sie **Erstellen** aus.
12. Auf der Seite **Projekte** wählen Sie **Ressource erfüllen**.

## <a name="monitor-project-teams"></a>Projektteams überwachen
1. Auf der Seite **Alle Projekte** wählen Sie die Verknüpfung **Projekt-ID** für das Projekt **XYZ Aktualisierung Phase 2**.
2. Auf der Registerkarte **Projektteam und Terminplanung** überprüfen Sie, ob die aufgelisteten Projektressourcen korrekt sind.


[!INCLUDE[footer-include](../includes/footer-banner.md)]