---
title: Projekteinstellungen
description: Dieses Thema enthält Informationen zu den Einstellungen für das Projektmanagement.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123107"
---
# <a name="project-settings"></a>Projekteinstellungen

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Mithilfe der folgenden Einstellungen können Sie auf die Projektplanungsfunktionen zugreifen.

## <a name="work-template"></a>Arbeitsvorlage

Zur Erstellung eines Projektzeitplans erstellen Sie zuerst eine Projektkalendervorlage, in der die Anzahl der Arbeitsstunden pro Tag sowie etwaige Betriebsferien definiert werden. Zur Erstellung einer Projektkalendervorlage weisen Sie dem Feld **Kalendervorlage** eine Arbeitsvorlage für das Projekt zu. Führen Sie die folgenden Schritte aus, um eine Arbeitsvorlage zu erstellen.

1. Klicken Sie in PSA im linken Navigationsbereich auf **Ressourcen**. 
2. Öffnen Sie auf der Listenseite **Ressourcen** einen Benutzerdatensatz und wählen Sie dann **Arbeitsstunden anzeigen** aus.

  > [!NOTE]
  > Stellen Sie sicher, dass auf der Browserseite Popups zulässig sind. So können Sie die für die Ressource festgelegten Arbeitsstunden anzeigen.
  
3. Klicken Sie auf der Registerkarte **Monatliche Ansicht** auf **Einrichten**. Eine Liste mit drei Optionen wird angezeigt: 

  - Neuer wöchentlicher Zeitplan
  - Arbeitsplan für einen Tag
  - Arbeitsfreie Zeit

> ![Festlegen von Optionen](media/project-13.png)

4. Wählen Sie **Neuer wöchentlicher Zeitplan** aus und legen Sie anschließend die Optionen für den Ressourcenzeitplan fest. Sie können einen wöchentlichen Serienzeitplan, tägliche Stundenparameter, Betriebsferien und mehr festlegen.
5. Legen Sie den Datumsbereich fest, wählen Sie **Speichern** aus und klicken Sie dann auf **Schließen**. 
6. Kehren Sie zur Listenseite **Ressourcen** zurück und wählen Sie die Ressource aus, für die Sie die Arbeitsstunden festgelegt haben. 
7. Wählen Sie **Kalender festlegen als** aus, um die Arbeitsvorlage festzulegen. 
8. Geben Sie im Dialogfeld **Arbeitsvorlage** einen Namen für die Arbeitsvorlage ein und wählen Sie dann **Übernehmen** aus. 

Sie können die Arbeitsvorlage jetzt einer Projektkalendervorlage zuordnen.

## <a name="resource-roles"></a>Ressourcenrollen

Der Begriff *Ressourcenrolle* bezieht sich auf die Reihe von Fähigkeiten, Kompetenzen und Zertifizierungen, die eine Person haben muss, um eine bestimmte Gruppe von Aufgaben bei einem Projekt durchzuführen. PSA ermöglicht die Kalkulation und Abrechnung der Zeit einer Ressource basierend auf der Rolle, der die Ressource zugeordnet ist. Jede Organisation muss diese Rollen über den linken Navigationsbereich im Menü **Project Service** festlegen.

Jede Organisation muss diese Rollen auf der Seite **Aktive Ressourcenkategorien** festlegen. Wählen Sie im linken Navigationsbereich **Ressourcenrollen** aus, um diese Seite zu öffnen.

## <a name="price-lists"></a>Preislisten

Mithilfe von Preislisten können Sie Einkaufs- und Verkaufspreise für Ressourcenrollen, Ausgabenkategorien, Produkte und andere Elemente in einer Organisation festlegen. Bevor Sie finanzielle Vorkalkulationen für die im Rahmen eines Projekts zu leistende Arbeit erstellen, sollten Sie eine unterstützende Kosten- und Verkaufspreisliste erstellen. Im Parameterbereich sollten Sie außerdem eine standardmäßige Kosten- und Verkaufspreisliste festlegen, die für alle in der Organisation erstellten Projekte gilt. Achten Sie auf der Seite **Aktive Projektparameter** darauf, eine standardmäßige Kosten- und Verkaufspreisliste festzulegen.
