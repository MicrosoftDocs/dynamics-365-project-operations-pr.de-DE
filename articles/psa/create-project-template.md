---
title: Eine Projektvorlage erstellen
description: Erstellen einer Projektvorlage (Project Service)
author: ruhercul
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
ms.openlocfilehash: 127b6e43a15f19a42791e78b55865ab11ca50c7a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598993"
---
# <a name="create-a-project-template-project-service"></a>Erstellen einer Projektvorlage (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektvorlagen sparen Zeit, wenn Ihr Unternehmen regelmäßig Gebote für ähnliche Typen von Projekten abgibt. Sie stellen einen Standardsatz von Rollen und geschätzten Stunden für einen Typ von Projekt bereit. Konto- und Projektmanager können auf Basis einer Projektvorlage Projekte erstellen, oder sie können die Vorlage kopieren und selbst eine erstellen.  
  
## <a name="components-of-project-template"></a>Komponenten der Projektvorlage
 Eine Projektvorlage besteht aus drei Komponenten:  
  
- **Projektstrukturplan**: Ein Projektstrukturplan hat in einer Projektvorlage denselben Satz von Elementen wie im Projekt. Sie können eine Aufgabenhierarchie erstellen, Rollen zu Aufgaben zuordnen, Zeitplanattribute definieren, Abhängigkeiten festlegen und alle Daten im Gantt-Diagramm anzeigen. Der Projektstrukturplan in den Projektvorlagen unterstützt auch Aufgabenmodi für die Aufgaben. Es gibt keinen Unterschied zwischen einer Projektvorlage und einem Projekt beim Erstellen eines Arbeitszeitplans.  
  
- **Projektschätzungen**: Projektschätzungen in Vorlagen funktionieren wie in Projekten, abgesehen davon, dass Preislisten für die Standardkosten und die Verkaufspreise immer die Standardkosten und Verkaufspreislisten sind, die in den [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Parametern definiert werden. Die restlichen Funktionalitäten sind identisch mit einem Projekt.  
  
- **Projektteambildung**: Wenn Sie ein Projektteam für eine Projektvorlage zusammenstellen, können Sie keine benannte Ressource in einer Vorlage buchen. Sie können im Projektstrukturplan **Projektteam generieren** verwenden, um einen Satz allgemeiner Ressourcen zu generieren. Sie könne auch erforderliche Kompetenzen und Fähigkeiten für allgemeine Ressourcen angeben. Sie können keine allgemeine Ressource durch eine buchbare Ressource in den Projektvorlagen ersetzen.  
  
## <a name="create-a-project-from-a-template"></a>Erstellen eines Projekts aus einer Vorlage  
 Sie können ein Projekt aus einer Vorlage auf die folgenden Arten erstellen:  
  
-   Wenn Sie ein Projekt aus einem Angebot erstellen, können Sie eine Projektvorlage im Projektschnellerfassungsformular auswählen.  
  
-   Wenn Sie ein Projekt durch Klicken auf **Neues Projekt** erstellen, wird das Projektformular angezeigt, bevor Sie den Datensatz speichern. Von hier können Sie auf das Feld **Eine Vorlage auswählen** klicken, um aus der Liste der vordefinierten Projektvorlagen in der Organisation auszuwählen.  
  
-   Klicken Sie auf **Projekt aus Vorlage erstellen** auf der Seite **Projektvorlage**, um ein Projekt aus der Vorlage zu erstellen.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopieren von Komponenten einer Vorlage in ein Projekt:  
 Wenn Sie Komponenten einer Vorlage in ein Projekt kopieren, gibt es einige Dinge, die Sie wissen sollten.  
  
 **Kopieren eines Projektstrukturplans**: Wenn Sie den Projektstrukturplan aus einer Projektvorlage kopieren, wenn das Projekt einen anderen Projektkalender als die Vorlage hat, werden die Arbeitsstunden aus dem Kalender des Projekts auf den Aufgabenplan angewendet. Dadurch wird der Zeitplan an den zugrundeliegenden Projektkalender angepasst. Entsprechend nimmt die erste Aufgabe im Projektstrukturplan das Startdatum des Projekts, sodass der restliche Aufgabenhierarchienzeitplan anhand der Dauer und den Abhängigkeiten aktualisiert wird, die im Projektstrukturplan der Vorlage angegeben wurden.  
  
 **Kopieren von Projektschätzungen**: Wenn Sie Projektschätzungspositionen kopieren, werden Preislisten anhand der besitzenden Einheit des Projekts für die Kostenpreisliste und Kunden für die Verkaufspreisliste aktualisiert. Die Einstandspreise die Verkaufspreise der Einheit werden anhand dieser Preisliste für die Projekte bestimmt, die einer Vertriebsentität zugeordnet sind.  
  
 **Kopieren eines Projektteams**: Wenn Sie das Projektteam aus der Vorlage in ein Projekt kopieren, werden die generischen Ressourcen einschließlich der Kompetenzen und Fähigkeiten kopiert, die in der Datenbanktabelle definiert wurden. Generische Ressourcenzuweisungen werden wie in der Projektvorlage verwaltet.  
  
### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
