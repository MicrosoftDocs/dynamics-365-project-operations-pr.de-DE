---
title: Projektzeitplan-API-Leistung
description: Dieses Thema bietet Informationen zu den Leistungs-Benchmarks der Projektzeitplan-APIs und identifiziert Best Practices für eine optimale Nutzung.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750601"
---
# <a name="project-schedule-api-performance"></a>Projektzeitplan-API-Leistung

_**Gilt für:** Die Basisbereitstellung ist für die Szenarien Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen und Lite-Bereitstellung – Abschluss zur Pro-forma-Rechnungsstellung verfügbar, Project for the web_

Dieses Thema bietet Informationen zu den Leistungs-Benchmarks der Projektzeitplan-APIs (Schnittstellen zur Anwendungsprogrammierung) und identifiziert Best Practices für eine optimale Nutzung.

## <a name="project-scheduling-service"></a>Projektplanungsservice
Der Projektplanungsservice ist ein Service für mehrere Mandanten, der in Microsoft Azure ausgeführt wird. Er wurde entwickelt, um die Interaktion zu verbessern, indem er eine schnelle und flüssige Erfahrung bietet, wenn Benutzer an Projekten arbeiten. Diese Verbesserung wird erreicht, indem Änderungsanforderungen angenommen und bearbeitet werden und anschließend das Ergebnis sofort zurückgegeben wird. Der Service bleibt asynchron zu Dataverse und hindert Benutzer nicht daran, andere Vorgänge auszuführen.

Die Projektzeitplan-APIs verlassen sich auf den Projektplanungsservice, um Anforderungen auszuführen, die in späteren Abschnitten dieses Themas ausführlicher beschrieben werden.

Die Projektzeitplan-APIs sind so konzipiert, dass sie mit den folgenden Projektstrukturplan-Entitäten (PSP) funktionieren:

  - Project
  - Projektaufgabe
  - Abhängigkeit der Projektaufgaben
  - Projektteammitglied
  - Ressourcenzuweisung
  
Sowohl Standardfelder als auch benutzerdefinierte Felder werden unterstützt. Sofern nicht anders angegeben, werden alle gängigen Operationen unterstützt, z. B. Erstellen, Aktualisieren und Löschen. Weitere Informationen finden Sie unter [Projektzeitplan-APIs verwenden, um Vorgänge mit Planungsentitäten auszuführen](schedule-api-preview.md).

Als Teil der Projektzeitplan-APIs wurde ein Arbeitseinheitsmuster hinzugefügt. Dieses Muster wird als OperationSet bezeichnet und kann verwendet werden, wenn mehrere Anforderungen in einer einzigen Transaktion verarbeitet werden müssen.

Die folgende Abbildung zeigt den Flow, den ein Partner erlebt, wenn diese Funktion verwendet wird.

![Dataverse und Projektzeitplanungsservice-Flow.](./media/dataverse-project-scheduling-service-flow.png)

**Schritt 1**: Ein Client macht einen API-Aufruf an einen Open Data Protocol (OData)-Endpunkt in Dataverse, um ein OperationSet zu erstellen.

**Schritt 2**: Nachdem das neue OperationSet erstellt wurde, wird ein **OperationSetId**-Wert zurückgegeben.

**Schritt 3**: Der Client verwendet den **OperationSetId**-Wert, um eine weitere Projektzeitplan-API-Anfrage zu stellen. Das Ergebnis ist eine Erstellungs-, Aktualisierungs- oder Löschanforderung für eine Planungsentität. Wenn diese Anfrage gestellt wird, wird die Metadatenvalidierung durchgeführt. Wenn die Validierung fehlschlägt, wird die Anfrage beendet und ein Fehler zurückgegeben.

**Schritte 4a–4c**: Diese Schritte repräsentieren die ACCEPT-Phase. Der Client ruft die **ExecuteOperationSetV1**-API auf, die alle Änderungen in einem Batch an den Projektplanungsservice sendet. Der Projektplanungsservice führt seine eigenen Validierungen für Anforderungen im Batch aus. Validierungsfehler machen den Batch rückgängig und geben eine Ausnahme an den Aufrufer zurück. Wenn der Batch erfolgreich vom Projektplanungsservice akzeptiert wird, wird der OperationSet-Status aktualisiert, um die Tatsache widerzuspiegeln, dass das OperationSet vom Projektplanungsservice verarbeitet wird.

**Schritt 5**: Dieser Schritt stellt die PERSIST-Phase dar. Der Projektplanungsservice schreibt den Batch bei einer Transaktion asynchron in Dataverse. Wenn der Schreibvorgang erfolgreich ist, wird das OperationSet markiert als **Abgeschlossen**. Bei Fehlern wird die Transaktion und der Batch zurückgesetzt und das OperationSet wird als **Fehlgeschlagen** markiert.

## <a name="performance-methodology"></a>Leistungsmethodik
Die Ausführungszeit ist definiert als die Zeit vom Aufruf der **ExecuteOperationSetV1**-API, bis der Projektplanungsservice fertig in Dataverse geschrieben hat. Alle Operationen werden zusammen 2.200 Mal ausgeführt, und die P99-Ausführungszeitmessungen werden gemeldet. Einzeldatensatz- und Massenoperationen werden gemessen.

Für eine Operation mit einem einzigen Datensatz enthält das OperationSet eine Anforderung. Bei Massenvorgängen enthält es 20, 50 oder 100 Anfragen. Jede Bulk-Größe wird separat gemeldet.

Diese Vorgänge werden in einer UR 15 Project Operations Lite-Bereitstellung in Nordamerika ausgeführt.

## <a name="results"></a>Ergebnisse
### <a name="create-operations"></a>Vorgänge erstellen
#### <a name="single-record-create-operations"></a>Erstellen von Einzeldatensätzen
Die folgende Tabelle zeigt die Ausführungszeiten für die Erstellung eines einzelnen Datensatzes. Die Zeiten sind in Sekunden angegeben.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Datensatztyp&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Zeit</th>
  </tr>
  <tr>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Aufgabe</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zuweisung</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammitglied</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Abhängigkeit</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Massenerstellungsvorgänge
Die folgende Tabelle zeigt die Ausführungszeiten für die Erstellung zahlreicher Datensätze. Insbeondere hat Microsoft die Ausführungszeiten für die Erstellung von 20, 50 und 100 Datensätzen in einem einzigen OperationSet gemessen. Die Zeiten sind in Sekunden angegeben.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Datensatztyp&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Zeit</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 Datensätze</th>
    <th class="tg-0lax" colspan="2">50 Datensätze</th>
    <th class="tg-0lax" colspan="2">100 Datensätze</th>
  </tr>
  <tr>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Aufgabe</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zuweisung</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Abhängigkeit</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Massenerstellungsvorgänge in den **Projekt**- und **Teammitglied**-Entitäten sind in dieser Tabelle nicht enthalten, da die Laufzeit für diese Vorgänge der Laufzeit ähnelt, bei der die API zum Erstellen eines einzelnen Datensatzes mehrmals aufgerufen wird. Diese APIs werden sofort in Dataverse ausgeführt.

Die folgende Abbildung zeigt eine grafische Darstellung der Ausführungszeiten für die Entitäten **Aufgabe**, **Zuweisung** und **Abhängigkeit**, wenn 20, 50 und 100 Datensätze erstellt und alle unterstützten Felder verwendet werden.

![Erstellen Sie ein Diagramm zur Ausführungszeit eines Datensatzes.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Vorgänge aktualisieren
#### <a name="single-record-update-operations"></a>Einzeldatensatz-Aktualisierungsvorgänge
Die folgende Tabelle zeigt die Ausführungszeiten für die Aktualisierung eines einzelnen Datensatzes. Die Zeiten sind in Sekunden angegeben.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Datensatztyp&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="2">Zeit</th>
  </tr>
  <tr>
    <th class="tg-0lax">Erforderliche Felder </th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Aufgabe</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammitglied</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Aktualisierungsvorgänge der Entitäten **Ressourcenzuweisungen** und **Abhängigkeit der Projektaufgaben** werden nicht unterstützt.

#### <a name="bulk-update-operations"></a>Massenaktualisierungsvorgänge
Die folgende Tabelle zeigt die Ausführungszeiten für die Aktualisierung zahlreicher Datensätze. Insbeondere hat Microsoft die Ausführungszeiten für die Aktualisierung von 20, 50 und 100 Datensätzen in einem einzigen OperationSet gemessen. Die Zeiten sind in Sekunden angegeben.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Datensatztyp&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="6">Zeit</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 Datensätze</th>
    <th class="tg-0lax" colspan="2">50 Datensätze</th>
    <th class="tg-0lax" colspan="2">100 Datensätze</th>
  </tr>
  <tr>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
    <th class="tg-0lax">Erforderliche Felder</th>
    <th class="tg-0lax">Alle unterstützten Felder</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Aufgabe</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammitglied</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Aktualisierungsvorgänge der Entitäten **Ressourcenzuweisungen** und **Abhängigkeit der Projektaufgaben** werden nicht unterstützt.

Die folgende Abbildung zeigt eine grafische Darstellung der Ausführungszeiten für die Entitäten Aufgabe und Teammitglied, wenn 20, 50 und 100 Datensätze aktualisiert und alle unterstützten Felder verwendet werden.

![Aktualisieren Sie ein Diagramm zur Ausführungszeit eines Datensatzes.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Vorgänge löschen
#### <a name="single-record-delete-operations"></a>Einzeldatensatz-Löschvorgänge
Die folgende Tabelle zeigt die Ausführungszeiten für die Löschung eines einzelnen Datensatzes. Die Zeiten sind in Sekunden angegeben.

| Datensatztyp | Zeit  |
|-------------|-------|
| Aufgabe        | 20.12 |
| Zuweisung  | 10.86 |
| Teammitglied | 12.52 |
| Abhängigkeit  | 20.89 |

> [!NOTE]
> Löschvorgänge in der **Projekt**-Entität werden nicht unterstützt.

#### <a name="bulk-delete-operations"></a>Massenlöschungsvorgänge
Die folgende Tabelle zeigt die Ausführungszeiten für die Löschung zahlreicher Datensätze. Insbeondere hat Microsoft die Ausführungszeiten für die Löschung von 20, 50 und 100 Datensätzen in einem einzigen OperationSet gemessen. Die Zeiten sind in Sekunden angegeben.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Datensatztyp&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax" colspan="3">Zeit</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 Datensätze</th>
    <th class="tg-0lax">50 Datensätze</th>
    <th class="tg-0lax">100 Datensätze</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Aufgabe</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zuweisung</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Teammitglied</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Abhängigkeit</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Löschvorgänge in der **Projekt**-Entität werden nicht unterstützt.

Die folgende Abbildung zeigt eine grafische Darstellung der Ausführungszeiten für die Entitäten **Aufgabe**, **Zuweisung**, **Teammitglied** und **Abhängigkeit**, wenn 20, 50 und 100 Datensätze gelöscht werden.

![Löschen Sie ein Diagramm zur Ausführungszeit eines Datensatzes.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Beobachtungen
Für jeden Datensatzvorgang benötigt die **ExecuteOperationSet**-API etwa 800 Millisekunden, um eine Anfrage an den Projektplanungsservice zu senden. Der Projektplanungsservice benötigt dann etwa fünf Sekunden, um die Nutzlast zu verarbeiten und Dataverse aufzurufen. Die restliche Ausführungszeit wird damit verbracht, Geschäftslogik auszuführen und Daten in die Datenbank in Dataverse zu schreiben.

Wenn 100 Datensätze erstellt, aktualisiert oder gelöscht werden, wird die **ExecuteOperationSet**-API dauert etwa drei Sekunden, um die Anfrage an den Projektplanungsservice zu senden. Der Projektplanungsservice benötigt dann etwa fünf Sekunden, um die Anforderung zu verarbeiten und Dataverse aufzurufen. Massenoperationen müssen einmalig **Projektplanungsservice-Steuer** für alle Datensätze im OperationSet zahlen. Daher haben Massenoperationen eine deutlich kürzere durchschnittliche Ausführungszeit als Operationen mit einem einzigen Datensatz.

## <a name="scenarios"></a>Szenarien
Die folgende Tabelle zeigt die Ausführungszeiten, wenn die Projektzeitplan-APIs verwendet werden, um bestimmte Szenarien auszuführen. Die Zeiten sind in Sekunden angegeben.

| Szenario                                                                   | Zeit  |
|----------------------------------------------------------------------------|-------|
| Erstellen Sie ein Projekt mit 40 Aufgaben.                                      | 36.01 |
| Erstellen Sie ein Projekt mit 40 Aufgaben und 20 Abhängigkeiten.                  | 38.11 |
| Erstellen Sie ein Projekt mit 40 Aufgaben und 30 Zuweisungen.                   | 60.17 |
| Erstellen Sie ein Projekt mit 40 Aufgaben, 20 Abhängigkeiten und 30 Zuweisungen. | 60.27 |

## <a name="best-practices"></a>Bewährte Vorgehensweisen
Basierend auf den Ergebnissen des vorherigen Szenarios erzielen die APIs unter den folgenden Bedingungen eine bessere Leistung:

  - Gruppieren Sie so viele Operationen wie möglich. Die durchschnittliche Laufzeit für Massenvorgänge ist besser als die durchschnittliche Laufzeit für Einzeldatensatzvorgänge. Je kleiner die Anzahl der verwendeten OperationSets ist, desto schneller ist die durchschnittliche Ausführungszeit.
  - Legen Sie nur die Mindestattribute fest, die zum Ausführen Ihres Szenarios erforderlich sind. Seien Sie wählerisch bei den Typen nicht erforderlicher Felder, die in einer OperationSet-Anforderung enthalten sind. Felder, die Fremdschlüssel oder Rollupfelder enthalten, wirken sich negativ auf die Leistung aus.
