---
title: Upgrade von Project Service Automation auf Project Operations
description: Dieses Thema bietet einen Überblick zum Upgradeprozess von Microsoft Dynamics 365 Project Service Automation auf Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: 3f31173197a3055cdc51567261dd91925fc9f430
ms.sourcegitcommit: bec7382d1319d59645e8e79fdb20df58617c97c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8626714"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Upgrade von Project Service Automation auf Project Operations

Wir freuen uns, die erste von drei Phasen für das Upgrade von Microsoft Dynamics 365 Project Service Automation auf Dynamics 365 Project Operations ankündigen zu können. Dieses Thema bietet einen Überblick für Kunden, die sich auf diese spannende Reise begeben. Zukünftige Themen werden Überlegungen von Entwicklern und Details zu Funktionsverbesserungen umfassen. Sie bieten nicht nur Anleitungen zur Vorbereitung Ihres Upgrades auf Project Operations, sondern erklären auch, was Sie nach dem Upgrade erwarten können.

Das Upgrade-Lieferprogramm wird in drei Phasen unterteilt.

| Upgrade-Lieferung | Phase 1 (Januar 2022) | Phase 2 (April-Zyklus 2022) | Phase 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Keine Abhängigkeit vom Projektstrukturplan (PSP) für Projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP innerhalb der derzeit unterstützten Grenzen von Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP außerhalb der derzeit unterstützten Grenzen von Project Operations, einschließlich der Unterstützung für den Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funktionen des Upgradeprozesses 

Als Teil des Upgradeprozesses haben wir der Siteübersicht Upgrade-Protokolle hinzugefügt, damit Administratoren Fehler leichter diagnostizieren können. Neben der neuen Schnittstelle werden neue Validierungsregeln hinzugefügt, um die Datenintegrität nach einem Upgrade sicherzustellen. Die folgenden Validierungen werden dem Upgrade-Prozess hinzugefügt.

| Prüfungen | Phase 1 (Januar 2022) | Phase 2 (April-Zyklus 2022) | Phase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| Der PSP wird auf gängige Datenintegritätsverletzungen überprüft (z. B. Ressourcenzuweisungen, die derselben übergeordneten Aufgabe zugeordnet sind, aber unterschiedliche übergeordnete Projekte aufweisen). | | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP wird gegen die [bekannten Grenzen von Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) validiert. | | :heavy_check_mark: | :heavy_check_mark: |
| Der PSP wird gegen die bekannten Grenzen von Project Desktop Client validiert. | |  | :heavy_check_mark: |
| Buchbare Ressourcen und Projektkalender werden anhand allgemeiner inkompatibler Kalenderregelausnahmen bewertet. | | :heavy_check_mark: | :heavy_check_mark: |

In Phase 2 werden bei Kunden, die auf Project Operations aktualisieren, die bestehenden Projekte auf eine schreibgeschützte Erfahrung für die Projektplanung aktualisiert. In dieser schreibgeschützten Umgebung wird der vollständige PSP im Verfolgungsraster angezeigt. Um den PSP zu bearbeiten, können Projektmanager **Konvertieren** auf der Hauptseite **Projekte** auswählen. Ein Hintergrundprozess aktualisiert dann das Projekt, sodass es die neue Projektplanungserfahrung von Project for the Web unterstützt. Diese Phase ist für Kunden geeignet, die Projekte haben, die in die [bekannten Grenzen von Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries) passen.

In Phase 3 wird die Unterstützung für den Project Desktop Client zum Vorteil der Kunden hinzugefügt, die ihre Projekte weiterhin von dieser Anwendung aus bearbeiten möchten. Wenn jedoch vorhandene Projekte in die neue Project for the Web-Erfahrung konvertiert werden, wird der Zugriff auf das Add-In für jedes konvertierte Projekt deaktiviert.

## <a name="prerequisites"></a>Anforderungen

Um für das Phase-1-Upgrade berechtigt zu sein, muss ein Kunde die folgenden Kriterien erfüllen:

- Die Zielumgebung darf keine Datensätze in der **msdyn_projecttask**-Entität enthalten.
- Allen aktiven Benutzern des Kunden müssen gültige Project Operations-Lizenzen zugewiesen werden. 
- Der Kunde muss den Upgrade-Prozess in mindestens einer Nicht-Produktionsumgebung validieren, die einen repräsentativen Datensatz hat, der mit Produktionsdaten abgeglichen ist.
- Die Zielumgebung muss auf Project Service Automation Update Release 41 (3.10.62.162) oder höher aktualisiert werden.

Die Voraussetzungen für Phase 2 und Phase 3 werden aktualisiert, wenn sich die allgemeinen Verfügbarkeitstermine nähern.

## <a name="licensing"></a>Lizenzierung

Wenn Sie über aktive Lizenzen für Project Service Automation verfügen, können Sie Project Operations installieren und verwenden, das alle Funktionen von Project Service Automation und mehr umfasst. Auf diese Weise können Sie die Fähigkeiten von Project Operations testen, während Sie Project Service Automation weiterhin in der Produktion verwenden. Nach Ablauf Ihrer Project Service Automation-Lizenzen müssen Sie zu Project Operations wechseln. Wenn Sie diesen Übergang planen, müssen Sie berücksichtigen, dass die Project Operations-Lizenz keine Project Service Automation-Lizenz enthält.

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

    > [!NOTE]
    > Je nach Datenmenge in der Umgebung kann das Upgrade mehrere Stunden dauern. Das Kernteam, das das Upgrade verwaltet, sollte entsprechend planen und das Upgrade außerhalb der Geschäftszeiten durchführen. In manchen Fällen sollte das Upgrade bei großem Datenvolumen am Wochenende durchgeführt werden. Die Entscheidung über die Planung sollte auf den Testergebnissen in niedrigeren Umgebungen basieren.

3. Aktualisieren Sie benutzerdefinierte Lösungen nach Bedarf. Stellen Sie an dieser Stelle alle Änderungen bereit, die Sie an Ihren Anpassungen im Abschnitt [Testen und Umgestaltung von Anpassungen](#testing-and-refactoring-customizations) dieses Themas vorgenommen haben.
4. Gehen Sie zu **Einstellungen** \> **Lösungen** und wählen Sie zum Deinstallieren die Lösung **Project Operations Veraltete Komponenten**.

    Diese Lösung ist eine temporäre Lösung, die das vorhandene Datenmodell und die Komponenten enthält, die während des Upgrades vorhanden sind. Durch das Entfernen dieser Lösung entfernen Sie alle Felder und Komponenten, die nicht mehr verwendet werden. Auf diese Weise tragen Sie dazu bei, die Schnittstelle zu vereinfachen und die Integration und Erweiterung zu erleichtern.
    
### <a name="validate-common-scenarios"></a>Allgemeine Szenarien validieren

Wenn Sie Ihre spezifischen Anpassungen validieren, empfehlen wir Ihnen, auch die Geschäftsprozesse zu überprüfen, die von den Anwendungen unterstützt werden. Zu diesen Geschäftsprozessen gehören unter anderem die Erstellung von Verkaufsentitäten wie Angeboten und Verträgen sowie die Erstellung von Projekten, die PSPs und die Genehmigung von Ist-Werten enthalten.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Wesentliche Änderungen zwischen Project Service Automation und Project Operations

Dieser Abschnitt enthält eine Zusammenfassung der wichtigsten Änderungen, die Sie zwischen Project Service Automation und Project Operations erwarten können.

### <a name="project-planning"></a>Projektplanung

Die Projektplanungsfunktionen in Project Operations basieren nicht mehr auf einer Kombination aus clientseitiger Logik und serverseitiger Logik. Project Operations verwendet stattdessen Project for the Web als primäres Planungsmodul. Diese Änderung der Planungsfunktionen ermöglicht mehrere neue Funktionen wie Board- und Gantt-Ansichten, ressourcengesteuerte Planung, [Prüflistenelemente für die Aufgabe](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) und Projektplanungsmodi. Die neuen Planungsfunktionen werden auch durch eine Vielzahl neuer [Anwendungsprogrammierschnittstellen (APIs)](../project-management/schedule-api-preview.md) unterstützt. Diese APIs sollen sicherstellen, dass keine programmgesteuerten Operationen zum Erstellen, Aktualisieren oder Löschen einer Entität im PSP die berechneten Felder im Zeitplan beschädigen.

## <a name="billing-and-pricing"></a>Preise und Abrechnung

Als Teil der kontinuierlichen Investitionen in Project Operations stehen mehrere neue Funktionen in den Bereichen Abrechnung und Preisgestaltung zur Verfügung. Hier sehen Sie einige Beispiele:

- [Materialverbrauch für Projekte und Projektaufgaben erfassen](../material/material-usage-log.md)
- [Fremdarbeitsverwaltung](../pro/subcontracting/managing-subcontracts-overview.md)
- [Vorauszahlungen oder auf dem Vorbehalt basierende Verträge](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status und Validierungen des Vertrags, die nicht überschritten werden dürfen](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Aufgabenbasierte Abrechnung

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Welche Bereitstellungstypen werden derzeit für das Upgrade unterstützt?

| Source                                                 | Zielsprache                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite-Bereitstellung                        | Unterstützt               |
| Projektmanagement und -buchhaltung in Dynamics 365 Finance | Project Operations Lite-Bereitstellung                        | Aktuell nicht unterstützt |
| Finance Projektmanagement und -buchhaltung              | Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen     | Aktuell nicht unterstützt |
| Finance Projektmanagement und -buchhaltung              | Project Operations für Szenarien basierend auf vorrätigen Ressourcen/Fertigungsaufträgen | Aktuell nicht unterstützt |
| Project Service Automation 3.x                         | Project Operations für Szenarien basierend auf vorrätigen/nicht vorrätigen Ressourcen     | Aktuell nicht unterstützt |
| Project for the Web (dedizierte Umgebung)            | Project Operations Lite-Bereitstellung                        | Aktuell nicht unterstützt |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Wie kann ich Project Operations installieren, bevor die Upgrade-Tools verfügbar sind?

Es gibt zwei Optionen für die Installation von Project Operations, bevor die Upgrade-Tools verfügbar sind:

- Eine neue Umgebung bereitstellen.
- Stellen Sie Project Operations separat für jede Vertriebsorganisation bereit, in der Project Service Automation nicht vorhanden ist.

> [!NOTE]
> Wenn Project Service Automation in einer Organisation installiert ist, aber nicht verwendet wurde, kann es deinstalliert werden. Nachdem Sie Project Service Automation vollständig entfernt haben, kann Project Operations in derselben Organisation installiert werden.
