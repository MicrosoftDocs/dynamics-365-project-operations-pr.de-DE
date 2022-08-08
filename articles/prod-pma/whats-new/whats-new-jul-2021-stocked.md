---
title: Was ist neu oder geändert in Project Operations, Juli 2021 für lager-/produktionsbasierte Szenarien
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Version von Project Operations vom Juli 2021 für Szenarien auf Lager-/Produktionsbasis verfügbar sind.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028839"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Was ist neu oder geändert in Project Operations, Juli 2021 für lager-/produktionsbasierte Szenarien

_**Gilt für:** Project Operations für lager-/produktionsbasierte Szenarien_

Dieser Artikel bezieht sich auf die folgenden Dynamics 365 Project Operations-Komponenten und Versionen:

- Projektmanagement und -buchhaltung in Dynamics 365 Finance-Umgebungsversion 10.0.20
 
### <a name="quality-updates"></a>Qualitätsupdates
                                                                                                                                                                                  
| Funktionsbereich                      | Referenznummer| Qualitätsupdate                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektmanagement und -buchhaltung | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Kostenzusage-Datensätze aus einer Bestellanforderung werden gelöscht, sobald die Bestellung aus der Bestellanforderungsausgabe freigegeben wird.                                                                           |
| Projektmanagement und -buchhaltung | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Die Budgetvalidierung erfolgt zweimal bei einer Bestellanforderung. Diese Duplizierung führt dazu, dass die Bestellanforderung nicht abgeschlossen werden kann und die entsprechende Einkaufsbestellung nicht erstellt wird.                                                                                                                        |
| Projektmanagement und -buchhaltung | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Die Abrechnungsregel **Prozentsatz zur Abrechnung nach** konnte aufgrund eines Rundungsproblems nicht abgeschlossen werden.                                                                              |
| Projektmanagement und -buchhaltung | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Wenn Sie die Transaktion anpassen und der Prozentsatz Dezimalstellen hat, werden die Kalkulation und der Verkaufspreis nicht korrekt angepasst.                                      |
| Projektmanagement und -buchhaltung | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Der Buchhaltungsquellen-Explorer zeigt Stunden für eine einzelne Arbeitszeitnachweis-Zeile für mehrere Arbeitszeitnachweis-Zeilen mit unterschiedlichen Aktivitäten an.                                      |
| Projektmanagement und -buchhaltung | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Gespeicherte Ansichten und die Personalisierung von Arbeitszeitnachweisen führen dazu, dass das System beim Versuch, einen Arbeitszeitnachweis zu öffnen, immer die Details für den ersten Arbeitszeitnachweis in der Liste öffnet.  |
| Projektmanagement und -buchhaltung | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Der Projektstammknoten verschwindet und Projektstrukturplan-Datensätze werden nach dem Import gelöscht.                                                                                             |
| Projektmanagement und -buchhaltung | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Wenn Elemente empfangen und teilweise aus der Elementanforderung ausgegeben werden, aktualisiert das System den falschen Budgetverbrauchssaldo. |
| Projektmanagement und -buchhaltung | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Projekt-Vorschussbestellungen zeigen die Summen im Bereich **Summen** oder im Raster **Ausstehende Rechnung** nicht korrekt an.                                                                  |
| Projektmanagement und -buchhaltung | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Beim Abschluss des Bestands werden die Kostenanpassungen für Projektelemente auf das Bestandskonto statt auf das Gewinn- und Verlustkonto gebucht.                                                            |
| Projektmanagement und -buchhaltung | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Ein Beleg für eine projektgebuchte Transaktion und ein Schätzungsbeleg verwenden USD als Buchhaltungswährung, aber der Betrag zeigt an, was der CAD-Gegenwert wäre.              |
| Projektmanagement und -buchhaltung | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Gebundene Kosten mit einer Element-Anforderung und einer Bestellung sind im Rechnungsprozess der Bestellung mit teilweisem Produktzugang und teilweiser Rechnungsstellung falsch.       |
| Projektmanagement und -buchhaltung | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Die Projektanpassung aktualisiert den Umsatzbetrag mit indirekten Kosten nicht korrekt.                                                                                    |
| Projektmanagement und -buchhaltung | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Der Tabelle **Arbeitszeitnachweis** fehlt eine definierte Beziehung mit der Ansicht **Arbeitskraft/Ressource**.                                                                                   |
| Projektmanagement und -buchhaltung | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Das Feld **Aktivitätsnummer** kann nicht ausgefüllt werden, wenn Sie es aus dem Dropdown-Menü für einen Intercompany Arbeitszeitnachweis auswählen.                                                                 |
| Projektmanagement und -buchhaltung | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Sie können kein personalisiertes **Zweck** oder **Aktivitätsbeschreibung**-Feld auf den folgenden Seiten hinzufügen: **Projekt gebucht Transaktion**, **Rechnungsvorschlag erstellen** oder **Rechnungsvorschlag**.  |
| Projektmanagement und -buchhaltung | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Das Steuerelement für das falsche Lieferdatum wird bereitgestellt, wenn Sie Elementanforderungen mithilfe der Datenverwaltung erstellen (**ProjSalesItemRequirementEntity**).                                              |
| Projektmanagement und -buchhaltung | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Wenn Sie eine Projektvertrags-ID in Finance auswählen, öffnet die integrierte Umgebung von Project Operations die Seite zum Erstellen eines neuen Datensatzes, anstatt den vorhandenen Projektvertrag zu öffnen.                                                                                                                 |
| Projektmanagement und -buchhaltung | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Das Label „@SYS4083080“ („Es konnte kein eindeutiger Datensatz für Arbeitskräfte gefunden werden, der den eingegebenen Werten entspricht“) wird nicht ins Dänische übersetzt.                                |
| Projektmanagement und -buchhaltung | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Das Feld **Element Mehrwertsteuergruppe** ist auf einem Rechnungsvorschlag nicht editierbar.                                                                               |
| Projektmanagement und -buchhaltung | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Kalkulierte Kosten werden mit nicht abzugsfähigen Steuerbeträgen überbewertet.                                                                                                    |
| Projektmanagement und -buchhaltung | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Das Buchen eines Intercompany Arbeitszeitnachweises mit mehreren Projekten und unterschiedlichen finanziellen Dimensionen erzeugt unerwartete Werte im Hauptbuch.                             |
| Projektmanagement und -buchhaltung | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Zeilen des Rechnungsvorschlags werden dupliziert, weil mehrere Instanzen des periodischen Prozesses **Import aus Staging** gleichzeitig ausgeführt werden.                                      |
| Projektmanagement und -buchhaltung | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Es gibt einen Fehler bei der Buchung des Rechnungsvorschlags für die Gutschrift, sodass die Transaktionen auf dem Beleg nicht ausgeglichen sind.    |
| Projektmanagement und -buchhaltung | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Die für das Projekt kalkulierten Kosten werden nach der Freigabe von ausstehenden Rechnungen falsch.                                                                             |
| Projektmanagement und -buchhaltung | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Sie können keine Gutschrift für einen Projekt-Verkaufsauftrag erstellen, wenn die Steuer in einer anderen Währung als der Währung der Firma angegeben ist.                                      |
| Projektmanagement und -buchhaltung | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Beim Löschen eines Vertrags wird auch die mit dem Debitor verknüpfte Adresse gelöscht.                                                                                     |
| Projektmanagement und -buchhaltung | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Ein Rechnungsvorschlag, der aus einer negativen Zeittransaktionskorrektur resultiert, kann nicht gebucht werden.                                                                    |
| Reisekosten und Ausgaben                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Die Steuer wird in Spesenabrechnungen anders berechnet.                                                                                                                  |
| Reisekosten und Ausgaben                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Das Release-Update **DB72_Expense.updateTrvExpTransProjTransId()** lässt nicht zu, dass **trvExpTrans.ReferenceDataAreaId** die neue Nummernkreis-Sequenz erstellt.                    |
| Reisekosten und Ausgaben                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Der abgelegte Betrag wird nicht mit dem Pflichtfeld angezeigt.                                                                                                             |
| Reisekosten und Ausgaben                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Die Leistung beim Anhängen einer Spesenabrechnung an die Spesenabrechnung unter Verwendung der Benutzeroberfläche von neu gestalteten Spesen wurde verbessert.                                                            |
| Reisekosten und Ausgaben                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Sie können gebuchte Spesenabrechnungen löschen.                                                                                           |
| Reisekosten und Ausgaben                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Die Nachricht „Spesenrichtlinie“ wird mehrfach angezeigt.                                                                                                       |
| Reisekosten und Ausgaben                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Das Feld **Zahlungsmethode** ist im Bereich **Neue Leistung** enthalten.                                                                                                      |
| Reisekosten und Ausgaben                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Das Tool **Status des Spesenbelegs zurücksetzen** sollte den Status der Spesenabrechnung auf **Entwurf** zurücksetzen, wenn der Workflow nicht gefunden wurde. 

### <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften
Informationen zu regulatorischen Aktualisierungen für Finanz- und Betriebs-Apps finden Sie unter [Regulatorische Aktualisierungen](/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei Lifecycle Services (LCS) anmelden und die geplanten Aktualisierungen der Vorschriften mit dem Tool Ausgabensuche anzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
