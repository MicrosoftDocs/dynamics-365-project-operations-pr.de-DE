---
title: Schätzungen
description: Dieses Thema enthält Informationen zu Vorkalkulationen in Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 978af25fb89feb61e3c6fcfeafa212db034ff5cb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590667"
---
# <a name="estimates"></a>Schätzungen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

In einem projektbasierten Angebot können Sie die Entität „Detail zur Angebotsposition“ verwenden, um die für die Lieferung eines Projekts erforderliche Arbeit abzuschätzen. Sie können diese Schätzung anschließend mit dem Kunden teilen.

Projektbasierte Angebotszeilen müssen keine Detailinformationen zur Angebotsposition enthalten. Alternativ können sie viele Angebotspositionsdetails haben. Angebotspositionsdetails werden verwendet, um Zeit, Ausgaben oder Gebühren zu schätzen. PSA lässt keine Materialschätzungen für Angebotspositionsdetails zu. Diese werden als Transaktionsklassen bezeichnet. Geschätzte Steuerbeträge können ebenfalls für eine Transaktionsklasse eingegeben werden.

Zusätzlich zu den Transaktionsklassen enthalten Angebotspositionsdetails einen Transaktionstyp. PSA unterstützt zwei Transaktionstypen für Angebotspositionsdetails: **Kosten** und **Projektvertrag**.

## <a name="estimate-by-using-a-contract"></a>Schätzung mithilfe eines Vertrags

Wenn Sie beim Erstellen eines projektbasierten Vertrags ein PSA-Angebot verwendet haben, wird die Schätzung, die Sie im Angebot für jede Angebotsposition vorgenommen haben, in den Projektvertrag kopiert. Die Struktur eines Projektvertrags ähnelt der Struktur eines Projektangebots mit Positionen, Positionsdetails und Rechnungszeitplänen.

Schätzungen können direkt in einem Projektvertrag wie in einem Projektangebot vorgenommen werden. Bei einem Projektangebot wird die Schätzung unter Verwendung der Vertragszeilen und Vertragszeilendetails vorgenommen. Vertragspositionsdetails können auch aus einem Projektplan generiert werden, der mithilfe des Bottom-up-Schätzungsansatzes erstellt wurde.

Vertragspositionsdetails können verwendet werden, um Zeit, Kosten oder Gebühren zu schätzen. Geschätzte Steuerbeträge können ebenfalls bei den Vertragszeilendetails eingegeben werden.

PSA lässt keine Materialschätzungen für Vertragszeilendetails zu.

Die Prozesse, die bei einem Projektvertrag unterstützt werden sind Rechnungserstellung und -bestätigung. Rechnungserstellung erstellt einen Entwurf einer projektbasierten Rechnung, die alle nicht fakturierten vertrieblichen Ist-Werte bis zum aktuellen Datum enthält.

Durch die Bestätigung wird der Vertrag schreibgeschützt und sein Status wird von **Entwurf** in **Bestätigt** geändert. Nachdem Sie diese Aktion ausgeführt haben, können Sie sie nicht mehr rückgängig machen. Da es sich bei dieser Aktion um eine permanente Aktion handelt, empfiehlt es sich, den Vertrag im Status **Entwurf** zu belassen.

Die einzigen Unterschiede zwischen Vertragsentwürfen und bestätigten Verträgen sind ihr Status und die Tatsache, dass Vertragsentwürfe bearbeitet werden können, bestätigte Verträge hingegen nicht. Die Rechnungserstellung sowie die Nachverfolgung von Ist-Werten kann sowohl bei Vertragsentwürfen als auch bei bestätigten Verträgen erfolgen.

PSA unterstützt keine Änderungsaufträge bei Verträgen bzw. Projekten.

## <a name="estimating-projects"></a>Einschätzen von Projekten

Sie können Zeit und Ausgaben für Projekte schätzen. PSA lässt keine Material- bzw. Gebührenschätzungen für Projekte zu.

Zeitschätzungen werden generiert, wenn Sie eine Aufgabe erstellen und die Attribute einer allgemeinen Ressource identifizieren, die zur Ausführung der Aufgabe erforderlich ist. Zeitschätzungen werden aus Zeitplanaufgaben generiert. Wenn Sie generische Teammitglieder außerhalb des Zeitplankontexts erstellen, werden keine Zeitschätzungen erstellt.

Ausgabenschätzungen werden in das Raster auf der Seite **Schätzungen** eingegeben.

## <a name="understanding-estimation"></a>Grundlegendes zur Vorkalkulation

Verwenden Sie die folgende Tabelle als Leitfaden zum Verständnis der Geschäftslogik in der Vorkalkulationsphase.

| Szenario                                                                                                                                                                                                                                                                                                                                          | Entitätsdatensatz                                                                                                                                                                                                       | Transaktionstyp | Transaktionsklasse | Weitere Informationen                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Wenn Sie den Umsatzwert der Zeit für ein Angebot schätzen müssen                                                                                                                                                                                                                                                                                    | Datensatz „Detail zur Angebotsposition“ (QLD, Quote Line Detail) wird erstellt                                                                                                                                                                               | Projektvertrag | Time        | Das Feld „Transaktionsursprung“ in der Zeile „QLD“ auf der Verkaufsseite verweist auf die QLD auf der Kostenseite |
|                                                                                                                                                                                                                                                                                     | Ein zweiter QLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern. Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-QLD in die Kosten-QLD.                                                                                                                                                                               | Kosten | Time        | Das Feld „Transaktionsursprung“ in der Zeile „Angebotspositionsdetails“ (QLD) auf der Verkaufsseite verweist auf die QLD auf der Kostenseite |
| Wenn Sie den Umsatzwert der Zeit für einen Vertrag schätzen müssen                                                                                                                                                                                                                                                                                 | Datensatz „Projektvertragsposition“ (CLD, Contract Line Detail) wird erstellt                                                                                                                                                                    | Projektvertrag | Time        | Das Feld „Transaktionsursprung“ in der Zeile „CLD“ auf der Verkaufsseite verweist auf die CLD auf der Kostenseite      |
|                                                                                                                                                                                                                                                                                  | Ein zweiter CLD-Datensatz wird vom System erstellt, um die entsprechenden Kostenwerte zu speichern. Das System kopiert sämtliche Nicht-Geld-Felder aus der Umsatz-CLD in die Kosten-CLD.                                                                                                                                                                    | Kosten | Time        | Das Feld „Transaktionsursprung“ in der Zeile „CLD“ auf der Verkaufsseite verweist auf die CLD auf der Kostenseite      |
| Wenn der Benutzer eine Ressource für eine Projektaufgabe beschreibt                                                                                                                                                                                                                                                                                            | Der Datensatz „Schätzungszeile“ zeigt, dass der Umsatzwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird. Rolle und Organisationseinheiten sind die Preisdimensionen von OOB Project Service | Projektvertrag | Time        |                                                                                   |
|     | Der Datensatz „Schätzungszeile“ zeigt, dass der Kostenwert der Aufgabe beim Erstellen einer Aufgabe mit allen erforderlichen Preisdimensionen generiert wird. Das System kopiert sämtliche Nicht-Geld-Felder aus der Vertriebsvorkalkulationsposition in die Kostenvorkalkulationsposition. Rolle und Organisationseinheit sind die OOB PSA Preisdimensionen sowohl für Kosten als auch für Rechnungssätze.                                                                                                                                                                                                                | Kosten             | Zeit           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Anpassen der Entitäten „Detail zur Angebotsposition“ und „Detail zur Vertragszeile“

Verwenden Sie die Plug-In-Registrierungswerkzeuge PreOperationContractLineDetailUpdate und PreOperationQuoteLineDetailUpdate, wenn Sie den Angebotspositionsdetails ein benutzerdefiniertes Feld hinzugefügt haben und möchten, dass das System den Wert des Felds als Standardwert für die von ihm erstellte zugehörige Kostenposition eingibt. Diese Plug-Ins müssen erneut registriert werden, nachdem das Angebotspositionsdetail oder das Vertragszeilendetail geändert wurde. Befolgen Sie diese Schritte, um den Vorgang abzuschließen.

1. Öffnen Sie PluginRegistrationTool, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.
2. Wählen Sie **Suchen** aus und suchen Sie nach dem zu aktualisierenden Plug-In.

    ![Dialogfeld „Suchstruktur“.](media/basic-guide-19.png)

3. Wählen Sie das Plug-In aus und wählen Sie dann auf der Hauptseite **Auswählen** aus.
4. Wählen Sie den Schritt des zu aktualisierenden Plug-Ins aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.

    ![Auswählen eines Schritts im Plug-In.](media/basic-guide-20.png)

5. Wählen Sie im Dialogfeld **Vorhandenen Schritt aktualisieren** im Feld **Filterattribute** die Schaltfläche mit den Auslassungspunkten (**...**) aus:
 
    ![Dialogfeld „Vorhandenen Schritt aktualisieren“.](media/basic-guide-21.png)

6. Aktivieren Sie im Dialogfeld **Attribute auswählen** Kontrollkästchen für benutzerdefinierte Attribute.

    ![Dialogfeld „Attribute auswählen“.](media/basic-guide-22.png)

7. Wählen Sie **OK** aus, um das Dialogfeld zu schließen, und wählen Sie dann **Schritt aktualisieren** aus.
 
    ![Schaltfläche „Schritt aktualisieren“.](media/basic-guide-23.png)

8. Wiederholen Sie die Schritte 1 bis 7 für das zweite Plug-In.
9. Schließen Sie das PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
