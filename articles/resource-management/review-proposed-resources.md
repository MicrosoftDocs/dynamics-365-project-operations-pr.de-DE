---
title: Vorgeschlagene Ressourcen überprüfen
description: Dieses Thema enthält Informationen zum Vorschlagen von Projektressourcen.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897360"
---
# <a name="review-proposed-resources"></a>Vorgeschlagene Ressourcen überprüfen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Ressourcenmanager können dem Projektmanager mithilfe einer Ressourcenanfrage eine Ressource vorschlagen.

1. Wählen Sie im Anfrageraster oder in der Anfrage selbst **Ressourcen suchen** aus.
2. Wählen Sie auf der Seite **Zeitplan-Assistent** die Ressource aus. Wählen Sie dann im Bereich **Ressourcenbuchung erstellen** im Feld **Buchungsstatus** die Option **Buchen** aus.

Die folgenden Statusupdates erfolgen:

- Auf der Seite **Zeitplan-Assistent** werden die Statusbezeichner aktualisiert, um anzuzeigen, dass es sich um eine vorgeschlagene und nicht um eine verbindliche Buchung handelt.
- Für die Ressourcenanfrage wird der Status in **Prüfung erforderlich** geändert.
- Auf der Registerkarte **Team** des Projekts wird der Wert **Anforderungsstatus** für das generische Teammitglied in **Prüfung erforderlich** geändert.

Der Projektmanager kann den Vorschlag annehmen oder ablehnen.

Zum Verarbeiten von Ressourcenanfragen können Ressourcenmanager einen der folgenden Ansätze auswählen:

- Schlagen Sie mehrere Ressourcen vor, um die Nachfrage zu befriedigen, falls zur Erfüllung der erforderlichen Stunden keine einzelne Ressource verfügbar ist. Vorgeschlagene Stunden werden dann auf mehrere Ressourcen aufgeteilt, die für die erforderlichen Stunden ausreichend sind. In diesem Szenario können sich die Stunden nicht überschneiden.
- Schlagen Sie weniger Ressourcen als erforderlich vor. In diesem Szenario ist die vorgeschlagene Ressourcenkapazität geringer als die erforderlichen Stunden, die vom Anforderer angegeben wurden. Daher wird, wenn der Anforderer die vorgeschlagenen Ressourcen annimmt, eine nicht erfüllte Ressourcenanforderung erstellt, um die restliche Nachfrage zu erfassen.
- Buchen Sie mehrere Ressourcen, um die Nachfrage zu befriedigen, falls zum Abschließen der Arbeit keine einzelne Ressource verfügbar ist.
- Buchen Sie weniger Ressourcen als erforderlich. In diesem Szenario sind die gebuchten Stunden weniger als die erforderlichen Stunden. Das System führt Sie durch das Vorschlagen von Ressourcen statt durch Buchungen, damit der Anforderer die verbleibende Nachfrage verifizieren und nachverfolgen kann.

## <a name="billable-utilization"></a>Abrechenbare Nutzung

Ressourcen weisen für die abrechenbare Nutzung einen Zielwert auf. Dieser Zielwert für die Nutzung ist entweder als ein Attribut auf der Standardrolle einer Ressource definiert, oder er ist im Datensatz der einzelnen buchbaren Ressource festgelegt. Nutzungsberechnungen basieren auf den tatsächlichen Stunden, die von Ressourcen über genehmigte Zeiteinträge gemeldet wurden.

Die folgenden Formeln werden zur Berechnung der Nutzung verwendet:

- Abrechenbare Nutzung = Fakturierbare tatsächliche Stunden ÷ Ressourcenkapazität
- Nicht abrechenbare Nutzung = tatsächliche Zeit mit Abrechnungstyp-ID = nicht fakturierbare, komplementäre oder nicht verfügbare Stunden ÷ Ressourcenkapazität
- Intern = tatsächliche Zeit ohne Vertriebsvertrag ÷ Ressourcenkapazität
- Ressourcenkapazität = Ressourcenarbeitszeiten – arbeitsfreie Tage – Abwesenheit

Sie finden die Ansicht **Ressourcennutzung** im Bereich **Ressourcen**.

Jede Zelle im Raster steht für die abrechenbare Nutzung in Prozent der Ressource in einem Zeitraum, beispielsweise einem Tag, einer Woche oder einem Monat. Die folgenden Formeln werden für die Farbgebung der Zellen verwendet:

- **Grün:** Abrechenbare Nutzung \>= Zielnutzung für die Ressource
- **Gelb:** Zielnutzung – 20 \<= abrechenbare Nutzung \< Zielnutzung
- **Rot:** abrechenbare Nutzung \< Zielnutzung – 20

Da die Ansicht **Ressourcennutzung** auf der Zeitplanübersicht basiert, können Sie die Filterfunktionen der Zeitplanübersicht zum Filtern Ihrer Ergebnisse verwenden.

Das Raster erfordert das Festlegen einer Zielnutzung entweder für die Rolle oder die einzelne Ressource. Navigieren Sie hierfür zu **Ressourcen** \> **Ressourcenrollen**.

Zusätzlich muss jeder buchbaren Ressource eine Standardrolle zugewiesen werden. Navigieren Sie zu **Ressourcen** \> **Ressourcen**. Überprüfen Sie auf der Registerkarte **Project Service**, ob eine Ressourcenrolle definiert ist und das Feld **Ist Standard** für die Rolle auf **Ja** festgelegt ist. Sie können zusätzliche Rollen hinzufügen, für die **Ist-Standard = Nein** gilt. Die Rolle mit **Ist Standard = Ja** wird zur Evaluierung der Ressourcennutzung anhand des Ziels für diese Rolle verwendet.

Auf der Registerkarte **Project Service** können Sie außerdem eine individuelle Zielnutzung für die Ressource festlegen. Die Nutzungsberechnung verwendet dann die Zielnutzung, um statt dem Ziel der Standardrolle der Ressource das Ziel der Ressource zu evaluieren.

Die Nutzung für eine Ressource wird nur dann angezeigt, wenn diese Ressource für den Zeitraum ihrer Anzeige im Raster über genehmigte, fakturierbare Zeit verfügt.

## <a name="resource-availability"></a>Ressourcenverfügbarkeit

Es ist wichtig, dass Ressourcenmanager die Verfügbarkeit von Ressourcen anzeigen and Buchungen aktualisieren können. In manchen Fällen besteht zwar keine formelle Nachfrage (Ressourcenanfrage), aber ein Ressourcenmanager muss auf eine ungeplante Nachfrage reagieren können, die über Kanäle wie E-Mails, Telefonanrufe oder Sofortnachrichten eingeht. Ressourcenmanager verwenden die Zeitplanübersicht, um Ressourcen und Buchungen zu aktualisieren.

Ressourcenarbeitszeiten werden als Grundlage für die Berechnung der Verfügbarkeit einer Ressource verwendet. Ressourcenbuchungen verbrauchen die Kapazität der Ressourcen.

Die Zeitplanübersicht verwendet Farben und Schattierungen, um Buchungen, Verfügbarkeit und Überbuchungen sowie den Status von Buchungen anzuzeigen. Eine Einstellung für die Zeitplanübersicht ermöglicht das Anzeigen einer Legende.

Wenn neben einer einzelnen buchbaren Ressource in der Zeitplanübersicht ein nach rechts zeigender Pfeil angezeigt wird, kann die Ressource erweitert werden, um Details zur Arbeit anzuzeigen, für die die Ressource gebucht ist.

Da Dynamics 365 Project Operations die Universal Resource Scheduling-Engine nutzt, können Sie für den Fall, dass Dynamics 365 Field Service ebenfalls installiert ist, die Details von Ressourcenbuchungen für Projekte, Arbeitsaufträge und jegliche anderen Entitäten anzeigen, auf die Sie die Zeitplanung erweitert haben.

Um mehr Details zu einer individuellen Ressource anzuzeigen, klicken Sie mit der rechten Maustaste darauf, um die Ressourcenkarte zu öffnen.

