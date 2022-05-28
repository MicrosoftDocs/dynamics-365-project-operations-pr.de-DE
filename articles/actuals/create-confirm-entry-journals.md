---
title: Eingangserfassungen erstellen und bestätigen
description: Dieses Thema enthält Informationen zum Erstellen und Bestätigen von Eingangserfassungen in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584227"
---
# <a name="create-and-confirm-entry-journals"></a>Eingangserfassungen erstellen und bestätigen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Sie verwenden Eingangserfassungen, um Ist-Werte direkt in Microsoft Dynamics 365 Project Operations zu erfassen. Wenn Sie Eingangserfassungen verwenden, müssen Sie keine Zeit-, Ausgaben- und Materialnutzungsprotokolle in Project Operations eingeben.

Mit einer einzelnen Eingangserfassung können Sie mehrere Journaleinträge erstellen. Wenn das Journal bestätigt wird, zeichnet eine Eingangserfassungsposition den Ist-Wert für die folgenden Details auf:

- Die Kosten oder Einnahmen, je nach ausgewähltem Transaktionstyp.
- Die ausgewählte Klasse der Transaktion. Die verfügbaren Klassen sind **Zeit**, **Ausgaben**, **Material**, **Vorschuss**, **Meilenstein** und **Steuer**.
- Das Projekt und/oder eine Aufgabe, die in der Erfassungsposition ausgewählt ist.

Befolgen Sie diese Schritte, um eine Eingangserfassung in Project Operations zu erstellen.

1. Gehen Sie zu **Vertrieb** \> **Transaktionen** \> **Erfassungen**.
2. Wählen Sie auf der **Eingangserfassungen**-Listenseite im Aktivitätsbereich **Neu** aus, um eine Erfassung zu erstellen.
3. Geben Sie auf der **Neue Erfassung**-Seite im Feld **Beschreibung** eine Beschreibung der Erfassung ein.
4. Stellen Sie sicher, dass das **Erfassungstyp**-Feld auf **Eintrag** eingestellt ist, und wählen Sie dann **Speichern** aus. Nachdem die neue Eingangserfassung gespeichert wurde, sollte eine **Erfassungspositionen**-Registerkarte auf der Erfassungsseite erscheinen.
5. Wählen Sie auf der Registerkarte **Erfassungspositionen** über dem Raster in der Symbolleiste **Neu** aus, um eine Eingangserfassungsposition zu erstellen.
6. Legen Sie im Dialogfeld **Schnell erstellen** zum Erstellen einer Eingangserfassungsposition die Felder wie in der folgenden Tabelle beschrieben fest.

    | Feld | Beschreibung des Dataflows | Funktionsauswirkung |
    | --- | --- | --- |
    | Transaktionsklasse | Die Erfassungsposition kann in eine der sechs Transaktionsklassen eingeteilt werden: **Zeit**, **Ausgaben**, **Material**, **Vorschuss**, **Meilenstein** oder **Steuer**. | Die Transaktionsklasse **Steuer** ist in Project Operations veraltet. <br> Wenn Sie eine **Steuer**-Transaktionsklasse erstellen, wird sie nicht von der Rechnungsstellung oder in Kosten- oder Erlösberechnungen verarbeitet. **Meilenstein** ist eine Transaktionsklasse, die sich nur auf den Umsatz bezieht. <br>Die **Vorschuss**-Transaktionsklasse stellt einen Vorschuss dar, der von einem Kunden erhalten wurde. Es sollte immer als ein Paar aus fakturierten Verkäufen und nicht fakturierten Verkaufserfassungspositionen erstellt werden. |
    | Transaktionstyp | Die Transaktionstypen **Kosten**, **Interorg-Vertrieb** und **Einheitskosten für Ressourcen** sollten verwendet werden, um Kosten zu erfassen.<br> Die Transaktionstypen **Nicht fakturierte Verkäufe** und **Abgerechneter Umsatz** sollten verwendet werden, um Einnahmen zu erfassen. | Die Transaktionsklasse **Vorschussr** funktioniert nur mit den Transaktionstypen **Nicht fakturierte Verkäufe** und **Abgerechneter Umsatz**.<br> Die **Meilenstein**-Transaktionsklasse funktioniert nur mit dem Transaktionstyp **Abgerechneter Umsatz**. <br>Die Transaktionstypen **Interorg-Vertrieb** und **Einheitskosten für Ressourcen** gelten nur für die **Zeit**-Transaktionsklasse und diese sind nur für Eingangserfassungen im Lite-Bereitstellungsszenario verfügbar und nicht beim Bereitstellen von Project Operations in den Szenarios „Ressource/Nicht auf Lager“. |
    | Produkt auswählen | Wenn die **Material**-Transaktionsklasse ausgewählt ist, können Sie in diesem Feld angeben, ob es sich bei der Materialbuchung, für die Sie die Erfassungszeile erstellen, um ein vorhandenes Produkt oder um ein manuell einzutragendes Produkt handelt. | Wenn Sie **Manuell einzutragendes Produkt** auswählen, können Sie einen Namen für das Produkt eingeben. |
    | Produkt | Ein Verweis auf das Produkt aus dem Katalog. | |
    | Beschreibung des Dataflows | Eine Beschreibung der Erfassungsposition, um sie leichter identifizieren zu können. | Für nicht fakturierte Vertriebserfassungspositionen wird der Wert als Beschreibung verwendet, wenn die Rechnungspositionsdetails erstellt werden. |
    | Externe Beschreibung | Eine Beschreibung der Erfassungsposition, die für den Austausch mit externen Stakeholdern verwendet werden kann. | Für nicht fakturierte Vertriebserfassungspositionen wird der Wert als externe Beschreibung verwendet, wenn die Rechnungspositionsdetails erstellt werden. Sie kann auch auf der Rechnung erscheinen, die an den Kunden gesendet wird. |
    | Fakturierungstyp | Ein Wert, der angibt, ob die Erfassungsposition als gebührenpflichtige, kostenlose oder nicht gebührenpflichtige Komponente des Projekts gezählt wird. | In einem typischen Ablauf wird der Fakturierungstyp von den vereinbarten Bedingungen abgeleitet, die im Vertrag festgelegt sind. Wenn Sie jedoch eine Erfassungsposition erfassen, können Sie einen Wert in dieses Feld eingeben. |
    | Dokumentdatum | Verwenden Sie ein Datum, an dem diese Transaktion stattgefunden hat. | |
    | Startdatum | Verwenden Sie das Datum, an dem diese Transaktion stattgefunden hat. | Dieses Feld dient zum Abgleich mit dem Datum der Rechnungserstellung für Transaktionen des Typs **Nicht fakturierte Verkäufe**. Dieser Vergleich hilft Ihnen bei der Entscheidung, ob die Transaktion in der Zukunft oder in der Vergangenheit datiert ist. Der Rechnung werden nur vergangene Transaktionen hinzugefügt. |
    | Enddatum | Verwenden Sie das Datum, an dem diese Transaktion stattgefunden hat. | |
    | Buchhaltungsdatum | Verwenden Sie das Datum, an dem die Auswirkungen auf die Buchhaltung erfasst werden. | |
    | Vertragszeilenkunde | Wenn die Vertragszeile nur einen Kunden hat, wird dieses Feld standardmäßig auf den Kunden in der Vertragszeile gesetzt, wenn die Erfassungsposition gespeichert wird. Wenn die Vertragsposition mehrere Kunden hat, wählen Sie den richtigen Kunden in der Vertragszeile aus. | Wenn das System den Vertragszeilenkunden in der Erfassungsposition nicht ermitteln kann und diese in der Ist-Position des Typs **Nicht fakturierte Verkäufe** leer ist, der aus der Erfassungszeile erstellt wird, wird der Ist-Wert nicht fakturiert. |
    | Project | Wählen Sie das Projekt aus, für das der Ist-Wert aufgezeichnet werden soll. | Basierend auf dem ausgewählten Projekt, der Transaktionsklasse und der Aufgabe versucht das System, den Vertrag, die Vertragszeile und den Vertragszeilenkunden zu ermitteln. |
    | Task | Wählen Sie die Aufgabe aus, für das der Ist-Wert aufgezeichnet werden soll. | Wenn Sie während der Vertragseinrichtung Aufgaben mit Vertragszeilen verknüpft haben, verwendet das System die ausgewählte Aufgabe zusammen mit einem Projekt und einer Transaktionsklasse, um den Vertrag, die Vertragszeile und den Vertragszeilenkunden zu bestimmen. |
    | Transaktionskategorie | Wählen Sie die Transaktionskategorie, für die der Ist-Wert aufgezeichnet werden soll. | Für Ausgaben bestimmt die ausgewählte Transaktionskategorie den Standardpreis, der beim Speichern in die Erfassungsposition eingegeben wird. |
    | Role | Dieses Feld ist für Zeiterfassungszeilen relevant. Wählen Sie die Rolle der Ressource aus, die Zeit für das Projekt und/oder die Aufgabe aufgewendet hat. | Wenn Sie für Zeiterfassungspositionen die Standardkonfiguration für die Eingabe von Standardressourcenkosten und Rechnungssätzen verwenden, wird die ausgewählte Rolle zusammen mit der Ressourceneinheit verwendet, um den Standardpreis zu bestimmen, der in die Erfassungsposition eingegeben wird, wenn sie gespeichert wird. Wenn Sie eine benutzerdefinierte Konfiguration für die Eingabe von Standardpreisen verwenden, sollten Sie diese Konfiguration überprüfen, um festzustellen, ob das **Rolle**-Feld verwendet wird, um Standardpreiswerte einzugeben. |
    | Fremdarbeit | Wenn die Erfassungsposition fremdvergebene Kapazität oder fremdvergebene Ausgaben oder Materialien darstellt, wählen Sie den entsprechenden Untervertrag aus. | Wenn Kostenerfassungspositionen erfasst werden, bestimmt der ausgewählte Untervertrag die Preisliste, die verwendet wird, um die Standardeinheitskosten einzugeben. |
    | Fremdarbeitsposition | Wenn die Erfassungsposition fremdvergebene Kapazität oder fremdvergebene Ausgaben oder Materialien darstellt, wählen Sie die entsprechende Untervertragsposition aus. | Wenn Kostenerfassungspositionen erfasst werden, stellt die ausgewählte Untervertragsposition sicher, dass die verfügbaren Kapazitätsberechnungen für die Untervertragsposition korrekt berechnet werden. |
    | Betragsmethode | Standardmäßig ist dieses Feld auf **Menge mit Preis multiplizieren** festgelegt. Bei dieser Methode wird der Betrag wie folgt als *Menge* ×*Preis* berechnet. Die andere unterstützte Methode ist **Festpreis**. Wenn diese Methode verwendet wird, wird der Preis auf den Betrag festgelegt und die Menge wird nicht in die Berechnung einbezogen. | |
    | Einheitenplan und Einheit | Der Einheitenplan und die Einheit identifizieren zusammen die Einheit der Menge. | Die Kombination aus Einheit und Transaktionstyp wird verwendet, um Standardpreise für Ausgaben einzugeben. In der Standardkonfiguration von Project Operations wird die Kombination aus Einheit, Rolle und Ressourceneinheit verwendet, um Standardpreise für die Zeit einzugeben. Wenn Sie eine benutzerdefinierte Konfiguration für die Eingabe von Standardpreisen haben, wird diese zusammen mit der Einheit verwendet. Die Kombination aus Produkt und Einheit wird verwendet, um Standardpreise für Materialien einzugeben. |
    | Menge | Geben Sie die Menge ein. | |
    | Preis | Wenn der Preis beim Erstellen der Erfassungsposition leer gelassen wird, werden die entsprechenden Werte verwendet, um die Standardpreise abhängig von der Transaktionsklasse einzugeben. Wenn beim Erstellen der Erfassungsposition ein Preis eingegeben wird, wird dieser Preis verwendet. | |
    | Steuer | Geben Sie einen beliebigen Steuerbetrag ein. | Abhängig vom eingegebenen Steuerbetrag wird der erweiterte Betrag als *Menge* + *Steuer* berechnet. |

## <a name="confirm-an-entry-journal"></a>Bestätigen einer Eingangserfassung

Nachdem Sie alle Erfassungspositionen in eine Eingangserfassung eingegeben haben, können Sie die Erfassung bestätigen. Dieser Prozess erfasst jede Erfassungsposition als Ist-Werte für die entsprechenden Projekte.

Nachdem eine Erfassung bestätigt wurde, können Sie sie oder eine ihrer Zeilen nicht mehr bearbeiten.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Ist-Werte, die durch Bestätigung des Eingangserfassung erstellt wurden

Es gibt einige wichtige Unterschiede zwischen Ist-Werten, die durch die Bestätigung der Eingangserfassung erstellt werden, und Ist-Werten, die während der Genehmigung von Zeit-, Ausgaben- und Materialverwendungsprotokollen und der Rechnungsbestätigung in Project Operations erstellt werden:

- Eingangserfassungen verwenden keine Transaktionsverbindungen, um die Kosten-Ist-Werte mit den Ist-Werten von nicht fakturierten Verkäufen zu verknüpfen. Die Ist-Werte, die erstellt werden, wenn Zeit-, Kosten- und Materialverbrauchsprotokolle genehmigt werden, verwenden immer Transaktionsverbindungen, um die Ist-Werte für Kosten und nicht fakturierte Verkäufe zu verknüpfen.
- Eingangserfassungen verwenden keine Transaktionsursprünge, um die Kosten-Ist-Werte und die Ist-Werte von nicht fakturierten Verkäufen mit beliebigen ursprünglichen Datensätzen zu verknüpfen. Die Ist-Werte, die erstellt werden, wenn Zeit-, Kosten- und Materialverbrauchsprotokolle genehmigt werden, verwenden immer Transaktionsursprünge, um die Ist-Werte für Kosten und nicht fakturierte Verkäufe mit dem ursprünglichen Zeiteintrag zu verknüpfen.
- Wenn Ist-Werte von nicht fakturierten Verkäufen, die durch Eingangserfassungsbestätigung erstellt wurden, fakturiert werden, werden die fakturierten Verkaufs-Ist-Werte, die während der Rechnungsbestätigung erstellt werden, mit den Ist-Werten für nicht fakturierte Verkäufe verknüpft, ähnlich wie die Ist-Werte für nicht fakturierte Verkäufe, die erstellt werden, wenn Zeit-, Ausgaben- und Materialnutzungsprotokolle genehmigt werden.
- Eingangserfassungspositionen, die für die Zeit erstellt werden, die von organisationsübergreifenden Ressourcen eingegeben wird, verursachen nicht, dass Ist-Werte der Typen **Einheitskosten für Ressourcen** und **Interorg-Vertrieb** automatisch erstellt werden. Diese Ist-Werte müssen manuell erstellt werden. Dieses Verhalten unterscheidet sich von dem Verhalten für Zeiteinträge, die von organisationsübergreifenden Ressourcen erfasst werden. In diesem Fall erstellt die Anwendung nach Genehmigung der Zeit automatisch Ist-Werte des Typs **Kosten** für das Projekt und die Ist-Werte für **Einheitskosten für Ressourcen** und **Interorg-Vertrieb** werden in der zuständigen Abteilung des Mitarbeiters erstellt. Dann werden Transaktionsverbindungen verwendet, um diese Ist-Werte miteinander zu verknüpfen, und Transaktionsursprünge, um sie mit dem ursprünglichen Zeiteintrag zu verknüpfen.
- Wenn Eingangserfassungen bestätigt werden, erstellen sie Ist-Werte. Korrekturerfassungen können jedoch nicht verwendet werden, um diese Ist-Werte zu korrigieren. Dieses Verhalten unterscheidet sich von dem Verhalten für Ist-Werte, die erstellt werden, wenn Zeit-, Ausgaben- und Materialverwendungsprotokolle genehmigt werden. In diesem Fall ermöglicht die Anwendung die Verwendung von Korrekturerfassungen zum Korrigieren der Ist-Werte, um Fehler zu beheben, vorausgesetzt, dass diese Ist-Werte noch nicht fakturiert wurden. Wenn sie bereits fakturiert wurden, können Sie eine Ist-Rechnung dennoch korrigieren, wenn Sie eine vollständige Gutschrift dieser Ist-Rechnung an den Debitor verarbeiten.

> [!NOTE]
> Eingangserfassungen erzwingen keine strengen Standardregeln. Verwenden Sie daher diese Eingangserfassungen so wenig wie möglich und gehen Sie vorsichtig vor, um sicherzustellen, dass Sie keine beschädigten Finanzdaten in Ihrem System erstellen. Verwenden Sie nach Möglichkeit Zeit-, Ausgaben- und Materialverbrauchsprotokolle, die Einrichtung von Meilensteinen und Vorschüssen in Projektverträgen und den Bestätigungsprozess für Projektrechnungen anstelle von Eingangserfassungen, um Ist-Werte zu erstellen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
