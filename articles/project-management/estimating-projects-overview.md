---
title: Konzepte für finanzielle Vorkalkulationen
description: Dieses Thema enthält Informationen zu finanzielle Vorkalkulationen für Projekte in Project Operations.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a251be995abddba04cee689714d0a8f4e9d9e7d7
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701735"
---
# <a name="financial-estimation-concepts"></a>Konzepte für finanzielle Vorkalkulationen

_**Gilt für:** Project Operations für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

In Dynamics 365 Project Operations können Sie Ihre Projekte in zwei Schritten finanziell abschätzen: 
1. Während der Vorverkaufsphase, bevor der Deal gewonnen wird. 
2. Während der Ausführungsphase nach dem Erstellen des Projektvertrags. 

Sie können eine finanzielle Vorkalkulation für projektbasierte Arbeit auf einer der folgenden 3 Seiten erstellen:
- Auf der Seite **Angebotszeile** unter Verwendung der Angebotszeilendetails.  
- Auf der Seite **Projektvertragszeile** unter Verwendung der Vertragszeilendetails. 
- Auf der Seite **Projekt** mit den Registerkartenseiten **Aufgaben** oder **Ausgabenschätzungen**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Verwenden Sie ein Projektangebot, um einen Kostenvoranschlag zu erstellen
In einem projektbasierten Angebot können Sie die Entität **Detail zur Angebotsposition** verwenden, um die für die Lieferung eines Projekts erforderliche Arbeit abzuschätzen. Sie können diese Schätzung anschließend mit dem Kunden teilen.

Projektbasierte Angebotszeilen müssen Null bis viele Angebotsposition enthalten. Angebotspositionsdetails werden verwendet, um Zeit, Ausgaben oder Gebühren zu schätzen. Microsoft Dynamics 365 Project Operations lässt keine Materialvorkalkulationen für Angebotspositionsdetails zu. Diese werden als Transaktionsklassen bezeichnet. Geschätzte Steuerbeträge können ebenfalls für eine Transaktionsklasse eingegeben werden.

Zusätzlich zu den Transaktionsklassen enthalten Angebotspositionsdetails einen Transaktionstyp. Zwei Transaktionstypen werden für Angebotspositionsdetails unterstützt: **Kosten** und **Projektvertrag**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Verwenden Sie einen Projektvertrag, um einen Kostenvoranschlag zu erstellen

Wenn Sie beim Erstellen eines projektbasierten Vertrags ein Angebot verwendet haben, wird die Schätzung, die Sie im Angebot für jede Angebotsposition vorgenommen haben, in den Projektvertrag kopiert. Die Struktur eines Projektvertrags ähnelt der Struktur eines Projektangebots mit Positionen, Positionsdetails und Rechnungszeitplänen.

Schätzungen können direkt in einem Projektvertrag wie in einem Projektangebot vorgenommen werden. Bei einem Projektangebot wird die Schätzung unter Verwendung der Vertragszeilen und Vertragszeilendetails vorgenommen. Vertragszeilendetails können auch aus einem Projektplan erstellt wurden, der mithilfe des Bottom-up-Schätzungsansatzes erstellt wurde.

Vertragszeilendetails können zur Schätzung von Zeit, Ausgaben oder Gebühren verwendet werden. Geschätzte Steuerbeträge können ebenfalls bei den Vertragszeilendetails eingegeben werden.

Materialvorkalkulationen für Vertragszeilendetails sind nicht erlaubt.

## <a name="use-a-project-to-create-an-estimate"></a>Verwenden Sie ein Projekt, um einen Kostenvoranschlag zu erstellen 

Sie können Zeit und Ausgaben für Projekte schätzen. Project Operations unterstützt keine Schätzungen von Materialien oder Gebühren für Projekte.

Zeitvorkalkulationen werden generiert, wenn Sie eine Aufgabe erstellen und die Attribute einer allgemeinen Ressource identifizieren, die zur Ausführung der Aufgabe erforderlich ist. Zeitvorkalkulationen werden aus Zeitplanaufgaben generiert. Zeitvorkalkulationen werden nicht erstellt, wenn Sie allgemeine Teammitglieder außerhalb des Zeitplans erstellen.

Ausgabenschätzungen werden in das Raster auf der Seite **Ausgabenschätzungen** eingegeben.

Das Erstellen einer Schätzung für ein Projekt wird als bewährte Methode angesehen, da Sie für jede Aufgabe im Projektplan detaillierte Bottom-up-Schätzungen für Arbeit oder Zeit und Kosten erstellen können. Mit dieser detaillierten Schätzung können Sie dann Schätzungen für jede Angebotszeile erstellen und ein glaubwürdigeres Angebot für den Kunden erstellen. Wenn Sie mithilfe des Projektplans eine detaillierte Schätzung in die Angebotszeile importieren oder erstellen, importiert Project Operations die Verkaufswerte und die Kostenwerte dieser Schätzungen. Nach dem Import können Sie die Rentabilitäts-, Margen- und Durchführbarkeitsmetriken im Projektangebot anzeigen.

## <a name="understanding-estimates"></a>Grundlegendes zur Vorkalkulation

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

Verwenden Sie die Plug-In-Registrierungswerkzeuge **PreOperationContractLineDetailUpdate** und **PreOperationQuoteLineDetailUpdate**, wenn Sie den Angebotspositionsdetails ein benutzerdefiniertes Feld hinzugefügt haben und möchten, dass das System den Wert des Felds als Standardwert für die von ihm erstellte zugehörige Kostenposition eingibt. Diese Plug-Ins müssen erneut registriert werden, nachdem das Angebotspositionsdetail oder das Vertragszeilendetail geändert wurde. Befolgen Sie diese Schritte, um den Vorgang abzuschließen.

1. Öffnen Sie PluginRegistrationTool, und stellen Sie eine Verbindung mit Ihrer Online-Instanz her.
2. Wählen Sie **Suchen** aus und suchen Sie nach dem zu aktualisierenden Plug-In.
3. Wählen Sie das Plug-In aus und wählen Sie dann auf der Hauptseite **Auswählen**.
4. Wählen Sie den Schritt des zu aktualisierenden Plug-Ins aus, klicken Sie mit der rechten Maustaste, und wählen Sie dann **Aktualisieren** aus.
5. Wählen Sie im Dialogfeld **Vorhandenen Schritt aktualisieren** im Feld **Filterattribute** die Schaltfläche mit den Auslassungspunkten (**...**) aus:
6. Aktivieren Sie im Dialogfeld **Attribute auswählen** Kontrollkästchen für benutzerdefinierte Attribute.
7. Wählen Sie **OK** aus, um das Dialogfeld zu schließen, und wählen Sie dann **Schritt aktualisieren** aus.
8. Wiederholen Sie die Schritte 1 bis 7 für das zweite Plug-In.
9. Schließen Sie das **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
