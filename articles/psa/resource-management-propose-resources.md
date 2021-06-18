---
title: Projektressourcen vorschlagen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997960"
---
# <a name="propose-project-resources"></a>Projektressourcen vorschlagen

[!include [banner](../includes/psa-now-project-operations.md)]

Ressourcenmanager können dem Projektmanager mithilfe einer Ressourcenanfrage eine Ressource vorschlagen.

1. Wählen Sie im Anfrageraster oder in der Anfrage selbst **Ressourcen suchen** aus.
2. Wählen Sie auf der Seite **Zeitplan-Assistent** die Ressource aus. Wählen Sie dann im Bereich **Ressourcenbuchung erstellen** im Feld **Buchungsstatus** die Option **Buchen** aus.

    ![Ausgewählte vorgeschlagene Ressource](media/Resource-Management-image62.png)

Die folgenden Statusupdates erfolgen:

- Auf der Seite **Zeitplan-Assistent** werden die Statusbezeichner aktualisiert, um anzuzeigen, dass es sich um eine vorgeschlagene und nicht um eine verbindliche Buchung handelt.

    ![Statusbezeichner für vorgeschlagene Buchung auf der Seite „Zeitplan-Assistent“](media/Resource-Management-image63.png)

- Für die Ressourcenanfrage wird der Status in **Prüfung erforderlich** geändert.

    ![In „Prüfung erforderlich“ geänderter Status der Ressourcenanfrage](media/Resource-Management-image64.png)

- Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** für das generische Teammitglied in **Prüfung erforderlich** geändert.

    ![Anforderungsstatus des generischen Teammitglieds auf der Registerkarte „Team“ geändert in „Prüfung erforderlich“](media/Resource-Management-image48.png)

Der Projektmanager kann den Vorschlag annehmen oder ablehnen.

Zum Verarbeiten von Ressourcenanfragen können Ressourcenmanager einen der folgenden Ansätze auswählen:

- Mehrere Ressourcen vorschlagen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die geforderten Stunden zu erfüllen. Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind. In diesem Szenario können sich die Stunden nicht überschneiden.
- Schlagen Sie weniger Ressourcen als erforderlich vor. In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die vom Anforderer angegeben wurden. Wenn der Anfragende die vorgeschlagenen Ressourcen akzeptiert, wird daher eine nicht erfüllte Ressourcenanforderung erstellt, um den restlichen Bedarf zu erfassen.
- Mehrere Ressourcen buchen, um den Bedarf zu decken, wenn keine einzelne Ressource verfügbar ist, um die Arbeit zu erledigen.
- Weniger Ressourcen buchen als benötigt werden. In diesem Szenario sind die gebuchten Stunden geringer als die benötigten Stunden. Das System führt Sie durch das Vorschlagen von Ressourcen statt durch Buchungen, damit der Anforderer die verbleibende Nachfrage verifizieren und nachverfolgen kann.

## <a name="billable-utilization"></a>Abrechenbare Nutzung

Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf. Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt. Die Berechnung der Nutzung basiert auf den tatsächlichen Stunden, die Ressourcen in ihren genehmigten Zeiteinträgen angegeben haben.

Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:

- Fakturierbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität
- Nicht fakturierbare Nutzung = Tatsächliche Zeit mit Fakturierungstyp-ID = Nicht fakturierbar, komplementär oder nicht verfügbar ÷ Ressourcenkapazität
- Intern = Tatsächliche Zeit ohne Kaufvertrag ÷ Ressourcenkapazität
- Ressourcenkapazität = Ressourcenarbeitsstunden – Abwesend – Arbeitsfreie Tage

Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.

![Ansicht „Ressourcennutzung“](media/Resource-Management-image65.png)

Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat. Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:

- **Grün:** Abrechenbare Nutzung \>= Zielnutzung für die Ressource
- **Gelb:** Zielnutzung – 20 \<= abrechenbare Nutzung \< Zielnutzung
- **Rot:** abrechenbare Nutzung \< Zielnutzung – 20

Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.

Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource. Navigieren Sie hierfür zu **Ressourcen** \> **Ressourcenrollen**.

Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden. Navigieren Sie zu **Ressourcen** \> **Ressourcen**. Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist. Sie können zusätzliche Rollen hinzufügen, für die **Ist-Standard = Nein** gilt. Die Rolle mit **Ist Standard = Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.

![Festgelegte Standardrolle](media/Resource-Management-image67.png)

Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen. Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.

Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.

## <a name="resource-availability"></a>Ressourcenverfügbarkeit

Es ist wichtig, dass Ressourcenmanager die Verfügbarkeit von Ressourcen anzeigen and Buchungen aktualisieren können. In manchen Fällen besteht zwar keine formelle Nachfrage (Ressourcenanfrage), aber ein Ressourcenmanager muss auf eine ungeplante Nachfrage reagieren können, die über Kanäle wie E-Mails, Telefonanrufe oder Sofortnachrichten eingeht. Ressourcenmanager verwenden die Zeitplanübersicht, um Ressourcen und Buchungen zu aktualisieren.

Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet. Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.

![Zeitplanübersicht](media/Resource-Management-image68.png)

Die Zeitplanübersicht verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen. Eine Einstellung für die Zeitplanübersicht ermöglicht das Anzeigen einer Legende.

Wenn neben einer einzelnen buchbaren Ressource in der Zeitplanübersicht ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.

![Erweiterte buchbare Ressource in der Zeitplanübersicht](media/Resource-Management-image69.png)

Da Dynamics 365 Project Service Automation die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.

![Details zu Ressourcenbuchungen für Projekte und Arbeitsaufträge](media/Resource-Management-image70.png)

Um mehr Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.

![Ressourcenkarte](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]