---
title: Projektstrukturplan Übersicht
description: Ein Projektstrukturplan (PSP) ist eine Beschreibung der Arbeit, die für ein Projekt ausgeführt wird. Es ist eine Hierarchie von Aufgaben, die das Verständnis des Projektteams für die Zusammensetzung der Arbeit sowie für die Größe, die Kosten und die Dauer jeder Komponente oder Aufgabe darstellt.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eddaf8a868845bde11c8bb7bc04f63777d628cf4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369420"
---
# <a name="work-breakdown-structures-overview"></a>Projektstrukturplan Übersicht

[!include [banner](../includes/banner.md)]

Ein Projektstrukturplan (PSP) ist eine Beschreibung der Arbeit, die für ein Projekt ausgeführt wird. Es ist eine Hierarchie von Aufgaben, die das Verständnis des Projektteams für die Zusammensetzung der Arbeit sowie für die Größe, die Kosten und die Dauer jeder Komponente oder Aufgabe darstellt. Ein PSP hat drei Hauptziele:

-   Die Aufschlüsselung oder Zusammensetzung der Arbeit in den Aufgaben beschreiben
-   Projektarbeit planen
-   Die Kosten für jede Aufgabe schätzen

Der Detaillierungsgrad in einem PSP hängt von der Genauigkeit ab, die für Schätzungen erforderlich ist, und von der Nachverfolgung, die für diese Schätzungen erforderlich ist. Projekte mit einer sehr geringen Toleranz für Abweichungen im Zeitplan oder in den Kosten erfordern normalerweise einen detaillierteren PSP und eine sorgfältige Verfolgung des Arbeitsfortschritts und der Kosten gegenüber dem PSP. Diese Art von Projekt ist in der Bau- und Maschinenbauindustrie üblich. 

Im Gegensatz dazu sind Projekte in Branchen wie Medien und Werbung, Software und IT-Infrastruktur in der Regel einzigartig, und die Produktivität hängt von der Erfahrung und Kompetenz der Person ab, die die Aufgabe ausführt. Daher verwenden diese Branchen einen PSP, um eine Annäherung an die Größe eines Projekts zu erhalten, und nicht, um den Fortschritt dieses Projekts im Detail zu verfolgen. 

Das Erstellen eines PSP ist ein intensiver Prozess, der normalerweise über einen langen Zeitraum durchgeführt wird und der die Zusammenarbeit und Information einer Vielzahl von Personen erfordert. In diesem Thema wird beschrieben, wie Sie PSP-Verbesserungen verwenden können, um Ihre Anforderungen an Schätzungen und Nachverfolgung zu erfüllen.

## <a name="prerequisites-for-creating-a-wbs"></a>Voraussetzungen zum Erstellen von PSP-Richtlinien
Um einen PSP zu erstellen, müssen Sie in der Lage sein, einen Zeitplan zu erstellen und die Arbeitskosten zu schätzen.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Voraussetzungen für die Erstellung eines Zeitplans

Führen Sie die folgenden Einstellungen aus, um die vollständigen Planungsfunktionen der PSP-Funktionen zu nutzen:

1.  Richten Sie einen Standardkalender und einen Projektkalender ein:
    1.  Wählen Sie **Projektmanagement und Buchhaltung** &gt; **Einrichtung** &gt; **Projektmanagement- und Buchhaltungsparameter** &gt; **Zeitplan** aus. In dem Feld **Standardarbeitskalender** geben Sie im Feld einen Standardkalender an. Dies ist der Standardarbeitskalender für jedes neu erstellte Projekt.
    2.  Sie können den Standardkalender für ein bestimmtes Projekt ändern. Klicken Sie auf die Detailseite des Projekts und dann auf die Registerkarte **Projektteam und Terminplanung**, aktualisieren Sie das Feld **Kalender planen** durch Auswahl eines anderen Kalenders.

2.  Richten Sie Standardarbeitstage und -arbeitszeiten ein. Der Kalender, den Sie als Arbeitskalender für Ihr Projekt festgelegt haben, wird im PSP verwendet, um die folgenden Informationen zu ermitteln:

-   Arbeitstage und Feiertage
-   Die Anzahl der Arbeitsstunden pro Tag

Um die Arbeitstage und Arbeitszeiten für einen Kalender einzurichten oder einen neuen Kalender zu erstellen klicken Sie auf **Organisationsverwaltung** &gt; **Verbreitet** &gt; **Kalender**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Voraussetzungen für die Schätzung der Arbeitskosten

Um die vollständigen Kostenschätzungsfunktionen des PSP nutzen zu können, sollten Sie die Kosten und Verkaufspreise für Arbeitnehmer, Arbeitskategorien, Ausgaben und Gebühren sowie Artikel festlegen.

-   Um die Kosten und den Verkaufspreis für die Kategorien Arbeit, Kosten und Gebühren festzulegen, klicken Sie auf **Projektmanagement und Buchhaltung** &gt; **Konfiguration** &gt; **Preise**.
-   Um die Kosten und den Verkaufspreis von Artikeln festzulegen, verwenden Sie die Seite **Handelsabkommen** für jeden Artikel auf der Listenseite **Freigegebene Produkte** im Produktinformationsmanagement.

## <a name="creating-a-wbs"></a>Erstellen eines PSPs
Das Erstellen eines PSPs umfasst drei Aktivitäten:

1.  **Arbeitszerlegung** – Erstellen Sie eine Aufteilung der Arbeit in überschaubare Abschnitte oder Aufgaben.
2.  **Arbeitsplan** – Schätzen Sie die Zeit, die zum Ausführen einer Aufgabe erforderlich ist, legen Sie die Abhängigkeiten zwischen den Aufgaben fest und wählen Sie das Start- und Enddatum für Aufgaben aus.
3.  **Kostenschätzung** – Schätzen Sie die Kosten für jede Aufgabe.

In den folgenden Abschnitten wird erläutert, wie die PSP-Funktionen bei jeder dieser Aktivitäten helfen können.

### <a name="work-decomposition"></a>Arbeitszerlegung

Das Erstellen einer Aufschlüsselung oder Zerlegung von Arbeiten ist normalerweise der erste Schritt beim Erstellen eines PSP. Die PSP-Funktionalität unterstützt die folgenden grundlegenden Konstrukte für die Aufschlüsselung oder Zerlegung von Arbeiten. 

**Projektstammaufgabe** Die Projektstammaufgabe ist die Zusammenfassungsaufgabe der obersten Ebene für ein Projekt. Alle weiteren Projektaufgaben werden dann darunter erstellt. Der Name der Stammaufgabe ist immer auf den Projektnamen eingestellt. Der Aufwand, die Daten und die Dauer des Stammknotens fassen die Werte für die Aufgaben unter der Stammaufgabe zusammen. Sie können Stammknoteneigenschaften nicht bearbeiten oder löschen.

**Zusammenfassungs- oder Containeraufgaben** Eine zusammenfassende Aufgabe ist eine Aufgabe, unter der Unteraufgaben oder Teilaufgaben liegen. Eine zusammenfassende Aufgabe hat keinen eigenen Arbeitsaufwand oder keine eigenen Kosten. Stattdessen sind der Arbeitsaufwand und die Kosten einer zusammenfassenden Aufgabe die Summe aus Arbeitsaufwand und Kosten der einzelnen Aufgaben. Das früheste Startdatum der zugehörigen Aufgabe ist das Startdatum der Zusammenfassungsaufgabe und das aktuellste Enddatum ist das zugehörige Enddatum der Containeraufgaben. Der Name einer zusammenfassenden Aufgabe kann bearbeitet werden aber die Zeitplanungseigenschaften (Aufwand,Termine und Dauer) können nicht bearbeitet werden. Wenn Sie eine zusammenfassende Aufgabe löschen, dann löschen Sie auch all ihre zugehörigen Aufgaben. 

**Blattknotenaufgaben** Eine Blattknotenaufgabe repräsentiert das detaillierteste Arbeitspaket im Projekt. Ein Blattknoten hat einen geschätzten Aufwand, eine geplante Anzahl von Ressourcen, ein geplantes Start- und Enddaten und eine Dauer. 

Sie können die folgenden Hierarchieoperationen ausführen, um die Erstellung einer Arbeitshierarchie oder die Zerlegung für ein Projekt zu ermöglichen. 

**Neue Aufgabe** Jede neue Aufgabe, die Sie erstellen, wird automatisch unter dem Stammknoten hinzugefügt, und der Aufgabe wird automatisch eine PSP-Nummer zugewiesen. Die PSP-Nummer repräsentiert die Aufgabenebene in der Hierarchie. Für Aufgaben in der ersten Ebene unter der Projektstammaufgabe wird ein Nummerierungsschema von 1, 2, 3 usw. verwendet. Für Aufgaben die sich unter der ersten Ebene befinden, wird ein Nummerierungsschema von 1.1, 1.2, 1.3 usw. verwendet. Für jede Ebene, die unter einer vorherigen Ebene hinzugefügt wird, wird eine neue gepunktete Zahlenreihe hinzugefügt. 

Derzeit können Sie die PSP-Nummerierung nicht anpassen. 

**Aufgabe einrücken** Wenn Sie eine Aufgabe einrücken, wird sie zu einem untergeordneten Element der vorangegangenen Aufgabe. Die PSP-Nummer der neuen untergeordneten Aufgabe wird automatisch basierend auf der PSP-Nummer des neuen übergeordneten Elements neu berechnet. Die übergeordnete Aufgabe ist jetzt eine Zusammenfassung oder Containeraufgabe und wird daher zu einem Rollup ihrer zugehörigen Aufgaben. 

> [!NOTE] 
> Wenn Sie Aufgaben unter einer Aufgabe einrücken, die vor dem Einrückungsvorgang ein Blattknoten war, verliert die neu erstellte Zusammenfassungsaufgabe ihre eigenen Daten, ihren Aufwand und ihre Anzahl von Ressourcen. Es verwendet jetzt eine Zusammenfassung der Werte seiner neuen zugehörigen Aufgaben. 

**Aufgabe ausrücken** Wenn Sie eine Aufgabe ausrücken, ist sie keine zugehörige Aufgabe des übergeordneten Elements mehr. Die PSP-Nummer dieser Aufgabe wird automatisch neu berechnet, um die neue Ebene der Aufgabe in der Hierarchie widerzuspiegeln. Der Aufwand, die Kosten und Datumsangaben von der vorherigen übergeordneten Aufgabe werden neu berechnet, damit sie diese Aufgabe nicht mit einschließen. 

**Nach oben und nach unten bewegen** Wenn Sie **Nach oben** und **nach unten** anklicken, ändern Sie die Position einer Aufgabe innerhalb der übergeordneten Hierarchie. Die Position einer Aufgabe hat keinen Einfluss auf Aufwand, Kosten, Datumsangaben oder Dauer der Aufgabe. Aber die PSP-Nummer dieser Aufgabe wird automatisch neu berechnet, um die neue Ebene der Aufgabe in der Hierarchie widerzuspiegeln.

### <a name="schedule-estimation"></a>Zeitplanschätzung

Die Zeitplanschätzung ist normalerweise der zweite Schritt beim Erstellen eines PSP. Als bewährte Methode sollten Sie die Zeitplanschätzung abschließen, nachdem Sie die Aufgaben erstellt haben. Die Seite **Projektstrukturplan** in Finance hat zwei Abschnitte. Der obere Bereich ist für die Zeitplanschätzung vorgesehen, und der untere Bereich enthält die Registerkarte **Vorkalkulierte Kosten und Einnahmen**, die Sie für die Kostenschätzung verwenden können. 
**Aufgabenabhängigkeiten** In einem PSP können Sie eine Vorgängerbeziehung zwischen Aufgaben erstellen. Wenn Sie einer Aufgabe vorherige Aufgaben zuweisen, kann diese Aufgabe erst gestartet werden, nachdem alle vorherigen Aufgaben abgeschlossen wurden. Das geplante Startdatum der Aufgabe wird automatisch auf das späteste Datum aller vorherigen Aufgaben festgelegt. 

**Aufgabenplanung** Die folgenden Faktoren bestimmen die Zeitplanung von Blattknotenaufgaben:

-   Vorherige Aktivitäten
-   Aufwand
-   Die Anzahl der Ressourcen
-   Start- und Enddatum

Das Startdatum der Blattknotenaufgabe ohne vorherige Aktivitäten ist standardmäßig das geplante Anfangsdatum vom Projekt. Die Dauer einer Blattknotenaufgabe wird immer als Anzahl der Arbeitstage zwischen ihrem Start- und Enddatum berechnet. 

*<strong><em>Zeitplanregeln</em></strong>* Wenn die automatische Zeitplanunterstützung aktiviert ist, gelten die folgenden Regeln für die Aufgabenplanung für Blattknotenaufgaben:

-   Das Start- und Enddatum einer Aufgabe muss gemäß dem Planungskalender des Projekts ein Arbeitstag sein.
-   Das Startdatum einer Aufgabe mit vorherigen Aktivitäten wird automatisch auf das späteste Enddatum seiner vorherigen Aktivitäten festgelegt.
-   Der Aufwand für eine Aufgabe wird automatisch wie folgt berechnet:

Anzahl der Menschen x Dauer x Anzahl der Stunden an einem Standardwerktag im Projektkalender. 

In einigen Fällen möchten Sie möglicherweise von diesen Regeln abweichen. Sie können die automatische Planung deaktivieren, um zu verhindern, dass Finance Eigenschaften von Blattknotenaufgaben automatisch festlegt oder korrigiert. Wenn Sie Informationen für eine Aufgabe eingeben, die einen Verstoß gegen Planungsregeln verursachen, wird ein Planungsfehlersymbol für die Aufgabe angezeigt. Wenn Sie nicht möchten, dass Planungsfehler angezeigt werden, klicken Sie auf **Planungsfehler werden angezeigt**, um die Funktion auszuschalten. 

> [!NOTE] 
> Die Werte für eine Zusammenfassungs- oder Containeraufgabe werden weiterhin als Summe der Werte der einzelnen Aufgaben berechnet, unabhängig davon, ob die automatische Planungsunterstützung aktiviert oder deaktiviert ist. 

**Planungsfehler beheben** Wenn die automatische Planungsunterstützung aktiviert ist, treten wahrscheinlich keine Planungsfehler auf. Wenn Sie jedoch die automatische Planungsunterstützung deaktivieren und später wieder aktivieren, werden im PSP möglicherweise Planungsfehlersymbole angezeigt. 

**Beheben von Planungsfehlern nach Aufgaben** Wenn Sie auf das Symbol für Zeitplanfehler für eine bestimmte Aufgabe doppelklicken, werden in einem Dialogfeld alle Planungsfehler für diese Aufgabe angezeigt. Sie können entscheiden, welche Zeitplaungsfehler für die Aufgabe behoben werden sollen. 

**Behebung aller Zeitplanungsfehler** Wenn Finance alle Zeitplanungsfehler im PSP beheben soll, klicken Sie im Aktionsbereich auf **Beheben Sie alle Zeitplanungsdifferenzen**. 

> [!NOTE] 
> Diese Funktion kann zu erheblichen Änderungen am PSP führen. Fehler werden in der folgenden Reihenfolge korrigiert:

1.  Der geschätzte Aufwand für alle Aufgaben wird so geändert, dass er der im Projektkalender definierten Kapazität entspricht.
2.  Das Startdatum jeder Aufgabe wird so geändert, dass die Aufgabe gestartet wird, nachdem alle Vorgängeraufgaben abgeschlossen wurden.
3.  Das Startdatum jeder Aufgabe wird geändert, um Lücken in den Startdaten der Vorgängeraufgaben zu schließen.

### <a name="cost-estimation"></a>Kosteneinschätzung

Wie bereits in diesem Dokument erwähnt, geben Sie die Kostenschätzung für jede Blattknotenaufgabe mithilfe der Registerkarte **Geschätzte Kosten und Einnahmen** im unteren Bereich der Seite **Projektstrukturplan** ein. 

> [!NOTE] 
> Sie können die Kostenvorkalkulation für eine Zusammenfassung oder Containeraufgabe nicht ändern. Die Kostenvorkalkulation für eine Zusammenfassungsaufgabe ist gleich der Summe der Kostenvorkalkulation ihrer Blattknotenaufgaben. Die geschätzten Gesamtkosten für jede Aufgabe werden als Summe der vorkalkulierten Kostenbeträge für die folgenden Transaktionstypen berechnet:

-   Arbeit
-   Artikel oder Material
-   Ausgaben

Eine Transaktionstyp-**Gebühr** wird zur Schätzung der gebührenpflichtigen Einnahmen verwendet. Dieser Transaktionstyp hat keine Kostenkomponente und wird daher bei der Kostenschätzung nicht berücksichtigt. 

Ein Transaktionstyp **Auf Rechnung** wird verwendet, um den vertraglich vereinbarten Verkaufswert in einem Projekttyp mit festem Wert zu erfassen. Diese Vorgangsart wird auch bei der Kostenschätzung nicht berücksichtigt. 

Wenn Sie die Kosten für Arbeit, Material und Kosten für jede Aufgabe schätzen, müssen Sie den geschätzten Kosten eine Projektkategorie zuweisen. 

**Schätzung der Arbeitskosten** Für jede Blattknotenaufgabe weisen Sie einen Arbeitsaufwand in Stunden und eine Standardkategorie zu. Wenn Sie einen Zeitplan für eine Aufgabe einrichten, wird daher die Arbeitskostenschätzung für diese Aufgabe automatisch in die Standardkategorie für Arbeit aufgenommen. Dieser Kostenvoranschlag wird auf der Registerkarte **Vorkalkulierte Kosten und Einnahmen** im Raster **Zeilendetails** für diese Aufgabe angezeigt. Wenn Sie weitere Arbeitskostenschätzungen benötigen, können Sie sie auf dieser Registerkarte hinzufügen. Wenn Sie die Arbeitskostenschätzung erhöhen oder verringern, wird der Zeitplan für die Aufgabe automatisch neu berechnet. 

**Schätzung der Kosten und Materialkosten** Die Registerkarte **Geschätzte Kosten und Einnahmen** ermöglicht es Ihnen auch, Kosten und Materialkosten für eine Aufgabe zu schätzen, wenn Sie Schätzungen benötigen. 

Die Kosten und der Verkaufspreis für jede Arbeits- oder Kostenschätzungszeile basieren auf der Einrichtung, die für jede Kategorie in den Preistabellen unter **Projektmanagement und Buchhaltung** &gt; **Konfiguration** &gt; **Preisgestaltung** definiert ist. Die Kosten und der Verkaufspreis von Artikeln wird standardmäßig aus dem Artikel- oder Handelsabkommen auf der Listenseite **Freigegebene Produkte** im Produktinformationsmanagement hinzugefügt.

## <a name="tracking-progress-on-the-wbs"></a>Verfolgen des Fortschritts auf dem PSP
Einige Branchen verfolgen den Fortschritt eines Projekts gegenüber einem PSP auf einer sehr detaillierten Ebene, während andere den Fortschritt auf einer höheren Ebene des PSP verfolgen. In diesem Abschnitt wird beschrieben, wie Sie die PSP-Nachverfolgung für Ihre Projektanforderungen verwenden können. 

Finance hat drei Ansichten für den PSP eines Projekts: die Planungsansicht, die Aufwandsnachverfolgungsansicht und die Kostennachverfolgungsansicht.

### <a name="planning-view"></a>Planungsansicht

In der Planungsansicht wird die geplante oder Basisschätzung der Zeitplan- und Kosteninformationen angezeigt. Obwohl es keine Funktionen zum Verfolgen der Version und der Baseline für einen Projekt-PSP gibt, sollen die Werte in dieser Ansicht die Baseline-Version darstellen. In den Abschnitten Zeitplanschätzung und Kostenschätzung dieses Thema wird diese Ansicht beschrieben und es wird auch beschrieben, wie sie zum Erstellen eines PSP verwendet wird.

### <a name="effort-tracking-view"></a>Aufwandsnachverfolgungsansicht

Die Ansicht Aufwandsnachverfolgung zeigt den Fortschritt der Nachverfolgung in PSP an. Es vergleicht die kumulierten tatsächlichen Arbeitsstunden für eine Aufgabe mit den geplanten Arbeitsstunden. Die folgenden Formeln enthalten die Werte in der Aufwandsverfolgungsansicht:

-   Fortschritt in Prozent = tatsächlicher bisheriger Aufwand ÷ geplanter Aufwand für die Aufgabe
-   Verbleibender Aufwand (auch als Schätzung bis zum Abschluss bezeichnet \[ETC\]) = Geplanter Aufwand – Tatsächlicher Aufwand bis heute
-   Schätzung bei Abschluss (EAC) = verbleibender Aufwand + tatsächlicher bisheriger Aufwand
-   Hochgerechnete Aufwandsabweichung = geplanter Aufwand – EAC

In der Ansicht Aufwandnachverfolgung wird eine Projektion der Aufwandsabweichung für die Aufgabe angezeigt, basierend darauf, ob die EAC mehr oder weniger als der geplante Aufwand beträgt:

-   Wenn die EAC größer als der geplante Aufwand ist, wird prognostiziert, dass die Aufgabe länger als ursprünglich geplant dauern wird und hinter dem Zeitplan zurückliegt.
-   Wenn die EAC kleiner ist als der geplante Aufwand, wird prognostiziert, dass die Aufgabe weniger lang als ursprünglich geplant dauern wird und vor Zeitplan liegt.

**Neuprojektion des Projektmanagers** Gelegentlich muss der Projektmanager oder eine andere Person, die den Fortschritt eines Projekts verfolgt, die ursprünglichen Schätzungen für eine Aufgabe überarbeiten. Die Aufgabe kann aus verschiedenen Gründen schneller oder langsamer als ursprünglich angenommen ausgeführt werden. Zum Beispiel wurde der Umfang reduziert oder die Arbeitnehmer haben weniger Erfahrung als ursprünglich geplant. Die Projektion ist die Hochrechnung vom Projektmanager angesichts des aktuellen Status eines Projekts. Grundsätzlich ist es nicht empfehlenswert, die Baselinezahlen zu ändern, da die Projektbaseline die veröffentlichte Quelle für den Zeitplan und die Kostenvorkalkulationen des Projekt ist, der alle Projektbeteiligten zugestimmt haben. 

Es gibt zwei Möglichkeiten, mit denen ein Projektmanager eine erneute Hochrechnung des Aufwands für eine Aufgabe bearbeiten kann:

-   Ändern Sie den verbleibenden Aufwand, der automatisch festgelegt wird, um den tatsächlichen verbleibenden Aufwand für die Aufgabe zu aktualisieren.
-   Ändern Sie den prozentualen Fortschritt, der automatisch festgelegt wird, um den tatsächlichen verbleibenden Fortschritt für die Aufgabe zu aktualisieren.

Beide Ansätze führen zu einer Neuberechnung der ETC, der EAC sowie des Fortschritts in Prozent und der hochgerechneten Aufwandsabweichung für die Aufgabe. Die EAC, die ETC und der Fortschritt in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine aktualisierte Hochrechnung der Aufwandsabweichung. 

**Modifizierter Aufwand für Zusammenfassungsaufgaben** Sie können den Aufwand für Zusammenfassungs- oder Containeraufgaben ändern. Unabhängig davon, ob Sie diese Werte anhand des verbleibenden Aufwands oder des Fortschritts in Prozent auf der Zusammenfassungsaufgabe durchführen, erfolgen die Berechnungen automatisch in der folgenden Reihenfolge:

1.  Die EAC, die ETC und der Fortschritt in Prozent werden für die Aufgabe berechnet.
2.  Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie für den ursprünglichen EAC-Betrag.
3.  Die neue EAC für jede Blattknotenaufgabe wird berechnet.
4.  Der verbleibende Aufwand und der prozentuale Fortschritt werden für alle betroffenen untergeordneten Aufgaben basierend auf dem neuen EAC-Wert neu berechnet. Die Aufwandsabweichung der Aufgaben wird ebenfalls neu berechnet.
5.  Die EAC der Zusammenfassungsaufgaben wird ebenfalls aus den Blattknoten neu berechnet.

Klicken Sie auf **Auf Ebene erweitern** in der Ansicht Aufwandnachverfolgung, um die Ebene festzulegen, auf der Ihr PSP verfolgt und gewartet werden soll. Der PSP wird in der Ansicht Aufwandverfolgung automatisch auf diese Ebene erweitert, wenn Sie ihn öffnen.

### <a name="cost-tracking-view"></a>Die Ansicht „Kostennachverfolgung“

In der Ansicht Kostenverfolgung wird die Verfolgung des Kostenverbrauchs für eine Aufgabe angezeigt. In dieser Ansicht werden die tatsächlichen Kosten, die bisher für eine Aufgabe ausgegeben wurden, mit den geplanten Kosten für die Aufgabe verglichen. Die folgenden Formeln enthalten die Werte in der Kostenverfolgungsansicht:

-   Verbrauchte Kosten in Prozent = tatsächliche bisherige Kosten ÷ geplante Kosten für die Aufgabe
-   Kosten bis Abschluss (CTC) = geplante Kosten – tatsächliche bisherige Kosten
-   Schätzung bei Fertigstellung (EAC) = CTC + Tatsächliche Kosten bis heute
-   Hochgerechnete Kostenabweichung = geplante Kosten – EAC

In der Ansicht Kostennachverfolgung wird eine Projektion der Kostenabweichung für die Aufgabe angezeigt, basierend darauf, ob die EAC mehr oder weniger als die geplanten Kosten beträgt:

-   Wenn die EAC größer als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe mehr Geld als ursprünglich geplant verwendet und über dem Budget liegt.
-   Wenn EAC kleiner als die geplanten Kosten ist, wird prognostiziert, dass die Aufgabe weniger Geld als ursprünglich geplant verwendet und unter dem Budget liegt.

**Neuprojektion der Kosten durch den Projektmanager** Projektmanager müssen CTC verwenden, um den ursprünglichen Kostenvoranschlag für eine Aufgabe zu überarbeiten. Der Projektmanager kann den CTC-Wert an die Kosten anpassen, die zur Ausführung der Aufgabe erforderlich sind. Wenn Sie den CTC-Wert ändern, werden CTC, EAC und Prozentsatz der verbrauchten Kosten der Aufgabe sowie die projizierte Kostenabweichung für eine Aufgabe neu berechnet. Die EAC, die ETC und der Fortschritt der Kosten in Prozent für die Zusammenfassungsaufgaben werden ebenfalls neu berechnet. Hierdurch ergibt sich eine aktualisierte Hochrechnung der Aufwandsabweichung. 

> [!NOTE] 
> Wenn Sie den Aufwand für eine PSP-Aufgabe in der Ansicht Aufwandverfolgung überarbeiten, werden CTC, EAC, Prozentsatz der verbrauchten Kosten und projizierte Kostenabweichung der Aufgabe in der Ansicht Kostenverfolgung neu berechnet. Kostenrevisionen wirken sich jedoch nicht auf die Werte in der Ansicht Aufwandverfolgung aus, da die Kosten nach Transaktionstyp (Arbeit, Material oder Kosten) oder Projektkategorie nicht revidiert werden. 

**Projektionsrevision für Kosten für zusammenfassende Aufgaben** Sie können die Kosten für Zusammenfassungsaufgaben überarbeiten, und die Berechnungen werden automatisch in der folgenden Reihenfolge ausgeführt:

1.  Die EAC, CTC und der Prozentsatz der für die Aufgabe verbrauchten Kosten werden neu berechnet.
2.  Die neue EAC wird für die Aufgabe im selben Verhältnis auf die untergeordneten Aufgaben aufgeteilt wie ursprünglich auch.
3.  Die neue EAC für jede Aufgabe wird berechnet.
4.  Das CTS und der Prozentsatz der verbrauchten Kosten werden für die betroffenen untergeordneten Aufgaben basierend auf dem EAC-Wert neu berechnet. Die Kostenabweichung der Aufgaben wird ebenfalls neu berechnet.
5.  Die EAC für alle Zusammenfassungsaufgaben wird basierend auf dieser Änderung neu berechnet.

Klicken Sie auf **Ebene erweitern** in der Ansicht Kostennachverfolgung, um die Ebene festzulegen, auf der Ihr PSP verfolgt und gewartet werden soll. Der PSP wird in der Ansicht Kostenverfolgung automatisch auf diese Ebene erweitert, wenn Sie ihn öffnen.

### <a name="earned-value-management"></a>Ertragswertverwaltung

Mit der Ertragswertmethode (EWM) können Sie den Fortschritt eines Projekts verfolgen. Sie können Ertragswert-Metriken im Rollencenter des Projektmanagers anzeigen. Die Ertragswertdiagramm-Komponente zeigt die zeitlich gestaffelten Werte des Planwerts und der tatsächlichen Kosten. Der zum aktuellen Datum erzielte Wert wird als Punkt angezeigt. Zeitgesteuerte Daten für den Ertragswert sind derzeit nicht verfügbar. 

Die Zeitphase im Ertragswertdiagramm wird nach Woche oder Monat angezeigt. In diesem Abschnitt werden die drei Säulen von EWA beschrieben: Planwert, Ertragswert und tatsächliche Kosten. 

**Geplanter Wert** Die EWM-Theorie besagt, dass das geplante Wertdiagramm die Rate darstellt, mit der das Projektteam Wert für das Projekt erzielen wollte. 

Finance verwendet die 0:100-Ertragsregel, wenn der geplante Wert dargestellt wird. Nach dieser Regel wird der Wert der Aufgabe zum Enddatum in die Aufgabe gebucht. Es wird kein Wert gebucht, bis die Aufgabe zu 100 Prozent abgeschlossen ist. 

In Projektmanagement und Buchhaltung geben Sie das Enddatum der Blattknoten und die geplanten Kosten dafür ein. Wenn das Diagramm des geplanten Werts nach Woche angezeigt wird, wird der geplante Wert für alle Blattknotenaufgaben für die Dauer des Projekts nach Woche zusammengefasst. 

**Ertragswert** Die EWM-Theorie besagt, dass das Ertragswertdiagramm die Rate darstellt, mit der das Projektteam tatsächlich Wert für das Projekt erzielen wollte. 

Finance verwendet die 0:100-Ertragsregel, wenn der Ertragswert dargestellt wird. Nach dieser Regel wird der Wert der Aufgabe zum Enddatum in die Aufgabe gebucht. Es wird kein Wert gebucht, bis die Aufgabe zu 100 Prozent abgeschlossen ist. 

Bei der Berechnung des Ertragswerts wird der Fortschrittsprozentsatz jeder Aufgabe berücksichtigt. Nach der 0:100-Ertragswertregel werden nur Aufgaben berücksichtigt, die in einem bestimmten Zeitraum erledigt wurden, um den verdienten Wert zum Ende dieses Zeitraums zu berechnen. Der im Projekt erzielte Wert wird für alle Aufgaben berechnet, die beim Erstellen des Diagramms abgeschlossen wurden. 

> [!NOTE] 
> Derzeit verfügt das System für die PSP-Verfolgung nicht über Datenstrukturen zum Speichern historischer Fortschrittsprozentsätze für jede Aufgabe. Daher kann der Ertragswert nur zum Zeitpunkt der Verarbeitung des Cubes gemeldet werden. Verarbeiten Sie den Cube regelmäßig, um die im Rollencenter angezeigten Ertragswertdaten zu aktualisieren. 

**Tatsächliche Kosten** Die EWM-Theorie besagt, dass das tatsächliche Kostendiagramm die Rate darstellt, mit der Geld für das Projekt ausgegeben wird. 

Transaktionen, die in ein Projekt gebucht werden, werden verwendet, um die tatsächliche Kostenlinie zu zeichnen. Die Kosten werden nach Datum zusammengefasst. Diese Daten werden dann verwendet, um die tatsächlichen Kosten nach Woche oder Monat im Ertragswertdiagramm grafisch darzustellen.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Verwendung der Konzepte von geplantem Wert, Ertragswert und tatsächlichen Kosten

**Planen Sie Abweichungen** Während der Planung erstellen Sie eine Prognose für die Arbeit an einer Zeitskala. Der geplante Wert ist daher die Rate, mit der die Projektplaner dachten, die Arbeiten am Projekt würden abgeschlossen sein. Nachdem ein Projekt ausgeführt wurde, sind die Arbeiten abgeschlossen und das Projekt erzielt Wert. Durch Vergleichen des geplanten Werts mit dem Ertragswert können Sie den Fortschritt der Arbeit an einem Projekt anzeigen. Das Ergebnis dieses Vergleichs wird als Planabweichung bezeichnet. 

Wenn der geplante Wert für einen Zeitraum höher ist als der Ertragswert, ist der Arbeitsaufwand für ein Projekt geringer als geplant. Daher liegt das Projekt hinter der Zeitskala zurück. Da der geplante Wert und der Ertragswert in Geld ausgedrückt werden, erhält die Verzögerungszeit für das Projekt auch einen Geldwert. 

Wenn der geplante Wert für einen Zeitraum kleiner ist als der Ertragswert, ist der Arbeitsaufwand für ein Projekt höher als geplant. Daher ist das Projekt der Zeitskala voraus. Diese Vorlaufzeit erhält ebenfalls einen Geldwert.

**Kostenunterschied** Da der Ertragswert den Selbstkostenpreis als Multiplikator verwendet, gibt der Ertragswert die Kosten der Arbeit an, die an einem Projekt ausgeführt wird. Im Verlauf eines Projekts enthält das Transaktionsprotokoll eine Aufzeichnung der tatsächlich für dieses Projekt ausgegebenen Gelder. Durch Vergleichen des Ertragswerts mit den tatsächlichen Kosten können Sie den ausgegebenen Geldbetrag im Vergleich zum Ertragswert anzeigen. Das Ergebnis dieses Vergleichs wird als Kostenabweichung bezeichnet. 

Wenn die tatsächlichen Kosten, die für einen Zeitraum ausgegeben werden, höher sind als der Ertragswert, wurde mehr Geld ausgegeben als verdient. Daher ist das Projekt über dem Budget. 

Wenn die tatsächlichen Kosten, die für einen Zeitraum ausgegeben werden, kleiner sind als der Ertragswert, wurde mehr Geld verdient als ausgegeben. Daher ist das Projekt unter dem Budget.

## <a name="wbs-templates"></a>PSP Vorlagen
Mit der Funktion PSP-Vorlagen können Sie Standardvorlagen für Projekte erstellen. Wenn die von Ihrem Unternehmen angebotenen Projekte viel wiederholbare Arbeit erfordern, sollten Sie eine PSP-Vorlage erstellen. 

Sie können eine PSP-Vorlage aus dem PSP eines vorhandenen Projekts erstellen, damit das Wissen und die Best Practices, die Sie während der Planung dieses Projekts gesammelt haben, in Zukunft für ähnliche Projekte wiederverwendet werden können. Manchmal ist es jedoch möglicherweise nicht sinnvoll, den gesamten PSP als Vorlage zu speichern. Daher können Sie auch Vorlagen aus Teilen des PSP für ein Projekt erstellen.

### <a name="saving-a-projects-wbs-as-a-template"></a>Speichern des PSP eines Projekts als Vorlage

Nachdem Sie eine Vorlage erstellt haben, können Sie sie unter dem Stammknoten oder unter einer beliebigen Aufgabe im PSP des Projekts in den PSP eines neuen Projekts importieren.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importieren einer PSP-Vorlage in den PSP eines Projekts

Wenn Sie Aufgaben importieren, werden die Aufgaben in der Vorlage basierend auf dem Startdatum der Aufgabe organisiert, unter der sie importiert werden. Während des Imports werden Vorgängerbeziehungen für die Vorlagenaufgaben verwendet, um die Startdaten für die importierten Aufgaben zu berechnen. Der Standardarbeitskalender des Zielprojekts wird angewendet, um die Enddaten der importierten Aufgaben zu berechnen, sodass Arbeitstage und Standardarbeitszeiten, die im Arbeitskalender des aktuellen Projekts definiert sind, beibehalten werden. 

Kostenbeträge und Verkaufspreise in den Schätzzeilen werden angewendet, um sicherzustellen, dass die für das Projekt oder den Projektvertrag spezifischen Preise gültige Daten haben.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Unterschiede zwischen dem PSP eines Projekts und einer PSP-Vorlage

-   Die Aufgaben in PSP-Vorlagen haben keine Start- und Enddaten.

Die Arbeitstage und arbeitsfreien Tage sind für PSP-Vorlagen nicht festgelegt.

-   PSP-Vorlagen verwenden immer den Zeitplanungskalender, der als Standardkalender für alle Projekte eingerichtet ist.

Der Standard-Zeitplanungskalender wird nur verwendet, um die Stunden an einem Standardarbeitstag zu ermitteln.

-   Vorgängerbeziehungen werden nicht in eine PSP-Vorlage kopiert.

Da PSP-Vorlagen keine Datumsangaben haben, ist die Startdatumslogik, die auf dem Enddatum eines Vorgängers basiert, nicht erforderlich.

-   Eine Arbeitskostenschätzungszeile wird automatisch erstellt, wenn eine Aufgabe in einer PSP-Vorlage erstellt wird. Der Verkaufspreis und der Kostenbetrag werden vom ausgewählten Mitarbeiter kopiert.

Ausgaben- und Artikelkosten können manuell erstellt werden, genau wie im PSP eines Projekts.

-   Zeitplanungsfehler werden angezeigt, wenn Abweichungen von der folgenden Formel vorliegen:

Aufwand = Anzahl der Ressourcen × Dauer × Anzahl der Stunden an einem Standardarbeitstag 

Sie können alle Zeitplanungsfehler gleichzeitig korrigieren, indem Sie auf **Beheben Sie alle Zeitplanungsfehler** klicken. 

Alternativ können Sie Zeitplanungsfehler einzeln korrigieren, indem Sie für jede Aufgabe auf das Warnsymbol klicken.





[!INCLUDE[footer-include](../includes/footer-banner.md)]