---
title: Neuigkeiten für April 2021 – Project Operations – Lite-Bereitstellung
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations – Lite-Bereitstellung vom April 2021 verfügbar sind.
author: sigitac
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd6fbe8d75fbe9157a97d2edd38d40a97395c924
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868037"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Neuigkeiten für April 2021 – Project Operations – Lite-Bereitstellung

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

  - Project Operations in Dataverse, Umgebungsversion 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funktionen in dieser Version

Die folgenden Funktionen sind in dieser Version enthalten:

- Nicht vorrätige Materialien für Projekte. Die Hauptfunktionen umfassen Folgendes:
  - Schätzung und Preisgestaltung von nicht vorrätigen Materialien während des Verkaufszyklus für ein Projekt. Weitere Informationen finden Sie unter [Kosten und Verkaufsraten für Katalogprodukte einrichten – Lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Verfolgung der Verwendung nicht vorrätiger Materialien während der Projektabwicklung. Weitere Informationen finden Sie unter [Materialverbrauch für Projekte und Projektaufgaben erfassen](../../material/material-usage-log.md).
  - Fakturierung gebrauchter nicht vorrätiger Materialkosten. Weitere Informationen finden Sie unter [Abrechnungsstau verwalten – Lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Neue APIs in Dynamics 365 Dataverse ermöglichen das Erstellen, Aktualisieren und Löschen von Vorgängen mit **Planungsentitäten**. Weitere informationen finden Sie unter [Verwenden Sie Zeitplan-APIs, um Vorgänge mit Zeitplan-Entitäten auszuführen](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Qualitätsupdates

| **Funktionsbereich** | **Referenznummer** | **Qualitätsupdate** |
| --- | --- | --- |
| Preise und Abrechnung | 2224568 | Logik hinzugefügt, um Anpassungen zu ermöglichen, bei denen das Rechnungsbestätigungs-Plug-In aufgerufen wird. |
| Preise und Abrechnung | 2101098 | Die Logik der Standardfelder für die Proforma-Rechnung wurde verbessert: **Rechnungsadresse**, **Name für Rechnungsadresse** und **Zahlungsbedingungen** werden jetzt standardmäßig aus dem entsprechenden Projektvertrags-Kundendatensatz entnommen. |
| Preise und Abrechnung | 2021413 | Die Felder **Tatsächliche Kosten** und **Vertrieb** in der **Aufgabe**-Entität wurden aktualisiert, um Verkaufswerte aus nicht in Rechnung gestellten und in Rechnung gestellten Ausgaben für Aufgaben einzubeziehen. |
| Preise und Abrechnung | 2182110 | Beim Kopieren eines Projektvertrags wird die Vertragszeilen-ID im Zielprojektvertrag neu generiert, um sicherzustellen, dass sie eindeutig ist. |
| Verkaufschancenmanagement | 2186741 | Es wurden Validierungen hinzugefügt, um sicherzustellen, dass das Feld **Ursprung** und **Transaktionstyp** nicht auf vorhandenen Angebotszeilendetails aktualisiert werden kann. |
| Verkaufschancenmanagement | 2191353 | Meilensteine dürfen nicht auf einer zeitlichen und materiellen Vertragszeile erstellt werden. |
| Verkaufschancenmanagement | 2216956 | Probleme mit **Preise aktualisieren** behoben. |
| Planung und Nachverfolgung | 2182979 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass die Kostenvorkalkulationszeilen aus dem ursprünglichen Projekt kopiert werden. |
| Planung und Nachverfolgung | 2184144 | Die Projektkopierfunktion wurde verbessert, um sicherzustellen, dass der Ressourcenpositionsname aus dem ursprünglichen Projekt kopiert wird. |
| Planung und Nachverfolgung | 2184799 | Projektkopie: Das Steuerelement wurde verbessert, um sicherzustellen, dass das geschätzte Startdatum während des Kopiervorgangs nicht geändert werden kann. |
| Planung und Nachverfolgung | 2185134 | Projektkopie: Das geschätzte Startdatum des Zielprojekts wird auf das heutige Datum festgelegt. |
| Planung und Nachverfolgung | 2196373 | Projektkopie: Stellen Sie sicher, dass die Datensätze des Projektmanagers und der Teammitglieder nicht im Projektteam dupliziert werden. |
| Planung und Nachverfolgung | 2211833 | Projektkopie: Ressourcenzuweisungen werden von der Quellprojektaufgabe in das Zielprojekt kopiert. |
| Planung und Nachverfolgung | 2186541 | Probleme im **Schätzungen**-Raster bei der Gruppierung nach Ressourcen behoben. |
| Planung und Nachverfolgung | 2166906 | Die Transaktionskategorie einer Aufgabe muss in die **Ressourcenzuweisung**-Entität kopiert werden. |
| Ressourcenverwaltung | 2125362 | Probleme beim Erstellen eines generischen Teammitglieds mithilfe einer stundenbasierten Zuordnungsmethode behoben. |
| Zeit und Ausgaben | 2113603 | Das Anpassungsproblem beim Entfernen von Attributen von der **Zeiteintrag**-Seite wurde behoben. Das System prüft nun mithilfe eines Skripts, ob das Attribut auf der Seite vorhanden ist, bevor es darauf zugreift. |
| Zeit und Ausgaben | 2204377 | Kopierte Arbeitszeittabellen müssen bei der Auswahl von **Woche kopieren** während der Zeiteingabe automatisch angezeigt werden. |
| Zeit und Ausgaben | 2209059 | **Status**-Feld kann für Dynamics 365 Field Service-Zeiteinträge bearbeitet werden. |
