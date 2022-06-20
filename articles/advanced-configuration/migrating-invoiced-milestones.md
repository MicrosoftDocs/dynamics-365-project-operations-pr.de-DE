---
title: Vollständig fakturierte Abrechnungsmeilensteine bei der Übernahme migrieren
description: Dieser Artikel erklärt, wie Sie Meilensteine mit Festpreisabrechnung migrieren, die dem Kunden für offene Projektverträge vor dem Go-Live-Datum in Rechnung gestellt wurden.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912239"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Vollständig fakturierte Abrechnungsmeilensteine bei der Übernahme migrieren

_**Gilt für:** Project Operations für Szenarien basierend auf vorrätigen/nicht-vorrätigen Ressourcen_

## <a name="scenario"></a>Szenario

Contoso wird mit Microsoft Dynamics 365 Project Operations für Szenarios mit Ressourcen/nicht auf Lager live geschaltet. Im Rahmen der Übernahmeaktivitäten muss das Implementierungsteam offene Projektverträge aus dem Altsystem migrieren. Einige der Projektverträge beinhalten Vertragszeilen, die im Festpreisverfahren abgerechnet werden und bereits teilweise an den Endkunden fakturiert wurden. Das Implementierungsteam muss diese Abrechnungsmeilensteine als **Kundenrechnung gebucht** migrieren, da sie für Zwecke der Umsatzrealisierung in den Gesamtauftragswert einbezogen werden müssen. Kundensalden in der Debitorenbuchhaltung und im Hauptbuch dürfen jedoch nicht beeinträchtigt werden.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Anforderungen

- Dynamics 365 Finance 10.0.24 oder höher muss installiert sein.
- Die Umgebung, in der die Migrationsschritte ausgeführt werden, muss sich im Wartungsmodus befinden. Während der Migration der Meilensteine sollten keine anderen Aktivitäten durchgeführt werden.
- Die Migrationsschritte müssen genau wie hier beschrieben befolgt werden und können nur für die Übernahmeaktivität verwendet werden. Microsoft unterstützt keine andere Verwendung dieser Funktion.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Eine Übernahmeversion der Zuordnung für duales Schreiben für Meilensteine der Project Operations-Integrationsvertragsposition erstellen 

1. Stellen Sie sicher, dass die Zielzuordnung für die Entität **Meilensteine der Project Operations-Integrationsvertragsposition** auf dem neuesten Stand ist. 

    1. Gehen Sie in Finance zu **Datenmanagement** \> **Datenentitäten**, und wählen Sie die Entität **Meilensteine der Project Operations-Integrationsvertragsposition** aus. 
    2. Wählen Sie **Zielzuordnungen ändern** aus. 
    3. Auf der Seite **Staging zum Ziel zuordnen** wählen Sie **Zuordnung generieren**, und bestätigen Sie dann, dass Sie die Zuordnung generieren möchten.

2. Beenden und aktualisieren Sie die Zuordnung für duales Schreiben **Meilensteine der Project Operations-Integrationsvertragsposition** (**msdyn\_contractlinescheduleofvalues**). 

    1. Gehen Sie zu **Datumsmanagement** \> **Duales Schreiben**, wählen Sie die Zuordnung aus und öffnen Sie ihre Details. 
    2. Wählen Sie **Beenden**, und warten Sie, bis das System die Zuordnung stoppt. 
    3. Wählen Sie **Tabellen aktualisieren**.

3. Fügen Sie eine Zuordnung für den Transaktionsstatus hinzu.

    1. Wählen Sie **Zuordnung hinzufügen**.
    2. Wählen Sie auf der neuen Position in der **Finanz- und Betriebs-Apps**-Spalte das **TRANSSTATUS\[TRANSSTATUS\]**-Feld.
    3. Wählen Sie in der **Microsoft Dataverse**-Spalte **msdyn\_invoicestatus\[Rechnungsstatus \]**.
    4. In der **Kartentyp**-Spalte wählen Sie den Pfeil nach rechts (**\>**).
    5. Im angezeigten Dialogfenster im **Richtung synchronisieren**-Feld wählen Sie **Dataverse zu Finanz- und Betriebs-Apps**.
    6. Wählen Sie **Transformation hinzufügen** aus.
    7. Wählen Sie im Feld **Transformationstyp** **ValueMap** aus.
    8. Wählen Sie **Wertzuordnung hinzufügen**.
    9. Geben Sie im linken Feld **4** ein. Geben Sie im rechten Feld **192350001** ein. 
    10. Wählen Sie **Speichern** aus, und schließen Sie das Dialogfeld.

4. Wählen Sie **Speichern als**, um die Version der Zuordnung für duales Schreiben zu speichern. 
5. Wählen Sie im **Tabelle hinzufügen**-Bereich im **Verleger**-Feld **Standardherausgeber**.
6. In dem **Version**-Feld geben Sie die Version ein.
7. In dem **Beschreibung**-Feld geben Sie eine Notiz zu dieser Übernahmeversion der Zuordnung ein. 
8. Wählen Sie **Save** (Speichern).
9. Starten Sie die Zuordnung.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Fakturierte Meilensteine in die Dataverse-Umgebung migrieren

1. In der Project Operations Dataverse-Umgebung erstellen Sie Meilensteine mit einem Rechnungsstatus von **Bereit für die Rechnungsstellung**. Migrieren Sie zu diesem Zeitpunkt keine Meilensteine, die nicht in Rechnung gestellt wurden.

    > [!NOTE]
    > Bevor Sie die Abrechnungsmeilensteine migrieren, stellen Sie sicher, dass die Finanzdimensionen, die sich auf die Projektvertragsposition beziehen, wie erwartet eingestellt sind. Finanzdimensionen können nach Abschluss der Migration nicht mehr bearbeitet werden.

2. Nachdem alle Meilensteine migriert wurden, stoppen Sie die folgenden Zuordnungen für duales Schreiben:

    - Vertragszeilenmeilensteine für die Integration von Project Operations (msdyn\_contractlinescheduleofvalues)
    - Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)
    - Projektrechnungsvorschläge V2 (Rechnungen)

    Führen Sie die folgenden Schritte aus, um die Zuordnungen zu beenden:

    1. Gehen Sie in Finance zu **Datumsmanagement** \> **Duales Schreiben**, wählen Sie eine Zuordnung aus und öffnen Sie ihre Details.
    2. Wählen Sie **Beenden**, und warten Sie, bis das System die Zuordnung stoppt.

3. In der Project Operations Dataverse-Umgebung erstellen und bestätigen Sie Proforma-Rechnungen für die Abrechnungsmeilensteine. 

    1. Gehen Sie in der Sitemap zu den Projektverträgen, wählen Sie die Verträge aus und wählen Sie dann **Rechnungen erstellen**.
    2. Nachdem die Rechnungen erstellt wurden, öffnen Sie sie über das **Rechnungen**-Menü in der Sitemap, und wählen Sie dann **Bestätigen**.

    Dieser Schritt erstellt die erforderlichen Datensätze in der Dataverse-Umgebung. Finanz- und Debitorenbuchhaltung sind davon jedoch nicht betroffen, da die zuvor aufgeführten Zuordnungen für duales Schreiben gestoppt wurden.

4. Nachdem alle Proforma-Rechnungen bestätigt wurden, setzen Sie alle Zuordnungen für duales Schreiben in ihren ursprünglichen Zustand zurück.

    1. Aktualisieren Sie die Zuordnung für duales Schreiben **Meilensteine der Project Operations-Integrationsvertragsposition** (**msdyn\_contractlinescheduleofvalues**) wieder auf die ursprüngliche Version. 
    2. Wählen Sie die Zuordnung für duales Schreiben in der Zuordnungsliste aus, wählen Sie **Version der Tabellenzuordnung** und dann die ursprüngliche Version der Tabellenzuordnung aus.
    3. Wählen Sie **Save** (Speichern).
    4. Starten Sie die folgenden Zuordnungen für duales Schreiben neu:

        - Vertragszeilenmeilensteine für die Integration von Project Operations (msdyn\_contractlinescheduleofvalues)
        - Tatsächliche Werte der Project Operations-Integration (msdyn\_actuals)
        - Projektrechnungsvorschläge V2 (Rechnungen)

Die Meilensteine sind nun migriert und das System ist bereit für die nächsten Schritte in der Übernahmeaktivität.
