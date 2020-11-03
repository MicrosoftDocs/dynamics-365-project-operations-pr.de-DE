---
title: Schätzungen in einer Angebotsposition erstellen
description: Dieses Thema enthält Informationen zum Erstellen einer Schätzung in einer Angebotszeile für ein Projekt.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f949c639530aecf9f7368925208ab12b68d2062e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4076552"
---
# <a name="create-estimates-on-a-quote-line"></a>Schätzungen in einer Angebotsposition erstellen

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In einem projektbasierten Angebot können Sie die Entität „Detail zur Angebotsposition” verwenden, um die für die Lieferung eines Projekts erforderliche Arbeit abzuschätzen. Sie können diese Schätzung anschließend mit dem Kunden teilen.

Projektbasierte Angebotszeilen müssen keine Detailinformationen zur Angebotsposition enthalten. Alternativ können sie viele Angebotspositionsdetails haben. Angebotspositionsdetails werden verwendet, um Zeit, Ausgaben oder Gebühren zu schätzen. Dynamics 365 Project Operations lässt keine Materialschätzungen für Angebotspositionsdetails zu. Diese werden als Transaktionsklassen bezeichnet. Geschätzte Steuerbeträge können ebenfalls für eine Transaktionsklasse eingegeben werden.

Zusätzlich zu den Transaktionsklassen enthalten Angebotspositionsdetails einen Transaktionstyp. Es gibt zwei Transaktionstypen für Angebotspositionsdetails: **Kosten** und **Projektvertrag**.

## <a name="estimate-by-using-a-contract"></a>Schätzung mithilfe eines Vertrags

Wenn Sie beim Erstellen eines projektbasierten Vertrags ein Project Operations Angebot verwendet haben, wird die Schätzung, die Sie im Angebot für jede Angebotsposition vorgenommen haben, in den Projektvertrag kopiert. Die Struktur eines Projektvertrags ähnelt der Struktur eines Projektangebots mit Positionen, Positionsdetails und Rechnungszeitplänen.

Schätzungen können direkt in einem Projektvertrag wie in einem Projektangebot vorgenommen werden. Bei einem Projektangebot wird die Schätzung unter Verwendung der Vertragspositionen und Vertragspositionsdetails vorgenommen. Vertragspositionsdetails können auch aus einem Projektplan erstellt wurden, der mithilfe des Bottom-up-Schätzungsansatzes erstellt wurde.

Vertragspositionsdetails können zur Schätzung von Zeit, Ausgaben oder Gebühren verwendet werden. Geschätzte Steuerbeträge können ebenfalls bei den Vertragszeilendetails eingegeben werden.

Materialschätzungen für Vertragszeilendetails sind nicht erlaubt.

Die Prozesse, die bei einem Projektvertrag unterstützt werden sind Rechnungserstellung und -bestätigung. Rechnungserstellung erstellt einen Entwurf einer projektbasierten Rechnung, die alle nicht fakturierten vertrieblichen Ist-Werte bis zum aktuellen Datum enthält.

Durch die Bestätigung wird der Vertrag schreibgeschützt und der Status von **Entwurf** in **Bestätigt** geändert. Nachdem Sie diese Aktion ausgeführt haben, können Sie sie nicht mehr rückgängig machen. Da es sich bei dieser Aktion um eine permanente Aktion handelt, empfiehlt es sich, den Vertrag im Status **Entwurf** zu belassen.

Die einzigen Unterschiede zwischen Vertragsentwürfen und bestätigten Verträgen sind ihr Status und die Tatsache, dass Vertragsentwürfe bearbeitet werden können, bestätigte Verträge hingegen nicht. Die Rechnungserstellung sowie die Nachverfolgung von Ist-Werten kann sowohl bei Vertragsentwürfen als auch bei bestätigten Verträgen erfolgen.

Änderungsaufträge bei Verträgen bzw. Projekten werden nicht unterstützt.

## <a name="estimating-projects"></a>Einschätzen von Projekten

Sie können Zeit und Kosten für Projekte schätzen, jedoch keine Materialien oder Gebühren.

Zeitschätzungen werden generiert, wenn Sie eine Aufgabe erstellen und die Attribute einer allgemeinen Ressource identifizieren, die zur Ausführung der Aufgabe erforderlich ist. Zeitschätzungen werden aus Zeitplanaufgaben generiert. Zeitschätzungen werden nicht erstellt, wenn Sie allgemeine Teammitglieder außerhalb des Zeitplans erstellen.

Ausgabenschätzungen werden in das Raster auf der Seite **Schätzungen** eingegeben.

## <a name="understand-estimation"></a>Schätzungen verstehen

Verwenden Sie die folgende Tabelle als Leitfaden zum Verständnis der Geschäftslogik in der Vorkalkulationsphase.

| Szenario                                                                                                                                                                                                                                                                                                                                          | Entitätsdatensatz                                                                                                                                                                                                       | Transaktionstyp | Transaktionsklasse | Weitere Informationen                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Wenn Sie den Umsatzwert der Zeit für ein Angebot schätzen müssen                                                                                                                                                                                                                                                                                    | Datensatz „Detail zur Angebotsposition” (QLD, Quote Line Detail) wird erstellt                                                                                                                                                                               | Projektvertrag | Time        | Das Feld „Transaktionsursprung” in der Zeile „QLD” auf der Verkaufsseite verweist auf die QLD auf der Kostenseite |
|                                                                                                                                                                                                                                                                                     | Ein zweiter QLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern. Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-QLD in die Kosten-QLD.                                                                                                                                                                               | Kosten | Time        | Das Feld „Transaktionsursprung” in der Zeile „Angebotspositionsdetails” (QLD) auf der Verkaufsseite verweist auf die QLD auf der Kostenseite |
| Wenn Sie den Umsatzwert der Zeit für einen Vertrag schätzen müssen                                                                                                                                                                                                                                                                                 | Datensatz „Projektvertragsposition” (CLD, Contract Line Detail) wird erstellt                                                                                                                                                                    | Projektvertrag | Time        | Das Feld „Transaktionsursprung” in der Zeile „CLD” auf der Verkaufsseite verweist auf die CLD auf der Kostenseite      |
|                                                                                                                                                                                                                                                                                  | Ein zweiter CLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern. Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-CLD in die Kosten-CLD.                                                                                                                                                                    | Kosten | Time        | Das Feld „Transaktionsursprung” in der Zeile „CLD” auf der Verkaufsseite verweist auf die CLD auf der Kostenseite      |
| Wenn der Benutzer eine Ressource für eine Projektaufgabe beschreibt                                                                                                                                                                                                                                                                                            | Der Datensatz „Schätzungszeile” zeigt, dass der Umsatzwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird. Rolle und Organisationseinheiten sind die Preisdimensionen | Projektvertrag | Zeit        |                                                                                   |
|     | Der Datensatz „Schätzungszeile” zeigt, dass der Kostenwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird. Das System kopiert sämtliche Nicht-Geld-Felder aus der Vertriebsvorkalkulationsposition in die Kostenvorkalkulationsposition. Rolle und Organisationseinheit sind die Preisdimensionen sowohl für Kosten als auch für Rechnungssätze.                                                                                                                                                                                                                | Kosten             | Zeit           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Anpassen der Entitäten Detail zur Angebotsposition und Detail zur Vertragszeile

Verwenden Sie die Plug-In-Registrierungswerkzeuge PreOperationContractLineDetailUpdate und PreOperationQuoteLineDetailUpdate, wenn Sie den Angebotspositionsdetails ein benutzerdefiniertes Feld hinzugefügt haben und möchten, dass das System den Wert des Felds als Standardwert für die von ihm erstellte zugehörige Kostenposition eingibt. Diese Plug-Ins müssen erneut registriert werden, nachdem das Angebotspositionsdetail oder das Vertragspositionsdetail geändert wurde. Befolgen Sie diese Schritte, um den Vorgang abzuschließen.

1. Öffnen Sie PluginRegistrationTool, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.
2. Wählen Sie **Suchen** aus und suchen Sie nach dem zu aktualisierenden Plug-In.
3. Wählen Sie das Plug-In aus und wählen Sie dann auf der Hauptseite **Auswählen** aus.
4. Wählen Sie den Schritt des zu aktualisierenden Plug-Ins aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.
5. Wählen Sie im Dialogfeld **Vorhandenen Schritt aktualisieren** im Feld **Filterattribute** die Schaltfläche mit den Auslassungspunkten ( **...** ) aus:
6. Aktivieren Sie im Dialogfeld **Attribute auswählen** Kontrollkästchen für benutzerdefinierte Attribute.
7. Wählen Sie **OK** aus, um das Dialogfeld zu schließen, und wählen Sie dann **Schritt aktualisieren** aus.
8. Wiederholen Sie die Schritte 1 bis 7 für das zweite Plug-In.
9. Schließen Sie das PluginRegistrationTool.
