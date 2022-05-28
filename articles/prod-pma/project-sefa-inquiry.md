---
title: Zeitplan der Ausgaben für Bundeszuschüsse
description: Diese Thema enthält Informationen zum Zeitplan der Ausgaben der Federal Awards-Anfrage.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b88c97f3dcb1020ccf17788256990485580f6964
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684457"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Zeitplan der Ausgaben für Bundeszuschüsse

[!include [banner](../includes/banner.md)]

Laut Rundschreiben A-133 des Amtes für Verwaltung und Haushalt unterliegen Agenturen, die Bundesmittel erhalten, Prüfungsanforderungen, die auch als Einzelprüfungen bezeichnet werden. Der Prüfungsprozess wird verwendet, um regelmäßig über die Einnahmen und Ausgaben von Bundeszuschüssen zu berichten. Ein Teil des Einzelprüfungsberichts enthält die Aufstellung der Ausgaben für Bundeszuschüsse (SEFA).

Der Zeitplan für Ausgaben der Bundeszuschüsse enthält den Titel und die Nummer des Catalog of Federal Domestic Assistance (CFDA) (CFDA), die Zuschussnummer, das Jahr des Zuschusses, den Namen der Bundesbehörde, die die Mittel bereitstellt, und den Namen der Durchlauf-Entität. Die Anfrage ist für einen bestimmten Zeitraum vorgesehen. In der Regel entspricht dieser Zeitraum dem Abschlusszeitraum, bei dem es sich um ein Geschäftsjahr handelt.

Die Anfrage umfasst Zuschüsse mit Projektionsdaten im ausgewählten Zeitraum. Die Spalte **Geberbehörde** in der Anfrage zeigt den gebenden Kunden oder bei einem durchlaufenden Zuschuss, die Geberbehörde. Bei einem durchlaufenden Zuschuss zeigt die Spalte **Durchlaufbehörde** den gebenden Kunden an. Wenn es sich bei dem Zuschuss nicht um einen Durchlaufzuschuss handelt, ist die Spalte **Durchlaufbehörde** leer.

## <a name="set-up-the-cfda-clusters"></a>Die CFDA-Cluster einrichten

Sie müssen die CFDA-Cluster einrichten, die mit CFDA-Nummern in der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ verknüpft werden können.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Catalog of Federal Domestic Assistance-Cluster**.
2. Wählen Sie **Neu** aus, um das CFDA-Cluster zu erstellen.
3. Geben Sie den Clusternamen ein.
4. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

## <a name="set-up-cfda-numbers"></a>CFDA-Nummern einrichten

Sie müssen die CFDA-Nummern einrichten, die Zuschüssen hinzugefügt werden können und die in der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ enthalten sind.

1. Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Catalog of Federal Domestic Assistance-Nummern**.
2. Wählen Sie **Neu** aus, um eine CFDA-Nummer zu erstellen.
3. Geben Sie in der Spalte **Nummer** die CFDA-Nummer ein.
4. Drücken Sie die **Tab**-Taste.
5. Geben Sie in der Spalte **Beschreibung** den CFDA-Titel ein.
6. Drücken Sie die **Tab**-Taste.
7. Optional: Fügen Sie im Feld **Programmcluster** den entsprechenden CFDA-Cluster hinzu.
8. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Zuschüsse einrichten, um diese der Anfrage „Plan der Ausgaben der Bundeszuschüsse“ zu melden

1. Navigieren Sie zu **Projektmanagement und -buchhaltung \> Zuschüsse \> Zuschüsse**, und wählen Sie einen vorhandenen Zuschuss aus.
2. Weisen Sie im Inforegister **Einrichtung** im Feld **Catalog of Federal Domestic Assistance** die CFDA-Nummer zu. Die CFDA-Nummer auf dem Zuschuss bestimmt den CFDA-Cluster für die Meldung.
3. Geben Sie im Inforegister **Kontaktinformationen** die Informationen des Gebers ein, indem Sie diese Schritte befolgen:

    1. Geben Sie im Feld **Zuschusskunde** den Kunden ein, der für den Zuschuss verantwortlich ist. Bei einem vorhandenen Zuschuss sind diese Informationen möglicherweise bereits eingegeben.
    2. Geben Sie an, ob der Zuschusskunde der Geldgeber ist. Wenn der Zuschusskunde der Geldgeber ist, lassen Sie das Kontrollkästchen **Durchlauf** deaktiviert. Wenn ein anderer Kunde der Geldgeber ist und der Zuschusskunde für die Ausgabe und Nachverfolgung des Geldes verantwortlich ist, aktivieren Sie die Option **Durchlauf**.

4. Wenn Sie das Kontrollkästchen **Durchlauf** im vorherigen Schritt im Feld **Geberbehörde** aktiviert haben, geben Sie den Kunden ein, der den Zuschuss bereitgestellt hat. Die Geberbehörde und der Zuschusskunde können nicht derselbe Kunde sein.

Hier ist ein Beispiel für einen durchlaufenden Zuschuss:

Die Bundesregierung hat ein Infrastrukturprojekt für einen Staat finanziert. Die Bundesregierung gab dem Staat das Geld zum Ausgeben. In diesem Fall ist die Bundesregierung die Förderstelle und der Staat der Förderkunde.

> [!NOTE] 
> Wenn Sie die Funktion zum ersten Mal aktivieren, werden die anfänglichen CFDA-Nummern unter Verwendung der vorhandenen Nummern für Zuschüsse eingegeben.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Zuschüsse von der SEFA-Meldung basierend auf der Zuschussart ausschließen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung \> Einrichtung \> Zuschüsse \> Zuschusstypen**.
2. Aktivieren Sie im Inforegister **Standardinformationen** das Kontrollkästchen **Vom Plan der Ausgaben für Bundeszuschüsse ausschließen**.
3. Wählen Sie **Speichern** aus, um die Änderungen zu speichern.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Den Plan für die Ausgaben der Bundeszuschüsse ausführen

1. Navigieren Sie zu **Projektmanagement und -buchhaltung \> Abfragen und Berichte \> Zuschussanfrage \> Plan der Ausgaben der Bundeszuschüsse**.
2. Befolgen Sie im Abschnitt **Parameter** diese Schritte:

    1. Wählen Sie im Feld **Datumsintervall** den Code für das Datumsintervall aus. Definieren Sie alternativ in den Feldern **Von Datum** und **Bis Datum** das Datumsintervall.
    2. Optional: Um nur in Rechnung gestellte Transaktionen als Umsatz in die Anfrage einzubeziehen, legen Sie die Option **Nur fakturierte Umsätze einbeziehen** auf **Ja** fest.

## <a name="columns"></a>Spalten

Die Abfrage des Zeitplans der Ausgaben für Bundeszuschüsse umfasst die folgenden Spalten:

- Catalog of Federal Domestic Assistance-Clustername
- Zuschussgeberbehörde
- Durchlaufbehörde
- Zuschussname
- Zuschuss-ID
- Zuschuss-Antrags-ID
- Catalog of Federal Domestic Assistance
- Quittungen
- Ausgaben


[!INCLUDE[footer-include](../includes/footer-banner.md)]