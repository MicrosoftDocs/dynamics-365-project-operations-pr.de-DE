---
title: Produkte
description: Dieses Thema enthält Informationen zum Produktkatalog, mit denen Sie Kunden Informationen zu den Produkten und Preisen Ihres Unternehmens bereitstellen können.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898710"
---
# <a name="products"></a>Produkte

_**Gilt für:** Projektvorgänge für Ressourcen/nicht vorrätige Szenarien, Lite-Bereitstellung – Abwicklung der Proforma-Rechnungsstellung_

Produkte sind das Rückgrat Ihres Unternehmens. Der Produktkatalog in Dynamics 365 Sales Professional ist eine Sammlung von Produkten mit ihren Preisinformationen. Machen Sie es einfacher für Ihre Vertriebsmitarbeiter, ihre Verkäufe zu steigern, indem Sie schnell einen Produktkatalog erstellen.

## <a name="add-a-product"></a>Hinzufügen eines Produkts

1.  Stellen Sie sicher, dass Sie über die Rolle „Vertriebsmanager – Professional“ oder „Systemadministrator“ verfügen, damit Sie Produkte in Dynamics 365 Sales Professional hinzufügen können.
2.  Wählen Sie in der Siteübersicht unter **Einrichten** die Option **Produkte** aus.
3.  Wählen Sie **Produkt hinzufügen** und geben Sie die folgenden Informationen ein:

    -  **Name**
    -  **Produkt-ID**
    -  **Übergeordnetes Element**: Wählen Sie eine übergeordnete Produktfamilie für das Produktpaket aus. Wenn Sie ein untergeordnetes Produkt in einer Produktfamilie erstellen, wird der Name der übergeordneten Produktfamilie hier aufgefüllt. Dieser kann nicht geändert werden, nachdem der Datensatz gespeichert ist.
    -  **Gültig ab**/**Gültig bis**: Definieren Sie die Periode, während der das Produktpaket gültig ist, indem sie ein Datum **Gültig ab** und **Gültig bis** auswählen.
    -  **Einheitengruppe**: Wählen Sie eine Einheitengruppe aus. Eine Einheitengruppe ist eine Sammlung verschiedener Einheiten, in der ein Produkt vertrieben wird, und es definiert, wie individuelle Elemente in größere Mengen gruppiert werden. Wenn Sie z. B. Saaten als Produkt hinzufügen, haben Sie möglicherweise eine Einheitengruppe „Saaten” erstellt, und deren primäre Einheit wird als „Paket” definiert.
    -  **Standardseinheit**: Wählen Sie die häufigste Einheit aus, in der das Produkt berechnet wird. Einheiten sind die Mengen oder die Maße, in denen Sie Ihre Produkte verkaufen. Wenn Sie zum Beispiel Saat als Produkt hinzufügen, können Sie sie in Paketen, Kästen oder in Paletten verkaufen. Jedes davon wird eine Einheit des Produkts. Wenn Saaten meist in Paketen verkauft werden, wählen Sie dies als Einheit aus.
    -  **Standardpreisliste**Bei einem neuen Produkt ist dieses Feld schreibgeschützt. Bevor Sie eine Standardpreisliste auswählen können, müssen Sie alle Pflichtfelder ausfüllen und den Datensatz speichern. Die Standardpreisliste ist zwar nicht erforderlich, es kann sich jedoch als nützlich erweisen, nach dem Speichern des Produktdatensatzes für jedes Produkt eine Standardpreisliste festzulegen. Falls dann ein Kundendatensatz keine Preisliste enthält, kann der Vertrieb die Standardpreisliste zum Erstellen von Angeboten, Aufträgen oder Rechnungen verwenden.
    -  **Dezimalzahlen unterstützt**: Geben Sie eine ganze Zahl zwischen 0 und 5 ein. Wenn das Produkt nicht in Teilmengen unterteilt werden kann, geben Sie 0 ein. Die Anzahl der Stellen des Felds **Menge** im Angebots-, Auftrags- oder Rechnungsproduktdatensatz wird mit dem Wert in diesem Feld verglichen, wenn dem Produkt keine Preisliste zugeordnet ist.
    -  **Thema**: Sie können dieses Produkt einem Betreff zuordnen. Mithilfe von Betreffen können Sie die Produkte in Kategorien unterteilen und Berichte filtern.

4.  Wählen Sie **Speichern** aus.
5.  Auf der Registerkarte **Weitere Details** wählen Sie im Abschnitt **Preislistenelemente** das Symbol **Weitere Befehle** und dann **Neues Preislistenelement hinzufügen** aus.
7.  Auf der Registerkarte **Weitere Details** im Abschnitt **Produktbeziehung** wählen Sie das Symbol **Weitere Befehle** und dann **Neue Produktbeziehung hinzufügen** aus.
8.  Geben Sie im Formular **Neue Produktbeziehung** die folgenden Details ein, und wählen Sie in der Befehlsleiste die Option **Speichern und schließen** aus:

    -   **Verwandte Produkte**: Wählen Sie ein Produkt aus, das Sie als verknüpftes Produkt dem bestehenden Produktdatensatz, an dem Sie arbeiten, hinzufügen möchten.
    -   **Vertriebsbezugstyp**: Wählen Sie aus, ob Sie das Produkt als Upsell, Cross-Sell, Zubehör oder Ersatzprodukt hinzufügen möchten.
    -   **Richtung**: Wählen Sie aus, ob die Beziehung zwischen den Produkten unidirektional oder bidirektional ist. Wenn Sie unidirektional auswählen, wird das Produkt, das Sie in **Zugehöriges Produkt** auswählen, als Empfehlung für das bestehende Produkt ausgewählt, nicht aber umgekehrt.

9.  Wählen Sie im Produktformular **Speichern** aus.

## <a name="import-products"></a>Produkte importieren

Sie können auch Importvorlagen verwenden, um Massenproduktdaten in Dynamics 365 Sales zu übertragen.

## <a name="revise-a-product"></a>Ein Produkt überarbeiten

Halten Sie die Produktbestandsliste aktualisiert, indem Sie bei Bedarf schnell Eigenschaften für die Produkte überarbeiten und die Informationen neu veröffentlichen, damit Ihre Handelsvertreter die neuesten Änderungen am Bestand anzeigen können.

1.  Stellen Sie sicher, dass Sie über eine der folgenden Sicherheitsrollen oder entsprechende Berechtigungen verfügen: Systemadministrator, Systemanpasser, Vertriebsmanager, Vertriebsleiter, Marketingleiter oder Vorstandsvorsitzender.
2.  Wählen Sie in der Siteübersicht die Option **Produkte** aus.
3.  Öffnen Sie ein aktives Produkt, das Sie ändern möchten, und wählen Sie in der Befehlsleiste **Überarbeiten** aus.
4.  Wählen Sie im Dialogfeld **Überarbeitung bestätigen** die Option **Bestätigen**. Hiermit wird der Produktstatus auf **In Überarbeitung** geändert.
5.  Nachdem Sie Änderungen vorgenommen haben, wählen Sie in der Befehlsleiste **Veröffentlichen** aus.

    > [!TIP]
    > Um die Änderungen wieder rückgängig zu machen und mit der letzten aktiven Version des Produkts fortzufahren, wählen Sie **Wiederherstellen** aus. Hiermit wird der Status der Produkts zu **Aktiv** zurückgesetzt.

## <a name="clone-a-product"></a>Ein Produkt klonen 

Wenn Sie ein neues Produkt erstellen, können Sie Zeit sparen, indem Sie ein vorhandenes klonen. Dadurch wird eine Kopie des ursprünglichen Datensatzes mit allen Details außer dem Namen und der ID erstellt.

1.  Stellen Sie sicher, dass Sie über eine der folgenden Sicherheitsrollen oder entsprechende Berechtigungen verfügen: Systemadministrator, Systemanpasser, Vertriebsmanager, Vertriebsleiter, Marketingleiter oder Vorstandsvorsitzender.
2.  Wählen Sie in der Siteübersicht die Option **Produkte** aus.
3.  Wählen Sie einen Produktdatensatz aus, den Sie klonen möchten, und wählen Sie in der Befehlsleiste **Klonen** aus. Ein Bestätigungsdialogfeld wird angezeigt.
4.  Wählen Sie **Bestätigen** aus.

Ein neuer Produktdatensatz wird geöffnet und enthält dieselben Informationen wie die ursprüngliche, außer dem Namen und der ID.

## <a name="retire-a-product"></a>Ein Produkt zurückziehen 

Wenn Ihre Organisation en Produkt nicht mehr verkauft, ziehen Sie es zurück, sodass das Produkt nicht mehr für die Handelsvertreter verfügbar ist.

1.  Stellen Sie sicher, dass Sie über die Rolle „Systemadministrator“ oder „Sales Professional-Manager“ bzw. entsprechende Berechtigungen verfügen.
2.  Wählen Sie in der Siteübersicht die Option **Produkte** aus.
3.  Öffnen Sie ein aktives Produkt, das Sie zurückziehen möchten, und wählen Sie in der Befehlsleiste **Zurückziehen** aus.
4.  Wählen Sie im Dialogfeld **Zurückziehen bestätigen** die Option **Bestätigen**.


## <a name="delete-a-product"></a>Ein Produkt löschen

Um ein Produkt nihct mehr zu verkaufen, löschen Sie es.

> [!IMPORTANT]
> Gelöschte Datensätze können nicht wiederhergestellt werden.

1.  Stellen Sie sicher, dass Sie über die Rolle „Systemadministrator“ oder „Sales Professional-Manager“ bzw. entsprechende Berechtigungen verfügen.
2.  Wählen Sie in der Siteübersicht die Option **Produkte** aus.
3.  Wählen Sie einen Produktdatensatz aus, den Sie löschen möchten, und wählen Sie in der Befehlsleiste **Löschen** aus.
4.  Wählen Sie im Dialogfeld **Löschen bestätigen** die Option **Weiter** aus.
 
 ## <a name="quantity-factors-for-products"></a>Mengenfaktoren für Produkte

Mengenfaktoren unterstützen den Verkauf von Abonnement-basierten Produkten. Für Abonnement-basierte Produkte wird die Menge im Angebot oder in der Projektvertragszeile als Anzahl der Benutzermonate angegeben.

Normalerweise wird der Preis der Abonnement-Software im Katalog als Preis pro Benutzer pro Monat gespeichert. Sie können jedoch auch andere Zeitbeschreibungen verwenden. Während des Vertriebsprozesses wird der Preis in der Angebotsposition in der Regel als Preis pro Benutzer pro Monat angegeben, der vom IT-Vertriebsmitarbeiter verhandelt und diskontiert wurde. Jedes Geschäft umfasst eine andere Anzahl der Benutzer und eine andere Anzahl der Abonnementmonate. Die Menge, die verwendet wird, um die Menge der Angebotszeile zu berechnen, ergibt sich aus der Anzahl der Benutzer und der Anzahl der Abonnementmonate.

Mengenfaktoren basieren auf den Produktattributen. Wenn Sie bestimmte Eigenschaften für ein Produkt konfigurieren, können Sie eine Teilmenge dieser Eigenschaften oder alle Eigenschaften als Mengenfaktoren markieren.

Das System stellt sicher, dass nur numerische Eigenschaften oder Produkteigenschaften mit einem numerischen Datentyp als Mengenfaktoren gekennzeichnet werden. Wenn einem Produkt, dass für Mengenfaktoren konfiguriert wurde, eine Angebotsposition hinzugefügt wird, ist das Feld **Menge** in der Angebotsposition ein schreibgeschütztes Feld. Nachdem Sie Werte für Produkteigenschaften eingegeben haben, die Mengenfaktoren sind, wird die Menge der Angebotsposition berechnet.

Zum Beispiel, wenn es die folgenden Eigenschaften gibt: 

- **Anzahl der Benutzer**: Die Anzahl der Benutzer 
- **Anzahl der Monate**: Die Anzahl der Abonnementmonate
- **Produkt-SKU** 

Die Eigenschaften **Anzahl der Benutzer** und **Anzahl der Monate** können durch Bearbeitung der Produktposition als Mengenfaktoren gekennzeichnet werden. 
