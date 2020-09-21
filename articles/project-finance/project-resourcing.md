---
title: Projektressourcen
description: Dieses Thema enthält Informationen zu den Projektressourcen.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3716479"
---
# <a name="project-resourcing"></a>Projektressourcen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den Projektressourcen.

Eine Herausforderung für Projektmanager und Ressourcenmanager während der Projektplanungsphase ist die Ressourcenzuweisung, bei der sie die richtige Ressource für die Arbeit an einem Projekt ermitteln und reservieren müssen. In Dynamics 365 Finance können Sie Ressourcen-Funktionen für Projekte für Rollen definieren, die als temporäre Ressourcen behandelt werden, die für ein bestimmtes Engagement oder einen Teil eines Engagements reserviert werden können. Mit dieser Art der Beschaffung können Projektmanager und Ressourcenmanager die folgenden Aufgaben ausführen:

- Definieren Sie eine Rolle mit den erforderlichen Kompetenzen, damit die Ressourcen leicht zugeordnet werden können.
- Verwenden Sie Rollen, um einen anfänglichen Kundenbindungs-Zeitplan zu definieren, der auf reservierten Ressourcen basiert.
- Schätzen Sie die Kosten und legen Sie ein anfängliches Budget fest, basierend auf den zugewiesenen Rollen und Ressourcen für ein Projekt.
- Verwenden Sie Rollen, um die Anzahl der Ressourcenreservierungen zu schätzen, die für jedes Engagement erforderlich sind.
- Schätzen Sie die Anzahl der Ressourcen, die für den gesamten Lebenszyklus eines Projekts benötigt werden.
- Erstellen Sie einen Projektstrukturplan (PSP) unter Verwendung der anfänglichen Ressourcenzuweisungen.

[![Projektlebenszyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Mit fortschreitender Projektplanung können geplante Ressourcen durch besetzte Ressourcen ersetzt werden. Der Projektmanager kann auch zurückgehen und die Ressourcenreservierungen während jeder Projektphase aktualisieren.

## <a name="set-up-project-resources"></a>Projektressourcen einrichten
Sie müssen einen Kalender einrichten und ihn einem Mitarbeiter oder einem Mitarbeiter zuordnen. Der Kalender wird verwendet, um das Projekt und die Arbeitszeit der Ressourcen zu planen, die für das Projekt reserviert sind. Während der Kalendereinrichtung können Projektmanager im Rahmen der Ressourcenoptimierung eine Ressourcenebene erstellen. Basierend auf dem Kalenderzeitplan können Einschränkungen für Ressourcen festgelegt werden. Sie können einen Kalender auf der Seite **Kalender** einrichten.

Wenn Sie einen Mitarbeiter als Projektressource einrichten, können Sie aus Mitarbeitern auswählen, die in dem Unternehmen arbeiten, für das Sie Ressourcen einrichten. Alternativ können Sie Arbeiter aus anderen Unternehmen für Ihre Organisation auswählen. Diese Mitarbeiter werden als konzerninterne Ressourcen bezeichnet.

In den folgenden Verfahren wird erläutert, wie Sie einen Worker als Projektressource in Ihrem Unternehmen einrichten und eine konzerninterne Projektressource einrichten.

### <a name="set-up-a-worker-as-a-project-resource"></a>Richten Sie einen Worker als Projektressource ein

1. Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, den Sie als Projektressource hinzufügen, und öffnen Sie den Worker-Datensatz.
2. Wählen Sie im Aktionsbereich **Projekt** &gt; **Einrichtung** &gt; **Projekt einrichten**.
3. Wählen Sie einen Kalender aus, und schließen Sie die Seite.

Sie können auch Standardprojekte für eine Ressource als eine Art Vorzuweisung angeben. Vorabzuweisungen können verwendet werden, wenn der Ressourcenmanager oder Projektmanager im Voraus weiß, an welchen Projekten die Ressource arbeiten wird. Vorabzuweisungen können auch auf Anfrage eines Projektsponsors oder Kunden erfolgen. Um ein Projekt vorab zuzuweisen, klicken Sie auf die Seite **Projekte zuweisen** auf der Registerkarte **Projekte** in der Liste **Verbleibende Projekte** und wählen Sie das entsprechende Projekt.

### <a name="set-up-an-intercompany-resource"></a>Richten Sie eine Intercompany-Ressource ein

Wenn Sie einen Mitarbeiter als konzerninterne Ressource einrichten, müssen Sie die Einrichtung sowohl im Kreditunternehmen als auch im Kreditunternehmen abschließen.

**In der Kreditgesellschaft**

1. Vergewissern Sie sich unter Finanzen, dass das Kreditunternehmen ausgewählt ist, und führen Sie dann den Vorgang im vorherigen Abschnitt Einrichten eines Arbeitnehmers als Projektressource aus.
2. Klicken Sie auf der Seite **Intercompany-Buchhaltung** auf **Neu**.
3. In dem Feld **ID der juristischen Person** wählen Sie das kreditgebende Unternehmen aus. Füllen Sie die verbleibenden Felder aus, und klicken Sie dann auf **Speichern**.
4. Wählen Sie auf der Seite **Übertragungspreis** die Option **Neu** aus.
5. In dem Feld **Kreditgebende juristische Person** wählen Sie das entsprechende Unternehmen aus.
6. Um dem Kreditnehmer nur die Ressource zu verleihen, die Sie am Anfang dieses Abschnitts erstellt haben, wählen Sie im Feld **Ressource** den Namen der Ressource aus, die Sie erstellt haben. Um alle Ressourcen des kreditgebenden Unternehmens dem Kreditunternehmen zur Verfügung zu stellen, lassen Sie das Feld **Ressource** leer.
7. Auf der Seite **Projektmanagement- und Buchhaltungsparameter** auf der Registerkarte **Intercompany** legen Sie Option **Aktivieren Sie die unternehmensübergreifende Ressourcenplanung und Arbeitszeittabellen** auf **Ja** fest.

**Im Kreditunternehmen**

- Auf der Seite **Ressourcenliste** geben Sie im Suchfilter auf der Seite den Namen der Ressource ein, die Sie für das kreditgebende Unternehmen erstellt haben, um zu überprüfen, ob der Name in der Ressourcenliste des kreditgebenden Unternehmens enthalten ist.

## <a name="manage-resource-competencies"></a>Ressourcenanforderungskompetenzen verwalten
Ressourcenkompetenzen sind ein wesentlicher Bestandteil des Ressourcenmanagements. Kompetenzen können als Grundlage verwendet werden, um Ressourcen zu bestimmen, die das richtige Gleichgewicht zwischen Fähigkeiten, Ausbildung, Zertifizierung und Projekterfahrung aufweisen. Sie sollten diese Informationen für jede Ressource einrichten und regelmäßig aktualisieren. Auf diese Weise können Sie die Funktionen maximieren, wenn bestimmte Ressourcenkompetenzen während der Projektressourcenzuweisung übereinstimmen.

[![Beispiele für Fähigkeiten, Zertifizierungen, Ausbildung und Projekterfahrung](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

In den folgenden Verfahren wird erläutert, wie Sie einige der Kompetenzen für eine Ressource einrichten.

Um Kompetenzen für einen Mitarbeiter einzurichten, können Sie entweder die Listenseite **Arbeitskräfte** in der Personalabteilung oder der Listenseite **Ressourcen** in Projektmanagement und Buchhaltung verwenden. Für die folgenden Verfahren wird die Listenseite **Arbeitskräfte** in der Personalabteilung verwendet.

### <a name="set-up-competencies-certificates"></a>Kompetenzen einrichten: Zertifikate

1. Auf der Listenseite **Arbeitskräfte** wählen Sie die Zeile aus, für die der Worker Zertifikatinformationen hinzufügen soll.
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Worker** in der Gruppe **Kompetenzen** die Option **Zertifikat** aus.
3. Wählen Sie **Neu** und dann im Feld **Zertifikatstyp** wählen Sie **PMP** aus.
4. In dem Feld **Anfangsdatum** wählen Sie **01.10.2015** und dann **speichern**.

### <a name="set-up-competencies-skills"></a>Kompetenzen einrichten: Fähigkeiten

1. Auf der Listenseite **Workers** stellen Sie sicher, dass der Worker, den Sie im vorherigen Verfahren verwendet haben, noch ausgewählt ist. Wählen Sie im Aktionsbereich auf der Registerkarte **Worker** in der Gruppe **Kompetenzen** die Option **Fähigkeiten** aus.
2. Wählen Sie **Neu**.
3. In dem Feld **Fertigkeit** wählen Sie **Projektmanagement**.
4. Wählen Sie im Feld **Ebene** die Option **5 Experte** aus.
5. Wählen Sie im Feld **Ebenendatum** die Option **14.1.2014** aus.
6. Geben Sie in das Feld **Erfahrung in Jahren** **10** ein.
7. Wählen Sie **Speichern** aus, und schließen Sie die Seite.

## <a name="create-a-new-project"></a>Ein neues Projekt erstellen
1. Auf der Seite **Projektverwaltung** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:

    - **Projekttyp:** Zeit und Material
    - **Projektname:** XYZ-Upgrade-Phase 2
    - **Projektgruppe** TM\_WIP
    - **Projektvertrags-ID** 00000002

2. Wählen Sie **Projekt erstellen** aus.

### <a name="assign-a-resource-to-a-project"></a>Eine Ressource einem Projekt zuweisen

1. Auf der **Workers** Seite, in der **Workers** Liste, wählen Sie den Worker aus, für den Sie zuvor Kompetenzen eingerichtet haben und öffnen Sie den Worker-Datensatz.
2. Wählen Sie im Aktionsbereich auf der Registerkarte **Projekt** in der Gruppe **Einrichten** die Option **Projekt zuweisen** aus.
3. Auf der Seite **Projektzuweisungen für die Ressourcenvalidierung** auf der Registerkarte **Projekte** im Feld **Fügen Sie das Projekt ausgewählten Projekten hinzu** Filter auf das Projekt **XYZ-Upgrade-Phase 2**.
4. In dem Bereich **Verbleibende Projekte** wählen Sie ein Projekt aus und klicken Sie dann auf die Pfeilschaltfläche, um es dem Bereich **Ausgewählte Projekte** hinzuzufügen.

Sie können nach Bedarf auch Kategorien für eine Ressource zuweisen. Der Kategorietyp ist entweder **Kosten** oder **Umsatz**. Der Kategorietyp wird von Ihrer Organisation festgelegt. Wenn für eine Ressource keine Kategorien zugewiesen sind, sucht Finance die Standardkategorie für Stundenpreise nach Kosten und Einnahmen.

### <a name="set-up-project-resource-and-role-characteristics"></a>Richten Sie Projektressourcen- und Rollenmerkmale ein

Ein Projektmanager kann die Projektresssourcen-Funktion verwenden, um die für das Projekt erforderlichen Rollen zu erstellen. Rollen können verwendet werden, wenn bestätigte Ressourcen noch unbekannt sind, wenn Ressourcen reserviert werden. Rollen können vorübergehend als geplante Ressourcen reserviert werden, sodass Sie die Projektplanungsphase fortsetzen können.

[![Beispiel einer Rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Szenario:** Contoso wurde beauftragt, ein Zeit- und Materialprojekt mit einer genehmigten Projektcharta abzuschließen. Der Junior-Projektmanager schließt den Projektumfang noch ab. Der Ressourcenmanager identifiziert derzeit bestimmte Ressourcen, die für die Arbeit an dem neuen Projekt reserviert werden. Aufgrund der kritischen Natur des Projekts forderte der Projektsponsor den Senior-Projektmanager als eine der Rollen an. Der Ressourcenmanager muss die neue Ressource erwerben und die Rolle im System definieren, falls der Junior-Projektmanager die Ressourceninformationen während der Projektplanung benötigt.

Die folgenden Schritte zeigen, wie der Ressourcenmanager die Rolle des Senior-Projektmanagers einrichten und ihr Ressourcenmerkmale zuordnen kann. Später kann die Rolle verwendet werden, um nach verfügbaren Ressourcen zu suchen, die den erforderlichen Ressourcenkompetenzen entsprechen.

1. Auf der Seite **Rollen einrichten** wählen Sie **Neues Projekt** und geben die folgenden Werte ein:

    - **Rollen-ID:** Senior Projektmanager
    - **Beschreibung:** Senior Projektmanager

2. Wählen Sie **Erstellen** aus.
3. Wählen Sie die Rolle **Senior Projektmanager** aus und wählen Sie dann **Eigenschaften konfigurieren**.
4. In dem Feld **Eigenschaftentyp** wählen Sie **Fertigkeit**.
5. In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld die Fertigkeit ein, nach der gesucht werden soll.
6. In dem Feld **Eigenschaftentyp** wählen Sie **Zertifikat**.
7. In dem Feld **Verfügbare Eigenschaften** geben Sie in das Feld den Zertifikatstyp ein, nach dem gesucht werden soll.

### <a name="assign-a-project-resource-to-a-project"></a>Eine Projektressource einem Projekt zuweisen

1. Auf der Seite **Alle Projekte** wählen Sie das Projekt **XYZ-Upgrade-Phase 2** aus.
2. Auf der Registerkarte **Projektteam und Terminplanung** wählen Sie **Hinzufügen** aus.
3. In dem Feld **Rolle** wählen Sie **Teammitglied**.
4. Wählen Sie **Aus Kalender buchen** aus.
5. Auf der Seite **Verfügbarkeit von Ressourcen** wählen Sie **Einstellungen anzeigen**.
6. Auf der Seite **Passen Sie die Einstellungen an** geben Sie die folgenden Werte ein:

    - **Format für die Datumsbereichsansicht:** Tag
    - **Verfügbarkeitsbeschreibungen anzeigen:** Ja
    - **Restkapazität anzeigen:** Ja

7. Wählen Sie eine Ressource in der Liste der buchbaren Ressourcen aus.
8. Wählen Sie **Hartes Buch** und **Volle Kapazität** aus.


### <a name="assign-a-resource-to-a-default-role"></a>Zuweisen einer Ressource einer Standardrolle

Um Projekt- oder Ressourcenmanagern zu helfen, können Sie Drilldown zu den Ressourcen ausführen, die für ein Projekt reserviert werden können. Sie können einer vorhandenen Ressource oder einer neu erworbenen Ressource einer Standardrolle zuordnen. Als Daniel zum Beispiel eingestellt wurde, verfügte er über die Erfahrung und die Fähigkeiten, um die Rolle des Business Analyst zu übernehmen. Der Ressourcenmanager hat diese Rolle als Daniels Standardrolle zugewiesen. Aus diesem Grund hat der Ressourcenmanager Daniel zu einem Pool von Geschäftsanalysten hinzugefügt, die für die Arbeit an Projekten zur Verfügung stehen.

Während der Ressourcenreservierung können Projektmanager die Rollenressourcen filtern, die für die Arbeit an Projekten verfügbar sind. Sie können diese Informationen als ein Kriterium verwenden, wenn sie während der Ressourcenerfüllung eine Entscheidungsanalyse mit mehreren Kriterien durchführen. Sie können dem Filter auch andere Ressourcenmerkmale hinzufügen, um nach Ressourcen zu suchen, die über bestimmte Fähigkeiten, Ausbildung und Erfahrung für ein bestimmtes Projekt verfügen.

**Szenario:** Ein genehmigtes Projekt wurde gestartet, und die Rolle des Senior-Projektmanagers wurde während der Projektplanungsphase als geplante Ressource reserviert. Der Ressourcenmanager hat jetzt eine Ressource erworben, um die Rolle des Senior-Projektmanagers zu erfüllen.

1. Auf der Seite **Ressourcenliste** wählen Sie **Daniel Goldschmidt**.
2. Auf der Seite **Rollenressourcen** wählen Sie **Neu** und geben die folgenden Werte ein:

    - **Wirksam:** Geben Sie das aktuelle Datum ein.
    - **Ablauf:** Geben Sie **Nie** ein.
    - **Rolle:** Geben Sie **Senior Project Manager** ein.

3. Wählen Sie **Speichern** aus, und schließen Sie die Seite.
4. Auf der Registerkarte **Kompetenzen** fügen Sie die Fertigkeit **ProjectMgmt** und **PMP** Zertifikat hinzu.

## <a name="set-up-role-based-pricing"></a>Einrichten der rollenbasierten Preise
Alle Kosten-, Verkaufs- und Transferpreise können für Rollen eingerichtet werden.

1. Auf der Seite **Verkaufspreis (Stunde)** wählen Sie **Neu** und geben Sie ein Datum des Inkrafttretens ein.
2. Wählen Sie in der Spalte **Rolle** eine Rolle aus.
3. In der Spalte **Preise** geben Sie in dieser Spalte einen Preis für die ausgewählte Ressourcenrolle ein.

## <a name="form-a-project-team"></a>Stellen Sie ein Projektteam zusammen
Um die Rollen zu verwenden, die zuvor in einem Projekt eingerichtet wurden, muss ein Projektmanager die Rollen dem Projekt zuordnen. Für ein Projekt können mehrere Rollen zugewiesen werden. Um Verwirrung zu vermeiden, werden diese Rollen während der Reservierung automatisch gekennzeichnet. Wenn der Projektmanager beispielsweise drei Softwareentwickler und drei Softwareentwicklerrollen benötigt wie **Softwareentwickler 1**, **Softwareentwickler 2** und **Softwareentwickler 3**, werden ihre Beschriftungen automatisch generiert werden. Wenn zuvor Rollenmerkmale für die Rolle festgelegt wurden, werden sie bei der Suche nach einer Ressource als Filter angewendet. Bei Bedarf können zusätzliche Merkmale hinzugefügt werden, um die Suche weiter zu verfeinern.

Die Ansichtseinstellungen können auch angepasst werden, um eine bessere Ansicht der Ressourcenverfügbarkeit zu erhalten. Es gibt Optionen zur Anzeige der stündlichen, täglichen, wöchentlichen, monatlichen, vierteljährlichen und jährlichen Verfügbarkeit. Es besteht auch die Option, die verfügbare und verbleibende Kapazität der Ressourcen anzuzeigen. Diese Option ist nützlich für die Zeitverwaltung, wenn Sie die verfügbare Zeit für Aktivitäten oder die Verfügbarkeit von Ressourcen schätzen.

Der Projektmanager kann eine Rolle auf der Seite auswählen und dann, wenn eine Ressource verfügbar ist, die der Anforderung entspricht, eine Ressource reservieren, um die Rolle zu füllen. Beachten Sie, dass die Ressourcen zu diesem Zeitpunkt in der Planungsphase nicht reserviert werden müssen. Wenn Sie einen PSP erstellen, können Sie Rollen durch besetzte Ressourcen für das Projekt ersetzen. Wenn Rollen im PSP durch besetzte Ressourcen ersetzt werden, aktualisiert das Ressourcen-Setup automatisch die Liste und Planung des Projektteams.

[![Projektteamliste, die sowohl Rollen als auch tatsächliche Ressourcen enthält](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Der Projektmanager hat verschiedene Möglichkeiten, eine Ressource für ein Projekt zu buchen, wie **Verbleibende Kapazität**, **Volle Kapazität**, **Kapazitätsprozentsatz**, und **Stunden definieren**. Diese Buchungsoptionen können jederzeit storniert werden, wenn sich die Ressourcenzuweisungen ändern. Es werden zwei Arten der Buchung unterstützt:

- **Verbindlich buchen** – Die Ressourcenreservierung wurde genehmigt und bestätigt, um für die angegebene Dauer an dem Auftrag zu arbeiten.
- **Unverbindlich buchen** – Die Ressourcenreservierung wurde genehmigt und bestätigt, um für die angegebene Dauer an dem Auftrag zu arbeiten.

Der folgende Prozess erläutert, wie Sie ein Projektteam erstellen.

### <a name="create-a-project-team"></a>Ein Projektteam erstellen

1. Auf der **Alle Projekte** Listenseite, wählen Sie ein Projekt aus und wählen Sie dann **Bearbeiten**.
2. Auf der Registerkarte **Projektteam und Zeitplan** im Feld **Planen Sie das Enddatum** geben Sie im Feld das Startdatum des Zeitplans plus einen Monat ein. Wenn das Startdatum des Zeitplans beispielsweise der 24. Juni 2017 (24.06.2017) ist, geben Sie Folgendes ein **24/07/2017**.
3. Wählen Sie **Hinzufügen**.
4. In dem Bereich **Fügen Sie dem Projekt Rollen hinzu** geben Sie im Feld **Rolle** ein und wählen **Senior Projektmanager**.
5. Wählen Sie **Erforderliche Kompetenzen**.
6. Auf der Seite **Wählen Sie Eigenschaften** werden die Merkmale, die Sie zuvor für den Senior-Projektmanager festgelegt haben, standardmäßig die Merkmale ausgewählt, die Sie zuvor für die Rolle des Senior-Projektmanagers festgelegt haben. Klicken Sie auf **OK**.
7. Auf der Seite **Fügen Sie dem Projekt Rollen hinzu** im Feld **Anzahl der Ressourcen** geben Sie **1** ein.
8. In dem Feld **Ressource** zeigt die Suche alle Ressourcen, die die erforderlichen Kompetenzen haben. Wählen Sie **Daniel Goldschmidt** und dann **erstellen** aus.
9. Auf der Seite **Projekt** wählen Sie **Hinzufügen** aus.
10. In dem Bereich **Fügen Sie dem Projekt Rollen hinzu** und wählen Sie im Feld **Rolle** **Teammitglied** aus. Geben Sie **5** im Feld **Anzahl der Ressourcen** ein.
11. Wählen Sie **Erstellen** aus.
12. Auf der Seite **Projekte** wählen Sie **Ressource erfüllen**.

## <a name="resource-capacity-synchronization"></a>Synchronisation der Kapazität einer Ressource
Die Prozesse für die Ressourcensynchronisierung stellen sicher, dass Informationen für den Kalender und den Basiskalender in die Projektressourcenplanung einfließen. Wenn der Kalender geändert wird, nehmen die Prozesse die erforderlichen Aktualisierungen an der Planung der Projektressourcen vor. Die Prozesse tragen auch zur Verbesserung der Leistung bei, da die Ressourceninformationen des Kalenders im Voraus synchronisiert werden. Daher werden Aktualisierungen der Ressourcenzeitplanungsinformationen schneller durchgeführt. Wir empfehlen, dass Sie die Prozesse als Stapel anstatt einzeln planen. Andernfalls besteht die Gefahr, dass jemand die Inklusivdaten vergisst, an denen die Informationen zuletzt synchronisiert wurden. Wenn keine Inklusivdaten verwendet werden, können während der Datumssynchronisierung Lücken auftreten.

![Kalendersynchronisation](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synchronisation der Rollup-Kapazität

Der Synchronisierungsprozess dient zum Synchronisieren aller Ressourcenkalenderinformationen. Diese Informationen enthalten Basiskalenderinformationen zu Änderungen an der Kapazitätstabelle des Ressourcenkalenders des Projekts. Wenn dem Projekt neue Ressourcen hinzugefügt werden, stellt die Synchronisierung sicher, dass die aktualisierten Kalenderinformationen verfügbar sind. Diese Synchronisation kann jederzeit durchgeführt werden.

Es wird empfohlen, dass Sie einen Batch verwenden. Die Optionen stehen während der Synchronisierung von Kapazitätsreservierungen zur Verfügung.

1. Wählen Sie **Projektmanagement und Buchhaltung** &gt; **Periodisch** &gt; **Kapazitätssynchronisation** &gt; **Synchronisieren Sie Rollups der Ressourcenkapazität**.
2. Legen Sie die Optionen in der nachfolgenden Tabelle fest.

    | Option      | Beschreibung |
    |-------------|-------------|
    | Periodencode | Wählen Sie optional den Intervallcode für das Hauptbuchdatum aus, um das Start- und Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität festzulegen. |
    | Startdatum  | Geben Sie das Startdatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein. |
    | Enddatum    | Geben Sie das Enddatum für den Synchronisierungsprozess für Rollups der Ressourcenkapazität ein. |

[![Synchronisierungsprozess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Richten Sie Rollen in PSP-Vorlagen ein
Projektmanager können PSP-Vorlagen einrichten, die sie beim Erstellen eines PSP für neue Projekte anwenden können. Projektmanager können beim Erstellen einer Vorlage Rollen hinzufügen. Gehen Sie wie folgt vor, um einer PSP-Vorlage eine Rolle zuzuweisen.

1. Wählen Sie **Projektmanagement und Buchhaltung** &gt; **Einrichtung** &gt; **Projekte** &gt; **Vorlagen für Projektstrukturpläne**.
2. Wählen Sie **Einzelheiten** für eine ausgewählte PSP-Vorlage.
3. Wählen Sie eine Aufgabe in der Liste und dann im Feld **Rolle** wählen Sie eine Rolle aus, die der Aufgabe zugewiesen werden soll.

### <a name="work-with-a-wbs"></a>Mit einem PSP arbeiten

Sie können einen neuen PSP erstellen oder einen PSP aus einer vorhandenen PSP-Vorlage kopieren. Ein Projektmanager kann die Ressourcen einfach verwalten, indem er neuen Aufgaben im PSP Rollen zuweist. Rollen können entweder nach dem Erwerb einer Ressource oder nach der Identifizierung einer bestätigten Ressource für die Bearbeitung der Aufgabe ersetzt werden. Mit dieser Flexibilität können Projektmanager die folgenden Aufgaben ausführen:

- Identifizieren Sie die Anzahl der Ressourcen, die für PSP-Arbeitspakete erforderlich sind.
- Projektkosten schätzen.
- Bestimmen Sie ein vorläufiges Budget.
- Schätzen Sie die Aktivitätsdauer basierend auf Rollen und Ressourcen.
- Entwickeln Sie einige Projektmanagementpläne basierend auf den verfügbaren Projektinformationen.

Im PSP wurden zusätzliche Optionen hinzugefügt, um so die Ressourcing-Funktionalität besser nutzen zu können.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressourcenzuweisungen</td>
<td>Zeigen Sie die zugewiesenen Ressourcen, Daten, Anzahl Stunden und den Buchungstyp für Aufgaben im PSP an.</td>
</tr>
<tr class="even">
<td>Team automatisch generieren</td>
<td>Fügen Sie geplante Ressourcen automatisch hinzu, indem Sie Rollen verwenden, die einer Aufgabe zugeordnet sind. Finance schlägt automatisch die geplanten Ressourcen vor, indem eine Entscheidungsanalyse mit mehreren Kriterien verwendet wird, die auf Rollen basiert. Nachdem die Rollen und der Aufwand (Stunden) für die Aufgaben in einem PSP festgelegt wurden und nachdem die Struktur freigegeben wurde, wählen Sie <strong>Team automatisch generieren</strong> aus. Die erforderliche Anzahl geplanter Ressourcen wird dem PSP und der Registerkarte <strong>Projekt- und Teamzeitplanung</strong> hinzugefügt.</td>
</tr>
<tr class="odd">
<td>Ressourcen (Dropdownliste)</td>
<td>Auf der Seite <strong>Starten Sie die Ressourcenzuweisung</strong> können Sie Ressourcen für verbindliche oder unverbindliche Buchungen auswählen, basierend auf der angegebenen Dauer. Sie können die Ansichtseinstellungen anpassen, um die Dauer der Ressourcenaktivitäten anzuzeigen und festzulegen. Mit den folgenden Optionen können Sie Ressourcen auf Arbeitspaketebene auswählen und zuweisen:
<ul>
<li><strong>Akzeptieren</strong> – Bestätigen Sie die Änderungen an der Ressource, die einer Aufgabe zugewiesen ist.</li>
<li><strong>Abbrechen</strong> –Brechen Sie die Änderungen an der Ressource ab, die einer Aufgabe zugewiesen sind.</li>
<li><strong>Automatisch zuweisen</strong> – Eine verfügbare besetzte Ressource mit einer passenden Rolle wird automatisch ausgewählt und der ausgewählten Aufgabe zugewiesen.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Auf der Seite **Alle Projekte** wählen Sie das Projekt **XYZ-Upgrade-Phase 2** aus.
2. Wählen Sie **Planen** &gt; **Aktivitäten** &gt; **Projektstrukturplan**.
3. Wählen Sie **Neu**. um dem PSP die folgenden Aktivitäten der ersten Ebene hinzuzufügen:

    - Initiieren
    - Planung
    - Wird ausgeführt
    - Überwachung und Steuerung
    - Schließen

4. Stellen Sie die Daten und den Aufwand (Stunden) wie in der folgenden Abbildung gezeigt ein.

    [![Festlegen der Daten und des Aufwands](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Wählen Sie Aufgabenzeile **Initiieren** und dann im Feld **Rolle** wählen Sie **Senior Projektmanager** aus.
6. Wählen Sie **Veröffentlichen** aus.
7. In der gleichen Zeile im Feld **Ressource** wählen Sie **Daniel Goldschmidt** und dann **Akzeptieren**.
8. Wählen Sie die Aufgabenzeile **Planung** und dann im Feld **Rolle** wählen Sie **Business Analyst**.
9. Wählen Sie **Veröffentlichen** und dann **Team automatisch generieren**.
10. Klicken Sie im Meldungskästchen, das angezeigt wird und wählen Sie **Ja**.
11. In dem Feld **Ressource** überprüfen Sie, dass der Wert **Geschäftsanalyst 1** lautet.
12. Für die **Geschäftsanalyst 1** Ressource öffnen Sie die Suche und wählen Sie **Starten Sie Ressourcenzuweisungen**. Wählen Sie dann einen Mitarbeiter für die Aufgabe aus.
13. Wählen Sie **unverbindlich zuweisen** &gt; **Ganze Kapazität**.

    > [!NOTE] 
    > Sie erhalten keine Warnung, dass die angegebene Ressource jetzt 2 ist, da die Anzahl der Ressourcen 1 bleibt.

14. Auf der Seite **Projektstrukturplan** überprüfen Sie die Ressourcenzuweisung im PSP und wählen Sie dann **Speichern**.

## <a name="resource-fulfillment-for-planned-resources"></a>Ressourcenerfüllung für geplante Ressourcen
Ein Projektmanager kann die erforderlichen Ressourcenrollen für ein Projekt planen. Der Ressourcenmanager sieht diese geplanten Ressourcen als Anforderungen auf der Seite **Ressourcenerfüllung** und kann tatsächliche Ressourcen zuweisen.

1. Auf der Seite **Alle Projekte** wählen Sie das Projekt **XYZ-Upgrade-Phase 2** aus.
2. Wählen Sie **Projekt** und dann wählen Sie **Bearbeiten**.
3. Auf der Registerkarte **Projektteam und Terminplanung** wählen Sie **Hinzufügen** aus.
4. In dem Dialogfeld **Rollen hinzufügen** wählen Sie die Rolle **Softwareentwickler** aus.
5. Wählen Sie **Erstellen** und schließen Sie dann die Projektseite.
6. Auf der Seite **Ressourcenerfüllung** wählen Sie **Softwareentwickler 1** für das Projekt **XYZ-Upgrade-Projekt Phase 2**.
7. Wählen Sie einen Worker und wählen Sie dann **Zuweisen**.
8. Stellen Sie sicher, dass die Zeile für **Softwareentwickler 1** entfernt wurde für das Projekt **XYZ-Upgrade-Projekt Phase 2**.
9. Auf der Registerkarte **Projektteam und Terminplanung** für das Projekt **XYZ-Upgrade-Phase 2** überprüfen Sie im Projekt, ob der Worker, den Sie im vorherigen Schritt ausgewählt haben, als **Softwareentwickler** hinzugefügt wurde.

## <a name="requests-for-project-resources"></a>Anfragen nach Projektressourcen
Mit der Funktionalität für die Planung von Projektressourcen können Ressourcenmanager nur besetzte Ressourcen auf Aufträge oder Projekte verteilen. Um diese Funktionalität zu aktivieren, führen Sie die folgenden Aufgaben aus oder überprüfen Sie, ob sie abgeschlossen wurden:

- Nummernserien einrichten.
- Projektmanagement- und Buchhaltungsworkflows einrichten.
- Aktivieren Sie Workflows für Ressourcenanforderungen.

Nachdem die vorhergehenden Aufgaben abgeschlossen wurden, können Sie die folgenden Aufgaben nach Bedarf ausführen:

- Erstellen Sie eine Ressourcenanforderung aus einer mit Personal gebuchten Ressource.
- Ressourcenanforderungen überwachen.
- Erfüllen von Ressourcenanforderungen.
- Fordern Sie eine besetzte Ressource von einem PSP an.
- Buchen Sie Ressourcen für ein Projekt, ohne eine Personalressource anzufordern.

## <a name="monitor-project-teams"></a>Projektteams überwachen
1. Auf der Seite **Alle Projekte** wählen Sie die Verknüpfung **Projekt-ID** für das Projekt **XYZ Aktualisierung Phase 2**.
2. Auf der Registerkarte **Projektteam und Terminplanung** überprüfen Sie, ob die aufgelisteten Projektressourcen korrekt sind.
