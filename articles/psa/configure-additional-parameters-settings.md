---
title: Konfigurieren von zusätzlichen Parametereinstellungen
description: Konfigurieren Sie zusätzliche Parametereinstellungen (Project Service)
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0ceaa3af630df132339895a8497e49daf2e102c3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592323"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfigurieren Sie zusätzliche Parametereinstellungen (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sobald Sie die Elemente in den vorherigen Themen konfiguriert haben, müssen Sie zusätzliche Projektparameter festlegen, die für die Projekte benötigt werden. Bei der Installation des [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] haben Sie eine Parametereinstellungen für die erste Erstellung aller für den [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erforderlichen Datensätze erstellt. Jetzt ist es Zeit zurückzukehren und zusätzliche Felder für diese Parametereinstellung zu konfigurieren.  
  
 Sie müssen die folgenden Einstellungen konfiguriert haben:  
  
-   Organisationseinheit:  
  
-   Rechnungshäufigkeit  
  
-   Arbeitszeitvorlage  
  
-   Preisliste  
 
In diesem Schritt geben Sie an, welche der Ressourcenzuordnung Sie wünschen:  
  
- **Zentral**. Nur Ressourcen-Manager können Ressourcen zu Projekten zuordnen.  
  
- **Hybrid**. Ressourcen-Manager, Projektmanager und Account Manager können und den Projekten Ressourcen zuordnen.  
  
 
Um die Projektparameter festzulegen:  
  
1. Gehen Sie zu **Project Service > Parameter**.  
  
2. Klicken Sie auf die Sie die Parameter, die Sie konfigurieren möchten (die, die sie bei der ersten Installation des [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] erstellt haben), oder klicken Sie auf **Neu**, um eine neue Datenbank zu erstellen.  
  
3. Legen Sie im Bereich **Allgemein** alle Optionen für die Projektparameter fest.  
  
4. Klicken Sie im Bereich **Preisliste** auf **+**, um einer Preisliste hinzuzufügen, wählen Sie eine Preisliste in der Dropdownliste **Projekt-Parameter-Preisliste** aus, und klicken Sie dann auf **Speichern**.  
  
5. Klicken Sie auf die Schaltfläche **Speichern** in der unteren rechten Ecke des Bildschirms.  

> [!NOTE]
> Der Projektparametersatz muss gepflegt sein, damit Project Service ordnungsgemäß funktioniert. Dieser Datensatz sollte nicht gelöscht werden.

### <a name="see-also"></a>Siehe auch  
 [Ressourcen einrichten](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
