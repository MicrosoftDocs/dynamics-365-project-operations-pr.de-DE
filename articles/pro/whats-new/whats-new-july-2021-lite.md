---
title: Was ist neu Juli 2021 - Project Operations Lite-Bereitstellung
description: Dieser Artikel enthält Informationen über die Qualitätsupdates, die in der Lite-Bereitstellung von Project Operations im Juli 2021 verfügbar sind.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913987"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Was ist neu Juli 2021 - Project Operations Lite-Bereitstellung

_Gilt für: Lite Bereitstellung – Abschluss zur Proforma-Rechnungsstellung_

Dieser Artikel bezieht sich auf die folgenden Dynamics 365 Project Operations-Komponenten und Versionen:

  - Project Operations auf Dataverse Umgebung Version 4.12.0.148 oder 4.12.0.152.

## <a name="quality-updates"></a>Qualitätsupdates
| **Funktionsbereich**              | **Referenznummer** | **Qualitätsupdate**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Preise und Abrechnung           | 2224046              | Das Feld **Transaktionsklasse** kann auf der Registerkarte **Angebotszeile Details** bearbeitet werden, ist aber gesperrt, wenn Sie auf der Seite **Angebotszeile Details** arbeiten.                                                                     |
| Preise und Abrechnung           | 2224400              | Die Aktion **Angebot als gewonnen schließen** schlägt fehl, wenn ein Angebot keine Datums-Meilensteine hat.                                                                                                                                    |
| Preise und Abrechnung           | 2234089              | Wenn Sie eine Produktbeschreibung manuell eingeben, wird sie gelöscht, nachdem Sie eine Menge für eine Materialschätzung eingegeben haben.                                                                                                                         |
| Preise und Abrechnung           | 2234100              | Das Raster **Auftragsabrechnung einrichten** enthält nicht die Spalte **Material** und ihren Wert auf der Registerkarte **Auftragsabrechnung** des Projekts.                                                                                                       |
| Preise und Abrechnung           | 2277409              | Die Produkt-ID ist in den Details der Vertragszeile für eine Materialartzeile nicht verfügbar.                                                                                                                                        |
| Preise und Abrechnung           | 2281728              | Das Erstellen einer Vertragszeile führt unnötigerweise zu einer Neubewertung der Istwerte und damit zu einem erheblichen Anstieg des Datenvolumens, was die Leistung beeinträchtigt.                                                                                |
| Preise und Abrechnung           | 2298668              | Erfassungszeilen, die mit einer zurückgerufenen und gelöschten Ausgabe verbunden sind, werden nicht entfernt.                                                                                                                                     |
| Preise und Abrechnung           | 2300192              | Wenn mehrere Benutzer eine Rechnung bearbeiten, ist es möglich, dass ein neues Rechnungszeilendetail auf einer bestätigten Rechnung erstellt wird.                                                                                   |
| Preise und Abrechnung           | 2301569              | Rechnungen können nicht korrigiert werden, wenn ein Betragseinbehalt von \$0 angewendet wurde.                                                                                                                                        |
| Preise und Abrechnung           | 2307965              | Es tritt ein Fehler auf, wenn ein Kategoriepreis mit fehlenden Werten erstellt wird.                                                                                                                           |
| Preise und Abrechnung           | 2326870              | Es tritt ein Fehler in **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** auf, wenn **Producttypecode** null ist.                                                                            |
| Preise und Abrechnung           | 2332732              | Ein Fehler tritt auf, wenn ein Meilenstein für eine Vertragszeile ohne eine Auftragszeile erstellt wird.                                                                                                                |
| Projektplanung und -nachverfolgung | 2181094              | Die Projektplanungs-API unterstützt jetzt PSS-Protokolle und Vorgangs-Set-Protokolle, die für 90 Tage gespeichert werden.                                                                                                                  |
| Projektplanung und -nachverfolgung | 2254201              | Das Label **Geplanter Modus** wurde mit Details aktualisiert, die die Vorgabe-Logik beschreiben.                                                                                                                                      |
| Projektplanung und -nachverfolgung | 2300252              | Der **openProject** Antwort-Cache wird aktualisiert und enthält den Token-Besitzer im Cache-Schlüssel, **Basis-Url** und **Segment-Url**, sodass **Request-Url** immer neu erstellt werden kann, wenn sich die **Basis-Url** ändert. |
| Projektplanung und -nachverfolgung | 2301312              | **msdyn_membershipstatus** wurde aus der Ansicht **Projektteam-Mitglied** entfernt.                                                                                                                                        |
| Projektplanung und -nachverfolgung | 2302759              | Auf den Registerkarten **Ressourcenzuweisungen**, **Schätzungen** und **Aufwandsschätzungen** werden unnötigerweise Produkte geholt.                                                                                                        |
| Projektplanung und -nachverfolgung | 2308050              | **CopyProject** schlägt mit der Fehlermeldung „Fehler beim Abrufen von Token für die Kommunikation mit dem Remotedienst“ fehl.                                                                                                                           |
| Projektplanung und -nachverfolgung | 2322650              | Die Ansicht **Projektaufgabenliste** wurde aktualisiert und zeigt jetzt standardmäßig das Datum der Aufgabe an.                                                                                                            |
| Projektplanung und -nachverfolgung | 2327266              | **CopyProject** erzeugt beim Kopieren von Schätzungen den Fehler „Schlüssel nicht im Wörterbuch gefunden“.                                                                                                      |
| Projektplanung und -nachverfolgung | 2328123              | **CopyProject** erzeugt den Fehler, „Fehler beim Abrufen von Token für die Kommunikation mit dem Remotedienst“.                                                                                                                          |
| Projektplanung und -nachverfolgung | 2336258              | **CopyProject** kopiert fälschlicherweise die Positionsnamen von Ressourcen.                                                                                                                                                 |
| Preise und Abrechnung           | 2224476              | Das Feld **Buchbare Ressource** zeigt auf der Seite **Materialverwendung** nicht korrekt den angemeldeten Benutzer an.                                                                                                            |
| Ressourcenverwaltung           | 2277249              | Es tritt ein Fehler auf, wenn eine nicht projektbasierte Ressourcenanforderung aktualisiert wird.                                                                                                            |
| Ressourcenverwaltung           | 2323869              | Die Ressourcenauslastung erkennt gefilterte Ressourcen nicht korrekt.                                                                                                                                             |
| Zeit und Ausgaben              | 2176538              | Auf das Steuerelement **Zeiteintrag** werden falsche Filtervorgänge angewendet.                                                                                                                                                   |
| Zeit und Ausgaben              | 2177462              | Das Löschen eines Zeiteintrags im Raster aktualisiert den Status der Schaltflächen **Senden**, **Aufrufen**, **Löschen** und **Eintrag bearbeiten** nicht wie erwartet.                                                                                        |
| Zeit und Ausgaben              | 2299985              | **TimeEntriesImportFromResourceAssignment** erhält nicht die Start-/Endzeit aus den Zuweisungskonturen.                                                                                                  |
| Zeit und Ausgaben              | 2318426              | Nachdem ein Zeiteintrag gesendet wurde, können gesperrte Felder noch bearbeitet werden.                                                                                                                                   |
| Zeit und Ausgaben              | 2323749              | Ein Fehler tritt auf, wenn eine Leistung aus dem **Bezogen**-Register einer buchbaren Ressource erstellt wird.                                                                                                      |
| Zeit und Ausgaben              | 2327678              | Wenn Sie einen Zeiteintrag von der Registerkarte **Bezogen** einer buchbaren Ressource erstellen, wird die übergeordnete Ressource nicht an das Steuerelement für den Zeiteintrag übergeben.                                                                            |
| Allgemein                       | 2296857              | Fortschrittsverfolgung für lang ausgeführte Jobs.                                                                                                                                                                        |
| Allgemein                       | 2253682              | Die Project Operations Dual-Write-Lösung sollte nicht installiert werden, wenn Dual-Write Core in einer Umgebung ohne die Dual-Write-Orchestrierungslösung installiert ist.                                                |
| Allgemein                       | 2316420              | Die Bereitstellung von Project Service Core schlägt fehl, wenn die Einheit des Anwendungsbenutzers geändert wird.                                                                                                                     |
| Allgemein                       | 2376405              | Problem mit vom Herausgeber gesteuerten Updates behoben (Qualitätsupdate ist in Version 4.12.0.152 verfügbar)                                                                                                                     |
