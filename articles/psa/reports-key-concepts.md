---
title: Wichtige Konzepte
description: Dieses Thema enthält Informationen zu den wichtigen Konzepten für das Ressourcenmanagement in Project Service Automation.
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
ms.openlocfilehash: 5f314e3a6cc70748628145f693fb81b598e568dc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008850"
---
# <a name="key-concepts"></a>Wichtige Konzepte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Die folgende Tabelle definiert Schlüsselkonzepte, die in der Dynamics 365 Project Service Automation-App verwendet werden.

| Konzept                    | Definition |
|----------------------------|------------|
| Projektteammitglied        | Im Rahmen des Projektteams kann ein Projektteammitglied eine benannte Ressource mit Buchungen, eine Ressource ohne Buchungen oder eine generische Ressource sein. Generische Ressourcen verfügen nicht über Buchungen, sind für das Projekt lokal und verfügen nicht über Kapazitätsbeschränkungen für mehrere Projekte. |
| Generische Ressource für das Projekt   | Ein Ressourcenplatzhalter, der Ihnen die Bildung eines Teams und die Ausstattung eines Projektplans mit Mitarbeitern ermöglicht, ohne dass Sie die benannte Ressource kennen müssen. Der Projektkalender wird als Kalander der generischen Ressource verwendet. Generische Ressourcen können zu einem Projektteam hinzugefügt und Aufgaben zugewiesen werden. |
| Gebuchte Stunden               | Ressourcenstunden sind für ein Projekt verbindlich gebucht, um zu gewährleisten, dass die Projektarbeit abgeschlossen wird. Gebuchte Stunden werden von der Gesamtkapazität der Ressource verbraucht. Buchungen erfolgen nur für benannte Ressourcen, nicht für allgemeine Ressourcen. |
| Zugewiesene Stunden             | Ressourcenstunden werden den Aufgaben im Projektzeitplan zugewiesen. Zuweisungen können für benannte Ressourcen oder generische Ressourcen vorgenommen werden. Zuweisungen können unabhängig von Buchungen sein. |
| Erforderliche Stunden             | Die erforderliche Kapazität, die von einer benannten Ressource jedoch noch nicht erfüllt wird. Erforderliche Stunden sind nur für generische Teammitglieder relevant, für die Ressourcenanforderungen generiert wurden. |
| Bedarf                     | Die aktuelle und eingehende Workload. In Project Service Automation wird der Bedarf als Ressourcenanforderungen oder Ressourcenanfragen angezeigt. |
| Ressourcenanforderung       | Eine Entität, die verwendet wird, um erforderliche Stunden, Start- und Enddatum, Fähigkeiten, Geografie und andere Preisdimensionen für die erforderlichen Ressourcen zu erfassen. Ressourcenanforderungen werden entweder von Projektteammitgliedern generiert oder einzeln erstellt. |
| Ressourcenanfrage           | Eine Entität, die als ein „Umschlag“ für die Ressourcenanforderung verwendet wird, die von einem Ressourcen-Manager erfüllt werden muss. |
| Standardressourcenrolle      | Die Rolle, unter der eine Ressource für die Nutzungsberechnung gruppiert ist. Für die Ressource wird angenommen, dass sie über die erforderlichen Fähigkeiten für die Rolle verfügt und sie die Zielnutzung für diese Rolle erfüllt. |
| Ressourcenorganisationseinheit | Die Organisationseinheit, der eine Ressource zugewiesen ist. |
| Kontur                    | Aufgaben-, Anforderungs- oder Zuweisungsstunden, wie sie auf eine tägliche Verteilung aufgeteilt werden. Beispielsweise kann eine fünf Tage dauernde, 40-stündige Aufgabe auf acht Stunden pro Tag für fünf Tage konturiert werden. |
| Abstimmungsansicht        | Eine Ansicht, die die Buchungen und Zuweisungen für jedes Projektteammitglied anzeigt. In dieser Ansicht können Projektmanager nach Diskrepanzen zwischen Buchungen und Zuweisungen suchen und bei Diskrepanzen korrektive Maßnahmen ergreifen. |
| Arbeitszeit                 | Eine Entität, die verwendet wird, um die Ressourcenkapazität sowie die Arbeits- und die Nicht-Arbeitszeit zu identifizieren. Diese Entität wird auch als Ressourcenkalender bezeichnet. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]