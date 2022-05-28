---
title: Neuigkeiten und Änderungen in Project Service Automation, Version 3
description: Dieses Thema enthält Informationen über Neuigkeiten und Änderungen in Project Service Automation, Version 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
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
ms.openlocfilehash: 15925cb88cc413f9a23a25e89ddd29668e9171de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581651"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Neuigkeiten und Änderungen in Project Service Automation, Version 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Dieses Thema enthält Informationen zu den Änderungen an der Benutzeroberfläche (UI), zur Funktion und Terminologie in Project Service Automation zwischen Version 2 oder Version 1 und Version 3.

## <a name="project-scheduling"></a>Projektzeitpläne
Der Projektzeitplan, der als Projektstrukturplan (WBS) in früheren Versionen bekannt war, wurde in Zeitplan umbenannt und ist verfügbar, indem Sie auf die Registerkarte **Zeitplan** klicken. 

![Projektzeitplan.](media/psa-schedule-01.png)

Der Zeitplan hat jetzt eine neue Oberfläche für die Interaktion, die sowohl modern als auch zugänglich ist. Das zugrunde liegende Project Service Automation Planungsmodul wurde jedoch nicht geändert. Mit den Steuerschaltflächen im Menüband des Zeitplanrasters können Sie mit dem Zeitplan interagieren wie in der früheren Version von Project Service Automation. Zusätzliche Änderungen am Zeitplan:

- **Gantt-Diagramm** - Das Gantt-Diagramm ist nicht mehr vorhanden. Eine neue Gantt-Visualisierung wird in einem zukünftigen Update zurückkehren.
- **Spaltenüberschriften** - Sie können Spaltenüberschriften im Raster ausblenden, indem Sie unten auf den Indikator neben dem Spaltentitel klicken. 
- **Spalten** - Sie können ausgeblendete Spalten anzeigen, indem Sie auf **Spalten hinzufügen** klicken. 
- **Transaktionskategorie** - Eine Suche nach **Transaktionskategorie** wurde zum Zeitplanraster hinzugefügt und wird standardmäßig angezeigt. 
 
## <a name="project-templates"></a>Projektvorlagen
Die folgenden Änderungen wurden an den Projektvorlagenfunktionen vorgenommen.

### <a name="create-a-project-template"></a>Eine Projektvorlage erstellen 
Sie können eine Projektvorlage in Version 3 erstellen, die der letzten Version von Project Service Automation ähnlich ist. Die Vorlage kann nur einen Zeitplan enthalten und die Zeitplanung kann Zuweisungen enthalten, sie sind jedoch nicht erforderlich. Wenn der Zeitplan Zuweisungen hat, kann er nur für allgemeine Ressourcen sein. Sie können allgemeine Ressourcenanforderungen für Ressourcen erstellen, aber sie können nicht mit Ressourcen in der Vorlage gebucht werden. Sie können keine reale Ressource für ein Team in einer Vorlage buchen. 

### <a name="create-a-template-from-an-existing-template"></a>Erstellen einer Vorlage aus einer vorhandenen Vorlage
Wenn Sie eine neue Projektvorlage aus einer bestehenden Vorlage in Project Service Automation Version 3 erstellen, passiert Folgendes: 

- Der Zeitplan des Quellprojekts wird in die Vorlage kopiert. 
- Allgemeine Ressourcen werden in ins Team kopiert und alle allgemeinen Ressourcen-Zuweisungen werden darüber kopiert. Anforderungen für allgemeine Ressourcen werden nicht kopiert. 

### <a name="create-a-template-from-an-existing-project"></a>Erstellen einer Vorlage aus einem vorhandenen Projekt
Wenn Sie eine neue Projektvorlage aus einem bestehenden Projekt erstellen, passiert Folgendes: 

- Der Zeitplan des Quellprojekts wird in die Vorlage kopiert. 
- Allgemeine Ressourcen werden in ins Team kopiert und alle allgemeinen Ressourcen-Zuweisungen werden beibehalten. Anforderungen für allgemeine Ressourcen werden nicht kopiert.    
- Die benannten zugewiesenen oder nicht zugewiesenen Ressourcen werden aus dem Team entfernt und durch allgemeine Ressourcen ersetzt.
- Gegebenenfalls vorhandene Kundeninformationen werden entfernt. 
- Falls vorhanden, werden Verweise in Angeboten und Verträgen entfernt. 

### <a name="create-a-project-from-a-template"></a>Erstellen eines Projekts aus einer Vorlage
Wenn Sie eine neue Projektvorlage aus einer bestehenden Vorlage in Project Service Automation Version 3 erstellen, passiert Folgendes:

- Der Zeitplan, das Team und die Zuweisungen werden in das neue Projekt kopiert.   
- Das Startdatum ist entweder das Kopiendatum oder das Datum, das vom Benutzer ausgewählt wurde.   
- Für alle allgemeinen Teammitglieder mit Ressourcenanforderungen in der Vorlage werden die Anforderungen automatisch generiert. Sie müssen dies generieren. 

## <a name="copy-a-project"></a>Ein Projekt kopieren
Wenn Sie eine neue Projektvorlage aus einer bestehenden Vorlage in Project Service Automation Version 3 kopieren, passiert Folgendes: 

- Das geschätzte Startdatum wird kopiert, aber kann geändert werden.  
- Der Projektzeitplan und die Aufgaben werden kopiert. 
- Generische Ressourcen und ihre Zuweisungen werden kopiert. Ressourcenanforderungen für allgemeine Ressourcen werden nicht kopiert. Sie müssen dies neu generieren. 
- Reale Ressourcen und ihre Zuweisungen werden nicht kopiert. Stattdessen werden sie von allgemeinen Ressourcen ersetzt. 
- Ist-Werte werden nicht in das neue Projekt kopiert. 

## <a name="move-a-scheduled-project"></a>Verschieben Sie ein geplantes Projekt
Wenn Sie den Zeitplan des vorhandenen Projekts verchieben, passiert Folgendes: 

- Aufgabendatumsangaben werden automatisch verschoben, dass sie dem Bewegungszeitraum entsprechen. 
- Zugewiesene allgemeine Ressourcen bleiben zugewiesen.   
- Wenn sie generiert werden, bevor das Projekt verschoben wird, bleiben die Anforderungen für die allgemeine Ressource identisch und werden nicht automatisch neu generiert. Sie müssen sie erneut generieren, um die neuen Zuweisungen aufgrund der Aufgabenbewegung widerzuspiegeln. 
- Zuweisungen realer Ressourcen werden geändert, um der Aufgabendatumsbewegung zu entsprechen. Buchungen realer Ressourcen werden nicht geändert. Sie müssen die Buchungen mit der Abstimmungsansicht ändern. 
- Teamressourcen für Buchungen, aber Zuweisungen werden nicht geändert. 
- Ist-Werte werden nicht verschoben. 

## <a name="estimates"></a>Schätzungen
Schätzungen sind in zwei Registerkarten **Ressourcen-Zuweisung** und **Schätzungen** unterteilt. Die Registerkarte **Ressourcen-Zuweisung** enthält die Aufwandsschätzungen und die Ressourcen-Zuweisungen für die Aufgaben in einer Zeitphasenansicht. Sie können die Schätzungen basierend auf den generierten Werten des Planungsmoduls bearbeiten.

![Ressourcen-Zuweisungsregisterkarte mit Aufwandsschätzungen und Ressourcen-Zuweisungen für Aufgaben.](media/resource-assignments-tab-02.png)

Die Registerkarte **Schätzungen** zeigt die Kosten und Umsätze für Ressourcen-Zuweisungen an. Die Beträge sind schreibgeschützt. Die Kosten- und Vertriebspreisberechnungen werden nun von Teammitglieds-Zuweisungen im Zeitplan abgeleitet. Das bedeutet, dass bei einer Aufgabe ohne jegliche Zuweisung die Aufgabe unter dem nicht zugewiesenen Bucket dargestellt wird. Dies bedeutet auch, dass ohne **Rolle**, was eine Standardpreisberechnungsdimension ist, keine geschätzten Kosten oder Verkäufe existieren, wenn Sie einen Kunden oder einen Vertrag/ein Angebot haben, dem das Projekt zugeordnet ist. 

![Schätzungsregisterkarte mit Kosten und Verkaufsbeträgen.](media/estimates-tab-03.png)
  
Kategorie wird in Aufgaben in der Zeitplanansicht unterstützt. Eine Gruppierung nach Kategorie auf der Zeitphasenansicht der Schätzungen bietet eine verbesserte Erfahrung, insbesondere wenn Sie auch Ausgabenschätzungen in einem Projekt haben. Ausgabenschätzungen werden mithilfe eines Rasters auf einer separaten Registerkarte eingegeben. 

Ausgabenschätzungen können in das Raster auf der Registerkarte **Ausgabenschätzungen** eingegeben werden. 

![Ausgabenschätzungsregisterkarten mit Ausgabenschätzungsraster.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Ressourcenverwaltung
In Project Service Automation Version 3 mit der neuen einheitlichen Clientbenutzeroberfläche und den Änderungen in der Beziehung zwischen Buchungen und Zuweisungen hat die Stellenbesetzung eines Projekts mit allgemeinen oder realen Ressourcen von Version 2 und Version 1 stark geändert. Allerdings bleiben die Konzepte buchbarer Ressourcen bei **real** und **generisch** identisch, wie auch Teammitglieder, Anforderungen, Zuweisungen und Buchungen.   

![Verwenden der Ressourcenauswahl.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Zuweisen einer realen buchbaren Ressource 
In Project Service Automation Version 3 sind Buchungen und Aufgabenzuweisungen nicht so eng miteinander verknüpft wie in früheren Versionen von Project Service Automation. Sie können das Teamraster verwenden, um ein **reales** Team wie auf dem Markt zu buchen.

Mithilfe der Ressourcenauswahl im Zeitplan können Sie das Teammitglied auswählen, das in der Teamansicht erstellt wird, und diesem dann Aufgaben zuweisen. Sie können auch nach der Buchung Aufgaben zuweisen. Verwenden Sie die Registerkarte **Abstimmung**, um Teammitglieder abzugleichen, die über Unterschiede bei Buchungen und Zuweisungen verfügen.

Die Ressourcenauswahl zeigt Teammitglieder für das Projekt an. Sie können die Ressourcenauswahl auch verwenden, um nach einer buchbaren Ressource zu suchen und sie anzuzeigen, die nicht Teil des Projektteams ist. Sie können sie Aufgaben zuweisen, sodass sie Teil des Projektteams werden. Sie müssen sie mithilfe der **Zeitplanübersicht** oder über die Registerkarte **Abstimmung** buchen.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Weisen Sie eine allgemeine buchbare Projektressourcenrolle für eine Aufgabe und einem Projektteam zu und erfüllen Sie über die Zeitplanübersicht mit einer realen Ressource 
In Project Service Automation Version 3 wird die Funktion „Team generieren“ für allgemeine Ressourcen nicht verwendet. Stattdessen können Sie eine allgemeine Ressource direkt aus dem Zeitplan erstellen und zuweisen, indem Sie den Positionsnamen der generischen Ressource in der Ressourcenzelle des Zeitplans eingeben. Sie können auch das Ressourcensymbol in der Zelle auswählen und dann mit der Ressourcenauswahl den Namen der allgemeinen Ressource eingeben, die Sie erstellen möchten. Dadurch wird ein Schnellerstellungsfenster angezeigt, das Ihnen ermöglicht, die Rolle und Organisationseinheit des Ressourcenteammitglieds festzulegen. Nachdem Sie die Ressource erstellen, wird sie zur Aufgabe zugewiesen, und Sie können den Vorgang fortsetzen, um die Ressource für allgemeine Aufgaben im anderen Zeitplan zuzuweisen.    
 
Wenn die Ressource für alle entsprechenden Aufgaben zugewiesen wurde, können Sie eine Ressourcenanforderung erstellen und dann erfüllen, indem Sie mit der **Zeitplanübersicht** oder per Übermittlung einer Ressourcenanforderung direkt buchen. Sie können allgemeine Ressourcen auch direkt dem Teammitgliedsraster hinzufügen. 

Generische Ressourcen werden zum Projektteam ohne Ressourcenanforderungen und mit den Start-/Enddaten des Projekts hinzugefügt, bis die Ressourcenanforderungen generiert werden. Um eine bestimmte Anforderung zu generieren, wählen Sie die allgemeine Ressource aus, und klicken Sie auf **Generieren**. Der Anforderungslink wird nun angezeigt und die erforderlichen Stunden werden mit den zugewiesenen Stunden aufgefüllt. Sie können auf den Link klicken, um die Anforderung zu öffnen und zu aktualisieren.
  
Wenn die Buchung abgeschlossen und komplett von einer benannten Ressource erfüllt wurde, wird die allgemeine Ressource durch die benannte Ressource ersetzt und die Zuweisung im Zeitplan wird mit der benannten Ressource aktualisiert. 

Vorgeschlagene Ressourcen für Anforderungen werden nun auf einer separaten Registerkarte anstelle eines Abschnitts gespeichert.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Mehrere benannte Ressourcen, die eine allgemeine Ressource erfüllen
Wenn eine Anfrage mit mehreren Ressourcen erfüllt wird, bleibt die allgemeine Ressource im Team und der Aufgabe zugewiesen. Die Teammitglieder, die gebucht werden, werden nicht als Teil der Position zugewiesen. Der Projektmanager kann die Arbeit den realen Ressourcen nach Bedarf zuweisen.  Die Ansicht **Abstimmung** bietet eine Aufschlüsselung der Buchungen für mehrere Ressourcen zu mehreren Aufgabenzuordnungen. Dies wird nicht automatisch ausgeführt, da in schwierigeren Szenarien, beispielsweise in einem Aufgabenpaket, das die Anforderung ausmacht, muss die Absicht des Projektmanagers beim Zuweisen eingeschätzt werden. Da das System Absichten nicht verstehen kann, weichen die Annahmen wahrscheinlich von den Absichten ab und ein falsches oder unvorhersehbares Ergebnis tritt auf. Das vorhersagbare Ergebnis ist, dass die allgemeinen Ressourcen zugewiesen bleiben, bis der Projektmanager Ressourcen bewusst über die Ansicht **Abstimmung** zuweist.

### <a name="reconciliation"></a>Abstimmung
Die Registerkarte **Abstimmung** zeigt alle Buchungen und Zuweisungen für jedes Projektteammitglied an. Die Ansicht zeigt Stunden in Zellen an, was für Zeitpunkte von Monaten bis Tagen stehen kann. Mit dieser Ansicht können Projektmanager die Teammitgliedsbuchungen und Zuweisungen für das Projektteam abgleichen. Dies ist hilfreich, da Buchungen und Aufgabenzuordnungen nicht fest gekoppelt sind, wodurch mehr Flexibilität bei der Planung eines Projekts möglich ist. 

![Die Registerkarte „Abstimmung“ zeigt Buchungen und Zuweisungen für Projektteammitglieder an.](media/resource-reconciliation-tab-06.png)

Für jede Ressource nimmt die Ansicht den Unterschied zwischen den Buchungen eines Teammitglieds und einem Rollup der Aufgabenzuordnungen und zeigt die folgenden beiden Unterschiede an, die für Buchungen und Zuweisungen in einem Projekt auftreten können: 

- **Verlust der Buchung** - Buchungsverluste treten auf, wenn eine Ressource mehr Zuweisungen als Buchungen hat. Da diese Kapazität nicht reserviert wurde, kann ein Projektmanager dies korrigieren, indem er die Ressourcenbuchungen erweitert, um das Defizit abzudecken. 
- **Überzählige Buchungen** - Überzählige Buchungen treten auf, wenn eine Ressource für das Projekt gebucht wurde, aber keinen Aufgaben zugewiesen wurde.  Das kann ein akzeptables Vorkommen sein, wenn beispielsweise die Ressource vo der Aufgabenzuordnung gebucht wurde. In anderen Fällen wird die Zuordnung der Ressource nicht geplant, und der PM sollte das Verwerfen der Buchung der Ressource in Betracht ziehen, um die Kapazität für ein anderes Projekt bereitzustellen. 

Wenn Sie Aufgabenzuordnungen für eine Ressource ohne Buchungen (ein Verlust der Buchung) haben, können Sie den gesamten Buchungsverlust auswählen und **Anmeldung erweitern** klicken. Von hier können Sie Buchung anzeigen, die benötigt wird, um den Mangel und die Verfügbarkeit der Ressource zu beheben. 
 
## <a name="time-and-expense"></a>Zeit und Ausgaben
Dieser Abschnitt enthält Informationen zu den Änderungen an Zeitplanung, Ausgaben und Genehmigung in Version 3 von Project Service Automation. Als Teil der Dynamics 365 Project Service Automation-Lösung wurde die **Zeiteintrag**-Funktion aktualisiert, um das einheitliche Oberfläche-Framework zu nutzen. Dies bietet eine durchgängige, einheitliche Benutzeroberfläche (UI) und folgt den dynamischen Designgrundsätzen für eine optimale Anzeige auf jeder Bildschirmgröße oder jedem Gerät. 

### <a name="landing-page"></a>Angebotsseite
Die nicht erweiterbare benutzerdefinierte Zeiteintragungsumgebung wurde in Version 3 eingestellt. Stattdessen gibt es jetzt eine erweiterbare und zugreifbare systemeigene Rastererfahrung. Sie können auf die Zeiteintragsfunktion zugreifen, indem Sie die Siteübersicht auf der linken Seite verwenden. Mit dieser Änderung können Sie die Zeit für eine Woche nicht gleichzeitig eingeben. Stattdessen müssen Sie eine Zeiteintragung für jeden Tag im Raster erstellen. Wenn einige Zeiteintragungen erstellt wurden, können Benutzer Zeiteintragungen per **Kopieren** in Massen erstellen, wie später in diesem Thema beschrieben wird. 

![Zeiteintragungs-Angebotsseite.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Neue Zeiteinträge erstellen 
Klicken Sie im Menüband auf **Neu**, um eine Schnellerstellungsseite für die Zeiteintragung zu öffnen, in der Sie die Minuten, Stunden und Tage eingeben. Geben Sie hierzu nur h, m oder d zusammen mit der Menge ein.  

![Schnellerfassung für Zeiteintrag.](media/quick-create-time-entry-08.png)

Suchfelder werden von Systemansichten unterstützt. Wenn Sie beispielsweise Projektinformationen eingeben, ist das Feld **Projektaufgabe** standardmäßig auf **Meine offenen Projektaufgaben** festgelegt. Wenn Sie Zeiteinträge für Aufgaben erstellen möchten, die dem Benutzer nicht zugewiesen werden, klicken Sie auf **Ansicht ändern** ind er Suche und wählen **Alle aktiven Projektaufgaben**. Nachdem die Zeiteintragung erstellt wurde und im Raster angezeigt wird, können Sie direkt alle Zeilenwerte im Raster bearbeiten.  

### <a name="bulk-createcopy"></a>Massenerstellen/-kopieren 
Nachdem einige Zeiteinträge erstellt wurden, können Sie diese kopieren, um eine Massenerstellung zusätzlicher Zeiteinträge vorzunehmen. Klicken Sie auf **Kopieren**, um das Dialogfeld **Kopieren** zu öffnen. In **Zeitraum von: Startdatum** legen Sie den Datumsbereich fest, aus dem andere Buchhaltungsperioden kopiert werden müssen. Geben Sie in **Zeitraum bis: Startdatum** das Datum an, für das Zeiteintragungen erstellt werden müssen. Klicken Sie auf **Kopieren**, um die Zeiteintragungen zum entsprechenden Wochentag zu kopieren, der in **Zeitraum bis** angegeben ist. So wird z. B. der Zeiteintrag für Montag der vergangenen Woche in den Montag für die Woche kopiert, die in **Zeitraum bis** angegeben ist. 

![Zeiteinträge massenkopieren.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Daten importieren 
Zuweisung und Austausch folgen demselben Benutzeroberflächenmuster, mit dem Benutzer den Datumsbereich angeben können, wenn Buchungen importiert werden müssen. Sie müssen Buchungen dann explizit auswählen, die in **Entwurf**-Zeiteintragungen kopiert werden sollen. In Version 3 werden **Vorgeschlagen**-Zeiteintragungen im Raster und Kalender nicht mehr angezeigt.  

### <a name="change-in-calendar-control"></a>Änderung im Kalendersteuerelement
In Version 3 sind wir vom benutzerdefinierten Kalendersteuerelement abgewichen und nutzen jetzt den UC-Kalender, um Zeiteinträge der Woche anzuzeigen. In diesem Kalender können Sie nach Tag, Woche oder Monat anzeigen. 

> [!NOTE]
> Eine Einschränkung im Kalender ist, dass dieses Steuerelement keine Aktionen für einzelne Kalenderelemente unterstützt. Beispielsweise ist es nicht möglich, eine oder mehrere Kalenderelemente auszuwählen und die Elemente zu senden oder zu löschen. Beim Klicken auf ein Kalenderelement wird die Seite **Zeiteintragungsentität** für weitere Aktionen geöffnet. 

### <a name="extensibility"></a>-Erweiterbarkeit
**Nur Daten in benutzerdefinierten Feldern in Zeit- und Ausgabeneintragsentitäten aufzeichnen** - Zeiteintragung nutzt ein bearbeitbares Raster, ein schreibgeschütztes Raster und Kalendersteuerelemente der Plattform. All diese Steuerelemente sind systemeigen und unterstützen daher Anpassungen. In Project Service Automation Version 3 können Sie weitere benutzerdefinierte Felder hinzufügen, Suchfelder einrichten und Sie mit benutzerdefinierten Ansichten versehen. Sie können auch angepasste Geschäftslogik anhand ausgewählter Werte in den benutzerdefinierten Feldern festlegen.  

**Daten in benutzerdefinierten Feldern in Zeit- und Ausgabeneinträgen erfassen und über Entitäten übertragen, die den Übertragungs- und Genehmigungsfluss unterstützen** - Das normale Verarbeiten von Zeiteintragungen wird im folgenden Diagramm angezeigt.

![Flow zum Prozess der Zeiteingabe.](media/process-time-entries-10.png)

Wenn geschäftliche Anforderungen festlegen, dass Zeit- und Ausgabenentitäten benutzerdefinierte Preisberechnungsdimensionen erfassen und die Werte verbreiten müssen, die durch eine Zeit- und Eintragsressource in der benutzerdefinierten Preisberechnungsdimension für alle Entitäten aus der vorherigen Grafik festgelegt wurden, lesen Sie die Informationen unter [Einrichten von benutzerdefinierten Feldern als Preisdimensionen](set-up-pricing-dimensions.md)

Um geschäftliche Anforderungen zu unterstützen, bei denen Zeit- und Ausgabenentitäten benutzerdefinierte Nicht-Preisberechnungsdimensionen erfassen und die Werte verbreiten müssen, können Sie die Einrichtung der Preisberechnungsdimensionen verwenden und die benutzerdefinierten Dimensionen als Preisberechnungsdimensionen ohne Kosten oder Fakturierungsraten auszudrücken. Ein weiteres Szenario könnte das Hinzufügen eines benutzerdefinierten Felds zu allen Entitäten mit demselben Feldnamen für alle Entitäten sein. Benutzerdefinierte Plug-Ins können erstellt werden, um Datensätze in den Entitäten zu verknüpfen, die am Übertragungs-/Genehmigungsfluss mithilfe des Transaktionsursprungs und der Transaktionsverbindungs-Entitäten teilnehmen.  

### <a name="delegate-time-and-expense-entry"></a>Zeit- und Ausgabeneintrag delegieren
Die Common Data Service-Plattform unterstützt nciht, dass Benutzer die Identität anderer Benutzer annehmen, sodass Version 3 von Project Service Automation keine Unterstützung für delegierte Zeit- und Ausgabeneinträge bietet. Partner und Kunden haben jedoch eine Problemumgehung genutzt, um eine Unterstützung für delegierte Zeiteintragungserfahrungen in Version 3 zu aktivieren. Dies ist lediglich eine Problemumgehung und keine umfassende Lösung, deshalb ist es wichtig, die Beschränkungen zu kennen und nur diese Herangehensweise zu verwenden, wenn die Beschränkungen akzeptabel sind. 

> [!IMPORTANT]
> Diese Informationen sollten nur als vorgeschlagene Anweisungen für benutzerdefinierte Implementierung von einemPartner/von einem Kunden angesehen werden. Das Produktteam bietet keinen formellen Support für diese Funktion über die Supportkanäle.

### <a name="customization-details"></a>Details zur Anpassung 
Anpassung ermöglicht es Ihnen, eine **Buchbare Ressource** hinzuzufügen, um Erfahrungen zu erstellen und zu bearbeiten, mit denen ein Benutzer als Stellvertretung agieren kann, indem er das Feld **Buchungsressource** eiens anderen Benutzers ändert, dessen Zeit- und Ausgabeneinträge aufgezeichnet werden müssen. Die folgende Schritte decken die Zeiteintragungsdelegierung ab. Die gleichen Informationen gelten für Ausgabeneintragsdelegierung. 
 
1.  Stellen Sie sicher, dass der delegierte Benutzer über Sicherheitszugriff für globale Projekte und Projektaufgaben verfügt. 
1.  Da **Buchbare Ressource**, ein Feld der Entität **Zeiteintragung**, nicht auf der **Schnellerfassung**-Seite verfügbar gemacht wird, müssen Sie es hinzufügen.

    – oder –

    Erstellen Sie eine benutzerdefinierte Ansicht, die die Spalte **Buchbare Ressource** enthält, um nur Zeiteintragungen anzuzeigen, die für die Ressource erstellt wurden. Veröffentlichen Sie die Anpassungen im App-Moduldesigner für diese Ansicht, sodass sie unter **Ansichtsauswahl** auf der Seite **Zeiteinträge** angezeigt werden. Es gibt zwei Plug-Ins, die die Einstellungen für projektbezogene Zeiteintragungen behandeln:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Erstellen Sie ein neues Plug-In, um das Feld **Manager** für den Vorgesetzten des Benutzers zu überschreiben, der im Feld **Buchbare Ressource** zugeordnet ist. Verwenden Sie dieselbe **Ausführungsphase** wie das OOB-Plug-In (Vorüberprüfung) und verwenden Sie eine **Reihenfolge der Ausführung**, diehöher ist als die des OOB-Plug-Ins (mehr als 1). Dadurch wird sichergestellt, dass das benutzerdefinierte Plug-In nach den OOB-Plug-Ins ausgeführt wird.  
 
### <a name="end-user-experience"></a>Endbenutzererfahrung
1.  Wenn Sie eine Zeiteintragung auf der Schnellerfassungsseite erstellen, geben Sie die Projekt- und ein Projektaufgabendetails ein, und wählen Sie dann den Benutzer im Feld **Buchbare Ressource** aus, für den die Zeiteintragungen aufgezeichnet werden müssen. 
2.  Standardmäßig ist dies das Feld mit dem angemeldeten Benutzer, da der Benutzer das Feld jedoch überschrieben hat, wird die Zeiteintragung jetzt für die **Buchbare Ressource** erstellt.
3.  Wenn Sie die Zeiteintragungen senden, die für die Datensätze erstellt wurden, werden die Einträge für die genehmigende Person im Projekt erwartungsgemäß in die Warteschlange eingereiht. 
4.  Wenn Sie die Zeiteintragungen zurückrufen, die für den anderen Benutzer erstellt wurden, werden die Zeiteintragungen in den Status **Entwurf** zurückgesetzt und das Feld **Buchbare Ressource** wird auf den anderen Benutzer festgelegt. 
5.  Optional können Sie die benutzerdefinierte Ansicht ändern, um die Zeiteintragungen zu filtern, die für den anderen Benutzer erstellt wurden. 
 
### <a name="limitations"></a>Einschränkungen
Die Funktionen **Kopieren** und **Importieren** funktionieren nur im Kontext des Benutzers, der angemeldet ist. Dies bedeutet, dass es nicht möglich ist, Zeiteintragungen zu kopieren oder zu importieren, die für den Benutzer erstellt wurden, der als die Projektressourcenrolle angemeldet ist.

Zeiteintragungen, die nicht für ein Projekt sind, werden zur Genehmigung an den Manager der Projektressourcenrolle weitergeleitet, wenn Schritt 4 im Abschnitt **Anpassungs-Details** abgeschlossen ist. Andernfalls werden nicht-projektbezogene Zeiteintragungen für den anderen Benutzer fälschlicherweise an den Vorgesetzten des angemeldeten Benutzers weitergeleitet. 

### <a name="other-changes"></a>Andere Änderungen 
Die Funktion **Buchungen und Aufgaben** wurde entfernt. 

## <a name="multidimensional-pricing"></a>Mehrdimensionale Preisberechnung
Um die Flexibilität zu maximieren und verschiedene geschäftliche Anforderungen einzuhalten, unterstützt Version 3 von Project Service Automation diskrete Preisberechnung von Preisdimensionssätzen in Kosten und Rechnungssätze. Dimensionswerte können als Standard festgelegt werden und dann im Kostenberechnungs- und Preisberechnungsprozess der Ressource von der Profilerstellung über die Zeiteinträge und Projekt-Istwerte verteilt werden. Kundenspezifische Konfiguration und Änderung oder Erweiterung nutzt Standardanpassbarkeitsinfrastruktur.

Project Service Automation wird standardmäßig mit einem Satz an Preisberechnungsdimensionen und Rollen und Ressourceneinheiten ausgeliefert und ermöglicht die Einrichtung von Preisen und Kosten für jede Rollen- und Organisationseinheitkombination.

Für Kunden von Project Service Automation, die weiterhin vordefinierte Felder als Preisdimension in Version 3 verwenden möchten, entsteht keine wahrnehmbare Änderung. Sie können Project Service Automation wie gehabt verwenden. Wenn Sie jedoch Preise oder Kosten für die Ressourcen mit weiteren zusätzliche Attribute verwenden müssen, bietet Version 3 die Möglichkeit, eigene benutzerdefinierte Preisberechnungsdimensionen zu Project Service Automation hinzuzufügen. Die Erweiterung benutzerdefinierter Preisberechnungsdimensionen ist eine komplizierte Konfigurationserfahrung. 

## <a name="quotes-and-contracts"></a>Angebote und Verträge
In Version 3 von Project Service Automation haben sich die Aspekte des Setups und der Verwaltung von Angeboten und Verträgen geändert. Die folgenden Abschnitte enthalten ausführlichere Informationen.

### <a name="set-up-chargeability-options"></a>Einrichten von Fakturierbarkeitsoptionen
In den Versionen 1 und 2 wurde das Fakturierbarkeitssetup für Rollen und Kategorien sowie für bestimmte Angebote und Verträge mithilfe der Ansicht **Fakturierbarkeit** erledigt, die sich in der obersten Navigation einer Angebotszeile oder einer Vertragszeile befand. Dort wurden auch die Preise für diesen Rollen und Ausgabenkategorien festgelegt.

Ab Version 3 werden die Fakturierbarkeitsoptionen nach Rolle und Ausgabenkategorie auf der Angebots- oder Vertragszeilenebene ausgeführt. Das Preisberechnungssetup ist getrennt vom Fakturierbarkeitssetup. Sie finden **Fakturierbare Rollen** und **Fakturierbare Kategorie** als Registerkarten auf den Seiten **Angebotszeile** und **Vertragszeile**, ohne dafür die obere Navigation verwenden zu müssen.

![Fakturierbare Rollen.](media/chargeable-12.png)
 
Die Einrichtung der fakturierbaren Rollen und fakturierbaren Kategorien nutzt auch das vordefinierte bearbeitbare Rastersteuerelement. Für jede Rolle und Kategorie bleiben die unterstützten Optionen zum Berechnen des Typs der Veranschlagung und der Vertragsphase unverändert zu früheren Versionen mit **Fakturierbar** und **Nicht fakturierbar**. **Kostenlos** ist kein unterstützter Typ während der Veranschlagungs- oder Vertragsphase. **Kostenlos** wird nur bei der Zeit- und Ausgabengenehmigung unterstützt.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Erstellen und bearbeiten Sie die benutzerdefinierte Preisberechnung für einen Project Service Automation Angebots- und -Projektvertrag
In den Versionen 1 und 2 wurde die angepasste Preisliste für bestimmte Angebote und Verträge mithilfe der Ansichten **Preise bearbeiten** und **Fakturierbarkeit** ausgeführt. Die Ansicht **Fakturierbarkeit** befand sich in der obersten Navigation oder der Angebotszeile einer Vertragszeile. Dort wurden auch die Fakturierbarkeitsoptionen für Rollen und Ausgabenkategorien festgelegt.

Ab Version 3 ist das Erstellen und Verwenden einer benutzerdefinierten Projektpreisliste in einem Project Service Automation Angebots- und Project Service Automation Projektvertrag vom Fakturierbarkeitssetup getrennt. Das Angebot für Project Service Automation und die Projektverträge für Project Service Automation haben eine neue Registerkarte mit dem Namen **Projektpreislisten**. Diese Registerkarte zeigt eine zugeordnete Ansicht für Projektpreislisten an, die dem Project Service Automation Angebots- oder -Projektvertrag angefügt werden. Zum Erstellen einer benutzerdefinierten Preisliste aus einer vorhandenen Preisliste, die bereits dem Projekt-Angebot oder -Vertrag zugeordnet ist, klicken Sie auf **Benutzerdefinierte Preisberechnung erstellen** Dadurch wird eine Kopie aller zugeordneten Preislisten erstellt und dem Angebot oder Vertrag angefügt. Sie können die Preisliste jetzt öffnen und Rollen oder Ausgabenkategoriepreise bearbeiten, sodass diese Preisberechnungsänderungen nur für dieses Angebot oder Vertrag gelten. 
  
Die folgende Grafik stellt den Zeitpunkt dar, bevor Listen des benutzerdefinierten Preises erstellt wurden.

![Vor benutzerdefinierten Preislisten.](media/before-custom-price-lists-13.png)

Die folgende Grafik stellt den Zeitpunkt dar, nachdem Listen des benutzerdefinierten Preises erstellt wurden.

![Nach benutzerdefinierten Preislisten.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Eine kurze Verzögerung zwischen dem Klicken auf **Benutzerdefinierte Preisberechnung erstellen** kann auftreten, wenn die Liste des benutzerdefinierten Preises erstellt wird. Es ist empfehlenswert, das Raster zu aktualisieren, anstatt mehrmals zu klicken. Eine Liste von benutzerdefinierten Preises wird erstellt, wenn dem Preislistenname der Angebotsname oder der Projektvertragsname angefügt wurde.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
