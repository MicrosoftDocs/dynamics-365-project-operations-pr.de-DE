---
title: Upgrade von Project Service Automation auf Project Operations
description: Dieser Artikel gibt einen Überblick über den Prozess des Upgrades von Microsoft Dynamics 365 Project Service Automation auf Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736665"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade von Project Service Automation auf Project Operations

Wir freuen uns, die zweite von drei Phasen für das Upgrade von Microsoft Dynamics 365 Project Service Automation auf Microsoft Dynamics 365 Project Operations ankündigen zu können. Dieser Artikel bietet einen Überblick für Kunden, die sich auf diesen spannenden Verlauf einlassen. 

Das Upgrade-Lieferprogramm wird in drei Phasen unterteilt.

| Upgrade-Lieferung | Phase 1 (Januar 2022) | Phase 2 (November 2022) | Phase 3 (April-Zyklus 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Keine Abhängigkeit vom Projektstrukturplan (PSP) für Projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Ein PSP innerhalb der derzeit unterstützten Grenzen von Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Ein PSP außerhalb der derzeit unterstützten Grenzen von Project Operations, einschließlich der Unterstützung für den Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funktionen des Upgradeprozesses 

Als Teil des Upgradeprozesses haben wir der Siteübersicht Upgrade-Protokolle hinzugefügt, damit Administratoren die Fehler leichter diagnostizieren können. Neben der neuen Schnittstelle werden neue Validierungsregeln hinzugefügt, um die Datenintegrität nach einem Upgrade sicherzustellen. Die folgenden Validierungen werden dem Upgrade-Prozess hinzugefügt.

| Prüfungen | Phase 1 (Januar 2022) | Phase 2 (November 2022) | Phase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| Der PSP wird auf gängige Datenintegritätsverletzungen überprüft (z. B. Ressourcenzuweisungen, die derselben übergeordneten Aufgabe zugeordnet sind, aber unterschiedliche übergeordnete Projekte aufweisen). | | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP wird gegen die [bekannten Grenzen von Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) validiert. | | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP wird gegen die bekannten Grenzen von Project Desktop Client validiert. | |  | :heavy_check_mark: |
| Buchbare Ressourcen und Projektkalender werden anhand allgemeiner inkompatibler Kalenderregelausnahmen bewertet. | | :heavy_check_mark: | :heavy_check_mark: |

In Phase 2 werden bei Kunden, die auf Project Operations aktualisieren, die bestehenden Projekte auf eine schreibgeschützte Erfahrung für die Projektplanung aktualisiert. In dieser schreibgeschützten Umgebung wird der vollständige PSP im Verfolgungsraster angezeigt. Um den PSP zu bearbeiten, können Projektmanager [**Konvertieren**](/PSA-Upgrade-Project-Conversion.md) auf der Hauptseite Projekte auswählen. Ein Hintergrundprozess aktualisiert dann das Projekt, sodass es die neue Projektplanungserfahrung von Project for the Web unterstützt. Diese Phase ist für Kunden geeignet, die Projekte haben, die in die [bekannten Grenzen von Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) passen.

In Phase 3 wird die Unterstützung für den Project Desktop Client zum Vorteil der Kunden hinzugefügt, die ihre Projekte weiterhin von dieser Anwendung aus bearbeiten möchten. Wenn jedoch vorhandene Projekte in die neue Project for the Web-Erfahrung konvertiert werden, wird der Zugriff auf das Add-In für jedes konvertierte Projekt deaktiviert.

## <a name="prerequisites"></a>Anforderungen

Um für das Phase-1-Upgrade berechtigt zu sein, müssen Sie die folgenden Kriterien erfüllen:

- Die Zielumgebung darf keine Datensätze in der **msdyn_projecttask**-Entität enthalten.
- Allen aktiven Benutzern des Kunden müssen gültige Project Operations-Lizenzen zugewiesen werden. 
- Sie müssen den Upgrade-Prozess in mindestens einer Nicht-Produktionsumgebung validieren, die einen repräsentativen Datensatz enthält, der mit Ihrer Produktionsumgebung abgeglichen ist.
- Die Zielumgebung muss auf Project Service Automation Update Release 37 (V3.10.58.120) oder höher aktualisiert werden.

Um für das Phase-2-Upgrade berechtigt zu sein, müssen Sie folgende Kriterien erfüllen:

- Allen aktiven Benutzern des Kunden müssen gültige Project Operations-Lizenzen zugewiesen werden. 
- Sie müssen den Upgrade-Prozess in mindestens einer Nicht-Produktionsumgebung validieren, die einen repräsentativen Datensatz enthält, der mit Ihrer Produktionsumgebung abgeglichen ist.
- Die Zielumgebung muss auf Project Service Automation Update Release 37 (V3.10.58.120) oder höher aktualisiert werden.
- Umgebungen, die Aufgaben (msdyn_projecttask) enthalten, werden nur unterstützt, wenn die Gesamtzahl der Aufgaben pro Projekt 500 oder weniger beträgt.

Die Voraussetzungen für Phase 3 werden aktualisiert, wenn sich der allgemeine Verfügbarkeitstermin nähert.

## <a name="licensing"></a>Lizenzierung

Wenn Sie über aktive Lizenzen für Project Service Automation verfügen, können Sie Project Operations installieren und verwenden, das alle Funktionen von Project Service Automation und mehr umfasst. Auf diese Weise können Sie die Fähigkeiten von Project Operations testen, während Sie Project Service Automation weiterhin in der Produktion verwenden. Nach Ablauf Ihrer Project Service Automation-Lizenzen müssen Sie zu Project Operations wechseln. Wenn Sie diesen Übergang planen, müssen Sie berücksichtigen, dass die Project Operations-Lizenz keine Project Service Automation-Lizenz enthält. Kunden, die Project Service Automation bereitgestellt haben und ihre PSA-Lizenzen weiter nutzen oder erhöhen möchten, während sie einen Wechsel zu Project Operations planen, können temporäre PSA-Lizenzen auf der Grundlage der von Project Operations gekauften Lizenzen anfordern. Eine Project Service Automation-Lizenz wird für eine Project Operations-Lizenz ausgestellt. Temporäre PSA-Lizenzen können unter folgendem Link angefordert werden: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Testen und Umgestaltung von Anpassungen

Importieren Sie zunächst alle Anpassungen in eine saubere Project Operations (Lite)-Umgebung, um sicherzustellen, dass der Import erfolgreich ist und sich die Geschäftsvorgänge wie erwartet verhalten.

Hier sind einige Dinge, auf die Sie achten sollten:

- Der Import kann aufgrund fehlender Abhängigkeiten fehlschlagen. Mit anderen Worten, die Anpassungen verweisen auf Felder oder andere Komponenten, die in Project Operations entfernt wurden. Entfernen Sie in diesem Fall diese Abhängigkeiten aus der Entwicklungsumgebung.
- Wenn Ihre nicht verwalteten und verwalteten Lösungen nicht angepasste Komponenten enthalten, entfernen Sie diese Komponenten aus der Lösung. Zum Beispiel, wenn Sie die Entität **Projekt** anpassen, fügen Sie Ihrer Lösung nur den Entitätsheader hinzu. Fügen Sie nicht alle Felder hinzu. Wenn Sie zuvor alle Unterkomponenten hinzugefügt haben, müssen Sie möglicherweise manuell eine neue Lösung erstellen und ihr relevante Komponenten hinzufügen.
- Formulare und Ansichten werden möglicherweise nicht wie erwartet angezeigt. Wenn Sie eines der vordefinierten Formulare oder Ansichten angepasst haben, können die Anpassungen unter Umständen verhindern, dass neue Updates in Project Operations wirksam werden. Um diese Probleme zu identifizieren, empfehlen wir Ihnen, parallel eine Neuinstallation von Project Operations und eine Installation von Project Operations, die Ihre Anpassungen enthält, zu überprüfen. Vergleichen Sie die am häufigsten verwendeten Formulare in Ihrem Unternehmen, um sicherzustellen, dass Ihre Version des Formulars noch sinnvoll ist und nichts in der sauberen Version des Formulars fehlt. Führen Sie die gleiche Art der parallelen Überprüfung für alle Ansichten durch, die Sie angepasst haben.
- Die Geschäftslogik schlägt möglicherweise zur Laufzeit fehl. Da Verweise auf Felder in Ihren Plug-Ins zum Zeitpunkt des Imports nicht validiert werden, schlägt die Geschäftslogik möglicherweise aufgrund von Verweisen auf nicht mehr vorhandene Felder fehl, und Sie erhalten möglicherweise eine Fehlermeldung, die dem folgenden Beispiel ähnelt: „'Projekt'-Entität enthält kein Attribut mit Name = 'msdyn_plannedhours' und NameMapping = 'Logical'.“ Ändern Sie in diesem Fall Ihre Anpassungen so, dass sie die neuen Felder verwenden. Wenn Sie automatisch generierte Proxy-Klassen und starke Typreferenzen in Ihrer Plug-In-Logik verwenden, ziehen Sie in Betracht, diese Proxys aus einer Neuinstallation heraus neu zu generieren. Auf diese Weise können Sie leicht alle Stellen identifizieren, an denen Ihre Plug-Ins von veralteten Feldern abhängig sind.

Nachdem Sie Ihre Anpassungen aktualisiert haben, um Project Operations sauber zu importieren, fahren Sie mit den nächsten Schritten fort.

## <a name="end-to-end-testing-in-development-environments"></a>End-to-End-Tests in Bereitstellungsumgebungen

### <a name="initiate-upgrade"></a>Upgrade einleiten 

1. Finden und wählen Sie im Power Platform Portal Admin Center Ihre Umgebung aus. Suchen und wählen Sie dann in den Anwendungen **Dynamics 365 Project Operations**.
2. Wählen Sie **Installieren**, um das Upgrade zu starten. Das Power Platform Admin Center wird diese Installation als neue Installation präsentieren. Das Vorhandensein einer früheren Version von Project Service Automation wird jedoch erkannt und die vorhandene Installation wird aktualisiert.

    Nach Abschluss des Upgrades sollte in der Umgebung angezeigt werden, dass Project Operations installiert ist und dass Project Service Automation nicht installiert ist.

    Je nach Datenmenge in der Umgebung kann das Upgrade mehrere Stunden dauern. Das Kernteam, das das Upgrade verwaltet, sollte entsprechend planen und das Upgrade außerhalb der Geschäftszeiten durchführen. In manchen Fällen sollte das Upgrade bei großem Datenvolumen am Wochenende durchgeführt werden. Die Entscheidung über die Planung sollte auf den Testergebnissen in niedrigeren Umgebungen basieren.

3. Aktualisieren Sie benutzerdefinierte Lösungen nach Bedarf. Stellen Sie zu diesem Zeitpunkt alle Änderungen bereit, die Sie an Ihren Anpassungen im Abschnitt [Testen und Überarbeiten von Anpassungen](#testing-and-refactoring-customizations) in diesem Artikel vorgenommen haben.
4. Gehen Sie zu **make.powerapps.com**, wählen Sie Ihre Umgebung aus der Dropdown-Liste oben rechts im Portal aus, wählen Sie **Lösungen** und wählen Sie im linken Menü die **Project Operations weraltete Komponenten** Lösung und dann **Deinstallieren** aus.

    Diese Lösung ist eine temporäre Lösung, die das vorhandene Datenmodell und die Komponenten enthält, die während des Upgrades vorhanden sind. Durch das Entfernen dieser Lösung entfernen Sie alle Felder und Komponenten, die nicht mehr verwendet werden. Auf diese Weise tragen Sie dazu bei, die Schnittstelle zu vereinfachen und die Integration und Erweiterung zu erleichtern.
    
### <a name="upgrade-to-project-operations-lite"></a>Upgrade auf Project Operations Lite

Die folgenden Schritte beschreiben den Upgrade-Prozess und die zugehörige Fehlerprotokollierung:

1. **PSA-Versionsprüfung:** Um Project Operations zu installieren, benötigen Sie V3.10.58.120 oder höher.
1. **Vorvalidierung:** Wenn ein Administrator ein Upgrade initiiert, führt das System eine Vorabvalidierungsoperation für jede Entität aus, die den Kern der Project Operations-Lösung bildet. Dieser Schritt überprüft, ob alle Entitätsreferenzen gültig sind und stellt sicher, dass Daten, die sich auf den PSP beziehen, innerhalb der veröffentlichten Grenzen von Project for the Web liegen.
1. **Metadaten-Upgrade:** Nach erfolgreicher Vorabvalidierung initiiert das System Änderungen am Schema und erstellt eine veraltete Komponentenlösung. Sie können diese veraltete Lösung entfernen, nachdem Sie alle erforderlichen Umgestaltungen von Anpassungen abgeschlossen haben. Dieser Schritt ist der längste Teil des Upgrade-Prozesses und kann bis zu vier Stunden dauern.
1. **Datenupgrade:** Nachdem alle erforderlichen Schemaänderungen im Metadaten-Upgrade-Schritt abgeschlossen wurden, werden Ihre Daten in das neue Schema migriert und alle erforderlichen Standardeinstellungen und Neuberechnungen werden durchgeführt.
1. **Update der Projektplan-Engine:** Nach erfolgreicher Datenaktualisierung wird die Registerkarte **Zeitlicher Ablauf** auf der Hauptseite in **Aufgaben** umbenannt. Wenn ein Benutzer diese Registerkarte nach dem Upgrade auswählt, wird er angewiesen, zum Verfolgungsraster zu navigieren, um eine schreibgeschützte Version des PSP anzuzeigen. Um den PSP zu bearbeiten, müssen sie den Zeitplan [Umwandlungsprozess](/PSA-Upgrade-Project-Conversion.md) initiieren. Alle Projekte ohne bereits vorhandenen PSP können die neue Planungserfahrung direkt und ohne Konvertierung verwenden.
 
### <a name="validate-common-scenarios"></a>Allgemeine Szenarien validieren

Wenn Sie Ihre spezifischen Anpassungen validieren, empfehlen wir Ihnen, auch die Geschäftsprozesse zu überprüfen, die von den Anwendungen unterstützt werden. Zu diesen Geschäftsprozessen gehören unter anderem die Erstellung von Verkaufsentitäten wie Angeboten und Verträgen sowie die Erstellung von Projekten, die PSPs und die Genehmigung von Ist-Werten enthalten.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Wesentliche Änderungen zwischen Project Service Automation und Project Operations

Dieser Abschnitt enthält eine Zusammenfassung der wichtigsten Änderungen, die Sie zwischen Project Service Automation und Project Operations erwarten können.

### <a name="project-planning"></a>Projektplanung

Die Projektplanungsfunktionen in Project Operations basieren nicht mehr auf einer Kombination aus clientseitiger Logik und serverseitiger Logik. Project Operations verwendet stattdessen Project for the Web als primäres Planungsmodul. Diese Änderung der Planungsfunktionen ermöglicht mehrere neue Funktionen wie Board- und Gantt-Ansichten, ressourcengesteuerte Planung, [Prüflistenelemente für die Aufgabe](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) und Projektplanungsmodi. Die neuen Planungsfunktionen werden auch durch eine Vielzahl neuer [Anwendungsprogrammierschnittstellen (APIs)](../project-management/schedule-api-preview.md) unterstützt. Diese APIs sollen sicherstellen, dass keine programmgesteuerten Operationen zum Erstellen, Aktualisieren oder Löschen einer Entität im PSP die berechneten Felder im Zeitplan beschädigen.

### <a name="billing-and-pricing"></a>Preise und Abrechnung

Als Teil der kontinuierlichen Investitionen in Project Operations stehen mehrere neue Funktionen in den Bereichen Abrechnung und Preisgestaltung zur Verfügung. Hier sehen Sie einige Beispiele:

- [Materialverbrauch für Projekte und Projektaufgaben erfassen](../material/material-usage-log.md)
- [Fremdarbeitsverwaltung](../pro/subcontracting/managing-subcontracts-overview.md)
- [Vorauszahlungen oder auf dem Vorbehalt basierende Verträge](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status und Validierungen des Vertrags, die nicht überschritten werden dürfen](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Aufgabenbasierte Abrechnung

### <a name="resource-management"></a>Ressourcenverwaltung

Project Operations bietet optionale Unterstützung für den Universal Resource Scheduling (URS) Tableau- und Zeitplanungsassistent. Diese neue Erfahrung wird im Zyklus im April 2023 obligatorisch.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Welche Bereitstellungstypen werden derzeit für das Upgrade unterstützt?

| Source                                                 | Zielsprache                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite-Bereitstellung                        | Unterstützt               |
| Projektmanagement und -buchhaltung in Dynamics 365 Finance | Project Operations Lite-Bereitstellung                        | Aktuell nicht unterstützt |
| Finance Projektmanagement und -buchhaltung              | Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen     | Aktuell nicht unterstützt |
| Project Service Automation 3.x                         | Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen     | Aktuell nicht unterstützt |
| Project for the Web (dedizierte Umgebung)            | Project Operations Lite-Bereitstellung                        | Aktuell nicht unterstützt |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Wie kann ich Project Operations installieren, bevor die Upgrade-Tools verfügbar sind?

Es gibt zwei Optionen für die Installation von Project Operations, bevor die Upgrade-Tools verfügbar sind:

- Eine neue Umgebung bereitstellen.
- Stellen Sie Project Operations separat für jede Vertriebsorganisation bereit, in der Project Service Automation nicht vorhanden ist.

Wenn Project Service Automation in einer Organisation installiert ist, aber nicht verwendet wurde, kann es deinstalliert werden. Nachdem Sie Project Service Automation vollständig entfernt haben, kann Project Operations in derselben Organisation installiert werden.
