---
title: Microsoft Project Client-Integration
description: Das Planen und Verwalten eines Projektplans kann komplex sein. Daher müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe verwalten können. Die Integration mit Microsoft Project Client bietet Unterstützung beim Öffnen und Verwalten einer Projektstrukturplan.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076585"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client-Integration

[!include [banner](../includes/banner.md)]

Das Planen und Verwalten eines Projektplans kann komplex sein. Daher müssen Projektmanager Tools verwenden, mit denen sie diese Aufgabe verwalten können. Die Integration mit Microsoft Project Client bietet Unterstützung beim Öffnen und Verwalten einer Projektstrukturplan. Der Projektmanager kann alle Änderungen wieder im Dynamics 365 Finance Projektstrukturplan veröffentlichen.

> [!NOTE]
> Wenn Sie das Juli-Update (Version 10.0.4) verwenden, müssen Sie Wissensdatenbank 4054797 und 4055884 installieren.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurieren Sie das Microsoft Project Client-Add-In
So aktivieren Sie die Integration mit Microsoft Project Client: Ein Microsoft Dynamics 365 Add-In muss in der Microsoft Project Anwendung des Benutzers installiert sein. Dies erfolgt durch Öffnen des **Projektmanagement-Arbeitsbereichs**.

• Klicken Sie auf **Konfigurieren Sie das Projektclient-Add-In** aus dem Abschnitt **Verknüpfung** > **Einrichtung** des Arbeitsbereichs.

• Klicken Sie auf **Öffnen** und dann klicken Sie auf **Ausführen**, wenn Sie dazu aufgefordert werden.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Öffnen und bearbeiten Sie einen vorhandenen Entwurf einer Projektstrukturplanstruktur in Microsoft Project Client
Wenn ein Projekt in Dynamics 365 Finance bereits einen Projektstrukturplan hat, kann der Projektstrukturplan in der Microsoft Project Client-Anwendung geöffnet werden, wenn sich der Projektstrukturplan in einem Entwurfsstatus befindet. Zum Öffnen von der Seite **Projekt** klicken Sie auf die Verknüpfung **In Microsoft Project öffnen** aus der Registerkarte **Plan**. Diese Seite kann auch in der Microsoft Project Client-Anwendung durch Klicken  von **Öffnen** in der Registerkarte **Microsoft Dynamics 365** geöffnet werden. Wählen Sie die **Juristische Entität** und **Projekt** aus der Liste aus.

> [!NOTE]
> Wenn Sie den Internet Explorer als Ihren Browser verwenden, müssen Sie auf **speichern** klicken, um manuell von dem Speicherort zu öffnen, an den die Datei heruntergeladen wird. Oder klicken Sie auf **Speichern und öffnen**, um die Datei in Microsoft Project Client zu öffnen. Benennen Sie den Dateinamen beim Speichern nicht um.

Bevor Sie mit Microsoft Project Client Änderungen an der Datei vornehmen, müssen Sie diese auschecken. Klicken Sie auf **Auschecken** in der Registerkarte **Microsoft Dynamics 365**. Dadurch wird verhindert, dass andere Benutzer gleichzeitig die Projektstrukturplan innerhalb von Finance bearbeiten. Um den Projektstrukturplan nach Abschluss aller Änderungen zu veröffentlichen, klicken Sie auf **einchecken** auf der Registerkarte **Microsoft Dynamics 365**.

Wenn dem Projekt in Finance bereits ein Projektteam hinzugefügt wurde, wird die Ressourcenliste mit den Teammitgliedern gefüllt. Wenn dem Projekt noch kein Projektteam hinzugefügt wurde, können Sie Ressourcen auswählen und das Team in Microsoft Project Client erstellen, indem Sie auf die Schaltfläche **Ressourcen** auf der Registerkarte **Microsoft Dynamics 365** klicken. 

Die folgenden Daten werden im Rahmen des Check-in-Vorgangs wieder mit Finance synchronisiert:

• Aufgabenname

• Startdatum

• Fertigstellungsdatum

• Vorgänger

• Ressourcenname

• Kategorie

• Ressourcenkategorie

• Arbeitsstunden

• Hinweise

• Priorität

> [!NOTE]
> Wenn Sie Ihrer Microsoft Project Client Datei weitere Spalten hinzufügen, werden diese nicht in der Datei gespeichert und beim erneuten Öffnen der Datei nicht angezeigt.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstellen Sie den Projektstrukturplan für ein vorhandenes Projekt mit Microsoft Project Client
Um einen neuen Projektstrukturplan mithilfe von Microsoft Project Client zu erstellen, folgen Sie diesen Schritten:


1.  Öffnen Sie Microsoft Project Client.

2.  Auf der Registerkarte **Microsoft Dynamics 365** wählen Sie **Öffnen**.

3.  Wählen Sie die **Juristische Entität** für das Projekt.

4.  Wählen Sie das **Projekt** aus.

5.  Klicken Sie auf **Auschecken** auf der Registerkarte **Microsoft Dynamics 365**-

6.  Wenn Sie bereit sind, in Finance zu veröffentlichen, klicken Sie auf **Check-In** auf der Registerkarte **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Ersetzen Sie den bestehenden Projektstrukturplan für ein vorhandenes Projekt mit Microsoft Project Client
Gehen Sie folgendermaßen vor, um mit Microsoft Project Client einen neuen Projektstrukturplan zu erstellen und einen vorhandenen Projektstrukturplan für ein vorhandenes Projekt zu ersetzen:

1.  Öffnen Sie den Microsoft Project Client.

2.  Erstellen Sie den Zeitplan in Microsoft Project Client.

3.  Auf der Registerkarte **Microsoft Dynamics 365** klicken Sie auf **Änderungen speichern** > **Bestehendes Projekt ersetzen**.

4.  Wählen Sie die **Juristische Entität** für das Projekt.

5.  Wählen Sie das **Projekt** aus.

6.  Klicken Sie auf **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Erstellen Sie ein neues Projekt in Microsoft Project Client


1.  Öffnen Sie den Microsoft Project Client.

2.  Erstellen Sie den Zeitplan in Microsoft Project Client.

3.  Auf der Registerkarte **Microsoft Dynamics 365** klicken Sie auf **Änderungen speichern** > **In neuem Projekt speichern**.

4.  Wählen Sie die **Juristische Entität** für das Projekt.

5.  Geben Sie die **Projekt-ID** falls benötigt ein.

6.  Geben Sie den **Projektnamen** ein.

7.  Wählen Sie **Projekttyp**, **Projektgruppe** und die **Projektvertrags-ID** aus. Alternativ können Sie einen neuen Projektvertrag erstellen, indem Sie auf **Neu** klicken.

8.  Wählen Sie den **Kalender** aus, der für die Beschaffung verwendet werden soll.

11. Klicken Sie auf **OK**.
