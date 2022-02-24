---
title: Neuigkeiten für November 2020 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen
description: Dieses Thema enthält Informationen zu den Qualitätsupdates, die in der Version von Project Operations vom November 2020 für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen verfügbar sind.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367264"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Neuigkeiten für November 2020 – Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

Dieses Thema gilt für die folgenden Dynamics 365 Project Operations-Komponenten und -Versionen:

- Project Operations in CDS, Umgebungsversion 4.4.0.70
- Projektmanagement und Buchhaltung in Dynamics 365 Finance, Umgebungsversion 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Updates für Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen

### <a name="project-operations-on-cds"></a>Project Operations in CDS

| Funktionsbereich                 | Referenznummer | Qualitätsupdate                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Verkaufschancenmanagement       | 2036993          | Die Vertragszeilen für die geschätzte Zeilen- und Ressourcenzuweisung werden bei Gewinnangeboten aktualisiert, wenn der Angebotszeilentyp **Alle Aufgaben** lautet.                                                 |
| Preise und Abrechnung          | 2070392          | Die Projektvertragszeilen auf der Rechnung erhöhen sich jedes Mal, wenn **Transaktionen für Rechnung aktualisieren** ausgewählt wird.                                                                         |
| Projektplanung             | 2043336          | Ein Projektteammitgliedsdatensatz kann nicht gelöscht werden.                                                                                                                                  |
| Projektplanung             | 2046013          | Inkonsistentes Verhalten für Schätzungen von Tag-Spalten während des Ladens im Vergleich zur Änderung des Zeitphasentyps.                                                                                   |
| Projektplanung             | 2046647          | Die Start- und Endzeiten sind um eine Stunde verschoben, wenn Ressourcenanforderungen von Mitgliedern des Projektteams generiert werden.                                                                      |
| Projektplanung             | 2053879          | (Gemäß dem bevorstehenden CDS-Rollout) PublishUnassignedAssignments unterbricht den Versuch, eine Aufgabe zu speichern, wenn der Fehler „Der für ConditionOperator.In übergebene Wert ist leer“ angezeigt wird.                       |
| Projektplanung             | 2055501          | Wenn Sie das **Projektstartdatum** leer lassen, verursacht dies einen Fehler im Zeitplan.                                                                                                      |
| Projektplanung             | 2066817          | Mit der Personenauswahl auf der **Aufgaben**-Registerkarte kann keine generische Ressource erstellt werden.                                                                                                   |
| Projektplanung             | 2067034          | **Details anzeigen**-Schaltfläche ist auf der **Aufgabendetails**-Seite nicht verfügbar.                                                                                                       |
| Ressourcenverwaltung          | 2046667          | Generische Teammitglieder werden auch dann nicht gelöscht, wenn alle Ressourcen erfüllt sind.                                                                                                    |
| Zeit- und Schnellausgabeneinträge | 2047499          | Die **Neu**-Schaltfläche auf der Zeiteingabeseite öffnet die **Neue E-Mail-Signatur**-Seite.                                                                                               |
| Zeit- und Schnellausgabeneinträge | 2059859          | Das unerwartete Popup wird geöffnet, wenn eine Spesenbuchung erstellt wird.                                                                                                                         |
| Sonstige                        | 2044181          | (Bestellung deinstallieren) Beim Versuch, die Kernlösungen von msdyn_ProjectServiceCore_Patch und msdyn Project Service zu deinstallieren, tritt der Fehler „Datensatz ist nicht verfügbar“ auf.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektmanagement und -buchhaltung in Dynamics 365 Finance

| Funktionsbereich        | Referenznummer | Qualitätsupdate                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umsatzerkennung | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Der Prozentsatz der abgeschlossenen Projektschätzung der Prozentsatz des Arbeitsfortschritts für die vollständige Methode sind falsch, wenn der Vertrag eine Fremdwährung verwendet.                     |
| Umsatzerkennung | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Schätzungen mit der **Tatsächliche Kosten**-Abschlussmethode können nicht veröffentlicht werden.                                                                                                    |
| Umsatzerkennung | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Die Eliminierung schlägt aufgrund eines Beleg-Ungleichgewichtsfehlers fehl, wenn die Unternehmenswährung und die Transaktionswährung unterschiedlich sind.                                              |
| Ausgabenverwaltung  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Für Benutzer ohne Administratorrechte werden die Suchwerte für Spesenzeilenspalten wie z. B. **Projekt-ID** und **Ausgabenkategorie** im Datenverbindungsrahmen nicht korrekt angezeigt. |
| Ausgabenverwaltung  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Die Standardeinstellung für Zeileneigenschaften wird für Ausgabenkategorien nicht angezeigt.                                                                                                         |
| Ausgabenverwaltung  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Die Ausgabenintegration muss die Zeileneigenschaft aus der Spesenabrechnung enthalten.                                                                                             |
| Rechnungsstellung           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Projektrechnungsvorschläge können aufgrund einer Fehlermeldung, die besagt, dass die Kombination von FD nicht validiert wurde, nicht veröffentlicht werden.                                                    |
| Rechnungsstellung           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Transaktionen können auf der **Rechnung**-Detailseite nicht angezeigt werden.                                                                                                              |
| Rechnungsstellung           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Rechnungsvorschlagszeilen können gelöscht werden.                                                                                                                                  |
| Projektbuchhaltung  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | **Prognose**-Menüpunkte sind auf der **Projekte**-Listenseite nicht sichtbar.                                                                                                   |
| Projektbuchhaltung  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | **Projektbeschreibung**   > **Transaktionen und Prognosen** kann nicht geöffnet werden.                                                                                                       |
| Projektbuchhaltung  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Buchhaltung anpassen** ist für in Rechnung gestellte Projekttransaktionen nicht aktiviert.                                                                                                  |
| Projektbuchhaltung  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Buchhaltungsdetails sind nicht in der **ProjCDSActualsImport**-Tabelle enthalten, wenn das **Integrationsjournal** gebucht wird.                                                  |
| Projektbuchhaltung  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Der Projektprognoseeintrag wird verdoppelt, wenn Sie eine Ressourcenzuweisung entfernen und dann erneut lesen.                                                                            |
| Projektbuchhaltung  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Durch Auswahl eines Projekt-ID-Links wird die CDS-Deep-Link-URL nicht geöffnet.                                                                                                         |
| Projektbuchhaltung  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Das Startdatum einer Aufgabe in CDS kann nicht aktualisiert werden.                                                                                                                           |
| Projektbuchhaltung  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Durch Aktivieren der Funktion sind mehrere Vertragszeilen ohne CDS-Integration nicht möglich.                                                                                   |

### <a name="regulatory-updates"></a>Aktualisierungen der Vorschriften
Informationen zu behördlichen Aktualisierungen für Finance and Operations-Apps, siehe [Aktualisierungen der Vorschriften](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Sie können sich auch bei LCS anmelden und die geplanten regulatorischen Aktualisierungen mit dem Problem-Suchwerkzeug anzeigen. Mit der Problemsuche können Sie nach Land, Art der Funktion und Version suchen.
