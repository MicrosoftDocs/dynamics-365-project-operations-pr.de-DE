---
title: Angebote und Angebotszeilen
description: Dieses Thema enthält Informationen zu Angeboten und Angebotszeilen.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
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
ms.openlocfilehash: e5b0dfb3db2ddc6d43545a0f1f9429e343e830b5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291123"
---
# <a name="quotes-and-quote-lines"></a>Angebote und Angebotszeilen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In Dynamics 365 Project Service Automation gibt es zwei Typen von Angeboten: Projektangebote und Vertriebsangebote. Die zwei Typen unterscheiden sich folgendermaßen:

- Bei einem Verkaufsangebot gibt es nur ein Raster für Vertragszeilen. Bei einem Projektangebot gibt es zwei Raster für Vertragszeilen: eines für Projektzeilen und eines für Produktlinien.
- Ein Vertriebsangebot unterstützt die Aktivierung und Revisionen. Ein Projektangebot unterstützt diese Prozesse nicht.
- Sie können mehrere Aufträge einem Vertriebsangebot anfügen. Sie können nur einen Projektvertrag einem Projektangebot anfügen.
- Sie können ein Vertriebsangebot gewinnen und die verknüpfte Verkaufschance geöffnet lassen. Wenn ein Projektangebot gewonnen wird, wird die verknüpfte Verkaufschance geschlossen.
- Ein Vertriebsangebot enthält einige Felder und Konzepte nicht, die in einem Projektangebot enthalten sind. Die Felder enthalten **Vertragseinheit**, **Kontomanager** und **Kontaktname für Rechnungsadresse**.  
- Vertriebsangebote und Projektangebote werden ebenfalls über ein optionssatzbasiertes Feld namens **Typ** ermittelt. Für ein Verkaufsangebot hat dieses Feld den Wert **Elementbasiert**. Für ein Projektangebot hat es den Wert **Arbeitsbasiert**.

Dieses Thema konzentriert sich auf die Details von Projektangeboten.

Ein Projektangebot in PSA kann mehrere Vertragszeilen oder Angebotszeilen haben. Tatsächlich hat ein Projektangebot zwei Raster für Vertragszeilen. Ein Raster dient für projektbasierte Zeilen, die ausführliche Schätzungen ermöglichen. Das andere Raster ist für produktbasierte Zeilen, die einen einfachen Einheitenpreis und eine mengenbasierte Herangehensweise verwenden.

- **Projektbasiert** – Der Betrag (Angebotswert) wird bestimmt, nachdem Sie geschätzt haben, wie viel Arbeit erforderlich ist. Sie können die Arbeit auf einer hohen Ebene schätzen, oder Sie können sie direkt als Zeilendetails unter den einzelnen Angebotszeilen schätzen. Schließlich können Sie die Arbeit auch basierend auf grundlegenden Schätzungen einschätzen, und zwar indem Sie ein Projekt und einen Projektplan verwenden. Projektbasierte Angebotszeilen sind nur bei projektbasierten Angeboten zu finden, die mithilfe der Project Service Automation erstellt werden. Diese Art der Angebotszeile ist eine benutzerdefinierte Form der manuell auszufüllenden Zeilen, die in Microsoft Dynamics 365 Sales verfügbar sind.
- **Produktbasiert** – Der Betrag (Angebotswert) wird basierend auf der Menge an Einheiten, die verkauft wird, sowie auf dem Einheitenverkaufspreis des Produkts bestimmt. Das Produkt bei einer produktbasierten Zeile kann von einem Produktkatalog in Sales stammen, oder es kann ein von Ihnen festgelegtes Produkt sein. Diese Art der Angebotszeile ist auch bei projektbasierten Angeboten verfügbar, die mithilfe von PSA erstellt werden.

Der Betrag eines Angebots ist die Gesamtsumme der produktbasierten und projektbasierten Zeilen.

> [!NOTE]
> Angebote und Angebotszeilen sind in PSA nicht erforderlich. Sie können den Projektprozess mit einem Projektvertrag (verkauftes Projekt) beginnen. Eine Verkaufschance ist jedoch immer erforderlich, unabhängig davon, ob Sie mit einem Angebot oder einem Projektvertrag beginnen.

## <a name="project-based-quote-lines"></a>Projektbasierte Angebotszeilen

Eine projektbasierte Angebotszeile in PSA hat die folgenden Abrechnungsmethoden:

- Zeit und Materialien
- Festpreis

### <a name="time-and-material"></a>Zeit und Materialien

Die Zeit und die Materialabrechnungsmethode basiert auf dem Verbrauch. Wenn Sie diese Abrechnungsmethode auswählen, werden dem Kunden alle anfallenden Kosten in Rechnung gestellt. Rechnungen werden anhand einer datumsbasierten regelmäßigen Frequenz erstellt. Während des Vertriebsprozesses gibt der Angebotswert einer Komponente für Zeit und Materialien nur eine Schätzung der finalen Kosten für den Kunden an. Der Zulieferer verpflichtet sich nicht dazu, das Projekt genau zu dem Angebotswert abzuschließen. Komponenten für Zeit und Materialien erhöhen das Risiko des Kunden. Kunden möchten unter Umständen über zusätzliche Klauseln verhanden, die nicht überschritten werden dürfen, um ihr Risiko zu minimieren. PSA unterstützt nicht die Einstellung von Klauseln, die nicht überschritten werden dürfen.

### <a name="fixed-price"></a>Festpreis

Bei der Abrechnungmethode „Festpreis” verpflichtet sich ein Zulieferer dazu, das Projekt zu einem Festpreis an den Kunden zu liefern. Dem Kunden wird der Angebotswert der Angebotszeile mit dem Festpreis in Rechnung gestellt, unabhängig von den Kosten, die dem Zulieferer bei der Lieferung dieser Angebotszeile entstehen. Der Wert der Angebotszeile mit dem Festpreis wird auf eine der folgenden Arten in Rechnung gestellt: 

- Als Pauschalbetrag am Anfang oder Ende des Projekts, oder wenn ein Projektmeilenstein erreicht ist. 
- In einer datumsbasierten Frequenz mit gleichen Raten des festen Wertes in der Angebotszeile. Diese Raten werden auch regelmäßige Meilensteine genannt.
- Bei Raten mit einem monetären Wert, die auf den Fortschritt der Arbeit oder spezifische Meilensteine ausgerichtet werden, die im Rahmen des Projekts erreicht werden. In diesem Fall kann sich der Wert für die einzelnen Raten unterscheiden, aber alle zusammen müssen den Festpreis in der Angebotszeile ergeben.

PSA unterstützt alle drei Typen von Rechnungszeitplänen für Angebotszeilen mit Festpreis.

## <a name="transaction-classification"></a>Transaktionsklassifizierung

Organisationen für professionelle Services erstellen für ihre Kunden Angebote und Rechnungen für gewöhnlich basierend auf einer Klassifizierung von Kosten. In PSA werden die Kosten anhand der folgenden Transaktionsklassifizierungen dargestellt:

- **Zeit** – Diese Klassifizierung stellt den Arbeitslohn oder die Zeit des Personals für ein Projekt dar.
- **Ausgaben**: Diese Klassifizierung stellt alle anderen Arten von Ausgaben bei einem Projekt dar. Da Ausgaben breit klassifiziert werden können, erstellen die meisten Organisationen Unterkategorien, wie Reisekosten, Automiete, Hotelkosten oder Bürobedarf.
- **Gebühr** – Diese Klassifizierung stellt die verschiedenen Aufwände, Strafen und andere Elemente dar, die dem Kunden in Rechnung gestellt werden. 
- **Steuer** – Diese Klassifizierung stellt die Steuerbeträge dar, die Benutzer hinzufügen, während sie die Ausgaben eingeben.
- **Materialtransaktion** – Diese Klassifizierung stellt die tatsächlichen Werte von Produktzeilen auf einer bestätigten Projektrechnung dar.
- **Meilenstein** – Diese Klassifizierung wird von der Abrechnungslogik mit Festpreis in PSA verwendet.

Eine oder mehrere dieser Transaktionsklassifizierungen können den einzelnen Angebotszeilen zugeordnet werden. Nachdem ein Angebot gewonnen wurde, wird das Mapping zwischen der Transaktionsklassifizierung und der Angebotszeile an die Vertragszeile übertragen.
 
> ![Screenshot der Mappings von Transaktionstypen zu Angeboten und Vertragszeilen](media/basic-guide-5.png)
  
Beispielsweise könnte ein Angebot die folgenden zwei Angebotszeilen enthalten: 
- Eine Beratung, bei der eine Abrechnungsmethode für Zeit und Materialien verwendet wird, wobei Zeit- und Gebührentransaktionsklassifizierungen gelten. Beispielsweise werden alle Zeit- und Gebührentransaktionen für das Beispielprojekt **Dynamics AX-Implementierung** dem Kunden basierend auf der eingesetzten Zeit und den verwendeten Materialien in Rechnung gestellt. 
- Zugehörige Reisekosten, die eine Abrechnungsmethode mit Festpreis verwenden. Beispielsweise werden alle Reisekosten für das Beispielprojekt **Dynamics AX-Implementierung** zu einem monetären Festwert in Rechnung gestellt.

> [!NOTE]
> Die Kombination der Projekt- und Transaktionsklassifizierungen **Zeit**, **Ausgaben** und **Gebühr**, die einer Angebots- oder Vertragszeile zugeordnet sind, müssen eindeutig sein. Wenn die gleiche Kombination einer Projekt- und Transaktionsklasse mehreren Vertrags- oder Angebotszeilen zugeordnet ist, funktioniert PSA nicht ordnungsgemäß.

## <a name="billing-types"></a>Abrechnungstypen

Mit dem Feld **Abrechnungstyp** wird das Konzept der Fakturierbarkeit in PSA definiert. Es ist ein Optionssatz, der über die folgenden möglichen Werte verfügt:

- **Fakturierbar** – Die Kosten, die über diese Rolle/Kategorie anfallen, sind direkte Kosten, die die Projektausführung fördern. Der Kunde zahlt für diese Arbeit. Die Zahlung kann im Rahmen der Methode für Zeit und Materialien oder für einen Festpreis verwaltet werden. Allerdings erhält der Mitarbeiter, der diese Zeit dafür aufwendet, die entsprechende Gutschrift für seine Nutzung.
- **Nicht fakturierbar** – Die Kosten, die über diese Rolle/Kategorie anfallen, werden als direkte Kosten betrachtet, die die Projektausführung fördern, auch wenn der Kunde diese Tatsache nicht anerkennt und für diese Arbeit nicht zahlt. Der Mitarbeiter, der diese Zeit aufwendet, erhält keine Gutschrift mit einer abrechenbaren Nutzung dafür.
- **Kostenlos** – Die Kosten, die über diese Rolle/Kategorie anfallen, werden als direkte Kosten betrachtet, die die Projektausführung fördern, und der Kunde erkennt diese Tatsache an. Der Mitarbeiter, der diese Zeit aufwendet, erhält dafür eine Gutschrift für eine abrechenbare Nutzung. Diese Kosten werden dem Kunden jedoch nicht in Rechnung gestellt.
- **Nicht verfügbar** – Die Kosten, die für interne Projekte entstehen, und für die keine Umsatzverfolgung erforderlich ist, werden mithilfe dieser Option nachverfolgt.

## <a name="invoice-schedule"></a>Rechnungszeitplan

Ein Rechnungszeitplan ist eine Reihe von Datumsangaben, an denen die Abrechnung für ein Projekt fällig ist. Sie können optional einen Rechnungszeitplan in einer Angebotszeile in PSA erstellen. Jede Angebotszeile kann einen eigenen Rechnungszeitplan haben. Um einen Rechnungszeitplan zu erstellen, müssen die folgenden Attributwerte zur Verfügung gestellt werden:

- Ein Startdatum für die Abrechnung 
- Ein Lieferdatum, das das Enddatum der Abrechnung für das Projekt darstellt
- Eine Abrechnungshäufigkeit

PSA verwendet diese drei Attributwerte, um einen vorläufigen Satz an Datumsangaben zu generieren, anhand derer die Abrechnung eingerichtet wird.

## <a name="invoice-frequency"></a>Rechnungshäufigkeit

Die Rechnungshäufigkeit ist eine Entität, bei der Attributwerte gespeichert werden, die dabei helfen, die Häufigkeit der Rechnungserstellung auszudrücken. Der folgende Attribute drücken die Entität für die Rechnungshäufigkeit aus oder definieren sie:

- **Periode** – Monatlich, zweiwöchentlich und wöchentliche Perioden werden unterstützt. 
- **Ausführungen pro Periode** – Für wöchentliche und zweiwöchentliche Perioden können Sie nur eine Ausführung pro Periode definieren. Für Perioden von einem Monat können Sie zwischen einer und vier Ausführungen pro Periode definieren. 
- **Tage der Ausführung** – Die Tage, an denen die Rechnungsstellung ausgeführt werden soll. Sie können dieses Attribut auf zwei Arten konfigurieren:
  - **Wochentage** – Zum Beispiel können Sie angeben, dass die Rechnungsstellung jeden Montag oder jeden zweiten Montag ausgeführt werden soll. Kunden, die festlegen müssen, dass die Rechnungsstellung an einem Werktag ausgeführt werden soll, bevorzugen unter Umständen diese Art der Konfiguration. 
  - **Kalendertage** – Sie können zum Beispiel angeben, dass die Rechnungsstellung am siebten und einundzwanzigsten Tag jedes Monats ausgeführt wird. Einige Organisationen bevorzugen unter Umständen diese Art der Konfiguration, weil damit garantiert werden kann, dass die Rechnungsstellung jeden Monat gemäß einem festen Zeitplan ausgeführt wird.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Rechnungszeitplan für eine Angebotszeile mit Festpreis

Für eine-Angebotszeile mit Festpreis können Sie das Raster **Rechnungszeitplan** verwenden, um Abrechnungsmeilensteine zu erstellen, die dem Wert der Angebotszeile entsprechen.

- Um Abrechnungsmeilensteine zu erstellen, die gleichmäßig aufgeteilt werden, wählen Sie eine Rechnungshäufigkeit aus, geben Sie das Startdatum für die Abrechnung in die Angebotszeile ein, und wählen Sie **Angefordertes Abschlussdatum** für das Angebot im Abschnitt **Zusammenfassung** der Angebotskopfzeile aus. Wählen Sie dann **Periodische Meilensteine generieren** aus, um gleichmäßig aufgeteilte Meilensteine basierend auf der ausgewählten Rechnungsfrequenz zu erstellen. 
- Um einen Meilenstein mit Pauschalabrechnung zu erstellen, erstellen Sie einen Meilenstein und geben Sie den Wert der Angebotszeile als Meilensteinbetrag ein.
- Um Abrechnungsmeilensteine zu erstellen, die auf bestimmten Aufgaben im Projektplan basieren, erstellen Sie einen Meilenstein und ordnen Sie ihn dem Zeitplanelement in der Abrechnungsmeilenstein-Benutzeroberfläche zu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]