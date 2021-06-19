---
title: Projektkosten und Umsatz
description: Dieses Thema enthält Informationen zum Schätzen der Projektkosten und des Umsatzes.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 48f313b15f788645b88a4d878e3bece419d63126
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009165"
---
# <a name="project-costs-and-revenue"></a>Projektkosten und Umsatz

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekteinschätzungen stellen die Finanzansicht für die Arbeit bereit, die im Projektplan geschätzt und geplant wird. Die Registerkarte **Schätzungen** auf der **Projekte** zeigt die Kosten- und Umsatzauswirkungen der Arbeit an, die Sie planen. Sie enthält auch Informationen zu vielen vordefinierten Dimensionen. 

> ![Registerkarte „Schätzungen“](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Kosten- und Verkaufswerte des Projektes

Preislisten definieren die Kosten und die Rechnungssätze in Projekten. Sie können die Kosten- und Umsatzauswirkungen basierend auf den Rollen bestimmen, die dem Positionsnamen und der benannten Ressource zugeordnet sind, die einer Aufgabe zugewiesen sind. Wenn Aufgaben vorliegen, die keine Zuweisungen (generisch oder benannt) haben, können Sie keine Kosten- oder Umsatzschätzungen abrufen. Kosten- und Umsatzwerte beziehen das Datum mit ein, das in den preislisten definiert ist.

### <a name="default-cost-price"></a>Standard-Einstandspreise  

Jedes Projekt gehört einer Organisation. Diese Organisation wird im Feld **Vertragseinheit** des Projekts angezeigt. Die Preisliste, die der Vertragseinheit zugeordnet ist, wird verwendet, um den Einstandspreis pro Einheit zu ermitteln. Um die richtigen Einstandspreise der Rollen für das Datum zu ermitteln, das in Vorkalkulationsposition festgelegt ist, suchen Sie nach der Kombination aus Rolle, Einheit und Organisationseinheit in der Einstandspreisliste. 

Damit die Einstandspreise berechnet werden können, müssen alle Aufgaben einer Ressource zugeordnet sein. Alle nicht zugewiesenen Aufgaben haben einen Einstandspreis von 0,00.

Wenn die Kombination der Rolle, der Einheit und der Organisationseinheit keinen Einstandspreis aus der Preisliste der Vertragseinheit zurückgibt, ignoriert das System die Einheit. Stattdessen sucht es nach der Kombination aus Rolle und Organisationseinheit. Wenn ein Einstandspreis gefunden wurde, werden Umrechnungsfaktoren verwendet, um ihn in die Einheit zu konvertieren, die Sie in der Vorkalkulationsposition ausgewählt haben.

Wenn die Kombination der Rolle und der Organisationseinheit keinen Einstandspreis zurückgibt, ignoriert das System die Organisationseinheit. Stattdessen sucht es nach der Kombination aus Rolle und Einheit, um den Standardpreis festzulegen (nachdem Konvertierungen angewendet wurden).

Wenn das System keinen Preis für die Rolle findet, wird der Einstandspreis in der Vorkalkulationsposition standardmäßig auf **0,00** gesetzt. Alle Kostenmengen in der Kostenvorkalkulationsposition des Projekts werden in der Währung der Vertragseinheit aufgezeichnet.

> [!NOTE]
> Standardmäßig speichert Microsoft Dynamics 365 Beträge in der Basiswährung. Die Kostenbeträge, die auf der Registerkarte **Schätzungen** angezeigt werden, sind jedoch in der Währung der Vertragseinheit.  

### <a name="default-sales-price"></a>Standard-Verkaufspreis 

Die Verkaufspreisliste wird entweder von der Verkaufsentität festgelegt, der das Projekt angefügt ist, oder vom Projektkunden. Wenn eine Verkaufsentität, wie z. B. Verkaufschance, Angebot oder Vertrag, mit dem Projekt verknüpft ist, wird der Wertriebspreis der Verkaufsentität über die Preisliste festgelegt, die dem Angebot oder dem Vertrag zugeordnet ist. Wenn das Angebot oder der Vertrag eine benutzerdefinierte Preisliste hat, wird diese Preisliste als Standardverkaufspreisliste für Projektschätzungen verwendet. Wenn keine Zuordnung mit Verkaufsentitäten vorhanden ist, wird die Standardverkaufspreisliste der Parameter als Standardverkaufspreisliste des Projekts verwendet, die mit der Kundenwährung übereinstimmt, die für das Projekt definiert wurde.

Jede Schätzungsposition enthält eine Ressourceneinheit, die mit ihr verbunden ist. Die Ressourceneinheit gibt die Organisationseinheit an, in der Ressourcen gebucht werden, um die Aufgabe abschließen zu können. Um den Verkaufspreis für die zugeordneten Rollen festzustellen, suchen Sie nach der Kombination aus Rolle, Einheit und Ressourceneinheit in der Verkaufspreisliste. Wenn keine Zuweisungen für die Aufgabe vorhanden sind, ist der Verkaufspreis für die Aufgabe 0,00.

Wenn die Kombination der Rolle, der Einheit und der Ressourceneinheit keinen Verkaufspreis aus der Verkaufspreisliste zurückgibt, ignoriert das System die Einheit. Stattdessen sucht es nach der Kombination aus Rolle und Ressourceneinheit. Wenn ein Verkaufspreis gefunden wurde, werden Umrechnungsfaktoren verwendet, um ihn in die Einheit zu konvertieren, die Sie in der Verkaufsvorkalkulationsposition ausgewählt haben. 

Wenn die Kombination der Rolle, der Einheit und der Ressourceneinheit keinen Verkaufspreis aus der Verkaufspreisliste zurückgibt, ignoriert das System die Ressourceneinheit. Stattdessen sucht es nach der Kombination aus Rolle und Einheit, um den Standardpreis festzulegen (nachdem Konvertierungen angewendet wurden).

Wenn das System keinen Preis für die Rolle findet, wird der Verkaufspreis in der Vorkalkulationsposition standardmäßig auf **0,00** gesetzt.

Die Registerkarte **Schätzungen** hat eine Rasteransicht, in der die Vorkalkulationspositionen angezeigt werden. Das Raster enthält Spalten für die Einheit, den Gesamteinstandspreis und Gesamtverkaufspreis, wie in der folgenden Abbildung gezeigt. 

> ![Rasteransicht auf der Registerkarte „Schätzungen“](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Zeitphasenansicht von Projektschätzungen

Die Zeitphasenansicht der Projektschätzungen zeigt die Schätzungsdaten der Rasteransicht mit den Teitdaten in einer gewählten Zeitskala. Standardmäßig werden die Schätzungsdaten in der Dimension **Rolle** angezeigt.

> ![Zeitphasenansicht für Projektschätzungen](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Zuweisen des geschätzten Aufwands basierend auf dem Aufgabenmodus

In der Zeitphasenansicht verteilen Sie den Gesamtaufwand, der für die Aufgabe geschätzt wird, indem Sie die Aufwandsstunden pro Einheitszeitraum in der ausgewählten Zeitskala zuweisen. Der Aufgabenmodus legt fest, wie der Aufwand über die Dauer der Aufgabe zugeteilt wird. Die zwei Arten der Verteilung sind **Gleichmäßig** und auf **Arbeitsstunden basierend.**

### <a name="work-hours-based-allocation"></a>Arbeitsstunden basierte Zuteilung
 
Im Autoplanungs-Aufgabenmodus werden die täglichen Standardstunden für Aufgabenressourcen für die vollen Arbeitsstunden pro Tag festgelegt. Dieses Verhalten trifft auch zu, wenn die Zuweisung des Aufwands durch Aufteilung über der Dauer der Aufgaben in der Zeitphasenansicht erfolgt. Zum Beispiel: Wenn Sie schätzen, dass eine Aufgabe von einer Ressource in der Zeitskala **Tag** abgeschlossen wird, wird der Aufwand pro Tag nicht die Arbeitsstunden pro Tag überschreiten, die im Kalender des Projektes definiert sind. Deshalb garantiert die Aufwandszuweisung immer, dass die Ressourcen so geschätzt werden, dass sie den ganzen Tages verwendet werden.

### <a name="even-allocation"></a>Gleichmäßige Zuteilung

Im manuell geplanten Aufgabenmodus wird die Arbeitszeit der Projektkalender nicht verwendet. Stattdessen basiert der Arbeitsplan auf Benutzereingaben. Für diese Aufgaben hat die Aufwandszuteilung pro Einheitszeitraum in der ausgewählten Zeitskala keinen Begrenzungsfaktor. Der Gesamtaufwand für die Aufgabe wird gleichmäßig auf jeden Einheitszeitraum in der ausgewählten Zeitskala aufgeteilt und zugeteilt. Daher bestimmt der Aufgabenmodus für die Aufgabe die Aufwandsverteilung oder die Verteilung des Aufwands pro Einheitszeitraum in Zeitphasenschätzungen.

## <a name="grouping-and-time-phasing-options"></a>Gruppierung und Zeitphasenoptionen

Die Zeitphasenansicht zeigt die Verteilung des Aufwands, der Kosten und der Vertriebsschätzungen auf Tages-, Wochen-, Monats- oder Jahresbasis. Standardmäßig werden die Schätzungsdaten in der Dimension **Rolle** angezeigt. Sie können jedoch die Option **Gruppieren nach** verwenden, um auf zwei andere Dimensionen festgelegt zu werden: **Kategorie** und **Ressource**.

In der Rasteransicht und der Zeitphasenansicht können Sie auswählen, welche Felder angezeigt werden. Die Gesamtsummen werden für jeden Block unteren Rand des Projekts angezeigt. Sie zeigen den gesamten geschätzten Aufwand, die Kosten und den Vertrieb pro Tag, Woche, Monat oder Jahr. Der Standardeinstandspreis und der Verkaufspreis sind datumswirksam. Das bedeutet, sie werden für jede Ressource anhand der ausgewählten Zeitphasenansicht geändert.

## <a name="expense-estimates"></a>Ausgabenschätzungen

Mit der Schaltfläche **Neue Ausgabenvorkalkulation hinzufügen** können Sie in der Rasteransicht alle Ausgaben des Projekts aufzeichnen, die nicht direkt der Arbeit zugeordnet sind. Sie können die Ausgabenschätzungen für eine bestimmte Aufgabe oder für das gesamte Projekt aufzeichnen. Wählen Sie die Ausgabenkategorien und das vorläufige Datum, an dem Sie die Ausgabe erwarten. Wenn die verbundene Einstandspreisliste und die Verkaufspreisliste Standardpreise haben (oder Aufschlagprozentsätze für Ausgabenkategorien definiert wurden), werden sie automatisch bei der Zuweisung in die Vorkalkulationsposition einbezogen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]