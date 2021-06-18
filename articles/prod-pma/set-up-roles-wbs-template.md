---
title: Rollen in Vorlagen für Projektstrukturpläne einrichten
description: Dieses Thema enthält Informationen zum Einrichten von Rolleninformationen in Vorlagen für Projektstrukturpläne.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec952021f9da4d83520d29d68d040675f7933df7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997600"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Rollen in Vorlagen für Projektstrukturpläne einrichten

[!include [banner](../includes/banner.md)]

Projektmanager können Vorlagen für Projektstrukturpläne (PSP) einrichten, die sie beim Erstellen eines PSP für neue Projekte anwenden können. Projektmanager können beim Erstellen einer Vorlage Rollen hinzufügen. Gehen Sie wie folgt vor, um einer PSP-Vorlage eine Rolle zuzuweisen.

1. Wählen Sie **Projektmanagement und -buchhaltung** > **Einrichtung** > **Projekte** > **Vorlagen für Projektstrukturpläne** aus.
2. Wählen Sie **Einzelheiten** für eine ausgewählte PSP-Vorlage.
3. Wählen Sie eine Aufgabe in der Liste und dann im Feld **Rolle** wählen Sie eine Rolle aus, die der Aufgabe zugewiesen werden soll.

## <a name="work-with-a-wbs"></a>Mit einem PSP arbeiten

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
2. Wählen Sie **Planen** > **Aktivitäten** > **Projektstrukturplan** aus.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]