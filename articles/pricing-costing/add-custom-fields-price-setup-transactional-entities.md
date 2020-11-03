---
title: Hinzufügen von benutzerdefinierten Feldern zu Preisgestaltung und zu Transaktionsentitäten
description: Dieses Thema enthält Informationen zum Hinzufügen der erforderlichen benutzerdefinierten Feldreferenzen zu Entitäten sowie zu Formularen und Ansichten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e589465eb98723b3b49c5d96e263eb3abf15eb2c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076564"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Hinzufügen von benutzerdefinierten Feldern zu Preisgestaltung und zu Transaktionsentitäten

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In diesem Thema wird davon ausgegangen, dass Sie die im Thema [Erstellen benutzerdefinierter Felder und Entitäten, die als Preisdimensionen verwendet werden](create-custom-fields-entities-pricing-dimensions.md) beschriebenen Schritte ausgeführt haben. Wenn Sie diese Prozeduren nicht abgeschlossen abgeschlossen haben, kehren Sie zurück und schließen Sie diese ab. Dann kehren Sie zu diesem Thema zurück. 

In diesem Thema werden die Vorgehensweisen erläutert, wie Sie die erforderlichen Feldverweise zu benutzerdefinierten Entitäten und den Elementen der Benutzeroberfläche (UI) wie etwa Formularen und Ansichten hinzufügen.

## <a name="add-custom-pricing-dimension-fields"></a>Hinzufügen benutzerdefinierter Preisdimensions-Felder 
Nach dem Erstellen benutzerdefinierter Felder und Entitäten besteht der nächste Schritt darin, durch das Erstellen von Referenzfeldern dafür zu sorgen, dass die Preis- und Transaktionsentitäten die benutzerdefinierten Entitäten oder Optionssätze erkennen. Befolgen Sie nur die Schritte unter **Optionssatzbasierte benutzerdefinierte Preisdimensionen** bzw. **Entitätsbasierte benutzerdefinierte Preisdimensionen** oder beides – je nachdem, ob Ihre Preisdimensionsliste Optionssatzdimensionen oder Entitätsdimensionen oder beides enthält.

### <a name="option-set-based-custom-pricing-dimensions"></a>Optionssatzbasierte benutzerdefinierte Preisdimensionen
Wenn eine benutzerdefinierte Preisdimension optionssatzbasiert ist, fügen Sie sie als Feld den Schlüsselentitäten hinzu. Im folgenden Verfahren werden **Arbeitsstandort der Ressource** und **Arbeitszeiten der Ressource** als optionssatzbasierte Preisdimensionen verwendet. Dazu müssen diese zuerst den Preisentitäten **Rollenpreis** und **Rollenpreisaufschlag** als Felder hinzugefügt werden.

1. Wählen Sie im Projektvorgang **Einstellungen** > **Lösungen** und doppelklicken Sie auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Rollenpreis** aus.
3. Erweitern Sie die Entität **Rollenpreis** und wählen Sie **Felder** aus.
4. Wählen Sie **Neu** , um ein neues Feld namens **Arbeitsstandort der Ressource** zu erstellen und wählen Sie als Feldtyp **Optionssatz** aus. 
5. Wählen Sie **Einen vorhandenen Optionssatz verwenden** aus, wählen Sie den Optionssatz **Arbeitsstandort der Ressource** aus, und wählen Sie **Speichern**.
6. Wiederholen Sie die Schritte 1 - 5, um dieses Feld der Entität **Rollenpreisaufschlag** hinzuzufügen. 
7. Wiederholen Sie die Schritte 1 - 5 für den Optionssatz **Arbeitszeiten der Ressource**.

> [!IMPORTANT]
> Wenn Sie ein Feld mehr als einer Entität hinzufügen, verwenden Sie denselben Feldnamen für alle Entitäten. 

In der Vertriebs- und Schätzungsphase eines Projekts werden Schätzungen des Arbeitsaufwands verwendet, der erforderlich ist, um die Arbeiten **lokal** und **vor Ort** während der **regulären Arbeitszeit** und **Überstunden** durchzuführen, um den Wert des Angebots bzw. Projekts zu ermitteln. Die Felder **Arbeitsstandort der Ressource** und **Arbeitszeiten der Ressource** werden den Schätzungsentitäten **Detailinformationen zur Angebotsposition** , **Projektvertragsposition** , **Projektteammitglied** und **Vorkalkulationsposition** hinzugefügt.

1. Wählen Sie im Projektvorgang **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Detailinformationen zur Angebotsposition** aus.
3. Erweitern Sie die Entität **Detailinformationen zur Angebotsposition** und wählen Sie **Felder** aus.
4. Wählen Sie **Neu** , um ein neues Feld namens **Arbeitsstandort der Ressource** zu erstellen und wählen Sie den Feldtyp **Optionssatz**. 
5. Wählen Sie **Einen vorhandenen Optionssatz verwenden** und **Arbeitsstandort der Ressource** aus und wählen Sie dann **Speichern**.
6. Wiederholen Sie die Schritte 1 - 5, um dieses Feld den Entitäten **Positionsdetail von Projektvertrag** , **Projektteammitglied** und **Vorkalkulationsposition** hinzuzufügen.
7. Wiederholen Sie die Schritte 1 - 6 für den Optionssatz **Arbeitszeiten der Ressource**. 

Für die Lieferung und Rechnungsstellung muss in den Projekt-Ist-Werten der Preis für die abgeschlossenen Arbeiten genau ausgewiesen sein, um auszuwählen, ob sie **lokal** oder **vor Ort** und während der **regulären Arbeitszeit** oder während **Überstunden** ausgeführt wurden. Die Felder **Arbeitsstandort der Ressource** und **Arbeitszeiten der Ressource** sollten den Entitäten **Zeiteintrag** , **Tatsächlich** , **Rechnungsposition** und **Erfassungsposition** hinzugefügt werden.

1. Wählen Sie **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**.
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Zeiteintrag** aus.
3. Erweitern Sie die Entität **Detailinformationen zur Angebotsposition** und wählen Sie dann **Felder** aus.
4. Wählen Sie **Neu** , um ein neues Feld namens **Arbeitsstandort der Ressource** zu erstellen und wählen Sie als Feldtyp **Optionssatz** aus. 
5. Wählen Sie **Einen vorhandenen Optionssatz verwenden** aus, wählen Sie den Optionssatz **Arbeitsstandort der Ressource** aus, und wählen Sie **Speichern**.
6. Wiederholen Sie die Schritte 1 - 5, um dieses Feld den Entitäten **Tatsächlich** , **Rechnungsposition** und **Erfassungsposition** hinzuzufügen.
7. Wiederholen Sie die Schritte 1 - 6 für den Optionssatz **Arbeitszeiten der Ressource**. 

Damit sind die Schemaänderungen abgeschlossen, die für die optionssatzbasierten, benutzerdefinierten Dimensionen erforderlich sind.

## <a name="entity-based-custom-pricing-dimensions"></a>Entitätsbasierte benutzerdefinierte Preisdimensionen

Wenn es sich bei der benutzerdefinierten Preisdimension um eine Entität handelt, fügen Sie 1:n-Beziehungen zwischen der Dimensionsentität und den wichtigsten Project Service-Entitäten hinzu. Anhand des obigen Beispiels „Standardtitel” kann davon ausgegangen werden, dass jedem Mitarbeiter ein Standardtitel zugewiesen wird. Als Ergebnis benötigen Sie eine 1:n-Beziehung von „Standardtitel” zu „Buchbare Ressource” oder eine n:1-Beziehung, wenn sie von „Buchbare Ressource” zu „Standardtitel” erstellt wurde.

1. Wählen Sie im Projektvorgang **Einstellungen** > **Lösungen** und doppelklicken Sie dann auf **\<your organization name> Preisdimensionen**. 
2. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Standardtitel** aus.
3. Erweitern Sie die Entität **Standardtitel** und wählen Sie **1:n-Beziehungen** aus.
4. Wählen Sie **Neu** , um eine neue 1:n-Beziehung namens **Standardtitel zu Buchbare Ressource** zu erstellen. Geben Sie die gewünschten Informationen ein und wählen Sie anschließend **Speichern**.

Der Standardtitel muss dann auch den Project Service-Preisentitäten **Rollenpreis** und **Rollenpreisaufschlag** hinzugefügt werden. Dies erfolgt mithilfe von 1:n-Beziehungen zwischen den Entitäten **Standardtitel** und **Rollenpreis** sowie den Entitäten **Standardtitel** und **Rollenpreisaufschlag**.

1. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Standardtitel** aus.
2. Erweitern Sie die Entität **Standardtitel** und wählen Sie **1:n-Beziehungen** aus.
3. Wählen Sie **Neu** , um eine neue 1:n-Beziehung namens **Standardtitel zu Rollenpreis** zu erstellen. Geben Sie die gewünschten Informationen ein und wählen Sie anschließend **Speichern**.
4. Wiederholen Sie die Schritte 1 - 4, um 1:n-Beziehungen zwischen den Entitäten **Standardtitel** und **Rollenpreisaufschlags** zu erstellen.

In der Vertriebs- und Schätzungsphase des Projekts sind für jeden Standardtitel Schätzungen des Arbeitsaufwands erforderlich, um das Angebot bzw. Projekt zu bewerten. Das bedeutet, dass in Project Service 1:n-Beziehungen von Standardtitel zu jeder dieser Schätzungsentitäten erforderlich sind: 

- **Detailinformationen zur Angebotsposition**
- **Projektvertragsposition**
- **Projektteammitglied**
- **Vorkalkulationsposition**

5. Wiederholen Sie die Schritte 1 - 5, um 1:n-Beziehungen von **Standardtitel** zu **Detailinformationen zur Angebotsposition** , **Projektvertragsposition** , **Projektteammitglied** und **Vorkalkulationsposition** zu erstellen.

  In der Lieferungs- und Rechnungsstellungsphase muss der Preis der von jedem Standardtitel durchgeführten Arbeit in den Projekt-Ist-Werten genau ausgewiesen sein. Dies bedeutet, dass 1:n-Beziehungen von **Standardtitel** zu den Entitäten **Zeiteintrag** , **Tatsächlich** , **Rechnungsposition** und **Erfassungsposition** vorhanden sein müssen.

6. Wiederholen Sie die Schritte 1 - 6, um 1:n-Beziehungen von **Standardtitel** zu den Entitäten **Zeiteintrag** , **Tatsächlich** , **Rechnungsposition** und **Erfassungsposition** zu erstellen.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Einrichten von Standard-Dimensionswerten mithilfe der Zuordnungsfunktionen der Plattform
Für „Zeiteintrag” wäre es hilfreich, wenn das System standardmäßig den Standardtitel für den Zeiteintrag aus „Buchbare Ressource” verwendet, die den Zeiteintrag aufzeichnet. Führen Sie die folgenden Schritte aus, um Feldzuordnungen zur 1:n-Beziehung von **Buchbare Ressource** zu **Zeiteintrag** hinzuzufügen.

1. Wählen Sie im Lösungs-Explorer im linken Navigationsbereich **Entitäten > Standardtitel** aus.
2. Erweitern Sie die Entität **Standardtitel** und wählen Sie **1:n-Beziehungen** aus.
3. Doppelklicken Sie auf **Buchbare Ressource zu Zeiteintrag**. Klicken Sie auf der Seite **Beziehung** und wählen **Feldzuordnungen verwenden**. 
4. Wählen Sie **Neu** , um eine neue Feldzuordnung zwischen dem Feld **Standardtitel** auf der Entität **Buchbare Ressource** und dem Referenzfeld **Standardtitel** auf der Entität **Zeiteintrag** zu erstellen. 

Damit sind die Schemaänderungen abgeschlossen, die für die entitätsbasierten, benutzerdefinierten Dimensionen erforderlich sind.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Hinzufügen benutzerdefinierter Felder zu Formularen, Ansichten und Geschäftsregeln

Nachdem Sie alle erforderlichen Schemaänderungen vorgenommen haben, besteht der nächste Schritt darin, die Felder auf der Benutzeroberfläche sichtbar zu machen, indem Sie sie den Formularen und Ansichten hinzufügen.

1. Öffnen Sie das Formular oder die Ansicht. Wählen Sie im rechten Navigationsbereich das Feld aus und ziehen Sie es auf den Formularcanvas. 
2. Verwenden Sie beim Bearbeiten einer Ansicht den rechten Navigationsbereich, wählen Sie **Felder hinzufügen** und wählen Sie im Dialogfeld **Feldlisten** die Felder aus, die Sie benötigen, und wählen Sie **OK**.

Die folgende Tabelle enthält eine umfassende Liste vorkonfigurierter Formulare und Ansichten nach Entität, die mit den neuen Feldern aktualisiert werden müssen. Wenn Sie irgendwelche zusätzlichen Ansichten oder Formulare in Ihren Anpassungen für diese Entitäten haben, fügen Sie diesen die neuen Felder ebenfalls hinzu.

| Entity        | Formulare, für die das Feld erforderlich ist   |Ansichten, für die das Feld erforderlich ist      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollenpreis|• Informationen |• Preise der aktiven Ressourcenkategorie<br> • Zugeordnete Ansicht: Preis der Ressourcenkategorie|
|  Rollenpreisaufschlag|• Informationen|• Aktiver Rollenpreisaufschlag<br>• Zugeordnete Ansicht: Rollenpreisaufschlag|
|  Detailinformationen zur Angebotsposition|• Projektinformationen<br>• Projektschnellerfassung|• Details zu aktiver Angebotsposition<br>• Kombinierte Angebotspositionsdetails<br>• Zugeordnete Ansicht: Angebotspositionsdetail|
|  Positionsdetail von Projektvertrag|• Projektinformationen<br>• Projektschnellerfassung|• Kombinierte Vertragspositionsdetails<br>• Aktive Vertragspositionsdetails<br>• Zugeordnete Ansicht: Vertragszeilendetails|
|  Projektteammitglied|• Informationen<br>• Neues Formular|• Aktive Projektteammitglieder<br>• Projektteammitglieder<br>• Zugeordnete Ansicht: Projektteammitglieder|
|  Zeiteintrag|• Informationen<br>• Zeiteintrag erstellen|• Meine Zeiteinträge nach Datum<br>• Meine Zeiteinträge für diese Woche<br>• Zeiteinträge zur Genehmigung|
|  Erfassungsposition|• Informationen<br>• Schnellerfassung|• Aktive Erfassungspositionen<br>• Zugeordnete Ansicht: Erfassungsposition|
|  Rechnungsposition|• Informationen<br>• Schnellerfassung|• Aktive Rechnungspositionsdetails<br>• Fakturierbare Rechnungsbuchungen<br>• Zusätzliche Rechnungsbuchungen<br>• Zugeordnete Ansicht: Rechnungspositionsdetail<br>• Nicht-fakturierbare Rechnungsbuchungen|
|  Tatsächlich|• Informationen<br>• Aktive Ist-Werte|• Zugeordnete Ansicht: Ist-Werte|

Je nach Ihrer Definition müssen möglicherweise auch benutzerdefinierte Felder zu Geschäftsregeln hinzugefügt werden. Ein OOB-Beispiel für die Geschäftsregel ist **Bearbeitbarkeit des Zeiteintrags auf Grundlage des Status**. Diese Regel definiert, welche Felder gesperrt werden müssen, wenn sich der Zeiteintrag in einem nicht bearbeitbaren Status wie etwa **Genehmigt** befindet. Fügen Sie dieser Geschäftsregel Felder hinzu, damit die Felder für die Bearbeitung gesperrt sind, wenn sich der Zeiteintrag in einem anderen Status als **Entwurf** oder **Zurückgegeben** befindet.
