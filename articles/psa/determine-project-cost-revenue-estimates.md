---
title: Schätzungen bezüglich Arbeit, Kosten und Umsatz für ein Projekt bestimmen
description: Bestimmen von Projektkosten- und Umsatzschätzungen (Project Service)
author: ruhercul
ms.prod: ''
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
ms.openlocfilehash: 5d1bdde3c376a74952d54a1e7fade1f48e675d2f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580225"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Schätzungen bezüglich Arbeit, Kosten und Umsatz für ein Projekt bestimmen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekteinschätzungen stellen die Finanzansicht für die Arbeit bereit, die in der Projektstrukturplan des Projektes geschätzt und geplant wird. Die Schätzungsansicht informiert Sie über die Kosten und die Umsatzauswirkungen der geplanten Arbeit. Die Schätzungsansicht liefert ein Werkzeug, um die Informationen zu einer Reihe vorher festgelegter Dimensionen anzuzeigen, um Sie am besten über die Finanzauswirkung des Projektes zu informieren.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Kosten und Vertriebswert des Projektes  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-Preislisten definieren die Kosten und die Rechnungssätze für Rollen, die in Projekten verwendet werden. Basierend auf den Rollen, die mit den Aufgaben in der Projektstrukturplan des Projektes verbunden sind, können Sie die Kosten und die Umsatzauswirkung der betroffenen Arbeit bestimmen.  
  
## <a name="cost-price-defaulting"></a>Standard-Einstandspreis  
Jedes Projekt gehört einer Organisation an (angezeigt in **Zuständige Einheit** im Projekt). Die Preisliste, die mit der zuständigen Organisationseinheit verbunden ist, bestimmt den Einheitsselbstkostenpreis. Die [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] bestimmen Kostenpreise für Rollen, indem nach der Kombination der Rolle, der Einheit und der Organisationseinheit in der Kostenpreisliste gesucht wird, um den korrekten Kostenpreises für das Datum zu erhalten, das auf Vorkalkulationspositionen wirksam wird.  
  
Wenn die Kombination von Rollen, Einheiten und Organisationseinheit keinen Kostenpreis aus der zuständigen Einheitspreisliste ergibt, wird die Einheit zugunsten der Kombination der Rolle und der Organisationseinheit verworfen. Wenn es einen Kostenpreis gibt, wird dieser Preis in die Einheit umgewandelt, die Sie auf der Vorkalkulationsposition ausgewählt haben.  
  
Wenn die Kombination der Rolle und der Organisationseinheit keinen Kostenpreis ergibt, wird die Organisationseinheit zugunsten der Rollen- und Einheitskombination verworfen, und der Preis wird auf den Standard zurückgesetzt, nachdem alle notwendigen Umwandlungen angewendet wurden.  
  
 Wenn es keinen Preis für die Rolle gibt, dann wird der Kostenpreis standardmäßig auf 0,00 auf der Vorkalkulationsposition gesetzt.  
  
 Alle Kostenmengen auf Kostenvorkalkulationsposition des Projekts werden in der Währung der zuständigen Organisationseinheit angegeben.  
  
## <a name="sales-price-defaulting"></a>Standard-Vertriebspreis  
Die Vertriebspreisliste basiert auf der Vertriebsentität, die das Projekt zugewiesen ist. Die Vertriebspreisliste, die mit dem Angebot oder dem Vertrag verbunden ist, bestimmt den Einheitsvertriebskostenpreis. Wenn das Angebot oder der Vertrag eine benutzerdefinierte Preisliste hat, ist dies die Standardvertriebspreisliste für die Projektschätzungen. Wenn es keine Vereinigung zu den Verkaufsentitäten gibt, dann ist die Standardverkaufspreisliste, die in den Parametereinstellungen konfiguriert ist, die Standardverkaufspreisliste für das Projekt. Jeder Vorkalkulationsposition ist eine Organisationseinheit der Ressource zugewiesen, um die Organisationseinheit anzuzeigen, von der die Ressourcen für den Abschluss der Aufgabe gebucht werden. Der Vertriebspreis für die zugewiesenen Rollen, wird bestimmt, indem nach der Kombination der Rolle, der Einheit und der Organisationseinheit der Ressource in der Vertriebspreisliste gesucht wird, um den korrekten Vertriebspreises für das Datum zu erhalten, das auf Schätzungslinien wirksam wird.  
  
Wenn die Kombination der Rolle, der Einheit und der Organisationseinheit der Ressource keinen Vertriebspreis aus der Vertriebspreisliste ergibt, verwirft das System die Einheit und sucht nach der Kombination aus Rolle und Organisationseinheit der Ressource. Wenn ein Vertriebspreis gefunden wird, wird dieser in die Einheit umgewandelt, die Sie auf der Vertriebsvorkalkulationsposition ausgewählt haben.  
  
Wenn das System keinen Preis für die Rolle findet, dann muss der Vertriebspreis standardmäßig auf 0,00 auf der Vorkalkulationsposition gesetzt.  
  
Die Vorkalkulationsansicht hat eine Gitteransicht, die ein flaches Gitter von Vorkalkulationspositionen mit Einheit und Gesamtkosten und Vertriebspreis anzeigt.  
  
## <a name="time-phased-view-of-project-estimates"></a>Zeitphasenansicht von Projektschätzungen  
In der Zeitphasenansicht für Projektschätzungen werden die Schätzungsdaten von der Gitteransicht standardmäßig durch die Rolle kreuzgefiltert und zeigt eine Tabelle der Schätzungsdaten über der Zeitachse im ausgesuchten Zeitraum an.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Aufwandabschätzungsverteilung basierend auf Aufgabenmodus  
In der Zeitphasenansicht wird der Gesamtaufwand, der für die Aufgabe geschätzt wird, zugewiesen, indem eine bestimmte Anzahl von Aufwandsstunden pro Einheitszeitraum des ausgesuchten Zeitraums zugewiesen wird. Im Project Service bestimmt der Aufgabenmodus, wie der Aufwand über die Dauer der Aufgabe zugeteilt wird. Die zwei Arten der Verteilung sind gleichmäßige Zuteilung und auf Arbeitsstunden basierte Zuteilung. 
  
## <a name="work-hours-based-allocation"></a>Arbeitsstunden basierte Zuteilung  
Der automatische Aufgabenzeitplanmodus regelt den für die Anzahl von Ressourcen, die für die Aufgabe geschätzt werden, sie werden für die vollen Arbeitsstunden pro Tag geschätzt. Dies trifft auch zu, wenn die Zuweisung des Aufwands durch Aufteilung über der Dauer der Aufgaben in der Zeitphasenansicht erfolgt. Zum Beispiel: Bei einem ein „Tag“-Zeitraum für eine Aufgabe, die durch eine Ressource abgeschlossen werden soll, übersteigt der zugewiesene Aufwand pro Tag nicht die Arbeitsstunden pro Tag, die im Kalender des Projektes definiert werden. Deshalb garantiert die Aufwandszuweisung immer, dass die Ressourcen so geschätzt werden, dass sie den ganzen Tages verwendet werden.  
  
## <a name="even-distribution"></a>Gleichmäßige Verteilung  
Manuell geplanter Aufgabenmodus zieht die Arbeitsstunden, den Projektkalender oder die Anzahl der Ressourcen, die für die Aufgabe definiert werden, nicht in Betracht. Der Arbeitsplan basiert auf Benutzereingaben. Für solche Aufgaben hat die Aufwandszuteilung pro Einheitszeitraum des ausgesuchten Zeitraums keine Begrenzungsfaktoren. Der Gesamtaufwand für die Aufgabe wird gleichmäßig auf jeden Einheitszeitraum im ausgesuchten Zeitraum aufgeteilt und zugeteilt.  
  
Auf diese Art bestimmt der Aufgabenmodus für die Aufgabe die Aufwandsverteilung oder die Verteilung des Aufwands pro Einheitszeitraum in Zeitphasenschätzungen.  
  
## <a name="grouping-and-time-phasing-options"></a>Gruppierung und Zeitphasenoptionen  
Diese Ansicht hilft Ihnen, die Verteilung des Aufwands, der Kosten und der Vertriebsschätzungen auf Tages-, Wochen-, Monats- oder Jahresbasis zu verstehen. Die Option „Gruppieren nach“ erlaubt das Kreuzfiltern der Schätzungsdaten auf zwei anderer Dimensionen: Kategorie und Ressource. Auf der Gitteransicht und der Zeitphasenansicht können Sie die Felder auswählen, die angezeigt werden sollen. Summen für jeden der Zeitblöcke werden unten angezeigt, und geben die Summe des geschätzten Aufwands und der Kosten an sowie die Verkäufe für den Tag, die Woche, den Monat oder das Jahr.  
  
Der Standardeinstandspreis und der Verkaufspreis sind datumswirksam. Wenn sich die Sätze für die Rollen ändern, sind sie in der Zeitphasenansicht transparenter, wenn Schätzungsdaten, die auf Ressource gefiltert und mit wöchentlicher Zeitphase angezeigt werden.  
  
## <a name="expense-estimates"></a>Ausgabenschätzungen  
Jede Ausgabe im Projekt, die nicht direkt mit der verbrauchten Arbeit zusammenhängt, kann in den Projektschätzungen in der Gitteransicht notiert werden. Unter Verwendung der **Neue Ausgabenvorkalkulation hinzufügen**-Option in der Gitteransicht, können Sie dies erreichen. Die Ausgabenschätzungen können für eine bestimmte Aufgabe oder für das gesamte Projekt aufgezeichnet werden. In diesen Zeilen können Sie Ausgabenkategorien auswählen und ein vorläufiges Datum auswählen, an dem die Kosten voraussichtlich anfallen. Wenn die verbundenen Kosten und die Vertriebspreisliste Standardpreise oder die Aufschlagprozentsätze, die für Ausgabenkategorien definiert werden, haben, sind sie standardmäßig auf der Vorkalkulationsposition der Zuweisung.  
  
### <a name="see-also"></a>Siehe auch  
 [Handbuch des Projektmanagers](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
