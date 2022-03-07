---
title: Korrigieren der Buchhaltung auf Projektrechnungsvorschlägen
description: Dieses Thema erklärt, wie Sie buchhalterische Informationen auf einem Entwurf eines Rechnungsvorschlags korrigieren können.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251213"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Korrigieren der Buchhaltung auf Projektrechnungsvorschlägen

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

*Vorgänge* für Projektrechnungen werden vom Projekt Manager auf einer Proforma-Rechnung gepflegt. Zu diesen Details gehören die Entscheidung über die zu berechnenden Stunden, Spesen, Materialien oder Meilensteine, die Sätze und die Anwendung von Vorauszahlungsbeträgen und Vorschussbeträgen. Nachdem Sie die ursprüngliche Proforma-Rechnung bestätigt haben, können Sie die operativen Details anpassen, indem Sie eine [korrekte Proforma-Rechnung](../proforma-invoicing/corrective-invoices.md) erstellen und bestätigen.

*Buchhaltungsdetails* für Projektrechnungen werden in einem kundenorientierten Rechnungsbeleg gepflegt. Diese Details beinhalten die Mehrwertsteuer-Berechnung und die finanziellen Dimensionen, die auf die Rechnung angewendet werden. In diesem Thema wird beschrieben, wie diese Buchhaltungsdetails in einem Entwurf eines Projektrechnungsvorschlags angepasst werden können.

## <a name="adjust-sales-tax"></a>Anpassen der Mehrwertsteuer

Die voreingestellten Mehrwertsteuergruppen für die Fakturierung und die Mehrwertsteuergruppen für die Elemente können direkt im Beleg der Rechnungsvorschlag angepasst werden. Um diese Gruppen anzupassen, wählen Sie **Bearbeiten** und geben dann in jeder Zeile des Projektrechnungsvorschlags einen neuen Wert in das Feld **Umsatzsteuerklasse** oder **Element-Umsatzsteuerklasse** ein.

## <a name="adjust-financial-dimensions"></a>Finanzielle Dimensionen anpassen

Finanzielle Dimensionen können nicht direkt in einer Zeile des Projektrechnungsvorschlags bearbeitet werden. Gehen Sie stattdessen wie folgt vor, um finanzielle Dimensionen in einem Projektrechnungsvorschlag anzupassen.

1. Wählen Sie auf dem Projektrechnungsvorschlag die Option **Alle löschen**, um die Zeilen des Projektrechnungsvorschlags zu entfernen.

    > [!NOTE]
    > Die Schaltfläche **Alles löschen** ist nur verfügbar, nachdem der Systemadministrator die Funktion **Rechnungsvorschlagszeilen löschen bei Verwendung von Project Operations für ressourcenbasierte/ nicht vorrätige Szenarien** im Arbeitsbereich **Funktionsverwaltung** aktiviert hat.

2. Passen Sie die finanziellen Dimensionen an:

    - **Transaktionen auf Rechnung (Abrechnungs-Meilensteine):** Gehen Sie zu **Alle Projekte** \> **Verwalten** \> **Transaktionen auf Rechnung** und wählen Sie den Meilenstein aus, der angepasst werden muss. Aktualisieren Sie dann auf der Registerkarte **Finanzielle Dimensionen** die Werte wie gewünscht.
    - **Zeit-, Aufwands- und Materialtransaktionen:** Wählen Sie auf der Seite **gebuchte Projekttransaktionen** die Option **Buchhaltung anpassen**, um die finanziellen Dimensionen zu aktualisieren.

3. Nachdem Sie die Werte der finanziellen Dimensionen angepasst haben, gehen Sie zu **Projektmanagement und -buchhaltung** \> **Periodisch** \> **Project Operations Integration** und wählen Sie **Import aus Stagingtabelle**, um den periodischen Vorgang auszuführen. Dieser Prozess verwendet die aktualisierten Werte der finanziellen Dimensionen, um die Zeilen des Projektrechnungsvorschlags neu zu erstellen. Die aktualisierten Werte werden dann im untergeordneten Sachkonto und im Hauptbuch des Projekts verwendet, wenn die Projektrechnung gebucht wird.
